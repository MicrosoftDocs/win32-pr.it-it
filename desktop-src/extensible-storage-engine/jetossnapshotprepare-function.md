---
description: 'Altre informazioni su: Funzione JetOSSnapshotPrepare'
title: Funzione JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 010cafd19ffde09b3083dd3cb6e6a69fa2268f11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470328"
---
# <a name="jetossnapshotprepare-function"></a>Funzione JetOSSnapshotPrepare


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotprepare-function"></a>Funzione JetOSSnapshotPrepare

La **funzione JetOSSnapshotPrepare** avvia i preparativi per una sessione di snapshot. Una sessione snapshot è un breve intervallo di tempo in cui il motore non esegue operazioni di I/O di scrittura su disco, in modo che il motore possa partecipare a una sessione di snapshot del volume (se basata su un writer di snapshot).

**Windows XP:****JetOSSnapshotPrepare** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*psnapId*

Identificatore della sessione snapshot da iniziare.

*grbit*

Opzioni per questa chiamata. Questo parametro può avere una combinazione dei valori seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>0</p> | <p>Snapshot normale.</p> | 
| <p>JET_bitIncrementalSnapshot</p> | <p>Verranno prelevati solo i file di log.</p> | 
| <p>JET_bitCopySnapshot</p> | <p>Snapshot di copia (normale o incrementale) senza troncamento del log.</p> | 
| <p>JET_bitContinueAfterThaw</p> | <p>La sessione snapshot si verifica dopo <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> e richiederà una <a href="gg294136(v=exchg.10).md">chiamata di funzione JetOSSnapshotEnd.</a></p> | 
| <p>JET_bitExplicitPrepare</p> | <p>Per impostazione predefinita, non verrà preparata alcuna istanza.</p><p><strong>Windows 7:</strong>  JET_bitExplicitPrepare è stato introdotto in Windows 7.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Il puntatore all'ID dello snapshot è NULL o il <em>parametro grbit</em> non è valido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Una sessione snapshot è già in corso e l'operazione non può avere più di una sessione snapshot in un determinato momento.</p> | 



Se questa funzione ha esito positivo, una sessione snapshot potrà essere avviata in qualsiasi momento con la fase di blocco I/O. Verrà restituito l'identificatore per la sessione e deve essere utilizzato nelle chiamate successive per la sessione snapshot.

Le istanze in esecuzione del motore verranno ora considerate parte della sessione di snapshot.

**Windows Vista:**  Per specificare un subset diverso di istanze, è possibile [chiamare JetOSSnapshotPrepareInstance.](./jetossnapshotprepareinstance-function.md)

La normale chiamata della sequenza API è: **JetOSSnapshotPrepare**, facoltativamente seguita da una o più chiamate a [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)e quindi [da JetOSSnapshotFreeze.](./jetossnapshotfreeze-function.md) Dopo l'avvio, il blocco può essere terminato usando [JetOSSnapshotThaw.](./jetossnapshotthaw-function.md) In qualsiasi momento dopo la preparazione, la sessione snapshot può essere terminata improvvisamente con [JetOSSnapshotAbort](./jetossnapshotabort-function.md).

Se JET_bitContinueAfterThaw viene specificato dopo [JetOSSnapshotThaw,](./jetossnapshotthaw-function.md)la sessione snapshot rimarrà (anche se l'I/O riprenderà). In questo modo verrà abilitata la verifica dello snapshot e, se necessario, verrà abilitato il troncamento del log tramite [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) e sarà necessaria una chiamata a [JetOSSnapshotEnd.](./jetossnapshotend-function.md)

Se questa funzione ha esito negativo, non si verifica alcuna modifica dello stato del motore.

#### <a name="remarks"></a>Commenti

Verranno generate voci del registro eventi per i diversi passaggi dello snapshot.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)  
[JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md)
