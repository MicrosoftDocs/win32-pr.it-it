---
title: Messaggio di MCIWNDM_CAN_WINDOW (VFW. h)
description: Il \_ messaggio della finestra MCIWNDM può \_ determinare se un dispositivo MCI supporta i comandi MCI orientati a finestre. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanWindow.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- MCIWNDM_CAN_WINDOW messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964098"
---
# <a name="mciwndm_can_window-message"></a><span data-ttu-id="0f392-105">MCIWNDM \_ può \_ messaggio finestra</span><span class="sxs-lookup"><span data-stu-id="0f392-105">MCIWNDM\_CAN\_WINDOW message</span></span>

<span data-ttu-id="0f392-106">Il messaggio della **\_ \_ finestra MCIWNDM può** determinare se un dispositivo MCI supporta i comandi MCI orientati a finestre.</span><span class="sxs-lookup"><span data-stu-id="0f392-106">The **MCIWNDM\_CAN\_WINDOW** message determines if an MCI device supports window-oriented MCI commands.</span></span> <span data-ttu-id="0f392-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) .</span><span class="sxs-lookup"><span data-stu-id="0f392-107">You can send this message explicitly or by using the [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) macro.</span></span>


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="0f392-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f392-108">Return Value</span></span>

<span data-ttu-id="0f392-109">Restituisce **true** se il dispositivo supporta i comandi MCI orientati alla finestra o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0f392-109">Returns **TRUE** if the device supports window-oriented MCI commands or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f392-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f392-110">Requirements</span></span>



| <span data-ttu-id="0f392-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f392-111">Requirement</span></span> | <span data-ttu-id="0f392-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0f392-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0f392-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f392-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0f392-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f392-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0f392-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f392-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0f392-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f392-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0f392-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f392-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f392-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f392-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f392-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f392-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f392-120">**MCIWndCanWindow**</span><span class="sxs-lookup"><span data-stu-id="0f392-120">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





