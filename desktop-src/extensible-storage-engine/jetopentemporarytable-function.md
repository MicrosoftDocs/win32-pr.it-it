---
description: 'Altre informazioni su: funzione JetOpenTemporaryTable'
title: JetOpenTemporaryTable (funzione)
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315620"
---
# <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable (funzione)

La funzione **JetOpenTemporaryTable** crea una tabella volatile con un solo indice che può essere usato per archiviare e recuperare record, proprio come una tabella ordinaria creata tramite [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).

**Windows Vista:**  **JetOpenTemporaryTable** è stato introdotto in Windows Vista.

Le tabelle temporanee sono più veloci delle tabelle ordinarie a causa della loro natura volatile. Possono ordinare ed eseguire rapidamente la rimozione dei duplicati nei set di record quando sono accessibili in modo puramente sequenziale.

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione che verrà utilizzata per questa chiamata.

*popentemporarytable*

Puntatore a una struttura [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) contenente la descrizione della tabella temporanea da creare in input. Dopo una chiamata con esito positivo, la struttura contiene l'handle per gli identificatori di tabella e colonna temporanei.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</p>
<p><strong>JetOpenTemporaryTable</strong> può restituire JET_errOutOfMemory se lo spazio degli indirizzi del processo host diventa troppo frammentato. Il gestore tabelle temporanee allocherà un blocco di spazio degli indirizzi di 1 MB per ogni tabella temporanea creata indipendentemente dalla quantità di dati archiviati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri specificati contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</p>
<p>Questo errore viene restituito da <strong>JetOpenTemporaryTable</strong> nelle condizioni seguenti:</p>
<ul>
<li><p>Il membro <strong>cbStruct</strong> della struttura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> non corrisponde a una versione di questa struttura supportata da tale versione del motore di database</p></li>
<li><p>Il membro <strong>cbKeyMost</strong> della struttura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> è minore di JET_cbKeyMostMin.</p></li>
<li><p>Il membro <strong>cbKeyMost</strong> della struttura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> è più grande del valore supportato più grande per le dimensioni della pagina del database per l'istanza (JET_paramDatabasePageSize). Per ulteriori informazioni, vedere il parametro JET_paramKeyMost nell'elenco dei <a href="gg269241(v=exchg.10).md">parametri informativi</a> .</p></li>
<li><p>Il membro cbVarSegMac della struttura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> è più grande del membro <strong>cbKeyMost</strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza di associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</p>
<p><strong>Nota</strong>  Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in base al massimo sforzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore. Le risorse del cursore vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea. Le risorse della tabella temporanea vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p><strong>JetOpenTemporaryTable</strong> non riuscito perché è stato specificato JET_bitTTForwardOnly e non è stato possibile creare la tabella temporanea specificata con l'ottimizzazione di sola trasmissione.</p>
<p><strong>Windows Server 2003:</strong>  Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella. Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella. Per configurare il numero di tabelle che contengono schemi che possono essere memorizzati nella cache, utilizzare <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Il membro <strong>CP</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200). Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Il membro <strong>coltyp</strong> del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su un tipo di colonna valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un ID delle impostazioni locali non valido. È possibile che l'ID delle impostazioni locali sia completamente non valido o che il Language Pack associato non sia installato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un set di flag di normalizzazione non valido.</p>
<p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p>
<p><strong>Windows 2000:</strong>  In Windows 2000, i flag di normalizzazione non validi determineranno JET_errIndexInvalidDef.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Impossibile creare l'indice perché è stata specificata una definizione di indice non valida. <strong>JetOpenTemporaryTable</strong> restituirà questo errore nelle condizioni seguenti:</p>
<ul>
<li><p>Le impostazioni locali indipendenti dalla lingua sono specificate.</p></li>
<li><p>È stato specificato un set di flag di normalizzazione non valido.</p></li>
</ul>
<p><strong>Windows 2000:</strong>  Questo errore verrà restituito solo da Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella. Per configurare il numero di indici con schemi che possono essere memorizzati nella cache, utilizzare <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, verrà restituito un cursore aperto nella tabella temporanea appena creata. Lo stato del database temporaneo sarà pronto per contenere la nuova tabella temporanea. Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.

In caso di errore, la tabella temporanea non verrà creata e non verrà restituito un cursore. Lo stato del database temporaneo può essere modificato. Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.

#### <a name="remarks"></a>Commenti

Le tabelle temporanee non supportano il complemento completo delle opzioni di definizione di colonna normalmente supportate dal motore di database. In realtà, sono supportati solo JET_bitColumnFixed e JET_bitColumnTagged. Ciò significa che non è possibile creare un incremento automatico, una versione o una colonna multivalore in una tabella temporanea. Infine, le colonne di aggiornamento del deposito a garanzia non sono supportate perché possono essere utilizzate solo da una sessione alla volta. Se viene richiesta una qualsiasi di queste opzioni, queste verranno ignorate.

Le tabelle temporanee non supportano i valori predefiniti. Se viene fornita una definizione di colonna contenente una specifica del valore predefinito, tale specifica verrà ignorata.

Le tabelle temporanee vengono restituite al chiamante in seguito a numerose funzioni ESE diverse. Ad esempio, [JetGetIndexInfo](./jetgetindexinfo-function.md) con il set di opzioni JET_IdxInfo restituirà una tabella temporanea contenente un elenco di tutte le colonne chiave di un indice specificato. Le tabelle temporanee seguono le stesse regole del ciclo di vita delle tabelle temporanee comuni, come descritto qui.

Le tabelle temporanee vengono inoltre utilizzate internamente dal motore di database per molte attività. La più importante di queste attività è la creazione di un indice su una tabella esistente. Una tabella temporanea verrà utilizzata per ordinare le chiavi di indice utilizzate per costruire tale indice.

Tutte le tabelle temporanee vengono archiviate nel database temporaneo. Il database temporaneo è un file di database speciale mantenuto durante la durata di un'istanza ESE e viene eliminato quando l'istanza viene arrestata o riavviata. Il percorso del database temporaneo può essere configurato tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramTempPath](./temporary-database-parameters.md). La posizione del database temporaneo su disco rispetto ai file di log delle transazioni e dei file di database può essere importante se l'applicazione usa in modo intensivo le tabelle temporanee o crea gli indici di frequente.

Il ciclo di vita di una tabella temporanea è associato ai cursori che vi fanno riferimento. Se tutti i cursori che fanno riferimento a una tabella temporanea sono chiusi, in modo implicito o esplicito, la tabella temporanea verrà eliminata. Se una tabella temporanea viene creata all'interno di una transazione e successivamente viene eseguito il rollback della transazione, la tabella temporanea verrà eliminata perché i cursori che vi fanno riferimento in questo momento verranno chiusi in modo implicito. I nuovi cursori possono fare riferimento a una tabella temporanea solo tramite l'uso di [JetDupCursor](./jetdupcursor-function.md). In questo caso, i nuovi cursori verranno posizionati sulla prima voce di indice della tabella temporanea. [JetDupCursor](./jetdupcursor-function.md) funzionerà solo durante determinate fasi di utilizzo della tabella temporanea. Per ulteriori informazioni, vedere le osservazioni relative alle funzionalità del cursore della tabella temporanea. Non è possibile fare riferimento a una tabella temporanea da più di una sessione alla volta.

**Attenzione**  Si è verificato un problema importante in [JetDupCursor](./jetdupcursor-function.md) che influiscono sulle tabelle temporanee. Se viene effettuato un tentativo di duplicare una tabella temporanea in modalità di sola trasmissione, il cursore risultante non verrà creato correttamente e non funzionerà correttamente. È comunque possibile duplicare un cursore su una tabella temporanea materializzata.

Il gestore tabelle temporaneo può implementare una tabella temporanea in tre modi. Il primo metodo consiste nel mantenere una tabella in memoria. Questa strategia è la più veloce, ma può essere usata solo per le tabelle temporanee di piccole dimensioni. Il secondo metodo consiste nel creare un ordinamento basato su disco che può essere guidato utilizzando un iteratore di tipo "solo". Questa strategia può essere utilizzata solo in determinate circostanze ed è il modo più rapido per ordinare e rimuovere i duplicati da un set di dati di grandi dimensioni. Il terzo metodo consiste nel creare un albero B + nel database temporaneo che contenga la tabella temporanea. Questa strategia è la più lenta, ma la più versatile, ed è definita tabella temporanea materializzata. Queste strategie possono essere usate in combinazione per ottenere in definitiva la funzionalità richiesta della tabella temporanea.

Quando la tabella temporanea non viene materializzata, viene utilizzata principalmente in due fasi principali. La prima fase è la fase di inserimento in cui la tabella viene popolata con il set di dati iniziale. Durante questa fase, è consentito solo l'inserimento di dati. Questa fase termina quando viene effettuato un tentativo di spostare il cursore utilizzando [JetMove](./jetmove-function.md) o [JetSeek](./jetseek-function.md). La seconda fase è la fase di estrazione dei dati. Durante questa fase, i dati archiviati nella tabella temporanea possono essere estratti in base alle funzionalità richieste durante la creazione della tabella temporanea.

**Funzionalità del cursore tabella temporanea**

Quando la tabella temporanea viene materializzata, il cursore presenta le funzionalità seguenti, ma potrebbe essere ulteriormente limitato dalle opzioni richieste:

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

Quando la tabella temporanea non viene materializzata e si trova nella fase di inserimento, il cursore presenta le funzionalità seguenti, ma potrebbe essere ulteriormente limitato dalle opzioni richieste:

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

Quando la tabella temporanea non viene materializzata e si trova nella fase di estrazione, il cursore presenta le funzionalità seguenti, ma può essere ulteriormente limitato dalle opzioni richieste:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)
    
    **Nota**  Se viene effettuato un tentativo di duplicare una tabella temporanea in modalità di sola trasmissione, il cursore risultante non verrà creato correttamente e non funzionerà correttamente. È comunque possibile duplicare un cursore su una tabella temporanea materializzata.

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
<td><p>Richiede Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008.</p></td>
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
[JET_SESID](./jet-sesid.md)  
[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri informativi](./informational-parameters.md)  
[Parametri di database temporanei](./temporary-database-parameters.md)
