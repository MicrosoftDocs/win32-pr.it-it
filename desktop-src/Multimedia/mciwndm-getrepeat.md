---
title: Messaggio di MCIWNDM_GETREPEAT (VFW. h)
description: Il \_ messaggio GETREPEAT MCIWNDM determina se la riproduzione continua è stata attivata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetRepeat.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- MCIWNDM_GETREPEAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef47dc4f639c7aa34f7a00341e6ad2e19be909d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119155"
---
# <a name="mciwndm_getrepeat-message"></a><span data-ttu-id="2a222-105">\_Messaggio GETREPEAT MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="2a222-105">MCIWNDM\_GETREPEAT message</span></span>

<span data-ttu-id="2a222-106">Il **messaggio \_ getRepeat MCIWNDM** determina se la riproduzione continua è stata attivata.</span><span class="sxs-lookup"><span data-stu-id="2a222-106">The **MCIWNDM\_GETREPEAT** message determines if continuous playback has been activated.</span></span> <span data-ttu-id="2a222-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .</span><span class="sxs-lookup"><span data-stu-id="2a222-107">You can send this message explicitly or by using the [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) macro.</span></span>


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="2a222-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a222-108">Return Value</span></span>

<span data-ttu-id="2a222-109">Restituisce **true** se la riproduzione continua è attivata o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2a222-109">Returns **TRUE** if continuous playback is activated or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a222-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a222-110">Requirements</span></span>



| <span data-ttu-id="2a222-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a222-111">Requirement</span></span> | <span data-ttu-id="2a222-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2a222-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a222-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a222-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2a222-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a222-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2a222-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a222-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2a222-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a222-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2a222-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a222-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a222-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a222-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a222-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a222-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a222-120">**MCIWndGetRepeat**</span><span class="sxs-lookup"><span data-stu-id="2a222-120">**MCIWndGetRepeat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





