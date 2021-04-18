---
title: Mediacollection (oggetto)
description: L'oggetto Mediacollection consente di organizzare un'ampia raccolta di elementi multimediali. È possibile eseguire query su di essa per generare automaticamente playlist.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Media Player finestre oggetti mediacollection
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299209"
---
# <a name="mediacollection-object"></a><span data-ttu-id="f0482-105">Mediacollection (oggetto)</span><span class="sxs-lookup"><span data-stu-id="f0482-105">MediaCollection Object</span></span>

<span data-ttu-id="f0482-106">L'oggetto **mediacollection** consente di organizzare un'ampia raccolta di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="f0482-106">The **MediaCollection** object provides a way to organize a large collection of media items.</span></span> <span data-ttu-id="f0482-107">È possibile eseguire query su di essa per generare automaticamente playlist.</span><span class="sxs-lookup"><span data-stu-id="f0482-107">It can be queried to generate playlists automatically.</span></span>

<span data-ttu-id="f0482-108">L'oggetto **mediacollection** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="f0482-108">The **MediaCollection** object supports the following methods.</span></span>



| <span data-ttu-id="f0482-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="f0482-109">Method</span></span>                                                                           | <span data-ttu-id="f0482-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0482-110">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0482-111">add</span><span class="sxs-lookup"><span data-stu-id="f0482-111">add</span></span>](mediacollection-add.md)                                                   | <span data-ttu-id="f0482-112">Aggiunge un nuovo elemento multimediale o una playlist alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="f0482-112">Adds a new media item or playlist to the library.</span></span>                                                                                                              |
| [<span data-ttu-id="f0482-113">createQuery</span><span class="sxs-lookup"><span data-stu-id="f0482-113">createQuery</span></span>](mediacollection-createquery.md)                                   | <span data-ttu-id="f0482-114">Crea un nuovo oggetto [query](query-object.md) .</span><span class="sxs-lookup"><span data-stu-id="f0482-114">Creates a new [Query](query-object.md) object.</span></span>                                                                                                                |
| [<span data-ttu-id="f0482-115">getAll</span><span class="sxs-lookup"><span data-stu-id="f0482-115">getAll</span></span>](mediacollection-getall.md)                                             | <span data-ttu-id="f0482-116">Recupera un oggetto [playlist](playlist-object.md) contenente tutti gli elementi multimediali nella libreria.</span><span class="sxs-lookup"><span data-stu-id="f0482-116">Retrieves a [Playlist](playlist-object.md) object containing all media items in the library.</span></span>                                                                  |
| [<span data-ttu-id="f0482-117">getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="f0482-117">getAttributeStringCollection</span></span>](mediacollection-getattributestringcollection.md) | <span data-ttu-id="f0482-118">Recupera un oggetto [StringCollection](stringcollection-object.md) che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="f0482-118">Retrieves a [StringCollection](stringcollection-object.md) object representing the set of all values for a specified attribute within a specified media type.</span></span> |
| [<span data-ttu-id="f0482-119">getByAlbum</span><span class="sxs-lookup"><span data-stu-id="f0482-119">getByAlbum</span></span>](mediacollection-getbyalbum.md)                                     | <span data-ttu-id="f0482-120">Recupera un oggetto [playlist](playlist-object.md) contenente elementi multimediali dall'album specificato.</span><span class="sxs-lookup"><span data-stu-id="f0482-120">Retrieves a [Playlist](playlist-object.md) object containing media items from the specified album.</span></span>                                                            |
| [<span data-ttu-id="f0482-121">getByAttribute</span><span class="sxs-lookup"><span data-stu-id="f0482-121">getByAttribute</span></span>](mediacollection-getbyattribute.md)                             | <span data-ttu-id="f0482-122">Recupera un oggetto [playlist](playlist-object.md) contenente gli elementi multimediali con l'attributo specificato con il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="f0482-122">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified attribute having the specified value.</span></span>                             |
| [<span data-ttu-id="f0482-123">getByAttributeAndMediaType</span><span class="sxs-lookup"><span data-stu-id="f0482-123">getByAttributeAndMediaType</span></span>](mediacollection-getbyattributeandmediatype.md)     | <span data-ttu-id="f0482-124">Recupera un oggetto [playlist](playlist-object.md) contenente oggetti [multimediali](media-object.md) con l'attributo e il tipo di supporto specificati.</span><span class="sxs-lookup"><span data-stu-id="f0482-124">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects having the specified attribute and media type.</span></span>                 |
| [<span data-ttu-id="f0482-125">getByAuthor</span><span class="sxs-lookup"><span data-stu-id="f0482-125">getByAuthor</span></span>](mediacollection-getbyauthor.md)                                   | <span data-ttu-id="f0482-126">Recupera un oggetto [playlist](playlist-object.md) contenente elementi multimediali dall'autore specificato.</span><span class="sxs-lookup"><span data-stu-id="f0482-126">Retrieves a [Playlist](playlist-object.md) object containing media items by the specified author.</span></span>                                                             |
| [<span data-ttu-id="f0482-127">getByGenre</span><span class="sxs-lookup"><span data-stu-id="f0482-127">getByGenre</span></span>](mediacollection-getbygenre.md)                                     | <span data-ttu-id="f0482-128">Recupera un oggetto [playlist](playlist-object.md) contenente elementi multimediali con il genere specificato.</span><span class="sxs-lookup"><span data-stu-id="f0482-128">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified genre.</span></span>                                                            |
| [<span data-ttu-id="f0482-129">getByName</span><span class="sxs-lookup"><span data-stu-id="f0482-129">getByName</span></span>](mediacollection-getbyname.md)                                       | <span data-ttu-id="f0482-130">Recupera un oggetto [playlist](playlist-object.md) contenente elementi multimediali con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="f0482-130">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified name.</span></span>                                                             |
| [<span data-ttu-id="f0482-131">getMediaAtom</span><span class="sxs-lookup"><span data-stu-id="f0482-131">getMediaAtom</span></span>](mediacollection-getmediaatom.md)                                 | <span data-ttu-id="f0482-132">Recupera l'indice in corrispondenza del quale si trova una proprietà specificata nel set di proprietà disponibili.</span><span class="sxs-lookup"><span data-stu-id="f0482-132">Retrieves the index at which a specified property resides within the set of available properties.</span></span>                                                              |
| [<span data-ttu-id="f0482-133">getPlaylistByQuery</span><span class="sxs-lookup"><span data-stu-id="f0482-133">getPlaylistByQuery</span></span>](mediacollection-getplaylistbyquery.md)                     | <span data-ttu-id="f0482-134">Recupera un oggetto [playlist](playlist-object.md) contenente oggetti [multimediali](media-object.md) che corrispondono alle condizioni della query.</span><span class="sxs-lookup"><span data-stu-id="f0482-134">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects that match the query conditions.</span></span>                               |
| [<span data-ttu-id="f0482-135">getStringCollectionByQuery</span><span class="sxs-lookup"><span data-stu-id="f0482-135">getStringCollectionByQuery</span></span>](mediacollection-getstringcollectionbyquery.md)     | <span data-ttu-id="f0482-136">Recupera un oggetto [StringCollection](stringcollection-object.md) contenente stringhe corrispondenti alle condizioni della query.</span><span class="sxs-lookup"><span data-stu-id="f0482-136">Retrieves a [StringCollection](stringcollection-object.md) object containing strings that match the query conditions.</span></span>                                         |
| [<span data-ttu-id="f0482-137">isDeleted</span><span class="sxs-lookup"><span data-stu-id="f0482-137">isDeleted</span></span>](mediacollection-isdeleted.md)                                       | <span data-ttu-id="f0482-138">Recupera un valore che indica se l'elemento multimediale specificato si trova nella cartella elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="f0482-138">Retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>                                                                  |
| [<span data-ttu-id="f0482-139">remove</span><span class="sxs-lookup"><span data-stu-id="f0482-139">remove</span></span>](mediacollection-remove.md)                                             | <span data-ttu-id="f0482-140">Rimuove un elemento dall'insieme di supporti.</span><span class="sxs-lookup"><span data-stu-id="f0482-140">Removes an item from the media collection.</span></span>                                                                                                                     |
| [<span data-ttu-id="f0482-141">Eliminata</span><span class="sxs-lookup"><span data-stu-id="f0482-141">setDeleted</span></span>](mediacollection-setdeleted.md)                                     | <span data-ttu-id="f0482-142">Sposta l'elemento multimediale specificato nella cartella elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="f0482-142">Moves the specified media item to the deleted items folder.</span></span>                                                                                                    |



 

<span data-ttu-id="f0482-143">È possibile accedere all'oggetto **mediacollection** tramite la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="f0482-143">The **MediaCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="f0482-144">Oggetto</span><span class="sxs-lookup"><span data-stu-id="f0482-144">Object</span></span>                      | <span data-ttu-id="f0482-145">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0482-145">Property</span></span>                                      |
|-----------------------------|-----------------------------------------------|
| [<span data-ttu-id="f0482-146">Player</span><span class="sxs-lookup"><span data-stu-id="f0482-146">Player</span></span>](player-object.md) | [<span data-ttu-id="f0482-147">mediacollection</span><span class="sxs-lookup"><span data-stu-id="f0482-147">mediaCollection</span></span>](player-mediacollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="f0482-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0482-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0482-149">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="f0482-149">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




