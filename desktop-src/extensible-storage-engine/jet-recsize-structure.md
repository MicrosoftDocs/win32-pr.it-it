---
description: 'Altre informazioni su: JET_RECSIZE struttura'
title: JET_RECSIZE struttura
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
ms.openlocfilehash: a7ea4520a75e83c77a6403a583e9131a15df337b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988230"
---
# <a name="jet_recsize-structure"></a>JET_RECSIZE struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_recsize-structure"></a>JET_RECSIZE struttura

La **JET_RECSIZE** viene usata da [JetGetRecordSize](./jetgetrecordsize-function.md) per restituire informazioni sui requisiti di utilizzo di un record nello spazio dati utente, nel numero di colonne del set, nel numero di valori e nello spazio di sovraccarico della struttura dei record ESE.

**Windows Vista:** La **JET_RECSIZE** è stata introdotta in Windows Vista.

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

**Nota**  La dimensione della chiave non è inclusa in questo.

**cbLongValueData**

Dati utente associati al record ma archiviati nell'albero a valori lunghi.

**Nota**  In questo modo non vengono conteggiati i valori long intrinseci.

**cbOverhead**

Sovraccarico della struttura dei record ESE per questo record. Sono incluse le dimensioni della chiave del record.

**cbLongValueOverhead**

Sovraccarico dei dati a valore lungo.

**Nota**  In questo modo non vengono conteggiati i valori long intrinseci.

**cNonTaggedColumns**

Numero totale di colonne fisse e variabili impostate in questo record.

**cTaggedColumns**

Numero totale di colonne con tag impostate in questo record.

**cLongValues**

Numero totale di valori long archiviati nell'albero long-value per questo record.

**Nota**  In questo modo non vengono conteggiati i valori long intrinseci.

**cMultiValues**

Accumulo del numero totale di valori oltre il primo per tutte le colonne del record.

### <a name="remarks"></a>Commenti

Il numero totale di valori nel record sarà **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetGetRecordSize](./jetgetrecordsize-function.md)
