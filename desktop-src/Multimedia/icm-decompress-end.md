---
title: Messaggio di ICM_DECOMPRESS_END (VFW. h)
description: Il \_ \_ messaggio di fine decompressione ICM notifica a un driver di decompressione video di terminare la decompressione e liberare le risorse allocate per la decompressione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742970"
---
# <a name="icm_decompress_end-message"></a><span data-ttu-id="068cf-105">\_Messaggio finale di decompressione ICM \_</span><span class="sxs-lookup"><span data-stu-id="068cf-105">ICM\_DECOMPRESS\_END message</span></span>

<span data-ttu-id="068cf-106">Il messaggio di **\_ \_ fine** decompressione ICM notifica a un driver di decompressione video di terminare la decompressione e liberare le risorse allocate per la decompressione.</span><span class="sxs-lookup"><span data-stu-id="068cf-106">The **ICM\_DECOMPRESS\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="068cf-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .</span><span class="sxs-lookup"><span data-stu-id="068cf-107">You can send this message explicitly or by using the [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) macro.</span></span>


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="068cf-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="068cf-108">Return Value</span></span>

<span data-ttu-id="068cf-109">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="068cf-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="068cf-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="068cf-110">Remarks</span></span>

<span data-ttu-id="068cf-111">Il driver deve liberare tutte le risorse allocate per il messaggio di [**\_ \_ inizio della decompressione ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="068cf-111">The driver should free any resources allocated for the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="068cf-112">[**ICM \_ Decomprimi \_ Begin**](icm-decompress-begin.md) e **MCI \_ Decompress \_ end** non nidificano.</span><span class="sxs-lookup"><span data-stu-id="068cf-112">[**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) and **ICM\_DECOMPRESS\_END** do not nest.</span></span> <span data-ttu-id="068cf-113">Se il driver riceve la decompressione **MCI \_ \_ inizia** prima che la decompressione venga interrotta con la **\_ \_ terminazione MCI decomprimere**, deve riavviare la decompressione con nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="068cf-113">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="068cf-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="068cf-114">Requirements</span></span>



| <span data-ttu-id="068cf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="068cf-115">Requirement</span></span> | <span data-ttu-id="068cf-116">Valore</span><span class="sxs-lookup"><span data-stu-id="068cf-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="068cf-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="068cf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="068cf-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="068cf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="068cf-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="068cf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="068cf-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="068cf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="068cf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="068cf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="068cf-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="068cf-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="068cf-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="068cf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068cf-124">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="068cf-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="068cf-125">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="068cf-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





