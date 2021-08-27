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
ms.openlocfilehash: 04e59ddada8715872978ccc21da11a349e1b7c43
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983574"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**Si applica a:** Windows | Windows Server_

## <a name="jet_tableid"></a>JET_TABLEID

Il JET_TABLEID dati contiene un handle per il cursore di database da usare per una chiamata all'API JET. Un cursore può essere usato solo con la sessione usata per aprire il cursore.

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a>Tipi di dati

JET_TABLEID

È possibile usare **NULL** [o JET_tableidNil](./invalid-handle-constants.md) per indicare un handle di cursore non valido.

### <a name="remarks"></a>Commenti

Un cursore gestisce l'uso di una tabella per il motore di database. Un cursore può eseguire le attività seguenti:

  - Analizzare i record

  - Cercare i record

  - Scegliere l'ordinamento effettivo e la visibilità di tali record

  - Creare, aggiornare o eliminare record

  - Modificare lo schema della tabella

La funzionalità supportata del cursore potrebbe cambiare quando cambia lo stato o il tipo della tabella sottostante. Ad esempio, una tabella temporanea potrebbe non consentire la ricerca di dati quando viene aperta con determinate opzioni. Il cursore è sempre completamente connesso alla tabella sottostante e interagisce con i dati direttamente senza alcuna memorizzazione nella cache. Quasi tutte le funzionalità ISAM principali esposte da questo motore di database vengono esposte tramite il cursore.

È possibile creare un cursore [usando JetOpenTable](./jetopentable-function.md) o [JetOpenTempTable](./jetopentemptable-function.md). Un cursore può essere duplicato [usando JetDupCursor](./jetdupcursor-function.md). Un cursore può essere chiuso in modo esplicito [usando JetCloseTable](./jetclosetable-function.md) o chiuso in modo implicito tramite [JetEndSession](./jetendsession-function.md) o [JetTerm](./jetterm-function.md). Un cursore può anche essere chiuso in modo implicito [da JetRollback](./jetrollback-function.md) se è stato aperto nella transazione interrotta. Il numero massimo di cursori che è possibile creare in qualsiasi momento viene controllato da [JET_paramMaxCursors](./resource-parameters.md), che può essere configurato tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md).

### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 



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
