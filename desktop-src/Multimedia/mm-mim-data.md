---
title: MM_MIM_DATA messaggio (Mmsystem.h)
description: Il messaggio MM \_ MIM \_ DATA viene inviato a una finestra quando un messaggio MIDI completo viene ricevuto da un dispositivo di input MIDI.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA messaggio Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a79a5a4ab6b0422705fe737ba3da4a6fd4f923
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119696"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="5407c-104">Messaggio MM \_ MIM \_ DATA</span><span class="sxs-lookup"><span data-stu-id="5407c-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="5407c-105">Il **messaggio MM \_ MIM \_ DATA** viene inviato a una finestra quando un messaggio MIDI completo viene ricevuto da un dispositivo di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="5407c-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="5407c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5407c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5407c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="5407c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="5407c-108">Handle per il dispositivo di input MIDI che ha ricevuto il messaggio MIDI.</span><span class="sxs-lookup"><span data-stu-id="5407c-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="5407c-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="5407c-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="5407c-110">Messaggio MIDI ricevuto.</span><span class="sxs-lookup"><span data-stu-id="5407c-110">MIDI message that was received.</span></span> <span data-ttu-id="5407c-111">Il messaggio viene inserito in un valore doubleword come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="5407c-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="5407c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5407c-112">Requirement</span></span> | <span data-ttu-id="5407c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="5407c-113">Value</span></span> | <span data-ttu-id="5407c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5407c-114">Description</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="5407c-115">Parola alta</span><span class="sxs-lookup"><span data-stu-id="5407c-115">High word</span></span> | <span data-ttu-id="5407c-116">Byte di ordine elevato</span><span class="sxs-lookup"><span data-stu-id="5407c-116">High-order byte</span></span> | <span data-ttu-id="5407c-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="5407c-117">Not used.</span></span>                                           |
|           | <span data-ttu-id="5407c-118">Byte in ordine ridotto</span><span class="sxs-lookup"><span data-stu-id="5407c-118">Low-order byte</span></span>  | <span data-ttu-id="5407c-119">Contiene un secondo byte di dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="5407c-119">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="5407c-120">Parola bassa</span><span class="sxs-lookup"><span data-stu-id="5407c-120">Low word</span></span>  | <span data-ttu-id="5407c-121">Byte di ordine elevato</span><span class="sxs-lookup"><span data-stu-id="5407c-121">High-order byte</span></span> | <span data-ttu-id="5407c-122">Contiene il primo byte di dati MIDI (se necessario).</span><span class="sxs-lookup"><span data-stu-id="5407c-122">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="5407c-123">Byte in ordine ridotto</span><span class="sxs-lookup"><span data-stu-id="5407c-123">Low-order byte</span></span>  | <span data-ttu-id="5407c-124">Contiene lo stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="5407c-124">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="5407c-125">I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="5407c-125">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5407c-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5407c-126">Return Value</span></span>

<span data-ttu-id="5407c-127">Questo messaggio non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5407c-127">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5407c-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5407c-128">Remarks</span></span>

<span data-ttu-id="5407c-129">Lo stato di esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato. ogni messaggio viene espanso per includere il byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="5407c-129">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="5407c-130">Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo di sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="5407c-130">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="5407c-131">Con questo messaggio non è disponibile alcun timestamp.</span><span class="sxs-lookup"><span data-stu-id="5407c-131">No time stamp is available with this message.</span></span> <span data-ttu-id="5407c-132">Per i dati di input con timestamp, è necessario usare i messaggi inviati alle funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="5407c-132">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5407c-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5407c-133">Requirements</span></span>



| <span data-ttu-id="5407c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5407c-134">Requirement</span></span> | <span data-ttu-id="5407c-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5407c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5407c-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5407c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5407c-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5407c-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5407c-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5407c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5407c-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5407c-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5407c-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5407c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5407c-141"><dt>Mmsystem.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5407c-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5407c-142">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5407c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5407c-143">MidI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="5407c-143">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="5407c-144">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="5407c-144">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





