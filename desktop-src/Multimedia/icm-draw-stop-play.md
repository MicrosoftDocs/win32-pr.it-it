---
title: Messaggio di ICM_DRAW_STOP_PLAY (VFW. h)
description: Il \_ messaggio di \_ interruzione riproduzione del progetto ICM \_ notifica a un driver di rendering una volta completata un'operazione di riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawStopPlay.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- ICM_DRAW_STOP_PLAY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121686"
---
# <a name="icm_draw_stop_play-message"></a><span data-ttu-id="f32c3-105">\_Messaggio di \_ interruzione \_ riproduzione del progetto ICM</span><span class="sxs-lookup"><span data-stu-id="f32c3-105">ICM\_DRAW\_STOP\_PLAY message</span></span>

<span data-ttu-id="f32c3-106">Il messaggio di **\_ \_ interruzione \_ riproduzione del progetto ICM** notifica a un driver di rendering una volta completata un'operazione di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f32c3-106">The **ICM\_DRAW\_STOP\_PLAY** message notifies a rendering driver when a play operation is complete.</span></span> <span data-ttu-id="f32c3-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) .</span><span class="sxs-lookup"><span data-stu-id="f32c3-107">You can send this message explicitly or by using the [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) macro.</span></span>


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="f32c3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f32c3-108">Return Value</span></span>

<span data-ttu-id="f32c3-109">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="f32c3-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f32c3-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f32c3-110">Remarks</span></span>

<span data-ttu-id="f32c3-111">Utilizzare questo messaggio al termine dell'operazione di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f32c3-111">Use this message when the play operation is complete.</span></span> <span data-ttu-id="f32c3-112">Per terminare la temporizzazione, utilizzare il messaggio di [**\_ \_ interruzione di progetto ICM**](icm-draw-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="f32c3-112">Use the [**ICM\_DRAW\_STOP**](icm-draw-stop.md) message to end timing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f32c3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f32c3-113">Requirements</span></span>



| <span data-ttu-id="f32c3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f32c3-114">Requirement</span></span> | <span data-ttu-id="f32c3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f32c3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f32c3-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f32c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f32c3-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f32c3-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f32c3-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f32c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f32c3-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f32c3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f32c3-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f32c3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f32c3-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f32c3-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f32c3-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f32c3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f32c3-123">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="f32c3-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="f32c3-124">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="f32c3-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





