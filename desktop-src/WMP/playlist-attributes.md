---
title: Attributi della playlist
description: Attributi della playlist
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Windows Media Player,playlist
- Windows Media Player a oggetti, playlist
- modello a oggetti, playlist
- Windows Media Player Dispositivi mobili, playlist
- Windows Media Player ActiveX controllo, playlist
- Windows Media Player Controllo ActiveX per dispositivi mobili, playlist
- ActiveX, playlist
- playlist, attributi
- playlist di metafile, attributi
- Windows playlist metafile multimediali,attributi
- attributi, playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00416f641fac89c707405c03dc70af0497b34d4cf646aa44fad5124f97f09a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995711"
---
# <a name="playlist-attributes"></a>Attributi della playlist

Le playlist hanno informazioni sui metadati denominate attributi, proprio come gli elementi multimediali hanno attributi. È possibile recuperare i nomi e i valori degli attributi della playlist e visualizzarli nell'interfaccia utente oppure il codice può eseguire azioni in base al valore di un attributo.

Le playlist sono definite in file organizzati in formato XML e determinati elementi nel file definiscono gli attributi della playlist. Alcuni elementi di attributo sono noti. L'autore del metafile può anche definire attributi arbitrari. Per altre informazioni sugli elementi attributo nei file di playlist, vedere [Recupero di metadati](retrieving-metadata.md).

La libreria può fornire attributi di playlist aggiuntivi, ad esempio **SourceURL** o **UserLastPlayedTime.** Per altre informazioni sugli attributi della playlist della libreria, vedere le informazioni di Windows Media Player [sugli attributi](attribute-reference.md).

Playlist . **la proprietà attributeCount** recupera il numero di attributi associati alla playlist. Playlist . **la proprietà attributeName** recupera il nome di un attributo in base al relativo indice e la *playlist*. **Il metodo getItemInfo** recupera il valore di un attributo in base al nome.

È possibile modificare il valore di un attributo della playlist corrente con *playlist*. **Metodo setItemInfo.**

Un uso speciale del **metodo setItemInfo** è quello di ordinare gli elementi nella playlist usando l'attributo **SortAttribute.** Nell'esempio C# seguente una playlist viene ordinata in base ai valori **dell'attributo UserLastPlayedTime.** La variabile *Playlist* è un riferimento a un **oggetto Playlist.**


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



In questo argomento **l'oggetto Player** è stato definito nel modo seguente:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Il codice di esempio C# seguente illustra il recupero degli attributi della playlist. La prima funzione, ShowPlaylists, popola un controllo ListBox con i nomi delle playlist disponibili. La seconda parte è il gestore dell'evento della casella di riepilogo. Quando l'utente fa clic sul nome di una playlist, questo codice recupera gli attributi per tale playlist e visualizza tali attributi in una seconda casella di riepilogo.


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



L'evento SelectedIndexChanged per il controllo ListBox viene chiamato ogni volta che l'utente seleziona un nome di playlist. Il gestore eventi seguente riempie una seconda casella di riepilogo con i nomi degli attributi e i valori corrispondenti alla selezione dell'utente.


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

[**Attributi dell'elemento multimediale**](media-item-attributes.md)
</dt> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> </dl>

 

 




