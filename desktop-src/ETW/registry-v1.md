---
description: Questa classe è la classe padre per gli eventi del registro di sistema. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7ad92377-3fd7-47e0-b96e-bab530ea9d99
title: Classe Registry_V1
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
ms.openlocfilehash: 320a2bce9213228be4ff5c1880d884ee9622b68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977810"
---
# <a name="registry_v1-class"></a>Classe registro di sistema \_ V1

Questa classe è la classe padre per gli eventi del registro di sistema.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(1)]
class Registry_V1 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **Registry \_ V1** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi del registro di sistema in una sessione di registrazione del kernel NT, specificare il  **Registro di sistema dei \_ \_ flag \_ di traccia eventi** nel membro EnableFlags di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi del registro di sistema chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando **RegistryGuid** come parametro *pGuid* . Usare i tipi di eventi seguenti per identificare l'evento del registro di sistema effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ Tipo di traccia \_ \_ REGCREATE**(il valore del tipo di evento è 10)<br/>             | Crea evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                                     |
| **Evento \_ Tipo di traccia \_ \_ REGDELETE**(il valore del tipo di evento è 12)<br/>             | Elimina evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                                     |
| **Evento \_ Tipo di traccia \_ \_ REGDELETEVALUE**(il valore del tipo di evento è 15)<br/>        | Evento Delete value. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                                   |
| **Evento \_ Tipo di traccia \_ \_ REGENUMERATEKEY**(il valore del tipo di evento è 17)<br/>       | Enumera evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                                  |
| **Evento \_ Tipo di traccia \_ \_ REGENUMERATEVALUEKEY**(il valore del tipo di evento è 18)<br/>  | Enumera evento chiave valore. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                            |
| **Evento \_ Tipo di traccia \_ \_ REGFLUSH**(il valore del tipo di evento è 21)<br/>              | Scarica evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                                      |
| **Evento \_ Tipo di traccia \_ \_ REGKCBDMP**(il valore del tipo di evento è 22)<br/>             | Generato quando un'operazione del registro di sistema utilizza handle anziché stringhe per fare riferimento a sottochiavi. Questi eventi vengono registrati una volta per ogni handle, la prima volta che si fa riferimento all'handle. I riferimenti ripetuti all'handle non generano più eventi.<br/> La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.<br/> **Windows 2000:** Questo valore non è supportato.<br/> |
| **Evento \_ Tipo di traccia \_ \_ REGOPEN**(il valore del tipo di evento è 11)<br/>               | Apri evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                                       |
| **Evento \_ Tipo di traccia \_ \_ REGQUERY**(il valore del tipo di evento è 13)<br/>              | Evento chiave di query. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                                      |
| **Evento \_ Tipo di traccia \_ \_ REGQUERYMULTIPLEVALUE**(il valore del tipo di evento è 19)<br/> | Eseguire una query su un evento a più valori. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                           |
| **Evento \_ Tipo di traccia \_ \_ REGQUERYVALUE**(il valore del tipo di evento è 16)<br/>         | Evento valore query. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                                    |
| **Evento \_ Tipo di traccia \_ \_ REGSETINFORMATION**(il valore del tipo di evento è 20)<br/>     | Evento di impostazione delle informazioni. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                                |
| **Evento \_ Tipo di traccia \_ \_ REGSETVALUE**(il valore del tipo di evento è 14)<br/>           | Imposta evento valore. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**Registro**](registry.md)
</dt> <dt>

[**Registro di sistema \_ V0**](registry-v0.md)
</dt> <dt>

[**Registro di sistema \_ V1 \_ TypeGroup1**](registry-v1-typegroup1.md)
</dt> </dl>

 

 
