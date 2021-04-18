---
title: Messaggio MM_WIM_DATA (mmsystem. h)
description: Il \_ \_ messaggio di dati WIM mm viene inviato a una finestra quando i dati audio della forma d'onda sono presenti nel buffer di input e il buffer viene restituito all'applicazione. Il messaggio può essere inviato quando il buffer è pieno o dopo la chiamata della funzione waveInReset.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- MM_WIM_DATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c663d669635116500bc8aa7e7fdc994cdccd6dfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302505"
---
# <a name="mm_wim_data-message"></a><span data-ttu-id="6323f-105">\_ \_ Messaggio dati WIM mm</span><span class="sxs-lookup"><span data-stu-id="6323f-105">MM\_WIM\_DATA message</span></span>

<span data-ttu-id="6323f-106">Il messaggio di **\_ \_ dati WIM mm** viene inviato a una finestra quando i dati audio della forma d'onda sono presenti nel buffer di input e il buffer viene restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6323f-106">The **MM\_WIM\_DATA** message is sent to a window when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="6323f-107">Il messaggio può essere inviato quando il buffer è pieno o dopo la chiamata della funzione [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .</span><span class="sxs-lookup"><span data-stu-id="6323f-107">The message can be sent either when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="6323f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6323f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6323f-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="6323f-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="6323f-110">Handle per il dispositivo waveform-input audio che ha ricevuto i dati.</span><span class="sxs-lookup"><span data-stu-id="6323f-110">Handle to the waveform-audio input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="6323f-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="6323f-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="6323f-112">Puntatore a una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer contenente i dati.</span><span class="sxs-lookup"><span data-stu-id="6323f-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6323f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6323f-113">Return Value</span></span>

<span data-ttu-id="6323f-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="6323f-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6323f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6323f-115">Remarks</span></span>

<span data-ttu-id="6323f-116">Il buffer restituito potrebbe non essere pieno.</span><span class="sxs-lookup"><span data-stu-id="6323f-116">The returned buffer might not be full.</span></span> <span data-ttu-id="6323f-117">Usare il membro **dwBytesRecorded** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) specificata da *lParam* per determinare il numero di byte registrati nel buffer restituito.</span><span class="sxs-lookup"><span data-stu-id="6323f-117">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lParam* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6323f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6323f-118">Requirements</span></span>



| <span data-ttu-id="6323f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6323f-119">Requirement</span></span> | <span data-ttu-id="6323f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6323f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6323f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6323f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6323f-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6323f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6323f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6323f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6323f-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6323f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6323f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6323f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6323f-126"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6323f-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6323f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6323f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6323f-128">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="6323f-128">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="6323f-129">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="6323f-129">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

