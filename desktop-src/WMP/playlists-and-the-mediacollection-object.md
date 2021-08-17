---
title: Playlist e oggetto MediaCollection
description: Playlist e oggetto MediaCollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Windows Media Player,playlist
- Windows Media Player a oggetti, playlist
- modello a oggetti, playlist
- Windows Media Player Dispositivi mobili, playlist
- Windows Media Player ActiveX controllo, playlist
- Windows Media Player Controllo ActiveX per dispositivi mobili, playlist
- ActiveX, playlist
- playlist, oggetto MediaCollection
- playlist di metafile, oggetto MediaCollection
- Windows Playlist di metafile multimediali, oggetto MediaCollection
- Oggetto MediaCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a0bba2e966e51523dc24965c2f2a066767b059f26a08fde9ee5856a1694df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334454"
---
# <a name="playlists-and-the-mediacollection-object"></a>Playlist e oggetto MediaCollection

**L'oggetto MediaCollection** consente di accedere a un'ampia gamma di playlist speciali e include un metodo per creare una nuova playlist da un metafile.

I metodi seguenti recuperano playlist speciali:

-   **getAll**
-   **getByAlbum**
-   **getByAttribute**
-   **getByAuthor**
-   **getByGenre**
-   **getByName**

Come suggerito dai nomi, questi metodi recuperano playlist contenenti tutti gli elementi multimediali nella libreria che soddisfano determinati criteri.

Prestare attenzione a non confondere *MediaCollection*. **Metodo getByName** con *PlaylistCollection*. **Metodo getByName.** Il **metodo MediaCollection** restituisce un oggetto **Playlist** contenente tutti gli elementi multimediali con il nome specificato. Il **metodo PlaylistCollection** restituisce un **oggetto PlaylistArray** contenente tutte le playlist con il nome specificato.

È possibile usare *MediaCollection*. **Metodo add** per aggiungere playlist e elementi multimediali alla libreria. Per aggiungere una playlist, passare al metodo il percorso del metafile che definisce la playlist. Il metodo restituisce sempre un **oggetto Media.** Non è possibile eseguire il cast **tra oggetti Media** e **Playlist.** Per usare la playlist aggiunta, recuperare l'oggetto **Playlist** con lo stesso nome dell'oggetto **Media.**

Nell'esempio C# seguente viene illustrato come recuperare i supporti in base al tipo usando **MediaCollection**. **Metodo getByAttribute.** Questo codice recupera i nomi di tutti gli attributi associati a un determinato tipo, nonché lo stato di lettura/scrittura o di sola lettura di tali attributi. Genera un singolo file che contiene elenchi di attributi per i tipi Audio, Video, Radio, Playlist, Other, Musica e Photo.


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



L'esempio C# seguente illustra come aggiungere una playlist da un metafile alla libreria.


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



Le playlist statiche includono elementi multimediali specifici. Le playlist automatica esereranno ricerche nella libreria ogni volta che vengono aperte e possono contenere elementi multimediali diversi in momenti diversi. È possibile aggiungere sia playlist statiche che playlist auto alla libreria usando *MediaCollection*. **Metodo add.** È anche possibile aggiungere playlist statiche usando *PlaylistCollection*. **Metodo importPlaylist.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**Oggetto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Playlist e oggetto PlaylistCollection**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**Playlist statiche e auto**](static-and-auto-playlists.md)
</dt> </dl>

 

 




