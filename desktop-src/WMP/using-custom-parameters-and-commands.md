---
title: Uso di parametri e comandi personalizzati
description: Uso di parametri e comandi personalizzati
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Playlist Windows Media Metafile, parametri personalizzati
- playlist, parametri personalizzati
- playlist di metafile, parametri personalizzati
- Playlist Windows Media Metafile, comandi personalizzati
- playlist, comandi personalizzati
- playlist di metafile, comandi personalizzati
- Playlist di Windows Media Metafile, parametri
- playlist, parametri
- playlist di metafile, parametri
- parametri personalizzati
- comandi personalizzati
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59f577fa4f3af71799b163389f85987d8723e045
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856326"
---
# <a name="using-custom-parameters-and-commands"></a><span data-ttu-id="44428-114">Uso di parametri e comandi personalizzati</span><span class="sxs-lookup"><span data-stu-id="44428-114">Using Custom Parameters and Commands</span></span>

<span data-ttu-id="44428-115">È possibile creare parametri personalizzati per passare metadati aggiuntivi in una playlist di metafile usando l'elemento **param** .</span><span class="sxs-lookup"><span data-stu-id="44428-115">You can create custom parameters to pass additional metadata in a metafile playlist by using the **PARAM** element.</span></span> <span data-ttu-id="44428-116">Usare l'attributo **Name** dell'elemento **param** per definire il nome del parametro personalizzato.</span><span class="sxs-lookup"><span data-stu-id="44428-116">Use the **NAME** attribute of the **PARAM** element to define the custom parameter name.</span></span> <span data-ttu-id="44428-117">Utilizzare l'attributo **value** per definire il valore per il parametro personalizzato denominato.</span><span class="sxs-lookup"><span data-stu-id="44428-117">Use the **VALUE** attribute to define the value for the named custom parameter.</span></span>

<span data-ttu-id="44428-118">Recuperare i metadati **param** usando i metodi **GetItemInfo** degli oggetti **media** e **playlist** .</span><span class="sxs-lookup"><span data-stu-id="44428-118">Retrieve **PARAM** metadata by using the **getItemInfo** methods of the **Media** and **Playlist** objects.</span></span> <span data-ttu-id="44428-119">Per un esempio di utilizzo di questi metodi per recuperare i metadati, vedere il metodo [attributeCount](playlist-attributecount.md) dell'oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="44428-119">For an example using these methods to retrieve metadata, see the [attributeCount](playlist-attributecount.md) method of the **Playlist** object.</span></span>

<span data-ttu-id="44428-120">La playlist del metafile di esempio seguente illustra l'uso dell'elemento **param** per definire parametri personalizzati.</span><span class="sxs-lookup"><span data-stu-id="44428-120">The following example metafile playlist shows the use of the **PARAM** element to define custom parameters.</span></span>


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="44428-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44428-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44428-122">**Uso delle playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="44428-122">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




