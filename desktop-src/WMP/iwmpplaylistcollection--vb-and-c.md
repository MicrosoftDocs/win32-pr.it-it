---
title: Interfaccia IWMPPlaylistCollection (VB e C) (WMP. h)
description: Fornisce metodi per la modifica delle interfacce IWMPPlaylist e IWMPPlaylistArray in una raccolta.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- Interfaccia IWMPPlaylistCollection (VB e C) Windows Media Player
- Interfaccia IWMPPlaylistCollection (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc97f9e98838fedc3bd5441d6bfda2da5319dd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324989"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a><span data-ttu-id="32a72-105">Interfaccia IWMPPlaylistCollection (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="32a72-105">IWMPPlaylistCollection (VB and C#) interface</span></span>

<span data-ttu-id="32a72-106">Fornisce metodi per la modifica delle interfacce **IWMPPlaylist** e **IWMPPlaylistArray** in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="32a72-106">Provides methods for manipulating **IWMPPlaylist** and **IWMPPlaylistArray** interfaces in a collection.</span></span>

## <a name="members"></a><span data-ttu-id="32a72-107">Membri</span><span class="sxs-lookup"><span data-stu-id="32a72-107">Members</span></span>

<span data-ttu-id="32a72-108">L'interfaccia **IWMPPlaylistCollection (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="32a72-108">The **IWMPPlaylistCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="32a72-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="32a72-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="32a72-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="32a72-110">Methods</span></span>

<span data-ttu-id="32a72-111">L'interfaccia **IWMPPlaylistCollection (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="32a72-111">The **IWMPPlaylistCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="32a72-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="32a72-112">Method</span></span>                                                                                                 | <span data-ttu-id="32a72-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32a72-113">Description</span></span>                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32a72-114">**getAll**</span><span class="sxs-lookup"><span data-stu-id="32a72-114">**getAll**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | <span data-ttu-id="32a72-115">Restituisce un'interfaccia **IWMPPlaylistArray** che consente di accedere a tutte le playlist nella libreria.</span><span class="sxs-lookup"><span data-stu-id="32a72-115">Returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span><br/>             |
| [<span data-ttu-id="32a72-116">**getByName**</span><span class="sxs-lookup"><span data-stu-id="32a72-116">**getByName**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | <span data-ttu-id="32a72-117">Restituisce un'interfaccia **IWMPPlaylistArray** che consente di accedere alle playlist con il nome specificato, se presenti.</span><span class="sxs-lookup"><span data-stu-id="32a72-117">Returns an **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span><br/> |
| [<span data-ttu-id="32a72-118">**importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="32a72-118">**importPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | <span data-ttu-id="32a72-119">Aggiunge una playlist statica alla libreria.</span><span class="sxs-lookup"><span data-stu-id="32a72-119">Adds a static playlist to the library.</span></span><br/>                                                                              |
| [<span data-ttu-id="32a72-120">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="32a72-120">**isDeleted**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | <span data-ttu-id="32a72-121">Restituisce un valore che indica se la playlist specificata si trova nella cartella elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="32a72-121">Returns a value indicating whether the specified playlist is in the deleted items folder.</span></span><br/>                           |
| [<span data-ttu-id="32a72-122">**Nuova playlist**</span><span class="sxs-lookup"><span data-stu-id="32a72-122">**newPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | <span data-ttu-id="32a72-123">Restituisce un'interfaccia **IWMPPlaylist** per una nuova playlist vuota nella libreria.</span><span class="sxs-lookup"><span data-stu-id="32a72-123">Returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span><br/>                                     |
| [<span data-ttu-id="32a72-124">**rimuovere**</span><span class="sxs-lookup"><span data-stu-id="32a72-124">**remove**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | <span data-ttu-id="32a72-125">Rimuove una playlist dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="32a72-125">Removes a playlist from the library.</span></span><br/>                                                                                |
| <span data-ttu-id="32a72-126">**Eliminata**</span><span class="sxs-lookup"><span data-stu-id="32a72-126">**setDeleted**</span></span>                                                                                         | <span data-ttu-id="32a72-127">Non più supportata.</span><span class="sxs-lookup"><span data-stu-id="32a72-127">No longer supported.</span></span><br/>                                                                                                |



 

<span data-ttu-id="32a72-128">Ottenere un'interfaccia **IWMPPlaylistCollection** usando la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="32a72-128">Get an **IWMPPlaylistCollection** interface by using the following property.</span></span>



| <span data-ttu-id="32a72-129">Oggetto</span><span class="sxs-lookup"><span data-stu-id="32a72-129">Object</span></span>                                                                   | <span data-ttu-id="32a72-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32a72-130">Property</span></span>                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32a72-131">Oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="32a72-131">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="32a72-132">**playlistCollection**</span><span class="sxs-lookup"><span data-stu-id="32a72-132">**playlistCollection**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="32a72-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32a72-133">Requirements</span></span>



| <span data-ttu-id="32a72-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="32a72-134">Requirement</span></span> | <span data-ttu-id="32a72-135">Valore</span><span class="sxs-lookup"><span data-stu-id="32a72-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="32a72-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32a72-136">Header</span></span><br/> | <dl> <span data-ttu-id="32a72-137"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="32a72-137"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a72-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32a72-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a72-139">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="32a72-139">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="32a72-140">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="32a72-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="32a72-141">**Interfaccia IWMPPlaylistArray (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="32a72-141">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





