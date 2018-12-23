Tales
=====

In Labyrinth, an _interactive tale_ is based on a collection of interconnected scenes that are connected together by choices, which are conditional links between scenes. The structure of the tale is held in an [XML](https://en.m.wikipedia.org/wiki/XML) document called `talebones.xml` and it names the scenes, describes the choices and how the scenes and choices join up. It doesn't include any story text or pictures, which are always held in separate files.

The simplest possible tale has one scene and no choices. It might look something like the following:

```xml
<talebones layout='layout.mustache'>
	<scene name='Scene001' full-text='Scene001/full-text.md'>
	</scene>
</talebones>
```

When you run [this tale](link-to-be-provided), all it does is display the full-text of the scene that is held in the file `full-text.md`. The tale-telling engine sees that there are no continuations from this scene and realises that this is the end of the tale too, so displays the fancy "THE END" message too. 

Perhaps surprisingly there is quite a lot going on here:

  * The full-text itself is written in (Markdown)[https://daringfireball.net/], which is a popular format for writing rich-text content using only plain-text. Markdown is popular because it is simple to write, easy to embed in web applications, doesn't require special tools and easy to maintain in version control systems like git. This file that you are reading now is written in Markdown, for instance.

  * The overall look of the window is determined by a template called `layout.mustache`, which is written in the [Mustache](https://mustache.github.io/mustache.5.html) notation. Writing templates is an advanced topic because it requires not just knowing Mustache but also HTML, CSS and how Labyrinth passes data into the template. So, to start with, you can just use the [premade layouts](link-to-be-provided).
