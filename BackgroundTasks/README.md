# Background Tasks

## 1. OVERVIEW

This very ambitious example uses background tasks, canvas drawing, flow layout, and the desktop notification extension to show off multiple tasks running in the background and all updating the client at the same time.

## 2. WHAT TO LOOK FOR

There are several components and features used in this sample that are important to understand:

- `Application.StartTask()` starts a new task connected to the same session with the capability to push updates directly to the client in real time.
- The user control `SortBox` shows how to create a custom component drawing in an HTML5 canvas on the client. This control does two things:  
  1. Draws the entire state (all the lines)  
  2. Only swaps the lines being sorted
- Look also at the flow layout panel and how it arranges the child panels.

## 3. HOW TO CREATE YOUR OWN

You can add background tasks to any Wisej application simply by calling:

```csharp
Application.StartTask(() =>
{
    AlertBox.Show("Hello");
    Application.Update();
});
