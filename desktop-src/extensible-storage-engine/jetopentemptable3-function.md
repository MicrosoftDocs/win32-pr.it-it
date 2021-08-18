---
description: Altre informazioni sulla funzione JetOpenTempTable3
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
ms.openlocfilehash: 616a1a5a93c10ae79894c81e4530edc618848716190b887f16e850f89e3a79e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978817"
---
# <a name="jetopentemptable3-function"></a>Funzione JetOpenTempTable3


_**Si applica a:** Windows | Windows Server_

## <a name="jetopentemptable3-function"></a>Funzione JetOpenTempTable3

La **funzione JetOpenTempTable3** crea una tabella temporanea con un singolo indice che può essere usato per archiviare e recuperare record esattamente come una normale tabella creata usando [JetCreateTableColumnIndex.](./jetcreatetablecolumnindex-function.md) Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando vi si accede in modo puramente sequenziale.

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

Esistono limitazioni importanti per le opzioni di definizione della colonna che possono essere usate con una tabella temporanea. Per altre informazioni, vedere la sezione Osservazioni.

Oltre alle consuete opzioni di definizione della colonna, è possibile specificare anche zero o più delle opzioni seguenti rilevanti solo nel contesto di una tabella temporanea.

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
<p>L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea. La prima definizione di colonna nella matrice con questo set di opzioni sarà la colonna chiave più significativa e così via. Se sono richieste più colonne chiave di quelle supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</p></td>
</tr>
</tbody>
</table>


*ccolumn*

Vedere *prgcolumndef*.

*pidxunicode*

ID delle impostazioni locali e flag di normalizzazione che verranno usati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.

Quando questo parametro non è presente, verrà usato l'LCID predefinito per confrontare le colonne chiave Unicode nella tabella temporanea. L'LCID predefinito è l'inglese degli Stati Uniti.

Quando questo parametro non è presente, verranno usati i flag di normalizzazione predefiniti per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più delle opzioni seguenti.

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
<td><p>Questa opzione richiede che qualsiasi tentativo di inserire un record con la stessa chiave di indice di un record inserito in precedenza avrà immediatamente esito negativo JET_errKeyDuplicate. Se questa opzione non è richiesta, un duplicato può essere rilevato immediatamente e avere esito negativo o può essere rimosso automaticamente in un secondo momento a seconda della strategia scelta dal motore di database per implementare la tabella temporanea in base alla funzionalità richiesta.</p>
<p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Questa opzione impone al gestore tabelle temporaneo di abbandonare qualsiasi tentativo di scegliere una strategia intelligente per la gestione della tabella temporanea che comporta prestazioni migliorate.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>Questa opzione richiede che la tabella temporanea sia creata solo se il gestore tabelle temporaneo può usare l'implementazione ottimizzata per i risultati intermedi delle query. Se una caratteristica della tabella temporanea impedisce l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</p>
<p>Un effetto collaterale di questa opzione è consentire alla tabella temporanea di contenere record con chiavi di indice duplicate. Vedere JET_bitTTUnique per altre informazioni.</p>
<p>Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTIndexed</p></td>
<td><p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di <a href="gg294103(v=exchg.10).md">JetSeek</a> per cercare i record in base alla chiave di indice.</p>
<p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUnique</p></td>
<td><p>Questa opzione richiede che i record con chiavi di indice duplicate siano rimossi dal set finale di record nella tabella temporanea.</p>
<p>Prima di Windows Server 2003, il motore di database presupponeva sempre che questa opzione fosse attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci. A Windows Server 2003, è ora possibile creare una tabella temporanea che NON rimuove i duplicati quando viene specificata anche l'opzione JET_bitTTForwardOnly.</p>
<p>Non è possibile sapere quale duplicato vincerà e quali duplicati verranno eliminati in generale. Tuttavia, quando viene JET_bitTTErrorOnDuplicateInsertion richiesta l'opzione , il primo record con una chiave di indice specificata da inserire nella tabella temporanea vincerà sempre.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire la successiva modifica dei record inseriti in precedenza. Se questa funzionalità non è necessaria, è meglio non richiederla.</p>
<p>Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi dei record in ordine arbitrario e in direzione tramite <a href="gg294117(v=exchg.10).md">JetMove</a>.</p>
<p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Questa opzione richiede l'ordinamento dei valori di colonna chiave NULL più vicini alla fine dell'indice rispetto ai valori di colonna chiave non NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTIntrinsicLVsOnly</p></td>
<td><p>Richieste per consentire solo valori long intrinseci.</p>
<p><strong>Windows 7:</strong> <strong>la JET_bitTTIntrinsicLVsOnly</strong> è stata introdotta in Windows 7.</p></td>
</tr>
</tbody>
</table>


*ptableid*

Buffer di output che riceverà il nuovo cursore aperto nella tabella temporanea appena creata.

*prgcolumnid*

Buffer di output che riceverà la matrice di ID di colonna generati durante la creazione della tabella temporanea.

Gli ID colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni di questo buffer devono corrispondere alle dimensioni della matrice di input.

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
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p><strong>JetOpenTempTable3</strong> non riuscito perché JET_bitTTForwardOnly è stato specificato e non è stato possibile creare la tabella temporanea specificata usando l'ottimizzazione forward-only. Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Impossibile creare l'indice perché è stata specificata una definizione di indice non valida. <strong>JetOpenTempTable3</strong> restituirà questo errore quando:</p>
<ul>
<li><p>Vengono specificate le impostazioni locali indipendenti dalla lingua.</p></li>
<li><p>È stato specificato un set non valido di flag di normalizzazione.</p></li>
</ul>
<p>Questo errore verrà restituito solo da Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Il <strong>membro cp</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono Inglese (1252) e Unicode (1200). Il valore 0 indica che verrà usato il valore predefinito (inglese, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Il <strong>membro coltyp</strong> della <a href="gg294130(v=exchg.10).md">struttura JET_COLUMNDEF</a> non è stato impostato su un tipo di colonna valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Non è stato possibile creare l'indice perché si è tentato di usare un ID impostazioni locali non valido. L'ID delle impostazioni locali potrebbe non essere completamente valido o il language pack potrebbe non essere installato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un set non valido di flag di normalizzazione. Questo errore verrà restituito solo da Windows XP e versioni successive. In Windows 2000, i flag di normalizzazione non validi JET_errIndexInvalidDef invece.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa. Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo con il massimo sforzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore. Le risorse cursore vengono <a href="gg294044(v=exchg.10).md">configurate usando JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxCursors</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p>
<p><strong>JetOpenTempTable3</strong> può restituire JET_errOutOfMemory se lo spazio indirizzi del processo host diventa troppo frammentato. Il gestore tabelle temporanee alloca sempre un blocco di 1 MB di spazio di indirizzi per ogni tabella temporanea creata indipendentemente dalla quantità di dati da archiviare.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La stessa sessione non può essere usata per più thread contemporaneamente.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Si è tentato di aggiungere troppe colonne alla tabella. Una tabella non può contenere più JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella. Il numero di indici il cui schema può essere memorizzato nella cache viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella. Il numero di tabelle il cui schema può essere memorizzato nella cache viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea. Le risorse della tabella temporanea vengono <a href="gg294044(v=exchg.10).md">configurate usando JetSetSystemParameter</a> <a href="gg294140(v=exchg.10).md">con JET_paramMaxTemporaryTables</a>.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, verrà restituito un cursore aperto nella tabella temporanea appena creata. Lo stato del database temporaneo verrà preparato per contenere la nuova tabella temporanea. Lo stato di tutti i database comuni in uso dal motore di database rimarrà invariato.

In caso di errore, la tabella temporanea non verrà creata e non verrà restituito un cursore. Lo stato del database temporaneo può essere modificato. Lo stato di tutti i database comuni in uso dal motore di database rimarrà invariato.

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
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[Errori del motore Archiviazione estendibile](./extensible-storage-engine-errors.md)  
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
