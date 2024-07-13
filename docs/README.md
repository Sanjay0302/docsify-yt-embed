# Docsify Custom YouTube Embed Plugin

> This plugin enhances Docsify with `advanced YouTube video embedding` capabilities, allowing for easy insertion of responsive, customizable YouTube videos directly in your Markdown files.

---

## Features

1. **Simple Embed Syntax**
2. **Customizable Dimensions**
3. **Flexible Alignment**
4. **Responsive Design**

> **This repository has 2 ways of embedding YouTube videos**
>
> - `yt-embed`: will only embed a YouTube video with customizable size and alignment.
> - `yt-embed-collapse` can enclose a YouTube video within a collapsible element.

---

### Simple YouTube Embed (yt-embed)

<!-- tabs:start -->

#### **Preview**

> **Some arguments we need to pass in embedding syntax**
>
> - `ALIGNMENT`: The alignment on the page - 'left', 'center', or 'right' (optional, default is 'center')
> - `WIDTH`: The width of the video (optional, default is 100%)
> - `HEIGHT`: The height of the video (optional, default maintains 16:9 aspect ratio)

Note: As you can see in the Preview tab, this syntax will be automatically rendered as an embedded YouTube video.

<!-- tabs:start -->

<!-- tab:Syntax-1 -->
## No arguments <!-- {docsify-ignore} -->

```syntax
@yt(dQw4w9WgXcQ)
```

@yt(dQw4w9WgXcQ)

<!-- tab:Syntax-2 -->

## Custom width (500px, centered) <!-- {docsify-ignore} -->

```syntax
@yt(dQw4w9WgXcQ,500px)
```

@yt(dQw4w9WgXcQ,500px)

<!-- tab:Syntax-3 -->
## Left Allign <!-- {docsify-ignore} -->

```syntax
@yt(dQw4w9WgXcQ,400px,300px,left) 
```

@yt(dQw4w9WgXcQ,400px,300px,left)

<!-- tab:Syntax-4 -->

## Right Allign <!-- {docsify-ignore} -->

```syntax
@yt(dQw4w9WgXcQ,400px,300px,right) 
```

@yt(dQw4w9WgXcQ,400px,300px,right)

<!-- tab:Syntax-5 -->
## Center Allign <!-- {docsify-ignore} -->

> This embed will be centered by default;
> But also can be mentioned inline;

```syntax
@yt(dQw4w9WgXcQ,400px,300px,center) 
```

@yt(dQw4w9WgXcQ,400px,300px,center)

<!-- tab:Syntax-6 -->
## Ignoring a render <!-- {docsify-ignore} -->
>
> - When we need to include the syntax as normal text instead of rendering it as an embedding video;
> - We have 2 methods:
>   - Adding `<!-- {docsify-ignore} -->` inline to the syntax;
>   - Writing the code within [`code-fence`](https://markdown.land/markdown-code-block);

1. Add `<!-- {docsify-ignore} -->` inline to the syntax.

    ```syntax
    @yt(dQw4w9WgXcQ,400px,300px,center) <!-- {docsify-ignore} --> 
    ```

2. [code-fence](https://markdown.land/markdown-code-block)
   - Here enclose the syntax inside [`code-fence`](https://markdown.land/markdown-code-block).

<!-- tabs:end -->

#### **Installation**

- Download the `yt-embed.js` and `yt-embed.css` file and place it in your Docsify project directory.
- Add the following line to your index.html file, after the main Docsify script:

    ```html
    <script src="path/to/yt-embed.js"></script>
    ```

    ```html
    <link rel="stylesheet" href="path/to/yt-embed.css">
    ```

#### **Usage**

> In `Preview` tab explains usage of all syntax and its rendered view.

Use the following syntax in your Markdown files to embed YouTube videos:

```syntax
@yt(<EMBED-ID>,<WIDTH>,<height>,<ALIGNMENT>)"
```

### Where to find Embed-ID

- Go to [Youtube](https://www.youtube.com/)
- Select any video that you want to embed.
- then look for it's URL; (it will look like either of this)

```url
https://youtu.be/HccqokXN2n8?feature=shared
https://www.youtube.com/watch?v=HccqokXN2n8&list=PL4Gr5tOAPttLOY9IrWVjJlv4CtkYI5cI_&index=6
```

> So in this `Embed-ID` is `HccqokXN2n8`

<!-- tabs:end -->

---

### YT Collapsible element (yt-embed-collapse)

<!-- tabs:start -->

#### **Preview**

> **Some arguments we need to pass in embedding syntax**
>
> - `Embed-id`: Provide embed-id for yt-video, this is explained in `Usage tab`
> - `Title`: Title text to display; Probably it will be title of a video. (optional, default is `Click to expand`)

Note: As you can see in the Preview tab, this syntax will be automatically rendered as an embedded YouTube video.

<!-- tabs:start -->

<!-- tab:Syntax-1 -->

## No arguments <!-- {docsify-ignore} -->

> Default `title` is Click here to watch the video. (You can change this in `JS` file);
>
> No argument is passed;

```syntax
[youtube:dQw4w9WgXcQ]
```

[youtube:dQw4w9WgXcQ]

<!-- tab:Syntax-2 -->

## Custom Title <!-- {docsify-ignore} -->

> Custom `Title` tag can be given inline after this `|`.

```syntax
[youtube:dQw4w9WgXcQ | My own text - Click to expand]
```

[youtube:dQw4w9WgXcQ | My own text - Click to expand]

<!-- tab:Syntax-3 -->

## Ignoring a render <!-- {docsify-ignore} -->

>
> - When we need to include the syntax as normal text instead of rendering it as an embedding video;
> - We have 2 methods:
>   - Adding `<!-- {docsify-ignore} -->` inline to the syntax;
>   - Writing the code within [`code-fence`](https://markdown.land/markdown-code-block);

1. Add `<!-- {docsify-ignore} -->` inline to the syntax.

    ```syntax
    [youtube:dQw4w9WgXcQ] <!-- {docsify-ignore} --> 
    ```

2. [code-fence](https://markdown.land/markdown-code-block)
   - Here enclose the syntax inside [`code-fence`](https://markdown.land/markdown-code-block).

<!-- tabs:end -->

#### **Installation**

- Download the `yt-embed-collapse.js` and `yt-embed-collapse.css` file and place it in your Docsify project directory.
- Add the following line to your index.html file, after the main Docsify script:

    ```html
    <script src="path/to/yt-embed-collapse.js"></script>
    ```

    ```html
    <link rel="stylesheet" href="path/to/yt-embed-collapse.css">
    ```

#### **Usage**

> `Preview` tab explains how to use embedding syntax and also visualise its rendered view.

Use the following syntax in your Markdown files to embed YouTube videos:

```syntax
[youtube:<embed-id> | <title-text>]
```

> `title-text` is optional

### Where to find Embed-ID <!-- {docsify-ignore} -->

- Go to [Youtube](https://www.youtube.com/)
- Select any video that you want to embed.
- then look for it's URL; (it will look like either of this)

```url
https://youtu.be/HccqokXN2n8?feature=shared
https://www.youtube.com/watch?v=HccqokXN2n8&list=PL4Gr5tOAPttLOY9IrWVjJlv4CtkYI5cI_&index=6
```

> So in this attached example `Embed-ID` is `HccqokXN2n8`

<!-- tabs:end -->

---

## License

Copyright 2024 Sanjay0302

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   <http://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
