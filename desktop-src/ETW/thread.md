---
description: 'Classe di thread: questa classe è la classe padre per gli eventi del thread. La sintassi seguente è semplificata dal codice MOF.'
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
ms.openlocfilehash: b587441358d78d3300276ac3b59db2512f697ad95411bcc9b145df52180e4154
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813985"
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

Per abilitare gli eventi di thread in una sessione di registrazione del kernel NT, specificare il flag **EVENT \_ TRACE FLAG \_ \_ THREAD** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi del thread chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ThreadGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento del thread effettivo quando si usano gli eventi.



| Tipo di evento                                                      | Descrizione                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ END**(il valore del tipo di evento è 2)<br/>   | Evento del thread finale. La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                        |
| **EVENTO \_ TRACE \_ TYPE \_ START**(il valore del tipo di evento è 1)<br/> | Evento del thread di avvio. La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                      |
| Valore del tipo di evento, 3                                             | Evento del thread di avvio della raccolta dati. Enumera i thread attualmente in esecuzione al momento dell'avvio della sessione del kernel. La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 4                                             | Evento del thread di raccolta dati finale. Enumera i thread attualmente in esecuzione al termine della sessione del kernel. La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento.     |



 

Gli eventi di avvio del processo e del thread possono essere registrati nel contesto del processo o del thread padre. Di conseguenza, i **membri ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread da creare. Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Tipo \_ di threadGruppo1**](thread-typegroup1.md)
</dt> <dt>

[**Thread \_ V0**](thread-v0.md)
</dt> <dt>

[**Thread \_ V1**](thread-v1.md)
</dt> <dt>

[**Thread \_ V2**](thread-v2.md)
</dt> </dl>

 

 
