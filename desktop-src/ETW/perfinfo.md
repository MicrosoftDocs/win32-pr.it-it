---
description: Questa classe è la classe padre per gli eventi del contatore delle prestazioni. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: Classe PerfInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 641ebb361d14fa8abb0c8199cf113cfd85a2e6700e262447c1302f3f1b66231a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151407"
---
# <a name="perfinfo-class"></a>Classe PerfInfo

Questa classe è la classe padre per gli eventi del contatore delle prestazioni.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe PerfInfo** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi DPC (Deferred Procedure Call) in una sessione di registrazione del kernel NT, specificare il flag **\_ \_ \_ DPC EVENT TRACE FLAG** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) È anche possibile specificare uno o più dei flag seguenti:

-   **EVENT \_ TRACE \_ FLAG \_ INTERRUPT**
-   **PROFILO \_ FLAG DI TRACCIA \_ \_ EVENTI**
-   **EVENT \_ TRACE \_ FLAG \_ SYSTEMCALL**

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi DPC chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**PerfInfoGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento effettivo quando si utilizzano gli eventi.



| Tipo di evento           | Descrizione                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| Valore del tipo di evento, 46 | Evento del profilo campionato. La classe MOF [**SampledProfile**](sampledprofile.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 51 | Evento enter della chiamata di sistema. La [**classe MOF SysCallEnter**](syscallenter.md) definisce i dati dell'evento per questo evento.   |
| Valore del tipo di evento, 52 | Evento di uscita della chiamata di sistema. La [**classe MOF SysCallExit**](syscallexit.md) definisce i dati dell'evento per questo evento.      |
| Valore del tipo di evento, 66 | Evento DPC con thread. La [**classe MOF DPC**](dpc.md) definisce i dati dell'evento per questo evento.                          |
| Valore del tipo di evento, 67 | Evento di routine del servizio di interruzione (ISR). La classe MOF [**ISR**](isr.md) definisce i dati dell'evento per questo evento.       |
| Valore del tipo di evento, 68 | Evento DPC. La [**classe MOF DPC**](dpc.md) definisce i dati dell'evento per questo evento.                                   |
| Valore del tipo di evento, 69 | Evento timer DPC. La [**classe MOF DPC**](dpc.md) definisce i dati dell'evento per questo evento.                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 
