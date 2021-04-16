---
description: Valore che definisce il sistema di misurazione per un valore di profondità in un frame video.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: Attributo MF_MT_DEPTH_MEASUREMENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560652"
---
# <a name="mf_mt_depth_measurement-attribute"></a><span data-ttu-id="9167d-103">\_Attributo di \_ misurazione della profondità MF mt \_</span><span class="sxs-lookup"><span data-stu-id="9167d-103">MF\_MT\_DEPTH\_MEASUREMENT attribute</span></span>

<span data-ttu-id="9167d-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9167d-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9167d-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9167d-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9167d-106">Valore che definisce il sistema di misurazione per un valore di profondità in un frame video.</span><span class="sxs-lookup"><span data-stu-id="9167d-106">A value that defines the measurement system for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="9167d-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9167d-107">Data type</span></span>

<span data-ttu-id="9167d-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9167d-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9167d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="9167d-109">Remarks</span></span>

<span data-ttu-id="9167d-110">Questo valore è un membro dell'enumerazione [**\_ MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)</span><span class="sxs-lookup"><span data-stu-id="9167d-110">This value is a member of the [**\_MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement) enumeration</span></span>

<span data-ttu-id="9167d-111">Se questo attributo non è presente, si presuppone che sia **DistanceToFocalPlane**.</span><span class="sxs-lookup"><span data-stu-id="9167d-111">If this attribute is not present it is assumed to be **DistanceToFocalPlane**.</span></span> <span data-ttu-id="9167d-112">La distanza dal piano focale è in genere più facile da utilizzare in un sistema di coordinate euclideo 3D.</span><span class="sxs-lookup"><span data-stu-id="9167d-112">The distance to focal plane is typically easier to consume in a 3D Euclidian coordinate system.</span></span>

![illustrazione di distancetofocalplane](images/distance-to-focal-plane.png)

<span data-ttu-id="9167d-114">Il formato distanza dal centro focale è in genere costituito da dati non elaborati provenienti dal sensore, ad esempio il tempo delle fotocamere.</span><span class="sxs-lookup"><span data-stu-id="9167d-114">The distance to focal center format is typically raw data from sensor such as time of flight cameras.</span></span>

![illustrazione di distancetoopticalcenter](images/distance-to-optical-center.png)

<span data-ttu-id="9167d-116">Le fotocamere con profondità non possono comprendere la profondità di tutti i pixel.</span><span class="sxs-lookup"><span data-stu-id="9167d-116">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="9167d-117">Quando la confidenza di un pixel è bassa, a causa di materiale, occlusione o non compreso nell'intervallo e così via, il valore di profondità su tale pixel può non essere valido.</span><span class="sxs-lookup"><span data-stu-id="9167d-117">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="9167d-118">Quando un valore di pixel di profondità è 0, il pixel non è valido.</span><span class="sxs-lookup"><span data-stu-id="9167d-118">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="9167d-119">Alcune fotocamere di profondità allineano i metadati della maschera di maschera per ogni pixel oltre al valore di profondità per rappresentare il motivo per cui la profondità del pixel non è valida, a causa del materiale, dell'occlusione o dell'intervallo e così via. Si consiglia di evitare di alleghiare tali metadati come valori di profondità, perché in genere si verificano difficoltà quando si utilizzano tali valori in pixel shader.</span><span class="sxs-lookup"><span data-stu-id="9167d-119">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="9167d-120">Invece.</span><span class="sxs-lookup"><span data-stu-id="9167d-120">Instead.</span></span> <span data-ttu-id="9167d-121">si consiglia di usare un buffer di immagini a 8 bit separato con la stessa risoluzione e di associarlo come attributo di [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="9167d-121">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="9167d-122">Tali metadati variano a seconda del fornitore della fotocamera e non sono standardizzati dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="9167d-122">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="9167d-123">È consigliabile usare 16 bit completi per il valore di profondità per semplificare l'elaborazione a valle e usare un valore fisso, ad esempio 0, per l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="9167d-123">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9167d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9167d-124">Requirements</span></span>



| <span data-ttu-id="9167d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9167d-125">Requirement</span></span> | <span data-ttu-id="9167d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9167d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9167d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9167d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9167d-128">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="9167d-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9167d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9167d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9167d-130">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9167d-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="9167d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9167d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9167d-132"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9167d-132"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




