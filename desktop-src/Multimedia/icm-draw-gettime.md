---
title: Messaggio di ICM_DRAW_GETTIME (VFW. h)
description: Il \_ messaggio ICM Draw \_ getTime richiede un driver di rendering che controlla la tempistica di disegno dei frame per restituire il valore corrente del clock interno. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- ICM_DRAW_GETTIME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301827"
---
# <a name="icm_draw_gettime-message"></a><span data-ttu-id="01f7f-105">Messaggio di tempo di \_ richiamo ICM \_</span><span class="sxs-lookup"><span data-stu-id="01f7f-105">ICM\_DRAW\_GETTIME message</span></span>

<span data-ttu-id="01f7f-106">Il messaggio **ICM \_ Draw \_ getTime** richiede un driver di rendering che controlla la tempistica di disegno dei frame per restituire il valore corrente del clock interno.</span><span class="sxs-lookup"><span data-stu-id="01f7f-106">The **ICM\_DRAW\_GETTIME** message requests a rendering driver that controls the timing of drawing frames to return the current value of its internal clock.</span></span> <span data-ttu-id="01f7f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .</span><span class="sxs-lookup"><span data-stu-id="01f7f-107">You can send this message explicitly or by using the [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) macro.</span></span>


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="01f7f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="01f7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f7f-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span><span class="sxs-lookup"><span data-stu-id="01f7f-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span></span>
</dt> <dd>

<span data-ttu-id="01f7f-110">Indirizzo che contiene l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="01f7f-110">Address to contain the current time.</span></span> <span data-ttu-id="01f7f-111">Il valore restituito deve essere specificato negli esempi.</span><span class="sxs-lookup"><span data-stu-id="01f7f-111">The return value should be specified in samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01f7f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01f7f-112">Return Value</span></span>

<span data-ttu-id="01f7f-113">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="01f7f-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="01f7f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="01f7f-114">Remarks</span></span>

<span data-ttu-id="01f7f-115">Questo messaggio è generalmente supportato da hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.</span><span class="sxs-lookup"><span data-stu-id="01f7f-115">This message is generally supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span> <span data-ttu-id="01f7f-116">Il messaggio può essere inviato anche se l'hardware è usato come master di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="01f7f-116">The message can also be sent if the hardware is being used as the synchronization master.</span></span>

## <a name="requirements"></a><span data-ttu-id="01f7f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01f7f-117">Requirements</span></span>



| <span data-ttu-id="01f7f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="01f7f-118">Requirement</span></span> | <span data-ttu-id="01f7f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="01f7f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01f7f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01f7f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01f7f-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01f7f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="01f7f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01f7f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01f7f-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01f7f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="01f7f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01f7f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="01f7f-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="01f7f-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01f7f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01f7f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f7f-127">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="01f7f-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="01f7f-128">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="01f7f-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





