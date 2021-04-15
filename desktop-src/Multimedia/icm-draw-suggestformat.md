---
title: Messaggio di ICM_DRAW_SUGGESTFORMAT (VFW. h)
description: Il \_ \_ messaggio SUGGESTFORMAT per il progetto ICM esegue una query su un driver di rendering per suggerire un formato decompresso che può creare.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475701"
---
# <a name="icm_draw_suggestformat-message"></a><span data-ttu-id="556bc-104">\_ \_ Messaggio SUGGESTFORMAT per il progetto ICM</span><span class="sxs-lookup"><span data-stu-id="556bc-104">ICM\_DRAW\_SUGGESTFORMAT message</span></span>

<span data-ttu-id="556bc-105">Il **messaggio \_ \_ SUGGESTFORMAT per il progetto ICM** esegue una query su un driver di rendering per suggerire un formato decompresso che può creare.</span><span class="sxs-lookup"><span data-stu-id="556bc-105">The **ICM\_DRAW\_SUGGESTFORMAT** message queries a rendering driver to suggest a decompressed format that it can draw.</span></span>


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a><span data-ttu-id="556bc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="556bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="556bc-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span><span class="sxs-lookup"><span data-stu-id="556bc-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span></span>
</dt> <dd>

<span data-ttu-id="556bc-108">Puntatore a una struttura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) .</span><span class="sxs-lookup"><span data-stu-id="556bc-108">Pointer to an [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure.</span></span>

</dd> <dt>

<span data-ttu-id="556bc-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="556bc-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="556bc-110">Dimensioni, in byte, di [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span><span class="sxs-lookup"><span data-stu-id="556bc-110">Size, in bytes, of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="556bc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="556bc-111">Return Value</span></span>

<span data-ttu-id="556bc-112">Restituisce ICERR \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="556bc-112">Returns ICERR\_OK if successful.</span></span> <span data-ttu-id="556bc-113">Se il membro **lpbiSuggest** della struttura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) è **null**, questo messaggio restituisce la quantità di memoria necessaria per contenere il formato suggerito.</span><span class="sxs-lookup"><span data-stu-id="556bc-113">If the **lpbiSuggest** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure is **NULL**, this message returns the amount of memory required to contain the suggested format.</span></span>

## <a name="remarks"></a><span data-ttu-id="556bc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="556bc-114">Remarks</span></span>

<span data-ttu-id="556bc-115">Il driver deve esaminare il formato specificato nel membro **lpbiIn** della struttura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) e usare il membro **lpbiSuggest** per restituire un formato che può creare.</span><span class="sxs-lookup"><span data-stu-id="556bc-115">The driver should examine the format specified in the **lpbiIn** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure and use the **lpbiSuggest** member to return a format it can draw.</span></span> <span data-ttu-id="556bc-116">Il formato di output deve conservare il maggior quantità possibile di dati dal formato di input.</span><span class="sxs-lookup"><span data-stu-id="556bc-116">The output format should preserve as much data as possible from the input format.</span></span>

<span data-ttu-id="556bc-117">Facoltativamente, il driver può usare l'handle del compressore installabile passato nel membro **hicDecompressor** di [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) per effettuare selezioni più complesse.</span><span class="sxs-lookup"><span data-stu-id="556bc-117">Optionally, the driver can use the installable compressor handle passed in the **hicDecompressor** member of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) to make more complex selections.</span></span> <span data-ttu-id="556bc-118">Se, ad esempio, il formato di input è dati JPEG a 24 bit, un renderer potrebbe eseguire una query sul decompressore per verificare se è possibile decomprimerlo in un formato YUV, che potrebbe essere disegnato in modo più efficiente, prima di selezionare il formato da suggerire.</span><span class="sxs-lookup"><span data-stu-id="556bc-118">For example, if the input format is 24-bit JPEG data, a renderer could query the decompressor to find out if it can decompress to a YUV format (which might be drawn more efficiently) before selecting the format to suggest.</span></span>

## <a name="requirements"></a><span data-ttu-id="556bc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="556bc-119">Requirements</span></span>



| <span data-ttu-id="556bc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="556bc-120">Requirement</span></span> | <span data-ttu-id="556bc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="556bc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="556bc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="556bc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="556bc-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="556bc-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="556bc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="556bc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="556bc-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="556bc-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="556bc-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="556bc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="556bc-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="556bc-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="556bc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="556bc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="556bc-129">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="556bc-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="556bc-130">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="556bc-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





