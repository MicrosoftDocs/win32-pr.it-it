---
title: Messaggio di WM_CAP_ABORT (VFW. h)
description: Il \_ messaggio WM Cap \_ Abort interrompe l'operazione di acquisizione.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- WM_CAP_ABORT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517722"
---
# <a name="wm_cap_abort-message"></a><span data-ttu-id="9718c-104">Messaggio di interruzione di WM \_ Cap \_</span><span class="sxs-lookup"><span data-stu-id="9718c-104">WM\_CAP\_ABORT message</span></span>

<span data-ttu-id="9718c-105">Il messaggio **WM \_ Cap \_ Abort** interrompe l'operazione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9718c-105">The **WM\_CAP\_ABORT** message stops the capture operation.</span></span> <span data-ttu-id="9718c-106">Nel caso di Step Capture, i dati dell'immagine raccolti fino al punto del messaggio di **\_ \_ interruzione di WM Cap** verranno conservati nel file di acquisizione, ma l'audio non verrà acquisito.</span><span class="sxs-lookup"><span data-stu-id="9718c-106">In the case of step capture, the image data collected up to the point of the **WM\_CAP\_ABORT** message will be retained in the capture file, but audio will not be captured.</span></span> <span data-ttu-id="9718c-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) .</span><span class="sxs-lookup"><span data-stu-id="9718c-107">You can send this message explicitly or by using the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro.</span></span>


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="9718c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9718c-108">Return Value</span></span>

<span data-ttu-id="9718c-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9718c-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9718c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9718c-110">Remarks</span></span>

<span data-ttu-id="9718c-111">Per utilizzare questo messaggio, è necessario che l'operazione di acquisizione venga restituita.</span><span class="sxs-lookup"><span data-stu-id="9718c-111">The capture operation must yield to use this message.</span></span>

<span data-ttu-id="9718c-112">Usare il messaggio di [**\_ \_ arresto di WM Cap**](wm-cap-stop.md) per arrestare l'acquisizione del passaggio nella posizione corrente e quindi acquisire l'audio.</span><span class="sxs-lookup"><span data-stu-id="9718c-112">Use the [**WM\_CAP\_STOP**](wm-cap-stop.md) message to halt step capture at the current position, and then capture audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="9718c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9718c-113">Requirements</span></span>



| <span data-ttu-id="9718c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9718c-114">Requirement</span></span> | <span data-ttu-id="9718c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9718c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9718c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9718c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9718c-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9718c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9718c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9718c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9718c-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9718c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9718c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9718c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9718c-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9718c-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9718c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9718c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9718c-123">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="9718c-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9718c-124">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="9718c-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





