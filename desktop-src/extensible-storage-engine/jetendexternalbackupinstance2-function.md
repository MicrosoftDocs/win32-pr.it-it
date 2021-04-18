---
description: 'Altre informazioni su: funzione JetEndExternalBackupInstance2'
title: JetEndExternalBackupInstance2 (funzione)
TOCTitle: JetEndExternalBackupInstance2 Function
ms:assetid: a30961f7-a1fb-44fe-881a-d46bf8f743b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294047(v=EXCHG.10)
ms:contentKeyID: 32765646
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e719885cc61ff3f3193046b632e9969b8d660f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315075"
---
# <a name="jetendexternalbackupinstance2-function"></a>JetEndExternalBackupInstance2 (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetendexternalbackupinstance2-function"></a>JetEndExternalBackupInstance2 (funzione)

La funzione **JetEndExternalBackupInstance2** termina una sessione di backup esterna. Questa API è l'ultima API in una serie di API che devono essere chiamate per eseguire un backup online (non basato su VSS) riuscito.

**Windows XP: JetEndExternalBackupInstance2** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*istanza*

Istanza di da utilizzare per questa chiamata.

**Windows 2000:** Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza. In questo caso, l'utilizzo di questa istanza globale è implicito.

**Windows XP:** Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza. In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.

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
<td><p>JET_bitBackupEndAbort<br />
0x0002</p></td>
<td><p>L'applicazione client sta interrompendo il backup.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupEndNormal<br />
0x0001</p></td>
<td><p>L'applicazione client ha completato completamente il backup e termina normalmente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupTruncateDone<br />
0x0100</p></td>
<td><p><strong>Windows Vista:  </strong> JET_bitBackupTruncateDone è stato introdotto in Windows Vista.</p>
<p>Il motore può contrassegnare le intestazioni del database nel modo appropriato (ad esempio, un backup completo completato), anche se la chiamata a Truncate non è stata completata.</p></td>
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
<td><p>JET_errBackupAbortByCaller</p></td>
<td><p><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</p>
<p>Il chiamante ha terminato un backup al centro della sequenza di backup senza segnalare l'intenzione con <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Questo errore è causato da un bug nel client di backup in Windows Server 2003 e versioni successive. In Windows XP viene restituito questo errore per una chiusura intenzionale della sequenza di backup esterna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p><strong>Windows Server 2003:  </strong> Questo valore restituito è stato introdotto in Windows Server 2003.</p>
<p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p><strong>Windows XP:  </strong> Questo valore restituito è stato introdotto in Windows XP.</p>
<p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza, quando sono già presenti più istanze.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se la funzione ha esito positivo, il backup esterno ha avuto esito positivo. Success indica che tutti i file, ad esempio i database e i log, appropriati per il tipo di backup (specificato in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) sono stati recuperati dal motore di backup. I file di cui è stato eseguito il backup possono essere ripristinati con ripristino hardware ([JetExternalRestore](./jetexternalrestore-function.md)).

Se questa funzione ha esito negativo, il backup esterno termina in genere. Errore indica che il backup non è valido a causa di un errore di utilizzo del client o dell'applicazione. È importante controllare il codice restituito per questa API per verificare che la sequenza di backup sia stata completata correttamente.

#### <a name="remarks"></a>Commenti

Se il motore è configurato per registrare gli eventi, viene registrato un evento per indicare la risoluzione del backup esterno.

Se la sequenza di backup non viene completata in ordine e con una chiamata riuscita a [JetEndExternalBackup](./jetendexternalbackup-function.md), i successivi backup incrementali potrebbero contenere un numero di dati superiore a quello previsto dall'applicazione.

Per ulteriori informazioni sulla sequenza di API di backup esterno, vedere [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

Prima di Windows Vista, se il troncamento del log non è stato eseguito, il motore ha considerato che il backup era un backup di copia. Tuttavia, il backup potrebbe essere un backup normale per il quale non è stato eseguito il troncamento (ad esempio, se sono presenti database scollegati). È possibile utilizzare l'opzione JET_bitBackupTruncateDone per informare il motore e consentire le modifiche appropriate dell'intestazione del database.

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

[Parametri di gestione degli errori](./error-handling-parameters.md)  
[Errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
