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
# <a name="playlist-attributes"></a><span data-ttu-id="561cd-114">Attributi della playlist</span><span class="sxs-lookup"><span data-stu-id="561cd-114">Playlist Attributes</span></span>

<span data-ttu-id="561cd-115">Le playlist hanno informazioni sui metadati denominate attributi, così come gli elementi multimediali hanno attributi.</span><span class="sxs-lookup"><span data-stu-id="561cd-115">Playlists have metadata information called attributes, just as media items have attributes.</span></span> <span data-ttu-id="561cd-116">È possibile recuperare i nomi e i valori degli attributi della playlist e visualizzarli nell'interfaccia utente oppure il codice può eseguire azioni in base al valore di un attributo.</span><span class="sxs-lookup"><span data-stu-id="561cd-116">You can retrieve the names and values of playlist attributes and display them in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="561cd-117">Le playlist sono definite nei file organizzati in un formato XML e particolari elementi nel file definiscono gli attributi della playlist.</span><span class="sxs-lookup"><span data-stu-id="561cd-117">Playlists are defined in files organized in an XML format, and particular elements in the file define playlist attributes.</span></span> <span data-ttu-id="561cd-118">Alcuni elementi attribute sono ben noti; L'autore del metafile può anche definire attributi arbitrari.</span><span class="sxs-lookup"><span data-stu-id="561cd-118">Some attribute elements are well-known; the author of the metafile can also define arbitrary attributes.</span></span> <span data-ttu-id="561cd-119">Per ulteriori informazioni sugli elementi attributo nei file della playlist, vedere [recupero di metadati](retrieving-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="561cd-119">For more information about attribute elements in playlist files, see [Retrieving Metadata](retrieving-metadata.md).</span></span>

<span data-ttu-id="561cd-120">La libreria può fornire attributi aggiuntivi della playlist, ad esempio **SourceURL** o **UserLastPlayedTime**.</span><span class="sxs-lookup"><span data-stu-id="561cd-120">The library may provide additional playlist attributes, such as **SourceURL** or **UserLastPlayedTime**.</span></span> <span data-ttu-id="561cd-121">Per ulteriori informazioni sugli attributi della playlist della libreria, vedere le informazioni di [riferimento](attribute-reference.md)sugli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="561cd-121">For more information about the library playlist attributes, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="561cd-122">*Playlist*. la proprietà **attributeCount** Recupera il numero di attributi associati alla playlist.</span><span class="sxs-lookup"><span data-stu-id="561cd-122">The *Playlist*.**attributeCount** property retrieves the number of attributes associated with the playlist.</span></span> <span data-ttu-id="561cd-123">*Playlist*. la proprietà **attributeName** Recupera il nome di un attributo in base al relativo indice e alla *playlist*. il metodo **GetItemInfo** Recupera il valore di un attributo in base al nome.</span><span class="sxs-lookup"><span data-stu-id="561cd-123">The *Playlist*.**attributeName** property retrieves the name of an attribute based on its index, and the *Playlist*.**getItemInfo** method retrieves the value of an attribute based on its name.</span></span>

<span data-ttu-id="561cd-124">È possibile modificare il valore di un attributo della playlist corrente con la *playlist*. metodo **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="561cd-124">You can modify the value of an attribute of the current playlist with the *Playlist*.**setItemInfo** method.</span></span>

<span data-ttu-id="561cd-125">Un uso speciale del metodo **setItemInfo** consiste nell'ordinare gli elementi nella playlist usando l'attributo **SortAttribute** .</span><span class="sxs-lookup"><span data-stu-id="561cd-125">A special use of the **setItemInfo** method is to sort the items in the playlist, using the **SortAttribute** attribute.</span></span> <span data-ttu-id="561cd-126">Nell'esempio C# seguente viene ordinata una playlist in base ai valori dell'attributo **UserLastPlayedTime** .</span><span class="sxs-lookup"><span data-stu-id="561cd-126">The following C# example sorts a playlist by the values of the **UserLastPlayedTime** attribute.</span></span> <span data-ttu-id="561cd-127">La variabile *playlist* è un riferimento a un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="561cd-127">The variable *Playlist* is a reference to a **Playlist** object.</span></span>


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



<span data-ttu-id="561cd-128">In questo argomento, l'oggetto **Player** è stato definito nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="561cd-128">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="561cd-129">Il codice di esempio C# seguente illustra il recupero degli attributi della playlist.</span><span class="sxs-lookup"><span data-stu-id="561cd-129">The following C# example code demonstrates retrieving playlist attributes.</span></span> <span data-ttu-id="561cd-130">La prima funzione, ShowPlaylists, compila un controllo ListBox con i nomi delle playlist disponibili.</span><span class="sxs-lookup"><span data-stu-id="561cd-130">The first function, ShowPlaylists, populates a ListBox control with the names of the available playlists.</span></span> <span data-ttu-id="561cd-131">La seconda parte è il gestore eventi della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="561cd-131">The second part is the list box event handler.</span></span> <span data-ttu-id="561cd-132">Quando l'utente fa clic sul nome di una playlist, questo codice recupera gli attributi per la playlist e visualizza tali attributi in una seconda casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="561cd-132">When the user clicks a playlist name, this code retrieves the attributes for that playlist and displays those attributes in a second list box.</span></span>


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



<span data-ttu-id="561cd-133">L'evento SelectedIndexChanged per il controllo ListBox viene chiamato ogni volta che l'utente seleziona un nome della playlist.</span><span class="sxs-lookup"><span data-stu-id="561cd-133">The SelectedIndexChanged event for the ListBox control is called each time the user selects a playlist name.</span></span> <span data-ttu-id="561cd-134">Il gestore eventi seguente riempie una seconda casella di riepilogo con i nomi degli attributi e i valori corrispondenti alla selezione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="561cd-134">The following event handler fills a second list box with the attribute names and values corresponding to the user's selection.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="561cd-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="561cd-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="561cd-136">**Gestione delle playlist**</span><span class="sxs-lookup"><span data-stu-id="561cd-136">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="561cd-137">**Attributi elemento multimediale**</span><span class="sxs-lookup"><span data-stu-id="561cd-137">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="561cd-138">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="561cd-138">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




