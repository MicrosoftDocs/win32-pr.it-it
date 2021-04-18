---
title: Messaggio di MCIWNDM_GETSTYLES (VFW. h)
description: Il \_ messaggio MCIWNDM GETstyles recupera i flag che specificano gli stili correnti della finestra MCIWnd usati da una finestra. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetStyles.
ms.assetid: cd34ba05-47cb-488e-a6c6-4ec1c0d25de8
keywords:
- MCIWNDM_GETSTYLES messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 983e37291977edf2473c2b603cd5b40792fb7989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302508"
---
# <a name="mciwndm_getstyles-message"></a><span data-ttu-id="5024c-105">\_Messaggio GETstyles MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="5024c-105">MCIWNDM\_GETSTYLES message</span></span>

<span data-ttu-id="5024c-106">Il messaggio **MCIWNDM \_ GetStyles** recupera i flag che specificano gli stili correnti della finestra MCIWnd usati da una finestra.</span><span class="sxs-lookup"><span data-stu-id="5024c-106">The **MCIWNDM\_GETSTYLES** message retrieves the flags specifying the current MCIWnd window styles used by a window.</span></span> <span data-ttu-id="5024c-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .</span><span class="sxs-lookup"><span data-stu-id="5024c-107">You can send this message explicitly or by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>


```C++
MCIWNDM_GETSTYLES 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="5024c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5024c-108">Return Value</span></span>

<span data-ttu-id="5024c-109">Restituisce un valore che rappresenta gli stili correnti della finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="5024c-109">Returns a value representing the current styles of the MCIWnd window.</span></span> <span data-ttu-id="5024c-110">Il valore restituito è l'operatore OR bit per bit degli stili della finestra MCIWnd (flag MCIWNDF).</span><span class="sxs-lookup"><span data-stu-id="5024c-110">The return value is the bitwise OR operator of the MCIWnd window styles (MCIWNDF flags).</span></span>

## <a name="requirements"></a><span data-ttu-id="5024c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5024c-111">Requirements</span></span>



| <span data-ttu-id="5024c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5024c-112">Requirement</span></span> | <span data-ttu-id="5024c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="5024c-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5024c-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5024c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5024c-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5024c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5024c-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5024c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5024c-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5024c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5024c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5024c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5024c-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5024c-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5024c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5024c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5024c-121">**MCIWndGetStyles**</span><span class="sxs-lookup"><span data-stu-id="5024c-121">**MCIWndGetStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
</dt> </dl>

 

 





