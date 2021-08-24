---
title: Uso di script in una pagina Web visualizzata da Firefox
description: Uso di script in una pagina Web visualizzata da Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
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
- Windows Media Player ActiveX, esempio di scripting
- Windows Media Player Controllo ActiveX per dispositivi mobili, esempio di scripting
- ActiveX, esempio di scripting
- incorporamento, pagine Web
- Incorporamento di pagine Web, esempio di scripting
- Windows Media Player,Firefox
- Windows Media Player a oggetti, Firefox
- modello a oggetti,Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX controllo, Firefox
- Windows Media Player Controllo ActiveX per dispositivi mobili,Firefox
- ActiveX controllo, Firefox
- Firefox, esempio di scripting
- incorporamento di pagine Web,Firefox
- Esempio di scripting per l'incorporamento di pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450b03f7adefca1a887fb31207f0a3280e1925c9d3e1f1066df370d87f0a7779
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762061"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>Uso di script in una pagina Web visualizzata da Firefox

Lo script in una pagina Web può usare il modello a oggetti Player per controllare player mentre l'utente interagisce con la pagina. Ad esempio, l'elemento INPUT seguente include uno script che imposta il volume player.


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



Molti degli oggetti nel modello Windows Media Player a oggetti sono supportati da Internet Explorer e dal plug-in Firefox. Tuttavia, esistono alcuni oggetti che non sono supportati dal plug-in Firefox. La tabella seguente elenca tutti gli oggetti nel modello a oggetti di Player e mostra gli oggetti supportati dal plug-in Firefox.



| Oggetto                                              | Supporto di Firefox |
|-----------------------------------------------------|-----------------|
| [Cdrom](cdrom-object.md)                           | no              |
| [CdromCollection](cdromcollection-object.md)       | no              |
| [ClosedCaption](closedcaption-object.md)           | sì             |
| [Controlli](controls-object.md)                     | no              |
| [Dvd](dvd-object.md)                               | no              |
| [Error (Errore) (Error (Errore)e)](error-object.md)                           | sì             |
| [ErrorItem](erroritem-object.md)                   | sì             |
| [Supporti](media-object.md)                           | sì             |
| [MediaCollection](mediacollection-object.md)       | no              |
| [MetadataPicture](metadatapicture-object.md)       | no              |
| [MetadataText](metadatatext-object.md)             | no              |
| [Network](network-object.md)                       | sì             |
| [Player](player-object.md)                         | sì             |
| [PlayerApplication](playerapplication-object.md)   | no              |
| [Playlist](playlist-object.md)                     | sì             |
| [PlaylistArray](playlistarray-object.md)           | no              |
| [PlaylistCollection](playlistcollection-object.md) | no              |
| [Query](query-object.md)                           | no              |
| [Impostazioni](settings-object.md)                     | sì             |
| [StringCollection](stringcollection-object.md)     | no              |



 

Il plug-in Firefox supporta **l'oggetto Player,** ma alcune proprietà dell'oggetto **Player** restituiscono **NULL** in un browser Firefox. Ad esempio, la [proprietà cdromCollection](player-cdromcollection.md) dell'oggetto **Player** restituisce **NULL** perché il plug-in Firefox non supporta l'oggetto **Cdrom.** Analogamente, le proprietà [dvd](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md)e [playlistCollection](player-playlistcollection.md) dell'oggetto **Player** restituiscono **NULL** in un browser Firefox.

La **proprietà Player.pluginVersionInfo** è supportata dal plug-in Firefox, ma non da Internet Explorer. Questa proprietà restituisce la versione del plug-in Firefox.

Il plug-in Firefox supporta **l'oggetto Media,** inclusa la [proprietà getItemInfoByType.](media-getiteminfobytype.md) Tuttavia, in un browser Firefox, la **proprietà getItemInfoByType** non supporta i tipi restituiti **MetadataText** e **MetadataPicture.**

Il plug-in Firefox supporta [l'oggetto Impostazioni,](settings-object.md) ad eccezione del [metodo setMode](settings-setmode.md) e della [proprietà requestMediaAccessRights.](settings-requestmediaaccessrights.md) In un browser Firefox la **proprietà requestMediaAccessRight** restituisce sempre false.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Windows Media Player con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




