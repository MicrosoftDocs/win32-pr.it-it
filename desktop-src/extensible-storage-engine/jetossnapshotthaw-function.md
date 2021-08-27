---
description: Altre informazioni sulla funzione JetOSSnapshotThaw
title: Funzione JetOSSnapshotThaw
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9be4bcff435fe30186b3b7585c79e3066987cc5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479057"
---
# <a name="jetossnapshotthaw-function"></a>Funzione JetOSSnapshotThaw


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotthaw-function"></a>Funzione JetOSSnapshotThaw

La **funzione JetOSSnapshotThaw** notifica al motore che può riprendere le normali operazioni di I/O dopo un periodo di blocco e uno snapshot riuscito.

**Windows XP:****JetOSSnapshotThaw** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*snapId*

Identificatore della sessione snapshot.

*grbit*

Questo parametro è riservato per un uso futuro e l'unico valore valido supportato è 0.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>La sessione snapshot non è valida o il <em>parametro grbit</em> non è valido.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>La sessione snapshot ha avuto un timeout interno prima che si verifica questa chiamata. Di conseguenza, le operazioni di I/O tornano normali prima della chiamata.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L'identificatore per la sessione snapshot non è valido.</p> | 



Se questa funzione ha esito positivo, una sessione snapshot termina e il normale comportamento del motore riprende. Una nuova sessione snapshot può essere avviata in un secondo momento.

Se questa funzione ha esito negativo, la sessione di snapshot corrente termina ma il blocco delle operazioni di I/O durante il periodo di snapshot non è stato rispettato internamente.

#### <a name="remarks"></a>Commenti

Verranno generate voci del log eventi per i diversi passaggi dello snapshot.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)
