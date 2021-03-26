---
description: Questa classe è la classe padre per gli eventi del thread. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Classe Thread_V2
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
ms.openlocfilehash: f28b68a2aac5f2d5293f94ed2bab366d238ae662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882769"
---
# <a name="thread_v2-class"></a>\_Classe thread V2

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

La classe **thread \_ v2** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi del thread in una sessione di registrazione del kernel NT, specificare il flag di **thread del \_ flag di traccia \_ \_ eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . È inoltre possibile specificare i flag seguenti:

-   **\_flag di traccia evento \_ \_ CSWITCH**
-   **\_ \_ Dispatcher flag di traccia eventi \_**

I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi del thread chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ThreadGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di evento seguenti per identificare l'evento del thread effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                      | Descrizione                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ \_ \_ Fine tipo di traccia**(il valore del tipo di evento è 2)<br/>   | Evento thread finale. La classe MOF [**thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                        |
| **Evento \_ \_ \_ Inizio tipo di traccia**(il valore del tipo di evento è 1)<br/> | Evento thread di avvio. La classe MOF [**thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                      |
| Valore del tipo di evento, 3                                             | Inizio evento thread raccolta dati. Enumera i thread attualmente in esecuzione al momento dell'avvio della sessione kernel. La classe MOF [**thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 4                                             | Evento thread di raccolta dati finale. Enumera i thread attualmente in esecuzione al termine della sessione kernel. La classe MOF [**thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento.     |
| Valore del tipo di evento, 36                                            | Evento del cambio di contesto. La classe MOF [**Cswitch**](cswitch.md) definisce i dati dell'evento per questo evento.                                                                                                                                |
| Valore del tipo di evento, 50                                            | Evento thread pronto. La classe MOF [**ReadyThread**](readythread.md) definisce i dati dell'evento per questo evento.                                                                                                                          |



 

Gli eventi di avvio del processo e del thread possono essere registrati nel contesto del processo o del thread padre. Di conseguenza, i membri **ProcessID** e **ThreadID** dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread in fase di creazione. Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**CSwitch**](cswitch.md)
</dt> <dt>

[**Thread**](thread.md)
</dt> <dt>

[**\_TypeGroup1 thread**](thread-typegroup1.md)
</dt> <dt>

[**Thread \_ V0**](thread-v0.md)
</dt> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> </dl>

 

 
