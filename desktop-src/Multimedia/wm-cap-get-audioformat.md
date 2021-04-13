---
title: Messaggio di WM_CAP_GET_AUDIOFORMAT (VFW. h)
description: Il \_ messaggio WM Cap \_ get \_ AUDIOFORMAT ottiene il formato audio o le dimensioni del formato audio. È possibile inviare questo messaggio in modo esplicito o usando le macro capGetAudioFormat e capGetAudioFormatSize.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- WM_CAP_GET_AUDIOFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400218"
---
# <a name="wm_cap_get_audioformat-message"></a><span data-ttu-id="51d0f-105">\_ \_ \_ Messaggio AUDIOFORMAT di WM Cap</span><span class="sxs-lookup"><span data-stu-id="51d0f-105">WM\_CAP\_GET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="51d0f-106">Il messaggio **WM \_ Cap \_ get \_ AUDIOFORMAT** ottiene il formato audio o le dimensioni del formato audio.</span><span class="sxs-lookup"><span data-stu-id="51d0f-106">The **WM\_CAP\_GET\_AUDIOFORMAT** message obtains the audio format or the size of the audio format.</span></span> <span data-ttu-id="51d0f-107">È possibile inviare questo messaggio in modo esplicito o usando le macro [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) e [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) .</span><span class="sxs-lookup"><span data-stu-id="51d0f-107">You can send this message explicitly or by using the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros.</span></span>


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="51d0f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="51d0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51d0f-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="51d0f-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="51d0f-110">Dimensione, in byte, della struttura a cui fa riferimento **s**.</span><span class="sxs-lookup"><span data-stu-id="51d0f-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="51d0f-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span><span class="sxs-lookup"><span data-stu-id="51d0f-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="51d0f-112">Puntatore a una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) o **null**.</span><span class="sxs-lookup"><span data-stu-id="51d0f-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure, or **NULL**.</span></span> <span data-ttu-id="51d0f-113">Se il valore è **null**, viene restituita la dimensione, in byte, necessaria per mantenere la struttura.</span><span class="sxs-lookup"><span data-stu-id="51d0f-113">If the value is **NULL**, the size, in bytes, required to hold the structure is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51d0f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51d0f-114">Return Value</span></span>

<span data-ttu-id="51d0f-115">Restituisce la dimensione, in byte, del formato audio.</span><span class="sxs-lookup"><span data-stu-id="51d0f-115">Returns the size, in bytes, of the audio format.</span></span>

## <a name="remarks"></a><span data-ttu-id="51d0f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="51d0f-116">Remarks</span></span>

<span data-ttu-id="51d0f-117">Poiché i formati audio compressi variano in requisiti di dimensioni, le applicazioni devono prima recuperare le dimensioni, quindi allocare memoria e infine richiedere i dati in formato audio.</span><span class="sxs-lookup"><span data-stu-id="51d0f-117">Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="51d0f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51d0f-118">Requirements</span></span>



| <span data-ttu-id="51d0f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="51d0f-119">Requirement</span></span> | <span data-ttu-id="51d0f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="51d0f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="51d0f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51d0f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51d0f-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="51d0f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="51d0f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51d0f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51d0f-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="51d0f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="51d0f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51d0f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="51d0f-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="51d0f-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51d0f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51d0f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d0f-128">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="51d0f-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="51d0f-129">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="51d0f-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

