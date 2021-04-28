---
description: 'Process_V2 classe : questa classe è la classe padre per gli eventi del processo. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Process_V2 classe
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
ms.openlocfilehash: 77d700e7847d0ad19a019985a4e19343ce8f383d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106299"
---
# <a name="process_v2-class"></a>Classe \_ Process V2

Questa classe è la classe padre per gli eventi del processo.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
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
| Valore del tipo di evento, 32                                            | Evento dei contatori delle prestazioni. La [**classe \_ MOF Process V2 \_ TypeGroup2**](process-v2-typegroup2.md) definisce i dati dell'evento per questo evento.                                                                                          |
| Valore del tipo di evento, 33                                            | Rundown dei contatori delle prestazioni all'inizio della sessione. La [**classe \_ MOF Process V2 \_ TypeGroup2**](process-v2-typegroup2.md) definisce i dati dell'evento per questo evento.                                                     |
| Valore del tipo di evento, 39                                            | Evento del processo non in corso. La [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                      |



 

Gli eventi di avvio del processo e del thread possono essere registrati nel contesto del processo o del thread padre. Di conseguenza, i **membri ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread da creare. Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista \[ \| app UWP\]<br/>       |
| Server minimo supportato<br/> | App UWP per app desktop di Windows Server 2008 \[ \|\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Processo**](process.md)
</dt> <dt>

[**Process \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Processo \_ V0**](process-v0.md)
</dt> <dt>

[**Processo \_ V1**](process-v1.md)
</dt> </dl>

 

 
