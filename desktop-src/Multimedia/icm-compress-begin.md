---
title: Messaggio di ICM_COMPRESS_BEGIN (VFW. h)
description: Il \_ \_ messaggio di inizio della compressione ICM notifica a un driver di compressione video di preparare la compressione dei dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- ICM_COMPRESS_BEGIN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048744"
---
# <a name="icm_compress_begin-message"></a><span data-ttu-id="12188-105">\_Messaggio di \_ inizio compressione MCI</span><span class="sxs-lookup"><span data-stu-id="12188-105">ICM\_COMPRESS\_BEGIN message</span></span>

<span data-ttu-id="12188-106">Il messaggio di **\_ \_ inizio** della compressione ICM notifica a un driver di compressione video di preparare la compressione dei dati.</span><span class="sxs-lookup"><span data-stu-id="12188-106">The **ICM\_COMPRESS\_BEGIN** message notifies a video compression driver to prepare to compress data.</span></span> <span data-ttu-id="12188-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .</span><span class="sxs-lookup"><span data-stu-id="12188-107">You can send this message explicitly or by using the [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) macro.</span></span>


```C++
ICM_COMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="12188-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="12188-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12188-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="12188-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="12188-110">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.</span><span class="sxs-lookup"><span data-stu-id="12188-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="12188-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="12188-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="12188-112">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di output.</span><span class="sxs-lookup"><span data-stu-id="12188-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12188-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12188-113">Return Value</span></span>

<span data-ttu-id="12188-114">Restituisce ICERR \_ OK se il driver supporta la compressione specificata o ICERR \_ BADFORMAT se il formato di input o di output non è supportato.</span><span class="sxs-lookup"><span data-stu-id="12188-114">Returns ICERR\_OK if the driver supports the specified compression or ICERR\_BADFORMAT if the input or output format is not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="12188-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="12188-115">Remarks</span></span>

<span data-ttu-id="12188-116">Il driver deve allocare e inizializzare qualsiasi tabella o memoria necessaria per comprimere i formati di dati quando riceve il messaggio di [**\_ compressione ICM**](icm-compress.md) .</span><span class="sxs-lookup"><span data-stu-id="12188-116">The driver should allocate and initialize any tables or memory that it needs for compressing the data formats when it receives the [**ICM\_COMPRESS**](icm-compress.md) message.</span></span>

<span data-ttu-id="12188-117">VCM Salva le impostazioni del messaggio di **inizio della \_ compressione \_ ICM** più recente.</span><span class="sxs-lookup"><span data-stu-id="12188-117">VCM saves the settings of the most recent **ICM\_COMPRESS\_BEGIN** message.</span></span> <span data-ttu-id="12188-118">I messaggi di fine compressione **MCI \_ \_ Begin** e [**ICM \_ compress \_**](icm-compress-end.md) non vengono annidati.</span><span class="sxs-lookup"><span data-stu-id="12188-118">The **ICM\_COMPRESS\_BEGIN** and [**ICM\_COMPRESS\_END**](icm-compress-end.md) messages do not nest.</span></span> <span data-ttu-id="12188-119">Se il driver riceve **l' \_ \_ inizio** della compressione ICM prima che la compressione venga arrestata con la **\_ \_ fine** della compressione MCI, dovrebbe riavviare la compressione con i nuovi parametri.</span><span class="sxs-lookup"><span data-stu-id="12188-119">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="12188-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12188-120">Requirements</span></span>



| <span data-ttu-id="12188-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="12188-121">Requirement</span></span> | <span data-ttu-id="12188-122">Valore</span><span class="sxs-lookup"><span data-stu-id="12188-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12188-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12188-123">Minimum supported client</span></span><br/> | <span data-ttu-id="12188-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="12188-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="12188-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12188-125">Minimum supported server</span></span><br/> | <span data-ttu-id="12188-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="12188-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="12188-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12188-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="12188-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="12188-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12188-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12188-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12188-130">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="12188-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="12188-131">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="12188-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

