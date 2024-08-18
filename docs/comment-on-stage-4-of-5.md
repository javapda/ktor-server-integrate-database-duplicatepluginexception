# comment-on-stage-4-of-5 | [readme](../readme.md)

Bounty-Lovers Welcome

In this problem "a tutorial" is mentioned - https://ktor.io/docs/interactive-website-add-persistence.html (transformed to https://ktor.io/docs/server-integrate-database.html)

There is a section call [Add automated unit tests](https://ktor.io/docs/server-integrate-database.html#add-automated-tests) - when I go to run the test I get "DuplicatePluginException".

I created a git repository called hyperskill-mentioned-ktor-database-integration-tutorial-fails located HERE.


I began following the tutorial and things were fine until

If anyone out there has run through the Tutorial (https://ktor.io/docs/interactive-website-add-persistence.html) mentioned in this Stage 4, did you experience a "DuplicatePluginException"?

it appears to be due to the:
application {
val repository = FakeTaskRepository()
configureSerialization(repository)    // <==== 2nd load of ContentNegotiation
configureRouting()
}
---------------------------------------

Please make sure that you use unique name for the plugin and don't install it twice. Conflicting application plugin is already installed with the same key as `ContentNegotiation`
io.ktor.server.application.DuplicatePluginException: Please make sure that you use unique name for the plugin and don't install it twice. Conflicting application plugin is already installed with the same key as `ContentNegotiation`
at io.ktor.server.application.ApplicationPluginKt.install(ApplicationPlugin.kt:114)
at example.com.plugins.SerializationKt.configureSerialization(Serialization.kt:11)
