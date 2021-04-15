---
title: Messaggio di ICM_COMPRESS_END (VFW. h)
description: Il \_ \_ messaggio di fine compressione ICM notifica a un driver di compressione video di terminare la compressione e liberare le risorse allocate per la compressione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476007"
---
# <a name="icm_compress_end-message"></a><span data-ttu-id="44978-105">\_ \_ Messaggio finale compresso ICM</span><span class="sxs-lookup"><span data-stu-id="44978-105">ICM\_COMPRESS\_END message</span></span>

<span data-ttu-id="44978-106">Il messaggio di **\_ \_ fine compressione ICM** notifica a un driver di compressione video di terminare la compressione e liberare le risorse allocate per la compressione.</span><span class="sxs-lookup"><span data-stu-id="44978-106">The **ICM\_COMPRESS\_END** message notifies a video compression driver to end compression and free resources allocated for compression.</span></span> <span data-ttu-id="44978-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .</span><span class="sxs-lookup"><span data-stu-id="44978-107">You can send this message explicitly or by using the [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) macro.</span></span>


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="44978-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44978-108">Return Value</span></span>

<span data-ttu-id="44978-109">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="44978-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="44978-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="44978-110">Remarks</span></span>

<span data-ttu-id="44978-111">VCM Salva le impostazioni del messaggio di [**inizio della \_ compressione \_ ICM**](icm-compress-begin.md) più recente.</span><span class="sxs-lookup"><span data-stu-id="44978-111">VCM saves the settings of the most recent [**ICM\_COMPRESS\_BEGIN**](icm-compress-begin.md) message.</span></span> <span data-ttu-id="44978-112">**ICM \_ COMPRESS \_ Begin** e **MCI \_ compress \_ end** non nidificano.</span><span class="sxs-lookup"><span data-stu-id="44978-112">**ICM\_COMPRESS\_BEGIN** and **ICM\_COMPRESS\_END** do not nest.</span></span> <span data-ttu-id="44978-113">Se il driver riceve **l' \_ \_ inizio** della compressione ICM prima che la compressione venga arrestata con la **\_ \_ fine** della compressione MCI, dovrebbe riavviare la compressione con i nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="44978-113">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="44978-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44978-114">Requirements</span></span>



| <span data-ttu-id="44978-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="44978-115">Requirement</span></span> | <span data-ttu-id="44978-116">Valore</span><span class="sxs-lookup"><span data-stu-id="44978-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="44978-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44978-117">Minimum supported client</span></span><br/> | <span data-ttu-id="44978-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="44978-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="44978-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44978-119">Minimum supported server</span></span><br/> | <span data-ttu-id="44978-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="44978-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="44978-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44978-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="44978-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="44978-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44978-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44978-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44978-124">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="44978-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="44978-125">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="44978-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





