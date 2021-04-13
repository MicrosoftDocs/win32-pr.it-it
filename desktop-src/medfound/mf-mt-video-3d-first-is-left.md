---
description: Per un formato video 3D, specifica la visualizzazione a sinistra.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: Attributo MF_MT_VIDEO_3D_FIRST_IS_LEFT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401793"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a><span data-ttu-id="2a184-103">MF \_ mt \_ video \_ 3D \_ First \_ è l' \_ attributo Left</span><span class="sxs-lookup"><span data-stu-id="2a184-103">MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute</span></span>

<span data-ttu-id="2a184-104">Per un formato video 3D, specifica la visualizzazione a sinistra.</span><span class="sxs-lookup"><span data-stu-id="2a184-104">For a 3D video format, specifies which view is the left view.</span></span>

## <a name="data-type"></a><span data-ttu-id="2a184-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2a184-105">Data type</span></span>

<span data-ttu-id="2a184-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a184-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2a184-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a184-107">Remarks</span></span>

<span data-ttu-id="2a184-108">Per video 3D, ogni esempio video contiene due visualizzazioni, che sono designate per la *prima visualizzazione* e la *seconda*.</span><span class="sxs-lookup"><span data-stu-id="2a184-108">For 3D video, each video sample contains two views, which are designated *first view* and *second view*.</span></span> <span data-ttu-id="2a184-109">Il layout esatto delle visualizzazioni in memoria è indicato dall'attributo del [ \_ \_ \_ \_ Formato video 3D MF mt](mf-mt-video-3d-format.md) .</span><span class="sxs-lookup"><span data-stu-id="2a184-109">The exact layout of the views in memory is indicated by the [MF\_MT\_VIDEO\_3D\_FORMAT](mf-mt-video-3d-format.md) attribute.</span></span>



| <span data-ttu-id="2a184-110">Formato</span><span class="sxs-lookup"><span data-stu-id="2a184-110">Format</span></span>               | <span data-ttu-id="2a184-111">Prima visualizzazione</span><span class="sxs-lookup"><span data-stu-id="2a184-111">First View</span></span>              | <span data-ttu-id="2a184-112">Seconda visualizzazione</span><span class="sxs-lookup"><span data-stu-id="2a184-112">Second View</span></span>               |
|----------------------|-------------------------|---------------------------|
| <span data-ttu-id="2a184-113">Compresso affiancato</span><span class="sxs-lookup"><span data-stu-id="2a184-113">Packed side-by-side</span></span>  | <span data-ttu-id="2a184-114">Metà sinistra del buffer</span><span class="sxs-lookup"><span data-stu-id="2a184-114">Left half of the buffer</span></span> | <span data-ttu-id="2a184-115">Metà destra del buffer</span><span class="sxs-lookup"><span data-stu-id="2a184-115">Right half of the buffer</span></span>  |
| <span data-ttu-id="2a184-116">Dall'alto verso il basso compresso</span><span class="sxs-lookup"><span data-stu-id="2a184-116">Packed top-to-bottom</span></span> | <span data-ttu-id="2a184-117">Metà superiore del buffer</span><span class="sxs-lookup"><span data-stu-id="2a184-117">Top half of the buffer</span></span>  | <span data-ttu-id="2a184-118">Metà inferiore del buffer</span><span class="sxs-lookup"><span data-stu-id="2a184-118">Bottom half of the buffer</span></span> |
| <span data-ttu-id="2a184-119">MultiView</span><span class="sxs-lookup"><span data-stu-id="2a184-119">Multiview</span></span>            | <span data-ttu-id="2a184-120">Indice buffer 0</span><span class="sxs-lookup"><span data-stu-id="2a184-120">Buffer index 0</span></span>          | <span data-ttu-id="2a184-121">Indice buffer 1</span><span class="sxs-lookup"><span data-stu-id="2a184-121">Buffer index 1</span></span>            |
| <span data-ttu-id="2a184-122">Visualizzazione di base</span><span class="sxs-lookup"><span data-stu-id="2a184-122">Base view</span></span>            | <span data-ttu-id="2a184-123">Intero frame</span><span class="sxs-lookup"><span data-stu-id="2a184-123">Entire frame</span></span>            | <span data-ttu-id="2a184-124">Non presente</span><span class="sxs-lookup"><span data-stu-id="2a184-124">Not present</span></span>               |



 

<span data-ttu-id="2a184-125">Per impostazione predefinita, la prima visualizzazione è la visualizzazione a sinistra e la seconda visualizzazione è la vista corretta.</span><span class="sxs-lookup"><span data-stu-id="2a184-125">By default, the first view is the left view, and the second view is the right view.</span></span> <span data-ttu-id="2a184-126">Se le visualizzazioni a sinistra e a destra sono state scambiate, impostare la MF \_ mt \_ video \_ 3D \_ First \_ è \_ Left attribute su **false** nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="2a184-126">If the left and right views are swapped, set the MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute to **FALSE** in the media type.</span></span>

> [!Note]  
> <span data-ttu-id="2a184-127">Nel formato di *vista di base* (**MFVideo3DSampleFormat \_ BaseView**) viene mantenuta solo la visualizzazione di base, pertanto questo attributo non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="2a184-127">In *base view* format (**MFVideo3DSampleFormat\_BaseView**), only the base view is retained, so this attribute does not apply.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2a184-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a184-128">Requirements</span></span>



| <span data-ttu-id="2a184-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a184-129">Requirement</span></span> | <span data-ttu-id="2a184-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2a184-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a184-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a184-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2a184-132">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a184-132">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2a184-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a184-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2a184-134">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="2a184-134">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2a184-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a184-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a184-136"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a184-136"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a184-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a184-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a184-138">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a184-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




