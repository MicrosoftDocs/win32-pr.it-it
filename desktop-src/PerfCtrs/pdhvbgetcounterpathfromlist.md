---
description: La funzione PdhVbGetCounterPathFromList copia il percorso del contatore a cui fa riferimento il parametro index da un elenco di percorsi dei contatori creato dall'utente dalla chiamata più recente alla funzione PdhVbCreateCounterPathList.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: PdhVbGetCounterPathFromList (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312150"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a>PdhVbGetCounterPathFromList (funzione)

La funzione **PdhVbGetCounterPathFromList** copia il percorso del contatore a cui fa riferimento il parametro *index* da un elenco di percorsi dei contatori creato dall'utente dalla chiamata più recente alla funzione [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbGetCounterPathFromList ( \_ ByVal index As Long, \_ ByVal buffer As String, \_ ByVal bufferLength Long \_ ) Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Indice del percorso del contatore da recuperare. Deve essere un valore maggiore o uguale a 1 e minore o uguale al valore restituito dalla funzione [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .

</dd> <dt>

*Buffer* 
</dt> <dd>

Stringa dimensionata e inizializzata che riceverà il percorso del contatore che corrisponde al valore del parametro index.

</dd> <dt>

*BufferLength* 
</dt> <dd>

Numero massimo di caratteri che si adatteranno alla stringa a cui fa riferimento il buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il numero di caratteri copiati nel buffer.

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

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




