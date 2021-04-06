---
title: Messaggio di ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: Il \_ messaggio Begin DECOMPRESSEX di ICM \_ notifica a un driver di compressione video di preparare la decompressione dei dati.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- ICM_DECOMPRESSEX_BEGIN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742954"
---
# <a name="icm_decompressex_begin-message"></a><span data-ttu-id="847c5-104">\_Messaggio di \_ inizio DECOMPRESSEX ICM</span><span class="sxs-lookup"><span data-stu-id="847c5-104">ICM\_DECOMPRESSEX\_BEGIN message</span></span>

<span data-ttu-id="847c5-105">Il **messaggio \_ \_ Begin DECOMPRESSEX di ICM** notifica a un driver di compressione video di preparare la decompressione dei dati.</span><span class="sxs-lookup"><span data-stu-id="847c5-105">The **ICM\_DECOMPRESSEX\_BEGIN** message notifies a video compression driver to prepare to decompress data.</span></span>


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="847c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="847c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="847c5-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="847c5-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="847c5-108">Puntatore a una struttura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) contenente i formati di input e di output.</span><span class="sxs-lookup"><span data-stu-id="847c5-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input and output formats.</span></span>

</dd> <dt>

<span data-ttu-id="847c5-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="847c5-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="847c5-110">Dimensioni, in byte, di [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="847c5-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="847c5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="847c5-111">Return Value</span></span>

<span data-ttu-id="847c5-112">Restituisce ICERR \_ OK se la decompressione specificata è supportata o ICERR \_ BADFORMAT in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="847c5-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="847c5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="847c5-113">Remarks</span></span>

<span data-ttu-id="847c5-114">Quando il driver riceve questo messaggio, deve allocare buffer ed eseguire operazioni che richiedono molto tempo, in modo che sia in grado di elaborare i messaggi [**\_ DECOMPRESSEX ICM**](icm-decompressex.md) in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="847c5-114">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESSEX**](icm-decompressex.md) messages efficiently.</span></span>

<span data-ttu-id="847c5-115">Se si vuole che il driver decomprimere i dati direttamente sullo schermo, inviare il messaggio di [**\_ \_ inizio del progetto ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="847c5-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="847c5-116">I **messaggi \_ DECOMPRESSEX \_ Begin** e [**ICM \_ DECOMPRESSEX \_ end**](icm-decompressex-end.md) non vengono annidati.</span><span class="sxs-lookup"><span data-stu-id="847c5-116">The **ICM\_DECOMPRESSEX\_BEGIN** and [**ICM\_DECOMPRESSEX\_END**](icm-decompressex-end.md) messages do not nest.</span></span> <span data-ttu-id="847c5-117">Se il driver riceve **la \_ DECOMPRESSEX MCI \_ iniziare** prima che la decompressione venga interrotta con la **\_ \_ fine di DECOMPRESSEX ICM**, dovrebbe riavviare la decompressione con nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="847c5-117">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="847c5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="847c5-118">Requirements</span></span>



| <span data-ttu-id="847c5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="847c5-119">Requirement</span></span> | <span data-ttu-id="847c5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="847c5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="847c5-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="847c5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="847c5-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="847c5-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="847c5-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="847c5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="847c5-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="847c5-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="847c5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="847c5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="847c5-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="847c5-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="847c5-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="847c5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="847c5-128">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="847c5-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="847c5-129">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="847c5-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





