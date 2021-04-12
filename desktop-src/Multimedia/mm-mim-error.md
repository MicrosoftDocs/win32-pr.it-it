---
title: Messaggio MM_MIM_ERROR (mmsystem. h)
description: Il \_ \_ messaggio di errore mm MIM viene inviato a una finestra quando viene ricevuto un messaggio MIDI non valido.
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- MM_MIM_ERROR messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b45988259601b40a804f9eb8acfbb085bddcda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119139"
---
# <a name="mm_mim_error-message"></a><span data-ttu-id="4323e-104">MM \_ \_ messaggio di errore MIM</span><span class="sxs-lookup"><span data-stu-id="4323e-104">MM\_MIM\_ERROR message</span></span>

<span data-ttu-id="4323e-105">Il messaggio di **\_ \_ errore mm MIM** viene inviato a una finestra quando viene ricevuto un messaggio MIDI non valido.</span><span class="sxs-lookup"><span data-stu-id="4323e-105">The **MM\_MIM\_ERROR** message is sent to a window when an invalid MIDI message is received.</span></span>


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="4323e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4323e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4323e-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="4323e-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="4323e-108">Handle per il dispositivo di input MIDI che ha ricevuto il messaggio non valido.</span><span class="sxs-lookup"><span data-stu-id="4323e-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="4323e-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span><span class="sxs-lookup"><span data-stu-id="4323e-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="4323e-110">Messaggio MIDI non valido.</span><span class="sxs-lookup"><span data-stu-id="4323e-110">Invalid MIDI message.</span></span> <span data-ttu-id="4323e-111">Il messaggio viene compresso in un valore **DWORD** con il primo byte del messaggio nel byte di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="4323e-111">The message is packed into a **DWORD** value with the first byte of the message in the low-order byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4323e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4323e-112">Return Value</span></span>

<span data-ttu-id="4323e-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="4323e-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4323e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4323e-114">Requirements</span></span>



| <span data-ttu-id="4323e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4323e-115">Requirement</span></span> | <span data-ttu-id="4323e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4323e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4323e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4323e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4323e-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4323e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4323e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4323e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4323e-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4323e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4323e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4323e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4323e-122"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4323e-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4323e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4323e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4323e-124">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="4323e-124">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="4323e-125">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="4323e-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





