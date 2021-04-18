---
title: Messaggio di ICM_DECOMPRESS_SET_PALETTE (VFW. h)
description: Il \_ messaggio della \_ tavolozza del set di decomprimementi ICM \_ specifica una tavolozza per un driver di decompressione video da usare se viene decompresso in un formato che usa una tavolozza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressSetPalette.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- ICM_DECOMPRESS_SET_PALETTE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302266"
---
# <a name="icm_decompress_set_palette-message"></a><span data-ttu-id="654af-105">\_Messaggio della \_ tavolozza del set di DEcompressione ICM \_</span><span class="sxs-lookup"><span data-stu-id="654af-105">ICM\_DECOMPRESS\_SET\_PALETTE message</span></span>

<span data-ttu-id="654af-106">Il messaggio della **\_ \_ \_ tavolozza del set di decomprimementi ICM** specifica una tavolozza per un driver di decompressione video da usare se viene decompresso in un formato che usa una tavolozza.</span><span class="sxs-lookup"><span data-stu-id="654af-106">The **ICM\_DECOMPRESS\_SET\_PALETTE** message specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette.</span></span> <span data-ttu-id="654af-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) .</span><span class="sxs-lookup"><span data-stu-id="654af-107">You can send this message explicitly or by using the [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="654af-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="654af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="654af-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span><span class="sxs-lookup"><span data-stu-id="654af-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span></span>
</dt> <dd>

<span data-ttu-id="654af-110">Puntatore a una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) la cui tabella dei colori contiene i colori che devono essere utilizzati, se possibile.</span><span class="sxs-lookup"><span data-stu-id="654af-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure whose color table contains the colors that should be used if possible.</span></span> <span data-ttu-id="654af-111">È possibile specificare zero per usare il set predefinito di colori di output.</span><span class="sxs-lookup"><span data-stu-id="654af-111">You can specify zero to use the default set of output colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="654af-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="654af-112">Return Value</span></span>

<span data-ttu-id="654af-113">Restituisce ICERR \_ OK se il driver di decompressione può decomprimere con precisione le immagini nella tavolozza suggerita utilizzando il set di colori così come sono disposti nella tavolozza.</span><span class="sxs-lookup"><span data-stu-id="654af-113">Returns ICERR\_OK if the decompression driver can precisely decompress images to the suggested palette using the set of colors as they are arranged in the palette.</span></span> <span data-ttu-id="654af-114">Restituisce ICERR \_ in caso contrario non supportato.</span><span class="sxs-lookup"><span data-stu-id="654af-114">Returns ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="654af-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="654af-115">Remarks</span></span>

<span data-ttu-id="654af-116">Questo messaggio non dovrebbe influire sulla decompressione già in corso. al contrario, i colori passati con questo messaggio devono essere restituiti in risposta [**al \_ \_ \_ formato MCI Decompress Get**](icm-decompress-get-format.md) e ai messaggi [**MCI \_ Decompress \_ get \_ palette**](icm-decompress-get-palette.md) .</span><span class="sxs-lookup"><span data-stu-id="654af-116">This message should not affect decompression already in progress; rather, colors passed using this message should be returned in response to future [**ICM\_DECOMPRESS\_GET\_FORMAT**](icm-decompress-get-format.md) and [**ICM\_DECOMPRESS\_GET\_PALETTE**](icm-decompress-get-palette.md) messages.</span></span> <span data-ttu-id="654af-117">I colori vengono restituiti al driver di decompressione in un successivo messaggio di [**\_ \_ inizio**](icm-decompress-begin.md) decompressione di ICM.</span><span class="sxs-lookup"><span data-stu-id="654af-117">Colors are sent back to the decompression driver in a future [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="654af-118">Questo messaggio viene utilizzato principalmente quando un driver decomprime le immagini sullo schermo e un'altra applicazione che utilizza una tavolozza è in primo piano, forzando il driver di decompressione ad adattarsi a un set di colori esterno.</span><span class="sxs-lookup"><span data-stu-id="654af-118">This message is used primarily when a driver decompresses images to the screen and another application that uses a palette is in the foreground, forcing the decompression driver to adapt to a foreign set of colors.</span></span>

## <a name="requirements"></a><span data-ttu-id="654af-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="654af-119">Requirements</span></span>



| <span data-ttu-id="654af-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="654af-120">Requirement</span></span> | <span data-ttu-id="654af-121">Valore</span><span class="sxs-lookup"><span data-stu-id="654af-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="654af-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="654af-122">Minimum supported client</span></span><br/> | <span data-ttu-id="654af-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="654af-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="654af-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="654af-124">Minimum supported server</span></span><br/> | <span data-ttu-id="654af-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="654af-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="654af-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="654af-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="654af-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="654af-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="654af-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="654af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654af-129">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="654af-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="654af-130">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="654af-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

