---
title: Messaggio di ICM_DECOMPRESS_GET_PALETTE (VFW. h)
description: Il \_ messaggio della tavolozza Decomprimi MCI \_ \_ richiede che il driver di decompressione video fornisca la tabella dei colori della struttura di output BITMAPINFOHEADER. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressGetPalette.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- ICM_DECOMPRESS_GET_PALETTE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302268"
---
# <a name="icm_decompress_get_palette-message"></a><span data-ttu-id="862f8-105">\_Messaggio della \_ tavolozza Decompress Get di ICM \_</span><span class="sxs-lookup"><span data-stu-id="862f8-105">ICM\_DECOMPRESS\_GET\_PALETTE message</span></span>

<span data-ttu-id="862f8-106">Il messaggio della **\_ \_ \_ tavolozza Decomprimi MCI** richiede che il driver di decompressione video fornisca la tabella dei colori della struttura di output [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="862f8-106">The **ICM\_DECOMPRESS\_GET\_PALETTE** message requests that the video decompression driver supply the color table of the output [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure.</span></span> <span data-ttu-id="862f8-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="862f8-107">You can send this message explicitly or by using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="862f8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="862f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="862f8-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="862f8-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="862f8-110">Puntatore a una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) contenente il formato di input.</span><span class="sxs-lookup"><span data-stu-id="862f8-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="862f8-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="862f8-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="862f8-112">Puntatore a una struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) per contenere la tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="862f8-112">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure to contain the color table.</span></span> <span data-ttu-id="862f8-113">Lo spazio riservato per la tabella dei colori è sempre di almeno 256 colori.</span><span class="sxs-lookup"><span data-stu-id="862f8-113">The space reserved for the color table is always at least 256 colors.</span></span> <span data-ttu-id="862f8-114">È possibile specificare zero per questo parametro per restituire solo le dimensioni della tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="862f8-114">You can specify zero for this parameter to return only the size of the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="862f8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="862f8-115">Return Value</span></span>

<span data-ttu-id="862f8-116">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="862f8-116">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="862f8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="862f8-117">Remarks</span></span>

<span data-ttu-id="862f8-118">Se *lpbiOutput* è diverso da zero, il driver imposta il membro **biClrUsed** di [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) sul numero di colori nella tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="862f8-118">If *lpbiOutput* is nonzero, the driver sets the **biClrUsed** member of [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) to the number of colors in the color table.</span></span> <span data-ttu-id="862f8-119">Il driver riempie il membro **bmiColors** di [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con i colori effettivi.</span><span class="sxs-lookup"><span data-stu-id="862f8-119">The driver fills the **bmiColors** member of [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) with the actual colors.</span></span>

<span data-ttu-id="862f8-120">Il driver deve supportare questo messaggio solo se usa una tavolozza diversa da quella specificata nel formato di input.</span><span class="sxs-lookup"><span data-stu-id="862f8-120">The driver should support this message only if it uses a palette other than the one specified in the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="862f8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="862f8-121">Requirements</span></span>



| <span data-ttu-id="862f8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="862f8-122">Requirement</span></span> | <span data-ttu-id="862f8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="862f8-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="862f8-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="862f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="862f8-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="862f8-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="862f8-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="862f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="862f8-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="862f8-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="862f8-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="862f8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="862f8-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="862f8-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="862f8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="862f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862f8-131">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="862f8-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="862f8-132">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="862f8-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

