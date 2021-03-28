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
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977706"
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

La classe **PerfInfo** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di chiamata di procedura posticipata in una sessione di registrazione del kernel NT, specificare il flag **DPC del \_ flag di traccia \_ \_ eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . È anche possibile specificare uno o più dei flag seguenti:

-   **\_interrupt del \_ flag di traccia eventi \_**
-   **\_ \_ profilo contrassegno di traccia eventi \_**
-   **\_flag di traccia evento \_ \_ SYSTEMCALL**

I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi DPC chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**PerfInfoGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di evento seguenti per identificare l'evento effettivo quando si utilizzano gli eventi.



| Tipo di evento           | Descrizione                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| Valore del tipo di evento, 46 | Evento del profilo campionato. La classe MOF [**SampledProfile**](sampledprofile.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 51 | Evento di chiamata di sistema Enter. La classe MOF [**SysCallEnter**](syscallenter.md) definisce i dati dell'evento per questo evento.   |
| Valore del tipo di evento, 52 | Evento di uscita chiamata di sistema. La classe MOF [**SysCallExit**](syscallexit.md) definisce i dati dell'evento per questo evento.      |
| Valore del tipo di evento, 66 | Evento DPC a thread. La classe [**DPC**](dpc.md) MOF definisce i dati dell'evento per questo evento.                          |
| Valore del tipo di evento, 67 | Evento di interrupt service routine (ISR). La classe MOF [**ISR**](isr.md) definisce i dati dell'evento per questo evento.       |
| Valore del tipo di evento, 68 | Evento DPC. La classe [**DPC**](dpc.md) MOF definisce i dati dell'evento per questo evento.                                   |
| Valore del tipo di evento, 69 | Evento timer DPC. La classe [**DPC**](dpc.md) MOF definisce i dati dell'evento per questo evento.                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 
