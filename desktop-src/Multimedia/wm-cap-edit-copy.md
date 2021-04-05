---
title: Messaggio di WM_CAP_EDIT_COPY (VFW. h)
description: Il \_ \_ messaggio di copia di modifica di WM Cap \_ copia il contenuto del buffer del frame video e della tavolozza associata negli Appunti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capEditCopy.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- WM_CAP_EDIT_COPY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120451"
---
# <a name="wm_cap_edit_copy-message"></a><span data-ttu-id="3e5d2-105">\_ \_ Modifica \_ copia messaggio WM Cap</span><span class="sxs-lookup"><span data-stu-id="3e5d2-105">WM\_CAP\_EDIT\_COPY message</span></span>

<span data-ttu-id="3e5d2-106">Il messaggio di **\_ copia di \_ modifica \_ di WM Cap** copia il contenuto del buffer del frame video e della tavolozza associata negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="3e5d2-106">The **WM\_CAP\_EDIT\_COPY** message copies the contents of the video frame buffer and associated palette to the clipboard.</span></span> <span data-ttu-id="3e5d2-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) .</span><span class="sxs-lookup"><span data-stu-id="3e5d2-107">You can send this message explicitly or by using the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro.</span></span>


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="3e5d2-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e5d2-108">Return Value</span></span>

<span data-ttu-id="3e5d2-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3e5d2-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e5d2-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e5d2-110">Requirements</span></span>



| <span data-ttu-id="3e5d2-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e5d2-111">Requirement</span></span> | <span data-ttu-id="3e5d2-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3e5d2-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3e5d2-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e5d2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3e5d2-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e5d2-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3e5d2-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e5d2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3e5d2-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e5d2-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3e5d2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e5d2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e5d2-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e5d2-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e5d2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e5d2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e5d2-120">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="3e5d2-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3e5d2-121">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="3e5d2-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





