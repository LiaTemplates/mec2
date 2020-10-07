<!--
author:   André Dietrich

email:    LiaScript@web.de

logo:     

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Port of the Mec2 Simulator from https://github.com/goessner/mec2
          to LiaScript.

script:   https://jauhl.github.io/mecEdit/scripts/g2.js
          https://jauhl.github.io/mecEdit/scripts/mec2.min.js
          https://jauhl.github.io/mecEdit/scripts/mecelement/canvasInteractor.js
          https://jauhl.github.io/mecEdit/scripts/mecelement/g2.selector.js
          https://jauhl.github.io/mecEdit/scripts/mecelement/mec.htmlelement.js


@mec
<lia-keep>
<MEC-2 width=800 height=600 grid cartesian darkmode x0=385 y0=139 >
@0
</MEC-2>
</lia-keep>
@end

@mec.eval: @mec.eval_(@uid)

@mec.eval_
<script>
let json=`@input`

document.getElementById("@0").innerHTML = "<MEC-2 id='test' width=1530 height=680 grid cartesian darkmode x0=385 y0=139 >" + json + "</MEC-2>"

"LIA: stop"
</script>

<div id="@0"></div>

@end

-->

# mec2
Port of the mec2 2D physics simulation engine to LiaScript

https://goessner.github.io/mec2/
