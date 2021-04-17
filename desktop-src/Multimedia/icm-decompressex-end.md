---
title: Messaggio di ICM_DECOMPRESSEX_END (VFW. h)
description: Il \_ \_ messaggio di fine DECOMPRESSEX ICM notifica a un driver di decompressione video di terminare la decompressione e liberare le risorse allocate per la decompressione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressExEnd.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- ICM_DECOMPRESSEX_END messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518640"
---
# <a name="icm_decompressex_end-message"></a><span data-ttu-id="cec55-105">\_ \_ Messaggio finale DECOMPRESSEX ICM</span><span class="sxs-lookup"><span data-stu-id="cec55-105">ICM\_DECOMPRESSEX\_END message</span></span>

<span data-ttu-id="cec55-106">Il messaggio di **\_ \_ fine DECOMPRESSEX ICM** notifica a un driver di decompressione video di terminare la decompressione e liberare le risorse allocate per la decompressione.</span><span class="sxs-lookup"><span data-stu-id="cec55-106">The **ICM\_DECOMPRESSEX\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="cec55-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) .</span><span class="sxs-lookup"><span data-stu-id="cec55-107">You can send this message explicitly or by using the [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) macro.</span></span>


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="cec55-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cec55-108">Return Value</span></span>

<span data-ttu-id="cec55-109">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cec55-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cec55-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cec55-110">Remarks</span></span>

<span data-ttu-id="cec55-111">Il driver libera tutte le risorse allocate per il messaggio di [**\_ \_ inizio DECOMPRESSEX ICM**](icm-decompressex-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="cec55-111">The driver frees any resources allocated for the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

<span data-ttu-id="cec55-112">[**ICM \_ DECOMPRESSEX \_ Begin**](icm-decompressex-begin.md) e **ICM \_ DECOMPRESSEX \_ end** non nidificano.</span><span class="sxs-lookup"><span data-stu-id="cec55-112">[**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) and **ICM\_DECOMPRESSEX\_END** do not nest.</span></span> <span data-ttu-id="cec55-113">Se il driver riceve **la \_ DECOMPRESSEX MCI \_ iniziare** prima che la decompressione venga interrotta con la **\_ \_ fine di DECOMPRESSEX ICM**, dovrebbe riavviare la decompressione con nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="cec55-113">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec55-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cec55-114">Requirements</span></span>



| <span data-ttu-id="cec55-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cec55-115">Requirement</span></span> | <span data-ttu-id="cec55-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cec55-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cec55-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cec55-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cec55-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cec55-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cec55-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cec55-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cec55-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cec55-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cec55-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cec55-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cec55-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cec55-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cec55-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cec55-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec55-124">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="cec55-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="cec55-125">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="cec55-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





