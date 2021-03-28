---
description: Questa classe è la classe padre per gli eventi di immagine. La sintassi seguente è semplificata dal codice MOF.
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
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979871"
---
# <a name="image-class"></a>Classe Image

Questa classe è la classe padre per gli eventi di immagine.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **Image** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di immagine in una sessione di registrazione del kernel NT, specificare il flag di caricamento dell'  **immagine del flag di \_ traccia \_ \_ \_ eventi** nel membro EnableFlags della struttura delle [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di caricamento dell'immagine chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ImageLoadGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di eventi seguenti per identificare gli eventi di caricamento delle immagini quando si utilizzano gli eventi.



| Tipo di evento                                                          | Descrizione                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ \_ \_ Caricamento del tipo di traccia**(il valore del tipo di evento è 10)<br/>     | Evento di caricamento dell'immagine. Generato quando viene caricato un file eseguibile o una DLL. Il provider genera un solo evento per la prima volta che una determinata DLL viene caricata. La classe MOF [**\_ Load Image**](image-load.md) definisce i dati degli eventi per questo evento.      |
| **Evento \_ \_ \_ Fine tipo di traccia**(il valore del tipo di evento è 2)<br/>       | Evento di scaricamento immagine. Generato quando viene scaricato un file eseguibile o una DLL. Il provider genera un solo evento per l'ultima volta in cui una determinata DLL viene scaricata. La classe MOF [**\_ Load Image**](image-load.md) definisce i dati degli eventi per questo evento. |
| **Evento \_ Tipo di traccia \_ \_ DC \_ Start**(il valore del tipo di evento è 3)<br/> | Evento di avvio raccolta dati. Enumera tutte le immagini caricate all'inizio della traccia. La classe MOF [**\_ Load Image**](image-load.md) definisce i dati degli eventi per questo evento.                                                                  |
| **Evento \_ Tipo di traccia \_ \_ DC \_ end**(il valore del tipo di evento è 4)<br/>   | Evento di fine raccolta dati. Enumera tutte le immagini caricate alla fine della traccia. La classe MOF [**\_ Load Image**](image-load.md) definisce i dati degli eventi per questo evento.                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**\_Caricamento immagine**](image-load.md)
</dt> <dt>

[**Immagine \_ V0**](image-v0.md)
</dt> <dt>

[**Immagine \_ V1**](image-v1.md)
</dt> </dl>

 

 
