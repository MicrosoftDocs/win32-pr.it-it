---
title: Messaggio WIM_DATA (mmsystem. h)
description: Il \_ messaggio di dati WIM viene inviato alla funzione di callback di input della forma d'onda-audio specificata quando i dati audio della forma d'onda sono presenti nel buffer di input e il buffer viene restituito all'applicazione.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- WIM_DATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302348"
---
# <a name="wim_data-message"></a><span data-ttu-id="4894a-104">\_Messaggio dati WIM</span><span class="sxs-lookup"><span data-stu-id="4894a-104">WIM\_DATA message</span></span>

<span data-ttu-id="4894a-105">Il messaggio di **\_ dati WIM** viene inviato alla funzione di callback di input della forma d'onda-audio specificata quando i dati audio della forma d'onda sono presenti nel buffer di input e il buffer viene restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4894a-105">The **WIM\_DATA** message is sent to the given waveform-audio input callback function when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="4894a-106">Il messaggio può essere inviato quando il buffer è pieno o dopo la chiamata della funzione [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .</span><span class="sxs-lookup"><span data-stu-id="4894a-106">The message can be sent when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="4894a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4894a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4894a-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="4894a-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4894a-109">Puntatore a una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer contenente i dati.</span><span class="sxs-lookup"><span data-stu-id="4894a-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="4894a-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4894a-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4894a-111">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4894a-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4894a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4894a-112">Return Value</span></span>

<span data-ttu-id="4894a-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="4894a-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4894a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4894a-114">Remarks</span></span>

<span data-ttu-id="4894a-115">Il buffer restituito potrebbe non essere pieno.</span><span class="sxs-lookup"><span data-stu-id="4894a-115">The returned buffer might not be full.</span></span> <span data-ttu-id="4894a-116">Usare il membro **dwBytesRecorded** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) specificata da *lpwvhdr* per determinare il numero di byte registrati nel buffer restituito.</span><span class="sxs-lookup"><span data-stu-id="4894a-116">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lpwvhdr* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4894a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4894a-117">Requirements</span></span>



| <span data-ttu-id="4894a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4894a-118">Requirement</span></span> | <span data-ttu-id="4894a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4894a-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4894a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4894a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4894a-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4894a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4894a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4894a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4894a-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4894a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4894a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4894a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4894a-125"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4894a-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4894a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4894a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4894a-127">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="4894a-127">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="4894a-128">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="4894a-128">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

