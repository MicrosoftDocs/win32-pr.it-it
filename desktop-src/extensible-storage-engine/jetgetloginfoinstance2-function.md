---
description: 'Altre informazioni su: funzione JetGetLogInfoInstance2'
title: JetGetLogInfoInstance2 (funzione)
TOCTitle: JetGetLogInfoInstance2 Function
ms:assetid: 50fdae92-611c-4dbf-846e-86cc836a23db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269247(v=EXCHG.10)
ms:contentKeyID: 32765549
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance2W
- JetGetLogInfoInstance2
- JetGetLogInfoInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f58a04c49a82604fb5ded09b6328e9e03df7963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313102"
---
# <a name="jetgetloginfoinstance2-function"></a>JetGetLogInfoInstance2 (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetloginfoinstance2-function"></a>JetGetLogInfoInstance2 (funzione)

La funzione **JetGetLogInfoInstance2** viene utilizzata durante un backup avviato da [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) per eseguire una query su un'istanza di per i nomi dei file di patch del database e i file di log delle transazioni che devono diventare parte del set di file di backup. Questi file possono essere successivamente aperti con [JetOpenFile](./jetopenfile-function.md) e letti usando [JetReadFile](./jetreadfile-function.md).

**Windows XP: JetGetLogInfoInstance2** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetGetLogInfoInstance2(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in_out_opt  JET_LOGINFO* pLogInfo
    );
```

### <a name="parameters"></a>Parametri

*istanza*

Istanza di da utilizzare per questa chiamata.

Per Windows 2000, la variante API che accetta questo parametro non è disponibile perché è supportata una sola istanza. In questo caso, l'utilizzo di questa istanza globale è implicito.

Per Windows XP e versioni successive, la variante API che non accetta questo parametro può essere chiamata solo quando il motore è in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza. In caso contrario, l'operazione avrà esito negativo con JET_errRunningInMultiInstanceMode.

*SZZ*

Il buffer di output che riceverà l'elenco di stringhe con terminazione null che descrivono il set di file di patch del database e i file di log delle transazioni che devono far parte del set di file di backup.

L'elenco di stringhe restituite in questo buffer è nello stesso formato di un multistringhe utilizzato dal registro di sistema. Ogni stringa con terminazione null viene restituita in sequenza seguita da un terminatore null finale.

*cbMax*

Dimensione massima in byte del buffer di output.

*pcbActual*

Riceve la quantità effettiva di dati stringa ricevuti nel buffer di output.

*pLogInfo*

Riceve informazioni strutturate sui file di log delle transazioni che devono far parte del set di file di backup.

Se questo parametro non è presente, il relativo valore viene considerato NULL.

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
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>L'operazione non è riuscita perché il backup esterno corrente è stato interrotto da una chiamata a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence</p></td>
<td><p>L'operazione di backup non è riuscita perché è stata chiamata fuori sequenza. <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> restituirà questo errore se sono presenti handle di file in attesa creati utilizzando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> per l'istanza di.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo problema può verificarsi per <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> quando l'handle di istanza specificato non è valido (Windows XP e versioni successive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>L'operazione non è riuscita perché non è in corso alcun backup esterno.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L'operazione non è riuscita perché è stato effettuato un tentativo di usare il motore in modalità legacy (modalità di compatibilità di Windows 2000) in cui è supportata una sola istanza quando sono già presenti più istanze.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, le informazioni richieste sul set di file di patch del database e i file di log delle transazioni che devono far parte del set di file di backup verranno inseriti nei buffer di output specificati. La macchina a stati di backup sarà avanzata in modo che il backup dei file di database non sia più consentito. Solo i file di patch del database e i file di log delle transazioni possono essere aperti per il backup oltre questo punto.

In caso di errore, lo stato dei buffer di output non è definito. L'errore comporterà l'annullamento dell'intero processo di backup per l'istanza.

#### <a name="remarks"></a>Commenti

È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup. L'applicazione deve sempre fornire un buffer per ricevere le dimensioni effettive dell'elenco e utilizzare tali informazioni per determinare se l'elenco è stato troncato.

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
<td><p>Implementato come <strong>JetGetLogInfoInstance2W</strong> (Unicode) e <strong>JetGetLogInfoInstance2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)
