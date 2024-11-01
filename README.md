# a11y-oral-history
Accessible oral history web component


## Objectives

- An accessible oral history web component that can be used to present audio recordings with transcripts.
- Support for [WebVTT](https://www.w3.org/TR/webvtt1/) captions and transcripts. 
- Support for screen readers
- No framework dependencies


See: [Making Audio and Video Media Accessible](https://www.w3.org/WAI/media/av/)

## Definitions

- [Web components](https://developer.mozilla.org/en-US/docs/Web/API/Web_Components): custom HTML tags like that extend the web and act as native HTML elements. Fast and work anywhere.
- [Lit](https://lit.dev/) - A popular, small library for making web components.

## Accessible Media Player Options

- [Oral History Metadata Synchronizer (OHMS)](https://www.oralhistoryonline.org/)
- [Able Player](https://github.com/ableplayer/ableplayer)
- [Video.js](https://github.com/videojs/video.js)
- [MediaElement.js](https://github.com/mediaelement/mediaelement)
- [Plyr](https://github.com/sampotts/plyr)
- [HaxTheWeb - a11y-media-player](https://github.com/haxtheweb/webcomponents/tree/master/elements/a11y-media-player)

## Test Implementation 

Penn State's HaxTheWeb a11y-media-player

### Examples

- https://exhibitions.psu.edu/s/african-brilliance/page/clemente-abrokwaa (Omeka)

### GitHub repositories

- https://github.com/haxtheweb/webcomponents
- https://github.com/haxtheweb/webcomponents/tree/master/elements/a11y-media-player
- https://github.com/haxtheweb/unbundled-webcomponents

### Screen Reader Issues

- The screen reader will continually announce the play status unless you set `hide-play-status` on the element.
- The screen reader will announce tooltips. Need to set `aria-hidden="true"` on the tooltip elements to prevent this.
- Each transcript entry is also a form element that tends to add noise to the screen reader. Maybe set `aria-hidden="true"` on the form elements to prevent this.
- Treating audio as video is preferred currently since it renders better in terms of the poster image.
