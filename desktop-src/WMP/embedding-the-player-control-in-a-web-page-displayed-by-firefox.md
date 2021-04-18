---
title: Incorporamento del controllo Player in una pagina Web visualizzata da Firefox
description: Incorporamento del controllo Player in una pagina Web visualizzata da Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX, pagine Web
- Windows Media Player, Firefox
- Modello a oggetti di Windows Media Player, Firefox
- modello a oggetti, Firefox
- Windows Media Player Mobile, Firefox
- Controllo ActiveX di Windows Media Player, Firefox
- Controllo ActiveX Windows Media Player Mobile, Firefox
- Controllo ActiveX, Firefox
- Firefox, informazioni sull'incorporamento di pagine Web
- incorporamento, pagine Web
- Incorporamento di pagine Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "106299014"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Incorporamento del controllo Player in una pagina Web visualizzata da Firefox

Per incorporare il controllo Media Player di Windows in una pagina Web che può essere visualizzata da un browser Firefox, creare un elemento oggetto o un elemento di INCORPORAmento con uno dei seguenti tipi MIME come attributo di **tipo** :

-   applicazione/x-ms-WMP
-   applicazione/ASX
-   video/x-ms-asf-plug-in
-   applicazione/x-mplayer2
-   video/x-ms-asf
-   video/x-ms-WM
-   audio/x-ms-WMA
-   audio/x-ms-Wax
-   video/x-MS-WMV
-   video/x-ms-wvx

Il tipo MIME preferito è application/x-ms-WMP.

Negli esempi seguenti viene illustrato come incorporare il controllo Player utilizzando un elemento oggetto o un elemento EMBED.


```HTML
<OBJECT id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320">
  <PARAM name="autostart" value="false"/>
</OBJECT>

<EMBED id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320"
  autostart="false"/>

```



Gli esempi di precedente funzionano in Firefox ma non in Internet Explorer. Per incorporare il controllo Player in una pagina Web che può essere visualizzata da Internet Explorer, è necessario creare un elemento oggetto con un attributo **ClassID** impostato sull'ID classe del controllo Media Player di Windows.

Nell'esempio seguente viene illustrato come incorporare il controllo Windows Media Player in una pagina Web che può essere visualizzata correttamente da Internet Explorer e Firefox. Lo script nella pagina rileva il tipo di browser e genera il tag oggetto appropriato.


```HTML
<HTML>
  <BODY>
    <SCRIPT type="text/javascript">
      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {
        document.write('<OBJECT id="Player"');
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');
        document.write(' width=300 height=200></OBJECT>');
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {
        document.write('<OBJECT id="Player"'); 
        document.write(' type="application/x-ms-wmp"'); 
        document.write(' width=300 height=200></OBJECT>');
      }         
    </SCRIPT>
  </BODY>
</HTML>

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Media Player Windows con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




