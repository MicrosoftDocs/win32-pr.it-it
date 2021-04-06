---
title: Messaggio MM_MOM_POSITIONCB (mmsystem. h)
description: Il \_ messaggio mm MOM \_ POSITIONCB viene inviato a una finestra quando \_ viene raggiunto un evento di callback F MEVT \_ nel flusso di output MIDI.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963823"
---
# <a name="mm_mom_positioncb-message"></a><span data-ttu-id="b64bc-104">MM \_ \_ POSITIONCB messaggio MOM</span><span class="sxs-lookup"><span data-stu-id="b64bc-104">MM\_MOM\_POSITIONCB message</span></span>

<span data-ttu-id="b64bc-105">Il messaggio **mm \_ MOM \_ POSITIONCB** viene inviato a una finestra quando \_ viene raggiunto un evento di callback F MEVT \_ nel flusso di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="b64bc-105">The **MM\_MOM\_POSITIONCB** message is sent to a window when an MEVT\_F\_CALLBACK event is reached in the MIDI output stream.</span></span>


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b64bc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b64bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64bc-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="b64bc-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="b64bc-108">Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica l'evento che ha causato il callback.</span><span class="sxs-lookup"><span data-stu-id="b64bc-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure that identifies the event that caused the callback.</span></span> <span data-ttu-id="b64bc-109">Il membro **dwOffset** restituisce l'offset dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b64bc-109">The **dwOffset** member gives the offset of the event.</span></span>

</dd> <dt>

<span data-ttu-id="b64bc-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b64bc-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b64bc-111">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="b64bc-111">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b64bc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b64bc-112">Return Value</span></span>

<span data-ttu-id="b64bc-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="b64bc-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b64bc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b64bc-114">Remarks</span></span>

<span data-ttu-id="b64bc-115">La riproduzione del buffer del flusso continua anche mentre la funzione di callback è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b64bc-115">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="b64bc-116">Tutti gli eventi dopo l' \_ \_ evento di callback F MEVT nel buffer verranno pianificati e inviati in tempo indipendentemente dalla quantità di tempo impiegato nella funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="b64bc-116">Any events after the MEVT\_F\_CALLBACK event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="b64bc-117">Se i callback di posizione vengono generati più rapidamente di quanto l'applicazione possa elaborarli, il membro **dwOffset** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) può fare riferimento a un evento che l'applicazione non ha ancora elaborato.</span><span class="sxs-lookup"><span data-stu-id="b64bc-117">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b64bc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b64bc-118">Requirements</span></span>



| <span data-ttu-id="b64bc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b64bc-119">Requirement</span></span> | <span data-ttu-id="b64bc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b64bc-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b64bc-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b64bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b64bc-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b64bc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b64bc-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b64bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b64bc-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b64bc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b64bc-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b64bc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b64bc-126"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b64bc-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b64bc-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b64bc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64bc-128">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="b64bc-128">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

