---
description: L' \_ enumerazione dell'evento partecipante descrive gli eventi del partecipante.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: Enumerazione PARTICIPANT_EVENT (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327491"
---
# <a name="participant_event-enumeration"></a><span data-ttu-id="bcdc2-103">\_Enumerazione evento partecipante</span><span class="sxs-lookup"><span data-stu-id="bcdc2-103">PARTICIPANT\_EVENT enumeration</span></span>

<span data-ttu-id="bcdc2-104">\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bcdc2-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="bcdc2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bcdc2-106">L'enumerazione dell' **\_ evento partecipante** descrive gli eventi del partecipante.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-106">The **PARTICIPANT\_EVENT** enum describes participant events.</span></span> <span data-ttu-id="bcdc2-107">Il metodo [**ITParticipantEvent:: Get \_ Event**](itparticipantevent-get-event.md) restituisce un membro di questa enumerazione per indicare il tipo di evento del partecipante alla conferenza che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-107">The [**ITParticipantEvent::get\_Event**](itparticipantevent-get-event.md) method returns a member of this enum to indicate the type of conference participant event that occurred.</span></span> <span data-ttu-id="bcdc2-108">Questa enumerazione viene utilizzata dalle applicazioni che accedono al [IPConf msp](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="bcdc2-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bcdc2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcdc2-109">Syntax</span></span>


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a><span data-ttu-id="bcdc2-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="bcdc2-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bcdc2-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_nuovo \_ partecipante PE**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**PE\_NEW\_PARTICIPANT**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-112">Un nuovo partecipante è stato aggiunto alla conferenza.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-112">A new participant has been added to the conference.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**\_modifica informazioni \_ PE**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE\_INFO\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-114">Le informazioni su un partecipante sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-114">Information on a participant has changed.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**\_uscita da partecipante PE \_**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE\_PARTICIPANT\_LEAVE**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-116">Un partecipante ha lasciato la conferenza.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-116">A participant has left the conference.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**\_nuovo \_ SOTTOflusso PE**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**PE\_NEW\_SUBSTREAM**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-118">Un nuovo sottoflusso è stato aggiunto al partecipante.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-118">A new substream has been added to the participant.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**\_SOTTOFLUSSO PE \_ rimosso**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**PE\_SUBSTREAM\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-120">Un nuovo sottoflusso è stato rimosso dal partecipante.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-120">A new substream has been removed from the participant.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**\_SOTTOFLUSSO PE \_ mappato**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**PE\_SUBSTREAM\_MAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-122">È stato eseguito il mapping di un partecipante a un sottoflusso.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-122">A participant has been mapped to a substream.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**sottoflusso PE non \_ \_ mappato**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE\_SUBSTREAM\_UNMAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-124">È stato annullato il mapping di un partecipante da un sottoflusso.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-124">A participant has been unmapped from a substream.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**\_timeout partecipante \_ PE**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**PE\_PARTICIPANT\_TIMEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-126">Un partecipante è stato rimosso dalla conferenza a causa di un timeout.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-126">A participant has been removed from the conference due to a timeout.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**\_partecipante PE \_ recuperato**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PE\_PARTICIPANT\_RECOVERED**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-128">Un partecipante rimosso è nuovamente visibile.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-128">A removed participant is again visible.</span></span> <span data-ttu-id="bcdc2-129">In genere, si tratta di un partecipante che ha raggiunto il timeout, ma i segnali sono ora in fase di ricezione.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-129">Usually, this is a participant who timed out but signals are now being received.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**\_partecipante PE \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**PE\_PARTICIPANT\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-131">Il partecipante è diventato attivo nella conferenza.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-131">The participant has become active in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**\_partecipante PE \_ inattivo**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE\_PARTICIPANT\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-133">Il partecipante è diventato inattivo nella conferenza.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-133">The participant has become inactive in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**\_conversazione locale \_ PE**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE\_LOCAL\_TALKING**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-135">Il partecipante locale ha iniziato a comunicare.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-135">The local participant has started to talk.</span></span>

</dd> <dt>

<span data-ttu-id="bcdc2-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE \_ locale \_ invisibile all'utente**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE\_LOCAL\_SILENT**</span></span>
</dt> <dd>

<span data-ttu-id="bcdc2-137">Il partecipante locale è diventato invisibile alla conferenza.</span><span class="sxs-lookup"><span data-stu-id="bcdc2-137">The local participant has become silent in the conference.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcdc2-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcdc2-138">Requirements</span></span>



| <span data-ttu-id="bcdc2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcdc2-139">Requirement</span></span> | <span data-ttu-id="bcdc2-140">Valore</span><span class="sxs-lookup"><span data-stu-id="bcdc2-140">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bcdc2-141">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="bcdc2-141">TAPI version</span></span><br/> | <span data-ttu-id="bcdc2-142">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="bcdc2-142">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="bcdc2-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcdc2-143">Header</span></span><br/>       | <dl> <span data-ttu-id="bcdc2-144"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcdc2-144"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcdc2-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcdc2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcdc2-146">**Evento ITParticipantEvent:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="bcdc2-146">**ITParticipantEvent::get\_Event**</span></span>](itparticipantevent-get-event.md)
</dt> <dt>

[<span data-ttu-id="bcdc2-147">MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="bcdc2-147">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="bcdc2-148">Interfacce MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="bcdc2-148">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




