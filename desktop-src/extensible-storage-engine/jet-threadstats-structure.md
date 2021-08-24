---
description: 'Altre informazioni su: JET_THREADSTATS struttura'
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
ms.openlocfilehash: 9dcf88afc4b0f01a1691f9fb287491e9adfe71521e394a0e6b278c556fb5741f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832861"
---
# <a name="jet_threadstats-structure"></a>JET_THREADSTATS struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_threadstats-structure"></a>JET_THREADSTATS struttura

La **JET_THREADSTATS** contiene statistiche cumulative sul lavoro eseguito dal motore di database nel thread corrente. Queste informazioni vengono restituite [tramite JetGetThreadStats.](./jetgetthreadstats-function.md)

**Windows Vista:**  La **JET_THREADSTATS** è stata introdotta in Windows Vista.

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

Dimensione della struttura **JET_THREADSTATS** restituita, in byte.

**Nota**  La **JET_THREADSTATS** si espanderà in futuro per contenere altre statistiche. Le nuove statistiche verranno aggiunte alla fine della struttura e potranno essere recuperate con un aumento delle dimensioni del buffer di output. La presenza di statistiche aggiuntive può essere dedotto da un valore **cbStruct più** grande.

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

Dimensioni totali in byte dei record del log delle transazioni generati dal motore di database nel thread corrente.

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JetGetThreadStats](./jetgetthreadstats-function.md)
