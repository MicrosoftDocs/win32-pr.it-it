---
description: Questa classe è la classe padre per gli eventi di I/O su disco. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: Classe DiskIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0e91f5e8b84d77b0938f35da69a84c26fa0f34a4da63bce40330484a29e19b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395302"
---
# <a name="diskio-class"></a>Classe DiskIo

Questa classe è la classe padre per gli eventi di I/O su disco.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe DiskIo** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di I/0 del disco in una sessione di registrazione del kernel NT, specificare il flag **EVENT TRACE FLAG DISK \_ \_ \_ \_ IO** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) È anche possibile specificare uno o più dei flag seguenti:

-   **EVENT \_ TRACE \_ FLAG \_ DISK \_ IO \_ INIT**
-   **\_DRIVER DEL FLAG DI TRACCIA \_ \_ EVENTI**

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi di I/O su disco chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**DiskIoGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento di I/O su disco effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                                      | Descrizione                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ IO \_ READ**(il valore del tipo di evento è 10)<br/>             | Evento di lettura. La [**classe MOF DiskIo \_ TypeGroup1**](diskio-typegroup1.md) definisce i dati dell'evento per questo evento.                                              |
| **EVENTO \_ TRACE \_ TYPE \_ IO \_ WRITE**(il valore del tipo di evento è 11)<br/>            | Evento di scrittura. La [**classe MOF DiskIo \_ TypeGroup1**](diskio-typegroup1.md) definisce i dati dell'evento per questo evento.                                             |
| **EVENTO \_ TRACE \_ TYPE IO READ \_ \_ \_ INIT**(il valore del tipo di evento è 12)<br/>       | Inizializzare l'evento di lettura. La [**classe MOF DiskIo \_ TypeGroup2**](diskio-typegroup2.md) definisce i dati dell'evento per questo evento.                                   |
| **EVENTO \_ TRACE \_ TYPE IO WRITE \_ \_ \_ INIT**(il valore del tipo di evento è 13)<br/>      | Inizializzare l'evento di scrittura. La [**classe MOF DiskIo \_ TypeGroup2**](diskio-typegroup2.md) definisce i dati dell'evento per questo evento.                                  |
| **EVENTO \_ TRACE \_ TYPE \_ IO \_ FLUSH**(il valore del tipo di evento è 14)<br/>            | Inizializzare l'evento di scrittura. La [**classe MOF DiskIo \_ TypeGroup3**](diskio-typegroup3.md) definisce i dati dell'evento per questo evento.                                  |
| **EVENTO \_ TRACE \_ TYPE IO FLUSH \_ \_ \_ INIT**(il valore del tipo di evento è 15)<br/>      | Inizializzare l'evento flush. La [**classe MOF DiskIo \_ TypeGroup2**](diskio-typegroup2.md) definisce i dati dell'evento per questo evento.                                  |
| **EVENTO \_ TRACE \_ TYPE \_ IO \_ REDIRECTED \_ INIT**(Il valore del tipo di evento è 16)<br/> | Inizializzare l'evento reindirizzato. Gli eventi di I/O reindirizzati vengono usati per eseguire il mapping degli I/O del disco a Windows Imaging Format (WIM) al nome file all'interno di WIM.                  |
| Il valore del tipo di evento è 52<br/>                                               | Evento di richiesta di completamento del driver. La classe MOF [**DriverCompleteRequest**](drivercompleterequest.md) definisce i dati dell'evento per questo evento.                    |
| Il valore del tipo di evento è 53<br/>                                               | Evento di restituzione della richiesta di completamento del driver. La [**classe MOF DriverCompleteRequestReturn**](drivercompleterequestreturn.md) definisce i dati dell'evento per questo evento. |
| Il valore del tipo di evento è 37<br/>                                               | Evento di routine di completamento del driver. La [**classe MOF DriverCompletionRoutine**](drivercompletionroutine.md) definisce i dati dell'evento per questo evento.              |
| Il valore del tipo di evento è 34<br/>                                               | Evento di chiamata di funzione principale del driver. La [**classe MOF DriverMajorFunctionCall**](drivermajorfunctioncall.md) definisce i dati dell'evento per questo evento.             |
| Il valore del tipo di evento è 35<br/>                                               | Evento restituito della chiamata di funzione principale del driver. La [**classe MOF DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) definisce i dati dell'evento per questo evento.  |



 

Il provider di I/0 su disco non è in grado di identificare il file letto o scritto durante un evento di I/O su disco. Per recuperare il nome del file associato all'evento di I/O su disco, abilitare il provider di eventi I/0 del file.

Gli eventi di I/O su disco vengono registrati all'ora di completamento dell'I/O. Per determinare quando è iniziata l'operazione di I/O, usare gli eventi di inizializzazione, ad esempio EVENT \_ TRACE TYPE IO READ \_ \_ \_ \_ INIT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DiskIo \_ TypeGroup1**](diskio-typegroup1.md)
</dt> <dt>

[**DiskIo \_ TypeGroup2**](diskio-typegroup2.md)
</dt> <dt>

[**DiskIo \_ TypeGroup3**](diskio-typegroup3.md)
</dt> <dt>

[**DriverCompleteRequest**](drivercompleterequest.md)
</dt> <dt>

[**DriverCompleteRequestReturn**](drivercompleterequestreturn.md)
</dt> <dt>

[**DriverCompletionRoutine**](drivercompletionroutine.md)
</dt> <dt>

[**DriverMajorFunctionCall**](drivermajorfunctioncall.md)
</dt> <dt>

[**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
