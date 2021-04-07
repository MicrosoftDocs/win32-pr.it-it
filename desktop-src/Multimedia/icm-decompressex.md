---
title: Messaggio di ICM_DECOMPRESSEX (VFW. h)
description: Il \_ messaggio ICM DECOMPRESSEX notifica a un driver di compressione video di decomprimere un frame di dati direttamente sullo schermo, decomprimerlo in una DIB a discesa o decomprimere le immagini descritte con i rettangoli di origine e di destinazione.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- ICM_DECOMPRESSEX messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048633"
---
# <a name="icm_decompressex-message"></a><span data-ttu-id="a5251-104">\_Messaggio DECOMPRESSEX ICM</span><span class="sxs-lookup"><span data-stu-id="a5251-104">ICM\_DECOMPRESSEX message</span></span>

<span data-ttu-id="a5251-105">Il messaggio **ICM \_ DECOMPRESSEX** notifica a un driver di compressione video di decomprimere un frame di dati direttamente sullo schermo, decomprimerlo in una DIB a discesa o decomprimere le immagini descritte con i rettangoli di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a5251-105">The **ICM\_DECOMPRESSEX** message notifies a video compression driver to decompress a frame of data directly to the screen, decompress to an upside-down DIB, or decompress images described with source and destination rectangles.</span></span>


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="a5251-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5251-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5251-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="a5251-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="a5251-108">Puntatore a una struttura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) .</span><span class="sxs-lookup"><span data-stu-id="a5251-108">Pointer to an [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a5251-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5251-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="a5251-110">Dimensioni, in byte, di [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="a5251-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5251-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5251-111">Return Value</span></span>

<span data-ttu-id="a5251-112">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a5251-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5251-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5251-113">Remarks</span></span>

<span data-ttu-id="a5251-114">Questo messaggio è simile a [**ICM \_ decomprimete**](icm-decompress.md) , ad eccezione del fatto che usa la struttura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) per definire le informazioni di decompressione.</span><span class="sxs-lookup"><span data-stu-id="a5251-114">This message is similar to [**ICM\_DECOMPRESS**](icm-decompress.md) except that it uses the [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure to define its decompression information.</span></span>

<span data-ttu-id="a5251-115">Se si desidera che il driver decomprimere i dati direttamente sullo schermo, inviare il messaggio di [**\_ progetto ICM**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="a5251-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="a5251-116">Il driver restituisce un errore se questo messaggio viene ricevuto prima del messaggio di [**\_ \_ inizio DECOMPRESSEX di ICM**](icm-decompressex-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="a5251-116">The driver returns an error if this message is received before the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5251-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5251-117">Requirements</span></span>



| <span data-ttu-id="a5251-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5251-118">Requirement</span></span> | <span data-ttu-id="a5251-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a5251-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a5251-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5251-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a5251-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a5251-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a5251-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5251-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a5251-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a5251-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a5251-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5251-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5251-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5251-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5251-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5251-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5251-127">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="a5251-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a5251-128">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="a5251-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





