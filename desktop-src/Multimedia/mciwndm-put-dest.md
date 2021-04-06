---
title: Messaggio di MCIWNDM_PUT_DEST (VFW. h)
description: Il \_ \_ messaggio dest MCIWNDM put ridefinisce le coordinate del rettangolo di destinazione usato per lo zoom o l'estensione delle immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndPutDest.
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- MCIWNDM_PUT_DEST messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742951"
---
# <a name="mciwndm_put_dest-message"></a><span data-ttu-id="d95bb-105">MCIWNDM \_ put \_ messaggio dest</span><span class="sxs-lookup"><span data-stu-id="d95bb-105">MCIWNDM\_PUT\_DEST message</span></span>

<span data-ttu-id="d95bb-106">Il **messaggio \_ \_ dest MCIWNDM put** ridefinisce le coordinate del rettangolo di destinazione usato per lo zoom o l'estensione delle immagini di un file AVI durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="d95bb-106">The **MCIWNDM\_PUT\_DEST** message redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="d95bb-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .</span><span class="sxs-lookup"><span data-stu-id="d95bb-107">You can send this message explicitly or by using the [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macro.</span></span>


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="d95bb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d95bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d95bb-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="d95bb-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="d95bb-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) contenente le coordinate del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d95bb-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure containing the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d95bb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d95bb-111">Return Value</span></span>

<span data-ttu-id="d95bb-112">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="d95bb-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d95bb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d95bb-113">Requirements</span></span>



| <span data-ttu-id="d95bb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d95bb-114">Requirement</span></span> | <span data-ttu-id="d95bb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d95bb-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d95bb-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d95bb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d95bb-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d95bb-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d95bb-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d95bb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d95bb-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d95bb-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d95bb-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d95bb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d95bb-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d95bb-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d95bb-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d95bb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d95bb-123">**MCIWndPutDest**</span><span class="sxs-lookup"><span data-stu-id="d95bb-123">**MCIWndPutDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

