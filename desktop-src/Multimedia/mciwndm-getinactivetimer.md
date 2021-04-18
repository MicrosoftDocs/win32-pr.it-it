---
title: Messaggio di MCIWNDM_GETINACTIVETIMER (VFW. h)
description: Il \_ messaggio MCIWNDM GETINACTIVETIMER Recupera il periodo di aggiornamento usato quando la finestra di MCIWnd è la finestra inattiva. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetInactiveTimer.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- MCIWNDM_GETINACTIVETIMER messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301080"
---
# <a name="mciwndm_getinactivetimer-message"></a><span data-ttu-id="e00ad-105">\_Messaggio MCIWNDM GETINACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="e00ad-105">MCIWNDM\_GETINACTIVETIMER message</span></span>

<span data-ttu-id="e00ad-106">Il messaggio **MCIWNDM \_ GETINACTIVETIMER** Recupera il periodo di aggiornamento usato quando la finestra di MCIWnd è la finestra inattiva.</span><span class="sxs-lookup"><span data-stu-id="e00ad-106">The **MCIWNDM\_GETINACTIVETIMER** message retrieves the update period used when the MCIWnd window is the inactive window.</span></span> <span data-ttu-id="e00ad-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="e00ad-107">You can send this message explicitly or by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span>


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e00ad-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e00ad-108">Return Value</span></span>

<span data-ttu-id="e00ad-109">Restituisce il periodo di aggiornamento, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="e00ad-109">Returns the update period, in milliseconds.</span></span> <span data-ttu-id="e00ad-110">Il valore predefinito è 2000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="e00ad-110">The default value is 2000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00ad-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e00ad-111">Requirements</span></span>



| <span data-ttu-id="e00ad-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e00ad-112">Requirement</span></span> | <span data-ttu-id="e00ad-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e00ad-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e00ad-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e00ad-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e00ad-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e00ad-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e00ad-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e00ad-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e00ad-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e00ad-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e00ad-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e00ad-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e00ad-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e00ad-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e00ad-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e00ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00ad-121">**MCIWndGetInactiveTimer**</span><span class="sxs-lookup"><span data-stu-id="e00ad-121">**MCIWndGetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





