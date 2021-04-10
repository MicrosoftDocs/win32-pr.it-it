---
title: Messaggio MM_MIM_LONGDATA (mmsystem. h)
description: Il \_ \_ messaggio LONGDATA in mm MIM viene inviato a una finestra quando viene ricevuto un messaggio esclusivo del sistema MIDI completo o quando un buffer è stato riempito con dati esclusivi del sistema.
ms.assetid: 72b9eade-4224-436f-bfef-32204eaf51ae
keywords:
- MM_MIM_LONGDATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIM_LONGDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf1900ef2e9394b9d8772747eba873f8d607f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121254"
---
# <a name="mm_mim_longdata-message"></a><span data-ttu-id="3b181-104">MM \_ \_ messaggio LONGDATA MIM</span><span class="sxs-lookup"><span data-stu-id="3b181-104">MM\_MIM\_LONGDATA message</span></span>

<span data-ttu-id="3b181-105">Il **messaggio \_ \_ LONGDATA in mm MIM** viene inviato a una finestra quando viene ricevuto un messaggio esclusivo del sistema MIDI completo o quando un buffer è stato riempito con dati esclusivi del sistema.</span><span class="sxs-lookup"><span data-stu-id="3b181-105">The **MM\_MIM\_LONGDATA** message is sent to a window when either a complete MIDI system-exclusive message is received or when a buffer has been filled with system-exclusive data.</span></span>


```C++
MM_MIM_LONGDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="3b181-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b181-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b181-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="3b181-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="3b181-108">Handle per il dispositivo di input MIDI che ha ricevuto i dati.</span><span class="sxs-lookup"><span data-stu-id="3b181-108">Handle to the MIDI input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="3b181-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="3b181-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="3b181-110">Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer.</span><span class="sxs-lookup"><span data-stu-id="3b181-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b181-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b181-111">Return Value</span></span>

<span data-ttu-id="3b181-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="3b181-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b181-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b181-113">Remarks</span></span>

<span data-ttu-id="3b181-114">Il buffer restituito potrebbe non essere pieno.</span><span class="sxs-lookup"><span data-stu-id="3b181-114">The returned buffer might not be full.</span></span> <span data-ttu-id="3b181-115">Per determinare il numero di byte registrati nel buffer restituito, usare il membro **dwBytesRecorded** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) a cui punta *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="3b181-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure pointed to by *lpMidiHdr*.</span></span>

<span data-ttu-id="3b181-116">Nessun timestamp disponibile con questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="3b181-116">No time stamp is available with this message.</span></span> <span data-ttu-id="3b181-117">Per i dati di input con timestamp, è necessario utilizzare i messaggi inviati alle funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="3b181-117">For time-stamped input data, you must use the messages that are sent to callback functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b181-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b181-118">Requirements</span></span>



| <span data-ttu-id="3b181-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b181-119">Requirement</span></span> | <span data-ttu-id="3b181-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3b181-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b181-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b181-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b181-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3b181-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3b181-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b181-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b181-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3b181-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3b181-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b181-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b181-126"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b181-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b181-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b181-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b181-128">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="3b181-128">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="3b181-129">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="3b181-129">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

