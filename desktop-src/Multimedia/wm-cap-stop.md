---
title: Messaggio di WM_CAP_STOP (VFW. h)
description: Il messaggio di arresto di WM \_ Cap \_ interrompe l'operazione di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743538"
---
# <a name="wm_cap_stop-message"></a><span data-ttu-id="2bc01-105">Messaggio di arresto del \_ Cap WM \_</span><span class="sxs-lookup"><span data-stu-id="2bc01-105">WM\_CAP\_STOP message</span></span>

<span data-ttu-id="2bc01-106">Il messaggio di **\_ \_ arresto di WM Cap** interrompe l'operazione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2bc01-106">The **WM\_CAP\_STOP** message stops the capture operation.</span></span> <span data-ttu-id="2bc01-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) .</span><span class="sxs-lookup"><span data-stu-id="2bc01-107">You can send this message explicitly or by using the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro.</span></span>

<span data-ttu-id="2bc01-108">In Step Frame Capture i dati dell'immagine raccolti prima dell'invio del messaggio vengono conservati nel file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2bc01-108">In step frame capture, the image data that was collected before this message was sent is retained in the capture file.</span></span> <span data-ttu-id="2bc01-109">Se è stata abilitata l'acquisizione audio, nel file di acquisizione viene mantenuta anche una durata equivalente dei dati audio.</span><span class="sxs-lookup"><span data-stu-id="2bc01-109">An equivalent duration of audio data is also retained in the capture file if audio capture was enabled.</span></span>


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="2bc01-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2bc01-110">Return Value</span></span>

<span data-ttu-id="2bc01-111">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2bc01-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bc01-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bc01-112">Remarks</span></span>

<span data-ttu-id="2bc01-113">Per utilizzare questo messaggio, è necessario che l'operazione di acquisizione venga restituita.</span><span class="sxs-lookup"><span data-stu-id="2bc01-113">The capture operation must yield to use this message.</span></span> <span data-ttu-id="2bc01-114">Usare il messaggio [**WM \_ Cap \_ Abort**](wm-cap-abort.md) per abbandonare l'operazione di acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="2bc01-114">Use the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message to abandon the current capture operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc01-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bc01-115">Requirements</span></span>



| <span data-ttu-id="2bc01-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bc01-116">Requirement</span></span> | <span data-ttu-id="2bc01-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2bc01-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2bc01-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bc01-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc01-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2bc01-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2bc01-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bc01-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc01-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2bc01-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2bc01-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2bc01-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bc01-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bc01-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bc01-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bc01-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc01-125">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2bc01-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2bc01-126">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2bc01-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





