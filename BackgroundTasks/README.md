<h1 id="background-tasks">Background Tasks</h1>
<h2 id="overview">1. OVERVIEW</h2>
<p>This very ambitious example uses background tasks, canvas drawing, flow layout, and the desktop notification extension to show off multiple tasks running in the background and all updating the client at the same time.</p>
<h2 id="what-to-look-for">2. WHAT TO LOOK FOR</h2>
<p>There are several components and features used in this sample that are important to understand:</p>
<ul>
<li><code>Application.StartTask()</code> starts a new task connected to the same session with the capability to push updates directly to the client in real time.</li>
<li>The user control <code>SortBox</code> shows how to create a custom component drawing in an HTML5 canvas on the client. This control does two things:
<ol>
<li>Draws the entire state (all the lines)</li>
<li>Only swaps the lines being sorted</li>
</ol>
</li>
<li>Look also at the flow layout panel and how it arranges the child panels.</li>
</ul>
<h2 id="how-to-create-your-own">3. HOW TO CREATE YOUR OWN</h2>
<p>You can add background tasks to any Wisej application simply by calling:</p>
<pre><code class="language-csharp">Application.StartTask(() =&gt;
{
    AlertBox.Show(&quot;Hello&quot;);
    Application.Update();
});
</code></pre>
