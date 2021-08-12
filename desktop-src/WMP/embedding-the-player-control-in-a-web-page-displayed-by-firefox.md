---
title: Incorporamento del controllo Player in una pagina Web visualizzata da Firefox
description: Incorporamento del controllo Player in una pagina Web visualizzata da Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Windows Media Player,incorporamento ActiveX controllo
- Windows Media Player a oggetti, incorporamento ActiveX controllo
- modello a oggetti, incorporamento ActiveX controllo
- Windows Media Player Dispositivi mobili, incorporamento ActiveX controllo
- Windows Media Player ActiveX, incorporamento
- Windows Media Player Controllo ActiveX per dispositivi mobili, incorporamento
- ActiveX, incorporamento
- Windows Media Player ActiveX, pagine Web
- Windows Media Player Controllo ActiveX per dispositivi mobili, pagine Web
- ActiveX, pagine Web
- Windows Media Player,Firefox
- Windows Media Player a oggetti, Firefox
- modello a oggetti,Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX controllo, Firefox
- Windows Media Player Controllo ActiveX per dispositivi mobili,Firefox
- ActiveX controllo, Firefox
- Firefox, informazioni sull'incorporamento di pagine Web
- incorporamento, pagine Web
- incorporamento di pagine Web,Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c1db799df78cb6c62516798f4bbd196c093f02225386f0c1009bfa11d9a668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578588"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Incorporamento del controllo Player in una pagina Web visualizzata da Firefox

Per incorporare il controllo Windows Media Player in una pagina Web che può essere visualizzata da un browser Firefox, creare un elemento OBJECT o un elemento EMBED con uno dei tipi MIME seguenti come attributo **type:**

-   application/x-ms-wmp
-   application/asx
-   video/x-ms-asf-plugin
-   application/x-mplayer2
-   video/x-ms-asf
-   video/x-ms-wm
-   audio/x-ms-wma
-   audio/x-ms-cerere
-   video/x-ms-wmv
-   video/x-ms-wvx

Il tipo mime preferito è application/x-ms-wmp.

Gli esempi seguenti illustrano come incorporare il controllo Player usando un elemento OBJECT o un elemento EMBED.


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



Gli esempi precedenti funzionano in Firefox, ma non in Internet Explorer. Per incorporare il controllo Player in una pagina Web che può essere visualizzata da Internet Explorer, è necessario creare un elemento OBJECT con un attributo **classid** impostato sull'ID classe del controllo Windows Media Player.

L'esempio seguente illustra come incorporare il controllo Windows Media Player in una pagina Web che può essere visualizzata correttamente sia da Internet Explorer che da Firefox. Lo script nella pagina rileva il tipo di browser e genera il tag OBJECT appropriato.


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

[**Uso del controllo Windows Media Player con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




