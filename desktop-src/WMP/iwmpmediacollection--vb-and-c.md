---
title: Interfaccia IWMPMediaCollection (VB e C) (WMP. h)
description: Fornisce metodi che possono essere usati per organizzare un'ampia raccolta di elementi multimediali.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- Interfaccia IWMPMediaCollection (VB e C) Windows Media Player
- Interfaccia IWMPMediaCollection (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424fd45b1fd3d02000a9774ffe75ec87e52dd9c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333750"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a><span data-ttu-id="f5e9b-105">Interfaccia IWMPMediaCollection (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="f5e9b-105">IWMPMediaCollection (VB and C#) interface</span></span>

<span data-ttu-id="f5e9b-106">Fornisce metodi che possono essere usati per organizzare un'ampia raccolta di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-106">Provides methods that can be used to organize a large collection of media items.</span></span>

## <a name="members"></a><span data-ttu-id="f5e9b-107">Membri</span><span class="sxs-lookup"><span data-stu-id="f5e9b-107">Members</span></span>

<span data-ttu-id="f5e9b-108">L'interfaccia **IWMPMediaCollection (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f5e9b-108">The **IWMPMediaCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="f5e9b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f5e9b-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f5e9b-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="f5e9b-110">Methods</span></span>

<span data-ttu-id="f5e9b-111">L'interfaccia **IWMPMediaCollection (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-111">The **IWMPMediaCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="f5e9b-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="f5e9b-112">Method</span></span>                                                                                                                       | <span data-ttu-id="f5e9b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5e9b-113">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5e9b-114">**add**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-114">**add**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | <span data-ttu-id="f5e9b-115">Aggiunge un nuovo elemento multimediale o una playlist alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-115">Adds a new media item or playlist to the library.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f5e9b-116">**getAll**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-116">**getAll**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | <span data-ttu-id="f5e9b-117">Restituisce un'interfaccia **IWMPPlaylist** che corrisponde alla playlist che contiene tutti gli elementi multimediali nella libreria.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-117">Returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span><br/>               |
| [<span data-ttu-id="f5e9b-118">**getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-118">**getAttributeStringCollection**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | <span data-ttu-id="f5e9b-119">Restituisce un'interfaccia **IWMPStringCollection** che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-119">Returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span><br/> |
| [<span data-ttu-id="f5e9b-120">**getByAlbum**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-120">**getByAlbum**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | <span data-ttu-id="f5e9b-121">Restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali dall'album specificato.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-121">Returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span><br/>                                |
| [<span data-ttu-id="f5e9b-122">**getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-122">**getByAttribute**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | <span data-ttu-id="f5e9b-123">Restituisce un'interfaccia **IWMPPlaylist** che corrisponde all'attributo specificato con il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-123">Returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span><br/>                      |
| [<span data-ttu-id="f5e9b-124">**getByAuthor**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-124">**getByAuthor**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | <span data-ttu-id="f5e9b-125">Restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali dall'autore specificato.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-125">Returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span><br/>                             |
| [<span data-ttu-id="f5e9b-126">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-126">**getByGenre**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | <span data-ttu-id="f5e9b-127">Restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali del genere specificato.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-127">Returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span><br/>                                  |
| [<span data-ttu-id="f5e9b-128">**getByName**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-128">**getByName**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | <span data-ttu-id="f5e9b-129">Restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-129">Returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span><br/>                                 |
| [<span data-ttu-id="f5e9b-130">**getMediaAtom**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-130">**getMediaAtom**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | <span data-ttu-id="f5e9b-131">Restituisce l'indice di un attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-131">Returns the index of a specified attribute.</span></span><br/>                                                                                        |
| <span data-ttu-id="f5e9b-132">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-132">**isDeleted**</span></span>                                                                                                                | <span data-ttu-id="f5e9b-133">Non più supportata.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-133">No longer supported.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="f5e9b-134">**rimuovere**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-134">**remove**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | <span data-ttu-id="f5e9b-135">Rimuove l'elemento multimediale specificato dall'insieme di supporti.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-135">Removes the specified media item from the media collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="f5e9b-136">**Eliminata**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-136">**setDeleted**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | <span data-ttu-id="f5e9b-137">Sposta l'elemento multimediale specificato nella cartella elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-137">Moves the specified media item to the deleted items folder.</span></span><br/>                                                                        |



 

<span data-ttu-id="f5e9b-138">Ottenere un'interfaccia **IWMPMediaCollection** usando le proprietà seguenti a cui si accede tramite l'oggetto o l'interfaccia seguente.</span><span class="sxs-lookup"><span data-stu-id="f5e9b-138">Get an **IWMPMediaCollection** interface by using the following properties accessed through the following object or interface.</span></span>



| <span data-ttu-id="f5e9b-139">Oggetto o interfaccia</span><span class="sxs-lookup"><span data-stu-id="f5e9b-139">Object or interface</span></span>                                               | <span data-ttu-id="f5e9b-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f5e9b-140">Property</span></span>                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5e9b-141">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="f5e9b-141">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="f5e9b-142">**mediacollection**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-142">**mediaCollection**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [<span data-ttu-id="f5e9b-143">**IWMPLibrary**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-143">**IWMPLibrary**</span></span>](iwmplibrary--vb-and-c.md)                      | [<span data-ttu-id="f5e9b-144">**mediacollection**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-144">**mediaCollection**</span></span>](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="f5e9b-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5e9b-145">Requirements</span></span>



| <span data-ttu-id="f5e9b-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5e9b-146">Requirement</span></span> | <span data-ttu-id="f5e9b-147">Valore</span><span class="sxs-lookup"><span data-stu-id="f5e9b-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f5e9b-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5e9b-148">Header</span></span><br/> | <dl> <span data-ttu-id="f5e9b-149"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5e9b-149"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5e9b-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5e9b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e9b-151">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-151">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="f5e9b-152">**Interfaccia IWMPMediaCollection2**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-152">**IWMPMediaCollection2 Interface**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f5e9b-153">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-153">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f5e9b-154">**Interfaccia IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f5e9b-154">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





