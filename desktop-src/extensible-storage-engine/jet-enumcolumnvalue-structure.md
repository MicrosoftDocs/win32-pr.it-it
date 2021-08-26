---
description: 'Altre informazioni su: JET_ENUMCOLUMNVALUE Structure'
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
ms.openlocfilehash: 86905d49bb798d37bad48087c48e77349ec10f57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482287"
---
# <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE struttura

La **JET_ENUMCOLUMNVALUE** enumera i valori di colonna di un record usando la [funzione JetEnumerateColumns.](./jetenumeratecolumns-function.md) [JetEnumerateColumns](./jetenumeratecolumns-function.md) restituisce una matrice **di** JET_ENUMCOLUMNVALUE struttura. La matrice viene restituita in memoria allocata usando il callback compatibile di [riallocare](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito a tale funzione.

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


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_wrnColumnNull</p> | <p>Il valore della colonna richiesta è NULL.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p><em>L'elemento itagSequence</em> specificato nell'elemento della matrice <em>rgtagSequence</em> nello struct <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> corrispondente JET_ENUMCOLUMNVALUE <strong>struct</strong> era zero.</p> | 
| <p>JET_wrnColumnTruncated</p> | <p>Il valore della colonna richiesta è stato troncato alle dimensioni specificate prima di essere restituito.</p><p>Questo troncamento si verifica solo per le colonne di testo lungo e binarie lunghe che contengono grandi quantità di dati.</p> | 



**cbData**

Valore della colonna enumerata per la colonna.

Il buffer di output viene restituito in memoria allocata usando il callback compatibile di [riallocare](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito [a JetEnumerateColumns](./jetenumeratecolumns-function.md).

**pvData**

Valore della colonna enumerata per la colonna.

Il buffer di output viene restituito in memoria allocata usando il callback compatibile di [riallocare](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito [a JetEnumerateColumns](./jetenumeratecolumns-function.md).

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
