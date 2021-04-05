---
title: Messaggio di ICM_DRAW_END (VFW. h)
description: Il \_ messaggio di \_ fine disegno ICM notifica a un driver di rendering di decomprimere l'immagine corrente sullo schermo e di rilasciare le risorse allocate per la decompressione e il disegno. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- ICM_DRAW_END messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741962"
---
# <a name="icm_draw_end-message"></a><span data-ttu-id="5c9a7-105">\_Messaggio finale di disegnato ICM \_</span><span class="sxs-lookup"><span data-stu-id="5c9a7-105">ICM\_DRAW\_END message</span></span>

<span data-ttu-id="5c9a7-106">Il messaggio di **\_ \_ fine disegno ICM** notifica a un driver di rendering di decomprimere l'immagine corrente sullo schermo e di rilasciare le risorse allocate per la decompressione e il disegno.</span><span class="sxs-lookup"><span data-stu-id="5c9a7-106">The **ICM\_DRAW\_END** message notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing.</span></span> <span data-ttu-id="5c9a7-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .</span><span class="sxs-lookup"><span data-stu-id="5c9a7-107">You can send this message explicitly or by using the [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) macro.</span></span>


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="5c9a7-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c9a7-108">Return Value</span></span>

<span data-ttu-id="5c9a7-109">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5c9a7-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c9a7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c9a7-110">Remarks</span></span>

<span data-ttu-id="5c9a7-111">I messaggi di [**\_ \_ inizio**](icm-draw-begin.md) e **di \_ \_ fine progetto** ICM non nidificano.</span><span class="sxs-lookup"><span data-stu-id="5c9a7-111">The [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) and **ICM\_DRAW\_END** messages do not nest.</span></span> <span data-ttu-id="5c9a7-112">Se il driver riceve **l' \_ \_ inizio dell'estrazione ICM** prima che la decompressione venga arrestata con la **\_ \_ fine del progetto ICM**, dovrebbe riavviare la decompressione con nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="5c9a7-112">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c9a7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c9a7-113">Requirements</span></span>



| <span data-ttu-id="5c9a7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c9a7-114">Requirement</span></span> | <span data-ttu-id="5c9a7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5c9a7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5c9a7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c9a7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5c9a7-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c9a7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5c9a7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c9a7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5c9a7-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c9a7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5c9a7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c9a7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c9a7-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c9a7-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c9a7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c9a7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9a7-123">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="5c9a7-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="5c9a7-124">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="5c9a7-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





