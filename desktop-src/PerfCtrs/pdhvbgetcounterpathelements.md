---
description: La funzione PdhVbGetCounterPathElements analizza una stringa di percorso del contatore delle prestazioni completa nei singoli elementi.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: Funzione PdhVbGetCounterPathElements
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
ms.openlocfilehash: fecd9ecac573ecc1a5afabcfc4a14bf6fd1ca5cee7b44387ea910b0cf1a5820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011329"
---
# <a name="pdhvbgetcounterpathelements-function"></a>Funzione PdhVbGetCounterPathElements

La **funzione PdhVbGetCounterPathElements** analizza una stringa di percorso del contatore delle prestazioni completa nei singoli elementi. Ogni variabile stringa deve avere le stesse dimensioni (*BufferSize*) e deve essere dimensionata e inizializzata prima di essere usata in questa funzione.

> [!IMPORTANT]
> La funzione descritta in questo argomento potrebbe essere modificata o non disponibile in futuro. È invece consigliabile usare le funzioni descritte in [Funzioni dei contatori delle prestazioni.](performance-counters-functions.md)

Funzione PdhVbGetCounterPathElements( \_ ByVal PathString as String, \_ ByVal MachineName as String, \_ ByVal ObjectName as String, \_ ByVal InstanceName as String, \_ ByVal ParentInstance as String, \_ ByVal CounterName as String, \_ ByVal BufferSize As Long \_ ) As Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*PathString* 
</dt> <dd>

Stringa del percorso del contatore che deve essere suddivisa nei singoli elementi.

</dd> <dt>

*MachineName* 
</dt> <dd>

Stringa per ricevere il nome del computer.

</dd> <dt>

*ObjectName* 
</dt> <dd>

Stringa per ricevere il nome dell'oggetto.

</dd> <dt>

*InstanceName* 
</dt> <dd>

Stringa per ricevere il nome dell'istanza, se utilizzato.

</dd> <dt>

*ParentInstance* 
</dt> <dd>

Stringa per ricevere l'istanza padre, se utilizzata.

</dd> <dt>

*Countername* 
</dt> <dd>

Stringa per ricevere il nome del contatore.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Dimensione massima di ogni variabile stringa usata come parametro per questa chiamata di funzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce un **valore Long** Integer uguale a ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice [di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di errore [PDH](pdh-error-codes.md). Di seguito sono riportati i valori possibili.



| Codice restituito                                                                                                     | Descrizione                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>**ARGOMENTO PDH \_ NON \_ VALIDO**</dt> </dl>           | Uno o più buffer di stringa non hanno le dimensioni corrette.<br/>                          |
| <dl> <dt>**PDH \_ MORE \_ DATA**</dt> </dl>                  | Uno o più elementi del percorso del contatore sono troppo grandi per la lunghezza del buffer restituito.<br/> |
| <dl> <dt>**ERRORE DI ALLOCAZIONE \_ DELLA MEMORIA PDH \_ \_**</dt> </dl> | Impossibile allocare un buffer di memoria temporaneo.<br/>                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

