---
description: 'Classe di processo: questa classe è la classe padre per gli eventi del processo. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Classe Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: 25c21e5f301d88f3790900c70873d9485161f5041d28bb1a30f3bb85082a9bd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069901"
---
# <a name="process-class"></a>Classe Process

Questa classe è la classe padre per gli eventi del processo.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe Process** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di elaborazione in una sessione di registrazione del kernel NT, specificare il flag **EVENT \_ TRACE FLAG \_ \_ PROCESS** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) È anche possibile specificare il flag seguente:

-   **CONTATORI \_ DEI PROCESSI DEI FLAG DI TRACCIA \_ \_ \_ EVENTI**

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi del processo chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ProcessGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento di processo effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                      | Descrizione                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ END**(il valore del tipo di evento è 2)<br/>   | Evento di fine processo. La [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                          |
| **EVENTO \_ TRACE \_ TYPE \_ START**(il valore del tipo di evento è 1)<br/> | Evento di avvio del processo. La [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                        |
| Valore del tipo di evento, 3                                             | Evento di avvio del processo di raccolta dati. Enumera i processi attualmente in esecuzione al momento dell'avvio della sessione del kernel. La [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 4                                             | Evento del processo di raccolta dati finale. Enumera i processi attualmente in esecuzione al termine della sessione del kernel. La [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.     |



 

Gli eventi di avvio di processi e thread possono essere registrati nel contesto del processo o del thread padre. Di conseguenza, i **membri ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread da creare. Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>       |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Process \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Processo \_ V0**](process-v0.md)
</dt> <dt>

[**Processo \_ V1**](process-v1.md)
</dt> <dt>

[**Processo \_ V2**](process-v2.md)
</dt> </dl>

 

 
