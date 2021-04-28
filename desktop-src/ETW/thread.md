---
description: 'Classe di thread: questa classe è la classe padre per gli eventi di thread. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: 121a8d4aa04017011648d80329ee02396582987a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105529"
---
# <a name="thread-class"></a>Thread (classe)

Questa classe è la classe padre per gli eventi del thread.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe Thread** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi del thread in una sessione di registrazione del kernel NT, specificare il flag **EVENT \_ TRACE FLAG \_ \_ THREAD** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi del thread chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ThreadGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento del thread effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                      | Descrizione                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ END**(il valore del tipo di evento è 2)<br/>   | Evento del thread finale. La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                        |
| **EVENTO \_ TRACE \_ TYPE \_ START**(il valore del tipo di evento è 1)<br/> | Evento del thread di avvio. La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                      |
| Valore del tipo di evento, 3                                             | Avviare l'evento del thread di raccolta dati. Enumera i thread attualmente in esecuzione al momento dell'avvio della sessione del kernel. La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 4                                             | Evento del thread di raccolta dati finale. Enumera i thread attualmente in esecuzione al termine della sessione del kernel. La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento.     |



 

Gli eventi di avvio di processi e thread possono essere registrati nel contesto del processo o del thread padre. Di conseguenza, i **membri ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread da creare. Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Thread \_ TypeGroup1**](thread-typegroup1.md)
</dt> <dt>

[**Thread \_ V0**](thread-v0.md)
</dt> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> <dt>

[**Thread \_ V2**](thread-v2.md)
</dt> </dl>

 

 
