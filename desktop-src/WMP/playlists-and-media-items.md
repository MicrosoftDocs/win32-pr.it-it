---
title: Playlist e elementi multimediali
description: Playlist e elementi multimediali
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Media Player di Windows, playlist
- Modello a oggetti di Windows Media Player, playlist
- modello a oggetti, playlist
- Windows Media Player Mobile, playlist
- Controllo ActiveX di Windows Media Player, playlist
- Controllo ActiveX Windows Media Player Mobile, playlist
- Controllo ActiveX, playlist
- playlist, elementi multimediali
- playlist di metafile, elementi multimediali
- Playlist Windows Media Metafile, elementi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955325"
---
# <a name="playlists-and-media-items"></a>Playlist e elementi multimediali

Una playlist è un set di elementi multimediali. Un oggetto **playlist** può modificare gli oggetti **multimediali** che rappresentano tali elementi.

## <a name="retrieving-media-items"></a>Recupero di elementi multimediali

Per una playlist esistente, è possibile leggere la *playlist*. proprietà **count** per determinare il numero di elementi multimediali presenti nella playlist ed è possibile ottenere un riferimento all'oggetto **multimediale** corrispondente a un elemento specifico usando la *playlist*. proprietà **Item** .

Nell'esempio C# seguente viene recuperato un riferimento a un oggetto in un elemento multimediale specifico. (In questo argomento, la variabile *plist* è un riferimento a un oggetto **playlist** ).


```C++
currMedia = pList.Item(0);

```



Nell'esempio C# seguente vengono recuperati i nomi di tutti gli elementi multimediali in una playlist e inseriti in una casella di riepilogo denominata lstOutput.


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a>Aggiunta di elementi a una playlist

È possibile aggiungere un elemento multimediale alla fine di una playlist o in una posizione specifica in una playlist, usando la *playlist*. **appendItem** e *playlist*. metodi **InsertItem** .

In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Nell'esempio C# seguente vengono illustrate entrambe le tecniche aggiungendo l'elemento multimediale corrente a una playlist denominata "BluesTest", prima alla fine e quindi all'inizio della playlist.


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



Quando si crea una nuova playlist vuota utilizzando *PlaylistCollection*. metodo **nuova playlist** , è possibile aggiungere elementi multimediali chiamando ripetutamente la *playlist*. metodo **appendItem** .

## <a name="manipulating-media-items-in-a-playlist"></a>Manipolazione di elementi multimediali in una playlist

È possibile modificare la posizione di un elemento multimediale nella playlist usando la *playlist*. metodo **moveItem** . L'elemento viene specificato in base al relativo indice corrente, quindi viene specificato il nuovo indice. L'esempio C# seguente sposta un elemento dall'indice 5 all'indice 0 all'interno di una playlist.


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



È possibile rimuovere un elemento multimediale dalla playlist usando la **playlist**. metodo **RemoveItem** . Si noti che se l'elemento rimosso non è l'elemento finale nella playlist, i valori di indice degli elementi successivi cambiano. Nell'esempio C# seguente viene rimosso l'elemento specificato.


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> Gli utenti possono modificare il contenuto di una playlist all'esterno dell'applicazione. Ogni volta che si modificano gli elementi in una playlist, è necessario monitorare e gestire gli eventi correlati alla playlist del controllo Media Player Windows per verificare il corretto funzionamento del codice. Questi eventi sono *Player*. **CurrentPlaylistChange** e *Player*. **PlaylistChange**.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> </dl>

 

 




