---
title: Messaggio di MCIWNDM_SETOWNER (VFW. h)
description: Il \_ messaggio SEtowner MCIWNDM imposta la finestra per ricevere i messaggi di notifica associati alla finestra di MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetOwner.
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- MCIWNDM_SETOWNER messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120463"
---
# <a name="mciwndm_setowner-message"></a><span data-ttu-id="aff77-105">\_Messaggio SEtowner MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="aff77-105">MCIWNDM\_SETOWNER message</span></span>

<span data-ttu-id="aff77-106">Il **messaggio \_ SetOwner MCIWNDM** imposta la finestra per ricevere i messaggi di notifica associati alla finestra di MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="aff77-106">The **MCIWNDM\_SETOWNER** message sets the window to receive notification messages associated with the MCIWnd window.</span></span> <span data-ttu-id="aff77-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .</span><span class="sxs-lookup"><span data-stu-id="aff77-107">You can send this message explicitly or by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="aff77-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aff77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff77-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span><span class="sxs-lookup"><span data-stu-id="aff77-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span></span>
</dt> <dd>

<span data-ttu-id="aff77-110">Handle per la finestra per ricevere i messaggi di notifica.</span><span class="sxs-lookup"><span data-stu-id="aff77-110">Handle to the window to receive the notification messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aff77-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aff77-111">Return Value</span></span>

<span data-ttu-id="aff77-112">Restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="aff77-112">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff77-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aff77-113">Requirements</span></span>



| <span data-ttu-id="aff77-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aff77-114">Requirement</span></span> | <span data-ttu-id="aff77-115">Valore</span><span class="sxs-lookup"><span data-stu-id="aff77-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="aff77-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aff77-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aff77-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aff77-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="aff77-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aff77-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aff77-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aff77-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aff77-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aff77-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aff77-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff77-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff77-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aff77-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff77-123">**MCIWndSetOwner**</span><span class="sxs-lookup"><span data-stu-id="aff77-123">**MCIWndSetOwner**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





