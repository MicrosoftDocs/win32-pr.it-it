---
description: 'Altre informazioni su: funzione JetBackup'
title: Funzione JetBackup
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319187"
---
# <a name="jetbackup-function"></a>Funzione JetBackup


_**Si applica a:** Windows | Windows Server_

## <a name="jetbackup-function"></a>Funzione JetBackup

La funzione **JetBackup** crea un backup del database mentre il database è online. Questa funzione è principalmente per la compatibilità con le versioni precedenti di Windows 2000 e dei motori di database precedenti, in cui è consentita una sola istanza di un database. In questo caso, l'istanza attiva è l'istanza di di cui viene eseguito il backup.

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parametri

*szBackupPath*

Directory in cui è archiviato il backup. Se il percorso di backup è NULL, la funzione tronca i log, se possibile.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.

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
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Crea un backup completo del database. In questo modo è possibile mantenere un backup esistente nella stessa directory se il nuovo backup non riesce.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Crea un backup incrementale anziché un backup completo. Ciò significa che verrà eseguito il backup solo dei file di log dall'ultimo backup completo o incrementale.</p></td>
</tr>
</tbody>
</table>


*pfnStatus*

Puntatore alla funzione di callback [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , che fornisce informazioni di notifica sullo stato di avanzamento dell'operazione di backup.

### <a name="return-value"></a>Valore restituito

La funzione restituisce uno dei codici di errore [JET_ERR](./jet-err.md) . Di seguito sono riportati i più comunemente restituiti. Per un elenco completo degli errori per questa API, vedere [codici di errore del motore di archiviazione estensibile](./extensible-storage-engine-error-codes.md).

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
<td><p>JET_errBackupInProgress</p></td>
<td><p>È già in corso un backup per la stessa istanza. Non sono consentiti più backup contemporaneamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>L'istanza non è ancora pronta per il backup mentre è in fase di inizializzazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>Un backup incrementale non è consentito se la registrazione circolare è attiva.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Le opzioni specificate non sono valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un parametro non valido è stato passato nell'API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Il percorso di destinazione non esiste.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>L'istanza è in esecuzione senza registrazione. Nessun backup consentito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>Si è verificato un errore di verifica del checksum in un file di log.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogWriteFail</p></td>
<td><p>La registrazione per l'istanza è temporanea o è disabilitata definitivamente a causa di un errore imprevisto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>Si è verificato un errore di verifica del checksum in una pagina del database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se la funzione ha esito positivo, tutti i file necessari per un ripristino fino al momento del backup saranno contenuti nella directory di backup. Se si tratta di un backup completo, i file saranno i file di database e i file di log necessari per portare il database in uno stato coerente. Se si tratta di un backup incrementale, verranno aggiunti solo i file di log alle directory, ma i file già esistenti (database e file di log), insieme ai nuovi file di log, potranno essere ripristinati per riportare il database allo stato in cui si trovava nel momento in cui è iniziato il backup.

Come effetto collaterale del backup, i file di log che non sono più necessari verranno troncati.

Allo stesso tempo, le intestazioni del database verranno aggiornate con le informazioni relative al momento in cui è avvenuto l'ultimo backup.

Se la funzione ha esito negativo, non saranno presenti file nella destinazione della directory di backup, quindi non sarà possibile eseguire alcun ripristino. Nello stesso tempo, i file di log correnti non verranno troncati.

#### <a name="remarks"></a>Commenti

Per i diversi passaggi del backup vengono generate voci del registro eventi, inclusi i nomi dei file, il troncamento del log e il risultato finale del backup.

I backup incrementali sono possibili solo dopo che è stato eseguito un backup completo. Inoltre, i backup incrementali sono possibili solo se la registrazione circolare è disattivata. È consigliabile che la directory di backup non contenga alcun file diverso da quello usato nel backup o aggiunto da un backup precedente riuscito.

La directory di backup deve esistere a meno che non sia impostato il parametro *JET_paramCreatePathIfNotExist* per l'istanza. Per informazioni, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md).

Il backup eseguirà una verifica del checksum su tutte le pagine di database utilizzate e a partire da Windows Server 2003 anche nei file di log. Questo consente di stimare l'integrità del database, anche per le pagine che non vengono lette durante le normali operazioni. Se viene rilevato un danneggiamento di questo tipo, il backup avrà esito negativo.

Durante il backup, il file di log corrente verrà completato e verrà generato un nuovo log. In questo modo, tutti i file di log necessari possono essere copie, perché il log corrente non verrà più usato.

Si consiglia vivamente di non usare il backup per scopi diversi dal backup e dal ripristino a livello di motore. Questo consente di ridurre al minimo la possibilità di ottenere errori durante le operazioni di backup e ripristino.

#### <a name="requirements"></a>Requisiti

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
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetBackupW</strong> (Unicode) e <strong>JetBackupA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
