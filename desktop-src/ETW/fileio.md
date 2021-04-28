---
description: 'Classe FileIo: questa classe è la classe padre per gli eventi di I/O di file. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: Classe FileIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716528902a115e23eae5b49ef572b87a71d11e25
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106529"
---
# <a name="fileio-class"></a>Classe FileIo

Questa classe è la classe padre per gli eventi di I/O di file.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe FileIo** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di I/O di file in una sessione di registrazione del kernel NT, specificare il flag **EVENT TRACE FLAG DISK FILE \_ \_ \_ \_ \_ IO** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea) È anche possibile specificare uno o più dei flag seguenti:

-   **\_I/O DEL FILE DEL FLAG DI TRACCIA \_ \_ \_ EVENTI**
-   **FILE \_ DEL FLAG DI TRACCIA EVENTI IO \_ \_ \_ \_ INIT**

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi di I/O di file chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**FileIoGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento effettivo quando si usano gli eventi.



| Tipo di evento             | Descrizione                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il valore del tipo di evento è 0  | Evento nome file. La [**classe MOF FileIo \_ Name**](fileio-name.md) definisce i dati dell'evento per questo evento.                                                                               |
| Il valore del tipo di evento è 32 | Evento di creazione file. La [**classe MOF FileIo \_ Name**](fileio-name.md) definisce i dati dell'evento per questo evento.                                                                             |
| Il valore del tipo di evento è 35 | Evento di eliminazione file. La classe MOF [**FileIo \_ Name**](fileio-name.md) definisce i dati dell'evento.                                                                             |
| Il valore del tipo di evento è 36 | Evento di rundown del file. Enumera tutti i file aperti nel computer alla fine della sessione di traccia. La classe MOF [**FileIo \_ Name**](fileio-name.md) definisce i dati dell'evento. |
| Il valore del tipo di evento è 64 | Evento di creazione file. La [**classe FileIo \_ Create**](fileio-create.md) MOF definisce i dati dell'evento per questo evento.                                                                         |
| Il valore del tipo di evento è 72 | Evento di enumerazione della directory. La [**classe MOF FileIo \_ DirEnum**](fileio-direnum.md) definisce i dati dell'evento per questo evento.                                                             |
| Il valore del tipo di evento è 77 | Evento di notifica della directory. La [**classe MOF FileIo \_ DirEnum**](fileio-direnum.md) definisce i dati dell'evento per questo evento.                                                            |
| Il valore del tipo di evento è 69 | Evento di impostazione delle informazioni. La [**classe MOF FileIo \_ Info**](fileio-info.md) definisce i dati dell'evento per questo evento.                                                                         |
| Il valore del tipo di evento è 70 | Evento di eliminazione del file. La [**classe MOF FileIo \_ Info**](fileio-info.md) definisce i dati dell'evento.                                                                             |
| Il valore del tipo di evento è 71 | Rinominare l'evento del file. La [**classe MOF FileIo \_ Info**](fileio-info.md) definisce i dati dell'evento.                                                                             |
| Il valore del tipo di evento è 74 | Eseguire query sull'evento di informazioni sul file. La [**classe MOF FileIo \_ Info**](fileio-info.md) definisce i dati dell'evento.                                                                  |
| Il valore del tipo di evento è 75 | Evento di controllo del file system. La [**classe MOF FileIo \_ Info**](fileio-info.md) definisce i dati dell'evento.                                                                     |
| Il valore del tipo di evento è 76 | Evento di fine operazione. La [**classe MOF FileIo \_ OpEnd**](fileio-opend.md) definisce i dati dell'evento per questo evento.                                                                      |
| Il valore del tipo di evento è 67 | Evento di lettura file. La [**classe MOF FileIo \_ ReadWrite**](fileio-readwrite.md) definisce i dati dell'evento per questo evento.                                                                     |
| Il valore del tipo di evento è 68 | Evento di scrittura file. La [**classe MOF FileIo \_ ReadWrite**](fileio-readwrite.md) definisce i dati dell'evento per questo evento.                                                                    |
| Il valore del tipo di evento è 65 | Evento di pulizia. L'evento viene generato quando viene rilasciato l'ultimo handle per il file. La [**classe MOF FileIo \_ SimpleOp**](fileio-simpleop.md) definisce i dati dell'evento per questo evento.   |
| Il valore del tipo di evento è 66 | Evento di chiusura. L'evento viene generato quando l'oggetto file viene liberato. La [**classe MOF FileIo \_ SimpleOp**](fileio-simpleop.md) definisce i dati dell'evento per questo evento.                     |
| Il valore del tipo di evento è 73 | Evento Flush. Questo evento viene generato quando i buffer dei file vengono scaricati completamente su disco. La [**classe MOF FileIo \_ SimpleOp**](fileio-simpleop.md) definisce i dati dell'evento per questo evento.  |



 

Gli eventi di I/O di file vengono registrati all'inizio dell'operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**FileIo \_ V0**](fileio-v0.md)
</dt> <dt>

[**FileIo \_ V1**](fileio-v1.md)
</dt> </dl>

 

 
