# video-beamer-mwe
A minimal working example for using video in beamer.

To compile:

pdflatex videoMWE.tex
pdflatex videoMWE.tex

To view, in previous times, I would have to use the [Okular](https://okular.kde.org/) pdf reader.  Now, in 2019, I have been able to get video to play in Ubuntu 18.04 using [Evince](https://wiki.gnome.org/Apps/Evince).

This 2-frame file includes my now-standard title page, with a title box over a background image. 

To get the video to embed, I use the multimedia package. This is described in the [Beamer user guide](http://www.ctan.org/tex-archive/macros/latex/contrib/beamer/doc/beameruserguide.pdf) (search for multimedia).

````latex
\usepackage{multimedia}
````

Then, 

````latex
\movie[label=show3, height = 6cm, poster, autostart, showcontrols]{\includegraphics[height = 6cm]{\imagepath/Potato-poster.png}}{\imagepath/Potato.mp4}
````

includes an image `Potato-poster.png` over the region reserved for the video, and the video is `Potato.mp`.  All the options are specified for `\movie` are specified in [Beamer user guide](http://www.ctan.org/tex-archive/macros/latex/contrib/beamer/doc/beameruserguide.pdf), and I have had different results depending on the .pdf viewer.   

*If you are having compilation problems, note, that I usually install all of the texlive packages.*

Like in Windows Powerpoint, if you move the entire directory structure, the videos will play.  However, if the directory structure is disturbed ... uncertain results.  I always test!



 
