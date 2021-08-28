---
description: 'Altre informazioni su: JET_RECSIZE Structure'
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
ms.openlocfilehash: 4fd0f59c821fa80d8de46f97e05aa1944354018e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475947"
---
# <a name="jet_recsize-structure"></a>JET_RECSIZE struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_recsize-structure"></a>JET_RECSIZE struttura

La **JET_RECSIZE** utilizzata da [JetGetRecordSize](./jetgetrecordsize-function.md) per restituire informazioni sui requisiti di utilizzo di un record nello spazio dati utente, sul numero di colonne del set, sul numero di valori e sullo spazio di sovraccarico della struttura dei record ESE.

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

**Nota:**  Le dimensioni della chiave non sono incluse in questo.

**cbLongValueData**

Dati utente associati al record ma archiviati nell'albero a valori lunghi.

**Nota:**  In questo modo non vengono conteggiati i valori long intrinseci.

**cbOverhead**

Sovraccarico della struttura di record ESE per questo record. Sono incluse le dimensioni della chiave del record.

**cbLongValueOverhead**

Sovraccarico dei dati long-value.

**Nota:**  In questo modo non vengono conteggiati i valori long intrinseci.

**cNonTaggedColumns**

Numero totale di colonne fisse e variabili impostate in questo record.

**cTaggedColumns**

Numero totale di colonne contrassegnate impostate in questo record.

**cLongValues**

Numero totale di valori long archiviati nell'albero dei valori long per questo record.

**Nota:**  In questo modo non vengono conteggiati i valori long intrinseci.

**cMultiValues**

Accumulo del numero totale di valori oltre la prima per tutte le colonne del record.

### <a name="remarks"></a>Commenti

Il numero totale di valori nel record sarà **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetGetRecordSize](./jetgetrecordsize-function.md)
