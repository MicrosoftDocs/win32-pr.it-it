---
title: Messaggio di MCIWNDM_EJECT (VFW. h)
description: Il \_ messaggio MCIWNDM EJECT Invia un comando a un dispositivo MCI per espellerne i supporti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndEject.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400356"
---
# <a name="mciwndm_eject-message"></a><span data-ttu-id="f6ca5-105">\_Messaggio di espulsione MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="f6ca5-105">MCIWNDM\_EJECT message</span></span>

<span data-ttu-id="f6ca5-106">Il messaggio **MCIWNDM \_ eject** Invia un comando a un dispositivo MCI per espellerne i supporti.</span><span class="sxs-lookup"><span data-stu-id="f6ca5-106">The **MCIWNDM\_EJECT** message sends a command to an MCI device to eject its media.</span></span> <span data-ttu-id="f6ca5-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) .</span><span class="sxs-lookup"><span data-stu-id="f6ca5-107">You can send this message explicitly or by using the [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) macro.</span></span>


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="f6ca5-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6ca5-108">Return Value</span></span>

<span data-ttu-id="f6ca5-109">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="f6ca5-109">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6ca5-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6ca5-110">Requirements</span></span>



| <span data-ttu-id="f6ca5-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6ca5-111">Requirement</span></span> | <span data-ttu-id="f6ca5-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f6ca5-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f6ca5-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6ca5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f6ca5-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6ca5-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f6ca5-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6ca5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f6ca5-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6ca5-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f6ca5-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6ca5-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6ca5-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6ca5-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6ca5-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6ca5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ca5-120">**MCIWndEject**</span><span class="sxs-lookup"><span data-stu-id="f6ca5-120">**MCIWndEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





