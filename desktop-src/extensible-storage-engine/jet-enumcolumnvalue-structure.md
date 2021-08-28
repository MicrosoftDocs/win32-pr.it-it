---
description: 'Altre informazioni su: JET_ENUMCOLUMNVALUE struttura'
title: JET_ENUMCOLUMNVALUE struttura
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a4d9500980434c21f9dfa6584db666418605de8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988614"
---
# <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE struttura

La **JET_ENUMCOLUMNVALUE** enumera i valori di colonna di un record usando la [funzione JetEnumerateColumns.](./jetenumeratecolumns-function.md) [JetEnumerateColumns](./jetenumeratecolumns-function.md) restituisce una matrice **JET_ENUMCOLUMNVALUE** strutture. La matrice viene restituita in memoria allocata usando il callback compatibile con [la riallocazione](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a tale funzione.

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>Membri

**itagSequence**

Valore della colonna (in base all'indice in base uno) enumerato.

**Err**

Codice di stato della colonna risultante dall'enumerazione del valore della colonna.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_wrnColumnNull</p> | <p>Il valore della colonna richiesto è NULL.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p><em>L'elemento itagSequence</em> specificato nell'elemento della matrice <em>rgtagSequence</em> nello struct <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> corrispondente a questo <strong>JET_ENUMCOLUMNVALUE</strong> struct è zero.</p> | 
| <p>JET_wrnColumnTruncated</p> | <p>Il valore della colonna richiesto è stato troncato alla dimensione specificata prima di essere restituito.</p><p>Questo troncamento si verifica solo per le colonne di testo lungo e binarie lunghe che contengono grandi quantità di dati.</p> | 



**cbData**

Valore della colonna enumerato per la colonna.

Il buffer di output viene restituito in memoria allocata utilizzando il callback compatibile con [la rialloca](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns.](./jetenumeratecolumns-function.md)

**pvData**

Valore della colonna enumerato per la colonna.

Il buffer di output viene restituito in memoria allocata utilizzando il callback compatibile con [la rialloca](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a [JetEnumerateColumns.](./jetenumeratecolumns-function.md)

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
