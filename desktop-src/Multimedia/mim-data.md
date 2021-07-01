---
title: MIM_DATA messaggio (Mmsystem.h)
description: Il messaggio MIM DATA viene inviato a una funzione di callback di input MIDI quando un messaggio MIDI viene \_ ricevuto da un dispositivo di input MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA message Windows Multimedia
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11d2701d488fe29ae6d0bc0742c32c803b28076
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118406"
---
# <a name="mim_data-message"></a><span data-ttu-id="acc8c-104">Messaggio DATI \_ MIM</span><span class="sxs-lookup"><span data-stu-id="acc8c-104">MIM\_DATA message</span></span>

<span data-ttu-id="acc8c-105">Il **messaggio MIM \_ DATA** viene inviato a una funzione di callback di input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="acc8c-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="acc8c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="acc8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc8c-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="acc8c-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="acc8c-108">Messaggio MIDI ricevuto.</span><span class="sxs-lookup"><span data-stu-id="acc8c-108">MIDI message that was received.</span></span> <span data-ttu-id="acc8c-109">Il messaggio viene inserito in un valore doubleword come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="acc8c-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="acc8c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="acc8c-110">Requirement</span></span> | <span data-ttu-id="acc8c-111">Valore</span><span class="sxs-lookup"><span data-stu-id="acc8c-111">Value</span></span> | <span data-ttu-id="acc8c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acc8c-112">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="acc8c-113">Parola alta</span><span class="sxs-lookup"><span data-stu-id="acc8c-113">High word</span></span> | <span data-ttu-id="acc8c-114">Byte di ordine elevato</span><span class="sxs-lookup"><span data-stu-id="acc8c-114">High-order byte</span></span> | <span data-ttu-id="acc8c-115">Non usato.</span><span class="sxs-lookup"><span data-stu-id="acc8c-115">Not used.</span></span>                                           |
|           | <span data-ttu-id="acc8c-116">Byte di ordine ridotto</span><span class="sxs-lookup"><span data-stu-id="acc8c-116">Low-order byte</span></span>  | <span data-ttu-id="acc8c-117">Contiene un secondo byte di dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="acc8c-117">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="acc8c-118">Parola bassa</span><span class="sxs-lookup"><span data-stu-id="acc8c-118">Low word</span></span>  | <span data-ttu-id="acc8c-119">Byte di ordine elevato</span><span class="sxs-lookup"><span data-stu-id="acc8c-119">High-order byte</span></span> | <span data-ttu-id="acc8c-120">Contiene il primo byte dei dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="acc8c-120">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="acc8c-121">Byte di ordine ridotto</span><span class="sxs-lookup"><span data-stu-id="acc8c-121">Low-order byte</span></span>  | <span data-ttu-id="acc8c-122">Contiene lo stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="acc8c-122">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="acc8c-123">I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="acc8c-123">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="acc8c-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="acc8c-124"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="acc8c-125">Ora di ricezione del messaggio da parte del driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="acc8c-125">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="acc8c-126">Il timestamp è specificato in millisecondi, a partire da zero quando è stata chiamata la funzione [**midiInStart.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)</span><span class="sxs-lookup"><span data-stu-id="acc8c-126">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acc8c-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="acc8c-127">Return Value</span></span>

<span data-ttu-id="acc8c-128">Questo messaggio non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="acc8c-128">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="acc8c-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="acc8c-129">Remarks</span></span>

<span data-ttu-id="acc8c-130">Lo stato di esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato. ogni messaggio viene espanso per includere il byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="acc8c-130">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="acc8c-131">Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="acc8c-131">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="acc8c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acc8c-132">Requirements</span></span>



| <span data-ttu-id="acc8c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="acc8c-133">Requirement</span></span> | <span data-ttu-id="acc8c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="acc8c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acc8c-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acc8c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="acc8c-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="acc8c-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="acc8c-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acc8c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="acc8c-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="acc8c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="acc8c-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="acc8c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="acc8c-140"><dt>Mmsystem.h (include Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="acc8c-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acc8c-141">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="acc8c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc8c-142">Instrument Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="acc8c-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="acc8c-143">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="acc8c-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

