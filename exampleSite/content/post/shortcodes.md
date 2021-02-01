+++
author = "Hugo Authors"
title = "Shortcodes"
date = "2021-02-01"
description = "Lorem Ipsum Dolor Si Amet"
tags = [
    "markdown",
    "text",
]
image = "/images/Lorem-Ipsum.png"
+++

There are a few shortcodes available in this theme. 

# Hide Text
You can hide text with HTML `<details>` tag. Use `details` shortcode:

```
{{</* details Read more...*/>}}
... more text ...
{{</* /details */>}}

```

{{< details "Read more..." >}}
Lorem est tota propiore conpellat pectoribus de pectora summo. <!--more-->Redit teque digerit hominumque toris verebor lumina non cervice subde tollit usus habet Arctonque, furores quas nec ferunt. Quoque montibus nunc caluere tempus inhospita parcite confusaque translucet patri vestro qui optatis lumine cognoscere flos nubis! Fronde ipsamque patulos Dryopen deorum.

1. Exierant elisi ambit vivere dedere
2. Duce pollice
3. Eris modo
4. Spargitque ferrea quos palude

```
Exierant elisi ambit vivere dedere
```
{{< /details >}}

{{< details >}}
Rursus nulli murmur; hastile inridet ut ab gravi sententia! Nomine potitus silentia flumen, sustinet placuit petis in dilapsa erat sunt. Atria tractus malis.

1. Comas hunc haec pietate fetum procerum dixit
2. Post torum vates letum Tiresia
3. Flumen querellas
4. Arcanaque montibus omnes
5. Quidem et
{{< /details >}}


# Raw HTML

Use raw HTML in your posts like this:

```
{{</* rawhtml */>}}
  <p class="speshal-fancy-custom">
    This is <strong>raw HTML</strong>, inside Markdown.
  </p>
{{</* /rawhtml */>}}
```

{{< rawhtml >}}
  <p class="speshal-fancy-custom">
    This is <strong>raw HTML</strong>, inside Markdown.
  </p>
{{< /rawhtml >}}
