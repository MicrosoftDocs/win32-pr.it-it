---
title: Messaggio di ICM_DECOMPRESS (VFW. h)
description: Il \_ messaggio di decompressione ICM notifica a un driver di decompressione video di decomprimere un frame di dati in un buffer definito dall'applicazione.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- ICM_DECOMPRESS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048634"
---
# <a name="icm_decompress-message"></a><span data-ttu-id="7034b-104">\_Messaggio di decompressione ICM</span><span class="sxs-lookup"><span data-stu-id="7034b-104">ICM\_DECOMPRESS message</span></span>

<span data-ttu-id="7034b-105">Il messaggio di decompressione **ICM \_** notifica a un driver di decompressione video di decomprimere un frame di dati in un buffer definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7034b-105">The **ICM\_DECOMPRESS** message notifies a video decompression driver to decompress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="7034b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7034b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7034b-107"><span id="icd"></span><span id="ICD"></span>*ICD*</span><span class="sxs-lookup"><span data-stu-id="7034b-107"><span id="icd"></span><span id="ICD"></span>*icd*</span></span>
</dt> <dd>

<span data-ttu-id="7034b-108">Puntatore a una struttura [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) .</span><span class="sxs-lookup"><span data-stu-id="7034b-108">Pointer to an [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7034b-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="7034b-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7034b-110">Dimensioni, in byte, di [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span><span class="sxs-lookup"><span data-stu-id="7034b-110">Size, in bytes, of [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7034b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7034b-111">Return Value</span></span>

<span data-ttu-id="7034b-112">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7034b-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7034b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7034b-113">Remarks</span></span>

<span data-ttu-id="7034b-114">Se si desidera che il driver decomprimere i dati direttamente sullo schermo, inviare il messaggio di [**\_ progetto ICM**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="7034b-114">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="7034b-115">Il driver restituisce un errore se questo messaggio viene ricevuto prima del messaggio di [**\_ \_ inizio della decompressione MCI**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="7034b-115">The driver returns an error if this message is received before the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7034b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7034b-116">Requirements</span></span>



| <span data-ttu-id="7034b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7034b-117">Requirement</span></span> | <span data-ttu-id="7034b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7034b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7034b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7034b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7034b-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7034b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7034b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7034b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7034b-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7034b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7034b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7034b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7034b-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7034b-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7034b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7034b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7034b-126">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="7034b-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7034b-127">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="7034b-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





