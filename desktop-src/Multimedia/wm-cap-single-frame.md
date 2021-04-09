---
title: Messaggio di WM_CAP_SINGLE_FRAME (VFW. h)
description: Il \_ messaggio con \_ frame singolo WM Cap \_ aggiunge un singolo frame a un file di acquisizione aperto con il messaggio di \_ apertura del \_ singolo frame WM Cap \_ \_ . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121383"
---
# <a name="wm_cap_single_frame-message"></a><span data-ttu-id="49563-105">\_Messaggio con \_ frame singolo WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="49563-105">WM\_CAP\_SINGLE\_FRAME message</span></span>

<span data-ttu-id="49563-106">Il messaggio con **\_ \_ \_ frame singolo WM Cap** aggiunge un singolo frame a un file di acquisizione aperto con il messaggio di [**\_ \_ \_ \_ apertura del singolo frame WM Cap**](wm-cap-single-frame-open.md) .</span><span class="sxs-lookup"><span data-stu-id="49563-106">The **WM\_CAP\_SINGLE\_FRAME** message appends a single frame to a capture file that was opened using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="49563-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) .</span><span class="sxs-lookup"><span data-stu-id="49563-107">You can send this message explicitly or by using the [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="49563-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49563-108">Return Value</span></span>

<span data-ttu-id="49563-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="49563-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="49563-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49563-110">Requirements</span></span>



| <span data-ttu-id="49563-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="49563-111">Requirement</span></span> | <span data-ttu-id="49563-112">Valore</span><span class="sxs-lookup"><span data-stu-id="49563-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="49563-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49563-113">Minimum supported client</span></span><br/> | <span data-ttu-id="49563-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49563-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="49563-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49563-115">Minimum supported server</span></span><br/> | <span data-ttu-id="49563-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49563-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="49563-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49563-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="49563-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="49563-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49563-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49563-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49563-120">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="49563-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="49563-121">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="49563-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





