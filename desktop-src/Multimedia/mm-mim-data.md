---
title: Messaggio MM_MIM_DATA (mmsystem. h)
description: Il \_ \_ messaggio di dati MIM mm viene inviato a una finestra quando un messaggio MIDI completo viene ricevuto da un dispositivo di input MIDI.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- MM_MIM_DATA messaggi multimediali di Windows
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
ms.openlocfilehash: aa8c015ba5e08302f7567fe8f474bedca74d3064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047969"
---
# <a name="mm_mim_data-message"></a><span data-ttu-id="d0a10-104">MM \_ \_ messaggio dati MIM</span><span class="sxs-lookup"><span data-stu-id="d0a10-104">MM\_MIM\_DATA message</span></span>

<span data-ttu-id="d0a10-105">Il messaggio di **\_ \_ dati MIM mm** viene inviato a una finestra quando un messaggio MIDI completo viene ricevuto da un dispositivo di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="d0a10-105">The **MM\_MIM\_DATA** message is sent to a window when a complete MIDI message is received by a MIDI input device.</span></span>


```C++
MM_MIM_DATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="d0a10-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0a10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a10-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="d0a10-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="d0a10-108">Handle per il dispositivo di input MIDI che ha ricevuto il messaggio MIDI.</span><span class="sxs-lookup"><span data-stu-id="d0a10-108">Handle to the MIDI input device that received the MIDI message.</span></span>

</dd> <dt>

<span data-ttu-id="d0a10-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="d0a10-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="d0a10-110">Messaggio MIDI ricevuto.</span><span class="sxs-lookup"><span data-stu-id="d0a10-110">MIDI message that was received.</span></span> <span data-ttu-id="d0a10-111">Il messaggio viene compresso in un valore parola doppia come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="d0a10-111">The message is packed into a doubleword value as follows:</span></span>



| <span data-ttu-id="d0a10-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0a10-112">Requirement</span></span> | <span data-ttu-id="d0a10-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d0a10-113">Value</span></span> |
|-----------|-----------------|-----------------------------------------------------|
| <span data-ttu-id="d0a10-114">Parola alta</span><span class="sxs-lookup"><span data-stu-id="d0a10-114">High word</span></span> | <span data-ttu-id="d0a10-115">Byte di ordine superiore</span><span class="sxs-lookup"><span data-stu-id="d0a10-115">High-order byte</span></span> | <span data-ttu-id="d0a10-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d0a10-116">Not used.</span></span>                                           |
|           | <span data-ttu-id="d0a10-117">Byte di ordine inferiore</span><span class="sxs-lookup"><span data-stu-id="d0a10-117">Low-order byte</span></span>  | <span data-ttu-id="d0a10-118">Contiene un secondo byte di dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="d0a10-118">Contains a second byte of MIDI data (when needed).</span></span>  |
| <span data-ttu-id="d0a10-119">Parola bassa</span><span class="sxs-lookup"><span data-stu-id="d0a10-119">Low word</span></span>  | <span data-ttu-id="d0a10-120">Byte di ordine superiore</span><span class="sxs-lookup"><span data-stu-id="d0a10-120">High-order byte</span></span> | <span data-ttu-id="d0a10-121">Contiene il primo byte dei dati MIDI (quando necessario).</span><span class="sxs-lookup"><span data-stu-id="d0a10-121">Contains the first byte of MIDI data (when needed).</span></span> |
|           | <span data-ttu-id="d0a10-122">Byte di ordine inferiore</span><span class="sxs-lookup"><span data-stu-id="d0a10-122">Low-order byte</span></span>  | <span data-ttu-id="d0a10-123">Contiene lo stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="d0a10-123">Contains the MIDI status.</span></span>                           |



 

<span data-ttu-id="d0a10-124">I due byte di dati MIDI sono facoltativi, a seconda del byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="d0a10-124">The two MIDI data bytes are optional, depending on the MIDI status byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0a10-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0a10-125">Return Value</span></span>

<span data-ttu-id="d0a10-126">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="d0a10-126">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a10-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0a10-127">Remarks</span></span>

<span data-ttu-id="d0a10-128">Lo stato dell'esecuzione dei messaggi MIDI ricevuti da una porta di input MIDI è disabilitato; ogni messaggio viene espanso in modo da includere il byte di stato MIDI.</span><span class="sxs-lookup"><span data-stu-id="d0a10-128">MIDI messages received from a MIDI input port have running status disabled; each message is expanded to include the MIDI status byte.</span></span>

<span data-ttu-id="d0a10-129">Questo messaggio non viene inviato quando viene ricevuto un messaggio esclusivo del sistema MIDI.</span><span class="sxs-lookup"><span data-stu-id="d0a10-129">This message is not sent when a MIDI system-exclusive message is received.</span></span> <span data-ttu-id="d0a10-130">Nessun timestamp disponibile con questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="d0a10-130">No time stamp is available with this message.</span></span> <span data-ttu-id="d0a10-131">Per i dati di input con timestamp, è necessario utilizzare i messaggi inviati alle funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="d0a10-131">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a10-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0a10-132">Requirements</span></span>



| <span data-ttu-id="d0a10-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0a10-133">Requirement</span></span> | <span data-ttu-id="d0a10-134">Valore</span><span class="sxs-lookup"><span data-stu-id="d0a10-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a10-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0a10-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a10-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0a10-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d0a10-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0a10-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a10-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0a10-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d0a10-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0a10-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0a10-140"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0a10-140"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a10-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0a10-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a10-142">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="d0a10-142">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="d0a10-143">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="d0a10-143">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





