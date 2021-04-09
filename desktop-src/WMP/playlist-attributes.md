---
title: Attributi della playlist
description: Attributi della playlist
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Media Player di Windows, playlist
- Modello a oggetti di Windows Media Player, playlist
- modello a oggetti, playlist
- Windows Media Player Mobile, playlist
- Controllo ActiveX di Windows Media Player, playlist
- Controllo ActiveX Windows Media Player Mobile, playlist
- Controllo ActiveX, playlist
- playlist, attributi
- playlist di metafile, attributi
- Elenchi di canzoni di Windows Media Metafile, attributi
- attributi, playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955340"
---
# <a name="playlist-attributes"></a>Attributi della playlist

Le playlist hanno informazioni sui metadati denominate attributi, così come gli elementi multimediali hanno attributi. È possibile recuperare i nomi e i valori degli attributi della playlist e visualizzarli nell'interfaccia utente oppure il codice può eseguire azioni in base al valore di un attributo.

Le playlist sono definite nei file organizzati in un formato XML e particolari elementi nel file definiscono gli attributi della playlist. Alcuni elementi attribute sono ben noti; L'autore del metafile può anche definire attributi arbitrari. Per ulteriori informazioni sugli elementi attributo nei file della playlist, vedere [recupero di metadati](retrieving-metadata.md).

La libreria può fornire attributi aggiuntivi della playlist, ad esempio **SourceURL** o **UserLastPlayedTime**. Per ulteriori informazioni sugli attributi della playlist della libreria, vedere le informazioni di [riferimento](attribute-reference.md)sugli attributi di Windows Media Player.

*Playlist*. la proprietà **attributeCount** Recupera il numero di attributi associati alla playlist. *Playlist*. la proprietà **attributeName** Recupera il nome di un attributo in base al relativo indice e alla *playlist*. il metodo **GetItemInfo** Recupera il valore di un attributo in base al nome.

È possibile modificare il valore di un attributo della playlist corrente con la *playlist*. metodo **setItemInfo** .

Un uso speciale del metodo **setItemInfo** consiste nell'ordinare gli elementi nella playlist usando l'attributo **SortAttribute** . Nell'esempio C# seguente viene ordinata una playlist in base ai valori dell'attributo **UserLastPlayedTime** . La variabile *playlist* è un riferimento a un oggetto **playlist** .


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Il codice di esempio C# seguente illustra il recupero degli attributi della playlist. La prima funzione, ShowPlaylists, compila un controllo ListBox con i nomi delle playlist disponibili. La seconda parte è il gestore eventi della casella di riepilogo. Quando l'utente fa clic sul nome di una playlist, questo codice recupera gli attributi per la playlist e visualizza tali attributi in una seconda casella di riepilogo.


```C++
// Member variables
IWMPPlaylistCollection PlaylistColl;
IWMPPlaylistArray PlaylistArray;

private void ShowPlaylists()
{
    // Retrieve the playlist collection
    PlaylistColl = Player.playlistCollection;
    // Store the collection in a playlist array
    PlaylistArray = PlaylistColl.getAll();

    // Retrieve the count of elements
    iCount = PlaylistArray.count;

    // Update the list box with the playlist names.
    lstPlaylist.BeginUpdate();
    for (int i=0; i<iCount; i++)
    {
        lstPlaylist.Items.Add(PlaylistArray.Item(i).name);
    }
    lstPlaylist.EndUpdate();

    // Set the selected index to zero
    lstPlaylist.SelectedIndex = 0;
}

```



L'evento SelectedIndexChanged per il controllo ListBox viene chiamato ogni volta che l'utente seleziona un nome della playlist. Il gestore eventi seguente riempie una seconda casella di riepilogo con i nomi degli attributi e i valori corrispondenti alla selezione dell'utente.


```C++
private void lstPlaylist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    IWMPPlaylist Playlist = PlaylistArray.Item(lstPlaylist.SelectedIndex);
    string strAttr="";
    string strItemNames="";
    int iAttribCount=0;

    iAttribCount = Playlist.attribCount;
    for (j=0; j<iAttribCount; j++)
    {
        strAttr=Playlist.get_attributeName(j) + " -- ";
        strAttr+=Playlist.getItemInfo(Playlist.get_attributeName(j));
        lstOutput.Items.Add(strAttr);
    }
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione delle playlist**](managing-playlists.md)
</dt> <dt>

[**Attributi elemento multimediale**](media-item-attributes.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> </dl>

 

 




