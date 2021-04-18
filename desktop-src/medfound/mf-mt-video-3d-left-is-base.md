---
description: Per un formato video 3D, specifica quale visualizzazione è la visualizzazione di base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: Attributo MF_MT_VIDEO_3D_LEFT_IS_BASE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316442"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a><span data-ttu-id="02c48-103">MF \_ mt \_ video \_ 3D \_ Left \_ è l' \_ attributo di base</span><span class="sxs-lookup"><span data-stu-id="02c48-103">MF\_MT\_VIDEO\_3D\_LEFT\_IS\_BASE attribute</span></span>

<span data-ttu-id="02c48-104">Per un formato video 3D, specifica quale visualizzazione è la visualizzazione di base.</span><span class="sxs-lookup"><span data-stu-id="02c48-104">For a 3D video format, specifies which view is the base view.</span></span>

## <a name="data-type"></a><span data-ttu-id="02c48-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="02c48-105">Data type</span></span>

<span data-ttu-id="02c48-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02c48-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="02c48-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="02c48-107">Remarks</span></span>

<span data-ttu-id="02c48-108">Per impostazione predefinita, la visualizzazione a sinistra in una sequenza video 3D è la visualizzazione di base.</span><span class="sxs-lookup"><span data-stu-id="02c48-108">By default, the left view in a 3D video sequence is the base view.</span></span> <span data-ttu-id="02c48-109">Se la visualizzazione a destra è la visualizzazione di base, impostare questo attributo su **false**.</span><span class="sxs-lookup"><span data-stu-id="02c48-109">If the right view is the base view, set this attribute to **FALSE**.</span></span>

<span data-ttu-id="02c48-110">Per convertire il video stereoscopico in 2D, lasciare la visualizzazione di base ed eliminare l'altra visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="02c48-110">To convert stereoscopic video to 2D, keep the base view and discard the other view.</span></span>

## <a name="requirements"></a><span data-ttu-id="02c48-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02c48-111">Requirements</span></span>



| <span data-ttu-id="02c48-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="02c48-112">Requirement</span></span> | <span data-ttu-id="02c48-113">Valore</span><span class="sxs-lookup"><span data-stu-id="02c48-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02c48-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02c48-114">Minimum supported client</span></span><br/> | <span data-ttu-id="02c48-115">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="02c48-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="02c48-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02c48-116">Minimum supported server</span></span><br/> | <span data-ttu-id="02c48-117">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="02c48-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="02c48-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02c48-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="02c48-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="02c48-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02c48-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02c48-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c48-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="02c48-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




