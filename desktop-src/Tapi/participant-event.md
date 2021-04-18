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
# <a name="participant_event-enumeration"></a>\_Enumerazione evento partecipante

\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'enumerazione dell' **\_ evento partecipante** descrive gli eventi del partecipante. Il metodo [**ITParticipantEvent:: Get \_ Event**](itparticipantevent-get-event.md) restituisce un membro di questa enumerazione per indicare il tipo di evento del partecipante alla conferenza che si è verificato. Questa enumerazione viene utilizzata dalle applicazioni che accedono al [IPConf msp](ipconf-msp.md).

## <a name="syntax"></a>Sintassi


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_nuovo \_ partecipante PE**
</dt> <dd>

Un nuovo partecipante è stato aggiunto alla conferenza.

</dd> <dt>

<span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**\_modifica informazioni \_ PE**
</dt> <dd>

Le informazioni su un partecipante sono state modificate.

</dd> <dt>

<span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**\_uscita da partecipante PE \_**
</dt> <dd>

Un partecipante ha lasciato la conferenza.

</dd> <dt>

<span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**\_nuovo \_ SOTTOflusso PE**
</dt> <dd>

Un nuovo sottoflusso è stato aggiunto al partecipante.

</dd> <dt>

<span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**\_SOTTOFLUSSO PE \_ rimosso**
</dt> <dd>

Un nuovo sottoflusso è stato rimosso dal partecipante.

</dd> <dt>

<span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**\_SOTTOFLUSSO PE \_ mappato**
</dt> <dd>

È stato eseguito il mapping di un partecipante a un sottoflusso.

</dd> <dt>

<span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**sottoflusso PE non \_ \_ mappato**
</dt> <dd>

È stato annullato il mapping di un partecipante da un sottoflusso.

</dd> <dt>

<span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**\_timeout partecipante \_ PE**
</dt> <dd>

Un partecipante è stato rimosso dalla conferenza a causa di un timeout.

</dd> <dt>

<span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**\_partecipante PE \_ recuperato**
</dt> <dd>

Un partecipante rimosso è nuovamente visibile. In genere, si tratta di un partecipante che ha raggiunto il timeout, ma i segnali sono ora in fase di ricezione.

</dd> <dt>

<span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**\_partecipante PE \_ attivo**
</dt> <dd>

Il partecipante è diventato attivo nella conferenza.

</dd> <dt>

<span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**\_partecipante PE \_ inattivo**
</dt> <dd>

Il partecipante è diventato inattivo nella conferenza.

</dd> <dt>

<span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**\_conversazione locale \_ PE**
</dt> <dd>

Il partecipante locale ha iniziato a comunicare.

</dd> <dt>

<span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE \_ locale \_ invisibile all'utente**
</dt> <dd>

Il partecipante locale è diventato invisibile alla conferenza.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                              |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento ITParticipantEvent:: Get \_**](itparticipantevent-get-event.md)
</dt> <dt>

[MSP IPConf](ipconf-msp.md)
</dt> <dt>

[Interfacce MSP IPConf](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




