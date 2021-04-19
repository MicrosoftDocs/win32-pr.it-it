---
description: 'Altre informazioni su: struttura JET_THREADSTATS'
title: Struttura JET_THREADSTATS
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
ms.openlocfilehash: 2b84de9a4f64db5dda261b8ee177787f62fd01ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316471"
---
# <a name="jet_threadstats-structure"></a>Struttura JET_THREADSTATS


_**Si applica a:** Windows | Windows Server_

## <a name="jet_threadstats-structure"></a>Struttura JET_THREADSTATS

La struttura **JET_THREADSTATS** contiene statistiche cumulative sul lavoro eseguito dal motore di database sul thread corrente. Queste informazioni vengono restituite tramite [JetGetThreadStats](./jetgetthreadstats-function.md).

**Windows Vista:**  La struttura **JET_THREADSTATS** è stata introdotta in Windows Vista.

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

Dimensioni in byte della struttura **JET_THREADSTATS** restituita.

**Nota**  La struttura di **JET_THREADSTATS** si espanderà in futuro per contenere più statistiche. Le nuove statistiche verranno aggiunte alla fine della struttura e potranno essere recuperate con una dimensione del buffer di output maggiore. La presenza di statistiche aggiuntive può essere dedotta da un valore **cbStruct** più grande.

**cPageReferenced**

Numero totale di pagine di database visitate dal motore di database sul thread corrente.

**cPageRead**

Numero totale di pagine del database recuperate dal disco dal motore di database sul thread corrente.

**cPagePreread**

Numero totale di pagine di database prelette dal disco dal motore di database sul thread corrente.

**cPageDirtied**

Numero totale di pagine di database, senza modifiche non scritte, modificate dal motore di database sul thread corrente.

**cPageRedirtied**

Numero totale di pagine di database, con modifiche non scritte, modificate dal motore di database sul thread corrente.

**cLogRecord**

Numero totale di record del log delle transazioni generati dal motore di database sul thread corrente.

**cbLogRecord**

Dimensioni totali in byte dei record del log delle transazioni generati dal motore di database sul thread corrente.

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

[JetGetThreadStats](./jetgetthreadstats-function.md)
