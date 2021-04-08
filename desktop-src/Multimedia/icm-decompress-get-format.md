---
title: Messaggio di ICM_DECOMPRESS_GET_FORMAT (VFW. h)
description: Il \_ messaggio MCI Decompress \_ get \_ format richiede il formato di output dei dati decompressi da un driver di decompressione video. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressGetFormat.
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- ICM_DECOMPRESS_GET_FORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7eefa655646deae8e67fa16a87bfdb81a8b936
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048636"
---
# <a name="icm_decompress_get_format-message"></a><span data-ttu-id="582f6-105">\_Messaggio di \_ formato Get decomprit MCI \_</span><span class="sxs-lookup"><span data-stu-id="582f6-105">ICM\_DECOMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="582f6-106">Il messaggio **MCI \_ Decompress \_ get \_ Format** richiede il formato di output dei dati decompressi da un driver di decompressione video.</span><span class="sxs-lookup"><span data-stu-id="582f6-106">The **ICM\_DECOMPRESS\_GET\_FORMAT** message requests the output format of the decompressed data from a video decompression driver.</span></span> <span data-ttu-id="582f6-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="582f6-107">You can send this message explicitly or by using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="582f6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="582f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="582f6-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="582f6-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="582f6-110">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.</span><span class="sxs-lookup"><span data-stu-id="582f6-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="582f6-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="582f6-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="582f6-112">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) per contenere il formato di output.</span><span class="sxs-lookup"><span data-stu-id="582f6-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="582f6-113">È possibile specificare zero per richiedere solo le dimensioni del formato di output, come nella macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) .</span><span class="sxs-lookup"><span data-stu-id="582f6-113">You can specify zero to request only the size of the output format, as in the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="582f6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="582f6-114">Return Value</span></span>

<span data-ttu-id="582f6-115">Se *lpbiOutput* è zero, restituisce le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="582f6-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="582f6-116">Se *lpbiOutput* è diverso da zero, restituisce ICERR \_ OK in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="582f6-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="582f6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="582f6-117">Remarks</span></span>

<span data-ttu-id="582f6-118">Se *lpbiOutput* è diverso da zero, il driver deve riempire la struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con il formato di output predefinito corrispondente al formato di input specificato per *lpbiInput*.</span><span class="sxs-lookup"><span data-stu-id="582f6-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="582f6-119">Se il compressore può produrre diversi formati, il formato predefinito dovrebbe essere quello che conserva la maggior quantità di informazioni.</span><span class="sxs-lookup"><span data-stu-id="582f6-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="582f6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="582f6-120">Requirements</span></span>



| <span data-ttu-id="582f6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="582f6-121">Requirement</span></span> | <span data-ttu-id="582f6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="582f6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="582f6-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="582f6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="582f6-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="582f6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="582f6-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="582f6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="582f6-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="582f6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="582f6-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="582f6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="582f6-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="582f6-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="582f6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="582f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="582f6-130">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="582f6-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="582f6-131">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="582f6-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

