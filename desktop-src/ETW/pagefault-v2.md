---
description: Questa classe è la classe padre per gli eventi di errore di pagina. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: PageFault_V2 classe
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
ms.openlocfilehash: bd8adfa698975f7661abdbd849136d04049b5539ff3fed3b52b61660791add0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900751"
---
# <a name="pagefault_v2-class"></a>Classe PageFault \_ V2

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

La **classe PageFault \_ V2** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare tutti gli eventi di errore di pagina in una sessione di registrazione del kernel NT, specificare il flag **EVENT TRACE FLAG MEMORY PAGE \_ \_ \_ \_ \_ FAULTS** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) È anche possibile specificare i flag seguenti:

-   **ERRORI \_ RIGIDI DI \_ MEMORIA DEL FLAG DI TRACCIA \_ \_ \_ EVENTI**
-   **FLAG \_ DI TRACCIA EVENTI VIRTUAL \_ \_ \_ ALLOC**

I consumer di traccia eventi possono implementare un'elaborazione speciale per tutti gli eventi di errore di pagina chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**PageFaultGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento di memoria effettivo durante l'utilizzo degli eventi.



| Tipo di evento                                                     | Descrizione                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVENT \_ TRACE TYPE MM \_ \_ \_ COW(Il valore del tipo di evento è 12)<br/> | Evento di copia in scrittura. La [**classe MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento. Prima di Windows Vista, la [**classe MOF PageFault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.     |
| EVENT \_ TRACE TYPE MM \_ \_ \_ DZF (Il valore del tipo di evento è 11)<br/> | Evento di errore demand zero. La [**classe MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento. Prima di Windows Vista, la [**classe MOF PageFault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento. |
| EVENT \_ TRACE TYPE MM \_ \_ \_ GPF (Il valore del tipo di evento è 13)<br/> | Evento di errore della pagina di protezione. La [**classe MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento. Prima di Windows Vista, la [**classe MOF PageFault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.  |
| EVENT \_ TRACE TYPE MM \_ \_ \_ HPF (Il valore del tipo di evento è 14)<br/> | Evento di errore di pagina hard. La [**classe MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento. Prima di Windows Vista, la [**classe MOF PageFault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.   |
| EVENT \_ TRACE TYPE MM \_ \_ \_ TF (Il valore del tipo di evento è 10)<br/>  | Evento di errore di transizione. La [**classe MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento. Prima di Windows Vista, la [**classe MOF PageFault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.  |
| EVENT \_ TRACE TYPE MM \_ \_ \_ AV(Il valore del tipo di evento è 15)<br/>  | Evento di violazione dell'accesso. La [**classe MOF PageFault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento.                                                                                                                           |
| Valore del tipo di evento, 32                                           | Evento di errore di pagina hard. La [**classe MOF PageFault \_ HardFault**](pagefault-hardfault.md) definisce i dati dell'evento per questo evento.                                                                                                                               |
| Valore del tipo di evento, 105                                          | Evento di caricamento dell'immagine nel file di pagina. La [**classe MOF PageFault \_ ImageLoadBacked**](pagefault-imageloadbacked.md) definisce i dati dell'evento per questo evento.                                                                                                          |
| Valore del tipo di evento, 98                                           | Evento di allocazione virtuale. La [**classe MOF VirtualAlloc**](pagefault-virtualalloc.md) definisce i dati dell'evento per questo evento.                                                                                                                                |
| Valore del tipo di evento, 99                                           | Evento gratuito virtuale. La [**classe MOF VirtualAlloc**](pagefault-virtualalloc.md) definisce i dati dell'evento per questo evento.                                                                                                                                      |



 

È possibile usare i **membri ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare il processo o il thread di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



 

 
