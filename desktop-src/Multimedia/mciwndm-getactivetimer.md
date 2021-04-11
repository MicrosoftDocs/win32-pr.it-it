---
title: Messaggio di MCIWNDM_GETACTIVETIMER (VFW. h)
description: Il \_ messaggio MCIWNDM GETACTIVETIMER Recupera il periodo di aggiornamento usato quando la finestra di MCIWnd è la finestra attiva. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- MCIWNDM_GETACTIVETIMER messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121671"
---
# <a name="mciwndm_getactivetimer-message"></a><span data-ttu-id="98b17-105">\_Messaggio MCIWNDM GETACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="98b17-105">MCIWNDM\_GETACTIVETIMER message</span></span>

<span data-ttu-id="98b17-106">Il messaggio **MCIWNDM \_ GETACTIVETIMER** Recupera il periodo di aggiornamento usato quando la finestra di MCIWnd è la finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="98b17-106">The **MCIWNDM\_GETACTIVETIMER** message retrieves the update period used when the MCIWnd window is the active window.</span></span> <span data-ttu-id="98b17-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="98b17-107">You can send this message explicitly or by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span>


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="98b17-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98b17-108">Return Value</span></span>

<span data-ttu-id="98b17-109">Restituisce il periodo di aggiornamento in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="98b17-109">Returns the update period in milliseconds.</span></span> <span data-ttu-id="98b17-110">Il valore predefinito è 500 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="98b17-110">The default is 500 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="98b17-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98b17-111">Requirements</span></span>



| <span data-ttu-id="98b17-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="98b17-112">Requirement</span></span> | <span data-ttu-id="98b17-113">Valore</span><span class="sxs-lookup"><span data-stu-id="98b17-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="98b17-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98b17-114">Minimum supported client</span></span><br/> | <span data-ttu-id="98b17-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98b17-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="98b17-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98b17-116">Minimum supported server</span></span><br/> | <span data-ttu-id="98b17-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98b17-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="98b17-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98b17-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="98b17-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="98b17-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98b17-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98b17-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b17-121">**MCIWndGetActiveTimer**</span><span class="sxs-lookup"><span data-stu-id="98b17-121">**MCIWndGetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





