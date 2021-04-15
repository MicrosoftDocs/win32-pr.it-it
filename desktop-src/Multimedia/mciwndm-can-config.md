---
title: Messaggio di MCIWNDM_CAN_CONFIG (VFW. h)
description: Il messaggio di configurazione MCIWNDM \_ può \_ determinare se un dispositivo MCI può visualizzare una finestra di dialogo di configurazione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- MCIWNDM_CAN_CONFIG messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479138"
---
# <a name="mciwndm_can_config-message"></a><span data-ttu-id="57d66-105">MCIWNDM è in \_ grado di \_ configurare il messaggio</span><span class="sxs-lookup"><span data-stu-id="57d66-105">MCIWNDM\_CAN\_CONFIG message</span></span>

<span data-ttu-id="57d66-106">Il messaggio di configurazione **MCIWNDM \_ può \_** determinare se un dispositivo MCI può visualizzare una finestra di dialogo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="57d66-106">The **MCIWNDM\_CAN\_CONFIG** message determines if an MCI device can display a configuration dialog box.</span></span> <span data-ttu-id="57d66-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) .</span><span class="sxs-lookup"><span data-stu-id="57d66-107">You can send this message explicitly or by using the [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) macro.</span></span>


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="57d66-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57d66-108">Return Value</span></span>

<span data-ttu-id="57d66-109">Restituisce **true** se il dispositivo supporta la configurazione o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="57d66-109">Returns **TRUE** if the device supports configuration or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="57d66-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57d66-110">Requirements</span></span>



| <span data-ttu-id="57d66-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="57d66-111">Requirement</span></span> | <span data-ttu-id="57d66-112">Valore</span><span class="sxs-lookup"><span data-stu-id="57d66-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57d66-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57d66-113">Minimum supported client</span></span><br/> | <span data-ttu-id="57d66-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="57d66-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="57d66-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57d66-115">Minimum supported server</span></span><br/> | <span data-ttu-id="57d66-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="57d66-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="57d66-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57d66-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="57d66-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="57d66-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57d66-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57d66-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57d66-120">**MCIWndCanConfig**</span><span class="sxs-lookup"><span data-stu-id="57d66-120">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





