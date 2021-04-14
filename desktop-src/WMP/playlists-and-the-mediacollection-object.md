---
title: Playlist e oggetto Mediacollection
description: Playlist e oggetto Mediacollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Media Player di Windows, playlist
- Modello a oggetti di Windows Media Player, playlist
- modello a oggetti, playlist
- Windows Media Player Mobile, playlist
- Controllo ActiveX di Windows Media Player, playlist
- Controllo ActiveX Windows Media Player Mobile, playlist
- Controllo ActiveX, playlist
- playlist, oggetto Mediacollection
- playlist di metafile, oggetto Mediacollection
- Playlist di Windows Media Metafile, oggetto Mediacollection
- Mediacollection (oggetto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395662"
---
# <a name="playlists-and-the-mediacollection-object"></a>Playlist e oggetto Mediacollection

L'oggetto **mediacollection** consente di accedere a un'ampia gamma di playlist speciali e include un metodo per la creazione di una nuova playlist da un metafile.

I metodi seguenti recuperano playlist speciali:

-   **getAll**
-   **getByAlbum**
-   **getByAttribute**
-   **getByAuthor**
-   **getByGenre**
-   **getByName**

Come suggerisce il nome, questi metodi recuperano le playlist che contengono tutti gli elementi multimediali nella libreria che corrispondono a determinati criteri.

Prestare attenzione a non confondere l'elemento *mediacollection*. metodo **GetByName** con *PlaylistCollection*. metodo **GetByName** . Il metodo **mediacollection** restituisce un oggetto **playlist** contenente tutti gli elementi multimediali con il nome specificato. Il metodo **PlaylistCollection** restituisce un oggetto **PlaylistArray** contenente tutte le playlist con il nome specificato.

È possibile usare *mediacollection*. **aggiungere** un metodo per aggiungere playlist e elementi multimediali alla libreria. Per aggiungere una playlist, passare il metodo al percorso del metafile che definisce la playlist. Il metodo restituisce sempre un oggetto **multimediale** . Non è possibile eseguire il cast tra oggetti **supporto** e **playlist** . Per usare la playlist aggiunta, recuperare l'oggetto **playlist** con lo stesso nome dell'oggetto **multimediale** .

Nell'esempio C# riportato di seguito viene illustrato come recuperare i supporti per tipo utilizzando **mediacollection**. metodo **getByAttribute** . Questo codice recupera i nomi di tutti gli attributi associati a un tipo specificato, nonché lo stato di lettura/scrittura o di sola lettura di tali attributi. Genera un singolo file che contiene elenchi di attributi per i tipi audio, video, Radio, playlist, other, Music e Photo.


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



Nell'esempio C# riportato di seguito viene illustrato come aggiungere una playlist da un metafile alla libreria.


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



Le playlist statiche includono elementi multimediali specifici. Le playlist automatiche eseguono ricerche nella libreria ogni volta che vengono aperte e possono contenere elementi multimediali diversi in momenti diversi. È possibile aggiungere playlist statiche e automatiche alla libreria usando *mediacollection*. **aggiungere** il metodo. È anche possibile aggiungere playlist statiche usando *PlaylistCollection*. metodo **importPlaylist** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection (oggetto)**](playlistcollection-object.md)
</dt> <dt>

[**Playlist e oggetto PlaylistCollection**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**Playlist statiche e automatiche**](static-and-auto-playlists.md)
</dt> </dl>

 

 




