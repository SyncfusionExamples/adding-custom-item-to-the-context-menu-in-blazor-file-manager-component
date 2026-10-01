# Adding Custom Item to the Context Menu in Blazor File Manager Component

## Overview
 
This sample demonstrates how to customize the Syncfusion [Blazor File Manager](https://www.syncfusion.com/blazor-components/blazor-file-manager) by adding a custom item to the component's context menu. The example shows how to define a custom command, display a custom icon, and respond to user actions when the custom menu item is selected.
 
Context menu customization is useful when an application needs file-management actions that are specific to business workflows. By extending the File Manager's built-in context menu, developers can provide additional commands while preserving the familiar file browsing experience.

## Key Features

- Uses the Syncfusion Blazor File Manager component in Details view mode through the `View="ViewType.Details"` configuration.
- Connects the File Manager to ASP.NET Core backend services using `FileManagerAjaxSettings`.
- Configures File Manager endpoints for file operations, upload, download, and image retrieval.
- Customizes the File Manager context menu using `FileManagerContextMenuSettings`.
- Adds a custom context menu item (`Undo`) alongside built-in menu commands (`Open` and `Details`) for files, folders, and layout areas.
- Handles the `MenuOpened` event to dynamically modify context menu items before rendering.
- Assigns a custom icon (`oi oi-action-undo`) to the custom context menu item at runtime.
- Handles custom context menu interactions through the `OnMenuClick` event.
- Demonstrates custom command execution by detecting and processing clicks on the `Undo` menu item.
- Implements a server-side file system provider using `PhysicalFileProvider`.
- Supports File Manager CRUD operations including read, create, rename, delete, copy, move, search, and details retrieval.
- Provides file upload, file download, and image thumbnail retrieval endpoints for File Manager integration.
- Uses a physical file storage location (`Data\Files`) as the File Manager root directory.

## Prerequisites
 
- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project
 
**Visual Studio 2022**
 
1. Clone or download this repository.
2. Open `AddCustomItemToContextMenu.sln`.
3. Restore NuGet packages if prompted.
4. Ensure the startup project is `AddCustomItemToContextMenu.Server`.
5. Build the solution.
6. Run the application using `Ctrl+F5`.
 
**Visual Studio Code**
 
1. Open the repository folder in Visual Studio Code.
2. Navigate to the repository root that contains `AddCustomItemToContextMenu.sln`.
3. Restore packages:
 
```bash
dotnet restore
```
 
4. Run the hosted application:
 
```bash
dotnet run --project Server/AddCustomItemToContextMenu.Server.csproj
```
 
5. Open the URL displayed in the console output.

## Project Structure

`Client/Pages/Index.razor` - Main sample page that hosts the Syncfusion Blazor File Manager, configures custom context menu items, assigns a custom icon in the `MenuOpened` event, and handles custom menu actions through the `OnMenuClick` event.

`Server/Controllers/FileManagerController.cs` - ASP.NET Core API controller that provides File Manager backend services including file operations, upload, download, image retrieval, and physical file system access.

`Server/Data/Files/` - Physical root folder configured through `PhysicalFileProvider.RootFolder()` and used as the File Manager's storage location.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Refer to the official documentation for adding custom context menu items in Blazor File Manager: https://help.syncfusion.com/file-manager-sdk/blazor/how-to/adding-custom-item-to-context-menu

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.