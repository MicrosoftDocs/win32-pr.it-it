---
description: 'Altre informazioni su: JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
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
ms.openlocfilehash: e2eae9590d0151bcdb2dc5621ae6df9e41e068a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315634"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_tableid"></a>JET_TABLEID

Il tipo di dati JET_TABLEID contiene un handle per il cursore del database da usare per una chiamata all'API JET. Un cursore può essere utilizzato solo con la sessione utilizzata per aprire il cursore.

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a>Tipi di dati

JET_TABLEID

È possibile utilizzare **null** o [JET_tableidNil](./invalid-handle-constants.md) per indicare un handle di cursore non valido.

### <a name="remarks"></a>Commenti

Un cursore gestisce l'utilizzo di una tabella per il motore di database. Un cursore può eseguire le attività seguenti:

  - Analizza record

  - Cercare i record

  - Scegliere il tipo di ordinamento e la visibilità effettivi dei record

  - Creare, aggiornare o eliminare record

  - Modificare lo schema della tabella

La funzionalità supportata del cursore può variare in base alla modifica dello stato o del tipo della tabella sottostante. Ad esempio, una tabella temporanea potrebbe impedire la ricerca di dati quando viene aperta con determinate opzioni. Il cursore è sempre completamente connesso alla tabella sottostante e interagisce direttamente con tali dati senza alcuna memorizzazione nella cache. Quasi tutte le funzionalità di base di ISAM esposte da questo motore di database vengono elaborate tramite il cursore.

È possibile creare un cursore utilizzando [JetOpenTable](./jetopentable-function.md) o [JetOpenTempTable](./jetopentemptable-function.md). È possibile duplicare un cursore utilizzando [JetDupCursor](./jetdupcursor-function.md). Un cursore può essere chiuso in modo esplicito tramite [JetCloseTable](./jetclosetable-function.md) o chiuso in modo implicito tramite [JetEndSession](./jetendsession-function.md) o [JetTerm](./jetterm-function.md). Un cursore può essere anche chiuso in modo implicito da [JetRollback](./jetrollback-function.md) se è stato aperto nella transazione interrotta. Il numero massimo di cursori che è possibile creare in qualsiasi momento è controllato da [JET_paramMaxCursors](./resource-parameters.md), che può essere configurato tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md).

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_paramMaxSessions](./resource-parameters.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
