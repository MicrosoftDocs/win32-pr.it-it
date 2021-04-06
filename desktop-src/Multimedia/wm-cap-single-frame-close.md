---
title: Messaggio di WM_CAP_SINGLE_FRAME_CLOSE (VFW. h)
description: Il \_ \_ \_ messaggio di chiusura singolo frame WM Cap \_ chiude il file di acquisizione aperto dal \_ \_ messaggio di apertura del singolo frame WM Cap \_ \_ . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureSingleFrameClose.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- WM_CAP_SINGLE_FRAME_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743546"
---
# <a name="wm_cap_single_frame_close-message"></a><span data-ttu-id="bb04d-105">\_Messaggio di \_ \_ chiusura frame singolo WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="bb04d-105">WM\_CAP\_SINGLE\_FRAME\_CLOSE message</span></span>

<span data-ttu-id="bb04d-106">Il messaggio di **\_ \_ \_ \_ chiusura singolo frame WM Cap** chiude il file di acquisizione aperto dal messaggio di [**\_ \_ \_ \_ apertura del singolo frame WM Cap**](wm-cap-single-frame-open.md) .</span><span class="sxs-lookup"><span data-stu-id="bb04d-106">The **WM\_CAP\_SINGLE\_FRAME\_CLOSE** message closes the capture file opened by the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="bb04d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) .</span><span class="sxs-lookup"><span data-stu-id="bb04d-107">You can send this message explicitly or by using the [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="bb04d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb04d-108">Return Value</span></span>

<span data-ttu-id="bb04d-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bb04d-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb04d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb04d-110">Remarks</span></span>

<span data-ttu-id="bb04d-111">Per informazioni sull'installazione delle funzioni di callback, vedere l' [**errore di callback di WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) e [**WM \_ Cap \_ set callback message \_ \_ frame**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="bb04d-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb04d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb04d-112">Requirements</span></span>



| <span data-ttu-id="bb04d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb04d-113">Requirement</span></span> | <span data-ttu-id="bb04d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="bb04d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb04d-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb04d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bb04d-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb04d-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bb04d-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb04d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bb04d-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb04d-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bb04d-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb04d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb04d-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb04d-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb04d-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb04d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb04d-122">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="bb04d-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="bb04d-123">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="bb04d-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





