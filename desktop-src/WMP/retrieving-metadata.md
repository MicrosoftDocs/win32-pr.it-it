---
title: Recupero dei metadati
description: Recupero dei metadati
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Playlist Windows Media Metafile, recupero di metadati
- playlist, recupero di metadati
- playlist di metafile, recupero di metadati
- Playlist Windows Media Metafile, recupero di metadati
- playlist, recupero di metadati
- playlist di metafile, recupero di metadati
- metadati, recupero
- recupero di metadati
- Media Player di Windows, recupero di metadati
- Media Player di Windows, recupero di metadati
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955610"
---
# <a name="retrieving-metadata"></a><span data-ttu-id="36ad3-113">Recupero dei metadati</span><span class="sxs-lookup"><span data-stu-id="36ad3-113">Retrieving Metadata</span></span>

<span data-ttu-id="36ad3-114">Durante la riproduzione di una visualizzazione o di una clip, lo script può recuperare i metadati, ad esempio il titolo e l'autore, usando i metodi **GetItemInfo** degli oggetti Windows Media Player **media** e **playlist** .</span><span class="sxs-lookup"><span data-stu-id="36ad3-114">While a show or clip is playing, your script can retrieve metadata, such as title and author, by using the **getItemInfo** methods of the Windows Media Player **Media** and **Playlist** objects.</span></span> <span data-ttu-id="36ad3-115">È possibile recuperare i metadati dall'ambito ASX usando i metodi dell'oggetto **playlist** e dall'ambito della voce usando i metodi dell'oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="36ad3-115">You can retrieve metadata from the ASX scope using **Playlist** object methods and from the ENTRY scope using **Media** object methods.</span></span>

<span data-ttu-id="36ad3-116">Ad esempio, per recuperare i valori per AUTHOR, ABSTRACT e PARAM nel file seguente, usare il metodo **GetItemInfo** dell'oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="36ad3-116">For example, to retrieve the values for AUTHOR, ABSTRACT and PARAM in the following file, use the **getItemInfo** method of the **Playlist** object.</span></span> <span data-ttu-id="36ad3-117">Il nome dell'attributo è obbligatorio per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="36ad3-117">The attribute name is required for this method.</span></span> <span data-ttu-id="36ad3-118">I nomi degli attributi possono essere ottenuti specificando il numero di indice per la proprietà **attributeName** .</span><span class="sxs-lookup"><span data-stu-id="36ad3-118">Attribute names can be obtained by providing the index number to the **attributeName** property.</span></span> <span data-ttu-id="36ad3-119">Gli indici disponibili per un oggetto **playlist** possono essere ottenuti usando la proprietà **attributeCount** .</span><span class="sxs-lookup"><span data-stu-id="36ad3-119">The available indexes for a **Playlist** object can be obtained using the **attributeCount** property.</span></span>

## <a name="example-code"></a><span data-ttu-id="36ad3-120">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="36ad3-120">Example Code</span></span>


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



<span data-ttu-id="36ad3-121">Per recuperare i valori dell'oggetto **multimediale** corrente nell'ambito della voce per ref, title, copyright e Param ("Three"), usare la proprietà **CurrentMedia** dell'oggetto **Player** .</span><span class="sxs-lookup"><span data-stu-id="36ad3-121">To retrieve the values of the current **Media** object in the ENTRY scope for REF,TITLE,COPYRIGHT, and PARAM ("three"), use the **currentMedia** property of the **Player** object.</span></span> <span data-ttu-id="36ad3-122">Utilizzare la proprietà **attributeCount** dell'oggetto **supporto** per determinare il numero di attributi disponibili per l'oggetto **supporto** specificato.</span><span class="sxs-lookup"><span data-stu-id="36ad3-122">Use the **attributeCount** property of the **Media** object to determine the number of attributes available for the specified **Media** object.</span></span> <span data-ttu-id="36ad3-123">Usare i numeri di indice con il metodo **getItemInfoByAtom** per recuperare i valori di attributo.</span><span class="sxs-lookup"><span data-stu-id="36ad3-123">Use index numbers with the **getItemInfoByAtom** method to retrieve attribute values.</span></span> <span data-ttu-id="36ad3-124">Usare i numeri di indice con il metodo **GetAttribute** dell'oggetto **multimediale** per determinare i nomi degli attributi disponibili e quindi usare i risultati con il metodo **GetItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="36ad3-124">Use index numbers with the **getAttributeName** method of the **Media** object to determine the names of the available attributes, and then use the results with the **getItemInfo** method.</span></span>

<span data-ttu-id="36ad3-125">Per un esempio dell'uso di Windows Media Player metodi dell'oggetto per recuperare i metadati, vedere [playlist. attributeCount](playlist-attributecount.md).</span><span class="sxs-lookup"><span data-stu-id="36ad3-125">For an example of using Windows Media Player object methods to retrieve metadata, see [Playlist.attributeCount](playlist-attributecount.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="36ad3-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36ad3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36ad3-127">**Creazione di playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="36ad3-127">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="36ad3-128">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="36ad3-128">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="36ad3-129">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="36ad3-129">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




