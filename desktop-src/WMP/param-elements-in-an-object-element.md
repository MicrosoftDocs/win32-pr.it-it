---
title: Elementi PARAM in un elemento OBJECT
description: Elementi PARAM in un elemento OBJECT
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Media Player di Windows, elementi PARAM nell'elemento OBJECT
- Modello a oggetti di Windows Media Player, elementi PARAM nell'elemento OBJECT
- modello a oggetti, elementi PARAM nell'elemento OBJECT
- Windows Media Player Mobile, elementi PARAM nell'elemento oggetto
- Controllo ActiveX Windows Media Player, elementi PARAM nell'elemento OBJECT
- Controllo ActiveX Windows Media Player Mobile, elementi PARAM nell'elemento oggetto
- Controllo ActiveX, elementi PARAM nell'elemento OBJECT
- incorporamento, pagine Web
- Incorporamento di pagine Web, elementi PARAM nell'elemento OBJECT
- Elementi PARAM nell'elemento OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0fc5b9f64fa462386ec037eba34ed4e0659bb1
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "103857046"
---
# <a name="param-elements-in-an-object-element"></a>Elementi PARAM in un elemento OBJECT

Windows Media Player utilizza l'elemento PARAM per definire condizioni di avvio specifiche per il controllo. L'elemento PARAM è incorporato all'interno dell'elemento OBJECT.

Se, ad esempio, si desidera definire se la proprietà **autostart** è true, è necessario incorporare l'elemento param nell'elemento Object.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



È possibile avere tutti gli elementi PARAM in un elemento oggetto desiderato. PARAM ha due attributi, Name e value. È necessario impostare entrambi gli attributi.

Gli attributi PARAM supportati variano leggermente tra i browser e i tipi MIME. La tabella seguente Mostra gli attributi supportati dai browser di Internet Explorer e Firefox. Il tipo MIME preferito per il browser Firefox è application/x-ms-WMP. Tuttavia, esistono diversi altri tipi MIME che è possibile usare per incorporare il controllo Player in una pagina Web ospitata dal browser Firefox. La quarta colonna della tabella Mostra gli attributi supportati quando si usa un tipo MIME diverso da Application/x-ms-WMP.



| Nome PARAM                                            | Internet Explorer | Firefox con tipo MIME application/x-ms-WMP | Firefox con qualsiasi altro tipo MIME |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [Avvio automatico](settings-autostart.md)                   | sì               | sì                                         | sì                              |
| [bilanciare](settings-balance.md)                       | sì               | sì                                         | sì                              |
| [baseURL](settings-baseurl.md)                       | sì               | sì                                         | sì                              |
| [captioningID](closedcaption-captioningid.md)        | sì               | sì                                         | sì                              |
| [currentMarker](controls-currentmarker.md)           | sì               | sì                                         | sì                              |
| [currentPosition](controls-currentposition.md)       | sì               | sì                                         | sì                              |
| [defaultFrame](settings-defaultframe.md)             | sì               | no                                          | no                               |
| [enableContextMenu](player-enablecontextmenu.md)     | sì               | sì                                         | sì                              |
| [abilitato](player-enabled.md)                         | sì               | sì                                         | sì                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | sì               | sì                                         | no                               |
| **fileName**                                          | no                | sì                                         | sì                              |
| [Schermo intero](player-fullscreen.md)                   | sì               | no                                          | no                               |
| [invokeURLs](settings-invokeurls.md)                 | sì               | no                                          | no                               |
| [mute](settings-mute.md)                             | sì               | sì                                         | sì                              |
| [playCount](settings-playcount.md)                   | sì               | sì                                         | no                               |
| [tasso](settings-rate.md)                             | sì               | sì                                         | sì                              |
| [SAMIFileName](closedcaption-samifilename.md)        | sì               | sì                                         | sì                              |
| [SAMILang](closedcaption-samilang.md)                | sì               | sì                                         | sì                              |
| [SAMIStyle](closedcaption-samistyle.md)              | sì               | sì                                         | sì                              |
| **SRC**                                               | no                | sì                                         | sì                              |
| [stretchToFit](player-stretchtofit.md)               | sì               | sì                                         | no                               |
| [URL](player-url.md)                                 | sì               | sì                                         | sì                              |
| [volume](settings-volume.md)                         | sì               | sì                                         | sì                              |
| [windowlessVideo](player-windowlessvideo.md)         | sì               | sì                                         | sì                              |



 

> [!Note]  
> Gli elementi **filename** e **src** param sono supportati dal plug-in di Firefox, ma non da Internet Explorer. Entrambi eseguono la stessa funzione dell'elemento param dell' **URL** .

 

Per ulteriori informazioni sui valori per ogni attributo Name, vedere [riferimento del modello a oggetti per lo scripting](object-model-reference-for-scripting.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Media Player di Windows in una pagina Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




