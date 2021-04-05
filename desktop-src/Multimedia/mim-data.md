---
title: Messaggio MIM_DATA (mmsystem. h)
description: Il \_ messaggio di dati MIM viene inviato a una funzione di callback input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA messaggi multimediali di Windows
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
ms.openlocfilehash: 48f96d2c23e64700a7a923cdd7633dabfcba9d1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874630"
---
# <a name="mim_data-message"></a><span data-ttu-id="c0715-104">\_Messaggio dati MIM</span><span class="sxs-lookup"><span data-stu-id="c0715-104">MIM\_DATA message</span></span>

<span data-ttu-id="c0715-105">Il messaggio di **\_ dati MIM** viene inviato a una funzione di callback input MIDI quando un messaggio MIDI viene ricevuto da un dispositivo di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="c0715-105">The **MIM\_DATA** message is sent to a MIDI input callback function when a MIDI message is received by a MIDI input device.</span></span>


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="c0715-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0715-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="c0715-107"><span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="c0715-108">Messaggio MIDI ricevuto.</span><span class="sxs-lookup"><span data-stu-id="c0715-108">MIDI message that was received.</span></span> <span data-ttu-id="c0715-109">Il messaggio viene compresso in un valore parola doppia come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c0715-109">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="c0715-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0715-110">Requirement</span></span> | <span data-ttu-id="c0715-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c0715-111">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="c0715-112">Parola alta</span><span class="sxs-lookup"><span data-stu-id="c0715-112">High word</span></span> | <span data-ttu-id="c0715-113">Byte di ordine superiore</span><span class="sxs-lookup"><span data-stu-id="c0715-113">High-order byte</span></span> | <span data-ttu-id="c0715-114">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c0715-114">Not used.</span></span>                                           |
|           | <span data-ttu-id="c0715-115">Byte di ordine inferiore</span><span class="sxs-lookup"><span data-stu-id="c0715-115">Low-order byte</span></span>  | <span data-ttu-id="c0715-116">Contiene un secondo byte di dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="c0715-116">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="c0715-117">Parola bassa</span><span class="sxs-lookup"><span data-stu-id="c0715-117">Low word</span></span>  | <span data-ttu-id="c0715-118">Byte di ordine superiore</span><span class="sxs-lookup"><span data-stu-id="c0715-118">High-order byte</span></span> | <span data-ttu-id="c0715-119">Contiene il primo byte dei dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="c0715-119">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="c0715-120">Byte di ordine inferiore</span><span class="sxs-lookup"><span data-stu-id="c0715-120">Low-order byte</span></span>  | <span data-ttu-id="c0715-121">Contiene lo stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="c0715-121">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="c0715-122">I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="c0715-122">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> <dt>

<span data-ttu-id="c0715-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="c0715-123"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="c0715-124">Ora in cui il messaggio è stato ricevuto dal driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="c0715-124">Time that the message was received by the input device driver.</span></span> <span data-ttu-id="c0715-125">Il timestamp viene specificato in millisecondi, a partire da zero quando è stata chiamata la funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="c0715-125">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0715-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0715-126">Return Value</span></span>

<span data-ttu-id="c0715-127">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="c0715-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0715-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0715-128">Remarks</span></span>

<span data-ttu-id="c0715-129">Lo stato dell'esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato; ogni messaggio viene espanso in modo da includere il byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="c0715-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="c0715-130">Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="c0715-130">This message is not sent when a MIDI system-exclusive message is received.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0715-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0715-131">Requirements</span></span>



| <span data-ttu-id="c0715-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0715-132">Requirement</span></span> | <span data-ttu-id="c0715-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c0715-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0715-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0715-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c0715-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0715-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c0715-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0715-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c0715-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0715-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c0715-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0715-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0715-139"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0715-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0715-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0715-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0715-141">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="c0715-141">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="c0715-142">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="c0715-142">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

