---
title: Interfaccia IWMPMetadataPicture (VB e C) (WMP. h)
description: Fornisce le proprietà per ottenere informazioni sull'immagine contenuta in un file multimediale digitale rappresentato da un attributo WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- Interfaccia IWMPMetadataPicture (VB e C) Windows Media Player
- Interfaccia IWMPMetadataPicture (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331388"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a><span data-ttu-id="03e50-105">Interfaccia IWMPMetadataPicture (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="03e50-105">IWMPMetadataPicture (VB and C#) interface</span></span>

<span data-ttu-id="03e50-106">Fornisce le proprietà per ottenere informazioni sull'immagine contenuta in un file multimediale digitale rappresentato da un attributo di metadati [**WM/Picture**](/windows/desktop/wmformat/wmpicture).</span><span class="sxs-lookup"><span data-stu-id="03e50-106">Provides properties for getting information about the image contained in a digital media file that is represented by a [**WM/Picture**](/windows/desktop/wmformat/wmpicture)metadata attribute.</span></span> <span data-ttu-id="03e50-107">Questo attributo corrisponde alle immagini dell'album Art contenute in un file multimediale digitale, non all'Art album scaricato tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="03e50-107">This attribute corresponds to album art images contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="03e50-108">L'interfaccia **IWMPMetadataPicture** espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="03e50-108">The **IWMPMetadataPicture** interface exposes the following properties.</span></span>



| <span data-ttu-id="03e50-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03e50-109">Property</span></span>                                                                                   | <span data-ttu-id="03e50-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03e50-110">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="03e50-111">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="03e50-111">**Description**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | <span data-ttu-id="03e50-112">Ottiene la descrizione dell'immagine rappresentata dall'attributo dei metadati.</span><span class="sxs-lookup"><span data-stu-id="03e50-112">Gets the description of the image represented by the metadata attribute.</span></span>  |
| [<span data-ttu-id="03e50-113">**mimeType**</span><span class="sxs-lookup"><span data-stu-id="03e50-113">**mimeType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | <span data-ttu-id="03e50-114">Ottiene il tipo MIME dell'immagine rappresentata dall'attributo dei metadati.</span><span class="sxs-lookup"><span data-stu-id="03e50-114">Gets the MIME type of the image represented by the metadata attribute.</span></span>    |
| [<span data-ttu-id="03e50-115">**pictureType**</span><span class="sxs-lookup"><span data-stu-id="03e50-115">**pictureType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | <span data-ttu-id="03e50-116">Ottiene il tipo di immagine dell'immagine rappresentata dall'attributo dei metadati.</span><span class="sxs-lookup"><span data-stu-id="03e50-116">Gets the picture type of the image represented by the metadata attribute.</span></span> |
| [<span data-ttu-id="03e50-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="03e50-117">**URL**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | <span data-ttu-id="03e50-118">Solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="03e50-118">Internal use only.</span></span>                                                        |



 

<span data-ttu-id="03e50-119">Ottenere un'interfaccia **IWMPMetadataPicture** passando il nome dell'attributo [**WM/Picture**](/windows/desktop/wmformat/wmpicture) al metodo seguente ed eseguendo il cast dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="03e50-119">Get an **IWMPMetadataPicture** interface by passing in the attribute name [**WM/Picture**](/windows/desktop/wmformat/wmpicture) to the following method and casting the object that is returned.</span></span>



| <span data-ttu-id="03e50-120">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="03e50-120">Interface</span></span>                                  | <span data-ttu-id="03e50-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03e50-121">Property</span></span>                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="03e50-122">**IWMPMedia3**</span><span class="sxs-lookup"><span data-stu-id="03e50-122">**IWMPMedia3**</span></span>](iwmpmedia3--vb-and-c.md) | [<span data-ttu-id="03e50-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="03e50-123">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a><span data-ttu-id="03e50-124">Membri</span><span class="sxs-lookup"><span data-stu-id="03e50-124">Members</span></span>

<span data-ttu-id="03e50-125">L'interfaccia **IWMPMetadataPicture (VB e C#)** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="03e50-125">The **IWMPMetadataPicture (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="03e50-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03e50-126">Requirements</span></span>



| <span data-ttu-id="03e50-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="03e50-127">Requirement</span></span> | <span data-ttu-id="03e50-128">Valore</span><span class="sxs-lookup"><span data-stu-id="03e50-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="03e50-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03e50-129">Header</span></span><br/> | <dl> <span data-ttu-id="03e50-130"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="03e50-130"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03e50-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03e50-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e50-132">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="03e50-132">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

