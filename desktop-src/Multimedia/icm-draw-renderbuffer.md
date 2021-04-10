---
title: Messaggio di ICM_DRAW_RENDERBUFFER (VFW. h)
description: Il \_ \_ messaggio RENDERBUFFER per il progetto ICM notifica a un driver di rendering di creare i frame passati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawRenderBuffer.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- ICM_DRAW_RENDERBUFFER messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964687"
---
# <a name="icm_draw_renderbuffer-message"></a><span data-ttu-id="94ba7-105">\_ \_ Messaggio RENDERBUFFER per il progetto ICM</span><span class="sxs-lookup"><span data-stu-id="94ba7-105">ICM\_DRAW\_RENDERBUFFER message</span></span>

<span data-ttu-id="94ba7-106">Il **messaggio \_ \_ RENDERBUFFER per il progetto ICM** notifica a un driver di rendering di creare i frame passati.</span><span class="sxs-lookup"><span data-stu-id="94ba7-106">The **ICM\_DRAW\_RENDERBUFFER** message notifies a rendering driver to draw the frames that have been passed to it.</span></span> <span data-ttu-id="94ba7-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) .</span><span class="sxs-lookup"><span data-stu-id="94ba7-107">You can send this message explicitly or by using the [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) macro.</span></span>


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="94ba7-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94ba7-108">Return Value</span></span>

<span data-ttu-id="94ba7-109">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="94ba7-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94ba7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="94ba7-110">Remarks</span></span>

<span data-ttu-id="94ba7-111">Utilizzare questo messaggio con hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.</span><span class="sxs-lookup"><span data-stu-id="94ba7-111">Use this message with hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="94ba7-112">Questo messaggio viene in genere usato per eseguire un'operazione di ricerca quando il driver deve essere indicato in modo specifico per visualizzare ogni fotogramma video passato anziché riprodurre una sequenza di fotogrammi video.</span><span class="sxs-lookup"><span data-stu-id="94ba7-112">This message is typically used to perform a seek operation when the driver must be specifically instructed to display each video frame passed to it rather than playing a sequence of video frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ba7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94ba7-113">Requirements</span></span>



| <span data-ttu-id="94ba7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="94ba7-114">Requirement</span></span> | <span data-ttu-id="94ba7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="94ba7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="94ba7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94ba7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="94ba7-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="94ba7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="94ba7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94ba7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="94ba7-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="94ba7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="94ba7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94ba7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="94ba7-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="94ba7-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94ba7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94ba7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ba7-123">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="94ba7-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="94ba7-124">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="94ba7-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





