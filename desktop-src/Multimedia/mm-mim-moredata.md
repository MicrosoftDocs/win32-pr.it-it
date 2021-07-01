---
title: MM_MIM_MOREDATA messaggio (Mmsystem.h)
description: Il messaggio MM MIM MOREDATA viene inviato a una finestra di callback quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI ma l'applicazione non elabora i messaggi MIM DATA in modo sufficientemente veloce da rimanere al passo con il driver di dispositivo di \_ \_ \_ input.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- MM_MIM_MOREDATA messaggio Windows Multimedia
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
ms.openlocfilehash: 3079c537ddca056ca690537c27edd95826de1189
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120026"
---
# <a name="mm_mim_moredata-message"></a><span data-ttu-id="7dabb-104">Mm \_ MIM \_ MOREDATA message</span><span class="sxs-lookup"><span data-stu-id="7dabb-104">MM\_MIM\_MOREDATA message</span></span>

<span data-ttu-id="7dabb-105">Il messaggio **MM \_ MIM \_ MOREDATA** viene inviato a una finestra di callback quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI ma l'applicazione non elabora i messaggi [**MIM \_ DATA**](mim-data.md) in modo sufficientemente veloce da rimanere al passo con il driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="7dabb-105">The **MM\_MIM\_MOREDATA** message is sent to a callback window when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="7dabb-106">La finestra riceve questo messaggio solo quando l'applicazione specifica MIDI \_ IO STATUS nella chiamata alla funzione \_ [**midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)</span><span class="sxs-lookup"><span data-stu-id="7dabb-106">The window receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="7dabb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7dabb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dabb-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="7dabb-108"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="7dabb-109">Handle per il dispositivo di input MIDI che ha ricevuto il messaggio MIDI.</span><span class="sxs-lookup"><span data-stu-id="7dabb-109">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="7dabb-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="7dabb-110"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="7dabb-111">Specifica il messaggio MIDI ricevuto.</span><span class="sxs-lookup"><span data-stu-id="7dabb-111">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="7dabb-112">Il messaggio viene inserito in un valore doubleword come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="7dabb-112">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="7dabb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dabb-113">Requirement</span></span> | <span data-ttu-id="7dabb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7dabb-114">Value</span></span> | <span data-ttu-id="7dabb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dabb-115">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="7dabb-116">Parola alta</span><span class="sxs-lookup"><span data-stu-id="7dabb-116">High word</span></span> | <span data-ttu-id="7dabb-117">Byte di ordine elevato</span><span class="sxs-lookup"><span data-stu-id="7dabb-117">High-order byte</span></span> | <span data-ttu-id="7dabb-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="7dabb-118">Not used.</span></span>                                           |
|           | <span data-ttu-id="7dabb-119">Byte di ordine ridotto</span><span class="sxs-lookup"><span data-stu-id="7dabb-119">Low-order byte</span></span>  | <span data-ttu-id="7dabb-120">Contiene un secondo byte di dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="7dabb-120">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="7dabb-121">Parola bassa</span><span class="sxs-lookup"><span data-stu-id="7dabb-121">Low word</span></span>  | <span data-ttu-id="7dabb-122">Byte di ordine elevato</span><span class="sxs-lookup"><span data-stu-id="7dabb-122">High-order byte</span></span> | <span data-ttu-id="7dabb-123">Contiene il primo byte dei dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="7dabb-123">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="7dabb-124">Byte di ordine ridotto</span><span class="sxs-lookup"><span data-stu-id="7dabb-124">Low-order byte</span></span>  | <span data-ttu-id="7dabb-125">Contiene lo stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="7dabb-125">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="7dabb-126">I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="7dabb-126">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dabb-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7dabb-127">Return Value</span></span>

<span data-ttu-id="7dabb-128">Questo messaggio non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7dabb-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dabb-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="7dabb-129">Remarks</span></span>

<span data-ttu-id="7dabb-130">Se l'applicazione riceverà i dati MIDI più velocemente di quanto possa elaborarlo, non è consigliabile usare un meccanismo di callback della finestra.</span><span class="sxs-lookup"><span data-stu-id="7dabb-130">If your application will receive MIDI data faster than it can process it, you should not use a window callback mechanism.</span></span> <span data-ttu-id="7dabb-131">Per ottimizzare la velocità, usare una funzione di callback e usare il messaggio [**\_ MIM MOREDATA**](mim-moredata.md) anziché MM \_ MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="7dabb-131">To maximize speed, use a callback function, and use the [**MIM\_MOREDATA**](mim-moredata.md) message instead of MM\_MIM\_MOREDATA.</span></span>

<span data-ttu-id="7dabb-132">Un'applicazione deve eseguire solo una quantità minima di elaborazione dei messaggi MM \_ MIM \_ MOREDATA.</span><span class="sxs-lookup"><span data-stu-id="7dabb-132">An application should do only a minimal amount of processing of MM\_MIM\_MOREDATA messages.</span></span> <span data-ttu-id="7dabb-133">In particolare, le applicazioni non devono chiamare la [funzione PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante l'elaborazione di MM \_ MIM \_ MOREDATA. Al contrario, l'applicazione deve inserire i dati dell'evento in un buffer e quindi restituire .</span><span class="sxs-lookup"><span data-stu-id="7dabb-133">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MM\_MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="7dabb-134">Quando un'applicazione riceve un messaggio [**MM \_ MIM \_ DATA**](mm-mim-data.md) dopo una serie di messaggi MM \_ MIM MOREDATA, ha raggiunto gli eventi MIDI in ingresso e può chiamare in modo sicuro funzioni a elevato utilizzo \_ di tempo.</span><span class="sxs-lookup"><span data-stu-id="7dabb-134">When an application receives an [**MM\_MIM\_DATA**](mm-mim-data.md) message after a series of MM\_MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="7dabb-135">Lo stato di esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato. ogni messaggio viene espanso per includere il byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="7dabb-135">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="7dabb-136">Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="7dabb-136">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="7dabb-137">Con questo messaggio non è disponibile alcun timestamp.</span><span class="sxs-lookup"><span data-stu-id="7dabb-137">No time stamp is available with this message.</span></span> <span data-ttu-id="7dabb-138">Per i dati di input con timestamp, è necessario usare i messaggi inviati alle funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="7dabb-138">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dabb-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dabb-139">Requirements</span></span>



| <span data-ttu-id="7dabb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dabb-140">Requirement</span></span> | <span data-ttu-id="7dabb-141">Valore</span><span class="sxs-lookup"><span data-stu-id="7dabb-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dabb-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dabb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7dabb-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7dabb-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7dabb-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dabb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7dabb-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7dabb-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7dabb-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7dabb-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dabb-147"><dt>Mmsystem.h (include Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7dabb-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dabb-148">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7dabb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dabb-149">Instrument Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="7dabb-149">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="7dabb-150">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="7dabb-150">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

