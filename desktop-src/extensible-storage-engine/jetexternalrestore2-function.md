---
description: Altre informazioni sulla funzione JetExternalRestore2
title: Funzione JetExternalRestore2
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d2cbd4a13555d754cdbc1f9c02011b5891d6d6fcfae3fea822ddf6ad9953b78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719191"
---
# <a name="jetexternalrestore2-function"></a>Funzione JetExternalRestore2


_**Si applica a:** Windows | Windows Server_

## <a name="jetexternalrestore2-function"></a>Funzione JetExternalRestore2

La **funzione JetExternalRestore2** ripristina un backup esterno eseguito con le API di backup esterne e fornisce checkpoint da usare per le operazioni di registrazione circolare. Questa operazione è nota come ripristino rigido, che è simile ma diverso dal ripristino soft eseguito dalla [funzione JetInit.](./jetinit-function.md)

**Windows XP: JetExternalRestore2** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>Parametri

*szCheckpointFilePath*

Percorso del file del checkpoint da usare durante il ripristino se *szTargetInstanceCheckpointPath* non è specificato o il percorso ha un'istanza attiva o in esecuzione.

*szLogPath*

Percorso o directory per i log per la fase finale (annullamento) del ripristino ed eventualmente per i log di roll forward. Questo percorso può essere lo stesso di *szBackupLogPath*.

*rgrstmap*

Si tratta di una matrice [di JET_RSTMAP](./jet-rstmap-structure.md) struttura. Si tratta di una mappa di percorsi o nomi di file di database vecchi e nuovi. Viene usato perché potrebbe essere necessario ripristinare i database in un percorso diverso da quello da cui è stato eseguito il backup. Nel caso in cui più database siano collegati a un singolo set di registrazione, la mappa di ripristino può specificare un subset dei database da ripristinare.

*crstfilemap*

Numero di voci nel parametro di matrice *rgrstmap.*

*szBackupLogPath*

Percorso della directory in cui vengono ripristinati i file di log. Si tratta dei log letti durante la sequenza di backup esterna. Questo percorso può essere lo stesso di *szLogPath*.

*pLogInfo*

*PLogInfo* descrive diversi aspetti dei log di backup da recuperare. Questo parametro consente a **JetExternalRestore2** di prendere i parametri *genLow* e *genHigh* espliciti di **JetExternalRestore2,** nonché il nome del log di base, anziché un nome di base del log presunto di "edb".

*szTargetInstanceName*

Questo parametro è deprecato e non può essere usato nell'applicazione.

*szTargetInstanceLogPath*

Percorso per i log di roll forward se il percorso dei log da eseguire è in un'istanza o in un set di registrazione attivo. Questo valore non deve essere specificato se l'istanza di destinazione usa la registrazione circolare.

*szTargetInstanceCheckpointPath*

Percorso del checkpoint durante il ripristino se non è presente alcuna istanza attiva in esecuzione in questa destinazione. Questo valore non deve essere specificato se l'istanza di destinazione usa la registrazione circolare.

*Pfn*

Callback di stato, che segnala lo stato di avanzamento del ripristino.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Errori del motore Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).

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
<td><p>JET_errBadRestoreTargetInstance</p></td>
<td><p><em>SzTargetInstanceLogPath specificato</em> non appartiene a un'istanza inizializzata. Questo errore verrà restituito solo in Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted</p></td>
<td><p>Indica che il database è stato danneggiato o un file non riconosciuto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errEndingRestoreLogTooLow</p></td>
<td><p>Questo errore viene restituito se per uno dei file di log in <em>szBackupLogPath</em>è presente una generazione di log superiore a quella specificata in <em>genHigh</em> o <em>pLogInfo.ulGenHigh</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile aprire il file richiesto perché non è stato trovato nel percorso specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti conteneva un valore imprevisto o conteneva un valore che non aveva senso se combinato con il valore di un altro parametro. Ciò può verificarsi per <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>e così via quando <em>szTargetCheckpointPath</em> e <em>szTargetInstanceLogPath</em> non sono entrambi specificati o non entrambi non specificati. In altri casi, devono corrispondere ed essere entrambi specificati o entrambi non specificati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile trovare il percorso specificato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase</p></td>
<td><p>Questo errore viene restituito se il file di database specificato durante il ripristino non è un database di cui è stato eseguito il backup esterno.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>Il motore di database non può eseguire il ripristino esterno o il ripristino rigido in modalità a istanza singola. Questo errore verrà restituito solo in Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errStartingRestoreLogTooHigh</p></td>
<td><p>Questo errore viene restituito se uno dei file di log in <em>szBackupLogPath</em>ha una generazione di log inferiore a quella specificata da <em>genLow</em> o <em>pLogInfo.ulGenLow</em>.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, tutti i database di *rgrstmap* vengono completamente ripristinati e in uno stato pulito o coerente. A questo punto il database può essere rimontaggio in un'istanza esistente.

In caso di errore, il motore non è riuscito a ripristinare il database. Il database è in uno stato non valido e per ritentare il ripristino rigido è necessario ripristinare nuovamente l'intero database. In genere, l'origine di una situazione di questo tipo è il danneggiamento del disco o del log o un'altra forma di gestione errata del log o un set di log non continuo.

#### <a name="remarks"></a>Commenti

Vedere [JetExternalRestore](./jetexternalrestore-function.md).

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetExternalRestore2W</strong> (Unicode) e <strong>JetExternalRestore2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetInit](./jetinit-function.md)
