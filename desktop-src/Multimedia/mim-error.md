---
title: Messaggio MIM_ERROR (mmsystem. h)
description: Il \_ messaggio di errore MIM viene inviato a una funzione di callback input MIDI quando viene ricevuto un messaggio MIDI non valido.
ms.assetid: ea720da5-1f18-4d0d-ac9d-45cd1c3219d6
keywords:
- MIM_ERROR messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add5b675a557ab25d41e79d99864e090364d384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119150"
---
# <a name="mim_error-message"></a><span data-ttu-id="5919e-104">\_Messaggio di errore MIM</span><span class="sxs-lookup"><span data-stu-id="5919e-104">MIM\_ERROR message</span></span>

<span data-ttu-id="5919e-105">Il messaggio di **\_ errore MIM** viene inviato a una funzione di callback input MIDI quando viene ricevuto un messaggio MIDI non valido.</span><span class="sxs-lookup"><span data-stu-id="5919e-105">The **MIM\_ERROR** message is sent to a MIDI input callback function when an invalid MIDI message is received.</span></span>


```C++
MIM_ERROR 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="5919e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5919e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5919e-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="5919e-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="5919e-108">Il messaggio MIDI ricevuto non è valido.</span><span class="sxs-lookup"><span data-stu-id="5919e-108">Invalid MIDI message that was received.</span></span> <span data-ttu-id="5919e-109">Il messaggio viene compresso in un valore parola doppia con il primo byte del messaggio nel byte di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="5919e-109">The message is packed into a doubleword value with the first byte of the message in the low-order byte.</span></span>

</dd> <dt>

<span data-ttu-id="5919e-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="5919e-110"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="5919e-111">Ora in cui il messaggio è stato ricevuto dal driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="5919e-111">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="5919e-112">Il timestamp viene specificato in millisecondi, a partire da zero quando è stata chiamata la funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="5919e-112">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5919e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5919e-113">Return Value</span></span>

<span data-ttu-id="5919e-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="5919e-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5919e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5919e-115">Requirements</span></span>



| <span data-ttu-id="5919e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5919e-116">Requirement</span></span> | <span data-ttu-id="5919e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5919e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5919e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5919e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5919e-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5919e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5919e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5919e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5919e-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5919e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5919e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5919e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5919e-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5919e-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5919e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5919e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5919e-125">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="5919e-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="5919e-126">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="5919e-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

