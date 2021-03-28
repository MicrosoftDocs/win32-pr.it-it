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
ms.openlocfilehash: 97f9907e4da51675bb1a5f562931e471ee0e133e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966507"
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

La classe **DiskIo** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di I/o su disco in una sessione di registrazione del kernel NT, specificare il flag di i  /o del **disco del flag di \_ traccia \_ \_ \_ eventi** nel membro EnableFlags di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . È anche possibile specificare uno o più dei flag seguenti:

-   **i/o \_ \_ \_ disco \_ flag \_ di traccia eventi**
-   **\_ \_ driver flag di traccia eventi \_**

I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di I/O su disco chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**DiskIoGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di evento seguenti per identificare l'evento di I/O del disco effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                                      | Descrizione                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ Tipo di traccia \_ \_ io \_ letti**(il valore del tipo di evento è 10)<br/>             | Evento Read. La classe MOF [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) definisce i dati dell'evento per questo evento.                                              |
| **Evento \_ Tipo di traccia \_ \_ io \_ Write**(il valore del tipo di evento è 11)<br/>            | Evento Write. La classe MOF [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) definisce i dati dell'evento per questo evento.                                             |
| **Evento \_ Tipo di traccia \_ \_ io \_ Read \_ init**(il valore del tipo di evento è 12)<br/>       | Inizializza l'evento di lettura. La classe MOF [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) definisce i dati dell'evento per questo evento.                                   |
| **Evento \_ Tipo di traccia \_ \_ io \_ Write \_ init**(il valore del tipo di evento è 13)<br/>      | Inizializza l'evento di scrittura. La classe MOF [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) definisce i dati dell'evento per questo evento.                                  |
| **Evento \_ Tipo di traccia \_ \_ io \_ Flush**(il valore del tipo di evento è 14)<br/>            | Inizializza l'evento di scrittura. La classe MOF [**DiskIo \_ TypeGroup3**](diskio-typegroup3.md) definisce i dati dell'evento per questo evento.                                  |
| **Evento \_ Tipo di traccia \_ \_ io \_ Flush \_ init**(il valore del tipo di evento è 15)<br/>      | Inizializzare l'evento di scaricamento. La classe MOF [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) definisce i dati dell'evento per questo evento.                                  |
| **Evento \_ Tipo di traccia \_ \_ io \_ reindirizzato \_ init**(il valore del tipo di evento è 16)<br/> | Inizializzare l'evento reindirizzato. Gli eventi i/o reindirizzati vengono usati per eseguire il mapping di IOs del disco a un formato Windows Imaging (WIM) al nome file all'interno del file WIM.                  |
| Il valore del tipo di evento è 52<br/>                                               | Evento di richiesta completo del driver. La classe MOF [**DriverCompleteRequest**](drivercompleterequest.md) definisce i dati dell'evento per questo evento.                    |
| Il valore del tipo di evento è 53<br/>                                               | Evento restituito della richiesta di completamento del driver. La classe MOF [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) definisce i dati dell'evento per questo evento. |
| Il valore del tipo di evento è 37<br/>                                               | Evento di routine di completamento del driver. La classe MOF [**DriverCompletionRoutine**](drivercompletionroutine.md) definisce i dati dell'evento per questo evento.              |
| Il valore del tipo di evento è 34<br/>                                               | Evento di chiamata di funzione principale del driver. La classe MOF [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) definisce i dati dell'evento per questo evento.             |
| Il valore del tipo di evento è 35<br/>                                               | Evento di chiamata di funzione principale del driver. La classe MOF [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) definisce i dati dell'evento per questo evento.  |



 

Il provider I/O su disco non è in grado di identificare il file letto o scritto durante un evento di I/O su disco. Per recuperare il nome del file associato all'evento di I/O su disco, abilitare il provider di eventi I/0 del file.

Gli eventi di I/O su disco vengono registrati all'ora di completamento di I/O. Per determinare quando è iniziata l'operazione di I/O, utilizzare gli eventi di inizializzazione, ad esempio, il \_ tipo di traccia eventi \_ \_ io \_ Read \_ init.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TypeGroup1 DiskIo**](diskio-typegroup1.md)
</dt> <dt>

[**\_TypeGroup2 DiskIo**](diskio-typegroup2.md)
</dt> <dt>

[**\_TypeGroup3 DiskIo**](diskio-typegroup3.md)
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

 

 
