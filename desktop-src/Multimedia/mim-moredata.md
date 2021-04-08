---
title: Messaggio MIM_MOREDATA (mmsystem. h)
description: Il \_ messaggio MOREDATA MIM viene inviato a una funzione di callback input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora \_ i messaggi di dati MIM in modo sufficientemente veloce da restare al passo con il driver di dispositivo di input.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743930"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="2d022-104">\_Messaggio MOREDATA MIM</span><span class="sxs-lookup"><span data-stu-id="2d022-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="2d022-105">Il **messaggio \_ MOREDATA MIM** viene inviato a una funzione di callback input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora i messaggi di [**\_ dati MIM**](mim-data.md) in modo sufficientemente veloce da restare al passo con il driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="2d022-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="2d022-106">La funzione di callback riceve questo messaggio solo quando l'applicazione specifica \_ lo stato di io MIDI \_ nella chiamata alla funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="2d022-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="2d022-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d022-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d022-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="2d022-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="2d022-109">Specifica il messaggio MIDI ricevuto.</span><span class="sxs-lookup"><span data-stu-id="2d022-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="2d022-110">Il messaggio viene compresso in un valore **DWORD** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2d022-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="2d022-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d022-111">Requirement</span></span> | <span data-ttu-id="2d022-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2d022-112">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="2d022-113">Parola alta</span><span class="sxs-lookup"><span data-stu-id="2d022-113">High word</span></span> | <span data-ttu-id="2d022-114">Byte di ordine superiore</span><span class="sxs-lookup"><span data-stu-id="2d022-114">High-order byte</span></span> | <span data-ttu-id="2d022-115">Non usato.</span><span class="sxs-lookup"><span data-stu-id="2d022-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="2d022-116">Byte di ordine inferiore</span><span class="sxs-lookup"><span data-stu-id="2d022-116">Low-order byte</span></span>  | <span data-ttu-id="2d022-117">Contiene un secondo byte di dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="2d022-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="2d022-118">Parola bassa</span><span class="sxs-lookup"><span data-stu-id="2d022-118">Low word</span></span>  | <span data-ttu-id="2d022-119">Byte di ordine superiore</span><span class="sxs-lookup"><span data-stu-id="2d022-119">High-order byte</span></span> | <span data-ttu-id="2d022-120">Contiene il primo byte dei dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="2d022-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="2d022-121">Byte di ordine inferiore</span><span class="sxs-lookup"><span data-stu-id="2d022-121">Low-order byte</span></span>  | <span data-ttu-id="2d022-122">Contiene lo stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="2d022-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="2d022-123">I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="2d022-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="2d022-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="2d022-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="2d022-125">Specifica l'ora in cui il messaggio è stato ricevuto dal driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="2d022-125">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="2d022-126">Il timestamp viene specificato in millisecondi, a partire da 0 quando è stata chiamata la funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="2d022-126">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d022-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d022-127">Return Value</span></span>

<span data-ttu-id="2d022-128">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="2d022-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d022-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d022-129">Remarks</span></span>

<span data-ttu-id="2d022-130">Un'applicazione deve eseguire solo una quantità minima di elaborazione dei \_ messaggi MOREDATA MIM.</span><span class="sxs-lookup"><span data-stu-id="2d022-130">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="2d022-131">In particolare, le applicazioni non devono chiamare la funzione [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante l'elaborazione di MIM \_ MOREDATA.) L'applicazione deve invece inserire i dati dell'evento in un buffer e quindi restituire.</span><span class="sxs-lookup"><span data-stu-id="2d022-131">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="2d022-132">Quando un'applicazione riceve un messaggio di [**\_ dati MIM**](mim-data.md) dopo una serie di \_ messaggi MOREDATA MIM, ha rilevato gli eventi MIDI in ingresso e può chiamare in modo sicuro funzioni a elevato utilizzo di tempo.</span><span class="sxs-lookup"><span data-stu-id="2d022-132">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="2d022-133">Lo stato dell'esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato; ogni messaggio viene espanso in modo da includere il byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="2d022-133">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="2d022-134">Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="2d022-134">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d022-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d022-135">Requirements</span></span>



| <span data-ttu-id="2d022-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d022-136">Requirement</span></span> | <span data-ttu-id="2d022-137">Valore</span><span class="sxs-lookup"><span data-stu-id="2d022-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d022-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d022-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2d022-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d022-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2d022-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d022-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2d022-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d022-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2d022-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d022-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d022-143"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d022-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d022-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d022-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d022-145">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="2d022-145">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="2d022-146">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="2d022-146">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

