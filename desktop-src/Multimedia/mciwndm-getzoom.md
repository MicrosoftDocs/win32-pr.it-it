---
title: Messaggio di MCIWNDM_GETZOOM (VFW. h)
description: Il \_ messaggio MCIWNDM getzoom Recupera il valore di zoom corrente usato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- MCIWNDM_GETZOOM messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476228"
---
# <a name="mciwndm_getzoom-message"></a><span data-ttu-id="16087-105">\_Messaggio GETZOOM MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="16087-105">MCIWNDM\_GETZOOM message</span></span>

<span data-ttu-id="16087-106">Il messaggio **MCIWNDM \_ getzoom** Recupera il valore di zoom corrente usato da un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="16087-106">The **MCIWNDM\_GETZOOM** message retrieves the current zoom value used by an MCI device.</span></span> <span data-ttu-id="16087-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .</span><span class="sxs-lookup"><span data-stu-id="16087-107">You can send this message explicitly or by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span>


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="16087-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16087-108">Return Value</span></span>

<span data-ttu-id="16087-109">Restituisce i valori più recenti utilizzati con [**MCIWNDM \_ sezoom**](mciwndm-setzoom.md).</span><span class="sxs-lookup"><span data-stu-id="16087-109">Returns the most recent values used with [**MCIWNDM\_SETZOOM**](mciwndm-setzoom.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="16087-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="16087-110">Remarks</span></span>

<span data-ttu-id="16087-111">Il valore restituito 100 indica che l'immagine non è ingrandita.</span><span class="sxs-lookup"><span data-stu-id="16087-111">A return value of 100 indicates the image is not zoomed.</span></span> <span data-ttu-id="16087-112">Il valore 200 indica che l'immagine viene ingrandita in base al doppio delle dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="16087-112">A value of 200 indicates the image is enlarged to twice its original size.</span></span> <span data-ttu-id="16087-113">Il valore 50 indica che l'immagine è ridotta a metà delle dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="16087-113">A value of 50 indicates the image is reduced to half its original size.</span></span>

## <a name="requirements"></a><span data-ttu-id="16087-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16087-114">Requirements</span></span>



| <span data-ttu-id="16087-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="16087-115">Requirement</span></span> | <span data-ttu-id="16087-116">Valore</span><span class="sxs-lookup"><span data-stu-id="16087-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="16087-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16087-117">Minimum supported client</span></span><br/> | <span data-ttu-id="16087-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="16087-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="16087-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16087-119">Minimum supported server</span></span><br/> | <span data-ttu-id="16087-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="16087-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="16087-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16087-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="16087-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="16087-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16087-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16087-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16087-124">**MCIWndGetZoom**</span><span class="sxs-lookup"><span data-stu-id="16087-124">**MCIWndGetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[<span data-ttu-id="16087-125">**MCIWNDM- \_ Zoom**</span><span class="sxs-lookup"><span data-stu-id="16087-125">**MCIWNDM\_SETZOOM**</span></span>](mciwndm-setzoom.md)
</dt> </dl>

 

 





