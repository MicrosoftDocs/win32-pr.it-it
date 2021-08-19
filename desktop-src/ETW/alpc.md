---
description: Questa classe è la classe padre per gli eventi di chiamata di routine locali avanzati. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: Classe ALPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 435b55c44f06b6be062653a45e14a1a890e026371d8bd8e649c87ce3542118c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070291"
---
# <a name="alpc-class"></a>Classe ALPC

Questa classe è la classe padre per gli eventi di chiamata di routine locali avanzati.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe ALPC** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare eventi di chiamata di routine locali avanzati in una sessione di registrazione del kernel NT, specificare il flag **\_ \_ \_ ALPC EVENT TRACE FLAG** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi ALPC chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ALPCGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento ALPC effettivo quando si utilizzano gli eventi.



| Tipo di evento           | Descrizione                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore del tipo di evento, 33 | Inviare un evento di messaggio. La [**classe MOF ALPC \_ Send \_ Message**](alpc-send-message.md) definisce i dati dell'evento.                           |
| Valore del tipo di evento, 34 | Ricevere un evento di messaggio. La [**classe MOF ALPC \_ Receive \_ Message**](alpc-receive-message.md) definisce i dati dell'evento.                  |
| Valore del tipo di evento, 35 | Attendere l'evento di risposta. La [**classe MOF ALPC \_ Wait For \_ \_ Reply**](alpc-wait-for-reply.md) definisce i dati dell'evento per questo evento.                    |
| Valore del tipo di evento, 36 | Attendere il nuovo evento del messaggio. La [**classe MOF ALPC \_ Wait For New \_ \_ \_ Message**](alpc-wait-for-new-message.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 37 | Arresta evento in attesa. La [**classe MOF ALPC \_ Unwait**](alpc-unwait.md) definisce i dati dell'evento per questo evento.                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

