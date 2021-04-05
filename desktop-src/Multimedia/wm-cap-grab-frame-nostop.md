---
title: Messaggio di WM_CAP_GRAB_FRAME_NOSTOP (VFW. h)
description: Il \_ \_ messaggio NOSTOP di WM Cap \_ \_ Capture frame riempie il frame buffer con un singolo frame non compresso dal dispositivo di acquisizione e lo Visualizza.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073cf5eae44f564d24cd1ebb67193d8738fd77b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874293"
---
# <a name="wm_cap_grab_frame_nostop-message"></a><span data-ttu-id="0c631-104">\_ \_ \_ Messaggio NOSTOP frame di cattura WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="0c631-104">WM\_CAP\_GRAB\_FRAME\_NOSTOP message</span></span>

<span data-ttu-id="0c631-105">Il **messaggio \_ \_ \_ \_ NOSTOP di WM Cap Capture frame** riempie il frame buffer con un singolo frame non compresso dal dispositivo di acquisizione e lo Visualizza.</span><span class="sxs-lookup"><span data-stu-id="0c631-105">The **WM\_CAP\_GRAB\_FRAME\_NOSTOP** message fills the frame buffer with a single uncompressed frame from the capture device and displays it.</span></span> <span data-ttu-id="0c631-106">A differenza del messaggio [**di \_ \_ cattura del \_ frame WM Cap**](wm-cap-grab-frame.md) , lo stato della sovrimpressione o dell'anteprima non viene modificato da questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="0c631-106">Unlike with the [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message, the state of overlay or preview is not altered by this message.</span></span> <span data-ttu-id="0c631-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) .</span><span class="sxs-lookup"><span data-stu-id="0c631-107">You can send this message explicitly or by using the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="0c631-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c631-108">Return Value</span></span>

<span data-ttu-id="0c631-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0c631-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c631-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c631-110">Remarks</span></span>

<span data-ttu-id="0c631-111">Per informazioni sull'installazione delle funzioni di callback, vedere l' [**errore di callback di WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) e [**WM \_ Cap \_ set callback message \_ \_ frame**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="0c631-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c631-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c631-112">Requirements</span></span>



| <span data-ttu-id="0c631-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c631-113">Requirement</span></span> | <span data-ttu-id="0c631-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0c631-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0c631-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c631-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0c631-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0c631-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0c631-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c631-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0c631-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0c631-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0c631-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c631-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c631-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c631-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c631-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c631-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c631-122">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="0c631-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0c631-123">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="0c631-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





