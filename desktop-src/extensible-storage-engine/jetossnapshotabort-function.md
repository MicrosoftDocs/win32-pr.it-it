---
description: 'Altre informazioni su: Funzione JetOSSnapshotAbort'
title: Funzione JetOSSnapshotAbort
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08e56bc95798559453c383549570f9470b55fa82
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474417"
---
# <a name="jetossnapshotabort-function"></a>Funzione JetOSSnapshotAbort


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotabort-function"></a>Funzione JetOSSnapshotAbort

La **funzione JetOSSnapshotAbort** notifica al motore che è possibile riprendere le normali operazioni di I/O dopo che un periodo di blocco è terminato con uno snapshot non riuscito.

**Windows Server 2003:****JetOSSnapshotAbort** è stato introdotto in Windows Server 2003.  

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*snapId*

Identificatore della sessione snapshot.

*grbit*

Opzioni per questa chiamata. Questo parametro è riservato per un uso futuro e l'unico valore valido supportato è 0 (zero).

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>La sessione snapshot non è valida o il parametro grbit non è valido.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L'identificatore per la sessione snapshot non è valido.</p> | 



Se questa funzione ha esito positivo, la sessione snapshot terminerà e verrà ripreso il normale comportamento del motore. Una nuova sessione snapshot può essere avviata in un secondo momento.

Se questa funzione ha esito negativo, la sessione snapshot non verrà interrotta.

#### <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata al posto di [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) per informare il motore che lo snapshot è stato interrotto per motivi non correlati al motore. Queste informazioni possono essere usate in un secondo momento per inviare messaggi del registro eventi relativi alla sessione snapshot o per determinare altre azioni appropriate.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
