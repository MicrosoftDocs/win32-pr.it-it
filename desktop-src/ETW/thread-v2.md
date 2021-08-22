---
description: 'Thread_V2 classe: questa classe è la classe padre per gli eventi del thread. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Thread_V2 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: d057f80d5cf29f6660ee3a2ebd651c468496529a56a11147225ebd504451184c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069391"
---
# <a name="thread_v2-class"></a>Classe \_ Thread V2

Questa classe è la classe padre per gli eventi del thread.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe Thread \_ V2** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di thread in una sessione di registrazione del kernel NT, specificare il flag **EVENT \_ TRACE FLAG \_ \_ THREAD** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) È anche possibile specificare i flag seguenti:

-   **FLAG \_ DI TRACCIA EVENTI \_ \_ CSWITCH**
-   **\_DISPATCHER DEL FLAG DI TRACCIA \_ \_ EVENTI**

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi del thread chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ThreadGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento del thread effettivo durante l'utilizzo degli eventi.



| Tipo di evento                                                      | Descrizione                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ END**(il valore del tipo di evento è 2)<br/>   | Evento del thread finale. La [**classe MOF \_ Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                        |
| **EVENTO \_ TRACE \_ TYPE \_ START**(il valore del tipo di evento è 1)<br/> | Evento del thread di avvio. La [**classe MOF \_ Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                      |
| Valore del tipo di evento, 3                                             | Evento del thread di avvio della raccolta dati. Enumera i thread attualmente in esecuzione al momento dell'avvio della sessione del kernel. La [**classe MOF \_ Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 4                                             | Evento del thread di raccolta dati finale. Enumera i thread attualmente in esecuzione al termine della sessione del kernel. La [**classe MOF \_ Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento.     |
| Valore del tipo di evento, 36                                            | Evento di cambio di contesto. La classe MOF [**CSwitch**](cswitch.md) definisce i dati dell'evento per questo evento.                                                                                                                                |
| Valore del tipo di evento, 50                                            | Evento del thread pronto. La [**classe MOF ReadyThread**](readythread.md) definisce i dati dell'evento per questo evento.                                                                                                                          |



 

Gli eventi di avvio di processi e thread possono essere registrati nel contesto del processo o del thread padre. Di conseguenza, i **membri ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread da creare. Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**CSwitch**](cswitch.md)
</dt> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**Tipo \_ di threadGruppo1**](thread-typegroup1.md)
</dt> <dt>

[**Thread \_ V0**](thread-v0.md)
</dt> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> </dl>

 

 
