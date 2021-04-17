---
title: Messaggio di WM_CAP_GRAB_FRAME (VFW. h)
description: Il \_ \_ \_ messaggio di cattura frame WM Cap recupera e visualizza un singolo frame dal driver di acquisizione. Dopo l'acquisizione, la sovrapposizione e l'anteprima sono disabilitate. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capGrabFrame.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- WM_CAP_GRAB_FRAME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd91ce767ad86ddac002bb216420b604883d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477254"
---
# <a name="wm_cap_grab_frame-message"></a><span data-ttu-id="e3d1f-106">\_Messaggio di \_ cattura del frame WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="e3d1f-106">WM\_CAP\_GRAB\_FRAME message</span></span>

<span data-ttu-id="e3d1f-107">Il messaggio di cattura **\_ \_ \_ frame WM Cap** recupera e visualizza un singolo frame dal driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="e3d1f-107">The **WM\_CAP\_GRAB\_FRAME** message retrieves and displays a single frame from the capture driver.</span></span> <span data-ttu-id="e3d1f-108">Dopo l'acquisizione, la sovrapposizione e l'anteprima sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="e3d1f-108">After capture, overlay and preview are disabled.</span></span> <span data-ttu-id="e3d1f-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) .</span><span class="sxs-lookup"><span data-stu-id="e3d1f-109">You can send this message explicitly or by using the [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a><span data-ttu-id="e3d1f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3d1f-110">Return Value</span></span>

<span data-ttu-id="e3d1f-111">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e3d1f-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3d1f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3d1f-112">Remarks</span></span>

<span data-ttu-id="e3d1f-113">Per informazioni sull'installazione delle funzioni di callback, vedere l' [**errore di callback di WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) e [**WM \_ Cap \_ set callback message \_ \_ frame**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="e3d1f-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3d1f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3d1f-114">Requirements</span></span>



| <span data-ttu-id="e3d1f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3d1f-115">Requirement</span></span> | <span data-ttu-id="e3d1f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e3d1f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e3d1f-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3d1f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d1f-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e3d1f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e3d1f-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3d1f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d1f-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e3d1f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e3d1f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3d1f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3d1f-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3d1f-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3d1f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3d1f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d1f-124">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e3d1f-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e3d1f-125">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e3d1f-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





