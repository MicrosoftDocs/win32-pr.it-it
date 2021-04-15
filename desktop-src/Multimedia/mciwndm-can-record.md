---
title: Messaggio di MCIWNDM_CAN_RECORD (VFW. h)
description: Il MCIWNDM \_ può \_ registrare il messaggio determina se un dispositivo MCI supporta la registrazione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndCanRecord.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- MCIWNDM_CAN_RECORD messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478719"
---
# <a name="mciwndm_can_record-message"></a><span data-ttu-id="68ded-105">MCIWNDM \_ può \_ registrare il messaggio</span><span class="sxs-lookup"><span data-stu-id="68ded-105">MCIWNDM\_CAN\_RECORD message</span></span>

<span data-ttu-id="68ded-106">Il **MCIWNDM \_ può \_ registrare** il messaggio determina se un dispositivo MCI supporta la registrazione.</span><span class="sxs-lookup"><span data-stu-id="68ded-106">The **MCIWNDM\_CAN\_RECORD** message determines if an MCI device supports recording.</span></span> <span data-ttu-id="68ded-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) .</span><span class="sxs-lookup"><span data-stu-id="68ded-107">You can send this message explicitly or by using the [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) macro.</span></span>


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="68ded-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68ded-108">Return Value</span></span>

<span data-ttu-id="68ded-109">Restituisce **true** se il dispositivo supporta la registrazione o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="68ded-109">Returns **TRUE** if the device supports recording or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="68ded-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68ded-110">Requirements</span></span>



| <span data-ttu-id="68ded-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="68ded-111">Requirement</span></span> | <span data-ttu-id="68ded-112">Valore</span><span class="sxs-lookup"><span data-stu-id="68ded-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="68ded-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68ded-113">Minimum supported client</span></span><br/> | <span data-ttu-id="68ded-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="68ded-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="68ded-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68ded-115">Minimum supported server</span></span><br/> | <span data-ttu-id="68ded-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="68ded-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="68ded-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68ded-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="68ded-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="68ded-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68ded-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68ded-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ded-120">**MCIWndCanRecord**</span><span class="sxs-lookup"><span data-stu-id="68ded-120">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





