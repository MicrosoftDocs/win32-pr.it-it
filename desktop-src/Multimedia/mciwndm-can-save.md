---
title: Messaggio di MCIWNDM_CAN_SAVE (VFW. h)
description: Il MCIWNDM \_ può \_ salvare il messaggio determina se un dispositivo MCI può salvare i dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanSave.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475682"
---
# <a name="mciwndm_can_save-message"></a><span data-ttu-id="c8c70-105">MCIWNDM \_ consente di \_ salvare il messaggio</span><span class="sxs-lookup"><span data-stu-id="c8c70-105">MCIWNDM\_CAN\_SAVE message</span></span>

<span data-ttu-id="c8c70-106">Il **MCIWNDM \_ può \_ salvare** il messaggio determina se un dispositivo MCI può salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="c8c70-106">The **MCIWNDM\_CAN\_SAVE** message determines if an MCI device can save data.</span></span> <span data-ttu-id="c8c70-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) .</span><span class="sxs-lookup"><span data-stu-id="c8c70-107">You can send this message explicitly or by using the [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) macro.</span></span>


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="c8c70-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8c70-108">Return Value</span></span>

<span data-ttu-id="c8c70-109">Restituisce **true** se il dispositivo supporta il salvataggio o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c8c70-109">Returns **TRUE** if the device supports saving or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c70-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8c70-110">Requirements</span></span>



| <span data-ttu-id="c8c70-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8c70-111">Requirement</span></span> | <span data-ttu-id="c8c70-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c8c70-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c8c70-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8c70-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c8c70-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8c70-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c8c70-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8c70-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c8c70-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8c70-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c8c70-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8c70-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8c70-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8c70-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8c70-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8c70-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8c70-120">**MCIWndCanSave**</span><span class="sxs-lookup"><span data-stu-id="c8c70-120">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





