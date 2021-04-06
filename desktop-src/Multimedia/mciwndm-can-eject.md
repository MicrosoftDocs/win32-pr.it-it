---
title: Messaggio di MCIWNDM_CAN_EJECT (VFW. h)
description: MCIWNDM \_ può \_ rimuovere il messaggio determina se un dispositivo MCI può espellerne i supporti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanEject.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743687"
---
# <a name="mciwndm_can_eject-message"></a><span data-ttu-id="f0656-105">MCIWNDM \_ può \_ rimuovere il messaggio</span><span class="sxs-lookup"><span data-stu-id="f0656-105">MCIWNDM\_CAN\_EJECT message</span></span>

<span data-ttu-id="f0656-106">**MCIWNDM \_ può \_ rimuovere** il messaggio determina se un dispositivo MCI può espellerne i supporti.</span><span class="sxs-lookup"><span data-stu-id="f0656-106">The **MCIWNDM\_CAN\_EJECT** message determines if an MCI device can eject its media.</span></span> <span data-ttu-id="f0656-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) .</span><span class="sxs-lookup"><span data-stu-id="f0656-107">You can send this message explicitly or by using the [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) macro.</span></span>


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="f0656-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0656-108">Return Value</span></span>

<span data-ttu-id="f0656-109">Restituisce **true** se il dispositivo può espellere il relativo supporto o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f0656-109">Returns **TRUE** if the device can eject its media or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0656-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0656-110">Requirements</span></span>



| <span data-ttu-id="f0656-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0656-111">Requirement</span></span> | <span data-ttu-id="f0656-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f0656-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f0656-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0656-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f0656-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f0656-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f0656-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0656-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f0656-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f0656-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f0656-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0656-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0656-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0656-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0656-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0656-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0656-120">**MCIWndCanEject**</span><span class="sxs-lookup"><span data-stu-id="f0656-120">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





