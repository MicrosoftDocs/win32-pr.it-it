---
title: Messaggio di ICM_DRAW_START (VFW. h)
description: Il \_ \_ messaggio di avvio del disegno ICM notifica a un driver di rendering di avviare il clock interno per la tempistica di disegno dei frame. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400536"
---
# <a name="icm_draw_start-message"></a><span data-ttu-id="45685-105">Messaggio di avvio del \_ progetto ICM \_</span><span class="sxs-lookup"><span data-stu-id="45685-105">ICM\_DRAW\_START message</span></span>

<span data-ttu-id="45685-106">Il messaggio di **\_ \_ avvio del disegno ICM** notifica a un driver di rendering di avviare il clock interno per la tempistica di disegno dei frame.</span><span class="sxs-lookup"><span data-stu-id="45685-106">The **ICM\_DRAW\_START** message notifies a rendering driver to start its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="45685-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .</span><span class="sxs-lookup"><span data-stu-id="45685-107">You can send this message explicitly or by using the [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) macro.</span></span>


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="45685-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45685-108">Return Value</span></span>

<span data-ttu-id="45685-109">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="45685-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45685-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="45685-110">Remarks</span></span>

<span data-ttu-id="45685-111">Questo messaggio viene usato dall'hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.</span><span class="sxs-lookup"><span data-stu-id="45685-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="45685-112">Quando il driver riceve questo messaggio, deve iniziare a eseguire il rendering dei dati alla velocità specificata con il messaggio di [**\_ \_ inizio del progetto ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="45685-112">When the driver receives this message, it should start rendering data at the rate specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="45685-113">I messaggi di **\_ \_ avvio** e [**di \_ \_ arresto del progetto**](icm-draw-stop.md) ICM non vengono annidati.</span><span class="sxs-lookup"><span data-stu-id="45685-113">The **ICM\_DRAW\_START** and [**ICM\_DRAW\_STOP**](icm-draw-stop.md) messages do not nest.</span></span> <span data-ttu-id="45685-114">Se il driver riceve **l' \_ \_ avvio del progetto ICM** prima che il rendering venga interrotto con l' **\_ \_ arresto del progetto ICM**, dovrebbe riavviare il rendering con nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="45685-114">If your driver receives **ICM\_DRAW\_START** before rendering is stopped with **ICM\_DRAW\_STOP**, it should restart rendering with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="45685-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45685-115">Requirements</span></span>



| <span data-ttu-id="45685-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="45685-116">Requirement</span></span> | <span data-ttu-id="45685-117">Valore</span><span class="sxs-lookup"><span data-stu-id="45685-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="45685-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45685-118">Minimum supported client</span></span><br/> | <span data-ttu-id="45685-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45685-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="45685-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45685-120">Minimum supported server</span></span><br/> | <span data-ttu-id="45685-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45685-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="45685-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45685-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="45685-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="45685-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45685-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45685-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45685-125">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="45685-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="45685-126">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="45685-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





