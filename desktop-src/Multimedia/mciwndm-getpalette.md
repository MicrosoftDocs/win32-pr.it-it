---
title: Messaggio di MCIWNDM_GETPALETTE (VFW. h)
description: Il \_ messaggio MCIWNDM getPalette recupera un handle della tavolozza utilizzata da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetPalette.
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- MCIWNDM_GETPALETTE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047972"
---
# <a name="mciwndm_getpalette-message"></a><span data-ttu-id="1921e-105">\_Messaggio GETtavolozza MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="1921e-105">MCIWNDM\_GETPALETTE message</span></span>

<span data-ttu-id="1921e-106">Il messaggio **MCIWNDM \_ getPalette** recupera un handle della tavolozza utilizzata da un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="1921e-106">The **MCIWNDM\_GETPALETTE** message retrieves a handle of the palette used by an MCI device.</span></span> <span data-ttu-id="1921e-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="1921e-107">You can send this message explicitly or by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span>


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="1921e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1921e-108">Return Value</span></span>

<span data-ttu-id="1921e-109">Restituisce l'handle della tavolozza in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1921e-109">Returns the handle of the palette if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="1921e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1921e-110">Requirements</span></span>



| <span data-ttu-id="1921e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1921e-111">Requirement</span></span> | <span data-ttu-id="1921e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="1921e-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1921e-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1921e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1921e-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1921e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1921e-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1921e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1921e-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1921e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1921e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1921e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1921e-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1921e-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1921e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1921e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1921e-120">**MCIWndGetPalette**</span><span class="sxs-lookup"><span data-stu-id="1921e-120">**MCIWndGetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





