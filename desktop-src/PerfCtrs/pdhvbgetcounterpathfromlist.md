---
description: La funzione PdhVbGetCounterPathFromList copia il percorso del contatore a cui fa riferimento il parametro Index da un elenco di percorsi dei contatori creato dall'utente dalla chiamata più recente alla funzione PdhVbCreateCounterPathList.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: Funzione PdhVbGetCounterPathFromList
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
ms.openlocfilehash: 85760bbcdcc81204340004304be1f0c14bf9bcbbbd7a5b59eebf47a25f7b15c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033781"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a>Funzione PdhVbGetCounterPathFromList

La funzione **PdhVbGetCounterPathFromList** copia il percorso del contatore a cui fa riferimento il parametro *Index* da un elenco di percorsi dei contatori creato dall'utente dalla chiamata più recente alla [**funzione PdhVbCreateCounterPathList.**](pdhvbcreatecounterpathlist.md)

> [!IMPORTANT]
> La funzione descritta in questo argomento potrebbe essere modificata o non disponibile in futuro. Microsoft consiglia invece di usare le funzioni descritte in [Funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbGetCounterPathFromList( \_ ByVal Index As Long, \_ ByVal Buffer As String, \_ ByVal BufferLength As Long \_ ) As Long

## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Indice del percorso del contatore da recuperare. Deve essere un valore maggiore o uguale a 1 e minore o uguale al valore restituito dalla funzione [**PdhVbCreateCounterPathList.**](pdhvbcreatecounterpathlist.md)

</dd> <dt>

*Buffer* 
</dt> <dd>

Stringa dimensionata e inizializzata che riceverà il percorso del contatore corrispondente al valore del parametro Index.

</dd> <dt>

*BufferLength* 
</dt> <dd>

Numero massimo di caratteri che si adatteranno alla stringa a cui fa riferimento Buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il numero di caratteri copiati in Buffer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




