---
title: Messaggio di ICM_DRAW_BEGIN (VFW. h)
description: Il \_ \_ messaggio inizio progetto ICM notifica a un driver di rendering di prepararsi a creare dati.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- ICM_DRAW_BEGIN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964723"
---
# <a name="icm_draw_begin-message"></a><span data-ttu-id="d7b56-104">\_ \_ Messaggio inizio estrazione ICM</span><span class="sxs-lookup"><span data-stu-id="d7b56-104">ICM\_DRAW\_BEGIN message</span></span>

<span data-ttu-id="d7b56-105">Il **messaggio \_ \_ inizio progetto ICM** notifica a un driver di rendering di prepararsi a creare dati.</span><span class="sxs-lookup"><span data-stu-id="d7b56-105">The **ICM\_DRAW\_BEGIN** message notifies a rendering driver to prepare to draw data.</span></span>


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="d7b56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7b56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7b56-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span><span class="sxs-lookup"><span data-stu-id="d7b56-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span></span>
</dt> <dd>

<span data-ttu-id="d7b56-108">Puntatore a una struttura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) contenente il formato di input.</span><span class="sxs-lookup"><span data-stu-id="d7b56-108">Pointer to an [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="d7b56-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7b56-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d7b56-110">Dimensioni, in byte, di **ICDRAWBEGIN**.</span><span class="sxs-lookup"><span data-stu-id="d7b56-110">Size, in bytes, of **ICDRAWBEGIN**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7b56-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7b56-111">Return Value</span></span>

<span data-ttu-id="d7b56-112">Restituisce ICERR \_ OK se il driver supporta il disegno dei dati sullo schermo con la modalità e il formato specificati oppure un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="d7b56-112">Returns ICERR\_OK if the driver supports drawing the data to the screen in the specified manner and format, or an error code otherwise.</span></span> <span data-ttu-id="d7b56-113">I possibili valori di errore includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="d7b56-113">Possible error values include the following.</span></span>



| <span data-ttu-id="d7b56-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d7b56-114">Value</span></span>               | <span data-ttu-id="d7b56-115">Significato</span><span class="sxs-lookup"><span data-stu-id="d7b56-115">Meaning</span></span>                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="d7b56-116">\_BADFORMAT ICERR</span><span class="sxs-lookup"><span data-stu-id="d7b56-116">ICERR\_BADFORMAT</span></span>    | <span data-ttu-id="d7b56-117">Il formato di input o output non è supportato.</span><span class="sxs-lookup"><span data-stu-id="d7b56-117">Input or output format is not supported.</span></span>                                      |
| <span data-ttu-id="d7b56-118">\_NotSupported ICERR</span><span class="sxs-lookup"><span data-stu-id="d7b56-118">ICERR\_NOTSUPPORTED</span></span> | <span data-ttu-id="d7b56-119">Il driver non viene disegnato direttamente sullo schermo o non supporta questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="d7b56-119">Driver does not draw directly to the screen or does not support this message.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d7b56-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7b56-120">Remarks</span></span>

<span data-ttu-id="d7b56-121">Se si desidera che il driver decomprimere i dati in un buffer, inviare il messaggio di [**\_ \_ inizio di decompressione ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="d7b56-121">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="d7b56-122">I messaggi di **\_ \_ inizio** e [**di \_ \_ fine progetto**](icm-draw-end.md) ICM non nidificano.</span><span class="sxs-lookup"><span data-stu-id="d7b56-122">The **ICM\_DRAW\_BEGIN** and [**ICM\_DRAW\_END**](icm-draw-end.md) messages do not nest.</span></span> <span data-ttu-id="d7b56-123">Se il driver riceve **l' \_ \_ inizio dell'estrazione ICM** prima che la decompressione venga arrestata con la **\_ \_ fine del progetto ICM**, dovrebbe riavviare la decompressione con nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="d7b56-123">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7b56-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7b56-124">Requirements</span></span>



| <span data-ttu-id="d7b56-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7b56-125">Requirement</span></span> | <span data-ttu-id="d7b56-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d7b56-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d7b56-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7b56-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b56-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d7b56-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d7b56-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7b56-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b56-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d7b56-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7b56-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7b56-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7b56-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7b56-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7b56-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7b56-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b56-134">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="d7b56-134">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="d7b56-135">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="d7b56-135">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





