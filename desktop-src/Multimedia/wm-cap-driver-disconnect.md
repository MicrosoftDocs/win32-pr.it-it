---
title: Messaggio di WM_CAP_DRIVER_DISCONNECT (VFW. h)
description: Il \_ \_ \_ messaggio di disconnessione del driver WM Cap disconnette un driver di acquisizione da una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capDriverDisconnect.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acad628cc61bbb50c56f68fda91ac87be4feb728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964094"
---
# <a name="wm_cap_driver_disconnect-message"></a><span data-ttu-id="e14bd-105">\_Messaggio di \_ disconnessione driver WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="e14bd-105">WM\_CAP\_DRIVER\_DISCONNECT message</span></span>

<span data-ttu-id="e14bd-106">Il messaggio di **\_ \_ \_ disconnessione del driver WM Cap disconnette** un driver di acquisizione da una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="e14bd-106">The **WM\_CAP\_DRIVER\_DISCONNECT** message disconnects a capture driver from a capture window.</span></span> <span data-ttu-id="e14bd-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) .</span><span class="sxs-lookup"><span data-stu-id="e14bd-107">You can send this message explicitly or by using the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="e14bd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e14bd-108">Return Value</span></span>

<span data-ttu-id="e14bd-109">Restituisce **true** se l'operazione ha esito positivo o **false** se la finestra di acquisizione non è connessa a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="e14bd-109">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="e14bd-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e14bd-110">Requirements</span></span>



| <span data-ttu-id="e14bd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e14bd-111">Requirement</span></span> | <span data-ttu-id="e14bd-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e14bd-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e14bd-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e14bd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e14bd-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e14bd-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e14bd-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e14bd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e14bd-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e14bd-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e14bd-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e14bd-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e14bd-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e14bd-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e14bd-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e14bd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e14bd-120">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e14bd-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e14bd-121">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e14bd-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





