---
title: Messaggio di ICM_COMPRESS_GET_SIZE (VFW. h)
description: Il \_ messaggio MCI compress \_ get \_ size richiede che il driver di compressione video fornisca la dimensione massima di un frame di dati quando viene compresso nel formato di output specificato. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICCompressGetSize.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964726"
---
# <a name="icm_compress_get_size-message"></a><span data-ttu-id="df1e2-105">\_ \_ Messaggio dimensioni compressione Get MCI \_</span><span class="sxs-lookup"><span data-stu-id="df1e2-105">ICM\_COMPRESS\_GET\_SIZE message</span></span>

<span data-ttu-id="df1e2-106">Il messaggio **MCI \_ compress \_ get \_ size** richiede che il driver di compressione video fornisca la dimensione massima di un frame di dati quando viene compresso nel formato di output specificato.</span><span class="sxs-lookup"><span data-stu-id="df1e2-106">The **ICM\_COMPRESS\_GET\_SIZE** message requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format.</span></span> <span data-ttu-id="df1e2-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) .</span><span class="sxs-lookup"><span data-stu-id="df1e2-107">You can send this message explicitly or by using the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro.</span></span>


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="df1e2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="df1e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df1e2-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="df1e2-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="df1e2-110">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.</span><span class="sxs-lookup"><span data-stu-id="df1e2-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="df1e2-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="df1e2-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="df1e2-112">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di output.</span><span class="sxs-lookup"><span data-stu-id="df1e2-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df1e2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df1e2-113">Return Value</span></span>

<span data-ttu-id="df1e2-114">Restituisce il numero massimo di byte che può essere occupato da un singolo frame compresso.</span><span class="sxs-lookup"><span data-stu-id="df1e2-114">Returns the maximum number of bytes a single compressed frame can occupy.</span></span>

## <a name="remarks"></a><span data-ttu-id="df1e2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="df1e2-115">Remarks</span></span>

<span data-ttu-id="df1e2-116">In genere, le applicazioni inviano questo messaggio per determinare la dimensione di un buffer da allocare per il frame compresso.</span><span class="sxs-lookup"><span data-stu-id="df1e2-116">Typically, applications send this message to determine how large a buffer to allocate for the compressed frame.</span></span>

<span data-ttu-id="df1e2-117">Il driver deve calcolare la dimensione del frame possibile più grande in base ai formati di input e di output.</span><span class="sxs-lookup"><span data-stu-id="df1e2-117">The driver should calculate the size of the largest possible frame based on the input and output formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="df1e2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df1e2-118">Requirements</span></span>



| <span data-ttu-id="df1e2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="df1e2-119">Requirement</span></span> | <span data-ttu-id="df1e2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="df1e2-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="df1e2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df1e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="df1e2-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df1e2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="df1e2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df1e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="df1e2-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df1e2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="df1e2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df1e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="df1e2-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="df1e2-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df1e2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df1e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df1e2-128">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="df1e2-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="df1e2-129">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="df1e2-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

