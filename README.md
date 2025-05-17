# Introduction

Power Platform Javascript scripts (Client-side and Ribbon button) for **Sales Configuration** solution - **Plugin Testing** application.

Use `Dataverse REST Builder` from the `XrmToolBox` to build the Javascript script to call the Custom Action. Use `namespace` is the best practice to run the script.

# Development Note

_Ordered from newest to oldest_

## 2025-05-01

I want to clone multiple record so I created a loop within the Javascript script to call the plugin multiple time but this hurts the performance. The suggest solution is to use Unbound Custom Action where it will pass in an array (the JS script will be called once) and the loop will be handled by the plugin which improves performance.

Orginally, I pass in just `selectedControlSelectedItemIds` to get the GUID, but later I passed in `selectedControl` to get the control of the homepage grid (because I was using a button) in order to use `selectedControl.refresh()` to refresh the homepage grid once the cloning process has been completed.

Additionally, here are some tools you will also need to download:

- Plugin Registration Tool
- Early-bound Generator v2
- FetchXML Tool, I used ChatGPT to generate this.
