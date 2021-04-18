---
title: Informazioni sugli oggetti playlist, PlaylistCollection e PlaylistArray
description: Informazioni sugli oggetti playlist, PlaylistCollection e PlaylistArray
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Windows Media Player, oggetto playlist
- Modello a oggetti di Windows Media Player, oggetto playlist
- modello a oggetti, oggetto playlist
- Controllo ActiveX Windows Media Player, oggetto playlist
- Controllo ActiveX, oggetto playlist
- Controllo ActiveX Windows Media Player Mobile, oggetto playlist
- Windows Media Player Mobile, oggetto playlist
- Oggetto playlist
- Windows Media Player, oggetto PlaylistCollection
- Modello a oggetti di Windows Media Player, oggetto PlaylistCollection
- modello a oggetti, oggetto PlaylistCollection
- Controllo ActiveX Windows Media Player, oggetto PlaylistCollection
- Controllo ActiveX, oggetto PlaylistCollection
- Controllo ActiveX Windows Media Player Mobile, oggetto PlaylistCollection
- Windows Media Player Mobile, oggetto PlaylistCollection
- PlaylistCollection (oggetto)
- Windows Media Player, oggetto PlaylistArray
- Modello a oggetti di Windows Media Player, oggetto PlaylistArray
- modello a oggetti, oggetto PlaylistArray
- Controllo ActiveX Windows Media Player, oggetto PlaylistArray
- Controllo ActiveX, oggetto PlaylistArray
- Controllo ActiveX Windows Media Player Mobile, oggetto PlaylistArray
- Windows Media Player Mobile, oggetto PlaylistArray
- Oggetto PlaylistArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298225"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a>Informazioni sugli oggetti playlist, PlaylistCollection e PlaylistArray

Gli oggetti playlist, **PlaylistCollection** e **PlaylistArray** governano le playlist che Windows Media Player può usare per specificare l'ordine in cui verrà riprodotto **il contenuto**. Si ottiene l'oggetto **PlaylistCollection** dalla proprietà **PlaylistCollection** dell'oggetto **Player** . La proprietà **PlaylistCollection** restituisce l'oggetto **PlaylistCollection** . È possibile accedere alle proprietà dell'oggetto **PlaylistCollection** solo dopo averlo creato. Ad esempio, per creare una nuova playlist, è innanzitutto necessario ottenere l'oggetto **PlaylistCollection** e quindi usare un metodo su tale oggetto.


```C++
player.playlistcollection.newplaylist('myplaylist');
```



È possibile ottenere la playlist corrente usando la proprietà **currentPlaylist** . Per ottenere, ad esempio, il nome della playlist corrente, usare il codice seguente:


```C++
myname = player.currentplaylist.name;
```



L'oggetto **PlaylistArray** viene restituito dai metodi **GetAll** e **GetByName** dell'oggetto **PlaylistCollection** . Per ottenere il numero di playlist, ad esempio, usare il codice seguente:


```C++
howmany = player.playlistcollection.getAll().count;
```



Per recuperare una playlist nota in base al nome, usare il codice seguente:


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modello a oggetti del lettore per i linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**Oggetto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**PlaylistCollection (oggetto)**](playlistcollection-object.md)
</dt> </dl>

 

 




