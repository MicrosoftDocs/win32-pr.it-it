---
description: 'Altre informazioni su: funzione JetBackupInstance'
title: Funzione JetBackupInstance
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128175"
---
# <a name="jetbackupinstance-function"></a>Funzione JetBackupInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetbackupinstance-function"></a>Funzione JetBackupInstance

La funzione **JetBackupInstance** esegue un backup di flusso di un'istanza, inclusi tutti i database collegati, in una directory. Con più metodi di backup supportati dal motore di, questa è la funzione più semplice e incapsulata.

**Windows XP: JetBackupInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>Parametri

*istanza*

Istanza del database di cui eseguire il backup.

*szBackupPath*

Directory in cui è archiviato il backup. Se il percorso di backup è NULL per usare la funzione, i log vengono troncati, se possibile.

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
<td><p>Crea un backup incrementale anziché un backup completo. Ciò significa che verrà eseguito il backup solo dei file di log creati dopo l'ultimo backup completo o incrementale.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Riservato per utilizzi futuri.</p></td>
</tr>
</tbody>
</table>


*pfnStatus*

Puntatore alla funzione di callback [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , che fornisce informazioni di notifica sullo stato di avanzamento dell'operazione di backup.

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
<td><p>JET_errBackupInProgress</p></td>
<td><p>È già in corso un backup per la stessa istanza. Non sono consentiti più backup contemporaneamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>L'istanza non è ancora pronta per il backup mentre è in fase di inizializzazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</p></td>
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


Dopo che la funzione ha restituito esito positivo, nella directory di backup saranno presenti tutti i file necessari per un ripristino fino al momento del backup. Se si tratta di un backup completo, i file saranno i file di database e i file di log necessari per portare il database in uno stato coerente. Se si tratta di un backup incrementale, verranno aggiunti solo i file di log alle directory, ma i file già esistenti (database e file di log) insieme ai nuovi file di registro saranno in grado di ripristinare e ripristinare lo stato del database al momento del backup.

Come effetto collaterale del backup, i file di log che non sono più necessari verranno troncati.

Allo stesso tempo, le intestazioni del database verranno aggiornate con le informazioni relative al momento in cui è avvenuto l'ultimo backup.

In caso di errore, non saranno presenti file nella destinazione della directory di backup, quindi non sarà possibile eseguire alcun ripristino. Nello stesso tempo, i file di log correnti non verranno troncati.

#### <a name="remarks"></a>Commenti

Nei diversi passaggi del backup vengono generate voci del registro eventi, inclusi i nomi dei file, il troncamento del log e il risultato finale del backup.

Il backup incrementale è possibile solo dopo che è stato eseguito un backup completo. Inoltre, i backup incrementali sono possibili solo se la registrazione circolare è disattivata. È consigliabile che la directory di backup non contenga altri file, quindi quello incluso nel backup o aggiunto da un backup precedente riuscito.

La directory di backup deve esistere a meno che non sia impostato il parametro *JET_paramCreatePathIfNotExist* per l'istanza. Per informazioni, vedere [parametri di sistema](./extensible-storage-engine-system-parameters.md).

Il backup eseguirà la verifica del checksum su tutte le pagine di database utilizzate e a partire da Windows Server 2003 anche nei file di log. Questo consente di stimare l'integrità del database anche per le pagine che non vengono lette durante le normali operazioni. Se viene rilevato un danneggiamento di questo tipo, il backup avrà esito negativo.

Durante il backup, il file di log corrente verrà completato e verrà avviata una nuova generazione del log. In questo modo sarà possibile copiare i file di log necessari, perché l'ultimo necessario non sarà più in uso.

Si consiglia vivamente di non usare il backup per altri scopi, quindi il backup e il ripristino a livello di motore. Questa operazione consente di ridurre al minimo le modifiche apportate agli errori durante le operazioni di backup e ripristino.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetBackupInstanceW</strong> (Unicode) e <strong>JetBackupInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
