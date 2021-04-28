---
description: 'Registry_V1: questa classe è la classe padre per gli eventi del Registro di sistema. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 7ad92377-3fd7-47e0-b96e-bab530ea9d99
title: Registry_V1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20ef88f5bd46af116b0c04e24a3c6edd39afbcdc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106149"
---
# <a name="registry_v1-class"></a>Classe Registry \_ V1

Questa classe è la classe padre per gli eventi del Registro di sistema.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(1)]
class Registry_V1 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe Registry \_ V1** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi del Registro di sistema in una sessione di registrazione del kernel NT, specificare **EVENT \_ TRACE FLAG \_ \_ REGISTRY** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

I consumer di tracce eventi possono implementare un'elaborazione speciale per gli eventi del Registro di sistema chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando **RegistryGuid** come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento effettivo del Registro di sistema quando si utilizzano gli eventi.



| Tipo di evento                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ REGCREATE**(il valore del tipo di evento è 10)<br/>             | Creare un evento chiave. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                                     |
| **EVENTO \_ TRACE \_ TYPE \_ REGDELETE**(il valore del tipo di evento è 12)<br/>             | Evento di eliminazione del tasto. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                                     |
| **EVENTO \_ TRACE \_ TYPE \_ REGDELETEVALUE**(il valore del tipo di evento è 15)<br/>        | Evento delete value. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                                   |
| **EVENTO \_ TRACE \_ TYPE \_ REGENUMERATEKEY**(il valore del tipo di evento è 17)<br/>       | Enumerare l'evento chiave. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                                  |
| **EVENTO \_ TRACE \_ TYPE \_ REGENUMERATEVALUEKEY**(il valore del tipo di evento è 18)<br/>  | Enumerare l'evento chiave del valore. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                            |
| **EVENTO \_ TRACE \_ TYPE \_ REGFLUSH**(il valore del tipo di evento è 21)<br/>              | Evento del tasto di scaricamento. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                                      |
| **EVENTO \_ TRACE \_ TYPE \_ REGKCBDMP**(il valore del tipo di evento è 22)<br/>             | Generato quando un'operazione del Registro di sistema usa handle anziché stringhe per fare riferimento alle sottochiavi. Questi eventi vengono registrati una volta per ogni handle, la prima volta che viene fatto riferimento all'handle. I riferimenti ripetuti all'handle non generano più eventi.<br/> La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.<br/> **Windows 2000:** Questo valore non è supportato.<br/> |
| **EVENTO \_ TRACE \_ TYPE \_ REGOPEN**(il valore del tipo di evento è 11)<br/>               | Evento chiave di apertura. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                                       |
| **EVENTO \_ TRACE \_ TYPE \_ REGQUERY**(il valore del tipo di evento è 13)<br/>              | Evento chiave di query. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                                      |
| **EVENTO \_ TRACE \_ TYPE \_ REGQUERYMULTIPLEVALUE**(il valore del tipo di evento è 19)<br/> | Eseguire query su un evento con più valori. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                           |
| **EVENTO \_ TRACE \_ TYPE \_ REGQUERYVALUE**(il valore del tipo di evento è 16)<br/>         | Evento del valore della query. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                                    |
| **EVENTO \_ TRACE \_ TYPE \_ REGSETINFORMATION**(il valore del tipo di evento è 20)<br/>     | Evento di impostazione delle informazioni. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                                |
| **EVENTO \_ TRACE \_ TYPE \_ REGSETVALUE**(il valore del tipo di evento è 14)<br/>           | Impostare l'evento value. La [**classe \_ MOF Registry TypeGroup1**](registry-typegroup1.md) definisce i dati dell'evento.                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Registro**](registry.md)
</dt> <dt>

[**Registro \_ di sistema V0**](registry-v0.md)
</dt> <dt>

[**\_TypeGroup1 del Registro di sistema \_ V1**](registry-v1-typegroup1.md)
</dt> </dl>

 

 
