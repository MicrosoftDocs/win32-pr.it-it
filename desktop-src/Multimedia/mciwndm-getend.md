---
title: Messaggio di MCIWNDM_GETEND (VFW. h)
description: Il \_ messaggio MCIWNDM GETEND recupera la posizione della fine del contenuto di un file o di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetEnd.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874453"
---
# <a name="mciwndm_getend-message"></a><span data-ttu-id="8991d-105">\_Messaggio MCIWNDM GETEND</span><span class="sxs-lookup"><span data-stu-id="8991d-105">MCIWNDM\_GETEND message</span></span>

<span data-ttu-id="8991d-106">Il messaggio **MCIWNDM \_ GETEND** recupera la posizione della fine del contenuto di un file o di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="8991d-106">The **MCIWNDM\_GETEND** message retrieves the location of the end of the content of an MCI device or file.</span></span> <span data-ttu-id="8991d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .</span><span class="sxs-lookup"><span data-stu-id="8991d-107">You can send this message explicitly or by using the [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macro.</span></span>


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="8991d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8991d-108">Return Value</span></span>

<span data-ttu-id="8991d-109">Restituisce la posizione nel formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="8991d-109">Returns the location in the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="8991d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8991d-110">Requirements</span></span>



| <span data-ttu-id="8991d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8991d-111">Requirement</span></span> | <span data-ttu-id="8991d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8991d-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8991d-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8991d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8991d-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8991d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8991d-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8991d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8991d-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8991d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8991d-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8991d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8991d-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8991d-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8991d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8991d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8991d-120">**MCIWndGetEnd**</span><span class="sxs-lookup"><span data-stu-id="8991d-120">**MCIWndGetEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





