---
title: Interfaccia IWMPPlaylist (VB e C) (Wmp.h)
description: Fornisce proprietà e metodi per organizzare, gestire e modificare gli elementi multimediali in una playlist. L'interfaccia IWMPPlaylist espone le proprietà seguenti.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- Interfaccia IWMPPlaylist (VB e C) Windows Media Player
- Interfaccia IWMPPlaylist (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52090588905e2fd79b218abe939f78c1e38fc79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329995"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a><span data-ttu-id="57fcf-105">Interfaccia IWMPPlaylist (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="57fcf-105">IWMPPlaylist (VB and C#) interface</span></span>

<span data-ttu-id="57fcf-106">Fornisce proprietà e metodi per organizzare, gestire e modificare gli elementi multimediali in una playlist.</span><span class="sxs-lookup"><span data-stu-id="57fcf-106">Provides properties and methods to organize, manage, and manipulate media items in a playlist.</span></span>

<span data-ttu-id="57fcf-107">L'interfaccia **IWMPPlaylist** espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="57fcf-107">The **IWMPPlaylist** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="57fcf-108">Membri</span><span class="sxs-lookup"><span data-stu-id="57fcf-108">Members</span></span>

<span data-ttu-id="57fcf-109">L'interfaccia **IWMPPlaylist (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="57fcf-109">The **IWMPPlaylist (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="57fcf-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="57fcf-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="57fcf-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57fcf-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="57fcf-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="57fcf-112">Methods</span></span>

<span data-ttu-id="57fcf-113">L'interfaccia **IWMPPlaylist (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="57fcf-113">The **IWMPPlaylist (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="57fcf-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="57fcf-114">Method</span></span>                                                                       | <span data-ttu-id="57fcf-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57fcf-115">Description</span></span>                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="57fcf-116">**appendItem**</span><span class="sxs-lookup"><span data-stu-id="57fcf-116">**appendItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | <span data-ttu-id="57fcf-117">Aggiunge un elemento multimediale alla fine della playlist.</span><span class="sxs-lookup"><span data-stu-id="57fcf-117">Adds a media item to the end of the playlist.</span></span><br/>                |
| [<span data-ttu-id="57fcf-118">**deselezionare**</span><span class="sxs-lookup"><span data-stu-id="57fcf-118">**clear**</span></span>](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | <span data-ttu-id="57fcf-119">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="57fcf-119">Reserved for future use.</span></span><br/>                                     |
| [<span data-ttu-id="57fcf-120">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="57fcf-120">**getItemInfo**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | <span data-ttu-id="57fcf-121">Restituisce il valore di un attributo della playlist specificato in base al nome.</span><span class="sxs-lookup"><span data-stu-id="57fcf-121">Returns the value of a playlist attribute specified by name.</span></span><br/> |
| [<span data-ttu-id="57fcf-122">**insertItem**</span><span class="sxs-lookup"><span data-stu-id="57fcf-122">**insertItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | <span data-ttu-id="57fcf-123">Inserisce un elemento multimediale in una posizione specificata in una playlist.</span><span class="sxs-lookup"><span data-stu-id="57fcf-123">Inserts a media item at a specified location in a playlist.</span></span><br/>  |
| [<span data-ttu-id="57fcf-124">**moveItem**</span><span class="sxs-lookup"><span data-stu-id="57fcf-124">**moveItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | <span data-ttu-id="57fcf-125">Modifica la posizione di un elemento multimediale nella playlist.</span><span class="sxs-lookup"><span data-stu-id="57fcf-125">Changes the location of a media item in the playlist.</span></span><br/>        |
| [<span data-ttu-id="57fcf-126">**removeItem**</span><span class="sxs-lookup"><span data-stu-id="57fcf-126">**removeItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | <span data-ttu-id="57fcf-127">Rimuove l'elemento multimediale specificato dalla playlist.</span><span class="sxs-lookup"><span data-stu-id="57fcf-127">Removes the specified media item from the playlist.</span></span><br/>          |
| [<span data-ttu-id="57fcf-128">**setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="57fcf-128">**setItemInfo**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | <span data-ttu-id="57fcf-129">Imposta il valore di un attributo della playlist.</span><span class="sxs-lookup"><span data-stu-id="57fcf-129">Sets the value of a playlist attribute.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="57fcf-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57fcf-130">Properties</span></span>

<span data-ttu-id="57fcf-131">L'interfaccia **IWMPPlaylist (VB e C#)** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="57fcf-131">The **IWMPPlaylist (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="57fcf-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57fcf-132">Property</span></span>                                                                                      | <span data-ttu-id="57fcf-133">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="57fcf-133">Access type</span></span>           | <span data-ttu-id="57fcf-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57fcf-134">Description</span></span>                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57fcf-135">**attributeCount**</span><span class="sxs-lookup"><span data-stu-id="57fcf-135">**attributeCount**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | <span data-ttu-id="57fcf-136">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="57fcf-136">Read-only</span></span><br/>  | <span data-ttu-id="57fcf-137">Ottiene il numero di attributi associati a una playlist.</span><span class="sxs-lookup"><span data-stu-id="57fcf-137">Gets the number of attributes associated with a playlist.</span></span><br/>                                                                                |
| [<span data-ttu-id="57fcf-138">**attributeName**</span><span class="sxs-lookup"><span data-stu-id="57fcf-138">**attributeName**</span></span>](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | <span data-ttu-id="57fcf-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="57fcf-139">Read-only</span></span><br/>  | <span data-ttu-id="57fcf-140">Ottiene il nome di un attributo della playlist specificato da un indice.</span><span class="sxs-lookup"><span data-stu-id="57fcf-140">Gets the name of a playlist attribute specified by an index.</span></span> <span data-ttu-id="57fcf-141">In C# si tratta del \_ metodo Get AttributeName.</span><span class="sxs-lookup"><span data-stu-id="57fcf-141">In C# this is the get\_attributeName method.</span></span><br/>                               |
| [<span data-ttu-id="57fcf-142">**count**</span><span class="sxs-lookup"><span data-stu-id="57fcf-142">**count**</span></span>](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | <span data-ttu-id="57fcf-143">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="57fcf-143">Read-only</span></span><br/>  | <span data-ttu-id="57fcf-144">Ottiene il numero di elementi multimediali in una playlist.</span><span class="sxs-lookup"><span data-stu-id="57fcf-144">Gets the number of media items in a playlist.</span></span><br/>                                                                                            |
| [<span data-ttu-id="57fcf-145">**Identico**</span><span class="sxs-lookup"><span data-stu-id="57fcf-145">**isIdentical**</span></span>](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | <span data-ttu-id="57fcf-146">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="57fcf-146">Read-only</span></span><br/>  | <span data-ttu-id="57fcf-147">Ottiene un valore che indica se la playlist specificata è identica alla playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="57fcf-147">Gets a value indicating whether the specified playlist is identical to the current playlist.</span></span> <span data-ttu-id="57fcf-148">In C# il metodo Get è \_ identico.</span><span class="sxs-lookup"><span data-stu-id="57fcf-148">In C# this is the get\_isIdentical method.</span></span><br/> |
| [<span data-ttu-id="57fcf-149">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="57fcf-149">**Item**</span></span>](iwmpplaylist-item--vb-and-c.md)<br/>                                        | <span data-ttu-id="57fcf-150">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="57fcf-150">Read-only</span></span><br/>  | <span data-ttu-id="57fcf-151">Ottiene un'interfaccia per l'elemento multimediale in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="57fcf-151">Gets an interface to the media item at the specified index.</span></span> <span data-ttu-id="57fcf-152">In C# si tratta del \_ metodo Get Item.</span><span class="sxs-lookup"><span data-stu-id="57fcf-152">In C# this is the get\_Item method.</span></span><br/>                                         |
| [<span data-ttu-id="57fcf-153">**nome**</span><span class="sxs-lookup"><span data-stu-id="57fcf-153">**name**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | <span data-ttu-id="57fcf-154">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="57fcf-154">Read/write</span></span><br/> | <span data-ttu-id="57fcf-155">Ottiene o imposta il nome della playlist.</span><span class="sxs-lookup"><span data-stu-id="57fcf-155">Gets or sets the name of the playlist.</span></span><br/>                                                                                                   |



 

<span data-ttu-id="57fcf-156">Ottenere un'interfaccia **IWMPPlaylist** usando le proprietà o i metodi seguenti a cui si accede tramite l'oggetto o l'interfaccia seguente.</span><span class="sxs-lookup"><span data-stu-id="57fcf-156">Get an **IWMPPlaylist** interface by using the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="57fcf-157">Oggetto o interfaccia</span><span class="sxs-lookup"><span data-stu-id="57fcf-157">Object or interface</span></span>                                                | <span data-ttu-id="57fcf-158">Proprietà o metodo</span><span class="sxs-lookup"><span data-stu-id="57fcf-158">Property or method</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57fcf-159">**IWMPCdrom**</span><span class="sxs-lookup"><span data-stu-id="57fcf-159">**IWMPCdrom**</span></span>](iwmpcdrom--vb-and-c.md)                           | [<span data-ttu-id="57fcf-160">**Playlist**</span><span class="sxs-lookup"><span data-stu-id="57fcf-160">**Playlist**</span></span>](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="57fcf-161">**IWMPMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="57fcf-161">**IWMPMediaCollection**</span></span>](iwmpmediacollection--vb-and-c.md)       | <span data-ttu-id="57fcf-162">[**GetAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**GetByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)</span><span class="sxs-lookup"><span data-stu-id="57fcf-162">[**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)</span></span> |
| [<span data-ttu-id="57fcf-163">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="57fcf-163">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md)  | <span data-ttu-id="57fcf-164">[**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **nuova playlist**](axwmplib-axwindowsmediaplayer-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="57fcf-164">[**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [**newPlaylist**](axwmplib-axwindowsmediaplayer-newplaylist.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="57fcf-165">**IWMPPlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="57fcf-165">**IWMPPlaylistArray**</span></span>](iwmpplaylistarray--vb-and-c.md)           | [<span data-ttu-id="57fcf-166">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="57fcf-166">**Item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="57fcf-167">**IWMPPlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="57fcf-167">**IWMPPlaylistCollection**</span></span>](iwmpplaylistcollection--vb-and-c.md) | [<span data-ttu-id="57fcf-168">**Nuova playlist**</span><span class="sxs-lookup"><span data-stu-id="57fcf-168">**newPlaylist**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="57fcf-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57fcf-169">Requirements</span></span>



| <span data-ttu-id="57fcf-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="57fcf-170">Requirement</span></span> | <span data-ttu-id="57fcf-171">Valore</span><span class="sxs-lookup"><span data-stu-id="57fcf-171">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57fcf-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57fcf-172">Header</span></span><br/> | <dl> <span data-ttu-id="57fcf-173"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="57fcf-173"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57fcf-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57fcf-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57fcf-175">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="57fcf-175">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





