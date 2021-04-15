---
title: Messaggio di ICM_DRAW_WINDOW (VFW. h)
description: Il \_ messaggio della \_ finestra di progetto ICM notifica a un driver di rendering che è \_ necessario ricreare la finestra specificata per il messaggio di inizio del progetto ICM \_ .
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- ICM_DRAW_WINDOW messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476241"
---
# <a name="icm_draw_window-message"></a><span data-ttu-id="85ce9-104">Messaggio della finestra di \_ disegni ICM \_</span><span class="sxs-lookup"><span data-stu-id="85ce9-104">ICM\_DRAW\_WINDOW message</span></span>

<span data-ttu-id="85ce9-105">Il messaggio della **\_ \_ finestra di progetto ICM** notifica a un driver di rendering che è necessario ricreare la finestra specificata per il messaggio di [**\_ \_ inizio del progetto ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="85ce9-105">The **ICM\_DRAW\_WINDOW** message notifies a rendering driver that the window specified for the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message needs to be redrawn.</span></span> <span data-ttu-id="85ce9-106">La finestra è stata spostata o diventa temporaneamente nascosta.</span><span class="sxs-lookup"><span data-stu-id="85ce9-106">The window has moved or become temporarily obscured.</span></span> <span data-ttu-id="85ce9-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) .</span><span class="sxs-lookup"><span data-stu-id="85ce9-107">You can send this message explicitly or by using the [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) macro.</span></span>


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="85ce9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="85ce9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ce9-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="85ce9-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="85ce9-110">Puntatore al rettangolo di destinazione nelle coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="85ce9-110">Pointer to the destination rectangle in screen coordinates.</span></span> <span data-ttu-id="85ce9-111">Se questo parametro punta a un rettangolo vuoto, il disegno deve essere disattivato.</span><span class="sxs-lookup"><span data-stu-id="85ce9-111">If this parameter points to an empty rectangle, drawing should be turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85ce9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85ce9-112">Return Value</span></span>

<span data-ttu-id="85ce9-113">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="85ce9-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="85ce9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="85ce9-114">Remarks</span></span>

<span data-ttu-id="85ce9-115">Questo messaggio è supportato da hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.</span><span class="sxs-lookup"><span data-stu-id="85ce9-115">This message is supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="85ce9-116">I driver della sovrimpressione video usano questo messaggio per creare quando la finestra viene nascosta o spostata.</span><span class="sxs-lookup"><span data-stu-id="85ce9-116">Video-overlay drivers use this message to draw when the window is obscured or moved.</span></span> <span data-ttu-id="85ce9-117">Quando una finestra specificata per [**l' \_ \_ inizio di un progetto ICM**](icm-draw-begin.md) è completamente nascosta da altre finestre, il rettangolo di destinazione è vuoto.</span><span class="sxs-lookup"><span data-stu-id="85ce9-117">When a window specified for [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) is completely hidden by other windows, the destination rectangle is empty.</span></span> <span data-ttu-id="85ce9-118">Quando si verifica questa condizione, i driver devono disattivare l'hardware con sovrimpressione video.</span><span class="sxs-lookup"><span data-stu-id="85ce9-118">Drivers should turn off video-overlay hardware when this condition occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="85ce9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85ce9-119">Requirements</span></span>



| <span data-ttu-id="85ce9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="85ce9-120">Requirement</span></span> | <span data-ttu-id="85ce9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="85ce9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="85ce9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85ce9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85ce9-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="85ce9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="85ce9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85ce9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85ce9-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="85ce9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="85ce9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85ce9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="85ce9-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="85ce9-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85ce9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85ce9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ce9-129">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="85ce9-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="85ce9-130">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="85ce9-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





