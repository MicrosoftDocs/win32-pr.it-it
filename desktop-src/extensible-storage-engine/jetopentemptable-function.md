---
description: Altre informazioni sulla funzione JetOpenTempTable
title: Funzione JetOpenTempTable
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 522c64d946ab37d644ba6f146001bb9f6dd12489804539987b7098bb1a30189a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118072307"
---
# <a name="jetopentemptable-function"></a>Funzione JetOpenTempTable


_**Si applica a:** Windows | Windows Server_

## <a name="jetopentemptable-function"></a>Funzione JetOpenTempTable

La **funzione JetOpenTempTable** crea una tabella temporanea con un singolo indice. Una tabella temporanea archivia e recupera i record esattamente come una normale tabella creata usando [JetCreateTableColumnIndex.](./jetcreatetablecolumnindex-function.md) Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle normali a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire rapidamente la rimozione dei duplicati sui set di record quando vi si accede in modo puramente sequenziale.

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare.

*prgcolumndef*

Definizioni di colonna per le colonne create nella tabella temporanea.

**Esistono**   limitazioni importanti per le opzioni di definizione delle colonne usate con una tabella temporanea. Per altre informazioni, vedere la sezione Osservazioni.

Oltre alle normali opzioni di definizione delle colonne, è possibile specificare zero o più delle opzioni seguenti che sono rilevanti solo nel contesto di una tabella temporanea.

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
<td><p>L'ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente. Se questa opzione viene specificata senza JET_bitColumnTTKey, questa opzione viene ignorata.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>La colonna sarà una colonna chiave per la tabella temporanea.</p>
<p>L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea. La prima definizione di colonna nella matrice con questa opzione impostata sarà la colonna chiave più significativa e così via. Se vengono richieste più colonne chiave di quelle supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</p></td>
</tr>
</tbody>
</table>


*ccolumn*

Vedere *prgcolumndef.*

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
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Qualsiasi tentativo di inserire un record con la stessa chiave di indice di un record inserito in precedenza avrà immediatamente esito negativo con JET_errKeyDuplicate. Se questa opzione non è richiesta, un duplicato viene rilevato immediatamente e ha esito negativo o viene rimosso automaticamente in un secondo momento, a seconda della strategia scelta dal motore di database per implementare la tabella temporanea, in base alla funzionalità richiesta.</p>
<p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Forza la gestione tabelle temporanee ad abbandonare la ricerca per la strategia migliore da usare per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>La tabella temporanea viene creata solo se la gestione tabelle temporanee può utilizzare l'implementazione ottimizzata per i risultati intermedi delle query. Se una caratteristica della tabella temporanea impedirebbe l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</p>
<p>Un effetto collaterale di questa opzione è consentire alla tabella temporanea di contenere record con chiavi di indice duplicate. Vedere JET_bitTTUnique per altre informazioni.</p>
<p>Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTIndexed</p></td>
<td><p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di <a href="gg294103(v=exchg.10).md">JetSeek</a> per la ricerca di record in base alla chiave di indice.</p>
<p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUnique</p></td>
<td><p>Richiede che i record con chiavi di indice duplicate siano rimossi dal set finale di record nella tabella temporanea.</p>
<p>Prima di Windows Server 2003, il motore di database presupponeva sempre che questa opzione fosse attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci. A Windows Server 2003, è ora possibile creare una tabella temporanea che non rimuove i duplicati quando viene specificata anche l'opzione JET_bitTTForwardOnly.</p>
<p>Non è possibile sapere quale duplicato avrà esito positivo e quali duplicati verranno eliminati, in generale. Tuttavia, quando viene richiesta JET_bitTTErrorOnDuplicateInsertion'opzione , il primo record con una determinata chiave di indice da inserire nella tabella temporanea avrà sempre esito positivo.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Richiede che la tabella temporanea sia sufficientemente flessibile da consentire la successiva modifica dei record inseriti in precedenza. Se questa funzionalità non è necessaria, è meglio non richiederla.</p>
<p>Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi dei record in ordine arbitrario e in direzione tramite <a href="gg294117(v=exchg.10).md">JetMove.</a></p>
<p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Richiede che i valori delle colonne chiave NULL si sordinamento più vicino alla fine dell'indice rispetto ai valori di colonna chiave non NULL.</p>
<p></p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTIntrinsicLVsOnly</p></td>
<td><p>Richiede di consentire solo valori long intrinseci.</p>
<p><strong>Windows 7:</strong> <strong>JET_bitTTIntrinsicLVsOnly</strong> è stato introdotto in Windows 7.</p></td>
</tr>
</tbody>
</table>


*ptableid*

Buffer di output che riceve il nuovo cursore aperto nella tabella temporanea appena creata.

*prgcolumnid*

Buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.

Gli ID di colonna in questa matrice corrisponderanno esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni di questo buffer devono corrispondere alle dimensioni della matrice di input.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p><strong>JetOpenTempTable</strong> non è riuscito perché JET_bitTTForwardOnly è stato specificato e non è stato possibile creare la tabella temporanea specificata usando l'ottimizzazione forward-only. Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Impossibile creare l'indice perché è stata specificata una definizione di indice non valida.</p>
<p><strong>JetOpenTempTable</strong> restituirà questo errore quando:</p>
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
<td><p>Il campo cp del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono Inglese (1252) e Unicode (1200). Il valore 0 indica che verrà usato il valore predefinito (inglese, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Il <em>campo coltyp</em> del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su un tipo di colonna valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Impossibile creare l'indice perché è stato effettuato un tentativo di usare un ID impostazioni locali non valido. L'ID delle impostazioni locali potrebbe non essere completamente valido o il language pack potrebbe non essere installato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Impossibile creare l'indice perché è stato effettuato un tentativo di usare un set non valido di flag di normalizzazione. Questo errore verrà restituito solo da Windows XP e versioni successive. In Windows 2000, i flag di normalizzazione non validi JET_errIndexInvalidDef invece.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</p>
<p><strong>Nota:</strong>  Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in modo ottimale.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore. Le risorse cursore vengono <a href="gg294044(v=exchg.10).md">configurate tramite JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxCursors</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p>
<p><strong>JetOpenTempTable</strong> può restituire JET_errOutOfMemory se lo spazio indirizzi del processo host diventa troppo frammentato. Il gestore tabelle temporaneo alloca sempre un blocco di 1 MB di spazio indirizzi per ogni tabella temporanea creata indipendentemente dalla quantità di dati da archiviare.</p></td>
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
<td><p>È stato effettuato un tentativo di aggiungere troppe colonne alla tabella. Una tabella non può avere più di JET_ccolFixedMost fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella. Il numero di indici il cui schema può essere memorizzato nella cache viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con</a>JET_paramMaxOpenTables .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella. Il numero di tabelle il cui schema può essere memorizzato nella cache viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea. Le risorse tabella temporanea vengono configurate <a href="gg294044(v=exchg.10).md">tramite JetSetSystemParameter</a> <a href="gg294140(v=exchg.10).md">con JET_paramMaxTemporaryTables</a>.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, verrà restituito un cursore aperto nella tabella temporanea appena creata. Lo stato del database temporaneo verrà preparato per contenere la nuova tabella temporanea. Lo stato di tutti i database comuni in uso dal motore di database rimarrà invariato.

In caso di errore, la tabella temporanea non verrà creata e non verrà restituito un cursore. Lo stato del database temporaneo può essere modificato. Lo stato di tutti i database comuni in uso dal motore di database rimarrà invariato.

#### <a name="remarks"></a>Commenti

Le tabelle temporanee non supportano il complemento completo delle opzioni di definizione delle colonne normalmente supportate dal motore di database. Sono infatti supportati solo JET_bitColumnFixed e JET_bitColumnTagged supportati. Ciò significa che non è possibile creare un incremento automatico, una versione o una colonna multivalore in una tabella temporanea. Infine, le colonne di aggiornamento del deposito non sono supportate perché non sono utili in una tabella temporanea perché possono essere usate solo da una sessione alla volta. Se viene richiesta una di queste opzioni, verranno ignorate.

Le tabelle temporanee non supportano i valori predefiniti. Se viene specificata una definizione di colonna che contiene una specifica del valore predefinito, tale specifica verrà ignorata.

Le tabelle temporanee vengono restituite al chiamante in seguito a molte funzioni ESE diverse. Ad esempio, [JetGetIndexInfo](./jetgetindexinfo-function.md) con l'opzione JET_IdxInfo impostata nel *parametro InfoLevel* restituirà una tabella temporanea contenente un elenco di tutte le colonne chiave in un determinato indice. Le tabelle temporanee seguono le stesse regole del ciclo di vita delle normali tabelle temporanee, come descritto qui.

Le tabelle temporanee vengono usate anche internamente dal motore di database per molte attività. La più importante di queste attività è la creazione di un indice su una tabella esistente. Verrà usata una tabella temporanea per ordinare le chiavi di indice usate per costruire tale indice.

Tutte le tabelle temporanee vengono archiviate nel database temporaneo. Il database temporaneo è un file di database speciale che viene mantenuto durante la durata di un'istanza ESE e viene eliminato quando tale istanza viene arrestata o riavviata. Il percorso del database temporaneo può essere configurato usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) [con JET_paramTempPath](./temporary-database-parameters.md). Il posizionamento del database temporaneo su disco rispetto ai file di log delle transazioni e ai file di database può essere importante se l'applicazione usa spesso tabelle temporanee o crea spesso indici.

Il ciclo di vita di una tabella temporanea è associato ai cursori che vi fanno riferimento. Se tutti i cursori che fanno riferimento a una tabella temporanea vengono chiusi in modo implicito o esplicito, la tabella temporanea verrà eliminata. Se viene creata una tabella temporanea all'interno di una transazione e successivamente ne viene eseguito il rollback, la tabella temporanea verrà eliminata perché tutti i cursori che vi fanno riferimento in questo momento verranno chiusi in modo implicito. I nuovi cursori possono fare riferimento a una tabella temporanea solo tramite l'uso di [JetDupCursor](./jetdupcursor-function.md). In questo caso, i nuovi cursori verranno posizionati sulla prima voce di indice della tabella temporanea. [JetDupCursor](./jetdupcursor-function.md) funzionerà solo durante determinate fasi di utilizzo per la tabella temporanea. Per altre informazioni, vedere le osservazioni relative alle funzionalità temporanee del cursore di tabella. Non è possibile fare riferimento a una tabella temporanea da più di una sessione alla volta.

Esiste un problema importante in [JetDupCursor](./jetdupcursor-function.md) che interessa le tabelle temporanee. Se si tenta di duplicare una tabella temporanea in modalità forward-only, il cursore risultante non verrà creato correttamente e non funziona correttamente. È comunque possibile duplicare un cursore su una tabella temporanea materializzata.

Gestione tabelle temporanee può scegliere di implementare una tabella temporanea in tre modi. Il primo metodo è mantenere una tabella in memoria. Questa strategia è la più veloce, ma può essere usata solo per tabelle temporanee semplici e di piccole dimensioni. Il secondo metodo è creare un ordinamento basato su disco che può essere guidato usando un iteratore forward-only. Questa strategia può essere usata solo in determinate circostanze ed è il modo più rapido per ordinare e rimuovere i duplicati da un set di dati molto grande. Il terzo metodo è creare un albero B+ nel database temporaneo per contenere la tabella temporanea. Questa strategia è la più lenta, ma la più versatile, e viene definita tabella temporanea materializzata. Queste strategie possono essere usate in combinazione per ottenere la funzionalità richiesta dalla tabella temporanea.

Quando la tabella temporanea non viene materializzata, viene usata principalmente in due fasi principali. La prima fase è la fase di inserimento in cui la tabella viene popolata con il relativo set di dati iniziale. Durante questa fase è consentito solo l'inserimento di dati. Questa fase termina quando viene effettuato un tentativo di spostare il cursore usando [JetMove](./jetmove-function.md) [o JetSeek](./jetseek-function.md). La seconda fase è la fase di estrazione dei dati. Durante questa fase, i dati archiviati nella tabella temporanea possono essere estratti in base alle funzionalità richieste al momento della creazione della tabella temporanea.

**Funzionalità del cursore tabella temporanea**

Quando la tabella temporanea viene materializzata, il cursore ha le funzionalità seguenti, ma può essere ulteriormente limitato dalle opzioni richieste:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDelete](./jetdelete-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUpdate](./jetupdate-function.md)

Quando la tabella temporanea non viene materializzata e si trova nella fase di inserimento, il cursore dispone delle funzionalità seguenti, ma può essere ulteriormente limitato dalle opzioni richieste:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)
    
    **Nota**  Causa la transizione alla fase di estrazione.

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)
    
    **Nota**  Causa la transizione alla fase di estrazione.

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetUpdate](./jetupdate-function.md)

Quando la tabella temporanea non viene materializzata e si trova nella fase di estrazione, il cursore dispone delle funzionalità seguenti, ma può essere ulteriormente limitato dalle opzioni richieste:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)
    
    **Nota**  Se si tenta di duplicare una tabella temporanea in modalità forward-only, il cursore risultante non verrà creato correttamente e non funziona correttamente. È comunque possibile duplicare un cursore su una tabella temporanea materializzata.

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

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
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri del database temporaneo](./temporary-database-parameters.md)
