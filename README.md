# What is Orchard Core CMS and what can this modular framework do for You?

## The Modular CMS Framework

# [YouTube Video](https://youtu.be/GZDJfIyB4Vs)

[![OrchardSkillsYouTubeThumbNailWhatIsOrchardCore](https://user-images.githubusercontent.com/59172485/90696852-4f061280-e23a-11ea-9e08-b96e9cee0a28.png)](https://youtu.be/GZDJfIyB4Vs)

# Introduction

Orchard Core is a redevelopment of [Orchard CMS](https://github.com/OrchardCMS/Orchard) on [ASP.NET Core](https://docs.microsoft.com/aspnet/core/). It is an open-source community-based application framework for building modular, multi-tenant applications. Orchard Core also includes Orchard Core CMS, a Web Content Management System (CMS), that is built on top of the Orchard Core Framework. It allows you to build full websites, or headless websites using GraphQL. 

Orchard Core consists of two different targets:

- **Orchard Core Framework**: An application framework for building **modular**, **multi-tenant** applications on ASP.NET Core.
- **Orchard Core CMS**: A Web Content Management System (CMS) built on top of the Orchard Core Framework.

It’s important to note the differences between the framework and the CMS. Some developers who want to develop SaaS applications will only be interested in the modular framework. Others who want to build administrable websites will focus on the CMS and build modules to enhance their sites or the whole ecosystem.

## Building Software as a Service (SaaS) solutions with the Orchard Core Framework

It’s very important to understand the Orchard Core Framework is distributed independently from the CMS on nuget.org. You can  build **modular** and **multi-tenant** applications using just Orchard Core Framework without any of the CMS specific features.

One of our goals is to enable community-based ecosystems of hosted applications which can be extended with modules, like e-commerce systems, blog engines and more. The Orchard Core Framework enables a modular environment that allows different teams to work on separate parts of an application and make components reusable across projects.

## Building Website with Orchard Core CMS

Orchard Core CMS is a complete rewrite of Orchard CMS on ASP.NET Core. It’s not just a port as we wanted to improve the performance drastically and align as close as possible to the development models of ASP.NET Core.

- **Performance**. This might the most obvious change when you start using Orchard Core CMS. It’s extremely fast for a CMS. So fast that we haven’t even cared about working on an output cache module. To give you an idea, without caching Orchard Core CMS is around 20 times faster than the previous version.

- **Portable**. You can now develop and deploy Orchard Core CMS on Windows, Linux and macOS. We also have Docker images ready for use.

- **Document database** abstraction. Orchard Core CMS still requires a relational database, and is compatible with SQL Server, MySQL, PostgreSQL and SQLite, but it’s now using a document abstraction (YesSql) that provides a document database API to store and query documents. This is a much better approach for CMS systems and helps performance significantly.

- **NuGet Packages**. Modules and themes are now shared as NuGet packages. Creating a new website with Orchard Core CMS is actually as simple as referencing a single meta package from the NuGet gallery. It also means that updating to a newer version only involves updating the version number of this package.

- **Live preview**. When editing a content item, you can now see live how it will look like on your site, even before saving your content. And it also works for templates, where you can browse any page to inspect the impact of a change on templates as you type it.

- **Liquid templates support**. Editors can safely change the HTML templates with the Liquid template language. It was chosen as it’s both very well documented (Jekyll, Shopify, …) and secure.

- **Custom queries**. We wanted to provide a way for developers to access all their data as simply as possible. We created a module that lets you create custom ad-hoc SQL and Lucene queries that can be re-used to display custom content, or exposed as API endpoints. You can use it to create efficient queries, or expose your data to SPA applications.

- **Deployment plans**. Deployment plans are scripts that can contain content and metadata to build a website. You can now include binary files, and even use them to deploy your sites remotely from a staging to a production environment for instance. They can also be part of NuGet Packages, allowing you to ship predefined websites.

- **Scalability**. Because Orchard Core is a multi-tenant system, you can host as many websites as you want with a single deployment. A typical cloud machine can then host thousands of sites in parallel, with database, content, theme and user isolation.

- **Workflows**. Create content approval workflows, react to webhooks, take actions when forms are submitted, and any other process you'd like to implement with a user friendly UI.

- **GraphQL**. We provide a very flexible GraphQL API, such that any authorized external application can reuse your content, like SPA applications or static site generators.

### Different website building strategies

Orchard Core CMS supports all major site building strategies:

- **Full CMS**. In this mode, the website uses a theme and templates to render your content, aiming for little to no custom development at all.
- **Decoupled CMS**. The site starts off blank, apart from the content management back-end. You create all the templates you need with Razor Pages or MVC actions and access your content via the content services. 
- **Headless CMS**. The site only manages the content, and you create a separate application that will fetch the managed content using GraphQL or REST APIs.



# Releases

Orchard Core's first GitHub commit was on November 19, 2014.

# Orchard Core 1.0.0-pre-alpha

Release dates:  November 19, 2014 - January 17, 2017

## Enhancements

- Setup
- Multi-tenancy
- Theming
- Shapes
- Document database with migrations
- Declarative dependency injection
- Navigation API
- Event bus
- Authentication & Authorization
- Content Items API
- Content Parts and Content Fields
- Content Types module
- Managing content types and settings
- List module
- Modules support
- Deferred tasks
- Resource manager
- Placement files
- Background tasks
- Recipes



# Orchard Core 1.0.0-alpha

Release date: January 17, 2017

## Enhancements

- Autoroute
- Tokens
- Deployment (Import/Export)
- Tenants management
- Modules management
- Indexing/Search (missing settings)
- Homepage
- Settings
- Live preview
- Body editors
- Markdown editor
- Menu
- Collapsible admin menu
- RSS API
- XmlRpc/MetaWeblog API
- Scripting (JS)

# Orchard Core 1.0.0-beta1

Release date: January 22, 2018

## Enhancements

- Updating to ASP.NET Core 2.0.1 [#1223](https://github.com/OrchardCMS/OrchardCore/pull/1223)
- Create static file provider feature [#1222](https://github.com/OrchardCMS/OrchardCore/pull/1222)
- Skip ImageShape when no resize command is set [#1206](https://github.com/OrchardCMS/OrchardCore/pull/1206)
- Adding IsNew on BuildEditorContext [#1194](https://github.com/OrchardCMS/OrchardCore/pull/1194)
- Updates liquid / templates docs. [#1188](https://github.com/OrchardCMS/OrchardCore/pull/1188)
- Support X-Forwarded-Host for tenants [#1185](https://github.com/OrchardCMS/OrchardCore/pull/1185)
- build_display filter also allow a JObject input. [#1181](https://github.com/OrchardCMS/OrchardCore/pull/1181)
- Update LayerMetadataWelder.cs [#1180](https://github.com/OrchardCMS/OrchardCore/pull/1180)
- html_classify liquid filter. [#1177](https://github.com/OrchardCMS/OrchardCore/pull/1177)
- Fixes matching tags in Features.cshtml [#1176](https://github.com/OrchardCMS/OrchardCore/pull/1176)
- Markdownify liquid filter. [#1175](https://github.com/OrchardCMS/OrchardCore/pull/1175)
- Fixes reloading lucene query editor on error [#1173](https://github.com/OrchardCMS/OrchardCore/pull/1173)
- Update LayerMetadataWelder.cs [#1174](https://github.com/OrchardCMS/OrchardCore/pull/1174)
- Fixing query editor [#1171](https://github.com/OrchardCMS/OrchardCore/pull/1171)
- Fixing tether url [#1168](https://github.com/OrchardCMS/OrchardCore/pull/1168)
- Refactoring prefix generation [#1161](https://github.com/OrchardCMS/OrchardCore/pull/1161)
- Working on build_display liquid filter. [#1142](https://github.com/OrchardCMS/OrchardCore/pull/1142)
- Unused lines in modules csproj files. [#1160](https://github.com/OrchardCMS/OrchardCore/pull/1160)
- Fixes razor pages if no shell feature manager. [#1159](https://github.com/OrchardCMS/OrchardCore/pull/1159)
- Update README.md [#1155](https://github.com/OrchardCMS/OrchardCore/pull/1155)
- Add missing The Agency Theme thumbnail [#1144](https://github.com/OrchardCMS/OrchardCore/pull/1144)
- Invoking IModularTenantEvents.Terminating events [#1133](https://github.com/OrchardCMS/OrchardCore/pull/1133)
- Creating ContentPart alternates automatically [#1135](https://github.com/OrchardCMS/OrchardCore/pull/1135)
- Issue a ChallengeResult for admin pages [#1132](https://github.com/OrchardCMS/OrchardCore/pull/1132)
- Update vscode settings [#1126](https://github.com/OrchardCMS/OrchardCore/pull/1126)
- Allows to congifure a global tenant middleware. [#1113](https://github.com/OrchardCMS/OrchardCore/pull/1113)
- Fix agency.recipe.json's hardcoded contentItemIds [#1122](https://github.com/OrchardCMS/OrchardCore/pull/1122)
- Prevents recipes from being copied twice. [#1114](https://github.com/OrchardCMS/OrchardCore/pull/1114)
- Adding support for ORCHARD_APP_DATA environment variable [#1111](https://github.com/OrchardCMS/OrchardCore/pull/1111)
- Fixed spaces for checkbox [#1110](https://github.com/OrchardCMS/OrchardCore/pull/1110)
- Update README.md [#1107](https://github.com/OrchardCMS/OrchardCore/pull/1107)
- Skip the copy step of content/razor/liquid files when there is none. [#1106](https://github.com/OrchardCMS/OrchardCore/pull/1106)
- Fixes null reference when ModularPageRazorFileProvider is no part of a composite. [#1102](https://github.com/OrchardCMS/OrchardCore/pull/1102)
- Allowing async drivers [#1084](https://github.com/OrchardCMS/OrchardCore/pull/1084)
- Don't show irrelevant menu items [#1090](https://github.com/OrchardCMS/OrchardCore/pull/1090)
- Update LiquidViewFilters.cs [#1067](https://github.com/OrchardCMS/OrchardCore/pull/1067)
- Fix parsing if default po header is added to po file [#1088](https://github.com/OrchardCMS/OrchardCore/pull/1088)
- Changes admin menu so that it is displayed on status codes other than 3xx [#1079](https://github.com/OrchardCMS/OrchardCore/pull/1079)
- Add liquidTemplate rendering in HtmlField. [#1066](https://github.com/OrchardCMS/OrchardCore/pull/1066)
- Adds User extension example to Demo module [#1060](https://github.com/OrchardCMS/OrchardCore/pull/1060)
- changed string encoding in template preview [#1006](https://github.com/OrchardCMS/OrchardCore/pull/1006)
- Displays list of IUsers as SummaryAdmin [#1055](https://github.com/OrchardCMS/OrchardCore/pull/1055)
- Makes IUser extensible [#1054](https://github.com/OrchardCMS/OrchardCore/pull/1054)
- Fixing part display name edition [#1057](https://github.com/OrchardCMS/OrchardCore/pull/1057)
- Fixes packages import files. [#1053](https://github.com/OrchardCMS/OrchardCore/pull/1053)
- Typos in Layout.liquid [#1042](https://github.com/OrchardCMS/OrchardCore/pull/1042)
- Adds All Features deployment step [#1034](https://github.com/OrchardCMS/OrchardCore/pull/1034)
- Removed obsolete project [#1031](https://github.com/OrchardCMS/OrchardCore/pull/1031)
- Fixes a couple of user validation issues [#1028](https://github.com/OrchardCMS/OrchardCore/pull/1028)
- Renaming Bundle to Application [#997](https://github.com/OrchardCMS/OrchardCore/pull/997)
- Update tag helper context attributes. [#1001](https://github.com/OrchardCMS/OrchardCore/pull/1001)
- Provides default route names for razor pages. [#1002](https://github.com/OrchardCMS/OrchardCore/pull/1002)
- Renaming media_url to asset_url to match Assets [#1003](https://github.com/OrchardCMS/OrchardCore/pull/1003)
- Setup page handles no recipes available gracefully [#1019](https://github.com/OrchardCMS/OrchardCore/pull/1019)
- Reusing compiled views across tenants [#999](https://github.com/OrchardCMS/OrchardCore/pull/999)
- Prevent MVC from populating an ApplicationPart for each module. [#991](https://github.com/OrchardCMS/OrchardCore/pull/991)
- Building docker images on linux [#990](https://github.com/OrchardCMS/OrchardCore/pull/990)
- Working on ILiquidTemplateEventHandler. [#984](https://github.com/OrchardCMS/OrchardCore/pull/984)
- Set Blog BodyPart Position after AutoroutePart [#978](https://github.com/OrchardCMS/OrchardCore/pull/978)
- Cleanup code [#974](https://github.com/OrchardCMS/OrchardCore/pull/974)
- Pages in any extension subpaths + path checkings. [#967](https://github.com/OrchardCMS/OrchardCore/pull/967)
- Creating Docker Hub image from CI [#968](https://github.com/OrchardCMS/OrchardCore/pull/968)
- Renaming OrchardCore [#966](https://github.com/OrchardCMS/OrchardCore/pull/966)
- Unused themeManager service in this part of code. [#954](https://github.com/OrchardCMS/OrchardCore/pull/954)
- Remove InvariantNumberLiteral. [#958](https://github.com/OrchardCMS/OrchardCore/pull/958)
- Fixes NLog and features  warnings. [#955](https://github.com/OrchardCMS/OrchardCore/pull/955)
- Uses "Microsoft.NET.Sdk" for modules [#956](https://github.com/OrchardCMS/OrchardCore/pull/956)
- Remove cms.recipe.json [#952](https://github.com/OrchardCMS/OrchardCore/pull/952)
- Fixes setup. [#953](https://github.com/OrchardCMS/OrchardCore/pull/953)
- Razor pages [#943](https://github.com/OrchardCMS/OrchardCore/pull/943)
- PO Files and Pluralization support [#732](https://github.com/OrchardCMS/OrchardCore/pull/732)
- Add more flexibility to Users/Roles (Merge Users branch into Master) [#810](https://github.com/OrchardCMS/OrchardCore/pull/810)
- Removing Event Bus [#946](https://github.com/OrchardCMS/OrchardCore/pull/946)
- Open id scope [#941](https://github.com/OrchardCMS/OrchardCore/pull/941)
- Renaming "Fluid" to "Liquid" [#939](https://github.com/OrchardCMS/OrchardCore/pull/939)
- Fixes scope validation in OpenId. [#940](https://github.com/OrchardCMS/OrchardCore/pull/940)
- Optimizing liquid tag helpers support. [#937](https://github.com/OrchardCMS/OrchardCore/pull/937)
- NET Core 2.0 migration [#887](https://github.com/OrchardCMS/OrchardCore/pull/887)
- The Agency [#933](https://github.com/OrchardCMS/OrchardCore/pull/933)
- Fluid view [#881](https://github.com/OrchardCMS/OrchardCore/pull/881)
- Improve blog recipe [#915](https://github.com/OrchardCMS/OrchardCore/pull/915)
- Adding support for media that are not images [#911](https://github.com/OrchardCMS/OrchardCore/pull/911)
- Better preview features [#897](https://github.com/OrchardCMS/OrchardCore/pull/897)
- Fixes dynamic content id in CMS recipe [#896](https://github.com/OrchardCMS/OrchardCore/pull/896)
- Media and Templates [#889](https://github.com/OrchardCMS/OrchardCore/pull/889)
- Adding missing services for multi-tenancy [#884](https://github.com/OrchardCMS/OrchardCore/pull/884)
- Manage themes from admin [#781](https://github.com/OrchardCMS/OrchardCore/pull/781)
- Auto watching module project razor files and static files. [#806](https://github.com/OrchardCMS/OrchardCore/pull/806)
- Fixes Theme ordering [#867](https://github.com/OrchardCMS/OrchardCore/pull/867)
- Update ThemingFileProvider.cs [#868](https://github.com/OrchardCMS/OrchardCore/pull/868)
- Update RazorPage.cs [#869](https://github.com/OrchardCMS/OrchardCore/pull/869)
- Update OrchardCore.Cms.csproj [#865](https://github.com/OrchardCMS/OrchardCore/pull/865)
- Fixes [#851](https://github.com/OrchardCMS/OrchardCore/pull/851) [#861](https://github.com/OrchardCMS/OrchardCore/pull/861)
- [#850](https://github.com/OrchardCMS/OrchardCore/pull/850) Support service suppression  [#853](https://github.com/OrchardCMS/OrchardCore/pull/853)
- Added 'Configuring Certificates' section OpenId README [#845](https://github.com/OrchardCMS/OrchardCore/pull/845)
- Module startup classes now get the same instance of service collection so that services aren't added multiple times to the tenant container. [#843](https://github.com/OrchardCMS/OrchardCore/pull/843)
- OpenId UserInfo endpoint hint and POST [#846](https://github.com/OrchardCMS/OrchardCore/pull/846)
- upgrade nlog and yaml [#833](https://github.com/OrchardCMS/OrchardCore/pull/833)
- [#829](https://github.com/OrchardCMS/OrchardCore/pull/829) Updated Orchard.Cms.Web to publish Nlog.config [#835](https://github.com/OrchardCMS/OrchardCore/pull/835)
- Fixes issue [#830](https://github.com/OrchardCMS/OrchardCore/pull/830)  [#831](https://github.com/OrchardCMS/OrchardCore/pull/831)
- Moving settings to use asp configuration properly. [#826](https://github.com/OrchardCMS/OrchardCore/pull/826)
- Using Fluid instead of DotLiquid [#823](https://github.com/OrchardCMS/OrchardCore/pull/823)
- Prevent Setup if the password is invalid [#819](https://github.com/OrchardCMS/OrchardCore/pull/819)
- Add an overload to Shape method in DisplayDriverBase [#824](https://github.com/OrchardCMS/OrchardCore/pull/824)
- Fixing the shape factory events [#816](https://github.com/OrchardCMS/OrchardCore/pull/816)
- Fix log filename format [#820](https://github.com/OrchardCMS/OrchardCore/pull/820)
- Updating Castle.Core version [#815](https://github.com/OrchardCMS/OrchardCore/pull/815)
- Adding RequireFeaturesAttribute [#795](https://github.com/OrchardCMS/OrchardCore/pull/795)
- Adding Orchard.Liquid module [#785](https://github.com/OrchardCMS/OrchardCore/pull/785)
- Added an overload of Combine method [#805](https://github.com/OrchardCMS/OrchardCore/pull/805)
- Add ability to remove MenuItems [#780](https://github.com/OrchardCMS/OrchardCore/pull/780)
- Add Messages zone into TheTheme [#800](https://github.com/OrchardCMS/OrchardCore/pull/800)
- Missing permission check [#799](https://github.com/OrchardCMS/OrchardCore/pull/799)
- Refactor IContentItemIdGenerator [#796](https://github.com/OrchardCMS/OrchardCore/pull/796)
- Fixing deferred task database locking [#782](https://github.com/OrchardCMS/OrchardCore/pull/782)
- Fixing tests [#784](https://github.com/OrchardCMS/OrchardCore/pull/784)
- Upgrade Libs [#779](https://github.com/OrchardCMS/OrchardCore/pull/779)
- Watching Modules / Themes razor files [#686](https://github.com/OrchardCMS/OrchardCore/pull/686)
- Validating ClientSecret using password validators [#778](https://github.com/OrchardCMS/OrchardCore/pull/778)
- Sql Queries [#771](https://github.com/OrchardCMS/OrchardCore/pull/771)
- Use DateEditor value to initialize CommonPart.CreatedUtc [#774](https://github.com/OrchardCMS/OrchardCore/pull/774)
- Fix openid settings jquery selectors [#769](https://github.com/OrchardCMS/OrchardCore/pull/769)
- Updated OpenIddict version and Nuget sources [#773](https://github.com/OrchardCMS/OrchardCore/pull/773)

# Orchard Core 1.0.0-beta2

Release date: June 22, 2018  

## Milestone

[Beta2](https://github.com/OrchardCMS/OrchardCore/milestone/4)

## Enhancements

- ResetPassword wrong redirect [#2043](https://github.com/OrchardCMS/OrchardCore/pull/2043)
- Removing Html migration [#2047](https://github.com/OrchardCMS/OrchardCore/pull/2047)
- Updating to ASP.NET Core 2.1.1 [#2040](https://github.com/OrchardCMS/OrchardCore/pull/2040)
- Improving templates [#2039](https://github.com/OrchardCMS/OrchardCore/pull/2039)
- Fixes that Media table view does not resize images [#2036](https://github.com/OrchardCMS/OrchardCore/pull/2036)
- Flickering of submenu on page reload Fixes [#2033](https://github.com/OrchardCMS/OrchardCore/pull/2033) [#2034](https://github.com/OrchardCMS/OrchardCore/pull/2034)
- Using a single Nuget templates project. [#2026](https://github.com/OrchardCMS/OrchardCore/pull/2026)
- Migration for BodyPart to HtmlBodyPart name changes. [#2025](https://github.com/OrchardCMS/OrchardCore/pull/2025)
- Fixes [#2023](https://github.com/OrchardCMS/OrchardCore/pull/2023) media added twice on several markdown editors [#2030](https://github.com/OrchardCMS/OrchardCore/pull/2030)
- Automatically reload the current tenant when the OpenID client/server/validation settings are updated [#2028](https://github.com/OrchardCMS/OrchardCore/pull/2028)
- Fix admin left menu by using click event instead of hover [#2024](https://github.com/OrchardCMS/OrchardCore/pull/2024)
- Clearing ModelState between TryUpdateModelAsync calls [#2021](https://github.com/OrchardCMS/OrchardCore/pull/2021)
- Fixes Html and Markdown bodies [#2022](https://github.com/OrchardCMS/OrchardCore/pull/2022)
- Rename BodyPart to HtmlBodyPart [#1933](https://github.com/OrchardCMS/OrchardCore/pull/1933)
- Removing package version [#2015](https://github.com/OrchardCMS/OrchardCore/pull/2015)
- Update templates project files. [#2017](https://github.com/OrchardCMS/OrchardCore/pull/2017)
- Dotnet new templates doc [#2018](https://github.com/OrchardCMS/OrchardCore/pull/2018)
- Delay a little the hover flyout  on collapsed left menu [#1990](https://github.com/OrchardCMS/OrchardCore/pull/1990)
- OrchardCore dotnet new templates [#1877](https://github.com/OrchardCMS/OrchardCore/pull/1877)
- Forms Module [#1821](https://github.com/OrchardCMS/OrchardCore/pull/1821)
- Set order explicitly DataProtection [#1992](https://github.com/OrchardCMS/OrchardCore/pull/1992)
- AddOrchardCms overload with a configure action. [#2005](https://github.com/OrchardCMS/OrchardCore/pull/2005)
- Ensuring settings drivers check permissions [#2009](https://github.com/OrchardCMS/OrchardCore/pull/2009)
- Fix broken path on media's drag-thumbnail [#2013](https://github.com/OrchardCMS/OrchardCore/pull/2013)
- Add move cursor to field list and part list on edit content type view [#1991](https://github.com/OrchardCMS/OrchardCore/pull/1991)
- Custom Activity Title [#2008](https://github.com/OrchardCMS/OrchardCore/pull/2008)
- Update dependencies to latest versions [#1986](https://github.com/OrchardCMS/OrchardCore/pull/1986)
- Removing restriction which activities are startable. [#2002](https://github.com/OrchardCMS/OrchardCore/pull/2002)
- Remove admin footer [#1996](https://github.com/OrchardCMS/OrchardCore/pull/1996)
- Migrate to OpenIddict RC3 [#1787](https://github.com/OrchardCMS/OrchardCore/pull/1787)
- Update Modules documentation [#1995](https://github.com/OrchardCMS/OrchardCore/pull/1995)
- Unused service [#1985](https://github.com/OrchardCMS/OrchardCore/pull/1985)
- Ensure Owner is not null [#1979](https://github.com/OrchardCMS/OrchardCore/pull/1979)
- Some csproj updates. [#1973](https://github.com/OrchardCMS/OrchardCore/pull/1973)
- Fix NLog orchard-tenant-name returns None. [#1974](https://github.com/OrchardCMS/OrchardCore/pull/1974)
- Update launchSettings.json [#1977](https://github.com/OrchardCMS/OrchardCore/pull/1977)
- Update AdminDashboard.cshtml [#1980](https://github.com/OrchardCMS/OrchardCore/pull/1980)
- Edit spelling and language, some formatting [#1975](https://github.com/OrchardCMS/OrchardCore/pull/1975)
- Moving security services to AddOrchardCore and isolating NotifyFilter [#1971](https://github.com/OrchardCMS/OrchardCore/pull/1971)
- Simplifying and documenting Widget templating [#1956](https://github.com/OrchardCMS/OrchardCore/pull/1956)
- Adding active menu items script [#1959](https://github.com/OrchardCMS/OrchardCore/pull/1959)
- Documenting theming [#1968](https://github.com/OrchardCMS/OrchardCore/pull/1968)
- Fixes LocalClock async api. [#1962](https://github.com/OrchardCMS/OrchardCore/pull/1962)
- Fixes BlobFileStore.GetDirectoryInfo returns a directory even if it does not exist [#1963](https://github.com/OrchardCMS/OrchardCore/pull/1963) [#1964](https://github.com/OrchardCMS/OrchardCore/pull/1964)
- Use standard AddIdentity [#1961](https://github.com/OrchardCMS/OrchardCore/pull/1961)
- TheTheme Content alternate [#1957](https://github.com/OrchardCMS/OrchardCore/pull/1957)
- Fix that media grid layout is broken when using azure blob storage. [#1954](https://github.com/OrchardCMS/OrchardCore/pull/1954)
- Fix Media Library error with AzureBlob file storage [#1653](https://github.com/OrchardCMS/OrchardCore/pull/1653) [#1955](https://github.com/OrchardCMS/OrchardCore/pull/1955)
- Update Getting Started section [#1952](https://github.com/OrchardCMS/OrchardCore/pull/1952)
- Fixing menu shapes alternates [#1951](https://github.com/OrchardCMS/OrchardCore/pull/1951)
- Remove dependencies on removed modules. [#1950](https://github.com/OrchardCMS/OrchardCore/pull/1950)
- Open id connect Client [#1622](https://github.com/OrchardCMS/OrchardCore/pull/1622)
- Fixes previewing when using the trumbowyg editor. [#1949](https://github.com/OrchardCMS/OrchardCore/pull/1949)
- Content filters [#1923](https://github.com/OrchardCMS/OrchardCore/pull/1923)
- TheTheme Footer [#1935](https://github.com/OrchardCMS/OrchardCore/pull/1935)
- Fixes trumbowyg preview is out of sync [#1948](https://github.com/OrchardCMS/OrchardCore/pull/1948)
- Update Dependencies.AspNetCore.props [#1947](https://github.com/OrchardCMS/OrchardCore/pull/1947)
- Bootstrap switch editor in css [#1885](https://github.com/OrchardCMS/OrchardCore/pull/1885)
- Fixing Microsoft.AspNetCore.TestHost package name [#1946](https://github.com/OrchardCMS/OrchardCore/pull/1946)
- Fixing ApiExplorer reference [#1945](https://github.com/OrchardCMS/OrchardCore/pull/1945)
- Adding DefaultTenantOnly on feature Manifest [#1931](https://github.com/OrchardCMS/OrchardCore/pull/1931)
- Fixing preset tenants Setup [#1941](https://github.com/OrchardCMS/OrchardCore/pull/1941)
- Media UI [#1944](https://github.com/OrchardCMS/OrchardCore/pull/1944)
- DateField implementation [#1929](https://github.com/OrchardCMS/OrchardCore/pull/1929)
- Placement documentation [#1939](https://github.com/OrchardCMS/OrchardCore/pull/1939)
- Autoroute documentation [#1934](https://github.com/OrchardCMS/OrchardCore/pull/1934)
- Menu documentation [#1936](https://github.com/OrchardCMS/OrchardCore/pull/1936)
- Resources documentation [#1938](https://github.com/OrchardCMS/OrchardCore/pull/1938)
- Using SixLabors.ImageSharp from nuget.org [#1930](https://github.com/OrchardCMS/OrchardCore/pull/1930)
- Hides connection string e.g if sqlite preselected. [#1926](https://github.com/OrchardCMS/OrchardCore/pull/1926)
- Migrate to netcoreapp21 [#1902](https://github.com/OrchardCMS/OrchardCore/pull/1902)
- Liquid Request.Form now handles requests without Form values [#1905](https://github.com/OrchardCMS/OrchardCore/pull/1905)
- Tenants configurable from the app [#1766](https://github.com/OrchardCMS/OrchardCore/pull/1766)
- Remove dependency on Indentity [#1896](https://github.com/OrchardCMS/OrchardCore/pull/1896)
- Update CommonPart-Date.Edit.cshtml [#1897](https://github.com/OrchardCMS/OrchardCore/pull/1897)
- CreatedUtc Datetime Editor [#1856](https://github.com/OrchardCMS/OrchardCore/pull/1856)
- Fix jQuery error in Sql Query admin [#1880](https://github.com/OrchardCMS/OrchardCore/pull/1880)
- Update TheTheme to Bootstrap 4 [#1883](https://github.com/OrchardCMS/OrchardCore/pull/1883)
- Autoroute Permalink: Display Site.BaseUrl and View button [#1879](https://github.com/OrchardCMS/OrchardCore/pull/1879)
- Edit Owner [#1881](https://github.com/OrchardCMS/OrchardCore/pull/1881)
- Password feature in Users module [#1789](https://github.com/OrchardCMS/OrchardCore/pull/1789)
- Makes SQLLite the default SQL provider [#1887](https://github.com/OrchardCMS/OrchardCore/pull/1887)
- Fixes BackgroundTaskService.Terminate(). [#1888](https://github.com/OrchardCMS/OrchardCore/pull/1888)
- TimeField implementation [#1858](https://github.com/OrchardCMS/OrchardCore/pull/1858)
- Fixes 2 use cases when resolving an IEnumerable of a given service type. [#1644](https://github.com/OrchardCMS/OrchardCore/pull/1644)
- Use IHttpContextAccessor to hold the IUpdateModel [#1695](https://github.com/OrchardCMS/OrchardCore/pull/1695)
- Updating RequestLiquidTemplateEventHandler to support {{ Request.Form.Keys }} [#1765](https://github.com/OrchardCMS/OrchardCore/pull/1765)
- Fixing view error and renaming ContentTypeDeploymentStep [#1804](https://github.com/OrchardCMS/OrchardCore/pull/1804)
- Embedded file last modified = last write time of the assembly file. [#1867](https://github.com/OrchardCMS/OrchardCore/pull/1867)
- User TimeZone feature [#1816](https://github.com/OrchardCMS/OrchardCore/pull/1816)
- Adds Azure Storage data protection [#1825](https://github.com/OrchardCMS/OrchardCore/pull/1825)
- Only add settings.txt as a config source if it exists [#1854](https://github.com/OrchardCMS/OrchardCore/pull/1854)
- Dynamic cache docs [#1855](https://github.com/OrchardCMS/OrchardCore/pull/1855)
- Display the draft of content items for a ListPart in admin [#1860](https://github.com/OrchardCMS/OrchardCore/pull/1860)
- Fixing LogTask activity [#1861](https://github.com/OrchardCMS/OrchardCore/pull/1861)
- Fix admin footer size and resize responsive behavior [#1818](https://github.com/OrchardCMS/OrchardCore/pull/1818)
- Fix launch settings [#1840](https://github.com/OrchardCMS/OrchardCore/pull/1840)
- Fixing resource cdn urls and integrity [#1843](https://github.com/OrchardCMS/OrchardCore/pull/1843)
- DateTimeField implementation [#1828](https://github.com/OrchardCMS/OrchardCore/pull/1828)
- Auto expand leftmenu [#1827](https://github.com/OrchardCMS/OrchardCore/pull/1827)
- Update to .NET Core SDK 2.1.200 [#1839](https://github.com/OrchardCMS/OrchardCore/pull/1839)
- Update MVC module order [#1830](https://github.com/OrchardCMS/OrchardCore/pull/1830)
- Update Azure Media Startup order [#1829](https://github.com/OrchardCMS/OrchardCore/pull/1829)
- Dynamic cache [#1624](https://github.com/OrchardCMS/OrchardCore/pull/1624)
- Prevent data protection logging errors on setup. [#1814](https://github.com/OrchardCMS/OrchardCore/pull/1814)
- Nodatime [#1659](https://github.com/OrchardCMS/OrchardCore/pull/1659)
- Add footer in admin and display version [#1706](https://github.com/OrchardCMS/OrchardCore/pull/1706)
- Fixing that generated Alias would not be persisted [#1797](https://github.com/OrchardCMS/OrchardCore/pull/1797)
- Adds alternate and wrapper attributes to the BaseShapeTagHelper. [#1792](https://github.com/OrchardCMS/OrchardCore/pull/1792)
- Updating ContentDefinitionDeploymentStepDriver [#1806](https://github.com/OrchardCMS/OrchardCore/pull/1806)
- Fixing handling of updating content fields with empty values [#1801](https://github.com/OrchardCMS/OrchardCore/pull/1801)
- Fixing default alias part setting pattern [#1798](https://github.com/OrchardCMS/OrchardCore/pull/1798)
- Applying correct logging practices [#1785](https://github.com/OrchardCMS/OrchardCore/pull/1785)
- Added null check to content item when indexing [#1802](https://github.com/OrchardCMS/OrchardCore/pull/1802)
- Functional tests [#1782](https://github.com/OrchardCMS/OrchardCore/pull/1782)
- Adjusting build warnings [#1780](https://github.com/OrchardCMS/OrchardCore/pull/1780)
- Package management cleanup [#1779](https://github.com/OrchardCMS/OrchardCore/pull/1779)
- User Task Activity [#1748](https://github.com/OrchardCMS/OrchardCore/pull/1748)
- Fixing media module's infinite loop on ie11 [#1751](https://github.com/OrchardCMS/OrchardCore/pull/1751)
- Number Fields editors [#1763](https://github.com/OrchardCMS/OrchardCore/pull/1763)
- Updating LiquidPart.Edit.cshtml [#1770](https://github.com/OrchardCMS/OrchardCore/pull/1770)
- Updating flows.edit.css [#1771](https://github.com/OrchardCMS/OrchardCore/pull/1771)
- Improve hover on submenus [#1772](https://github.com/OrchardCMS/OrchardCore/pull/1772)
- Updating HttpWorkflowController [#1778](https://github.com/OrchardCMS/OrchardCore/pull/1778)
- Streamline centalized package version management [#1777](https://github.com/OrchardCMS/OrchardCore/pull/1777)
- Add generated js and css files to wwwroot [#1738](https://github.com/OrchardCMS/OrchardCore/pull/1738)
- Activate a shell which may do migrations in an inner scope. [#1660](https://github.com/OrchardCMS/OrchardCore/pull/1660)
- Reset Password [#1662](https://github.com/OrchardCMS/OrchardCore/pull/1662)
- Fixing ForEach, For and Notify activities [#1728](https://github.com/OrchardCMS/OrchardCore/pull/1728)
- Leftbar collapsed by default on small screen [#1732](https://github.com/OrchardCMS/OrchardCore/pull/1732)
- Adding field alternate targeting field type and content type [#1729](https://github.com/OrchardCMS/OrchardCore/pull/1729)
- Various Workflows tweaks and bug-fixes [#1700](https://github.com/OrchardCMS/OrchardCore/pull/1700)
- Updating workflows verbiage [#1705](https://github.com/OrchardCMS/OrchardCore/pull/1705)
- Null checking in AutorouteRoute.cs. [#1698](https://github.com/OrchardCMS/OrchardCore/pull/1698)
- Upgrade to Bootstrap 4.1.0, Popper 1.14.3, Font awesome 5.0.9 [#1668](https://github.com/OrchardCMS/OrchardCore/pull/1668)
- Workflows [#1378](https://github.com/OrchardCMS/OrchardCore/pull/1378)
- Remove hardcoded Display Route for ContentItems [#1219](https://github.com/OrchardCMS/OrchardCore/pull/1219)
- Confirmation message on disabling a feature, with dependents features if any [#1672](https://github.com/OrchardCMS/OrchardCore/pull/1672)
- Minimizable leftbar [#1667](https://github.com/OrchardCMS/OrchardCore/pull/1667)
- Adding IStartupFilter support [#1675](https://github.com/OrchardCMS/OrchardCore/pull/1675)
- Add AccessAdminPanel to other roles than administrator [#1678](https://github.com/OrchardCMS/OrchardCore/pull/1678)
- Fix that the a media is still available on the page after deleting it. [#1686](https://github.com/OrchardCMS/OrchardCore/pull/1686)
- Reload current tenant when SmtpSettings are changed [#1677](https://github.com/OrchardCMS/OrchardCore/pull/1677)
- Allow to change BaseUrl SiteSetting [#1663](https://github.com/OrchardCMS/OrchardCore/pull/1663)
- Fixing Unprotect exception [#1657](https://github.com/OrchardCMS/OrchardCore/pull/1657)
- Update ImageSharp.Web to beta3 [#1656](https://github.com/OrchardCMS/OrchardCore/pull/1656)
- Fixes inner recipes [#1609](https://github.com/OrchardCMS/OrchardCore/pull/1609) [#1642](https://github.com/OrchardCMS/OrchardCore/pull/1642)
- Clicking cancel on edit-create template always returns to list of templates [#1647](https://github.com/OrchardCMS/OrchardCore/pull/1647)
- Fixes that adding an invalid named part displays success message [#1649](https://github.com/OrchardCMS/OrchardCore/pull/1649)
- Fixing Fixes Expand / Collapse buttons for widgets  [#1651](https://github.com/OrchardCMS/OrchardCore/pull/1651)
- Fixing typo in AdminAttribute.cs [#1652](https://github.com/OrchardCMS/OrchardCore/pull/1652)
- Move deferred tasks at the very end of the request and out of its scope [#1643](https://github.com/OrchardCMS/OrchardCore/pull/1643)
- Split the OpenID module into 3 distinct features and introduce the Antiforgery/Data Protection modules [#1602](https://github.com/OrchardCMS/OrchardCore/pull/1602)
- Update Microsoft.AspNetCore.All 2.0.6 dependencies [#1628](https://github.com/OrchardCMS/OrchardCore/pull/1628)
- Adding port matching and fallback option to RunningShellTable [#1640](https://github.com/OrchardCMS/OrchardCore/pull/1640)
- Implement IUserLoginStore<IUser> [#1481](https://github.com/OrchardCMS/OrchardCore/pull/1481)
- Clearing the shell context dependents upon release [#1639](https://github.com/OrchardCMS/OrchardCore/pull/1639)
- Validate part name  [#1638](https://github.com/OrchardCMS/OrchardCore/pull/1638)
- Implement shell dependencies [#1633](https://github.com/OrchardCMS/OrchardCore/pull/1633)
- Fixing sql string formatting [#1616](https://github.com/OrchardCMS/OrchardCore/pull/1616)
- Fixed error getting token [#1618](https://github.com/OrchardCMS/OrchardCore/pull/1618)
- Remove unnecessary class [#1606](https://github.com/OrchardCMS/OrchardCore/pull/1606)
- Fix HTTPS module admin menu item not showing in the configuration menu [#1605](https://github.com/OrchardCMS/OrchardCore/pull/1605)
- Fix Media browser [#1595](https://github.com/OrchardCMS/OrchardCore/pull/1595)



# Orchard Core 1.0.0-beta3

Release date: April 3, 2019  

## Milestone

[Beta3](https://github.com/OrchardCMS/OrchardCore/milestone/5)

## Enhancements

- Redirecting user to confirmation page after password reset request. [#3429](https://github.com/OrchardCMS/OrchardCore/pull/3429)
- Revert "Call PublishAsync instead of using VersionOptions. ([#3420](https://github.com/OrchardCMS/OrchardCore/pull/3420))" [#3427](https://github.com/OrchardCMS/OrchardCore/pull/3427)
- Fixing Media Liquid Filter 'resize_url' arguments [#3425](https://github.com/OrchardCMS/OrchardCore/pull/3425)
- Fix codemirror.css path [#3399](https://github.com/OrchardCMS/OrchardCore/pull/3399)
- Improve create button on ListPart [#3412](https://github.com/OrchardCMS/OrchardCore/pull/3412)
- small fix on dotnet restore [#3423](https://github.com/OrchardCMS/OrchardCore/pull/3423)
- Call PublishAsync instead of using VersionOptions. [#3420](https://github.com/OrchardCMS/OrchardCore/pull/3420)
- Add in `crop` for Resize Mode [#3411](https://github.com/OrchardCMS/OrchardCore/pull/3411)
- Adding localization file guide [#3397](https://github.com/OrchardCMS/OrchardCore/pull/3397)
- Fixing DataAnnotations localization [#3396](https://github.com/OrchardCMS/OrchardCore/pull/3396)
- Fix build for docker [#3395](https://github.com/OrchardCMS/OrchardCore/pull/3395)
- Add CodeMirror autorefresh [#3394](https://github.com/OrchardCMS/OrchardCore/pull/3394)
- HTML Escaping - Change 'Raw' to 'raw' [#3393](https://github.com/OrchardCMS/OrchardCore/pull/3393)
- Add return url to add and edit field  views to make them usable from different sources. [#3390](https://github.com/OrchardCMS/OrchardCore/pull/3390)
- Add screenshots to create cms guide. [#3387](https://github.com/OrchardCMS/OrchardCore/pull/3387)
- Missing description and name in manifests [#3385](https://github.com/OrchardCMS/OrchardCore/pull/3385)
- Fixing route [#3386](https://github.com/OrchardCMS/OrchardCore/pull/3386)
- Add new guide about creating cms application [#3379](https://github.com/OrchardCMS/OrchardCore/pull/3379)
- Add new guide about adding admin menus. [#3378](https://github.com/OrchardCMS/OrchardCore/pull/3378)
- Fix Get not returning changes made be Apply [#3365](https://github.com/OrchardCMS/OrchardCore/pull/3365)
- Defining Menu parts [#3367](https://github.com/OrchardCMS/OrchardCore/pull/3367)
- Replaces existing arrays when updating content items via script [#3357](https://github.com/OrchardCMS/OrchardCore/pull/3357)
- Rollback the key from "WorkflowExecutionContext" to "Workflow" [#3361](https://github.com/OrchardCMS/OrchardCore/pull/3361)
- Implementing content type permissions [#3354](https://github.com/OrchardCMS/OrchardCore/pull/3354)
- Added graphql query sample [#3285](https://github.com/OrchardCMS/OrchardCore/pull/3285)
- Update README.md [#3262](https://github.com/OrchardCMS/OrchardCore/pull/3262)
- Prevent loading all workflows in the startup [#3320](https://github.com/OrchardCMS/OrchardCore/pull/3320)
- [Https] Propose current port as SSL Port ([#3026](https://github.com/OrchardCMS/OrchardCore/pull/3026)) [#3350](https://github.com/OrchardCMS/OrchardCore/pull/3350)
- Use NullStringLocalizer by default in the CMS [#3344](https://github.com/OrchardCMS/OrchardCore/pull/3344)
- Fixing new content item edition [#3337](https://github.com/OrchardCMS/OrchardCore/pull/3337)
- Fix BlobFileStore [#3336](https://github.com/OrchardCMS/OrchardCore/pull/3336)
- Only add a user claim when it is not present [#3326](https://github.com/OrchardCMS/OrchardCore/pull/3326)
- Updating fluid [#3284](https://github.com/OrchardCMS/OrchardCore/pull/3284)
- Update CacheExpiresSlidingTag.cs [#3323](https://github.com/OrchardCMS/OrchardCore/pull/3323)
- Update ShapeCacheTag.cs [#3322](https://github.com/OrchardCMS/OrchardCore/pull/3322)
- Remove temporary reconfiguration of google options [#3321](https://github.com/OrchardCMS/OrchardCore/pull/3321)
- Fix bug workflow.JavaScriptWorkflowScriptEvaluator [#3314](https://github.com/OrchardCMS/OrchardCore/pull/3314)
- Reusing the same part instances [#3310](https://github.com/OrchardCMS/OrchardCore/pull/3310)
- Add guides section to docs [#3309](https://github.com/OrchardCMS/OrchardCore/pull/3309)
- Fix wrong language label of this repository [#3303](https://github.com/OrchardCMS/OrchardCore/pull/3303)
- Fixing LoadingAsync for known parts [#3308](https://github.com/OrchardCMS/OrchardCore/pull/3308)
- Setting liquid encodings explicitely [#3315](https://github.com/OrchardCMS/OrchardCore/pull/3315)
- Fixing plural translation exceptions [#3316](https://github.com/OrchardCMS/OrchardCore/pull/3316)
- Improving functional tests log [#3298](https://github.com/OrchardCMS/OrchardCore/pull/3298)
- Allows to get more application's module file infos. [#3296](https://github.com/OrchardCMS/OrchardCore/pull/3296)
- Use flexbox for content alignment on content picker [#3295](https://github.com/OrchardCMS/OrchardCore/pull/3295)
- Fix the issue of workflow-recipe [#3290](https://github.com/OrchardCMS/OrchardCore/pull/3290)
- Fix openid certificates on Azure App Services [#3255](https://github.com/OrchardCMS/OrchardCore/pull/3255)
- Allow to add alternates in OnProcessing [#3277](https://github.com/OrchardCMS/OrchardCore/pull/3277)
- Refactoring Media validation [#3282](https://github.com/OrchardCMS/OrchardCore/pull/3282)
- Revert "Fixing taxonomy recipes [#3253](https://github.com/OrchardCMS/OrchardCore/pull/3253)
- Represent OIDC authorities as System.Uri instances to perform automatic normalization [#3269](https://github.com/OrchardCMS/OrchardCore/pull/3269)
- Disable Layers on Admin themes [#3272](https://github.com/OrchardCMS/OrchardCore/pull/3272)
- Remove unnecessary fields from content picker view model [#3268](https://github.com/OrchardCMS/OrchardCore/pull/3268)
- Remove unused OrchardCore.Title dependency from OrchardCore.Media [#3266](https://github.com/OrchardCMS/OrchardCore/pull/3266)
- Fix icon picker initialization [#3271](https://github.com/OrchardCMS/OrchardCore/pull/3271)
- Using default content icon for non-image files [#3256](https://github.com/OrchardCMS/OrchardCore/pull/3256)
- Update content field readme [#3264](https://github.com/OrchardCMS/OrchardCore/pull/3264)
- Fix typo in icon picker style tag [#3265](https://github.com/OrchardCMS/OrchardCore/pull/3265)
- Simplifying theme template [#3254](https://github.com/OrchardCMS/OrchardCore/pull/3254)
- Fixing taxonomy recipes [#3253](https://github.com/OrchardCMS/OrchardCore/pull/3253)
- Update SixLabors.ImageSharp.Web Version 1.0.0-beta0007 [#3245](https://github.com/OrchardCMS/OrchardCore/pull/3245)
- Disable encoding for templated queries [#3224](https://github.com/OrchardCMS/OrchardCore/pull/3224)
- Add "property" attribute to the meta tag helper. [#3211](https://github.com/OrchardCMS/OrchardCore/pull/3211)
- Fix null error when BodyAspect is not populated [#3230](https://github.com/OrchardCMS/OrchardCore/pull/3230)
- Initialize content picker field with empty array [#3247](https://github.com/OrchardCMS/OrchardCore/pull/3247)
- Allow theming for Login/Registration/ResetPassword [#3218](https://github.com/OrchardCMS/OrchardCore/pull/3218)
- Adding configurable upload limits [#3221](https://github.com/OrchardCMS/OrchardCore/pull/3221)
- [GraphQL] collapsed where statements fixes [#3234](https://github.com/OrchardCMS/OrchardCore/pull/3234) [#3235](https://github.com/OrchardCMS/OrchardCore/pull/3235)
- Fixed introspection for contentitemtype ignored fields [#3238](https://github.com/OrchardCMS/OrchardCore/pull/3238)
- Add jquery as dependency of icon picker script [#3242](https://github.com/OrchardCMS/OrchardCore/pull/3242)
- Adding Step variable to the For Loop [#3248](https://github.com/OrchardCMS/OrchardCore/pull/3248)
- Added claims to the list of available properties [#3236](https://github.com/OrchardCMS/OrchardCore/pull/3236)
- Fix null reference exception in MediaField.cshtml [#3228](https://github.com/OrchardCMS/OrchardCore/pull/3228)
- Fixes part removal in where if the index has multiple aliases [#3217](https://github.com/OrchardCMS/OrchardCore/pull/3217)
- Fixes that graphql where statements have a suffix of part on partnames [#3206](https://github.com/OrchardCMS/OrchardCore/pull/3206) [#3207](https://github.com/OrchardCMS/OrchardCore/pull/3207)
- Adding shape_cache liquid tag [#3194](https://github.com/OrchardCMS/OrchardCore/pull/3194)
- Fixing IndexingTaskManager table prefix usage in FlushAsync [#3192](https://github.com/OrchardCMS/OrchardCore/pull/3192)
- Adding Hide to the Content Item which is what I actually wanted [#3193](https://github.com/OrchardCMS/OrchardCore/pull/3193)
- Fixing IndexingTaskManager table prefix usage [#3190](https://github.com/OrchardCMS/OrchardCore/pull/3190)
- [GraphQL] Add the hidden option [#3152](https://github.com/OrchardCMS/OrchardCore/pull/3152)
- Fixes plural localization in the DispayManagement project [#3185](https://github.com/OrchardCMS/OrchardCore/pull/3185)
- Updating dependencies [#3181](https://github.com/OrchardCMS/OrchardCore/pull/3181)
- Add OpenID config input hints for redirect URIs [#3179](https://github.com/OrchardCMS/OrchardCore/pull/3179)
- Make IRecipeExecutor a tenant singleton. [#3127](https://github.com/OrchardCMS/OrchardCore/pull/3127)
- Fix assets app position when a warning is visible. [#3173](https://github.com/OrchardCMS/OrchardCore/pull/3173)
- Fixing package references [#3175](https://github.com/OrchardCMS/OrchardCore/pull/3175)
- Take the PathBase into account. [#3094](https://github.com/OrchardCMS/OrchardCore/pull/3094)
- Fix z-index of child media modals [#3149](https://github.com/OrchardCMS/OrchardCore/pull/3149)
- Unecessary calls to AddMvc() and AddMvcCore(). [#3154](https://github.com/OrchardCMS/OrchardCore/pull/3154)
- Ensure meta tags are rendered self closing [#3159](https://github.com/OrchardCMS/OrchardCore/pull/3159)
- Remove interpolated strings from calls to IStringLocalizer [#3160](https://github.com/OrchardCMS/OrchardCore/pull/3160)
- NavigationBuilder AddAsync(). [#3151](https://github.com/OrchardCMS/OrchardCore/pull/3151)
- Updating YesSql [#3134](https://github.com/OrchardCMS/OrchardCore/pull/3134)
- Fixing stackoverflow when displaying media [#3132](https://github.com/OrchardCMS/OrchardCore/pull/3132)
- Fix connection usage not supplying transaction during upgrade from beta 2 [#3137](https://github.com/OrchardCMS/OrchardCore/pull/3137)
- Fixing connection usage [#3131](https://github.com/OrchardCMS/OrchardCore/pull/3131)
- Add Admin Attribute [#3124](https://github.com/OrchardCMS/OrchardCore/pull/3124)
- Prevent nested containers during setup step [#3120](https://github.com/OrchardCMS/OrchardCore/pull/3120)
- [GraphQL] Fixes UserContext being null for collapsed  fields [#3121](https://github.com/OrchardCMS/OrchardCore/pull/3121)
- Fixing concurrent execution of fields resolution [#3119](https://github.com/OrchardCMS/OrchardCore/pull/3119)
- Adding Visual Studio extension and training demo module references to index.md [#3102](https://github.com/OrchardCMS/OrchardCore/pull/3102)
- Updating yessql [#3099](https://github.com/OrchardCMS/OrchardCore/pull/3099)
- Missing references and cleanups. [#3093](https://github.com/OrchardCMS/OrchardCore/pull/3093)
- Fix that media modal is not shown when trumbowyg is full screen [#3116](https://github.com/OrchardCMS/OrchardCore/pull/3116)
- Use accepted values for resized images [#3113](https://github.com/OrchardCMS/OrchardCore/pull/3113)
- Manage Culture admin page [#3101](https://github.com/OrchardCMS/OrchardCore/pull/3101)
- Layer rule based on the current culture [#3108](https://github.com/OrchardCMS/OrchardCore/pull/3108)
- [GraphQL] Collapse fixes [#3112](https://github.com/OrchardCMS/OrchardCore/pull/3112)
- Deleting the web.config file [#3092](https://github.com/OrchardCMS/OrchardCore/pull/3092)
- Added validation for AliasPart to test for duplicate aliases ([#2310](https://github.com/OrchardCMS/OrchardCore/pull/2310)) [#3095](https://github.com/OrchardCMS/OrchardCore/pull/3095)
- [GraphQL] Should Filter On Multiple Indexes with the Same Alias [#3088](https://github.com/OrchardCMS/OrchardCore/pull/3088)
- [GraphQL] Option to collapse parts [#2842](https://github.com/OrchardCMS/OrchardCore/pull/2842)
- Adding missing ContentPart.TermAdmin template [#3091](https://github.com/OrchardCMS/OrchardCore/pull/3091)
- Fixes application view paths. [#3087](https://github.com/OrchardCMS/OrchardCore/pull/3087)
- [GraphQL] Multiple alias names with the same index [#3084](https://github.com/OrchardCMS/OrchardCore/pull/3084)
- Adding configuration support [#2824](https://github.com/OrchardCMS/OrchardCore/pull/2824)
- Tweak to [#2879](https://github.com/OrchardCMS/OrchardCore/pull/2879) - remove compiler directives [#3081](https://github.com/OrchardCMS/OrchardCore/pull/3081)
- Replace localization culture delimiter [#3076](https://github.com/OrchardCMS/OrchardCore/pull/3076)
- Add Crowdin badge [#3059](https://github.com/OrchardCMS/OrchardCore/pull/3059)
- Added unpublish workflow event [#3079](https://github.com/OrchardCMS/OrchardCore/pull/3079)
- Fixes [#2879](https://github.com/OrchardCMS/OrchardCore/pull/2879) [#3077](https://github.com/OrchardCMS/OrchardCore/pull/3077)
- Fixing index providers stack overflow exceptions [#3071](https://github.com/OrchardCMS/OrchardCore/pull/3071)
- Fixing liquid parsing exceptions [#3072](https://github.com/OrchardCMS/OrchardCore/pull/3072)
- Fix TitlePart XmlRpc update issue  [#3051](https://github.com/OrchardCMS/OrchardCore/pull/3051)
- Retain display text filter value [#3058](https://github.com/OrchardCMS/OrchardCore/pull/3058)
- Adding graphqk contentItems property to ListPart [#3057](https://github.com/OrchardCMS/OrchardCore/pull/3057)
- added Microsoft.AspNetCore.Mvc PackageReference to Google Module [#3064](https://github.com/OrchardCMS/OrchardCore/pull/3064)
- Added DisplayText filter for Admin/Contents/ContentItems [#3036](https://github.com/OrchardCMS/OrchardCore/pull/3036)
- Adding TitlePart migration [#3047](https://github.com/OrchardCMS/OrchardCore/pull/3047)
- Updating Fluid [#3042](https://github.com/OrchardCMS/OrchardCore/pull/3042)
- Fixing model binding [#3046](https://github.com/OrchardCMS/OrchardCore/pull/3046)
- Updating 2.2.1 packages [#3044](https://github.com/OrchardCMS/OrchardCore/pull/3044)
- Added mising updatedAsync content handler [#3045](https://github.com/OrchardCMS/OrchardCore/pull/3045)
- Removing classes related to content management [#3040](https://github.com/OrchardCMS/OrchardCore/pull/3040)
- Remove SqlProvider filter from tenants admin [#3030](https://github.com/OrchardCMS/OrchardCore/pull/3030)
- Tenants management improvements [#3009](https://github.com/OrchardCMS/OrchardCore/pull/3009)
- Prevent Notifier from displaying duplicite messages [#3017](https://github.com/OrchardCMS/OrchardCore/pull/3017)
- Fix view names for Admin menu deployment step [#3021](https://github.com/OrchardCMS/OrchardCore/pull/3021)
- Remove the testing mode feature and replace it by automatic signing certificate generation [#2886](https://github.com/OrchardCMS/OrchardCore/pull/2886)
- Google Analytics [#2934](https://github.com/OrchardCMS/OrchardCore/pull/2934)
- Change Smtp DefaultSender input to text [#3003](https://github.com/OrchardCMS/OrchardCore/pull/3003)
- Patching Google+ [#2996](https://github.com/OrchardCMS/OrchardCore/pull/2996)
- Introduce a role service relying on Identity's RoleManager and update the OpenID module to use it [#2872](https://github.com/OrchardCMS/OrchardCore/pull/2872)
- Localizations files search paths [#2986](https://github.com/OrchardCMS/OrchardCore/pull/2986)
- Fix TextField Editors options [#2994](https://github.com/OrchardCMS/OrchardCore/pull/2994)
- Fixes admin menu animations [#2992](https://github.com/OrchardCMS/OrchardCore/pull/2992)
- Add documentation on adding html attributes on img_tag liquid filter [#2989](https://github.com/OrchardCMS/OrchardCore/pull/2989)
- Basic health check [#2976](https://github.com/OrchardCMS/OrchardCore/pull/2976)
- Renaming Admin Tree to Admin Menu [#2923](https://github.com/OrchardCMS/OrchardCore/pull/2923)
- Optimize modules loading. [#2972](https://github.com/OrchardCMS/OrchardCore/pull/2972)
- Fixes multiple tenant shells initialization. [#2981](https://github.com/OrchardCMS/OrchardCore/pull/2981)
- Prevent liquid tag helper conflicts. [#2973](https://github.com/OrchardCMS/OrchardCore/pull/2973)
- Fix permission issue [#2979](https://github.com/OrchardCMS/OrchardCore/pull/2979)
- Fixed importing roles from setup recipes using existing documentation [#2969](https://github.com/OrchardCMS/OrchardCore/pull/2969)
- Added the gap between "Add User" button and "Search" box in mobile view. [#2938](https://github.com/OrchardCMS/OrchardCore/pull/2938)
- Added authorization check prior to creating new document. [#2968](https://github.com/OrchardCMS/OrchardCore/pull/2968)
- Text field editors [#2946](https://github.com/OrchardCMS/OrchardCore/pull/2946)
- [#2928](https://github.com/OrchardCMS/OrchardCore/pull/2928) fixed Azure blob storage basepath issue [#2948](https://github.com/OrchardCMS/OrchardCore/pull/2948)
- Fix Coming Soon: Missing Media feature [#2950](https://github.com/OrchardCMS/OrchardCore/pull/2950)
- Fixes url host and prefix in bg tasks [#2957](https://github.com/OrchardCMS/OrchardCore/pull/2957)
- Use AspNetCoreModuleV2 in mvc application. [#2958](https://github.com/OrchardCMS/OrchardCore/pull/2958)
- Fixing small UI issues [#2961](https://github.com/OrchardCMS/OrchardCore/pull/2961)
- Coming soon: Fix paths [#2937](https://github.com/OrchardCMS/OrchardCore/pull/2937)
- Fixes Razor Pages and Routing issues since 2.2 [#2940](https://github.com/OrchardCMS/OrchardCore/pull/2940)
- Google Authentication [#2920](https://github.com/OrchardCMS/OrchardCore/pull/2920)
- Fix media deployment [#2922](https://github.com/OrchardCMS/OrchardCore/pull/2922)
- Replace "facebook" by Azure AD [#2924](https://github.com/OrchardCMS/OrchardCore/pull/2924)
- Fix overflow in media modal [#2927](https://github.com/OrchardCMS/OrchardCore/pull/2927)
- Fixing Workflow items z-index [#2921](https://github.com/OrchardCMS/OrchardCore/pull/2921)
- Design : Admin Menu [#2819](https://github.com/OrchardCMS/OrchardCore/pull/2819)
- Admin Tree : fine tuning styling [#2919](https://github.com/OrchardCMS/OrchardCore/pull/2919)
- Fixing workflow edition [#2914](https://github.com/OrchardCMS/OrchardCore/pull/2914)
- ClockExtensions creates dateTimeUtc variable and ignores it [#2913](https://github.com/OrchardCMS/OrchardCore/pull/2913)
- Adding response compression module [#2911](https://github.com/OrchardCMS/OrchardCore/pull/2911)
- Placement match providers [#2864](https://github.com/OrchardCMS/OrchardCore/pull/2864)
- Building only merge commits [#2907](https://github.com/OrchardCMS/OrchardCore/pull/2907)
- Fix text wrap for long filenames in media table view [#2906](https://github.com/OrchardCMS/OrchardCore/pull/2906)
- Improve the HTTPS module [#2719](https://github.com/OrchardCMS/OrchardCore/pull/2719)
- Fixing popper.js usage [#2897](https://github.com/OrchardCMS/OrchardCore/pull/2897)
- Revert html body part's wysiwyg toolbar to be always visible [#2905](https://github.com/OrchardCMS/OrchardCore/pull/2905)
- Appveyor script maintenance [#2899](https://github.com/OrchardCMS/OrchardCore/pull/2899)
- Update assets references to use app-relative paths [#2893](https://github.com/OrchardCMS/OrchardCore/pull/2893)
- Fixing NRE when reading stereotype [#2888](https://github.com/OrchardCMS/OrchardCore/pull/2888)
- Fixes vue multiselect z-index [#2896](https://github.com/OrchardCMS/OrchardCore/pull/2896)
- Fixing Prefix leaks in ContentPartDisplayDriver [#2887](https://github.com/OrchardCMS/OrchardCore/pull/2887)
- Remove closing tags from <input> self-closing element [#2883](https://github.com/OrchardCMS/OrchardCore/pull/2883)
- Fixing OpenId applications creation [#2884](https://github.com/OrchardCMS/OrchardCore/pull/2884)
- Fixing vulnerability warnings in themes [#2868](https://github.com/OrchardCMS/OrchardCore/pull/2868)
- Registering Manage tenants Permissions [#2871](https://github.com/OrchardCMS/OrchardCore/pull/2871)



# Orchard Core 1.0.0-rc1

Release date: September 24, 2019  

## Breaking Changes

- .NET Core 3.0

## Milestone

[RC](https://github.com/OrchardCMS/OrchardCore/milestone/2)

## Enhancements

- Update Orchard Core to rc1 [#4370](https://github.com/OrchardCMS/OrchardCore/pull/4370)
- Allows shared views across tenants. [#4382](https://github.com/OrchardCMS/OrchardCore/pull/4382)
- Useless registration [#4366](https://github.com/OrchardCMS/OrchardCore/pull/4366)
- Using widgetlist.edit.css for Flow and Layers [#4378](https://github.com/OrchardCMS/OrchardCore/pull/4378)
- OrchardCore.Translations.All-beta -> OrchardCore.Translations.All-rc1 [#4371](https://github.com/OrchardCMS/OrchardCore/pull/4371)
- Fix razor options when no 'refs' folder exists. [#4379](https://github.com/OrchardCMS/OrchardCore/pull/4379)
- Fallback to Detail display type for bag parts [#4376](https://github.com/OrchardCMS/OrchardCore/pull/4376)
- Loading all po files from localization folders [#4375](https://github.com/OrchardCMS/OrchardCore/pull/4375)
- Update to .NET Core 3.0 [#4373](https://github.com/OrchardCMS/OrchardCore/pull/4373)
- Msbuild target to copy translation files. [#4346](https://github.com/OrchardCMS/OrchardCore/pull/4346)
- ModifiedUtc & PublishedUtc should take into account when recipe runs [#4279](https://github.com/OrchardCMS/OrchardCore/pull/4279)
- Add contentitem tag helper and liquid tag [#4360](https://github.com/OrchardCMS/OrchardCore/pull/4360)
- Fixes MiniProfiler [#4357](https://github.com/OrchardCMS/OrchardCore/pull/4357)
- Support for validation error class [#4355](https://github.com/OrchardCMS/OrchardCore/pull/4355)
- Handle standard Startup class [#4348](https://github.com/OrchardCMS/OrchardCore/pull/4348)
- Adding links to videos for decouple and headless [#4362](https://github.com/OrchardCMS/OrchardCore/pull/4362)
- Fixes [#4342](https://github.com/OrchardCMS/OrchardCore/pull/4342) [#4363](https://github.com/OrchardCMS/OrchardCore/pull/4363)
- Fix List Items route [#4350](https://github.com/OrchardCMS/OrchardCore/pull/4350)
- Import model state IPageFilter implementation for Forms module. [#4337](https://github.com/OrchardCMS/OrchardCore/pull/4337)
- Upgrade Fluid [#4344](https://github.com/OrchardCMS/OrchardCore/pull/4344)
- Register Content Parts and Fields in ContentOptions [#4335](https://github.com/OrchardCMS/OrchardCore/pull/4335)
- Security Critical Permissions [#4267](https://github.com/OrchardCMS/OrchardCore/pull/4267)
- Introducing FullTextAspect [#4012](https://github.com/OrchardCMS/OrchardCore/pull/4012)
- Format dependent features in disable feature dialog [#4278](https://github.com/OrchardCMS/OrchardCore/pull/4278)
- Regression fix: bootstrap confirm modal [#4336](https://github.com/OrchardCMS/OrchardCore/pull/4336)
- Fixing OrchardCore.Localization dependencies [#4320](https://github.com/OrchardCMS/OrchardCore/pull/4320)
- Removing dependencies on NETStandard.Library [#4328](https://github.com/OrchardCMS/OrchardCore/pull/4328)
- Remove workflow-menu.css and  remove dup'd images. [#4325](https://github.com/OrchardCMS/OrchardCore/pull/4325)
- Add translation metapackage to Cms.Targets [#4323](https://github.com/OrchardCMS/OrchardCore/pull/4323)
- StringBuilder best practices [#4318](https://github.com/OrchardCMS/OrchardCore/pull/4318)
- Fixes ConfiguredFeaturesShellDescriptorManager registration. [#4322](https://github.com/OrchardCMS/OrchardCore/pull/4322)
- Prettify Admin Menus page [#4307](https://github.com/OrchardCMS/OrchardCore/pull/4307)
- Prettify Queries page [#4305](https://github.com/OrchardCMS/OrchardCore/pull/4305)
- Add alert if no tenants found on search result [#4302](https://github.com/OrchardCMS/OrchardCore/pull/4302)
- result -> results [#4314](https://github.com/OrchardCMS/OrchardCore/pull/4314)
- Add alert if no features found on search result [#4301](https://github.com/OrchardCMS/OrchardCore/pull/4301)
- Add alert if no recipes found on search result [#4300](https://github.com/OrchardCMS/OrchardCore/pull/4300)
- Regression fix : ContentPickerField [#4282](https://github.com/OrchardCMS/OrchardCore/pull/4282)
- Page endpoint priority. [#4299](https://github.com/OrchardCMS/OrchardCore/pull/4299)
- LangVersion property is no more necessary [#4295](https://github.com/OrchardCMS/OrchardCore/pull/4295)
- Update ASP.NET dependencies to 3.0 RC1 [#4294](https://github.com/OrchardCMS/OrchardCore/pull/4294)
- Add default paging to GraphQL queries [#4291](https://github.com/OrchardCMS/OrchardCore/pull/4291)
- Updating default logging settings [#4296](https://github.com/OrchardCMS/OrchardCore/pull/4296)
- Fix ResourceManager dependency resolution [#4293](https://github.com/OrchardCMS/OrchardCore/pull/4293)
- WIP Optimize ResourceManager [#4292](https://github.com/OrchardCMS/OrchardCore/pull/4292)
- Migrate all Content Type / Part / Field Settings to Settings<T> [#4166](https://github.com/OrchardCMS/OrchardCore/pull/4166)
- Update vscode launch.json for core 3.0 [#4290](https://github.com/OrchardCMS/OrchardCore/pull/4290)
- Fix permission issue with PublishContent [#4286](https://github.com/OrchardCMS/OrchardCore/pull/4286)
- Fixes HomeRoute if no home route. [#4284](https://github.com/OrchardCMS/OrchardCore/pull/4284)
- CultureAspect must work for localization & content localization modules [#4258](https://github.com/OrchardCMS/OrchardCore/pull/4258)
- Diagnostics ISartupFilter to add a middleware before the routing one [#4264](https://github.com/OrchardCMS/OrchardCore/pull/4264)
- Update ImageProvider to work better with new ImageSharp version [#4254](https://github.com/OrchardCMS/OrchardCore/pull/4254)
- Use AddInitialRequestCultureProvider [#4266](https://github.com/OrchardCMS/OrchardCore/pull/4266)
- Update MediaField-Attached.Edit.cshtml [#4269](https://github.com/OrchardCMS/OrchardCore/pull/4269)
- Fixes razor pages and autoroutes conflicts. [#4272](https://github.com/OrchardCMS/OrchardCore/pull/4272)
- Update dependencies [#4274](https://github.com/OrchardCMS/OrchardCore/pull/4274)
- Fix media table valign [#4276](https://github.com/OrchardCMS/OrchardCore/pull/4276)
- Fixes NotFound page if not overridden in the current theme. [#4263](https://github.com/OrchardCMS/OrchardCore/pull/4263)
- Prettify Roles page [#4240](https://github.com/OrchardCMS/OrchardCore/pull/4240)
- Content Part creation : regression fix [#4262](https://github.com/OrchardCMS/OrchardCore/pull/4262)
- Migration to dotnet core 3.0 [#3398](https://github.com/OrchardCMS/OrchardCore/pull/3398)
- Some performance tweaks [#4251](https://github.com/OrchardCMS/OrchardCore/pull/4251)
- Prettify Users page [#4241](https://github.com/OrchardCMS/OrchardCore/pull/4241)
- Allows core shapes to be overridden [#4210](https://github.com/OrchardCMS/OrchardCore/pull/4210)
- Use proper BS4 classes for the login remember me checkbox. [#4245](https://github.com/OrchardCMS/OrchardCore/pull/4245)
- Upgrade ImageSharp.Web to v1.0.0-beta9 [#4167](https://github.com/OrchardCMS/OrchardCore/pull/4167)
- Liquid filter and tags to mutate shape properties [#4193](https://github.com/OrchardCMS/OrchardCore/pull/4193)
- Fix VueMultiselect issue with Widgets [#4225](https://github.com/OrchardCMS/OrchardCore/pull/4225)
- Azure Blob w/resizing [#4025](https://github.com/OrchardCMS/OrchardCore/pull/4025)
- Prettify content parts page [#4221](https://github.com/OrchardCMS/OrchardCore/pull/4221)
- Prettify content types page [#4220](https://github.com/OrchardCMS/OrchardCore/pull/4220)
- Using strongly typed content type setting [#4180](https://github.com/OrchardCMS/OrchardCore/pull/4180)
- Customize bootstrap confirm modal [#4181](https://github.com/OrchardCMS/OrchardCore/pull/4181)
- Add user arguments to Login events [#4182](https://github.com/OrchardCMS/OrchardCore/pull/4182)
- Update Https and Reverse Proxy setting sort orders [#4189](https://github.com/OrchardCMS/OrchardCore/pull/4189)
- Access to dynamic Reusable part. [#4192](https://github.com/OrchardCMS/OrchardCore/pull/4192)
- Add permission to ContentCulturePicker setting [#4194](https://github.com/OrchardCMS/OrchardCore/pull/4194)
- Use bootstrap confirm modal in assets page [#4207](https://github.com/OrchardCMS/OrchardCore/pull/4207)
- Fix TextAreaPart not using submitted form value [#4218](https://github.com/OrchardCMS/OrchardCore/pull/4218)
- Add CultureInfo to Liquid TemplateContext [#4219](https://github.com/OrchardCMS/OrchardCore/pull/4219)
- Import jquery-ui-override into TheAdmin.scss [#4196](https://github.com/OrchardCMS/OrchardCore/pull/4196)
- Update build dependencies + npm i + build [#4187](https://github.com/OrchardCMS/OrchardCore/pull/4187)
- Fix# 4168 : WidgetsListPart - Existing widgets are removed due to Null Zone [#4183](https://github.com/OrchardCMS/OrchardCore/pull/4183)
- Prettify recipes page [#4179](https://github.com/OrchardCMS/OrchardCore/pull/4179)
- Prettify Features page [#4176](https://github.com/OrchardCMS/OrchardCore/pull/4176)
- Change models namespace everywhere [#4173](https://github.com/OrchardCMS/OrchardCore/pull/4173)
- Fix typo on GitHub menus [#4066](https://github.com/OrchardCMS/OrchardCore/pull/4066)
- Remove rtl generation from front end theme related assets  [#4171](https://github.com/OrchardCMS/OrchardCore/pull/4171)
- Polish Tenants page [#4156](https://github.com/OrchardCMS/OrchardCore/pull/4156)
- Show/hide external logins in SaaS recipe [#4152](https://github.com/OrchardCMS/OrchardCore/pull/4152)
- Make OrchardCore.ContentFields.Indexing.SQL require OrchardCore.ContentFields [#4149](https://github.com/OrchardCMS/OrchardCore/pull/4149)
- Clean double encoding [#4150](https://github.com/OrchardCMS/OrchardCore/pull/4150)
- Taxonomy field required validation doesn't work with unique options [#4145](https://github.com/OrchardCMS/OrchardCore/pull/4145)
- Apply cache control headers to non-resized images or other assets served from the media file store with the Static File Middleware [#4135](https://github.com/OrchardCMS/OrchardCore/pull/4135)
- Some menu tweaks [#4132](https://github.com/OrchardCMS/OrchardCore/pull/4132)
- Add Properties Dictionary to IShape interface [#4131](https://github.com/OrchardCMS/OrchardCore/pull/4131)
- Editor direction should respect the localization part culture [#4039](https://github.com/OrchardCMS/OrchardCore/pull/4039)
- Content fields indexing [#3133](https://github.com/OrchardCMS/OrchardCore/pull/3133)
- Increased graphql default maxdepth to allow graphiql introspection query to run. [#4144](https://github.com/OrchardCMS/OrchardCore/pull/4144)
- Remove duplicate resource settings [#4137](https://github.com/OrchardCMS/OrchardCore/pull/4137)
- Make setting the page title format accessible to site administrators [#3401](https://github.com/OrchardCMS/OrchardCore/pull/3401)
- Add LocalizationSetContentPickerField [#3819](https://github.com/OrchardCMS/OrchardCore/pull/3819)
- List localization [#3891](https://github.com/OrchardCMS/OrchardCore/pull/3891)
- Remove unnecessary dependencies [#4072](https://github.com/OrchardCMS/OrchardCore/pull/4072)
- Sort groups alphabetically on Admin Features page [#4128](https://github.com/OrchardCMS/OrchardCore/pull/4128)
- Workflows Internationalization [#3634](https://github.com/OrchardCMS/OrchardCore/pull/3634)
- Handle UnauthorizedResult ([#3209](https://github.com/OrchardCMS/OrchardCore/pull/3209)) [#3215](https://github.com/OrchardCMS/OrchardCore/pull/3215)
- Add README.md to health check [#3010](https://github.com/OrchardCMS/OrchardCore/pull/3010)
- Add support for typed shape tag helper properties [#4114](https://github.com/OrchardCMS/OrchardCore/pull/4114)
- Remove IHttpContextAccessor from ResourceManager [#4120](https://github.com/OrchardCMS/OrchardCore/pull/4120)
- Add example for ContentPickerField [#4122](https://github.com/OrchardCMS/OrchardCore/pull/4122)
- GraphQL: Don't include ignored contenttype fields in where filters [#3832](https://github.com/OrchardCMS/OrchardCore/pull/3832)
- Rollback transaction during indexing [#3823](https://github.com/OrchardCMS/OrchardCore/pull/3823)
- GraphQL - allowed configuration for max depth/complexity and fieldimpact [#3879](https://github.com/OrchardCMS/OrchardCore/pull/3879)
- Fixes Pager in the home page [#4115](https://github.com/OrchardCMS/OrchardCore/pull/4115)
- Update run-code-on-startup example and formatting [#4117](https://github.com/OrchardCMS/OrchardCore/pull/4117)
- Add ORCHARD_APP_DATA Environment Variable section [#4116](https://github.com/OrchardCMS/OrchardCore/pull/4116)
- Refactor culture picker shape [#4111](https://github.com/OrchardCMS/OrchardCore/pull/4111)
- Localization files publishing [#4088](https://github.com/OrchardCMS/OrchardCore/pull/4088)
- Add Compare Attribute to PasswordConfirmation and validate ModelState in AdminController [#4099](https://github.com/OrchardCMS/OrchardCore/pull/4099)
- external links on README.md [#4103](https://github.com/OrchardCMS/OrchardCore/pull/4103)
- AliasPart index size [#4098](https://github.com/OrchardCMS/OrchardCore/pull/4098)
- Add liquid example for ContentCulturePicker [#4101](https://github.com/OrchardCMS/OrchardCore/pull/4101)
- README--add tutorial [#4108](https://github.com/OrchardCMS/OrchardCore/pull/4108)
- Documenttion of search query in new tab [#4102](https://github.com/OrchardCMS/OrchardCore/pull/4102)
- Implement IUserClaimStore to enable individual user claims. [#4070](https://github.com/OrchardCMS/OrchardCore/pull/4070)
- Localization Bugfix [#4078](https://github.com/OrchardCMS/OrchardCore/pull/4078)
- More async calls [#3930](https://github.com/OrchardCMS/OrchardCore/pull/3930)
- Move Localization folder out of App_Data [#4074](https://github.com/OrchardCMS/OrchardCore/pull/4074)
- Predefined List blank option fix [#4068](https://github.com/OrchardCMS/OrchardCore/pull/4068)
- Lucene indexation : convention on null field values [#4062](https://github.com/OrchardCMS/OrchardCore/pull/4062)
- add more detail step on README.md of OpenId [#4057](https://github.com/OrchardCMS/OrchardCore/pull/4057)
- Fix datepicker UI issue [#4050](https://github.com/OrchardCMS/OrchardCore/pull/4050)
- Fixes ToPascalCase [#4060](https://github.com/OrchardCMS/OrchardCore/pull/4060)
- Improve Kebab-casing performance [#4054](https://github.com/OrchardCMS/OrchardCore/pull/4054)
- Small refactors to Resources CDN and settings [#4044](https://github.com/OrchardCMS/OrchardCore/pull/4044)
- Using StringBuilder pooling from Fluid [#4047](https://github.com/OrchardCMS/OrchardCore/pull/4047)
- Updating Jint and Fluid [#4048](https://github.com/OrchardCMS/OrchardCore/pull/4048)
- Fix localization context issue in OrchardCore.Templates [#4042](https://github.com/OrchardCMS/OrchardCore/pull/4042)
- ContainedPart Index renaming [#4035](https://github.com/OrchardCMS/OrchardCore/pull/4035)
- Add a core CMS meta package [#4027](https://github.com/OrchardCMS/OrchardCore/pull/4027)
- Editing while reading: add a missing backtick and fix some typos [#4033](https://github.com/OrchardCMS/OrchardCore/pull/4033)
- Add sort on multiple fields for Lucene Queries [#4029](https://github.com/OrchardCMS/OrchardCore/pull/4029)
- Minor fixes [#3922](https://github.com/OrchardCMS/OrchardCore/pull/3922)
- BooleanField styling should match other fields [#4024](https://github.com/OrchardCMS/OrchardCore/pull/4024)
- Fix localized datepicker UI issue [#4002](https://github.com/OrchardCMS/OrchardCore/pull/4002)
- NullStringLocalizer shouldn't ignore formatted strings [#4019](https://github.com/OrchardCMS/OrchardCore/pull/4019)
- Indexes a Content.ContentItem.Parent field in Lucene for ContainedPart. [#4017](https://github.com/OrchardCMS/OrchardCore/pull/4017)
- Changing $zindex-sticky to 1000 instead of 1020 [#4023](https://github.com/OrchardCMS/OrchardCore/pull/4023)
- Display the workflow date with current timezone [#4003](https://github.com/OrchardCMS/OrchardCore/pull/4003)
- Adds Liquid Razor Extension Method & Markdown Helper parses liquid [#3992](https://github.com/OrchardCMS/OrchardCore/pull/3992)
- Added liquid support to markdown graphql query. [#4007](https://github.com/OrchardCMS/OrchardCore/pull/4007)
- Documentation to explain how to generate Po files [#3998](https://github.com/OrchardCMS/OrchardCore/pull/3998)
- Change Load Order of AntiforgeryToken [#3993](https://github.com/OrchardCMS/OrchardCore/pull/3993)
- Save hint text for link text [#3995](https://github.com/OrchardCMS/OrchardCore/pull/3995)
- Remove 'json' specified from GraphQL MD codeblocks [#3994](https://github.com/OrchardCMS/OrchardCore/pull/3994)
- Ability to extend/clear ContainedContentTypes. [#3978](https://github.com/OrchardCMS/OrchardCore/pull/3978)
- Updating yessql [#3988](https://github.com/OrchardCMS/OrchardCore/pull/3988)
- Make registered FB scripts virtual folder and tenant aware. [#3932](https://github.com/OrchardCMS/OrchardCore/pull/3932)
- Show connectionString hint for all data providers [#3484](https://github.com/OrchardCMS/OrchardCore/pull/3484)
- Plural extension should work with NullStringLocalizer [#3933](https://github.com/OrchardCMS/OrchardCore/pull/3933)
- Change label to "None" [#3965](https://github.com/OrchardCMS/OrchardCore/pull/3965)
- IShellConfiguration documentation [#3967](https://github.com/OrchardCMS/OrchardCore/pull/3967)
- Unpublish content should set modified datetime [#3972](https://github.com/OrchardCMS/OrchardCore/pull/3972)
- Admin scripts cache busting [#3960](https://github.com/OrchardCMS/OrchardCore/pull/3960)
- Bootstrap / Popper version  & cdn-integrity fixes [#3968](https://github.com/OrchardCMS/OrchardCore/pull/3968)
- Reload resource settings on update [#3971](https://github.com/OrchardCMS/OrchardCore/pull/3971)
- Graphql - make schema generation thread safe [#3935](https://github.com/OrchardCMS/OrchardCore/pull/3935)
- Bring back MediaSizeLimitAttribute [#3961](https://github.com/OrchardCMS/OrchardCore/pull/3961)
- Add permissions to localization & reverse proxy settings navigation [#3779](https://github.com/OrchardCMS/OrchardCore/pull/3779)
- Update style tag helper to use depends-on instead of dependencies [#3953](https://github.com/OrchardCMS/OrchardCore/pull/3953)
- ContentCulturePicker - Add ability to set Localization Cookie [#3894](https://github.com/OrchardCMS/OrchardCore/pull/3894)
- Add CustomSettings C# documentation [#3946](https://github.com/OrchardCMS/OrchardCore/pull/3946)
- Run AdminAttribute before any global filter with a default order of 0 [#3915](https://github.com/OrchardCMS/OrchardCore/pull/3915)
- Vue.js use proper CDN [#3920](https://github.com/OrchardCMS/OrchardCore/pull/3920)
- fix NRE on YoutubeFieldDisplayDriver when the field is not required [#3907](https://github.com/OrchardCMS/OrchardCore/pull/3907)
- NumericField (selectbox) not required fix [#3909](https://github.com/OrchardCMS/OrchardCore/pull/3909)
- Removing unnecessary styling on ReCaptcha [#3911](https://github.com/OrchardCMS/OrchardCore/pull/3911)
- Secure ContentPickerController with Admin filter [#3896](https://github.com/OrchardCMS/OrchardCore/pull/3896)
- ZoneOnDemand.AddAsync(). [#3864](https://github.com/OrchardCMS/OrchardCore/pull/3864)
- Add executeQuery GlobalMethod [#3903](https://github.com/OrchardCMS/OrchardCore/pull/3903)
- Role based permissions to display admin menus [#3875](https://github.com/OrchardCMS/OrchardCore/pull/3875)
- Prevents an antiforgery issue on setup. [#3622](https://github.com/OrchardCMS/OrchardCore/pull/3622)
- Fixes async call. [#3898](https://github.com/OrchardCMS/OrchardCore/pull/3898)
- Support single JTokenType.Object in BooleanQueryProvider [#3888](https://github.com/OrchardCMS/OrchardCore/pull/3888)
- Add permission for SearchController Api [#3883](https://github.com/OrchardCMS/OrchardCore/pull/3883)
- Prevent collisions with mvc scripttaghelper [#3886](https://github.com/OrchardCMS/OrchardCore/pull/3886)
- Update theme templates to use liquid filter on html fields [#3893](https://github.com/OrchardCMS/OrchardCore/pull/3893)
- LocalizationSettings recipe step documentation [#3895](https://github.com/OrchardCMS/OrchardCore/pull/3895)
- Adds asp-append-version support [#3581](https://github.com/OrchardCMS/OrchardCore/pull/3581)
- Content Culture Picker [#3813](https://github.com/OrchardCMS/OrchardCore/pull/3813)
- Localize setup screen [#3512](https://github.com/OrchardCMS/OrchardCore/pull/3512)
- Update Permissions [#3816](https://github.com/OrchardCMS/OrchardCore/pull/3816)
- Add pathbase. [#3857](https://github.com/OrchardCMS/OrchardCore/pull/3857)
- Add a .vsconfig file for easier provisioning when using VS 2019 [#3691](https://github.com/OrchardCMS/OrchardCore/pull/3691)
- Added grouping of widgets to their site layer. [#3873](https://github.com/OrchardCMS/OrchardCore/pull/3873)
- Always do a complete Liquid contextualization. [#3851](https://github.com/OrchardCMS/OrchardCore/pull/3851)
- Small improvement to ImageSharp pipeline [#3854](https://github.com/OrchardCMS/OrchardCore/pull/3854)
- Set content types during azure blob creation [#3856](https://github.com/OrchardCMS/OrchardCore/pull/3856)
- Fix misspelling (occured -> occurred) [#3858](https://github.com/OrchardCMS/OrchardCore/pull/3858)
- Implemented siteLayers graphql query. [#3861](https://github.com/OrchardCMS/OrchardCore/pull/3861)
- Implemented siteCultures graphql query. [#3863](https://github.com/OrchardCMS/OrchardCore/pull/3863)
- PluralRule is null for locale not recognized. [#3836](https://github.com/OrchardCMS/OrchardCore/pull/3836)
- Trumbowyg Semantic Defaults - div : div [#3843](https://github.com/OrchardCMS/OrchardCore/pull/3843)
- Rename Package.json -> package.json [#3822](https://github.com/OrchardCMS/OrchardCore/pull/3822)
- updated getting started guide, and remove missing file from OrchardCore.sln [#3830](https://github.com/OrchardCMS/OrchardCore/pull/3830)
- Create correct ContentZone for tab support when UpdateEditorAsync is called [#3845](https://github.com/OrchardCMS/OrchardCore/pull/3845)
- Clarify that Differentiator is the menu name (title). [#3424](https://github.com/OrchardCMS/OrchardCore/pull/3424)
- Order ContentPicker items by DisplayText [#3808](https://github.com/OrchardCMS/OrchardCore/pull/3808)
- Fixes WidgetsList delete [#3814](https://github.com/OrchardCMS/OrchardCore/pull/3814)
- Localize date picker [#3707](https://github.com/OrchardCMS/OrchardCore/pull/3707)
- Log invalid SMTP certificate info [#3806](https://github.com/OrchardCMS/OrchardCore/pull/3806)
- Return HasPublished in ContentPickerResult when used with Lucene. [#3804](https://github.com/OrchardCMS/OrchardCore/pull/3804)
- Update Permissions.cs [#3786](https://github.com/OrchardCMS/OrchardCore/pull/3786)
- Added media assets graphql query support. [#3784](https://github.com/OrchardCMS/OrchardCore/pull/3784)
- Add 'view' button to media library items [#3787](https://github.com/OrchardCMS/OrchardCore/pull/3787)
- Remove dead code [#3783](https://github.com/OrchardCMS/OrchardCore/pull/3783)
- Fixes liquid controller views. [#3777](https://github.com/OrchardCMS/OrchardCore/pull/3777)
- Link to the rendered pages on readthedocs [#3785](https://github.com/OrchardCMS/OrchardCore/pull/3785)
- Fix broken link in ContentLocalization when no cultures are installed [#3782](https://github.com/OrchardCMS/OrchardCore/pull/3782)
- Add documentation for overriding Views [#3778](https://github.com/OrchardCMS/OrchardCore/pull/3778)
- Async tweaks [#3770](https://github.com/OrchardCMS/OrchardCore/pull/3770)
- Working on shell scopes. [#3178](https://github.com/OrchardCMS/OrchardCore/pull/3178)
- Update shell container creation. [#3467](https://github.com/OrchardCMS/OrchardCore/pull/3467)
- Clear content item element cache when updating a field [#3764](https://github.com/OrchardCMS/OrchardCore/pull/3764)
- Extend Facebook Documentation [#3774](https://github.com/OrchardCMS/OrchardCore/pull/3774)
- Non awaited async call [#3769](https://github.com/OrchardCMS/OrchardCore/pull/3769)
- Update SimpleMDE repo link [#3768](https://github.com/OrchardCMS/OrchardCore/pull/3768)



# Orchard Core 1.0.0-rc2

Release date: June 12, 2020  

## Breaking Changes

- .NET Core 3.1
- Change to the default BagPart from Detail to Summary.
- Email now is differentiate between submitter and sender according to RFC
- Lucene index settings are now stored in the database and the data JSON schema has changed so it is required to reconfigure the indices.

## Milestone

[RC2](https://github.com/OrchardCMS/OrchardCore/milestone/10)

## New features

- New orchardcore.net domain (docs, try)
- New Admin UI for bulk actions
- New Admin menu structure
- New documentation structure
- Docs project in the solution
- Upgrade to MkDocs Material 5
- Use all-contributors to generate Contributors list
- Customize admin URL prefix
- Deployment plan Recipe export
- Full-text search enhancements
- Open Tags editor in Taxonomies
- Contained item routing
- Content Picker Menu
- Language selector on setup page
- Screen setup adapted to small resolutions
- Default pattern for autoroute and alias
- Display mode options
- Filter admin menu
- Flow editor UI improvements
- Toggle all widgets button
- Sorting items in ListPart
- Retrieve, Update Content workflow task
- Disable and Enable Tenant Workflows Tasks
- User disabled/enabled events
- Users can change email
- Disable a user account
- Allow Inserting image in HTML
- Themes with vendor- prefix
- ConsoleLog helper
- Preview feature improvement
- Trumbowyg editor, settings and plugins
- Add ability to generate DisplayText with a Pattern
- Database and Azure blob shells configuration
- External Login registration without password
- CodeMirror editor for TextField
- Export to json or send to remote
- Publish later
- Recipe idempotency
- Sitemaps

## Enhancements

- Use rc2 version in docs [#6403](https://github.com/OrchardCMS/OrchardCore/pull/6403)
- Release/rc2 [#6399](https://github.com/OrchardCMS/OrchardCore/pull/6399)
- ImageSharp license changes [#6395](https://github.com/OrchardCMS/OrchardCore/pull/6395)
- Update template generation docs [#6391](https://github.com/OrchardCMS/OrchardCore/pull/6391)
- Initialize setup supported cultures only if there is a meta package [#6357](https://github.com/OrchardCMS/OrchardCore/pull/6357)
- Upgrade ImageSharp package [#6375](https://github.com/OrchardCMS/OrchardCore/pull/6375)
- Reset twitter client [#6379](https://github.com/OrchardCMS/OrchardCore/pull/6379)
- .NET Core 3.1.5 and SDK 3.1.301 [#6387](https://github.com/OrchardCMS/OrchardCore/pull/6387)
- Fix resource hash for code mirror css [#6384](https://github.com/OrchardCMS/OrchardCore/pull/6384)
- Update OrchardCore_Shells_Database docs [#6380](https://github.com/OrchardCMS/OrchardCore/pull/6380)
- Add reference doc pages for missing features (Lombiq Technologies: OCORE-30) [#6350](https://github.com/OrchardCMS/OrchardCore/pull/6350)
- Docs contrib guide, MkDocs fixes, clarifying Configuration docs [#6281](https://github.com/OrchardCMS/OrchardCore/pull/6281)
- Coming soon theme fixes [#6346](https://github.com/OrchardCMS/OrchardCore/pull/6346)
- Reviewing encoders usages [#6330](https://github.com/OrchardCMS/OrchardCore/pull/6330)
- Add default edit display option [#6339](https://github.com/OrchardCMS/OrchardCore/pull/6339)
- Disable requried. move fields to below larger editors [#6340](https://github.com/OrchardCMS/OrchardCore/pull/6340)
- Fix Publish Later controls disappearing on validation error [#6337](https://github.com/OrchardCMS/OrchardCore/pull/6337)
- Adding branding assets to docs [#6282](https://github.com/OrchardCMS/OrchardCore/pull/6282)
- Allow classes by default with the html sanitizer [#6268](https://github.com/OrchardCMS/OrchardCore/pull/6268)
- Add ConfirmationEmailSubject in Edit RegisterUserTask [#6322](https://github.com/OrchardCMS/OrchardCore/pull/6322)
- Prevent array duplication when merging existing content [#6315](https://github.com/OrchardCMS/OrchardCore/pull/6315)
- Change to [image] tag. Make recursive [#6301](https://github.com/OrchardCMS/OrchardCore/pull/6301)
- Comong-soon script [#6304](https://github.com/OrchardCMS/OrchardCore/pull/6304)
- Change content api permissions [#6225](https://github.com/OrchardCMS/OrchardCore/pull/6225)
- Render nested bags in Summary also [#6288](https://github.com/OrchardCMS/OrchardCore/pull/6288)
- Preview package source to to docs [#6278](https://github.com/OrchardCMS/OrchardCore/pull/6278)
- Fixes FileSystemStore issues [#6272](https://github.com/OrchardCMS/OrchardCore/pull/6272) [#6277](https://github.com/OrchardCMS/OrchardCore/pull/6277)
- Themes: Title, default theme screenshot and tags [#6273](https://github.com/OrchardCMS/OrchardCore/pull/6273)
- MimeKit dependency [#6275](https://github.com/OrchardCMS/OrchardCore/pull/6275)
- Safe Mode Theme [#6261](https://github.com/OrchardCMS/OrchardCore/pull/6261)
- Update code generation templates [#6274](https://github.com/OrchardCMS/OrchardCore/pull/6274)
- Replace input by textarea in HtmlField.Edit [#6262](https://github.com/OrchardCMS/OrchardCore/pull/6262)
- Update session save usage [#6257](https://github.com/OrchardCMS/OrchardCore/pull/6257)
- Updating preview feed badge to Cloudsmith and adding the root Readme to the solution too [#6266](https://github.com/OrchardCMS/OrchardCore/pull/6266)
- Upgrade Npm packages [#6251](https://github.com/OrchardCMS/OrchardCore/pull/6251)
- Code Mirror 5.54.0 [#6256](https://github.com/OrchardCMS/OrchardCore/pull/6256)
- add service provider to shape creating/created contexts [#6250](https://github.com/OrchardCMS/OrchardCore/pull/6250)
- Update Fluid and YesSql [#6248](https://github.com/OrchardCMS/OrchardCore/pull/6248)
- Favicon for light and dark browser tabs [#6241](https://github.com/OrchardCMS/OrchardCore/pull/6241)
- Use optional param for CultureDictionary indexer [#6201](https://github.com/OrchardCMS/OrchardCore/pull/6201)
- Add constructor overload to CultureDictionaryRecord [#6200](https://github.com/OrchardCMS/OrchardCore/pull/6200)
- Fix typo ContentDeletedEvent constructor [#6222](https://github.com/OrchardCMS/OrchardCore/pull/6222)
- SDK 3.1.300 [#6220](https://github.com/OrchardCMS/OrchardCore/pull/6220)
- Html Script sanitizer [#6016](https://github.com/OrchardCMS/OrchardCore/pull/6016)
- Fixes DB Lock / Timeout in DeferredTask [#6170](https://github.com/OrchardCMS/OrchardCore/pull/6170)
- Allow a Timer waiting activity in any Workflow [#6124](https://github.com/OrchardCMS/OrchardCore/pull/6124)
- Little refactoring and cleanup [#6142](https://github.com/OrchardCMS/OrchardCore/pull/6142)
- Fixes Workflow Singleton [#6156](https://github.com/OrchardCMS/OrchardCore/pull/6156)
- Need a tilde if under a virtual folder [#6186](https://github.com/OrchardCMS/OrchardCore/pull/6186)
- Mark publish later with private assets [#6198](https://github.com/OrchardCMS/OrchardCore/pull/6198)
- Update .NET Core to 3.1.4 and SDK to 3.1.202 [#6181](https://github.com/OrchardCMS/OrchardCore/pull/6181)
- Revert "Added support for @section syntax for Views [#5413](https://github.com/OrchardCMS/OrchardCore/pull/5413)
- Trigger WF Content Versioned Event [#6131](https://github.com/OrchardCMS/OrchardCore/pull/6131)
- Update docker images [#6094](https://github.com/OrchardCMS/OrchardCore/pull/6094)
- Update version to RC2 [#6093](https://github.com/OrchardCMS/OrchardCore/pull/6093)
- Update version to rc2 in docs and templates example [#6091](https://github.com/OrchardCMS/OrchardCore/pull/6091)
- Remove permission check on custom settings recipe step [#6086](https://github.com/OrchardCMS/OrchardCore/pull/6086)
- PublishLater review [#6127](https://github.com/OrchardCMS/OrchardCore/pull/6127)
- Fix liquid filter doc [#6166](https://github.com/OrchardCMS/OrchardCore/pull/6166)
- Added support for @section syntax for Views [#5413](https://github.com/OrchardCMS/OrchardCore/pull/5413)
- Add formatting option to json filter [#6165](https://github.com/OrchardCMS/OrchardCore/pull/6165)
- Upgrade Bootstrap Select to 1.13.17 [#6160](https://github.com/OrchardCMS/OrchardCore/pull/6160)
- Upgrade dependencies Azure.Storage.Blobs and Castle.Core [#6163](https://github.com/OrchardCMS/OrchardCore/pull/6163)
- Configure Dev package source [#6150](https://github.com/OrchardCMS/OrchardCore/pull/6150)
- Update Manifest descriptions [#6155](https://github.com/OrchardCMS/OrchardCore/pull/6155)
- AdminMenu doc with PrefixPosition [#6152](https://github.com/OrchardCMS/OrchardCore/pull/6152)
- Switch buttons Events and Tasks in Workflow Edit [#6154](https://github.com/OrchardCMS/OrchardCore/pull/6154)
- Revisit Workflow Queries [#6144](https://github.com/OrchardCMS/OrchardCore/pull/6144)
- Update Doc Screenshots [#6153](https://github.com/OrchardCMS/OrchardCore/pull/6153)
- Fixing inconsistent internal docs links (half of them was referring to a Readme file, half not) and fixing several broken links too [#6146](https://github.com/OrchardCMS/OrchardCore/pull/6146)
- Add docs folder and project to solution [#6118](https://github.com/OrchardCMS/OrchardCore/pull/6118)
- Fixes [#6125](https://github.com/OrchardCMS/OrchardCore/pull/6125) bulk actions [#6130](https://github.com/OrchardCMS/OrchardCore/pull/6130)
- Add Scheduled Publish functionality (Lombiq Technologies: OCORE-16) [#5639](https://github.com/OrchardCMS/OrchardCore/pull/5639)
- Resolve potential media key conflicts [#5979](https://github.com/OrchardCMS/OrchardCore/pull/5979)
- Update Workflows dependencies [#6111](https://github.com/OrchardCMS/OrchardCore/pull/6111)
- an issue with table formatting in OrchardCore.Menu [#6117](https://github.com/OrchardCMS/OrchardCore/pull/6117)
- Upgrade Lucene.Net to beta 8 [#6108](https://github.com/OrchardCMS/OrchardCore/pull/6108)
- Fixes [#5987](https://github.com/OrchardCMS/OrchardCore/pull/5987): WF Activity infinite loop [#6107](https://github.com/OrchardCMS/OrchardCore/pull/6107)
- Fixes bulk actions filtering [#6106](https://github.com/OrchardCMS/OrchardCore/pull/6106)
- Maintain widget content item ids across flowpart and widget list part when updating [#5989](https://github.com/OrchardCMS/OrchardCore/pull/5989)
- Document activate-links and extend functionality for nested menu items and action urls [#6090](https://github.com/OrchardCMS/OrchardCore/pull/6090)
- Preserve external authentication tokens [#6057](https://github.com/OrchardCMS/OrchardCore/pull/6057)
- Fix login redirect for external providers [#6109](https://github.com/OrchardCMS/OrchardCore/pull/6109)
- Upgrade dependencies [#6110](https://github.com/OrchardCMS/OrchardCore/pull/6110)
- Upgrade mkdocs material [#6112](https://github.com/OrchardCMS/OrchardCore/pull/6112)
- Update bootstrap-select to 1.13.16 [#6101](https://github.com/OrchardCMS/OrchardCore/pull/6101)
- Set isNew to true only for ajax requests [#6084](https://github.com/OrchardCMS/OrchardCore/pull/6084)
- Revert "Fix login redirect for external providers [#6072](https://github.com/OrchardCMS/OrchardCore/pull/6072)
- Make Import Data a security critical permission [#6087](https://github.com/OrchardCMS/OrchardCore/pull/6087)
- Update configuration docs [#6045](https://github.com/OrchardCMS/OrchardCore/pull/6045)
- Revert "set isNew to true when buidling editor [#6077](https://github.com/OrchardCMS/OrchardCore/pull/6077)
- Add Content Menu Item [#4632](https://github.com/OrchardCMS/OrchardCore/pull/4632)
- Fix login redirect for external providers [#6072](https://github.com/OrchardCMS/OrchardCore/pull/6072)
- set isNew to true when buidling editor [#6077](https://github.com/OrchardCMS/OrchardCore/pull/6077)
- Make Content Recipe Step Idempotent [#5487](https://github.com/OrchardCMS/OrchardCore/pull/5487)
- Update version and website in Manifests and recipes [#5905](https://github.com/OrchardCMS/OrchardCore/pull/5905)
- Upgrade ImageSharp.Web [#6075](https://github.com/OrchardCMS/OrchardCore/pull/6075)
- Fixing typos, a lot of them (Lombiq Technologies: OCORE-20) [#6080](https://github.com/OrchardCMS/OrchardCore/pull/6080)
- Adding option to enable Mini Profiler on the admin too (Lombiq Technologies: OCORE-19) [#6052](https://github.com/OrchardCMS/OrchardCore/pull/6052)
- Making FormPart generic [#6053](https://github.com/OrchardCMS/OrchardCore/pull/6053)
- Fix null error when rendering html part in flow editor [#6040](https://github.com/OrchardCMS/OrchardCore/pull/6040)
- Use PrefixPosition for Admin menus [#6066](https://github.com/OrchardCMS/OrchardCore/pull/6066)
- Validate consecutive slashes in autoroute path [#6065](https://github.com/OrchardCMS/OrchardCore/pull/6065)
- Patch 1 [#6067](https://github.com/OrchardCMS/OrchardCore/pull/6067)
- Render bagpart items with summary displaytype. [#5933](https://github.com/OrchardCMS/OrchardCore/pull/5933)
- Fixing the file naming convention - Edit.cshtml not Editor.cshtml [#6058](https://github.com/OrchardCMS/OrchardCore/pull/6058)
- Fixing ModularBackgroundService logging and improving IsFatal() checks (Lombiq Technologies: OCORE-17) [#5859](https://github.com/OrchardCMS/OrchardCore/pull/5859)
- Adding note on hiding shapes from placement [#6041](https://github.com/OrchardCMS/OrchardCore/pull/6041)
- Make Login, Logout and ChangePassword paths configurable [#6028](https://github.com/OrchardCMS/OrchardCore/pull/6028)
- Fixes rendering draft on front end [#6038](https://github.com/OrchardCMS/OrchardCore/pull/6038)
- Fix RSS items description [#5934](https://github.com/OrchardCMS/OrchardCore/pull/5934)
- Allow registering named style and script resources with inline content [#5903](https://github.com/OrchardCMS/OrchardCore/pull/5903)
- Contributing and link to .NET Foundation [#6005](https://github.com/OrchardCMS/OrchardCore/pull/6005)
- Update GraphQL dependencies [#5837](https://github.com/OrchardCMS/OrchardCore/pull/5837)
- Admin menus positions [#6007](https://github.com/OrchardCMS/OrchardCore/pull/6007)
- Upgrade bootstrap-select version to 1.13.15 [#6023](https://github.com/OrchardCMS/OrchardCore/pull/6023)
- Upgrade CodeMirror version to 5.53.2 [#6015](https://github.com/OrchardCMS/OrchardCore/pull/6015)
- Check LinkField Url [#6022](https://github.com/OrchardCMS/OrchardCore/pull/6022)
- Fix typo optionsTextArea [#6006](https://github.com/OrchardCMS/OrchardCore/pull/6006)
- Change confirm bulk action message [#6004](https://github.com/OrchardCMS/OrchardCore/pull/6004)
- Remove items from media cache when events fired [#5617](https://github.com/OrchardCMS/OrchardCore/pull/5617)
- Returning null in case of not finding the entry [#5950](https://github.com/OrchardCMS/OrchardCore/pull/5950)
- Sort items collection on access [#5982](https://github.com/OrchardCMS/OrchardCore/pull/5982)
- Target new tab when viewing media [#5980](https://github.com/OrchardCMS/OrchardCore/pull/5980)
- Content culture picker shape documentation [#6003](https://github.com/OrchardCMS/OrchardCore/pull/6003)
- Fixes [#5761](https://github.com/OrchardCMS/OrchardCore/pull/5761) : Move HtmlField's media modal in footer [#6000](https://github.com/OrchardCMS/OrchardCore/pull/6000)
- Move HeadMeta section [#5991](https://github.com/OrchardCMS/OrchardCore/pull/5991)
- Deployment plans search [#5992](https://github.com/OrchardCMS/OrchardCore/pull/5992)
- Fixes AdminOptions resolution [#5975](https://github.com/OrchardCMS/OrchardCore/pull/5975)
- Upgrade dependencies [#5981](https://github.com/OrchardCMS/OrchardCore/pull/5981)
- Localize doc note: Restart after editing a .po file. [#5985](https://github.com/OrchardCMS/OrchardCore/pull/5985)
- Remove Site.Meta [#5946](https://github.com/OrchardCMS/OrchardCore/pull/5946)
- Add ability to restrict widgets within a flow part [#5970](https://github.com/OrchardCMS/OrchardCore/pull/5970)
- Fix widget list missing zone name when inserting [#5949](https://github.com/OrchardCMS/OrchardCore/pull/5949)
- Fixes [#5921](https://github.com/OrchardCMS/OrchardCore/pull/5921) shape table providers [#5938](https://github.com/OrchardCMS/OrchardCore/pull/5938)
- [doc] Correct text field usage in liquid example [#5955](https://github.com/OrchardCMS/OrchardCore/pull/5955)
- Adding support for IN (SELECT) sql statements [#5952](https://github.com/OrchardCMS/OrchardCore/pull/5952)
- Make config keys compatible with Linux OS [#5918](https://github.com/OrchardCMS/OrchardCore/pull/5918)
- Update PermissionHandler.cs [#5940](https://github.com/OrchardCMS/OrchardCore/pull/5940)
- Add icons to Configuration Settings menus [#5919](https://github.com/OrchardCMS/OrchardCore/pull/5919)
- Add BenchmarkDotNet in Dependencies.props and upgrade version [#5917](https://github.com/OrchardCMS/OrchardCore/pull/5917)
- Site Meta [#5854](https://github.com/OrchardCMS/OrchardCore/pull/5854)
- DictionaryAttributePrefix and ModelExplorer support in liquid [#5099](https://github.com/OrchardCMS/OrchardCore/pull/5099)
- Prevent too many liquid shape recursion [#4394](https://github.com/OrchardCMS/OrchardCore/pull/4394)
- Upgrade workflows dependencies [#5845](https://github.com/OrchardCMS/OrchardCore/pull/5845)
- Autoroute container routing [#5665](https://github.com/OrchardCMS/OrchardCore/pull/5665)
- Themes standardization [#5852](https://github.com/OrchardCMS/OrchardCore/pull/5852)
- Update dependencies versions [#5850](https://github.com/OrchardCMS/OrchardCore/pull/5850)
- fix(YoutubeField): blank value get's saved [#5909](https://github.com/OrchardCMS/OrchardCore/pull/5909)
- Top contributors [#5901](https://github.com/OrchardCMS/OrchardCore/pull/5901)
- Update 'Install culture' guide [#5900](https://github.com/OrchardCMS/OrchardCore/pull/5900)
- Wrap editor in a null check [#5884](https://github.com/OrchardCMS/OrchardCore/pull/5884)
- [doc] Correct shape tags usage with arrays [#5896](https://github.com/OrchardCMS/OrchardCore/pull/5896)
- Added an Update Content Item Task, i think we have CRUD now! [#5894](https://github.com/OrchardCMS/OrchardCore/pull/5894)
- Remove font awesome pseudoSearch config [#5872](https://github.com/OrchardCMS/OrchardCore/pull/5872)
- [doc] Correct liquid zone usage [#5887](https://github.com/OrchardCMS/OrchardCore/pull/5887)
- Upgrade documentation to Material 5 [#5777](https://github.com/OrchardCMS/OrchardCore/pull/5777)
- Fixes Workflow Timer [#5830](https://github.com/OrchardCMS/OrchardCore/pull/5830)
- ReleaseShellContext() methods [#5551](https://github.com/OrchardCMS/OrchardCore/pull/5551)
- Admin menus [#5855](https://github.com/OrchardCMS/OrchardCore/pull/5855)
- Update package.json dependencies [#5875](https://github.com/OrchardCMS/OrchardCore/pull/5875)
- Update Markdown package dependencies [#5876](https://github.com/OrchardCMS/OrchardCore/pull/5876)
- Update Themes package dependencies [#5877](https://github.com/OrchardCMS/OrchardCore/pull/5877)
- Tab placement documentation [#5861](https://github.com/OrchardCMS/OrchardCore/pull/5861)
- Add doc for missing content fields [#5870](https://github.com/OrchardCMS/OrchardCore/pull/5870)
- Cleanup unused things [#5853](https://github.com/OrchardCMS/OrchardCore/pull/5853)
- Update footer dates in theme recipes [#5838](https://github.com/OrchardCMS/OrchardCore/pull/5838)
- Fixes OC.ContentLocalization dependencies [#5844](https://github.com/OrchardCMS/OrchardCore/pull/5844)
- Add docs for Azure and Database Shells Configuration [#5835](https://github.com/OrchardCMS/OrchardCore/pull/5835)
- Upgrade Font awesome to 5.13.0 [#5832](https://github.com/OrchardCMS/OrchardCore/pull/5832)
- Setup screen improvements [#5781](https://github.com/OrchardCMS/OrchardCore/pull/5781)
- Moved SameSite.None to OpenId Module at startup [#5786](https://github.com/OrchardCMS/OrchardCore/pull/5786)
- Fixes AntiforgeryValidationException [#5803](https://github.com/OrchardCMS/OrchardCore/pull/5803)
- apply message styles [#5820](https://github.com/OrchardCMS/OrchardCore/pull/5820)
- Update ShellHost Registrations [#5824](https://github.com/OrchardCMS/OrchardCore/pull/5824)
- Update ITagCache registration [#5828](https://github.com/OrchardCMS/OrchardCore/pull/5828)
- Remove unnecessary constructor from DataAnnotationsDefaultErrorMessages [#5827](https://github.com/OrchardCMS/OrchardCore/pull/5827)



# Orchard Core 1.0
Release date: September 2020?

## Future Enhancements

* Localization-neutral fields
* Dynamic strings localization
* SEO
* Distributed hosting
* Jobs queue
* Output caching
* Entities API
* GraphQL mutations
* Audit trail
* Tracking
* Better Documentation
* Security
* Accessibility
* Deployment and hosting
* Better Performance



# What can this modular framework do for You?

![Orchard-Core-001](https://user-images.githubusercontent.com/59172485/90696770-254ceb80-e23a-11ea-89d3-0d16293d08e8.png)

Let's look back at a bit of History. Back in 1997, Sun Microsystems, sued Microsoft, charging them with trying to steal Sun's Java standard by shipping a conflicting version of the programming language. Back at the time, even though Java was supposed to be open-source, Microsoft had a competing product named Visual J++ which was extremely popular.



![Orchard-Core-002](https://user-images.githubusercontent.com/59172485/90696774-27af4580-e23a-11ea-8536-a56dd7a2dffb.png)

In the meantime, during the lengthy lawsuit, Microsoft decided to create it’s very own managed platform and language. With the help of Anders Hejlsberg, the original author of Turbo Pascal and the chief architect of Delphi (Turbo Pascal for Windows with Database) ), they created the C# programming language along with the .NET framework. 



![Orchard-Core-003](https://user-images.githubusercontent.com/59172485/90696781-2a119f80-e23a-11ea-8398-984c2f2573a7.png)

Miguel de Icaza had a job interview at Microsoft in 1997 shortly before he started the GNOME project. At Microsoft, he met Nat Friedman, who worked there as an intern. Afterward, they became good friends. In April 1999 Friedman came up with the idea to create a company to work on GNOME. The company was founded on October 19, 1999, as “International GNOME Support”, but its name was changed to Helix Code later. Because that name could not be trademarked the name was changed to Ximian on January 10, 2001



![Orchard-Core-004](https://user-images.githubusercontent.com/59172485/90696786-2c73f980-e23a-11ea-8c03-890c36bb73cc.png)

In December of 2000, the underlying Common Language Infrastructure was published as an open standard, "ECMA-335", opening up the potential for independent implementations such as the Mono project, .NET for Linux founded by Miguel de Icaza. The Mono project was without controversy within the open-source community, as it implements portions of the .NET Framework that were covered by Microsoft patents. 



![Orchard-Core-005](https://user-images.githubusercontent.com/59172485/90696788-2da52680-e23a-11ea-98b7-1077c26b3dd1.png)

Ximian was acquired by Novell on August 4, 2003, to improve its offerings of Linux for the enterprise. The terms of the all-cash transaction were not disclosed.

![Orchard-Core-006](https://user-images.githubusercontent.com/59172485/90696794-30078080-e23a-11ea-86f2-ed128722e84e.png)

In 2002, Microsoft eventually paid Sun $20 million and was permanently prohibited from using "Java compatible" trademarks on their products.



![Orchard-Core-007](https://user-images.githubusercontent.com/59172485/90696796-30a01700-e23a-11ea-868f-0bd5f3987ef5.png)

Java had a major impact on C#. Without Java, there would be no libraries such as NANT, NUnit, CruiseControl.net, log4net, NHibernate, and Lucene.net. These popular Java projects were ported to C#. 



![Orchard-Core-008](https://user-images.githubusercontent.com/59172485/90696798-31d14400-e23a-11ea-977b-560ace0ba663.png)

With Microsoft being investigated by the Department Of Justice. Microsoft was not favorably looked upon by developers. Developers in the 90s never forgot the horror story of how a big mean monopolist set out to destroy Netscape with its unfair marketing practices.



![Orchard-Core-009](https://user-images.githubusercontent.com/59172485/90696803-34339e00-e23a-11ea-956d-e14235c1b720.png)

Microsoft dominated the browser wars, In April 2002 IE was at 97%. In September of 2008, Chrome was introduced with just 1%. In July 2012 Chome dominated the browser wars at 27%. IE at 24% and Firefox at 19%. Today Chome is at 65%, Safari at 16%, Firefox at 5%, IE 3% and Edge at 2%.



![Orchard-Core-010](https://user-images.githubusercontent.com/59172485/90696805-34cc3480-e23a-11ea-93ce-10be5fac22ee.png)

In 2007, Google releases the Android platform announcing they use Java for its application development.



![Orchard-Core-011](https://user-images.githubusercontent.com/59172485/90696807-35fd6180-e23a-11ea-8804-997c1b58cc2d.png)

In 2010 Oracle, Oracle acquires Java by buying Sun Microsystems for $7.4B. And files a lawsuit against Google for its use of Java in Android.



![Orchard-Core-012](https://user-images.githubusercontent.com/59172485/90696808-372e8e80-e23a-11ea-97f2-892126e0efb0.png)

On November 22, 2010, Attachmate buys Novell for 2.2 Billion. Novell also announced that it has entered into an agreement to sell some of its intellectual property to CPTN Holdings, a consortium run by Microsoft. Miguel de Icaza and Nat Friedman were let go.



![Orchard-Core-013](https://user-images.githubusercontent.com/59172485/90696810-37c72500-e23a-11ea-9423-ae91d5c76266.png)

On May 16, 2011, Miguel de Icaza announced on his blog that Mono would be developed and supported by Xamarin, a newly formed company that planned to release a new suite of mobile products. After Xamarin was announced, the future of the project was questioned since MonoTouch and Mono for Android would now be in direct competition with the existing commercial offerings owned by Attachmate. It was not known at that time how Xamarin would prove they had not illegally used technologies previously developed when they were employed by Novell for the same work. In July 2011, however, Novell - now a subsidiary of Attachmate - and Xamarin announced that Novell had granted a perpetual license to Xamarin for Mono, MonoTouch and Mono for Android. Xamarin took official stewardship of the project.



![Orchard-Core-014](https://user-images.githubusercontent.com/59172485/90696812-385fbb80-e23a-11ea-98b2-917fa8bdce47.png)

On March 27, 2014, Satya Nadella made his first public appearance as CEO of Microsoft. For one thing, Microsoft had just paid $7.2 billion to acquire Nokia’s mobile business, a deal Nadella had voted against as a member of the senior leadership team because, as he explain “I don’t get why the world needed a third ecosystem in phones.” The Windows phone had a mere 4% market share, sipping off leftovers from Apple and Google. Satya was quick to wield the ax. 12,500 Nokia staffers were given their papers in July 2014.



![Orchard-Core-015](https://user-images.githubusercontent.com/59172485/90696813-3990e880-e23a-11ea-8cac-ae6e4da4d52b.png)

Satya focused the company on the Cloud, Microsoft may not have a phone platform but that doesn’t mean we can’t build the best mobile applications. Microsoft released versions of its signature software suite—Microsoft Office— for both iOS and Android for free.



![Orchard-Core-016](https://user-images.githubusercontent.com/59172485/90696815-3a297f00-e23a-11ea-8cf0-546c2e7246e1.png)

On November 12, 2014, Microsoft announced .NET Core, a cross-platform for .NET. The open-source development model would be managed under the stewardship of the .NET Foundation.



![Orchard-Core-017](https://user-images.githubusercontent.com/59172485/90696816-3ac21580-e23a-11ea-80c4-bc1894cdf7cc.png)

On February 24, 2016, Microsoft acquires Xamarin, With this acquisition, the entire C# .NET ecosystem is consolidated under one corporation. Microsoft can now concentrate on taking .NET to the next level. This set of technology is ubiquitous. The consolidated .NET platform now supports iOS, Android, Linux, macOS, Xbox, and Windows.



![Orchard-Core-018](https://user-images.githubusercontent.com/59172485/90696820-3b5aac00-e23a-11ea-9529-b316b85e4609.png)

With the acquisition of GitHub, it reflects the desire by Microsoft to reconnect with developers and persuade them that hey – the Beast of Redmond is not quite so beastly these days. It loves Linux, it contributes code to the kernel, it loves open-source, and it loves putting open-source projects on GitHub. Microsoft is committed to cross-platform development.



![Orchard-Core-019](https://user-images.githubusercontent.com/59172485/90696823-3c8bd900-e23a-11ea-9ee6-952b231f6218.png)

So why go through this historical exercise? Which is better Java or C#? To answer this question. Its really about what the developer is familiar with. Developers stick to the tools they know. I’ll tell you this. I have developed with both Java and C# for many years. I feel that I am more productive with C# and .NET. Microsoft makes some of the best development tools in the industry. Java being open source is controlled by the Java Community Process. It’s really Oracle’s that owns and controls this committee. Whereas C# and .NET are ECMA standards (ECMA-334, ECMA-335 respectively). Ecma is an International standards organization. C# and .NET are controlled by that committee. Microsoft has just one vote in that committee, One other major consideration is that Microsoft has ever sued any company for using .NET or C#. Unfortunately, Oracle /Sun Microsystems cannot say the same. 



![Orchard-Core-020](https://user-images.githubusercontent.com/59172485/90696825-3c8bd900-e23a-11ea-910d-e250efd77ee6.png)

So how does Orchard Core fit into all of this? Well, As we looked back at Microsoft’s history and its technology, let’s look back at the history of Orchard CMS. Microsoft first released the open-source content management system called Oxite at the 2008 MIX conference. MIX was a Microsoft conference held annually for web developers and designers at which Microsoft showcased upcoming web technologies. They had big plans for Oxite. They even contacted Miguel de Icaza, as we know, at the time, he was working for Novell to port the Oxite codebase to Linux. Microsoft made the source code available for the first open-source Oxite CMS at the end of 2008. According to Mary Jo Foley, Tech journalist, from ZDNet, “All about Microsoft”, Microsoft's open-source CMS platform Oxite was (re)born to the “Orchard Project” at TechEd Europe in November 2009.



![Orchard-Core-021](https://user-images.githubusercontent.com/59172485/90696827-3d246f80-e23a-11ea-8dbd-02da87f9ae50.png)

Here is the front page of the Orchard Gallery.



![Orchard-Core-022](https://user-images.githubusercontent.com/59172485/90696828-3dbd0600-e23a-11ea-9230-7dd9029e32be.png)

Here is an add for the Orchard media manager.



![Orchard-Core-023](https://user-images.githubusercontent.com/59172485/90696829-3e559c80-e23a-11ea-847c-132920bdbcb8.png)

Blazor Server apps are hosted on an ASP.NET Core server in ASP.NET Razor format. Remote clients act as a thin clients, meaning that the bulk of the processing load is on the server. The client's web browser downloads a small page and updates its UI over a SignalR connection. Blazor Server was released as a part of .NET Core 3.0 Blazor WebAssembly a Single-page apps that are downloaded to the client's web browser before running.

 The size of the download is larger than for Blazor Server, depends on the app, and the processing is entirely done on the client hardware. However, this app type enjoys rapid response time. As its name suggests, this client-side framework is written in WebAssembly, as opposed to JavaScript. The framework was released in May 2020. Microsoft plans to release Blazor PWA and Blazor Hybrid editions. Will Orchard Core utilize this technology. Who knows. It remains uncertain if the will. [Oqtane](https://github.com/oqtane/oqtane.framework) another competing Modular application framework is being developed with the Blazor WebAssembly technology.



# Conclusion

There are still many important pieces to add for the official release 1.0 but since the first commit back in November 19, 2014 it has come a long way. One crucial piece missing are requirements. Without requirements, how does anyone know when the software is complete. Passing tests need to created and run successfully for all requirements. For the developers on the Orchard Core team, it has become their life's work. They are very committed individuals. Will it be successful? That will be determined by the official 1.0 release date. This release date has been pushed back several times. A key component is documentation. Without concise and complete documentation, it will be hard for new developers to adopt the framework. Another key consideration is technical debt. Over the six years of developing Orchard Core, technology has changed. Orchard Core needs to adapt and embrace new technology.



# GitHub

The complete source code is located [here](https://github.com/OrchardCMS/OrchardCore).
