---
title: Messaggio di ICM_DRAW_FLUSH (VFW. h)
description: Il \_ messaggio di \_ SCARICAmento ICM invia una notifica a un driver di rendering per eseguire il rendering del contenuto di tutti i buffer di immagine in attesa di essere disegnati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawFlush.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- ICM_DRAW_FLUSH messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301826"
---
# <a name="icm_draw_flush-message"></a><span data-ttu-id="d10da-105">\_Messaggio di \_ scaricamento del progetto ICM</span><span class="sxs-lookup"><span data-stu-id="d10da-105">ICM\_DRAW\_FLUSH message</span></span>

<span data-ttu-id="d10da-106">Il messaggio di **\_ \_ scaricamento ICM** invia una notifica a un driver di rendering per eseguire il rendering del contenuto di tutti i buffer di immagine in attesa di essere disegnati.</span><span class="sxs-lookup"><span data-stu-id="d10da-106">The **ICM\_DRAW\_FLUSH** message notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn.</span></span> <span data-ttu-id="d10da-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) .</span><span class="sxs-lookup"><span data-stu-id="d10da-107">You can send this message explicitly or by using the [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) macro.</span></span>


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="d10da-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d10da-108">Return Value</span></span>

<span data-ttu-id="d10da-109">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d10da-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d10da-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d10da-110">Remarks</span></span>

<span data-ttu-id="d10da-111">Questo messaggio viene usato solo dall'hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.</span><span class="sxs-lookup"><span data-stu-id="d10da-111">This message is used only by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10da-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d10da-112">Requirements</span></span>



| <span data-ttu-id="d10da-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d10da-113">Requirement</span></span> | <span data-ttu-id="d10da-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d10da-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d10da-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d10da-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d10da-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d10da-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d10da-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d10da-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d10da-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d10da-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d10da-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d10da-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d10da-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d10da-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d10da-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d10da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10da-122">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="d10da-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="d10da-123">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="d10da-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





