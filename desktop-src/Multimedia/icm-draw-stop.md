---
title: Messaggio di ICM_DRAW_STOP (VFW. h)
description: Il messaggio di arresto del disegno ICM \_ \_ notifica a un driver di rendering di arrestare il clock interno per la tempistica di disegno dei frame. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476246"
---
# <a name="icm_draw_stop-message"></a><span data-ttu-id="87694-105">Messaggio di arresto del \_ progetto ICM \_</span><span class="sxs-lookup"><span data-stu-id="87694-105">ICM\_DRAW\_STOP message</span></span>

<span data-ttu-id="87694-106">Il messaggio di **\_ \_ arresto** del disegno ICM notifica a un driver di rendering di arrestare il clock interno per la tempistica di disegno dei frame.</span><span class="sxs-lookup"><span data-stu-id="87694-106">The **ICM\_DRAW\_STOP** message notifies a rendering driver to stop its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="87694-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) .</span><span class="sxs-lookup"><span data-stu-id="87694-107">You can send this message explicitly or by using the [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) macro.</span></span>


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="87694-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87694-108">Return Value</span></span>

<span data-ttu-id="87694-109">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="87694-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87694-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="87694-110">Remarks</span></span>

<span data-ttu-id="87694-111">Questo messaggio viene usato dall'hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.</span><span class="sxs-lookup"><span data-stu-id="87694-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="87694-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87694-112">Requirements</span></span>



| <span data-ttu-id="87694-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="87694-113">Requirement</span></span> | <span data-ttu-id="87694-114">Valore</span><span class="sxs-lookup"><span data-stu-id="87694-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="87694-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87694-115">Minimum supported client</span></span><br/> | <span data-ttu-id="87694-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87694-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="87694-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87694-117">Minimum supported server</span></span><br/> | <span data-ttu-id="87694-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87694-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="87694-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87694-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="87694-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="87694-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87694-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87694-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87694-122">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="87694-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="87694-123">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="87694-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





