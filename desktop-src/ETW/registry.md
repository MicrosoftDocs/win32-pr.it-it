---
description: 'Classe Registry: questa classe è la classe padre per gli eventi del Registro di sistema. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 362d7653-1ba0-45b7-80f3-0fccca0badf1
title: Classe Registry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23cd59e8d6afeb7578bd65625741caaae8156066
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106129"
---
# <a name="registry-class"></a>Classe Registry

Questa classe è la classe padre per gli eventi del Registro di sistema.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(2)]
class Registry : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe Registry** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi del Registro di sistema in una sessione di registrazione del kernel NT, specificare **EVENT \_ TRACE FLAG \_ \_ REGISTRY** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi del Registro di sistema chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**RegistryGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento effettivo del Registro di sistema quando si utilizzano gli eventi.



| Tipo di evento                                                                       | Descrizione                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ REGCREATE**(il valore del tipo di evento è 10)<br/>             | Creare un evento chiave. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                            |
| **EVENTO \_ TRACE \_ TYPE \_ REGDELETE**(il valore del tipo di evento è 12)<br/>             | Evento di eliminazione del tasto. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                            |
| **EVENTO \_ TRACE \_ TYPE \_ REGDELETEVALUE**(il valore del tipo di evento è 15)<br/>        | Evento delete value. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                          |
| **EVENTO \_ TRACE \_ TYPE \_ REGENUMERATEKEY**(il valore del tipo di evento è 17)<br/>       | Enumerare l'evento chiave. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                         |
| **EVENTO \_ TRACE \_ TYPE \_ REGENUMERATEVALUEKEY**(il valore del tipo di evento è 18)<br/>  | Enumerare l'evento chiave del valore. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                   |
| **EVENTO \_ TRACE \_ TYPE \_ REGFLUSH**(il valore del tipo di evento è 21)<br/>              | Evento del tasto di scaricamento. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                             |
| **EVENTO \_ TRACE \_ TYPE \_ REGKCBDMP**(il valore del tipo di evento è 22)<br/>             | Creare un evento chiave. Generato quando un'operazione del Registro di sistema usa handle anziché stringhe per fare riferimento alle sottochiavi. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento per questo evento. |
| **EVENTO \_ TRACE \_ TYPE \_ REGOPEN**(il valore del tipo di evento è 11)<br/>               | Evento open key. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                              |
| **EVENTO \_ TRACE \_ TYPE \_ REGQUERY**(il valore del tipo di evento è 13)<br/>              | Evento del tasto di query. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                             |
| **EVENTO \_ TRACE \_ TYPE \_ REGQUERYMULTIPLEVALUE**(il valore del tipo di evento è 19)<br/> | Eseguire query su un evento con più valori. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                  |
| **EVENTO \_ TRACE \_ TYPE \_ REGQUERYVALUE**(il valore del tipo di evento è 16)<br/>         | Evento del valore di query. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                           |
| **EVENTO \_ TRACE \_ TYPE \_ REGSETINFORMATION**(il valore del tipo di evento è 20)<br/>     | Evento di impostazione delle informazioni. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                       |
| **EVENTO \_ TRACE \_ TYPE \_ REGSETVALUE**(il valore del tipo di evento è 14)<br/>           | Evento di impostazione del valore. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                             |
| Valore del tipo di evento, 23                                                             | delete key event. Generato quando un'operazione del Registro di sistema usa handle anziché stringhe per fare riferimento alle sottochiavi. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento. |
| Valore del tipo di evento, 24                                                             | Enumera le chiavi del Registro di sistema aperte all'inizio della sessione. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                           |
| Valore del tipo di evento, 25                                                             | Enumera le chiavi del Registro di sistema aperte alla fine della sessione. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                  |
| Valore del tipo di evento, 26                                                             | La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                              |
| Valore del tipo di evento, 27                                                             | Evento open key. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows \[ Vista\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Tipo \_ del Registro di sistemaGruppo1**](registry-typegroup1.md)
</dt> <dt>

[**Registro \_ di sistema V0**](registry-v0.md)
</dt> <dt>

[**Registro \_ di sistema V1**](registry-v1.md)
</dt> </dl>

 

 
