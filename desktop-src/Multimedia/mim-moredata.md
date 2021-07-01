---
title: MIM_MOREDATA messaggio (Mmsystem.h)
description: Il messaggio MIM MOREDATA viene inviato a una funzione di callback di input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora i messaggi DI DATI MIM abbastanza velocemente da rimanere al passo con il driver di dispositivo di \_ \_ input.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA messaggio Windows Multimedia
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
ms.openlocfilehash: c6342823e13a085b377a3e71f28a0f9ff016681c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119406"
---
# <a name="mim_moredata-message"></a><span data-ttu-id="41d3d-104">Messaggio \_ MOREDATA MIM</span><span class="sxs-lookup"><span data-stu-id="41d3d-104">MIM\_MOREDATA message</span></span>

<span data-ttu-id="41d3d-105">Il messaggio **\_ MIM MOREDATA** viene inviato a una funzione di callback di input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI, ma l'applicazione non elabora i messaggi [**MIM \_ DATA**](mim-data.md) in modo sufficientemente veloce da rimanere al passo con il driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="41d3d-105">The **MIM\_MOREDATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device but the application is not processing [**MIM\_DATA**](mim-data.md) messages fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="41d3d-106">La funzione di callback riceve questo messaggio solo quando l'applicazione specifica MIDI IO STATUS nella \_ \_ chiamata alla funzione [**midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)</span><span class="sxs-lookup"><span data-stu-id="41d3d-106">The callback function receives this message only when the application specifies MIDI\_IO\_STATUS in the call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span>


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="41d3d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="41d3d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d3d-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="41d3d-108"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="41d3d-109">Specifica il messaggio MIDI ricevuto.</span><span class="sxs-lookup"><span data-stu-id="41d3d-109">Specifies the MIDI message that was received.</span></span> <span data-ttu-id="41d3d-110">Il messaggio viene inserito in un **valore DWORD** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="41d3d-110">The message is packed into a **DWORD** value as follows:</span></span>



| <span data-ttu-id="41d3d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d3d-111">Requirement</span></span> | <span data-ttu-id="41d3d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="41d3d-112">Value</span></span> | <span data-ttu-id="41d3d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41d3d-113">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="41d3d-114">Parola alta</span><span class="sxs-lookup"><span data-stu-id="41d3d-114">High word</span></span> | <span data-ttu-id="41d3d-115">Byte di ordine elevato</span><span class="sxs-lookup"><span data-stu-id="41d3d-115">High-order byte</span></span> | <span data-ttu-id="41d3d-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="41d3d-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="41d3d-117">Byte di ordine ridotto</span><span class="sxs-lookup"><span data-stu-id="41d3d-117">Low-order byte</span></span>  | <span data-ttu-id="41d3d-118">Contiene un secondo byte di dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="41d3d-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="41d3d-119">Parola bassa</span><span class="sxs-lookup"><span data-stu-id="41d3d-119">Low word</span></span>  | <span data-ttu-id="41d3d-120">Byte di ordine elevato</span><span class="sxs-lookup"><span data-stu-id="41d3d-120">High-order byte</span></span> | <span data-ttu-id="41d3d-121">Contiene il primo byte dei dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="41d3d-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="41d3d-122">Byte di ordine ridotto</span><span class="sxs-lookup"><span data-stu-id="41d3d-122">Low-order byte</span></span>  | <span data-ttu-id="41d3d-123">Contiene lo stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="41d3d-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="41d3d-124">I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="41d3d-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="41d3d-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="41d3d-125"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="41d3d-126">Specifica l'ora in cui il messaggio è stato ricevuto dal driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="41d3d-126">Specifies the time that the message was received by the input device driver.</span></span> <span data-ttu-id="41d3d-127">Il timestamp viene specificato in millisecondi, a partire da 0 quando è stata chiamata la funzione [**midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)</span><span class="sxs-lookup"><span data-stu-id="41d3d-127">The time stamp is specified in milliseconds, beginning at 0 when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d3d-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41d3d-128">Return Value</span></span>

<span data-ttu-id="41d3d-129">Questo messaggio non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="41d3d-129">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41d3d-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="41d3d-130">Remarks</span></span>

<span data-ttu-id="41d3d-131">Un'applicazione deve eseguire solo una quantità minima di elaborazione dei messaggi \_ MOREDATA MIM.</span><span class="sxs-lookup"><span data-stu-id="41d3d-131">An application should do only a minimal amount of processing of MIM\_MOREDATA messages.</span></span> <span data-ttu-id="41d3d-132">In particolare, le applicazioni non devono chiamare la [funzione PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante l'elaborazione di MIM \_ MOREDATA. Al contrario, l'applicazione deve inserire i dati dell'evento in un buffer e quindi restituire .</span><span class="sxs-lookup"><span data-stu-id="41d3d-132">(In particular, applications should not call the [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) function while processing MIM\_MOREDATA.) Instead, the application should place the event data into a buffer and then return.</span></span>

<span data-ttu-id="41d3d-133">Quando un'applicazione riceve un messaggio [**MIM \_ DATA**](mim-data.md) dopo una serie di messaggi MIM MOREDATA, ha raggiunto gli eventi MIDI in ingresso e può chiamare in modo sicuro funzioni a elevato utilizzo \_ di tempo.</span><span class="sxs-lookup"><span data-stu-id="41d3d-133">When an application receives an [**MIM\_DATA**](mim-data.md) message after a series of MIM\_MOREDATA messages, it has caught up with incoming MIDI events and can safely call time-intensive functions.</span></span>

<span data-ttu-id="41d3d-134">Lo stato di esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato. ogni messaggio viene espanso per includere il byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="41d3d-134">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="41d3d-135">Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="41d3d-135">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="41d3d-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41d3d-136">Requirements</span></span>



| <span data-ttu-id="41d3d-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d3d-137">Requirement</span></span> | <span data-ttu-id="41d3d-138">Valore</span><span class="sxs-lookup"><span data-stu-id="41d3d-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41d3d-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41d3d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="41d3d-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41d3d-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="41d3d-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41d3d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="41d3d-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41d3d-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="41d3d-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41d3d-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="41d3d-144"><dt>Mmsystem.h (include Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="41d3d-144"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d3d-145">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="41d3d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d3d-146">Instrument Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="41d3d-146">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="41d3d-147">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="41d3d-147">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

