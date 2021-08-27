---
description: Altre informazioni sulla funzione JetOpenTemporaryTable
title: Funzione JetOpenTemporaryTable
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
ms.openlocfilehash: a67a26a396f2910dd22fea351cc3d9b8a32a1c49
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983364"
---
# <a name="jetopentemporarytable-function"></a>Funzione JetOpenTemporaryTable


_**Si applica a:** Windows | Windows Server_

## <a name="jetopentemporarytable-function"></a>Funzione JetOpenTemporaryTable

La **funzione JetOpenTemporaryTable** crea una tabella volatile con un singolo indice che può essere usata per archiviare e recuperare record, proprio come una normale tabella creata tramite [JetCreateTableColumnIndex.](./jetcreatetablecolumnindex-function.md)

**Windows Vista:****JetOpenTemporaryTable** è stato introdotto in Windows Vista.  

Le tabelle temporanee sono più veloci delle tabelle ordinarie a causa della loro natura volatile. Possono ordinare ed eseguire rapidamente la rimozione dei duplicati nei set di record quando vi si accede in modo puramente sequenziale.

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione che verrà usata per questa chiamata.

*popentemporarytable*

Puntatore a una [struttura JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) che contiene la descrizione della tabella temporanea da creare in base all'input. Dopo una chiamata riuscita, la struttura contiene l'handle per le identificazioni di tabella e colonna temporanee.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p><p><strong>JetOpenTemporaryTable</strong> può restituire JET_errOutOfMemory se lo spazio indirizzi del processo host diventa troppo frammentato. Il gestore tabelle temporaneo alloca un blocco di 1 MB di spazio indirizzi per ogni tabella temporanea creata indipendentemente dalla quantità di dati archiviati.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</p><p>Questo errore viene restituito <strong>da JetOpenTemporaryTable</strong> nelle condizioni seguenti:</p><ul><li><p>Il <strong>membro cbStruct</strong> della <a href="gg269206(v=exchg.10).md">struttura JET_OPENTEMPORARYTABLE</a> non corrisponde a una versione di questa struttura supportata da tale versione del motore di database</p></li><li><p>Il <strong>membro cbKeyMost</strong> della struttura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> è minore di JET_cbKeyMostMin.</p></li><li><p>Il <strong>membro cbKeyMost</strong> della <a href="gg269206(v=exchg.10).md">struttura JET_OPENTEMPORARYTABLE</a> è maggiore del valore più grande supportato per le dimensioni della pagina del database per l'istanza (JET_paramDatabasePageSize). Per altre JET_paramKeyMost, vedere il parametro JET_paramKeyMost nell'elenco <a href="gg269241(v=exchg.10).md">dei parametri</a> in informazioni.</p></li><li><p>Il membro cbVarSegMac della <a href="gg269206(v=exchg.10).md">struttura JET_OPENTEMPORARYTABLE</a> è maggiore del membro <strong>cbKeyMost.</strong></p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidSesid</p> | <p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</p><p><strong>Nota:</strong>  Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in modo ottimale.</p> | 
| <p>JET_errOutOfCursors</p> | <p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore. Le risorse cursore vengono <a href="gg294044(v=exchg.10).md">configurate tramite JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxCursors</a>.</p> | 
| <p>JET_errTooManySorts</p> | <p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea. Le risorse tabella temporanea vengono configurate <a href="gg294044(v=exchg.10).md">usando JetSetSystemParameter</a> <a href="gg294140(v=exchg.10).md">con JET_paramMaxTemporaryTables</a>.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>JetOpenTemporaryTable</strong> non riuscito perché JET_bitTTForwardOnly è stato specificato e non è stato possibile creare la tabella temporanea specificata usando l'ottimizzazione forward-only.</p><p><strong>Windows Server 2003:</strong>  Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</p> | 
| <p>JET_errTooManyColumns</p> | <p>È stato effettuato un tentativo di aggiungere troppe colonne alla tabella. Una tabella non può avere più JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella. Per configurare il numero di tabelle con schemi che possono essere memorizzati nella cache, usare <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con</a>JET_paramMaxOpenTables .</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Il <strong>membro cp</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono Inglese (1252) e Unicode (1200). Il valore 0 indica che verrà usato il valore predefinito (inglese, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Il <strong>membro coltyp</strong> dell'JET_COLUMNDEF non è stato impostato su un tipo di colonna valido. <a href="gg294130(v=exchg.10).md"></a></p> | 
| <p>JET_errInvalidLanguageId</p> | <p>Impossibile creare l'indice perché è stato effettuato un tentativo di usare un ID impostazioni locali non valido. L'ID delle impostazioni locali potrebbe non essere completamente valido o il language pack potrebbe non essere installato.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>Impossibile creare l'indice perché è stato effettuato un tentativo di usare un set non valido di flag di normalizzazione.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p><p><strong>Windows 2000:</strong>  In Windows 2000, i flag di normalizzazione non validi JET_errIndexInvalidDef.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Impossibile creare l'indice perché è stata specificata una definizione di indice non valida. <strong>JetOpenTemporaryTable</strong> restituirà questo errore nelle condizioni seguenti:</p><ul><li><p>Vengono specificate le impostazioni locali indipendenti dalla lingua.</p></li><li><p>È stato specificato un set non valido di flag di normalizzazione.</p></li></ul><p><strong>Windows 2000:</strong>  Questo errore verrà restituito solo da Windows 2000.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella. Per configurare il numero di indici con schemi che possono essere memorizzati nella cache, usare <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con</a>JET_paramMaxOpenTables .</p> | 



In caso di esito positivo, verrà restituito un cursore aperto nella tabella temporanea appena creata. Lo stato del database temporaneo verrà preparato per contenere la nuova tabella temporanea. Lo stato di tutti i database comuni in uso dal motore di database rimarrà invariato.

In caso di errore, la tabella temporanea non verrà creata e non verrà restituito un cursore. Lo stato del database temporaneo può essere modificato. Lo stato di tutti i database comuni in uso dal motore di database rimarrà invariato.

#### <a name="remarks"></a>Commenti

Le tabelle temporanee non supportano il complemento completo delle opzioni di definizione delle colonne normalmente supportate dal motore di database. Sono infatti supportati solo JET_bitColumnFixed e JET_bitColumnTagged. Ciò significa che non è possibile creare un incremento automatico, una versione o una colonna multivalore in una tabella temporanea. Infine, le colonne di aggiornamento del deposito non sono supportate perché possono essere usate solo da una sessione alla volta. Se viene richiesta una di queste opzioni, queste verranno ignorate.

Le tabelle temporanee non supportano i valori predefiniti. Se viene specificata una definizione di colonna che contiene una specifica del valore predefinito, tale specifica verrà ignorata.

Le tabelle temporanee vengono restituite al chiamante in seguito a molte funzioni ESE diverse. Ad esempio, [JetGetIndexInfo](./jetgetindexinfo-function.md) con JET_IdxInfo set di opzioni restituirà una tabella temporanea contenente un elenco di tutte le colonne chiave in un determinato indice. Le tabelle temporanee seguono le stesse regole del ciclo di vita delle normali tabelle temporanee, come descritto qui.

Le tabelle temporanee vengono usate anche internamente dal motore di database per molte attività. La più importante di queste attività è la creazione di un indice su una tabella esistente. Verrà usata una tabella temporanea per ordinare le chiavi di indice usate per costruire tale indice.

Tutte le tabelle temporanee vengono archiviate nel database temporaneo. Il database temporaneo è un file di database speciale che viene mantenuto durante la durata di un'istanza ESE e viene eliminato quando tale istanza viene arrestata o riavviata. Il percorso del database temporaneo può essere configurato usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramTempPath](./temporary-database-parameters.md). Il posizionamento del database temporaneo su disco rispetto ai file di log delle transazioni e ai file di database può essere importante se l'applicazione usa spesso tabelle temporanee o crea spesso indici.

Il ciclo di vita di una tabella temporanea è associato ai cursori che vi fanno riferimento. Se tutti i cursori che fanno riferimento a una tabella temporanea vengono chiusi in modo implicito o esplicito, la tabella temporanea verrà eliminata. Se viene creata una tabella temporanea all'interno di una transazione e successivamente ne viene eseguito il rollback, la tabella temporanea verrà eliminata perché tutti i cursori che vi fanno riferimento in questo momento verranno chiusi in modo implicito. I nuovi cursori possono fare riferimento a una tabella temporanea solo tramite l'uso di [JetDupCursor](./jetdupcursor-function.md). In questo caso, i nuovi cursori verranno posizionati sulla prima voce di indice della tabella temporanea. [JetDupCursor](./jetdupcursor-function.md) funzionerà solo durante determinate fasi di utilizzo per la tabella temporanea. Per altre informazioni, vedere le osservazioni relative alle funzionalità temporanee del cursore di tabella. Non è possibile fare riferimento a una tabella temporanea da più di una sessione alla volta.

**Attenzione**  Esiste un problema importante in [JetDupCursor](./jetdupcursor-function.md) che interessa le tabelle temporanee. Se si tenta di duplicare una tabella temporanea in modalità forward-only, il cursore risultante non verrà creato correttamente e non funziona correttamente. È comunque possibile duplicare un cursore su una tabella temporanea materializzata.

Gestione tabelle temporanee può implementare una tabella temporanea in tre modi. Il primo metodo è mantenere una tabella in memoria. Questa strategia è la più veloce, ma può essere usata solo per tabelle temporanee di piccole dimensioni, semplici. Il secondo metodo è creare un ordinamento basato su disco che può essere guidato usando un iteratore forward-only. Questa strategia può essere usata solo in determinate circostanze ed è il modo più rapido per ordinare e rimuovere i duplicati da un set di dati di grandi dimensioni. Il terzo metodo è creare un albero B+ nel database temporaneo per contenere la tabella temporanea. Questa strategia è la più lenta, ma la più versatile, e viene definita tabella temporanea materializzata. Queste strategie possono essere usate in combinazione per ottenere la funzionalità richiesta dalla tabella temporanea.

Quando la tabella temporanea non viene materializzata, viene usata principalmente in due fasi principali. La prima fase è la fase di inserimento in cui la tabella viene popolata con il relativo set di dati iniziale. Durante questa fase è consentito solo l'inserimento di dati. Questa fase termina quando viene effettuato un tentativo di spostare il cursore usando [JetMove](./jetmove-function.md) [o JetSeek](./jetseek-function.md). La seconda fase è la fase di estrazione dei dati. Durante questa fase, i dati archiviati nella tabella temporanea possono essere estratti in base alle funzionalità richieste al momento della creazione della tabella temporanea.

**Funzionalità del cursore tabella temporanea**

Quando la tabella temporanea viene materializzata, il cursore ha le funzionalità seguenti, ma potrebbe essere ulteriormente limitato dalle opzioni richieste:

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

Quando la tabella temporanea non viene materializzata e si trova nella fase di inserimento, il cursore dispone delle funzionalità seguenti, ma potrebbe essere ulteriormente limitato dalle opzioni richieste:

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)
    
    **Nota:**  Causa la transizione alla fase di estrazione.

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)
    
    **Nota:**  Causa la transizione alla fase di estrazione.

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


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



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
[Parametri in informazioni](./informational-parameters.md)  
[Parametri di database temporanei](./temporary-database-parameters.md)
