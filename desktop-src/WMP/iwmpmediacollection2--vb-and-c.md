---
title: Interfaccia IWMPMediaCollection2 (VB e C) (WMP. h)
description: Fornisce metodi che integrano l'interfaccia IWMPMediaCollection.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- Interfaccia IWMPMediaCollection2 (VB e C) Windows Media Player
- Interfaccia IWMPMediaCollection2 (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329309"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a><span data-ttu-id="f06aa-105">Interfaccia IWMPMediaCollection2 (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="f06aa-105">IWMPMediaCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="f06aa-106">Fornisce metodi che integrano l'interfaccia **IWMPMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="f06aa-106">Provides methods that supplement the **IWMPMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="f06aa-107">Membri</span><span class="sxs-lookup"><span data-stu-id="f06aa-107">Members</span></span>

<span data-ttu-id="f06aa-108">L'interfaccia **IWMPMediaCollection2 (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f06aa-108">The **IWMPMediaCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="f06aa-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f06aa-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f06aa-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="f06aa-110">Methods</span></span>

<span data-ttu-id="f06aa-111">L'interfaccia **IWMPMediaCollection2 (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f06aa-111">The **IWMPMediaCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="f06aa-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="f06aa-112">Method</span></span>                                                                                                                     | <span data-ttu-id="f06aa-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f06aa-113">Description</span></span>                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f06aa-114">**createQuery**</span><span class="sxs-lookup"><span data-stu-id="f06aa-114">**createQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | <span data-ttu-id="f06aa-115">Restituisce un'interfaccia **IWMPQuery** che rappresenta una nuova query.</span><span class="sxs-lookup"><span data-stu-id="f06aa-115">Returns an **IWMPQuery** interface that represents a new query.</span></span><br/>                                                                                               |
| [<span data-ttu-id="f06aa-116">**getByAttributeAndMediaType**</span><span class="sxs-lookup"><span data-stu-id="f06aa-116">**getByAttributeAndMediaType**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | <span data-ttu-id="f06aa-117">Restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali con un attributo e un tipo di supporto specificati.</span><span class="sxs-lookup"><span data-stu-id="f06aa-117">Returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span><br/>                                     |
| [<span data-ttu-id="f06aa-118">**getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="f06aa-118">**getPlaylistByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | <span data-ttu-id="f06aa-119">Restituisce un'interfaccia **IWMPPlaylist** che consente di accedere agli elementi multimediali che corrispondono alle condizioni della query.</span><span class="sxs-lookup"><span data-stu-id="f06aa-119">Returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span><br/>                                                    |
| [<span data-ttu-id="f06aa-120">**getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="f06aa-120">**getStringCollectionByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | <span data-ttu-id="f06aa-121">Restituisce un'interfaccia **IWMPStringCollection** che fornisce l'accesso al set di tutti i valori stringa per un attributo specificato che soddisfano le condizioni della query.</span><span class="sxs-lookup"><span data-stu-id="f06aa-121">Returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span><br/> |



 

<span data-ttu-id="f06aa-122">Ottenere un'interfaccia **IWMPMediaCollection2** eseguendo il cast del valore restituito dalla proprietà [**AxWindowsMediaPlayer. mediacollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) o dal valore restituito dalla proprietà [**IWMPLibrary. mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="f06aa-122">Get an **IWMPMediaCollection2** interface by casting the value returned by the [**AxWindowsMediaPlayer.mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) property or the value returned by the [**IWMPLibrary.mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f06aa-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f06aa-123">Requirements</span></span>



| <span data-ttu-id="f06aa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f06aa-124">Requirement</span></span> | <span data-ttu-id="f06aa-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f06aa-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f06aa-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f06aa-126">Header</span></span><br/> | <dl> <span data-ttu-id="f06aa-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="f06aa-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f06aa-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f06aa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f06aa-129">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="f06aa-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="f06aa-130">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f06aa-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





