---
title: Messaggio di ICM_DRAW_START_PLAY (VFW. h)
description: Il \_ messaggio di \_ inizio riproduzione del progetto ICM \_ fornisce l'ora di inizio e di fine di un'operazione di riproduzione a un driver di rendering. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawStartPlay.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- ICM_DRAW_START_PLAY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119555"
---
# <a name="icm_draw_start_play-message"></a><span data-ttu-id="5e7b2-105">\_Messaggio di \_ inizio \_ riproduzione del progetto ICM</span><span class="sxs-lookup"><span data-stu-id="5e7b2-105">ICM\_DRAW\_START\_PLAY message</span></span>

<span data-ttu-id="5e7b2-106">Il messaggio di **\_ \_ inizio \_ riproduzione del progetto ICM** fornisce l'ora di inizio e di fine di un'operazione di riproduzione a un driver di rendering.</span><span class="sxs-lookup"><span data-stu-id="5e7b2-106">The **ICM\_DRAW\_START\_PLAY** message provides the start and end times of a play operation to a rendering driver.</span></span> <span data-ttu-id="5e7b2-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .</span><span class="sxs-lookup"><span data-stu-id="5e7b2-107">You can send this message explicitly or by using the [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) macro.</span></span>


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a><span data-ttu-id="5e7b2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e7b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e7b2-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span><span class="sxs-lookup"><span data-stu-id="5e7b2-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span></span>
</dt> <dd>

<span data-ttu-id="5e7b2-110">Ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="5e7b2-110">Start time.</span></span>

</dd> <dt>

<span data-ttu-id="5e7b2-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span><span class="sxs-lookup"><span data-stu-id="5e7b2-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span></span>
</dt> <dd>

<span data-ttu-id="5e7b2-112">Ora di fine.</span><span class="sxs-lookup"><span data-stu-id="5e7b2-112">End time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e7b2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e7b2-113">Return Value</span></span>

<span data-ttu-id="5e7b2-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="5e7b2-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e7b2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e7b2-115">Remarks</span></span>

<span data-ttu-id="5e7b2-116">Questo messaggio precede tutti i dati del frame inviati al driver di rendering.</span><span class="sxs-lookup"><span data-stu-id="5e7b2-116">This message precedes any frame data sent to the rendering driver.</span></span>

<span data-ttu-id="5e7b2-117">Le unità per *lFrom* e *LTO* vengono specificate con il messaggio di [**\_ \_ inizio del progetto ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="5e7b2-117">Units for *lFrom* and *lTo* are specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span> <span data-ttu-id="5e7b2-118">Per i dati video si tratta in genere di un numero di frame.</span><span class="sxs-lookup"><span data-stu-id="5e7b2-118">For video data this is normally a frame number.</span></span> <span data-ttu-id="5e7b2-119">Per ulteriori informazioni sulla velocità di riproduzione, vedere i membri **dwRate** e **DwScale** della struttura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .</span><span class="sxs-lookup"><span data-stu-id="5e7b2-119">For more information about the playback rate, see the **dwRate** and **dwScale** members of the [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure.</span></span>

<span data-ttu-id="5e7b2-120">Se l'ora di fine è inferiore all'ora di inizio, la direzione della riproduzione viene invertita.</span><span class="sxs-lookup"><span data-stu-id="5e7b2-120">If the end time is less than the start time, the playback direction is reversed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e7b2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e7b2-121">Requirements</span></span>



| <span data-ttu-id="5e7b2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e7b2-122">Requirement</span></span> | <span data-ttu-id="5e7b2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5e7b2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5e7b2-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e7b2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5e7b2-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e7b2-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5e7b2-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e7b2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5e7b2-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e7b2-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5e7b2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e7b2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e7b2-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e7b2-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e7b2-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e7b2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e7b2-131">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="5e7b2-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="5e7b2-132">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="5e7b2-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





