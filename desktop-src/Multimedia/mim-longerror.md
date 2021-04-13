---
title: Messaggio MIM_LONGERROR (mmsystem. h)
description: Il \_ messaggio LONGERROR MIM viene inviato a una funzione di callback input MIDI quando viene ricevuto un messaggio esclusivo del sistema MIDI non valido o incompleto.
ms.assetid: 7e3b0716-33c4-449c-a200-e5ba72428dc1
keywords:
- MIM_LONGERROR messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631c4fdcd31eef01d691aea80100427d116ae7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475509"
---
# <a name="mim_longerror-message"></a><span data-ttu-id="de109-104">\_Messaggio LONGERROR MIM</span><span class="sxs-lookup"><span data-stu-id="de109-104">MIM\_LONGERROR message</span></span>

<span data-ttu-id="de109-105">Il **messaggio \_ LONGERROR MIM** viene inviato a una funzione di callback input MIDI quando viene ricevuto un messaggio esclusivo del sistema MIDI non valido o incompleto.</span><span class="sxs-lookup"><span data-stu-id="de109-105">The **MIM\_LONGERROR** message is sent to a MIDI input callback function when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MIM_LONGERROR 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a><span data-ttu-id="de109-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de109-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de109-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="de109-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="de109-108">Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer contenente il messaggio non valido.</span><span class="sxs-lookup"><span data-stu-id="de109-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="de109-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span><span class="sxs-lookup"><span data-stu-id="de109-109"><span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*</span></span>
</dt> <dd>

<span data-ttu-id="de109-110">Tempo durante il quale i dati sono stati ricevuti dal driver di dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="de109-110">Time that the data was received by the input device driver.</span></span> <span data-ttu-id="de109-111">Il timestamp viene specificato in millisecondi, a partire da zero quando è stata chiamata la funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) .</span><span class="sxs-lookup"><span data-stu-id="de109-111">The time stamp is specified in milliseconds, beginning at zero when the [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function was called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de109-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de109-112">Return Value</span></span>

<span data-ttu-id="de109-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="de109-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de109-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="de109-114">Remarks</span></span>

<span data-ttu-id="de109-115">Il buffer restituito potrebbe non essere pieno.</span><span class="sxs-lookup"><span data-stu-id="de109-115">The returned buffer might not be full.</span></span> <span data-ttu-id="de109-116">Per determinare il numero di byte registrati nel buffer restituito, usare il membro **dwBytesRecorded** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) specificata da *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="de109-116">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="de109-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de109-117">Requirements</span></span>



| <span data-ttu-id="de109-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="de109-118">Requirement</span></span> | <span data-ttu-id="de109-119">Valore</span><span class="sxs-lookup"><span data-stu-id="de109-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de109-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de109-120">Minimum supported client</span></span><br/> | <span data-ttu-id="de109-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de109-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="de109-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de109-122">Minimum supported server</span></span><br/> | <span data-ttu-id="de109-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de109-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="de109-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de109-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="de109-125"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de109-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de109-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de109-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de109-127">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="de109-127">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="de109-128">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="de109-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

