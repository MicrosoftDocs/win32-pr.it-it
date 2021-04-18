---
title: Playlist e oggetto PlaylistCollection
description: Playlist e oggetto PlaylistCollection
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Media Player di Windows, playlist
- Modello a oggetti di Windows Media Player, playlist
- modello a oggetti, playlist
- Windows Media Player Mobile, playlist
- Controllo ActiveX di Windows Media Player, playlist
- Controllo ActiveX Windows Media Player Mobile, playlist
- Controllo ActiveX, playlist
- playlists, oggetto PlaylistCollection
- playlist di metafile, oggetto PlaylistCollection
- Playlist del metafile di Windows Media, oggetto PlaylistCollection
- PlaylistCollection (oggetto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98744c2c5b97129db2824c42567802a374f90b6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298005"
---
# <a name="playlists-and-the-playlistcollection-object"></a>Playlist e oggetto PlaylistCollection

L'oggetto **PlaylistCollection** consente di accedere alle playlist nella libreria e include metodi per la creazione di nuove playlist vuote e nuove playlist da Metafile.

## <a name="working-with-existing-playlists"></a>Uso delle playlist esistenti

*PlaylistCollection*. **GetAll** e *PlaylistCollection*. i metodi **GetByName** restituiscono ciascuno un oggetto **PlaylistArray** , che può contenere più playlist.

*PlaylistCollection*. il metodo **GetAll** restituisce tutte le playlist presenti nella libreria. Ad esempio, è possibile chiamare questo metodo e recuperare le playlist nell'oggetto **PlaylistArray** per determinare se un determinato nome della playlist è già stato usato o per visualizzare tutte le playlist per l'utente. Il codice di esempio negli [attributi della playlist](playlist-attributes.md) usa il metodo **GetAll** .

*PlaylistCollection*. il metodo **GetByName** restituisce tutte le playlist con un nome specificato. È possibile usare questo metodo per gestire separatamente ogni playlist.

È anche possibile usare il metodo **GetByName** per recuperare una playlist univoca in base al nome. In tal caso, l'oggetto **PlaylistArray** ha un solo elemento. Nell'esempio C# riportato di seguito viene illustrata questa tecnica.


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a>Uso di nuove playlist

È possibile usare *PlaylistCollection*. metodo **nuova playlist** per creare una nuova playlist vuota. Il metodo restituisce un riferimento al nuovo oggetto **playlist** . È quindi possibile chiamare la *playlist*. metodo **appendItem** per aggiungere elementi multimediali alla playlist.

È anche possibile creare una nuova playlist basata su un metafile della playlist. Per prima cosa, passare il nome della playlist e il percorso del metafile al *lettore*. metodo **nuova playlist** . Tale metodo restituisce un riferimento al nuovo oggetto **playlist** . Passare quindi il nuovo oggetto **playlist** a *PlaylistCollection*. metodo **importPlaylist** per aggiungerlo alla libreria.

Si noti la differenza tra *PlaylistCollection*. metodo **nuova playlist** e *lettore*. metodo **nuova playlist** . Il metodo **PlaylistCollection** crea una nuova playlist vuota e la aggiunge alla libreria. Il metodo **Player** crea un nuovo oggetto **playlist** popolato ma non lo aggiunge alla libreria.

In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Nell'esempio C# riportato di seguito viene illustrata l'importazione di una playlist da un metafile. L'argomento *strPListName* specifica il nome della nuova playlist. *StrMetaFileName* specifica il nome del metafile da cui viene importata la playlist.


```C++
private IWMPPlaylist importPlaylist(string strPlaylistName, string strMetaFileName)
{
    IWMPPlaylist  NewPlaylist;
    IWMPPlaylist  ImportPlaylist;

    NewPlaylist = Player.newPlaylist(strPlaylistName, strMetaFileName);
    ImportPlaylist = Player.playlistCollection.importPlaylist(NewPlaylist);

    return ImportPlaylist;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Player. nuova playlist**](player-newplaylist.md)
</dt> <dt>

[**Playlist. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Oggetto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**PlaylistCollection (oggetto)**](playlistcollection-object.md)
</dt> <dt>

[**Playlist e elementi multimediali**](playlists-and-media-items.md)
</dt> </dl>

 

 




