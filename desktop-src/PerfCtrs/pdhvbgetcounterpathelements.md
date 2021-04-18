---
description: La funzione PdhVbGetCounterPathElements analizza una stringa di percorso del contatore delle prestazioni completo nei singoli elementi.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: PdhVbGetCounterPathElements (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 003374141b0454d730ba4b844715bd6f00b544da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312152"
---
# <a name="pdhvbgetcounterpathelements-function"></a>PdhVbGetCounterPathElements (funzione)

La funzione **PdhVbGetCounterPathElements** analizza una stringa di percorso del contatore delle prestazioni completo nei singoli elementi. Ogni variabile di tipo stringa deve avere la stessa dimensione (*bufferSize*) e dimensionata e inizializzata prima di essere utilizzata in questa funzione.

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbGetCounterPathElements ( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal nomeoggetto As String, \_ ByVal NomeIstanza As String, \_ ByVal ParentInstance As String, \_ ByVal CounterName As String, \_ ByVal bufferSize Long \_ ) Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*PathString* 
</dt> <dd>

Stringa del percorso del contatore che deve essere suddivisa nei singoli elementi.

</dd> <dt>

*MachineName* 
</dt> <dd>

Stringa per la ricezione del nome del computer.

</dd> <dt>

*ObjectName* 
</dt> <dd>

Stringa che consente di ricevere il nome dell'oggetto.

</dd> <dt>

*InstanceName* 
</dt> <dd>

Stringa in cui ricevere il nome dell'istanza, se utilizzata.

</dd> <dt>

*ParentInstance* 
</dt> <dd>

Stringa per la ricezione dell'istanza padre, se utilizzata.

</dd> <dt>

*CounterName* 
</dt> <dd>

Stringa per la ricezione del nome del contatore.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Dimensione massima di ogni variabile di stringa utilizzata come parametro per la chiamata di funzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce un **Long** Integer uguale a Error \_ Success.

Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md). Di seguito sono riportati i valori possibili.



| Codice restituito                                                                                                     | Descrizione                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_argomento PDH non valido \_**</dt> </dl>           | La dimensione di uno o più buffer di stringa non è corretta.<br/>                          |
| <dl> <dt>**PDH \_ altri \_ dati**</dt> </dl>                  | Uno o più elementi del percorso del contatore sono troppo grandi per la lunghezza del buffer di ritorno.<br/> |
| <dl> <dt>**\_errore di \_ allocazione della memoria PDH \_**</dt> </dl> | Impossibile allocare un buffer di memoria temporaneo.<br/>                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

