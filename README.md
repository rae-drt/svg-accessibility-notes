This repo is a brief experiment in making an accessible SVG.

It starts with SVG output from exporting a PowerPoint slide to SVG.

This is pretty-printed, then some of the text is reworded to sound more right when read out by Edge's Read Aloud feature.

(Read Aloud: either `... -> More tools -> Read aloud` OR `Ctrl-Shift-U`).

Read Aloud is not really a screen reader (e.g. ignores `aria-label`) but is as close as I can get without installation pain and a learning curve.[^1]

Then I add some invisible text to provide "alt text" for images embedded in the slide.

I did think about adding more `aria-label` tags to make more clear what all the boxes were for screen reader users, but decided not to as this might be cluttering.

I did also initially follow the advice at https://data.europa.eu/apps/data-visualisation-guide/accessible-svg-and-aria to provide support for screen readers that do not understand SVG, but it did not seem possible to make this support conditional on not understanding SVG, resulting in repetition in Read Aloud. Decided to hope that modern screen readers will tend to understand SVG.

Some helpful sources:
* https://data.europa.eu/apps/data-visualisation-guide/accessible-svg-and-aria
* https://data.europa.eu/apps/data-visualisation-guide/making-svg-content-fully-accessible

Some potentially helpful sources:
* https://tympanus.net/codrops/2014/08/19/making-svgs-responsive-with-css/

A sadly not helpful source:
* https://webinsight.cs.washington.edu/wa/
  * This appears to have been a web-based screen reader, which sounds really useful. Sadly it seems to be defunct.

[^1]: I would like to do better here but have only limited time -- and I guess Read Aloud is likely to be widely used due to being part of Edge, so might not be a bad case to optimise for. Also, a random person on Stack Overflow did suggest that screen readers are sufficiently hard to learn to use that the only non-disabled people who tend to be able to use them properly are people who develop them.