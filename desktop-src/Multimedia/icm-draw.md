---
title: Messaggio di ICM_DRAW (VFW. h)
description: Il \_ messaggio di progetto ICM notifica a un driver di rendering di decomprimere un frame di dati e di trascinarlo sullo schermo.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- ICM_DRAW messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741170"
---
# <a name="icm_draw-message"></a><span data-ttu-id="3e61b-104">\_Messaggio di progetto ICM</span><span class="sxs-lookup"><span data-stu-id="3e61b-104">ICM\_DRAW message</span></span>

<span data-ttu-id="3e61b-105">Il messaggio di **\_ progetto ICM** notifica a un driver di rendering di decomprimere un frame di dati e di trascinarlo sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="3e61b-105">The **ICM\_DRAW** message notifies a rendering driver to decompress a frame of data and draw it to the screen.</span></span>


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="3e61b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e61b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e61b-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e61b-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="3e61b-108">Puntatore a una struttura [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) .</span><span class="sxs-lookup"><span data-stu-id="3e61b-108">Pointer to an [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3e61b-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e61b-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3e61b-110">Dimensioni, in byte, di [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span><span class="sxs-lookup"><span data-stu-id="3e61b-110">Size, in bytes, of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e61b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e61b-111">Return Value</span></span>

<span data-ttu-id="3e61b-112">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3e61b-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e61b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e61b-113">Remarks</span></span>

<span data-ttu-id="3e61b-114">Se il \_ flag di aggiornamento ICDRAW è impostato nel membro **DwFlags** di [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), l'area dello schermo utilizzata per il disegno non è valida e deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="3e61b-114">If the ICDRAW\_UPDATE flag is set in the **dwFlags** member of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), the area of the screen used for drawing is invalid and needs to be updated.</span></span> <span data-ttu-id="3e61b-115">La portata dell'aggiornamento dipende dal contenuto del membro **lpData** .</span><span class="sxs-lookup"><span data-stu-id="3e61b-115">The extent of updating depends on the contents of the **lpData** member.</span></span>

<span data-ttu-id="3e61b-116">Se **lpData** è **null**, il driver deve aggiornare l'intero rettangolo di destinazione con l'immagine corrente.</span><span class="sxs-lookup"><span data-stu-id="3e61b-116">If **lpData** is **NULL**, the driver should update the entire destination rectangle with the current image.</span></span> <span data-ttu-id="3e61b-117">Se il driver mantiene una copia dell'immagine in un buffer fuori schermo, questo messaggio può avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3e61b-117">If the driver maintains a copy of the image in an off-screen buffer, it can fail this message.</span></span> <span data-ttu-id="3e61b-118">Se **lpData** non è **null**, il driver deve creare i dati e assicurarsi che venga aggiornata l'intera destinazione.</span><span class="sxs-lookup"><span data-stu-id="3e61b-118">If **lpData** is not **NULL**, the driver should draw the data and make sure the entire destination is updated.</span></span>

<span data-ttu-id="3e61b-119">Se il \_ flag sbrigati di ICDRAW è impostato in **dwFlags**, l'applicazione chiamante desidera che il driver proceda il più rapidamente possibile, eventualmente non aggiornando neanche la schermata.</span><span class="sxs-lookup"><span data-stu-id="3e61b-119">If the ICDRAW\_HURRYUP flag is set in **dwFlags**, the calling application wants the driver to proceed as quickly as possible, possibly not even updating the screen.</span></span>

<span data-ttu-id="3e61b-120">Se il \_ flag di pre-registrazione ICDRAW è impostato in **dwFlags**, questo fotogramma video è costituito da informazioni preliminari e non deve essere visualizzato se possibile.</span><span class="sxs-lookup"><span data-stu-id="3e61b-120">If the ICDRAW\_PREROLL flag is set in **dwFlags**, this video frame is preliminary information and should not be displayed if possible.</span></span> <span data-ttu-id="3e61b-121">Se ad esempio Play prevede l'avvio dal frame 10 e frame 0 è il fotogramma chiave precedente più vicino, i frame da 0 a 9 avranno ICDRAW \_ preroll set.</span><span class="sxs-lookup"><span data-stu-id="3e61b-121">For example, if play is to start from frame 10, and frame 0 is the nearest previous key frame, frames 0 through 9 will have ICDRAW\_PREROLL set.</span></span>

<span data-ttu-id="3e61b-122">Se si desidera che il driver decomprimere i dati in un buffer, inviare il messaggio di [**\_ decompressione ICM**](icm-decompress.md) .</span><span class="sxs-lookup"><span data-stu-id="3e61b-122">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS**](icm-decompress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e61b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e61b-123">Requirements</span></span>



| <span data-ttu-id="3e61b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e61b-124">Requirement</span></span> | <span data-ttu-id="3e61b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3e61b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3e61b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e61b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3e61b-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e61b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3e61b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e61b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3e61b-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e61b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3e61b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e61b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e61b-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e61b-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e61b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e61b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e61b-133">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="3e61b-133">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3e61b-134">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="3e61b-134">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





