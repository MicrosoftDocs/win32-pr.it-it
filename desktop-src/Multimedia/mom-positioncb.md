---
title: Messaggio MOM_POSITIONCB (mmsystem. h)
description: Il \_ messaggio di posizione MOM viene inviato quando \_ \_ viene raggiunto un evento di callback MEVT F nel flusso di output MIDI.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743354"
---
# <a name="mom_positioncb-message"></a><span data-ttu-id="f7b3e-104">\_Messaggio MOM POSITIONCB</span><span class="sxs-lookup"><span data-stu-id="f7b3e-104">MOM\_POSITIONCB message</span></span>

<span data-ttu-id="f7b3e-105">Il messaggio di **\_ posizione MOM** viene inviato quando viene raggiunto un evento di **\_ \_ callback MEVT F** nel flusso di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="f7b3e-105">The **MOM\_POSITION** message is sent when an **MEVT\_F\_CALLBACK** event is reached in the MIDI output stream.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7b3e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7b3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b3e-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f7b3e-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f7b3e-108">Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer di input.</span><span class="sxs-lookup"><span data-stu-id="f7b3e-108">A pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f7b3e-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f7b3e-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f7b3e-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="f7b3e-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b3e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7b3e-111">Return Value</span></span>

<span data-ttu-id="f7b3e-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="f7b3e-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b3e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7b3e-113">Remarks</span></span>

<span data-ttu-id="f7b3e-114">La riproduzione del buffer del flusso continua anche mentre la funzione di callback è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f7b3e-114">Playback of the stream buffer continues even while the callback function is executing.</span></span> <span data-ttu-id="f7b3e-115">Tutti gli eventi dopo l'evento di **\_ \_ callback F MEVT** nel buffer verranno pianificati e inviati in tempo indipendentemente dalla quantità di tempo impiegato nella funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="f7b3e-115">Any events after the **MEVT\_F\_CALLBACK** event in the buffer will be scheduled and sent on time regardless of how much time is spent in the callback function.</span></span>

<span data-ttu-id="f7b3e-116">Se i callback di posizione vengono generati più rapidamente di quanto l'applicazione possa elaborarli, il membro **dwOffset** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) può fare riferimento a un evento che l'applicazione non ha ancora elaborato.</span><span class="sxs-lookup"><span data-stu-id="f7b3e-116">If position callbacks are being generated more quickly than your application can process them, the **dwOffset** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure might refer to an event your application has not yet processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b3e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7b3e-117">Requirements</span></span>



| <span data-ttu-id="f7b3e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b3e-118">Requirement</span></span> | <span data-ttu-id="f7b3e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f7b3e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b3e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7b3e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b3e-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7b3e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f7b3e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7b3e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b3e-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f7b3e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f7b3e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7b3e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b3e-125"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7b3e-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7b3e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7b3e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b3e-127">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="f7b3e-127">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

