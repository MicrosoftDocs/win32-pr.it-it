---
title: Messaggio di WM_CAP_SET_SCALE (VFW. h)
description: Il \_ \_ \_ messaggio di scalabilità set di WM consente di abilitare o disabilitare il ridimensionamento delle immagini video di anteprima.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121391"
---
# <a name="wm_cap_set_scale-message"></a><span data-ttu-id="e7319-104">\_Messaggio di \_ \_ scalabilità set di WM Cap</span><span class="sxs-lookup"><span data-stu-id="e7319-104">WM\_CAP\_SET\_SCALE message</span></span>

<span data-ttu-id="e7319-105">Il messaggio di **\_ \_ \_ scalabilità set di WM** consente di abilitare o disabilitare il ridimensionamento delle immagini video di anteprima.</span><span class="sxs-lookup"><span data-stu-id="e7319-105">The **WM\_CAP\_SET\_SCALE** message enables or disables scaling of the preview video images.</span></span> <span data-ttu-id="e7319-106">Se il ridimensionamento è abilitato, il fotogramma video acquisito viene allungato alle dimensioni della finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="e7319-106">If scaling is enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="e7319-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) .</span><span class="sxs-lookup"><span data-stu-id="e7319-107">You can send this message explicitly or by using the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro.</span></span>


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="e7319-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7319-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7319-109"><span id="f"></span><span id="F"></span>*f*</span><span class="sxs-lookup"><span data-stu-id="e7319-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="e7319-110">Flag di ridimensionamento anteprima.</span><span class="sxs-lookup"><span data-stu-id="e7319-110">Preview scaling flag.</span></span> <span data-ttu-id="e7319-111">Specificare **true** per questo parametro per estendere i frame di anteprima alla dimensione della finestra di acquisizione o **false** per visualizzarli alla dimensione naturale.</span><span class="sxs-lookup"><span data-stu-id="e7319-111">Specify **TRUE** for this parameter to stretch preview frames to the size of the capture window or **FALSE** to display them at their natural size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7319-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7319-112">Return Value</span></span>

<span data-ttu-id="e7319-113">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e7319-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7319-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7319-114">Remarks</span></span>

<span data-ttu-id="e7319-115">Il ridimensionamento delle immagini di anteprima controlla la presentazione immediata dei frame acquisiti all'interno della finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="e7319-115">Scaling preview images controls the immediate presentation of captured frames within the capture window.</span></span> <span data-ttu-id="e7319-116">Non ha alcun effetto sulle dimensioni dei frame salvati in un file.</span><span class="sxs-lookup"><span data-stu-id="e7319-116">It has no effect on the size of the frames saved to file.</span></span>

<span data-ttu-id="e7319-117">La scalabilità non ha alcun effetto quando si usa la sovrimpressione per visualizzare il video nel buffer del frame.</span><span class="sxs-lookup"><span data-stu-id="e7319-117">Scaling has no effect when using overlay to display video in the frame buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7319-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7319-118">Requirements</span></span>



| <span data-ttu-id="e7319-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7319-119">Requirement</span></span> | <span data-ttu-id="e7319-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e7319-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e7319-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7319-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e7319-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7319-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e7319-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7319-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e7319-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7319-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e7319-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7319-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7319-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7319-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7319-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7319-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7319-128">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e7319-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e7319-129">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e7319-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





