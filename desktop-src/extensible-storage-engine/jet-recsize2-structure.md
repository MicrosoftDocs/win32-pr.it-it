---
description: 'Altre informazioni su: JET_RECSIZE2 struttura'
title: JET_RECSIZE2 struttura
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
ms.openlocfilehash: c187d57149b7f0589d56439bfacbf7129ab4fe4a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987834"
---
# <a name="jet_recsize2-structure"></a>JET_RECSIZE2 struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_recsize2-structure"></a>JET_RECSIZE2 struttura

La **JET_RECSIZE2** viene usata da [JetGetRecordSize2](./jetgetrecordsize2-function.md) per restituire informazioni sui requisiti di utilizzo di un record nello spazio dati utente, nel numero di colonne del set, nel numero di valori e nello spazio di sovraccarico della struttura dei record ESE.

**Windows 7:** La **JET_RECSIZE2** è stata introdotta nel sistema operativo Windows 7.

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

**cCompressedColumns**

Numero totale di colonne compresse.

**cbDataCompressed**

Dimensione compressa dei dati utente in questo record. È uguale a cbData se non vengono compressi valori long intrinseci.

**cbLongValueDataCompressed**

Dimensione compressa dei dati utente nell'albero a valori lunghi. Corrisponde ai dati cbLongValue se non vengono compressi valori long separati.

### <a name="remarks"></a>Commenti

Il numero totale di valori nel record sarà **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

I dati logici nel record sono (cbData+cbLongValueData) e le dimensioni fisiche dei dati sono (cbDataCompressed+cbLongValueDataCompressed). Può essere usato per calcolare il rapporto di compressione dei dati archiviati.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows sistema operativo Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows sistema operativo Server 2008.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetGetRecordSize](./jetgetrecordsize-function.md)  
[JetGetRecordSize2](./jetgetrecordsize2-function.md)
