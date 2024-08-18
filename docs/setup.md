# setup | [readme](../readme.md)

1. go to [ktor starter](https://start.ktor.io/) and create a project with the following:
   * configuration
     ```
        Build system: Gradle Kotlin
        Use version catalog: Yes
        Ktor version: 2.3.12
        Engine: Netty
        Configuration: HOCON file
     ```
   * [plugins - 2.3.12](https://api.ktor.io/older/2.3.12/) 
     * [Routing](https://ktor.io/docs/server-routing.html)
     * [Content Negotiation](https://api.ktor.io/older/2.3.12/ktor-server/ktor-server-plugins/ktor-server-content-negotiation/io.ktor.server.plugins.contentnegotiation/-content-negotiation.html)
     * [Kotlinx.serialization](https://api.ktor.io/older/2.3.12/ktor-shared/ktor-serialization/ktor-serialization-kotlinx/index.html) | [docs](https://ktor.io/docs/serialization.html)
     * Static Content | [serving static content](https://ktor.io/docs/server-static-content.html)
     * [Status Pages](https://api.ktor.io/older/2.3.12/ktor-server/ktor-server-plugins/ktor-server-status-pages/index.html)
     * [Exposed](https://github.com/JetBrains/Exposed)
     * [Postgres](https://github.com/pgjdbc)
2. run `.\gradlew.bat build` to ensure everything is working
3. load in IntelliJ IDEA:  `idea .`
4. run the test :  [ApplicationTest](../src/test/kotlin/example/com/ApplicationTest.kt)
   *  .\gradlew.bat test --tests *ApplicationTest


## [versions](../gradle/libs.versions.toml) 
* ktor-version = "2.3.12"
* kotlin-version = "2.0.10"
* logback-version = "1.4.14"

## notes
* when you add kotlinx.serialization, you automatically get Routing, Content Negotiation
* when you add Content Negotiation plugin, you automatically get Routing
* when you add Static Content plugin, you automatically get Routing
* when you add Status Pages plugin, you automatically get Routing
* when you add Exposed plugin, you automatically get Routing, Content Negotiation, kotlinx.serialization 
* when you add Postgres plugin, you automatically get Routing, Content Negotiation, kotlinx.serialization
---
* w: file:///C:/Users/javap/ktor-server-integrate-database-duplicatepluginexception/src/main/kotlin/example/com/plugins/Routing.kt:21:9 '@Deprecated(...) fun Route.static(remotePath: String, configure: Route.() -> Unit): Route' is deprecated. Please use `staticFiles` or `staticResources` instead.
* w: file:///C:/Users/javap/ktor-server-integrate-database-duplicatepluginexception/src/main/kotlin/example/com/plugins/Routing.kt:22:13 '@Deprecated(...) fun Route.resources(resourcePackage: String? = ...): Unit' is deprecated. Please use `staticResources` instead.
