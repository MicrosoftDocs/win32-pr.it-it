---
description: 'Altre informazioni su: funzione JetOSSnapshotPrepare'
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
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315613"
---
# <a name="jetossnapshotprepare-function"></a>Funzione JetOSSnapshotPrepare


_**Si applica a:** Windows | Windows Server_

## <a name="jetossnapshotprepare-function"></a>Funzione JetOSSnapshotPrepare

La funzione **JetOSSnapshotPrepare** avvia i preparativi per una sessione snapshot. Una sessione snapshot è un breve intervallo di tempo in cui il motore non rilascia alcun disco IOs su disco, in modo che il motore possa partecipare a una sessione di snapshot del volume (se basata su uno snapshot writer).

**Windows XP:**  **JetOSSnapshotPrepare** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*psnapId*

Identificatore della sessione snapshot da avviare.

*grbit*

Opzioni per questa chiamata. Questo parametro può avere una combinazione dei valori seguenti.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valore</p></th>
<th><p>Significato</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>Snapshot normale.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIncrementalSnapshot</p></td>
<td><p>Verranno effettuati solo i file di log.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCopySnapshot</p></td>
<td><p>Uno snapshot di copia (normale o incrementale) senza troncamento del log.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitContinueAfterThaw</p></td>
<td><p>La sessione snapshot si verifica dopo <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> e richiede una chiamata di funzione <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitExplicitPrepare</p></td>
<td><p>Nessuna istanza verrà preparata per impostazione predefinita.</p>
<p><strong>Windows 7:</strong>  JET_bitExplicitPrepare è stato introdotto in Windows 7.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Il puntatore di ID snapshot è NULL o il parametro <em>grbit</em> non è valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Una sessione snapshot è già in corso e l'operazione non può avere più di una sessione snapshot in un determinato momento.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, sarà possibile avviare una sessione snapshot in qualsiasi momento con la fase di blocco IO. L'identificatore per la sessione verrà restituito e deve essere utilizzato nelle chiamate successive per la sessione snapshot.

Le istanze in esecuzione del motore verranno ora considerate parte della sessione snapshot.

**Windows Vista:**  Per specificare un subset diverso di istanze, è possibile chiamare [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) .

La normale chiamata di sequenza API è: **JetOSSnapshotPrepare**, seguita facoltativamente da una o più chiamate a [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)e quindi da [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Una volta avviato il blocco, è possibile terminarlo utilizzando [JetOSSnapshotThaw](./jetossnapshotthaw-function.md). In qualsiasi momento dopo la preparazione, la sessione snapshot può essere terminata improvvisamente con [JetOSSnapshotAbort](./jetossnapshotabort-function.md).

Se JET_bitContinueAfterThaw viene specificato dopo [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), la sessione snapshot rimarrà (anche se verrà ripresa l'i/O). In questo modo verrà abilitata una verifica dello snapshot e, se necessario, verrà abilitato il troncamento del log tramite [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) e verrà richiesta una chiamata a [JetOSSnapshotEnd](./jetossnapshotend-function.md).

Se questa funzione ha esito negativo, non viene apportata alcuna modifica allo stato del motore.

#### <a name="remarks"></a>Commenti

Verranno generate voci del registro eventi per i diversi passaggi dello snapshot.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)  
[JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md)
