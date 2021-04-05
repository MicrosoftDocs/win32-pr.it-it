---
title: Messaggio MM_MIM_MOREDATA (mmsystem. h)
description: Il \_ \_ messaggio MOREDATA in mm MIM viene inviato a una finestra di callback quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora \_ i messaggi di dati MIM abbastanza rapidamente da restare al passo con il driver di dispositivo di input.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67835a67c957a250fe1ae6d391f5ebd56d5301b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048337"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="9b5da-104">MM \_ \_ messaggio MOREDATA MIM</span><span class="sxs-lookup"><span data-stu-id="9b5da-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="9b5da-105">Il **messaggio \_ \_ MOREDATA in mm MIM** viene inviato a una finestra di callback quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora i messaggi di [**\_ dati MIM**](mim-data.md) abbastanza rapidamente da restare al passo con il driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="9b5da-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="9b5da-106">La finestra riceve questo messaggio solo quando l'applicazione specifica \_ lo stato di io MIDI \_ nella chiamata alla funzione [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="9b5da-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="9b5da-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b5da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b5da-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="9b5da-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="9b5da-109">Handle per il dispositivo di input MIDI che ha ricevuto il messaggio MIDI.</span><span class="sxs-lookup"><span data-stu-id="9b5da-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="9b5da-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="9b5da-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="9b5da-111">Specifica il messaggio MIDI ricevuto.</span><span class="sxs-lookup"><span data-stu-id="9b5da-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="9b5da-112">Il messaggio viene compresso in un valore parola doppia come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="9b5da-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="9b5da-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b5da-113">Requirement</span></span> | <span data-ttu-id="9b5da-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9b5da-114">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="9b5da-115">Parola alta</span><span class="sxs-lookup"><span data-stu-id="9b5da-115">High word</span></span> | <span data-ttu-id="9b5da-116">Byte di ordine superiore</span><span class="sxs-lookup"><span data-stu-id="9b5da-116">High-order byte</span></span> | <span data-ttu-id="9b5da-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9b5da-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="9b5da-118">Byte di ordine inferiore</span><span class="sxs-lookup"><span data-stu-id="9b5da-118">Low-order byte</span></span>  | <span data-ttu-id="9b5da-119">Contiene un secondo byte di dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="9b5da-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="9b5da-120">Parola bassa</span><span class="sxs-lookup"><span data-stu-id="9b5da-120">Low word</span></span>  | <span data-ttu-id="9b5da-121">Byte di ordine superiore</span><span class="sxs-lookup"><span data-stu-id="9b5da-121">High-order byte</span></span> | <span data-ttu-id="9b5da-122">Contiene il primo byte dei dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="9b5da-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="9b5da-123">Byte di ordine inferiore</span><span class="sxs-lookup"><span data-stu-id="9b5da-123">Low-order byte</span></span>  | <span data-ttu-id="9b5da-124">Contiene lo stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="9b5da-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="9b5da-125">I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="9b5da-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b5da-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b5da-126">Return Value</span></span>

<span data-ttu-id="9b5da-127">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="9b5da-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b5da-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b5da-128">Remarks</span></span>

<span data-ttu-id="9b5da-129">Se l'applicazione riceverà dati MIDI più velocemente di quanto possa elaborarla, è consigliabile non usare un meccanismo di callback della finestra.</span><span class="sxs-lookup"><span data-stu-id="9b5da-129">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="9b5da-130">Per ottimizzare la velocità, usare una funzione di callback e usare il messaggio [**\_ MOREDATA MIM**](mim-moredata.md) anziché mm \_ MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="9b5da-130">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="9b5da-131">Un'applicazione deve eseguire solo una quantità minima di elaborazione dei \_ messaggi MOREDATA MIM di mm \_ .</span><span class="sxs-lookup"><span data-stu-id="9b5da-131">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="9b5da-132">In particolare, le applicazioni non devono chiamare la funzione [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante l'elaborazione di mm \_ \_MOREDATA MIM). L'applicazione deve invece inserire i dati dell'evento in un buffer e quindi restituire.</span><span class="sxs-lookup"><span data-stu-id="9b5da-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="9b5da-133">Quando un'applicazione riceve un messaggio di [**\_ \_ dati MIM di mm**](mm-mim-data.md) dopo una serie \_ di \_ messaggi MOREDATA MIM, ha rilevato gli eventi MIDI in ingresso e può chiamare in modo sicuro funzioni a elevato utilizzo di tempo.</span><span class="sxs-lookup"><span data-stu-id="9b5da-133">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="9b5da-134">Lo stato dell'esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato; ogni messaggio viene espanso in modo da includere il byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="9b5da-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="9b5da-135">Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="9b5da-135">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="9b5da-136">Nessun timestamp disponibile con questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="9b5da-136">No time stamp is available with this message.</span></span> <span data-ttu-id="9b5da-137">Per i dati di input con timestamp, è necessario utilizzare i messaggi inviati alle funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="9b5da-137">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b5da-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b5da-138">Requirements</span></span>



| <span data-ttu-id="9b5da-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b5da-139">Requirement</span></span> | <span data-ttu-id="9b5da-140">Valore</span><span class="sxs-lookup"><span data-stu-id="9b5da-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5da-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b5da-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9b5da-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9b5da-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9b5da-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b5da-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9b5da-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9b5da-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9b5da-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b5da-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b5da-146"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b5da-146"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b5da-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b5da-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b5da-148">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="9b5da-148">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="9b5da-149">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="9b5da-149">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

