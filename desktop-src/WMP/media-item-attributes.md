---
title: Attributi elemento multimediale
description: Attributi elemento multimediale
ms.assetid: d43addec-e06c-4ef3-9012-3ecf589b105c
keywords:
- Windows Media Player, libreria
- Modello a oggetti di Windows Media Player, libreria
- modello a oggetti, libreria
- Windows Media Player Mobile, libreria per il modello a oggetti
- Controllo ActiveX di Windows Media Player, libreria per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Media Player di Windows, attributi per elementi multimediali
- Modello a oggetti di Windows Media Player, attributi per elementi multimediali
- modello a oggetti, attributi per elementi multimediali
- Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX di Windows Media Player, attributi per elementi multimediali
- Controllo ActiveX Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX, attributi per elementi multimediali
- Windows Media Player Library, attributi per elementi multimediali
- libreria, attributi per elementi multimediali
- attributi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac8595cc07504c9cd3e195431513a1f8565e87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044680"
---
# <a name="media-item-attributes"></a><span data-ttu-id="70443-120">Attributi elemento multimediale</span><span class="sxs-lookup"><span data-stu-id="70443-120">Media Item Attributes</span></span>

<span data-ttu-id="70443-121">Quando si esamina la libreria in Windows Media Player, in genere viene visualizzata una grande quantità di informazioni su un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="70443-121">When you look at the library in Windows Media Player, you typically see a great deal of information about a media item.</span></span> <span data-ttu-id="70443-122">Oltre al nome di una traccia audio, ad esempio, è probabile che venga visualizzato il nome dell'album in cui si trova la traccia, i nomi dell'artista e del compositore, il genere di musica e così via.</span><span class="sxs-lookup"><span data-stu-id="70443-122">In addition to the name of an audio track, for example, you will likely see the name of the album the track is on, the names of the artist and composer, the genre of the music, and so on.</span></span>

<span data-ttu-id="70443-123">Nel modello a oggetti di Windows Media Player questi elementi di metadati sono denominati attributi.</span><span class="sxs-lookup"><span data-stu-id="70443-123">In the Windows Media Player object model, these metadata items are called attributes.</span></span> <span data-ttu-id="70443-124">Il modello a oggetti include proprietà e metodi che è possibile usare per eseguire query su elementi multimediali e playlist per gli attributi.</span><span class="sxs-lookup"><span data-stu-id="70443-124">The object model includes properties and methods you can use to query media items and playlists for attributes.</span></span> <span data-ttu-id="70443-125">È quindi possibile visualizzare i valori degli attributi nell'interfaccia utente oppure il codice può eseguire azioni in base al valore di un attributo.</span><span class="sxs-lookup"><span data-stu-id="70443-125">You can then display attribute values in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="70443-126">Negli argomenti seguenti viene descritto l'utilizzo degli attributi degli elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="70443-126">The following topics describe working with media item attributes.</span></span>



| <span data-ttu-id="70443-127">Argomento</span><span class="sxs-lookup"><span data-stu-id="70443-127">Topic</span></span>                                                                                      | <span data-ttu-id="70443-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70443-128">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70443-129">Informazioni sulle origini degli attributi</span><span class="sxs-lookup"><span data-stu-id="70443-129">Understanding Attribute Sources</span></span>](understanding-attribute-sources.md)                     | <span data-ttu-id="70443-130">Descrive il modo in cui l'origine di un elemento multimediale influiscono sugli attributi che possono essere associati.</span><span class="sxs-lookup"><span data-stu-id="70443-130">Describes how the source of a media item affects the attributes that may be associated with it.</span></span> |
| [<span data-ttu-id="70443-131">Lettura di valori di attributo</span><span class="sxs-lookup"><span data-stu-id="70443-131">Reading Attribute Values</span></span>](reading-attribute-values.md)                                   | <span data-ttu-id="70443-132">Mostra i metodi per recuperare il valore di un attributo.</span><span class="sxs-lookup"><span data-stu-id="70443-132">Shows the methods for retrieving the value of an attribute.</span></span>                                     |
| [<span data-ttu-id="70443-133">Attributi con più valori</span><span class="sxs-lookup"><span data-stu-id="70443-133">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md)                     | <span data-ttu-id="70443-134">Mostra i metodi per recuperare il valore di un attributo multivalore.</span><span class="sxs-lookup"><span data-stu-id="70443-134">Shows the methods for retrieving the value of a multi-valued attribute.</span></span>                         |
| [<span data-ttu-id="70443-135">Lettura di valori di attributo da un CD o DVD</span><span class="sxs-lookup"><span data-stu-id="70443-135">Reading Attribute Values from a CD or DVD</span></span>](reading-attribute-values-from-a-cd-or-dvd.md) | <span data-ttu-id="70443-136">Fornisce un'applicazione di esempio che legge tutti gli attributi di un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="70443-136">Provides a sample application that reads all of the attributes of a media item.</span></span>                 |
| [<span data-ttu-id="70443-137">Modifica dei valori di attributo</span><span class="sxs-lookup"><span data-stu-id="70443-137">Changing Attribute Values</span></span>](changing-attribute-values.md)                                 | <span data-ttu-id="70443-138">Mostra il metodo per modificare il valore di un attributo.</span><span class="sxs-lookup"><span data-stu-id="70443-138">Shows the method for changing the value of an attribute.</span></span>                                        |
| [<span data-ttu-id="70443-139">Valori di attributo per il contenuto TV</span><span class="sxs-lookup"><span data-stu-id="70443-139">Attribute Values for TV Content</span></span>](attribute-values-for-tv-content.md)                     | <span data-ttu-id="70443-140">Mostra come specificare gli attributi per il contenuto video digitale che contiene programmi TV.</span><span class="sxs-lookup"><span data-stu-id="70443-140">Shows how to specify attributes for digital video content that contains TV shows.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="70443-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70443-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70443-142">**Attributi della playlist**</span><span class="sxs-lookup"><span data-stu-id="70443-142">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> <dt>

[<span data-ttu-id="70443-143">**Utilizzo della libreria**</span><span class="sxs-lookup"><span data-stu-id="70443-143">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




