---
description: Questa classe è la classe padre per gli eventi di I/O di file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: Classe FileIO
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
ms.openlocfilehash: 2f7c032cb7af325efa1d2ea76702068fc7b3be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978850"
---
# <a name="fileio-class"></a>Classe FileIO

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

La classe **FileIO** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi i/o di file in una sessione di registrazione del kernel NT, specificare il flag di i/o del **\_ \_ \_ \_ file \_ su disco del flag di traccia eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) . È anche possibile specificare uno o più dei flag seguenti:

-   **\_ \_ \_ io file flag di traccia eventi \_**
-   **\_file di flag di traccia eventi \_ \_ \_ io \_ init**

I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di I/O di file chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**FileIoGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di evento seguenti per identificare l'evento effettivo quando si utilizzano gli eventi.



| Tipo di evento             | Descrizione                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il valore del tipo di evento è 0  | Evento nome file. La classe MOF [**\_ Nome filegroup**](fileio-name.md) definisce i dati dell'evento per questo evento.                                                                               |
| Il valore del tipo di evento è 32 | Evento di creazione del file. La classe MOF [**\_ Nome filegroup**](fileio-name.md) definisce i dati dell'evento per questo evento.                                                                             |
| Il valore del tipo di evento è 35 | Evento di eliminazione file. La classe MOF [**\_ Nome filegroup**](fileio-name.md) definisce i dati dell'evento per questo evento.                                                                             |
| Il valore del tipo di evento è 36 | Evento rundown file. Enumera tutti i file aperti nel computer alla fine della sessione di traccia. La classe MOF [**\_ Nome filegroup**](fileio-name.md) definisce i dati dell'evento per questo evento. |
| Il valore del tipo di evento è 64 | Evento di creazione del file. La classe [**FileIO \_ create**](fileio-create.md) MOF definisce i dati degli eventi per questo evento.                                                                         |
| Il valore del tipo di evento è 72 | Evento di enumerazione directory. La classe MOF [**\_ DirEnum di filegroup**](fileio-direnum.md) definisce i dati dell'evento per questo evento.                                                             |
| Il valore del tipo di evento è 77 | Evento di notifica della directory. La classe MOF [**\_ DirEnum di filegroup**](fileio-direnum.md) definisce i dati dell'evento per questo evento.                                                            |
| Il valore del tipo di evento è 69 | Evento di impostazione delle informazioni. La classe MOF [**\_ info filegroup**](fileio-info.md) definisce i dati degli eventi per questo evento.                                                                         |
| Il valore del tipo di evento è 70 | Evento Delete file. La classe MOF [**\_ info filegroup**](fileio-info.md) definisce i dati degli eventi per questo evento.                                                                             |
| Il valore del tipo di evento è 71 | Rinominare un evento di file. La classe MOF [**\_ info filegroup**](fileio-info.md) definisce i dati degli eventi per questo evento.                                                                             |
| Il valore del tipo di evento è 74 | Evento di informazioni sul file di query. La classe MOF [**\_ info filegroup**](fileio-info.md) definisce i dati degli eventi per questo evento.                                                                  |
| Il valore del tipo di evento è 75 | Evento di controllo del file System. La classe MOF [**\_ info filegroup**](fileio-info.md) definisce i dati degli eventi per questo evento.                                                                     |
| Il valore del tipo di evento è 76 | Fine dell'evento dell'operazione. La classe MOF [**\_ aperto del FileIO**](fileio-opend.md) definisce i dati dell'evento per questo evento.                                                                      |
| Il valore del tipo di evento è 67 | Evento di lettura del file. La classe MOF [**\_ ReadWrite di filegroup**](fileio-readwrite.md) definisce i dati dell'evento per questo evento.                                                                     |
| Il valore del tipo di evento è 68 | Evento di scrittura file. La classe MOF [**\_ ReadWrite di filegroup**](fileio-readwrite.md) definisce i dati dell'evento per questo evento.                                                                    |
| Il valore del tipo di evento è 65 | Evento di pulizia. L'evento viene generato quando viene rilasciato l'ultimo handle del file. La classe MOF [**\_ SimpleOp di filegroup**](fileio-simpleop.md) definisce i dati dell'evento per questo evento.   |
| Il valore del tipo di evento è 66 | Evento Close. L'evento viene generato quando l'oggetto file viene liberato. La classe MOF [**\_ SimpleOp di filegroup**](fileio-simpleop.md) definisce i dati dell'evento per questo evento.                     |
| Il valore del tipo di evento è 73 | Scarica evento. Questo evento viene generato quando i buffer di file vengono scaricati completamente su disco. La classe MOF [**\_ SimpleOp di filegroup**](fileio-simpleop.md) definisce i dati dell'evento per questo evento.  |



 

Gli eventi di i/o di file vengono registrati all'inizio dell'operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**FileIO \_ V0**](fileio-v0.md)
</dt> <dt>

[**FileIO \_ V1**](fileio-v1.md)
</dt> </dl>

 

 
