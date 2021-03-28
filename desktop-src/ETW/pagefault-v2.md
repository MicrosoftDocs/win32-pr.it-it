---
description: Questa classe è la classe padre per gli eventi di errore di pagina. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: Classe PageFault_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: a545e8ae7c5afb000c26d89d9359f620fa7a653d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977639"
---
# <a name="pagefault_v2-class"></a>\_Classe pagefault V2

Questa classe è la classe padre per gli eventi di errore di pagina.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **pagefault \_ v2** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare tutti gli eventi di errore di pagina in una sessione di registrazione del kernel NT, specificare il flag di **\_ \_ \_ \_ \_ errore della pagina memoria del flag di traccia eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . È inoltre possibile specificare i flag seguenti:

-   **\_flag di traccia eventi \_ \_ \_ errori hardware memoria \_**
-   **FLAG di traccia eventi- \_ \_ \_ \_ Alloc virtuale**

I consumer di traccia degli eventi possono implementare un'elaborazione speciale per tutti gli eventi di errore di pagina chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**PageFaultGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di evento seguenti per identificare l'evento di memoria effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                     | Descrizione                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Tipo di traccia evento \_ \_ mm \_ mucca (il valore del tipo di evento è 12)<br/> | Evento copy-on-Write. La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento. Prima di Windows Vista, la classe MOF [**pagefault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.     |
| \_Tipo traccia \_ evento \_ mm \_ DZF (il valore del tipo di evento è 11)<br/> | Evento di errore di richiesta zero. La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento. Prima di Windows Vista, la classe MOF [**pagefault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento. |
| \_Tipo traccia \_ evento \_ mm \_ GPF (il valore del tipo di evento è 13)<br/> | Evento di errore di pagina Guard. La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento. Prima di Windows Vista, la classe MOF [**pagefault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.  |
| \_Tipo traccia \_ evento \_ mm \_ HPF (il valore del tipo di evento è 14)<br/> | Evento di errore di pagina hardware. La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento. Prima di Windows Vista, la classe MOF [**pagefault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.   |
| \_Tipo di traccia eventi \_ \_ mm \_ tf (il valore del tipo di evento è 10)<br/>  | Evento di errore di transizione. La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento. Prima di Windows Vista, la classe MOF [**pagefault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.  |
| \_Tipo di traccia eventi \_ \_ mm \_ AV (il valore del tipo di evento è 15)<br/>  | Evento di violazione di accesso. La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                           |
| Valore del tipo di evento, 32                                           | Evento di errore di pagina hardware. La classe MOF [**pagefault \_ HardFault**](pagefault-hardfault.md) definisce i dati dell'evento per questo evento.                                                                                                                               |
| Valore del tipo di evento, 105                                          | Caricamento dell'immagine nell'evento del file di paging. La classe MOF [**pagefault \_ ImageLoadBacked**](pagefault-imageloadbacked.md) definisce i dati dell'evento per questo evento.                                                                                                          |
| Valore del tipo di evento, 98                                           | Evento di allocazione virtuale. La classe MOF [**VirtualAlloc**](pagefault-virtualalloc.md) definisce i dati dell'evento per questo evento.                                                                                                                                |
| Valore del tipo di evento, 99                                           | Evento virtuale gratuito. La classe MOF [**VirtualAlloc**](pagefault-virtualalloc.md) definisce i dati dell'evento per questo evento.                                                                                                                                      |



 

È possibile utilizzare i membri **ProcessID** e **ThreadID** dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare il processo o il thread che ha generato l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



 

 
