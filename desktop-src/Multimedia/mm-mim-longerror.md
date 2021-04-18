---
title: Messaggio MM_MIM_LONGERROR (mmsystem. h)
description: '\_ \_ Quando viene ricevuto un messaggio esclusivo del sistema MIDI non valido o incompleto, il messaggio LONGERROR MIM viene inviato a una finestra.'
ms.assetid: 2de4c2f8-2ded-4994-934c-6e72c95637b2
keywords:
- MM_MIM_LONGERROR messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIM_LONGERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e274faca26a90a5cd3b3915a7e8e1ed27bcfd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302261"
---
# <a name="mm_mim_longerror-message"></a><span data-ttu-id="6871d-104">MM \_ \_ messaggio LONGERROR MIM</span><span class="sxs-lookup"><span data-stu-id="6871d-104">MM\_MIM\_LONGERROR message</span></span>

<span data-ttu-id="6871d-105">Quando viene ricevuto un messaggio esclusivo del sistema MIDI non valido o incompleto, il messaggio **\_ \_ LONGERROR MIM** viene inviato a una finestra.</span><span class="sxs-lookup"><span data-stu-id="6871d-105">The **MM\_MIM\_LONGERROR** message is sent to a window when an invalid or incomplete MIDI system-exclusive message is received.</span></span>


```C++
MM_MIM_LONGERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="6871d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6871d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6871d-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="6871d-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="6871d-108">Handle per il dispositivo di input MIDI che ha ricevuto il messaggio non valido.</span><span class="sxs-lookup"><span data-stu-id="6871d-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="6871d-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="6871d-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="6871d-110">Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer contenente il messaggio non valido.</span><span class="sxs-lookup"><span data-stu-id="6871d-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer containing the invalid message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6871d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6871d-111">Return Value</span></span>

<span data-ttu-id="6871d-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="6871d-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6871d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6871d-113">Remarks</span></span>

<span data-ttu-id="6871d-114">Il buffer restituito potrebbe non essere pieno.</span><span class="sxs-lookup"><span data-stu-id="6871d-114">The returned buffer might not be full.</span></span> <span data-ttu-id="6871d-115">Per determinare il numero di byte registrati nel buffer restituito, usare il membro **dwBytesRecorded** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) specificata da *lpMidiHdr*.</span><span class="sxs-lookup"><span data-stu-id="6871d-115">To determine the number of bytes recorded into the returned buffer, use the **dwBytesRecorded** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure specified by *lpMidiHdr*.</span></span>

## <a name="requirements"></a><span data-ttu-id="6871d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6871d-116">Requirements</span></span>



| <span data-ttu-id="6871d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6871d-117">Requirement</span></span> | <span data-ttu-id="6871d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6871d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6871d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6871d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6871d-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6871d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6871d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6871d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6871d-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6871d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6871d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6871d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6871d-124"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6871d-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6871d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6871d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6871d-126">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="6871d-126">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="6871d-127">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="6871d-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

