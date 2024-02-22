# Build first web app with ASP.NET Core using Blazor

## Intro
### Purpose
Build the first web app with ASP.NET Core using Blazor.

### Prerequisites
macOS 10.15 or later versions.

### Time to Complete
10-15 minutes + download/installation time

### Scenario
Create, use, and modify a simple counter component.

## Download and install
To start building .NET apps, download and install the .NET SDK.

**Download .NET 8 SDK (64-bit)**

**Arm64 download**

If on a Mac with an Apple M1 chip, need to install the Arm64 version of the SDK.

## Check everything installed correctly
Once installed, open a **new** terminal and run the following command:


```
dotnet --version
```
If the installation succeeded, should see version 8.0.100 or higher outputted:

```
8.0.100
```
If everything looks good, select the **Continue** button below to go to the next step.

## Create app
In the terminal, run the following command to create app:

```
dotnet new blazor -o BlazorApp
```

This command creates new Blazor Web App project and places it in a new directory called `BlazorApp` inside current location.

Navigate to the new `BlazorApp` directory created by the previous command:

```
cd BlazorApp
```

Take a quick look at the contents of the `BlazorApp` directory.

```
ls
```

Several files were created in the `BlazorApp` directory, to give a simple Blazor app that is ready to run.

- `Program.cs` is the entry point for the app that starts the server and where we configure the app services and middleware.
- `App.razor` is the root component for the app.
- `Routes.razor` configures the Blazor router.
The `Components/Pages` directory contains some example web pages for the app.
`BlazorApp.csproj` defines the app project and its dependencies.
The `launchSettings.json` file inside the `Properties` directory defines different profile settings for the local development environment. A port number is automatically assigned at project creation and saved on this file.

Take note of the `BlazorApp` directory path as we will use it later in the tutorial.

If everything looks good, select the **Continue** button below to go to the next step.

## Run our app
In the terminal, run the following command:

```
dotnet watch
```

The `dotnet watch` command will build and start the app, and then update the app whenever we make code changes. We can stop the app at any time by selecting `Ctrl+C`.

Wait for the app to display that it's listening on `http://localhost:<port number>` and for the browser to launch at that address.

Once we get to the following page, you have successfully run your first Blazor app!

[Screenshot Blazor Tutorial Run](https://dotnet.microsoft.com/static/images/blazor-tutorial/screenshot-blazor-tutorial-run.png)

The displayed page is defined by the `Home.razor` file located inside the `Components/Pages` directory. This is what its contents look like:

`Components/Pages/Home.razor`
```
@page "/"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.
```

It already contains the code that sets it as the homepage and displays the text `Hello, world!` and `Welcome to your new app`. The `PageTitle` component sets the title for the current page so that it shows up in the browser tab.


### Reference:
[Blazor Tutorial - Build your first Blazor app](https://dotnet.microsoft.com/learn/aspnet/blazor-tutorial/intro)