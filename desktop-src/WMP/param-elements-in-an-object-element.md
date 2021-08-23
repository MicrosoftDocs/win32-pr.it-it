---
title: Elementi PARAM in un elemento OBJECT
description: Elementi PARAM in un elemento OBJECT
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Windows Media Player,elementi PARAM nell'elemento OBJECT
- Windows Media Player modello a oggetti, elementi PARAM nell'elemento OBJECT
- modello a oggetti,elementi PARAM nell'elemento OBJECT
- Windows Media Player Elementi Mobile,PARAM nell'elemento OBJECT
- Windows Media Player ActiveX, elementi PARAM nell'elemento OBJECT
- Windows Media Player Controllo ActiveX per dispositivi mobili, elementi PARAM nell'elemento OBJECT
- ActiveX, elementi PARAM nell'elemento OBJECT
- incorporamento, pagine Web
- Incorporamento di pagine Web, elementi PARAM nell'elemento OBJECT
- Elementi PARAM nell'elemento OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da684a39739703038793abb2f4fdd32b924f35cdffc0c0f9d796fb7dbb5532b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054429"
---
# <a name="param-elements-in-an-object-element"></a>Elementi PARAM in un elemento OBJECT

Windows Media Player usa l'elemento PARAM per definire condizioni di avvio specifiche per il controllo. L'elemento PARAM è incorporato all'interno dell'elemento OBJECT.

Ad esempio, se si vuole definire se la **proprietà autoStart** è True, incorporare l'elemento PARAM all'interno dell'elemento OBJECT.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



È possibile avere il numero desiderato di elementi PARAM in un elemento OBJECT. PARAM ha due attributi, name e value. Entrambi gli attributi devono essere impostati.

Gli attributi PARAM supportati variano leggermente tra i browser e i tipi mime. La tabella seguente illustra gli attributi supportati dai browser Internet Explorer e Firefox. Il tipo mime preferito per il browser Firefox è application/x-ms-wmp, tuttavia, esistono diversi altri tipi mime che è possibile usare per incorporare il controllo Player in una pagina Web ospitata dal browser Firefox. La quarta colonna della tabella mostra gli attributi supportati quando si usa un tipo mime diverso da application/x-ms-wmp.



| Nome PARAM                                            | Internet Explorer | Firefox con tipo mime application/x-ms-wmp | Firefox con qualsiasi altro tipo mime |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [Autostart](settings-autostart.md)                   | sì               | sì                                         | sì                              |
| [Equilibrio](settings-balance.md)                       | sì               | sì                                         | sì                              |
| [baseURL](settings-baseurl.md)                       | sì               | sì                                         | sì                              |
| [captioningID](closedcaption-captioningid.md)        | sì               | sì                                         | sì                              |
| [currentMarker](controls-currentmarker.md)           | sì               | sì                                         | sì                              |
| [currentPosition](controls-currentposition.md)       | sì               | sì                                         | sì                              |
| [defaultFrame](settings-defaultframe.md)             | sì               | no                                          | no                               |
| [enableContextMenu](player-enablecontextmenu.md)     | sì               | sì                                         | sì                              |
| [abilitata](player-enabled.md)                         | sì               | sì                                         | sì                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | sì               | sì                                         | no                               |
| **Filename**                                          | no                | sì                                         | sì                              |
| [Fullscreen](player-fullscreen.md)                   | sì               | no                                          | no                               |
| [invokeURLs](settings-invokeurls.md)                 | sì               | no                                          | no                               |
| [Muto](settings-mute.md)                             | sì               | sì                                         | sì                              |
| [playCount](settings-playcount.md)                   | sì               | sì                                         | no                               |
| [Tasso](settings-rate.md)                             | sì               | sì                                         | sì                              |
| [SAMIFileName](closedcaption-samifilename.md)        | sì               | sì                                         | sì                              |
| [SAMILang](closedcaption-samilang.md)                | sì               | sì                                         | sì                              |
| [SAMIStyle](closedcaption-samistyle.md)              | sì               | sì                                         | sì                              |
| **Src**                                               | no                | sì                                         | sì                              |
| [stretchToFit](player-stretchtofit.md)               | sì               | sì                                         | no                               |
| [URL](player-url.md)                                 | sì               | sì                                         | sì                              |
| [Volume](settings-volume.md)                         | sì               | sì                                         | sì                              |
| [windowlessVideo](player-windowlessvideo.md)         | sì               | sì                                         | sì                              |



 

> [!Note]  
> Gli **elementi fileName** **e SRC** PARAM sono supportati dal plug-in Firefox, ma non da Internet Explorer. Entrambi eseguono la stessa funzione **dell'elemento URL** PARAM.

 

Per altri dettagli sui valori [per ogni attributo name,](object-model-reference-for-scripting.md) vedere Object Model Reference for Scripting (Riferimento al modello a oggetti per gli script).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del Windows Media Player in una pagina Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




