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
ms.openlocfilehash: a1005f9804e0ccf9c4aa5080b3985906471b1386
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988914"
---
# <a name="jetopentemptable3-function"></a>Funzione JetOpenTempTable3


_**Si applica a:** Windows | Windows Server_

## <a name="jetopentemptable3-function"></a>Funzione JetOpenTempTable3

La **funzione JetOpenTempTable3** crea una tabella temporanea con un singolo indice che può essere usato per archiviare e recuperare record esattamente come una tabella ordinaria creata usando [JetCreateTableColumnIndex.](./jetcreatetablecolumnindex-function.md) Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle normali a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire rapidamente la rimozione dei duplicati sui set di record quando vi si accede in modo puramente sequenziale.

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

Esistono limitazioni importanti per le opzioni di definizione delle colonne che possono essere usate con una tabella temporanea. Per altre informazioni, vedere la sezione Osservazioni.

Oltre alle normali opzioni di definizione delle colonne, è possibile specificare zero o più delle opzioni seguenti che sono rilevanti solo nel contesto di una tabella temporanea.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>Questa opzione indica che l'ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente. Se questa opzione viene specificata senza JET_bitColumnTTKey, questa opzione viene ignorata.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Questa opzione indica che la colonna sarà una colonna chiave per la tabella temporanea.</p><p>L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea. La prima definizione di colonna nella matrice con questo set di opzioni sarà la colonna chiave più significativa e così via. Se vengono richieste più colonne chiave di quelle supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</p> | 



*ccolumn*

Vedere *prgcolumndef.*

*pidxunicode*

ID delle impostazioni locali e flag di normalizzazione che verranno usati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.

Quando questo parametro non è presente, verrà utilizzato l'identificatore LCID predefinito per confrontare le colonne chiave Unicode nella tabella temporanea. L'LCID predefinito è la lingua inglese (Stati Uniti).

Quando questo parametro non è presente, verranno usati i flag di normalizzazione predefiniti per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più degli elementi seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Questa opzione richiede che qualsiasi tentativo di inserire un record con la stessa chiave di indice di un record inserito in precedenza avrà immediatamente esito negativo con JET_errKeyDuplicate. Se questa opzione non è richiesta, un duplicato può essere rilevato immediatamente e non riuscire o essere rimosso automaticamente in un secondo momento a seconda della strategia scelta dal motore di database per implementare la tabella temporanea in base alla funzionalità richiesta.</p><p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Questa opzione forza la gestione tabelle temporanee ad abbandonare qualsiasi tentativo di scegliere una strategia intelligente per la gestione della tabella temporanea che comporta prestazioni migliorate.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>Questa opzione richiede che la tabella temporanea sia creata solo se il gestore di tabelle temporanee può usare l'implementazione ottimizzata per i risultati intermedi delle query. Se una caratteristica della tabella temporanea impedirebbe l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</p><p>Un effetto collaterale di questa opzione è consentire alla tabella temporanea di contenere record con chiavi di indice duplicate. Vedere JET_bitTTUnique per altre informazioni.</p><p>Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</p> | 
| <p>JET_bitTTIndexed</p> | <p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di <a href="gg294103(v=exchg.10).md">JetSeek</a> per la ricerca di record in base alla chiave di indice.</p><p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p> | 
| <p>JET_bitTTUnique</p> | <p>Questa opzione richiede che i record con chiavi di indice duplicate siano rimossi dal set finale di record nella tabella temporanea.</p><p>Prima di Windows Server 2003, il motore di database presupponeva sempre che questa opzione fosse attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci. A Windows Server 2003, è ora possibile creare una tabella temporanea che NON rimuove i duplicati quando viene specificata anche l'opzione JET_bitTTForwardOnly.</p><p>Non è possibile sapere quale duplicato verrà vinto e quali duplicati verranno eliminati in generale. Tuttavia, quando viene JET_bitTTErrorOnDuplicateInsertion è richiesta l'opzione , il primo record con una determinata chiave di indice da inserire nella tabella temporanea avrà sempre la possibilità di ottenere il controllo.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire la successiva modifica dei record inseriti in precedenza. Se questa funzionalità non è necessaria, è meglio non richiederla.</p><p>Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi dei record in ordine arbitrario e in direzione tramite <a href="gg294117(v=exchg.10).md">JetMove.</a></p><p>Se questa funzionalità non è necessaria, è meglio non richiederla. Se questa funzionalità non è richiesta, gestione tabelle temporanee potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporta un miglioramento delle prestazioni.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Questa opzione richiede che i valori delle colonne chiave NULL si sordinamento più vicino alla fine dell'indice rispetto ai valori di colonna chiave non NULL.</p> | 
| <p>JET_bitTTIntrinsicLVsOnly</p> | <p>Richiede di consentire solo valori long intrinseci.</p><p><strong>Windows 7:</strong> <strong>JET_bitTTIntrinsicLVsOnly</strong> è stato introdotto in Windows 7.</p> | 



*ptableid*

Buffer di output che riceverà il nuovo cursore aperto nella tabella temporanea appena creata.

*prgcolumnid*

Buffer di output che riceverà la matrice di ID di colonna generati durante la creazione della tabella temporanea.

Gli ID di colonna in questa matrice corrisponderanno esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni di questo buffer devono corrispondere alle dimensioni della matrice di input.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>JetOpenTempTable3</strong> non è riuscito perché JET_bitTTForwardOnly è stato specificato e non è stato possibile creare la tabella temporanea come specificato usando l'ottimizzazione forward-only. Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Impossibile creare l'indice perché è stata specificata una definizione di indice non valida. <strong>JetOpenTempTable3</strong> restituirà questo errore quando:</p><ul><li><p>Vengono specificate le impostazioni locali indipendenti dalla lingua.</p></li><li><p>È stato specificato un set non valido di flag di normalizzazione.</p></li></ul><p>Questo errore verrà restituito solo da Windows 2000.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Il <strong>membro cp</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida. Gli unici valori validi per le colonne di testo sono Inglese (1252) e Unicode (1200). Il valore 0 indica che verrà usato il valore predefinito (inglese, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Il <strong>membro coltyp</strong> della <a href="gg294130(v=exchg.10).md">struttura JET_COLUMNDEF</a> non è stato impostato su un tipo di colonna valido.</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>Impossibile creare l'indice perché è stato effettuato un tentativo di usare un ID impostazioni locali non valido. L'ID delle impostazioni locali potrebbe non essere completamente valido o il language pack potrebbe non essere installato.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>Impossibile creare l'indice perché è stato effettuato un tentativo di usare un set non valido di flag di normalizzazione. Questo errore verrà restituito solo da Windows XP e versioni successive. In Windows 2000, i flag di normalizzazione non validi JET_errIndexInvalidDef invece.</p> | 
| <p>JET_errInvalidSesid</p> | <p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa. Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in modo ottimale.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errOutOfCursors</p> | <p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore. Le risorse cursore vengono <a href="gg294044(v=exchg.10).md">configurate tramite JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con JET_paramMaxCursors</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per completarla.</p><p><strong>JetOpenTempTable3</strong> può restituire JET_errOutOfMemory se lo spazio indirizzi del processo host diventa troppo frammentato. Il gestore tabelle temporaneo alloca sempre un blocco di 1 MB di spazio indirizzi per ogni tabella temporanea creata indipendentemente dalla quantità di dati da archiviare.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTooManyColumns</p> | <p>È stato effettuato un tentativo di aggiungere troppe colonne alla tabella. Una tabella non può avere più JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella. Il numero di indici il cui schema può essere memorizzato nella cache viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269201(v=exchg.10).md">con</a>JET_paramMaxOpenTables .</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella. Il numero di tabelle il cui schema può essere memorizzato nella cache viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p> | 
| <p>JET_errTooManySorts</p> | <p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea. Le risorse tabella temporanea vengono configurate <a href="gg294044(v=exchg.10).md">usando JetSetSystemParameter</a> <a href="gg294140(v=exchg.10).md">con JET_paramMaxTemporaryTables</a>.</p> | 



In caso di esito positivo, verrà restituito un cursore aperto nella tabella temporanea appena creata. Lo stato del database temporaneo verrà preparato per contenere la nuova tabella temporanea. Lo stato di tutti i database comuni in uso dal motore di database rimarrà invariato.

In caso di errore, la tabella temporanea non verrà creata e non verrà restituito un cursore. Lo stato del database temporaneo può essere modificato. Lo stato di tutti i database comuni in uso dal motore di database rimarrà invariato.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



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
