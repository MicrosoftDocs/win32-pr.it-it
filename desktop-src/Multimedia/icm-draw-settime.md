---
title: Messaggio di ICM_DRAW_SETTIME (VFW. h)
description: Il \_ \_ periodo di tempo di disegno MCI fornisce le informazioni di sincronizzazione a un driver di rendering che gestisce la tempistica di disegno dei frame.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873633"
---
# <a name="icm_draw_settime-message"></a><span data-ttu-id="4e237-104">\_Messaggio di tempo di rielaborazione ICM \_</span><span class="sxs-lookup"><span data-stu-id="4e237-104">ICM\_DRAW\_SETTIME message</span></span>

<span data-ttu-id="4e237-105">Il **\_ periodo di \_ tempo** di disegno MCI fornisce le informazioni di sincronizzazione a un driver di rendering che gestisce la tempistica di disegno dei frame.</span><span class="sxs-lookup"><span data-stu-id="4e237-105">The **ICM\_DRAW\_SETTIME** provides synchronization information to a rendering driver that handles the timing of drawing frames.</span></span> <span data-ttu-id="4e237-106">Le informazioni di sincronizzazione sono il numero di esempio del fotogramma da creare.</span><span class="sxs-lookup"><span data-stu-id="4e237-106">The synchronization information is the sample number of the frame to draw.</span></span> <span data-ttu-id="4e237-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) .</span><span class="sxs-lookup"><span data-stu-id="4e237-107">You can send this message explicitly or by using the [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) macro.</span></span>


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="4e237-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e237-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e237-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span><span class="sxs-lookup"><span data-stu-id="4e237-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span></span>
</dt> <dd>

<span data-ttu-id="4e237-110">Numero di esempio del frame di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="4e237-110">Sample number of the frame to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e237-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e237-111">Return Value</span></span>

<span data-ttu-id="4e237-112">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4e237-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e237-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e237-113">Remarks</span></span>

<span data-ttu-id="4e237-114">In genere, il driver confronta il valore specificato con il numero di frame associato all'ora del clock interno e tenta di sincronizzare i due se la differenza è significativa.</span><span class="sxs-lookup"><span data-stu-id="4e237-114">Typically, the driver compares the specified value with the frame number associated with the time of its internal clock and attempts to synchronize the two if the difference is significant.</span></span>

<span data-ttu-id="4e237-115">Utilizzare questo messaggio quando l'hardware esegue la decompressione asincrona, la temporizzazione e il disegno e l'hardware si basa su un segnale di sincronizzazione esterno (l'hardware non viene utilizzato come master di sincronizzazione).</span><span class="sxs-lookup"><span data-stu-id="4e237-115">Use this message when the hardware performs its own asynchronous decompression, timing, and drawing, and the hardware relies on an external synchronization signal (the hardware is not being used as the synchronization master).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e237-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e237-116">Requirements</span></span>



| <span data-ttu-id="4e237-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e237-117">Requirement</span></span> | <span data-ttu-id="4e237-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4e237-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4e237-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e237-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e237-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4e237-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4e237-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e237-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e237-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4e237-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4e237-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e237-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e237-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e237-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e237-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e237-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e237-126">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="4e237-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4e237-127">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="4e237-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





