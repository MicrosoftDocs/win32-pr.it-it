---
title: Interfaccia IWMPMedia3 (VB e C) (WMP. h)
description: Fornisce metodi aggiuntivi per accedere alle proprietà di un elemento multimediale.
ms.assetid: e16aa5e2-ae44-41c2-8c61-fb688c2e89e2
keywords:
- Interfaccia IWMPMedia3 (VB e C) Windows Media Player
- Interfaccia IWMPMedia3 (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPMedia3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb5438ad4d80031d5b45c738c6b6cc9335018af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324538"
---
# <a name="iwmpmedia3-vb-and-c-interface"></a><span data-ttu-id="16945-105">Interfaccia IWMPMedia3 (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="16945-105">IWMPMedia3 (VB and C#) interface</span></span>

<span data-ttu-id="16945-106">Fornisce metodi aggiuntivi per accedere alle proprietà di un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="16945-106">Provides additional methods to access the properties of a media item.</span></span>

## <a name="members"></a><span data-ttu-id="16945-107">Membri</span><span class="sxs-lookup"><span data-stu-id="16945-107">Members</span></span>

<span data-ttu-id="16945-108">L'interfaccia **IWMPMedia3 (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="16945-108">The **IWMPMedia3 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="16945-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="16945-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="16945-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="16945-110">Methods</span></span>

<span data-ttu-id="16945-111">L'interfaccia **IWMPMedia3 (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="16945-111">The **IWMPMedia3 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="16945-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="16945-112">Method</span></span>                                                                                           | <span data-ttu-id="16945-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16945-113">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16945-114">**getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="16945-114">**getAttributeCountByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="16945-115">Restituisce il numero di attributi associati al tipo di attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="16945-115">Returns the number of attributes associated with the specified attribute type.</span></span><br/>              |
| [<span data-ttu-id="16945-116">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="16945-116">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="16945-117">Restituisce il valore dell'attributo corrispondente al tipo di attributo e all'indice specificati.</span><span class="sxs-lookup"><span data-stu-id="16945-117">Returns the value of the attribute corresponding to the specified attribute type and index.</span></span><br/> |



 

<span data-ttu-id="16945-118">Ottenere un'interfaccia **IWMPMedia3** eseguendo il cast del valore restituito da uno dei metodi o delle proprietà seguenti a cui si accede tramite l'oggetto o l'interfaccia seguente.</span><span class="sxs-lookup"><span data-stu-id="16945-118">Get an **IWMPMedia3** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="16945-119">Oggetto o interfaccia</span><span class="sxs-lookup"><span data-stu-id="16945-119">Object or interface</span></span>                                               | <span data-ttu-id="16945-120">Proprietà o metodo</span><span class="sxs-lookup"><span data-stu-id="16945-120">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16945-121">IWMPControls</span><span class="sxs-lookup"><span data-stu-id="16945-121">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="16945-122">currentItem</span><span class="sxs-lookup"><span data-stu-id="16945-122">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="16945-123">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="16945-123">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="16945-124">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="16945-124">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="16945-125">IWMPPlaylist</span><span class="sxs-lookup"><span data-stu-id="16945-125">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="16945-126">[Item](iwmpplaylist-item--vb-and-c.md) ( **get \_ Item** in C#)</span><span class="sxs-lookup"><span data-stu-id="16945-126">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="16945-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16945-127">Requirements</span></span>



| <span data-ttu-id="16945-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="16945-128">Requirement</span></span> | <span data-ttu-id="16945-129">Valore</span><span class="sxs-lookup"><span data-stu-id="16945-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="16945-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16945-130">Header</span></span><br/> | <dl> <span data-ttu-id="16945-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="16945-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16945-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16945-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16945-133">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="16945-133">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="16945-134">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="16945-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="16945-135">**Interfaccia IWMPMedia2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="16945-135">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





