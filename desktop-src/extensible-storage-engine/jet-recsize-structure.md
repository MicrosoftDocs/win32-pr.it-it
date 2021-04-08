---
description: 'Altre informazioni su: struttura JET_RECSIZE'
title: Struttura JET_RECSIZE
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
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
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749855"
---
# <a name="jet_recsize-structure"></a>Struttura JET_RECSIZE


_**Si applica a:** Windows | Windows Server_

## <a name="jet_recsize-structure"></a>Struttura JET_RECSIZE

La struttura **JET_RECSIZE** viene utilizzata da [JetGetRecordSize](./jetgetrecordsize-function.md) per restituire informazioni sui requisiti di utilizzo di un record in spazio dati utente, numero di colonne set, numero di valori e spazio overhead della struttura dei record ESE.

**Windows Vista:** La struttura **JET_RECSIZE** è stata introdotta in Windows Vista.

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
    } JET_RECSIZE;
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

### <a name="remarks"></a>Commenti

Il numero totale di valori nel record sarà **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetGetRecordSize](./jetgetrecordsize-function.md)
