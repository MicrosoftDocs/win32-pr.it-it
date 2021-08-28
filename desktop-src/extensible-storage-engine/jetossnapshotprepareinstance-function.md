---
description: Altre informazioni sulla funzione JetOSSnapshotPrepareInstance
title: Funzione JetOSSnapshotPrepareInstance
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4997be8f268d676fbd4a164281061b488e948168
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474387"
---
# <a name="jetossnapshotprepareinstance-function"></a>Funzione JetOSSnapshotPrepareInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotprepareinstance-function"></a>Funzione JetOSSnapshotPrepareInstance

La **funzione JetOSSnapshotPrepareInstance** seleziona un'istanza specifica come parte della sessione snapshot.

**Windows Vista:** **JetOSSnapshotPrepareInstance** è stato introdotto in Windows Vista.

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*snapId*

Identificatore della sessione snapshot.

*Istanza*

Istanza di che verrà utilizzata per questa chiamata.

*grbit*

Opzioni per questa chiamata. Questo parametro è riservato per usi futuri. L'unico valore valido è 0 (zero).

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Il puntatore id snapshot è <strong>NULL</strong> o il <em>parametro grbit</em> non è valido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Una sessione snapshot è già in corso.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>L'identificatore per la sessione snapshot non è valido.</p> | 



Se questa funzione ha esito positivo, l'istanza specificata farà parte della sessione snapshot.

Se questa funzione ha esito negativo, non viene apportata alcuna modifica allo stato del motore.

#### <a name="remarks"></a>Commenti

La normale chiamata alla sequenza API è: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), facoltativamente seguita da una o più chiamate a **JetOSSnapshotPrepareInstance** e quindi [da JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Dopo l'avvio, il blocco può essere terminato usando [JetOSSnapshotThaw.](./jetossnapshotthaw-function.md) In qualsiasi momento dopo la preparazione, la sessione snapshot può essere terminata improvvisamente con [JetOSSnapshotAbort](./jetossnapshotabort-function.md). Verranno generate voci del log eventi per i diversi passaggi dello snapshot.

Se **JetOSSnapshotPrepareInstance** non viene chiamato tra l'inizio della sessione ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) e il momento di blocco ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), tutte le istanze in esecuzione nel motore si bloccano e diventano parte della sessione snapshot. Ciò si verifica per due motivi:

  - Semplifica il codice per gli utenti che vogliono tutte le istanze.

  - Consente la compatibilità con le versioni precedenti per i chiamanti delle API snapshot.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[Parametri di gestione degli errori](./error-handling-parameters.md)  
[Errori del motore Archiviazione estendibile](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
