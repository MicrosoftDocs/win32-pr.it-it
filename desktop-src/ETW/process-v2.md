---
description: Questa classe è la classe padre per gli eventi di elaborazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Classe Process_V2
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
ms.openlocfilehash: c055dc1f78da13c0dfa29bea948a8f0c94363ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968241"
---
# <a name="process_v2-class"></a>\_Classe processo V2

Questa classe è la classe padre per gli eventi di elaborazione.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **Process** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di elaborazione in una sessione di registrazione del kernel NT, specificare il flag di **processo del \_ flag di traccia \_ \_ eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . È anche possibile specificare il flag seguente:

-   **\_ \_ \_ contatori processo flag di traccia eventi \_**

I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di elaborazione chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ProcessGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di evento seguenti per identificare l'evento del processo effettivo durante l'utilizzo di eventi.



| Tipo di evento                                                      | Descrizione                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ \_ \_ Fine tipo di traccia**(il valore del tipo di evento è 2)<br/>   | Evento del processo finale. La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                          |
| **Evento \_ \_ \_ Inizio tipo di traccia**(il valore del tipo di evento è 1)<br/> | Evento di avvio processo. La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                        |
| Valore del tipo di evento, 3                                             | Avviare l'evento del processo di raccolta dati. Enumera i processi attualmente in esecuzione al momento dell'avvio della sessione kernel. La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 4                                             | Fine evento di elaborazione raccolta dati. Enumera i processi attualmente in esecuzione al termine della sessione kernel. La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.     |
| Valore del tipo di evento, 32                                            | Evento dei contatori delle prestazioni. La classe MOF [**Process \_ v2 \_ TypeGroup2**](process-v2-typegroup2.md) definisce i dati dell'evento per questo evento.                                                                                          |
| Valore del tipo di evento, 33                                            | Riepilogo dei contatori delle prestazioni all'inizio della sessione. La classe MOF [**Process \_ v2 \_ TypeGroup2**](process-v2-typegroup2.md) definisce i dati dell'evento per questo evento.                                                     |
| Valore del tipo di evento, 39                                            | Evento del processo inattivo. La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                      |



 

Gli eventi di avvio del processo e del thread possono essere registrati nel contesto del processo o del thread padre. Di conseguenza, i membri **ProcessID** e **ThreadID** dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread in fase di creazione. Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>       |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**Processo**](process.md)
</dt> <dt>

[**Elabora \_ TypeGroup1**](process-typegroup1.md)
</dt> <dt>

[**Processo \_ V0**](process-v0.md)
</dt> <dt>

[**Processo \_ V1**](process-v1.md)
</dt> </dl>

 

 
