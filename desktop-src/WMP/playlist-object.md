---
title: Oggetto playlist
description: L'oggetto playlist fornisce un modo per organizzare gli elementi multimediali in un elenco per semplificare la manipolazione usando le proprietà e i metodi seguenti.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Finestre oggetto playlist Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045514"
---
# <a name="playlist-object"></a><span data-ttu-id="b4c34-104">Oggetto playlist</span><span class="sxs-lookup"><span data-stu-id="b4c34-104">Playlist Object</span></span>

<span data-ttu-id="b4c34-105">L'oggetto **playlist** fornisce un modo per organizzare gli elementi multimediali in un elenco per semplificare la manipolazione usando le proprietà e i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b4c34-105">The **Playlist** object provides a way to organize media items in a list for easy manipulation by using the following properties and methods.</span></span>

<span data-ttu-id="b4c34-106">L'oggetto **playlist** supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="b4c34-106">The **Playlist** object supports the following properties.</span></span>



| <span data-ttu-id="b4c34-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4c34-107">Property</span></span>                                      | <span data-ttu-id="b4c34-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4c34-108">Description</span></span>                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="b4c34-109">attributeCount</span><span class="sxs-lookup"><span data-stu-id="b4c34-109">attributeCount</span></span>](playlist-attributecount.md) | <span data-ttu-id="b4c34-110">Recupera il numero di attributi associati alla playlist.</span><span class="sxs-lookup"><span data-stu-id="b4c34-110">Retrieves the number of attributes associated with the playlist.</span></span> |
| [<span data-ttu-id="b4c34-111">attributeName</span><span class="sxs-lookup"><span data-stu-id="b4c34-111">attributeName</span></span>](playlist-attributename.md)   | <span data-ttu-id="b4c34-112">Recupera il nome di un attributo specificato da un indice.</span><span class="sxs-lookup"><span data-stu-id="b4c34-112">Retrieves the name of an attribute specified by an index.</span></span>        |
| [<span data-ttu-id="b4c34-113">count</span><span class="sxs-lookup"><span data-stu-id="b4c34-113">count</span></span>](playlist-count.md)                   | <span data-ttu-id="b4c34-114">Recupera il numero di elementi nella playlist.</span><span class="sxs-lookup"><span data-stu-id="b4c34-114">Retrieves the number of items in the playlist.</span></span>                   |
| [<span data-ttu-id="b4c34-115">nome</span><span class="sxs-lookup"><span data-stu-id="b4c34-115">name</span></span>](playlist-name.md)                     | <span data-ttu-id="b4c34-116">Specifica o Recupera il nome della playlist.</span><span class="sxs-lookup"><span data-stu-id="b4c34-116">Specifies or retrieves the name of the playlist.</span></span>                 |



 

<span data-ttu-id="b4c34-117">L'oggetto **playlist** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b4c34-117">The **Playlist** object supports the following methods.</span></span>



| <span data-ttu-id="b4c34-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="b4c34-118">Method</span></span>                                  | <span data-ttu-id="b4c34-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4c34-119">Description</span></span>                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4c34-120">appendItem</span><span class="sxs-lookup"><span data-stu-id="b4c34-120">appendItem</span></span>](playlist-appenditem.md)   | <span data-ttu-id="b4c34-121">Aggiunge un elemento multimediale alla fine della playlist.</span><span class="sxs-lookup"><span data-stu-id="b4c34-121">Adds a media item to the end of the playlist.</span></span>                                                          |
| <span data-ttu-id="b4c34-122">**deselezionare**</span><span class="sxs-lookup"><span data-stu-id="b4c34-122">**clear**</span></span>                               | <span data-ttu-id="b4c34-123">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="b4c34-123">Reserved for future use.</span></span>                                                                               |
| [<span data-ttu-id="b4c34-124">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="b4c34-124">getItemInfo</span></span>](playlist-getiteminfo.md) | <span data-ttu-id="b4c34-125">Recupera il valore di un attributo della playlist.</span><span class="sxs-lookup"><span data-stu-id="b4c34-125">Retrieves the value of a playlist attribute.</span></span>                                                           |
| [<span data-ttu-id="b4c34-126">insertItem</span><span class="sxs-lookup"><span data-stu-id="b4c34-126">insertItem</span></span>](playlist-insertitem.md)   | <span data-ttu-id="b4c34-127">Inserisce un elemento multimediale nella playlist nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b4c34-127">Inserts a media item into the playlist at the specified location.</span></span>                                      |
| [<span data-ttu-id="b4c34-128">Identico</span><span class="sxs-lookup"><span data-stu-id="b4c34-128">isIdentical</span></span>](playlist-isidentical.md) | <span data-ttu-id="b4c34-129">Recupera un valore che indica se l'oggetto **playlist** fornito è identico a quello corrente.</span><span class="sxs-lookup"><span data-stu-id="b4c34-129">Retrieves a value indicating whether the supplied **Playlist** object is identical to the current one.</span></span> |
| [<span data-ttu-id="b4c34-130">item</span><span class="sxs-lookup"><span data-stu-id="b4c34-130">item</span></span>](playlist-item.md)               | <span data-ttu-id="b4c34-131">Recupera l'elemento multimediale in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="b4c34-131">Retrieves the media item at the specified index.</span></span>                                                       |
| [<span data-ttu-id="b4c34-132">moveItem</span><span class="sxs-lookup"><span data-stu-id="b4c34-132">moveItem</span></span>](playlist-moveitem.md)       | <span data-ttu-id="b4c34-133">Modifica la posizione di un elemento nella playlist.</span><span class="sxs-lookup"><span data-stu-id="b4c34-133">Changes the location of an item in the playlist.</span></span>                                                       |
| [<span data-ttu-id="b4c34-134">removeItem</span><span class="sxs-lookup"><span data-stu-id="b4c34-134">removeItem</span></span>](playlist-removeitem.md)   | <span data-ttu-id="b4c34-135">Rimuove l'elemento specificato dalla playlist.</span><span class="sxs-lookup"><span data-stu-id="b4c34-135">Removes the specified item from the playlist.</span></span>                                                          |
| [<span data-ttu-id="b4c34-136">setItemInfo</span><span class="sxs-lookup"><span data-stu-id="b4c34-136">setItemInfo</span></span>](playlist-setiteminfo.md) | <span data-ttu-id="b4c34-137">Specifica il valore di un attributo della playlist.</span><span class="sxs-lookup"><span data-stu-id="b4c34-137">Specifies the value of a playlist attribute.</span></span>                                                           |



 

<span data-ttu-id="b4c34-138">È possibile accedere all'oggetto **playlist** tramite le proprietà e i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b4c34-138">The **Playlist** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="b4c34-139">Oggetto</span><span class="sxs-lookup"><span data-stu-id="b4c34-139">Object</span></span>                                              | <span data-ttu-id="b4c34-140">Proprietà o metodo</span><span class="sxs-lookup"><span data-stu-id="b4c34-140">Property or method</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4c34-141">Cdrom</span><span class="sxs-lookup"><span data-stu-id="b4c34-141">Cdrom</span></span>](cdrom-object.md)                           | [<span data-ttu-id="b4c34-142">playlist</span><span class="sxs-lookup"><span data-stu-id="b4c34-142">playlist</span></span>](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="b4c34-143">Mediacollection</span><span class="sxs-lookup"><span data-stu-id="b4c34-143">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="b4c34-144">[GetAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [GetByName](mediacollection-getbyname.md)</span><span class="sxs-lookup"><span data-stu-id="b4c34-144">[getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md)</span></span> |
| [<span data-ttu-id="b4c34-145">Player</span><span class="sxs-lookup"><span data-stu-id="b4c34-145">Player</span></span>](player-object.md)                         | <span data-ttu-id="b4c34-146">[currentPlaylist](player-currentplaylist.md), [nuova playlist](player-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="b4c34-146">[currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="b4c34-147">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="b4c34-147">PlaylistArray</span></span>](playlistarray-object.md)           | [<span data-ttu-id="b4c34-148">item</span><span class="sxs-lookup"><span data-stu-id="b4c34-148">item</span></span>](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="b4c34-149">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="b4c34-149">PlaylistCollection</span></span>](playlistcollection-object.md) | [<span data-ttu-id="b4c34-150">Nuova playlist</span><span class="sxs-lookup"><span data-stu-id="b4c34-150">newPlaylist</span></span>](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

<span data-ttu-id="b4c34-151">Poiché si tratta del mezzo più comune di accesso, *Player*. **currentPlaylist** viene usato a scopo illustrativo nelle sezioni della sintassi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="b4c34-151">Because it is the most common means of access, *player*.**currentPlaylist** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4c34-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4c34-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c34-153">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="b4c34-153">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




