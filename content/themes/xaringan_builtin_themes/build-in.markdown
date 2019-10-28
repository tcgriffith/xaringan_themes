---
title: "xaringan_builtin_theme"
author: "TC"
date: '2019-10-27'
description: all builtin themes of xaringan
tags: [xaringan]
thumbnail: https://github.com/emitanaka/ninja-theme/raw/master/docs/themes/kunoichi/images/kunoichi-showcase.gif
categories: theme
toc: true
---



## Description

Here is a collection of the build-in themes in xaringan.


```r
example_slide=xfun::file_string("./template.Rmd")

builtins = names(xaringan:::list_css())

builtins_excludefont=builtins[!grepl("font", builtins)]
```



```r
dummy = lapply(builtins_excludefont, function(name){
  
  newstr=paste0("use_theme('",name,"')")
  newfile = gsub('use_theme\\(\"tcgriffith/xaringan_theme_example\"\\)',newstr,example_slide)
  
  writeLines(newfile, con = here::here("static/slides/",paste0("xaringan_",name,".Rmd")))
  
})

blogdown::build_dir(here::here("static"))
```


## All built-in themes


```r
slides=list.files(here::here("static/slides"), pattern="html$")

# slides
dummy = lapply(slides, function(fname){
  writeLines(sprintf("### %s",gsub(".html","",basename(fname))))
  
  writeLines(sprintf("[link](/slides/%s)\n\n", fname))
  
  writeLines(sprintf(
'<div class="resp-container">
<iframe class="testiframe" src="/slides/%s">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>\n\n',
    fname))
})
```

### xaringan_chocolate
[link](/slides/xaringan_chocolate.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_chocolate.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_default
[link](/slides/xaringan_default.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_default.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_duke-blue
[link](/slides/xaringan_duke-blue.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_duke-blue.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_fc
[link](/slides/xaringan_fc.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_fc.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_hygge-duke
[link](/slides/xaringan_hygge-duke.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_hygge-duke.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_hygge
[link](/slides/xaringan_hygge.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_hygge.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_kunoichi
[link](/slides/xaringan_kunoichi.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_kunoichi.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_lucy
[link](/slides/xaringan_lucy.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_lucy.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_metropolis
[link](/slides/xaringan_metropolis.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_metropolis.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_middlebury
[link](/slides/xaringan_middlebury.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_middlebury.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_ninjutsu
[link](/slides/xaringan_ninjutsu.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_ninjutsu.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_rladies
[link](/slides/xaringan_rladies.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_rladies.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_robot
[link](/slides/xaringan_robot.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_robot.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_rutgers
[link](/slides/xaringan_rutgers.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_rutgers.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_shinobi
[link](/slides/xaringan_shinobi.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_shinobi.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_tamu
[link](/slides/xaringan_tamu.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_tamu.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_uo
[link](/slides/xaringan_uo.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_uo.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


### xaringan_uol
[link](/slides/xaringan_uol.html)


<div class="resp-container">
<iframe class="testiframe" src="/slides/xaringan_uol.html">
    Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>
</div>


