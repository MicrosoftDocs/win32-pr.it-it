---
title: Messaggio di WM_CAP_SINGLE_FRAME_OPEN (VFW. h)
description: Il \_ \_ \_ messaggio di apertura del singolo frame WM Cap \_ apre il file di acquisizione per l'acquisizione di un singolo frame. Eventuali informazioni precedenti nel file di acquisizione vengono sovrascritte. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureSingleFrameOpen.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- WM_CAP_SINGLE_FRAME_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac38186e4b5a34bbc11563b7e37a1aefc3de18c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874510"
---
# <a name="wm_cap_single_frame_open-message"></a><span data-ttu-id="c42b0-106">\_ \_ \_ Messaggio aperto del singolo frame WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="c42b0-106">WM\_CAP\_SINGLE\_FRAME\_OPEN message</span></span>

<span data-ttu-id="c42b0-107">Il messaggio di **\_ \_ apertura del singolo \_ frame \_ WM Cap** apre il file di acquisizione per l'acquisizione di un singolo frame.</span><span class="sxs-lookup"><span data-stu-id="c42b0-107">The **WM\_CAP\_SINGLE\_FRAME\_OPEN** message opens the capture file for single-frame capturing.</span></span> <span data-ttu-id="c42b0-108">Eventuali informazioni precedenti nel file di acquisizione vengono sovrascritte.</span><span class="sxs-lookup"><span data-stu-id="c42b0-108">Any previous information in the capture file is overwritten.</span></span> <span data-ttu-id="c42b0-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) .</span><span class="sxs-lookup"><span data-stu-id="c42b0-109">You can send this message explicitly or by using the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_OPEN 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="c42b0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c42b0-110">Return Value</span></span>

<span data-ttu-id="c42b0-111">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c42b0-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c42b0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c42b0-112">Remarks</span></span>

<span data-ttu-id="c42b0-113">Per informazioni sull'installazione delle funzioni di callback, vedere l' [**errore di callback di WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) e [**WM \_ Cap \_ set callback message \_ \_ frame**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="c42b0-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="c42b0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c42b0-114">Requirements</span></span>



| <span data-ttu-id="c42b0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c42b0-115">Requirement</span></span> | <span data-ttu-id="c42b0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c42b0-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c42b0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c42b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c42b0-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c42b0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c42b0-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c42b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c42b0-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c42b0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c42b0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c42b0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c42b0-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c42b0-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c42b0-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c42b0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c42b0-124">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="c42b0-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c42b0-125">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="c42b0-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





