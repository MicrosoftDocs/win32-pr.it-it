---
description: 'Altre informazioni su: funzione JetOpenTempTable3'
title: Funzione JetOpenTempTable3
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7820f90ef0192c1f700759835bf1572b187cf3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305730"
---
# <a name="jetopentemptable3-function"></a>Funzione JetOpenTempTable3


_**Si applica a:** Windows | Windows Server_

## <a name="jetopentemptable3-function"></a>Funzione JetOpenTempTable3

La funzione **JetOpenTempTable3** crea una tabella temporanea con un solo indice che può essere usato per archiviare e recuperare record come una tabella ordinaria creata usando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale.

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*prgcolumndef*

Identifica le definizioni di colonna delle colonne da creare nella tabella temporanea.

Per le opzioni di definizione di colonna che possono essere utilizzate con una tabella temporanea sono presenti importanti limitazioni. Per altre informazioni, vedere la sezione Osservazioni.

Oltre alle normali opzioni di definizione di colonna, è possibile specificare anche zero o più delle opzioni seguenti che sono rilevanti solo nel contesto di una tabella temporanea.

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
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Questa opzione indica che l'ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente. Se questa opzione viene specificata senza JET_bitColumnTTKey, questa opzione viene ignorata.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Questa opzione indica che la colonna sarà una colonna chiave per la tabella temporanea.</p>
<p>L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea. La prima definizione di colonna nella matrice con questo set di opzioni sarà la colonna chiave più significativa e così via. Se sono richieste più colonne chiave che possono essere supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</p></td>
</tr>
</tbody>
</table>


*CColumn*

Vedere *prgcolumndef*.

*pidxunicode*

ID delle impostazioni locali e flag di normalizzazione che verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.

Quando questo parametro non è presente, viene utilizzato il valore LCID predefinito per confrontare eventuali colonne chiave Unicode nella tabella temporanea. Il valore LCID predefinito corrisponde alle impostazioni locali per l'inglese (Stati Uniti).

Quando questo parametro non è presente, i flag di normalizzazione predefiniti verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.

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
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Questa opzione richiede che qualsiasi tentativo di inserire un record con la stessa chiave di indice di un record inserito in precedenza avrà immediatamente esito negativo con JET_errKeyDuplicate. Se questa opzione non è richiesta, è possibile che un duplicato venga rilevato immediatamente e non riesca o venga rimosso automaticamente in un secondo momento, a seconda della strategia scelta dal motore di database per implementare la tabella temporanea in base alla funzionalità richiesta.</p>
<p>Se questa funzionalità non è necessaria, è consigliabile non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Questa opzione impone al gestore tabelle temporaneo di abbandonare qualsiasi tentativo di scegliere una strategia intelligente per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>Questa opzione richiede che la tabella temporanea venga creata solo se Gestione tabelle temporanee è in grado di utilizzare l'implementazione ottimizzata per i risultati intermedi delle query. Se una caratteristica della tabella temporanea impedisce l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</p>
<p>Un effetto collaterale di questa opzione consiste nel consentire alla tabella temporanea di contenere record con chiavi di indice duplicate. Per ulteriori informazioni, vedere JET_bitTTUnique.</p>
<p>Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTIndexed</p></td>
<td><p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di <a href="gg294103(v=exchg.10).md">JetSeek</a> per la ricerca di record in base alla chiave di indice.</p>
<p>Se questa funzionalità non è necessaria, è consigliabile non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUnique</p></td>
<td><p>Questa opzione richiede che i record con chiavi di indice duplicate vengano rimossi dal set di record finale nella tabella temporanea.</p>
<p>Prima di Windows Server 2003, il motore di database presuppone sempre che questa opzione sia attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci. A partire da Windows Server 2003, è ora possibile creare una tabella temporanea che non rimuove i duplicati quando viene specificata anche l'opzione JET_bitTTForwardOnly.</p>
<p>Non è possibile stabilire quale duplicato avrà vinto e quali duplicati verranno eliminati in generale. Tuttavia, quando viene richiesta l'opzione JET_bitTTErrorOnDuplicateInsertion, il primo record con una chiave di indice specificata da inserire nella tabella temporanea sarà sempre vincente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile per consentire la modifica successiva dei record che sono stati inseriti in precedenza. Se questa funzionalità non è necessaria, è consigliabile non richiederla.</p>
<p>Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi dei record in ordine arbitrario e direzione usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</p>
<p>Se questa funzionalità non è necessaria, è consigliabile non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Questa opzione richiede che i valori della colonna chiave NULL siano ordinati più vicino alla fine dell'indice rispetto ai valori di colonna chiave non NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTIntrinsicLVsOnly</p></td>
<td><p>Richieste per consentire solo valori Long intrinseci.</p>
<p><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> è stato introdotto in Windows 7.</p></td>
</tr>
</tbody>
</table>


*pTableID*

Il buffer di output che riceverà il nuovo cursore aperto nella tabella temporanea appena creata.

*prgcolumnid*

Buffer di output che riceverà la matrice di ID di colonna generati durante la creazione della tabella temporanea.

Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione della matrice di input.

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
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p><strong>JetOpenTempTable3</strong> non riuscito perché è stato specificato JET_bitTTForwardOnly e non è stato possibile creare la tabella temporanea specificata con l'ottimizzazione di sola trasmissione. Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Impossibile creare l'indice perché è stata specificata una definizione di indice non valida. <strong>JetOpenTempTable3</strong> restituirà questo errore quando:</p>
<ul>
<li><p>Le impostazioni locali indipendenti dalla lingua sono specificate.</p></li>
<li><p>È stato specificato un set di flag di normalizzazione non valido.</p></li>
</ul>
<p>Questo errore verrà restituito solo da Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Il membro <strong>CP</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200). Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Il membro <strong>coltyp</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su un tipo di colonna valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un ID delle impostazioni locali non valido. È possibile che l'ID delle impostazioni locali sia completamente non valido o che il Language Pack associato non sia installato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un set di flag di normalizzazione non valido. Questo errore verrà restituito solo da Windows XP e versioni successive. In Windows 2000, i flag di normalizzazione non validi comporteranno invece JET_errIndexInvalidDef.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa. Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in base al massimo sforzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore. Le risorse del cursore vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</p>
<p><strong>JetOpenTempTable3</strong> può restituire JET_errOutOfMemory se lo spazio degli indirizzi del processo host diventa troppo frammentato. Il gestore tabelle temporanee allocherà sempre un blocco di spazio degli indirizzi pari a 1 MB per ogni tabella temporanea creata indipendentemente dalla quantità di dati da archiviare.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns</p></td>
<td><p>È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella. Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella. Il numero di indici il cui schema può essere memorizzato nella cache viene configurato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella. Il numero di tabelle il cui schema può essere memorizzato nella cache viene configurato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea. Le risorse della tabella temporanea vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, verrà restituito un cursore aperto nella tabella temporanea appena creata. Lo stato del database temporaneo sarà pronto per contenere la nuova tabella temporanea. Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.

In caso di errore, la tabella temporanea non verrà creata e non verrà restituito un cursore. Lo stato del database temporaneo può essere modificato. Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.

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
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[Errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md)  
[Parametri di gestione degli errori](./error-handling-parameters.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
