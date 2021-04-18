---
title: Utilizzo di script in una pagina Web visualizzata da Firefox
description: Utilizzo di script in una pagina Web visualizzata da Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
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
- Controllo ActiveX di Windows Media Player, esempio di scripting
- Controllo ActiveX Windows Media Player Mobile, esempio di scripting
- Controllo ActiveX, esempio di scripting
- incorporamento, pagine Web
- Incorporamento di pagine Web, esempio di scripting
- Windows Media Player, Firefox
- Modello a oggetti di Windows Media Player, Firefox
- modello a oggetti, Firefox
- Windows Media Player Mobile, Firefox
- Controllo ActiveX di Windows Media Player, Firefox
- Controllo ActiveX Windows Media Player Mobile, Firefox
- Controllo ActiveX, Firefox
- Firefox, esempio di scripting
- Incorporamento di pagine Web, Firefox
- esempio di script per l'incorporamento di pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "106299009"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>Utilizzo di script in una pagina Web visualizzata da Firefox

Script in una pagina Web può usare il modello a oggetti del lettore per controllare il lettore quando l'utente interagisce con la pagina. Ad esempio, l'elemento di INPUT seguente contiene uno script che imposta il volume del lettore.


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



Molti degli oggetti nel modello a oggetti di Windows Media Player sono supportati da Internet Explorer e dal plug-in Firefox. Alcuni oggetti, tuttavia, non sono supportati dal plug-in di Firefox. La tabella seguente elenca tutti gli oggetti nel modello a oggetti del lettore e Mostra gli oggetti supportati dal plug-in di Firefox.



| Oggetto                                              | Supporto di Firefox |
|-----------------------------------------------------|-----------------|
| [Cdrom](cdrom-object.md)                           | no              |
| [Cdromcollection](cdromcollection-object.md)       | no              |
| [ClosedCaption](closedcaption-object.md)           | sì             |
| [Controlli](controls-object.md)                     | no              |
| [DVD](dvd-object.md)                               | no              |
| [Error (Errore) (Error (Errore)e)](error-object.md)                           | sì             |
| [ErrorItem](erroritem-object.md)                   | sì             |
| [Supporti](media-object.md)                           | sì             |
| [Mediacollection](mediacollection-object.md)       | no              |
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



 

Il plug-in di Firefox supporta l'oggetto **Player** , ma alcune proprietà dell'oggetto **Player** restituiscono **null** in un browser Firefox. Ad esempio, la proprietà [cdromcollection](player-cdromcollection.md) dell'oggetto **Player** restituisce **null** perché il plug-in di Firefox non supporta l'oggetto **CDROM** . Analogamente, le proprietà [DVD](player-dvd.md), [mediacollection](player-mediacollection.md), [playerApplication](player-playerapplication.md)e [PlaylistCollection](player-playlistcollection.md) dell'oggetto **Player** restituiscono **null** in un browser Firefox.

La proprietà **Player. pluginVersionInfo** è supportata dal plug-in di Firefox ma non da Internet Explorer. Questa proprietà restituisce la versione del plug-in Firefox.

Il plug-in di Firefox supporta l'oggetto **multimediale** , inclusa la proprietà [getItemInfoByType](media-getiteminfobytype.md) . Tuttavia, in un browser Firefox, la proprietà **getItemInfoByType** non supporta i tipi restituiti **MetadataText** e **MetadataPicture** .

Il plug-in di Firefox supporta l'oggetto [Settings](settings-object.md) , ad eccezione del metodo [semode](settings-setmode.md) e della proprietà [requestMediaAccessRights](settings-requestmediaaccessrights.md) . In un browser Firefox, la proprietà **requestMediaAccessRight** restituisce sempre false.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Media Player Windows con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




