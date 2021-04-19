---
description: 'Altre informazioni su: struttura JET_RECSIZE2'
title: Struttura JET_RECSIZE2
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315085"
---
# <a name="jet_recsize2-structure"></a>Struttura JET_RECSIZE2


_**Si applica a:** Windows | Windows Server_

## <a name="jet_recsize2-structure"></a>Struttura JET_RECSIZE2

La struttura **JET_RECSIZE2** viene utilizzata da [JetGetRecordSize2](./jetgetrecordsize2-function.md) per restituire informazioni sui requisiti di utilizzo di un record in spazio dati utente, numero di colonne set, numero di valori e spazio overhead della struttura dei record ESE.

**Windows 7:** La struttura **JET_RECSIZE2** viene introdotta nel sistema operativo Windows 7.

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
```

### <a name="members"></a>Membri

**cbData**

Set di dati utente nel record.

**Nota**  La dimensione della chiave non è inclusa in questo oggetto.

**cbLongValueData**

Dati utente associati al record ma archiviati nella struttura ad albero di valori Long.

**Nota**  Non vengono conteggiati valori Long intrinseci.

**cbOverhead**

Overhead della struttura di record ESE per questo record. Sono incluse le dimensioni della chiave del record.

**cbLongValueOverhead**

Overhead dei dati con valori Long.

**Nota**  Non vengono conteggiati valori Long intrinseci.

**cNonTaggedColumns**

Numero totale di colonne fisse e variabili impostate in questo record.

**cTaggedColumns**

Numero totale di colonne con tag impostati in questo record.

**cLongValues**

Numero totale di valori Long archiviati nell'albero dei valori Long per questo record.

**Nota**  Non vengono conteggiati valori Long intrinseci.

**cMultiValues**

Accumulo del numero totale di valori oltre il primo per tutte le colonne del record.

**cCompressedColumns**

Numero totale di colonne compresse.

**cbDataCompressed**

Dimensioni compresse dei dati utente in questo record. Si tratta dello stesso valore di cbData se non vengono compressi valori Long intrinseci.

**cbLongValueDataCompressed**

Dimensioni compresse dei dati utente nell'albero con valori Long. Si tratta dello stesso valore dei dati cbLongValue se non vengono compressi valori Long separati.

### <a name="remarks"></a>Commenti

Il numero totale di valori nel record sarà **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

I dati logici nel record sono (cbData + cbLongValueData) e la dimensione fisica dei dati è (cbDataCompressed + cbLongValueDataCompressed). Questa operazione può essere utilizzata per calcolare il rapporto di compressione dei dati archiviati.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede il sistema operativo Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede il sistema operativo Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetGetRecordSize](./jetgetrecordsize-function.md)  
[JetGetRecordSize2](./jetgetrecordsize2-function.md)
