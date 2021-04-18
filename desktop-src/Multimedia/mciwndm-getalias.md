---
title: Messaggio di MCIWNDM_GETALIAS (VFW. h)
description: Il \_ messaggio MCIWNDM getAlias recupera l'alias utilizzato per aprire un file o un dispositivo MCI con la funzione mciSendString. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetAlias.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- MCIWNDM_GETALIAS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e971c50b9abc450387ac29f9a7331bfdca5c38c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301081"
---
# <a name="mciwndm_getalias-message"></a><span data-ttu-id="91966-105">\_Messaggio GETALIAS MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="91966-105">MCIWNDM\_GETALIAS message</span></span>

<span data-ttu-id="91966-106">Il messaggio **MCIWNDM \_ getAlias** recupera l'alias utilizzato per aprire un file o un dispositivo MCI con la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="91966-106">The **MCIWNDM\_GETALIAS** message retrieves the alias used to open an MCI device or file with the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="91966-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .</span><span class="sxs-lookup"><span data-stu-id="91966-107">You can send this message explicitly or by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span>


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="91966-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91966-108">Return Value</span></span>

<span data-ttu-id="91966-109">Restituisce l'alias del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91966-109">Returns the device alias.</span></span>

## <a name="requirements"></a><span data-ttu-id="91966-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91966-110">Requirements</span></span>



| <span data-ttu-id="91966-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="91966-111">Requirement</span></span> | <span data-ttu-id="91966-112">Valore</span><span class="sxs-lookup"><span data-stu-id="91966-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="91966-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91966-113">Minimum supported client</span></span><br/> | <span data-ttu-id="91966-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91966-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="91966-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91966-115">Minimum supported server</span></span><br/> | <span data-ttu-id="91966-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91966-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="91966-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91966-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="91966-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="91966-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91966-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91966-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="91966-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91966-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="91966-121">**MCIWndGetAlias**</span><span class="sxs-lookup"><span data-stu-id="91966-121">**MCIWndGetAlias**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

