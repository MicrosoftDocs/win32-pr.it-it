---
description: 'Altre informazioni su: JET_THREADSTATS Structure'
title: JET_THREADSTATS struttura
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 7f94c9911fb7ab974f87cfed41e92b53ac0a66cb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983564"
---
# <a name="jet_threadstats-structure"></a>JET_THREADSTATS struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_threadstats-structure"></a>JET_THREADSTATS struttura

La **JET_THREADSTATS** contiene statistiche cumulative sul lavoro eseguito dal motore di database nel thread corrente. Queste informazioni vengono restituite [tramite JetGetThreadStats.](./jetgetthreadstats-function.md)

**Windows Vista:**  La **JET_THREADSTATS** struttura è stata introdotta in Windows Vista.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a>Membri

**cbStruct**

Dimensioni della struttura **JET_THREADSTATS** restituita, in byte.

**Nota:**  La **JET_THREADSTATS** struttura verrà espansa in futuro per contenere altre statistiche. Le nuove statistiche verranno aggiunte alla fine della struttura e possono essere recuperate con un aumento delle dimensioni del buffer di output. La presenza di statistiche aggiuntive può essere dedotto da un valore **cbStruct più** grande.

**cPageReferenced**

Numero totale di pagine di database visitate dal motore di database nel thread corrente.

**cPageRead**

Numero totale di pagine di database recuperate dal disco dal motore di database nel thread corrente.

**cPagePreread**

Numero totale di pagine di database preletturate dal disco dal motore di database nel thread corrente.

**cPageDirtied**

Numero totale di pagine di database, senza modifiche non scritte, modificate dal motore di database nel thread corrente.

**cPageRedirtied**

Numero totale di pagine di database, con modifiche non scritte, modificate dal motore di database nel thread corrente.

**cLogRecord**

Numero totale di record del log delle transazioni generati dal motore di database nel thread corrente.

**cbLogRecord**

Dimensione totale in byte dei record del log delle transazioni generati dal motore di database nel thread corrente.

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



### <a name="see-also"></a>Vedere anche

[JetGetThreadStats](./jetgetthreadstats-function.md)
