---
description: Questa classe è la classe padre per gli eventi immagine. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Classe Image
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: a7db8595dd09790d875e502e479d14669a6df90b8de38b71fcf9ed58f2b68b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070111"
---
# <a name="image-class"></a>Classe Image

Questa classe è la classe padre per gli eventi immagine.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe Image** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi immagine in una sessione di registrazione del kernel NT, specificare il flag **EVENT TRACE FLAG IMAGE \_ \_ \_ \_ LOAD** nel membro **EnableFlags** della struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi di caricamento delle immagini chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ImageLoadGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare gli eventi di caricamento delle immagini quando si usano gli eventi.



| Tipo di evento                                                          | Descrizione                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ LOAD**(il valore del tipo di evento è 10)<br/>     | Evento di caricamento dell'immagine. Generato quando viene caricata una DLL o un file eseguibile. Il provider genera un solo evento per la prima volta che viene caricata una determinata DLL. La classe MOF [**\_ caricamento**](image-load.md) immagine definisce i dati dell'evento per questo evento.      |
| **EVENTO \_ TRACE \_ TYPE \_ END**(il valore del tipo di evento è 2)<br/>       | Evento di scaricamento dell'immagine. Generato quando viene scaricato un file DLL o eseguibile. Il provider genera un solo evento per l'ultima volta che una determinata DLL viene scaricata. La classe MOF [**\_ caricamento**](image-load.md) immagine definisce i dati dell'evento per questo evento. |
| **EVENTO \_ TRACE \_ TYPE \_ DC \_ START**(il valore del tipo di evento è 3)<br/> | Evento di avvio della raccolta dati. Enumera tutte le immagini caricate all'inizio della traccia. La classe MOF [**\_ caricamento**](image-load.md) immagine definisce i dati dell'evento per questo evento.                                                                  |
| **EVENTO \_ TRACE \_ TYPE \_ DC \_ END**(il valore del tipo di evento è 4)<br/>   | Evento di fine della raccolta dati. Enumera tutte le immagini caricate alla fine della traccia. La classe MOF [**\_ caricamento**](image-load.md) immagine definisce i dati dell'evento per questo evento.                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**Caricamento \_ immagine**](image-load.md)
</dt> <dt>

[**Immagine \_ V0**](image-v0.md)
</dt> <dt>

[**Immagine \_ V1**](image-v1.md)
</dt> </dl>

 

 
