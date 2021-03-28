---
description: Questa classe è la classe padre per gli eventi del registro di sistema. La sintassi seguente è semplificata dal codice MOF.
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
ms.openlocfilehash: 6799756ebfe573fad6a32a191e79c3c2b745f563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129695"
---
# <a name="registry-class"></a>Classe Registry

Questa classe è la classe padre per gli eventi del registro di sistema.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(2)]
class Registry : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **Registry** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi del registro di sistema in una sessione di registrazione del kernel NT, specificare il  **Registro di sistema dei \_ \_ flag \_ di traccia eventi** nel membro EnableFlags di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi del registro di sistema chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**RegistryGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di eventi seguenti per identificare l'evento del registro di sistema effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                                       | Descrizione                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ Tipo di traccia \_ \_ REGCREATE**(il valore del tipo di evento è 10)<br/>             | Crea evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                            |
| **Evento \_ Tipo di traccia \_ \_ REGDELETE**(il valore del tipo di evento è 12)<br/>             | Elimina evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                            |
| **Evento \_ Tipo di traccia \_ \_ REGDELETEVALUE**(il valore del tipo di evento è 15)<br/>        | Evento Delete value. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                          |
| **Evento \_ Tipo di traccia \_ \_ REGENUMERATEKEY**(il valore del tipo di evento è 17)<br/>       | Enumera evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                         |
| **Evento \_ Tipo di traccia \_ \_ REGENUMERATEVALUEKEY**(il valore del tipo di evento è 18)<br/>  | Enumera evento chiave valore. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                   |
| **Evento \_ Tipo di traccia \_ \_ REGFLUSH**(il valore del tipo di evento è 21)<br/>              | Scarica evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                             |
| **Evento \_ Tipo di traccia \_ \_ REGKCBDMP**(il valore del tipo di evento è 22)<br/>             | Crea evento chiave. Generato quando un'operazione del registro di sistema utilizza handle anziché stringhe per fare riferimento a sottochiavi. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento. |
| **Evento \_ Tipo di traccia \_ \_ REGOPEN**(il valore del tipo di evento è 11)<br/>               | Apri evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                              |
| **Evento \_ Tipo di traccia \_ \_ REGQUERY**(il valore del tipo di evento è 13)<br/>              | Evento chiave di query. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                             |
| **Evento \_ Tipo di traccia \_ \_ REGQUERYMULTIPLEVALUE**(il valore del tipo di evento è 19)<br/> | Eseguire una query su un evento a più valori. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                  |
| **Evento \_ Tipo di traccia \_ \_ REGQUERYVALUE**(il valore del tipo di evento è 16)<br/>         | Evento valore query. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                           |
| **Evento \_ Tipo di traccia \_ \_ REGSETINFORMATION**(il valore del tipo di evento è 20)<br/>     | Evento di impostazione delle informazioni. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                       |
| **Evento \_ Tipo di traccia \_ \_ REGSETVALUE**(il valore del tipo di evento è 14)<br/>           | Imposta evento valore. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                             |
| Valore del tipo di evento 23                                                             | Elimina evento chiave. Generato quando un'operazione del registro di sistema utilizza handle anziché stringhe per fare riferimento a sottochiavi. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 24                                                             | Enumera le chiavi del registro di sistema aperte all'inizio della sessione. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                           |
| Valore del tipo di evento, 25                                                             | Enumera le chiavi del registro di sistema aperte alla fine della sessione. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                  |
| Valore del tipo di evento, 26                                                             | La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                              |
| Valore del tipo di evento, 27                                                             | Apri evento chiave. La classe MOF [**\_ TypeGroup1 del registro di sistema**](registry-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**Registro di sistema \_ TypeGroup1**](registry-typegroup1.md)
</dt> <dt>

[**Registro di sistema \_ V0**](registry-v0.md)
</dt> <dt>

[**Registro di sistema \_ V1**](registry-v1.md)
</dt> </dl>

 

 
