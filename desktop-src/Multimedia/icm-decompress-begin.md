---
title: Messaggio di ICM_DECOMPRESS_BEGIN (VFW. h)
description: Il \_ \_ messaggio di inizio della DEcompressione ICM invia una notifica a un driver di decompressione video per preparare la decompressione dei dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120942"
---
# <a name="icm_decompress_begin-message"></a><span data-ttu-id="43163-105">\_Messaggio di inizio decompressione ICM \_</span><span class="sxs-lookup"><span data-stu-id="43163-105">ICM\_DECOMPRESS\_BEGIN message</span></span>

<span data-ttu-id="43163-106">Il messaggio di **\_ \_ inizio** della decompressione ICM invia una notifica a un driver di decompressione video per preparare la decompressione dei dati.</span><span class="sxs-lookup"><span data-stu-id="43163-106">The **ICM\_DECOMPRESS\_BEGIN** message notifies a video decompression driver to prepare to decompress data.</span></span> <span data-ttu-id="43163-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .</span><span class="sxs-lookup"><span data-stu-id="43163-107">You can send this message explicitly or by using the [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) macro.</span></span>


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="43163-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="43163-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43163-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="43163-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="43163-110">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.</span><span class="sxs-lookup"><span data-stu-id="43163-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="43163-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="43163-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="43163-112">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di output.</span><span class="sxs-lookup"><span data-stu-id="43163-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43163-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43163-113">Return Value</span></span>

<span data-ttu-id="43163-114">Restituisce ICERR \_ OK se la decompressione specificata è supportata o ICERR \_ BADFORMAT in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="43163-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="43163-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="43163-115">Remarks</span></span>

<span data-ttu-id="43163-116">Quando il driver riceve questo messaggio, deve allocare buffer ed eseguire operazioni che richiedono molto tempo, in modo che sia in grado di elaborare i messaggi di [**\_ decompressione ICM**](icm-decompress.md) in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="43163-116">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESS**](icm-decompress.md) messages efficiently.</span></span>

<span data-ttu-id="43163-117">Se si desidera che il driver decomprimere i dati direttamente sullo schermo, inviare il messaggio di [**\_ progetto ICM**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="43163-117">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="43163-118">I messaggi di fine decompressione di **MCI \_ \_ Begin** e [**ICM \_ decomprimete \_**](icm-decompress-end.md) non vengono annidati.</span><span class="sxs-lookup"><span data-stu-id="43163-118">The **ICM\_DECOMPRESS\_BEGIN** and [**ICM\_DECOMPRESS\_END**](icm-decompress-end.md) messages do not nest.</span></span> <span data-ttu-id="43163-119">Se il driver riceve la decompressione **MCI \_ \_ inizia** prima che la decompressione venga interrotta con la **\_ \_ terminazione MCI decomprimere**, deve riavviare la decompressione con nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="43163-119">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="43163-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43163-120">Requirements</span></span>



| <span data-ttu-id="43163-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="43163-121">Requirement</span></span> | <span data-ttu-id="43163-122">Valore</span><span class="sxs-lookup"><span data-stu-id="43163-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="43163-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43163-123">Minimum supported client</span></span><br/> | <span data-ttu-id="43163-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="43163-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="43163-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43163-125">Minimum supported server</span></span><br/> | <span data-ttu-id="43163-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="43163-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="43163-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43163-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="43163-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="43163-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43163-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43163-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43163-130">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="43163-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="43163-131">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="43163-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

