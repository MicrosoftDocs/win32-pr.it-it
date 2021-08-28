---
description: Altre informazioni sulla funzione JetSetColumn
title: Funzione JetSetColumn
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d37762166f079c7810a5ea28f2affe460d3bc08f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478277"
---
# <a name="jetsetcolumn-function"></a>Funzione JetSetColumn


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetcolumn-function"></a>Funzione JetSetColumn

La **funzione JetSetColumn** modifica un singolo valore di colonna in un record modificato da inserire o aggiornare il record corrente. Può sovrascrivere un valore esistente, aggiungere un nuovo valore a una sequenza di valori in una colonna multivalore, rimuovere un valore da una sequenza di valori in una colonna multivalore o aggiornare tutto o parte di un valore long, una colonna di tipo [JET_coltypLongText](./jet-coltyp.md) [o JET_coltypLongBinary](./jet-coltyp.md).

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*columnid*

Valore [JET_COLUMNID](./jet-columnid.md) della colonna da recuperare. In alternativa, è possibile specificare un valore *columnid* pari a 0 (zero). Quando *viene specificato columnid* 0 (zero), tutte le colonne con tag, di tipo sparse e multivalore vengono considerate come una singola colonna. Ciò facilita il recupero di tutte le colonne di tipo sparse presenti in un record.

*pvData*

Buffer di input contenente i dati da utilizzare per il valore della colonna.

*cbData*

Dimensione in byte del buffer di input.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più dei seguenti:


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitSetAppendLV</p> | <p>Questa opzione viene usata per aggiungere dati a una colonna di <a href="gg269213(v=exchg.10).md">tipo JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. Lo stesso comportamento può essere ottenuto determinando le dimensioni del valore long esistente e specificando <em>ibLongValue</em> in <em>psetinfo</em>. Tuttavia, è più semplice usare questo <em>grbit</em> poiché non è necessario conoscere le dimensioni del valore di colonna esistente.</p> | 
| <p>JET_bitSetOverwriteLV</p> | <p>Questa opzione viene usata per sostituire il valore long esistente con i nuovi dati forniti. Quando si usa questa opzione, è come se il valore long esistente fosse stato impostato su una lunghezza pari a 0 (zero) prima di impostare i nuovi dati.</p> | 
| <p>JET_bitSetRevertToDefaultValue</p> | <p>Questa opzione è applicabile solo alle colonne con tag, sparse o multivalore. Fa in modo che la colonna restituirà il valore predefinito della colonna nelle successive operazioni di recupero della colonna. Tutti i valori di colonna esistenti vengono rimossi.</p> | 
| <p>JET_bitSetSeparateLV</p> | <p>Questa opzione viene usata per forzare l'archiviazione separata di un valore long, colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> <a href="gg269213(v=exchg.10).md">o JET_coltypLongBinary</a>, rispetto al resto dei dati del record. Ciò si verifica normalmente quando le dimensioni del valore long ne impediscono l'archiviazione con i dati dei record rimanenti. Tuttavia, questa opzione può essere usata per forzare l'archiviazione separata del valore long. Si noti che i valori lunghi di quattro byte di dimensioni inferiori non possono essere forzati per essere separati. In questi casi, l'opzione viene ignorata.</p> | 
| <p>JET_bitSetSizeLV</p> | <p>Questa opzione viene usata per interpretare il buffer di input come numero intero di byte da impostare come lunghezza del valore long descritto da <em>columnid</em> specificato e, se specificato, il numero di sequenza in psetinfo- &gt; itagSequence. Se le dimensioni specificate sono maggiori del valore della colonna esistente, la colonna verrà estesa con 0. Se le dimensioni sono inferiori al valore della colonna esistente, il valore verrà troncato.</p> | 
| <p>JET_bitSetUniqueMultiValues</p> | <p>Questa opzione viene usata per imporre che tutti i valori in una colonna multivalore siano distinti. Questa opzione confronta i dati della colonna di origine, senza alcuna trasformazione, con altri valori di colonna esistenti e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, JET_bitSetAppendLV, JET_bitSetOverwriteLV e JET_bitSetSizeLV non possono essere fornite.</p> | 
| <p>JET_bitSetUniqueNormalizedMultiValues</p> | <p>Questa opzione viene usata per imporre che tutti i valori in una colonna multivalore siano distinti. Questa opzione confronta la trasformazione normalizzata della chiave dei dati della colonna con altri valori di colonna esistenti trasformati in modo simile e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, JET_bitSetAppendLV, JET_bitSetOverwriteLV e JET_bitSetSizeLV non possono essere fornite.</p> | 
| <p>JET_bitSetZeroLength</p> | <p>Questa opzione viene usata per impostare un valore su lunghezza zero. In genere, un valore di colonna viene impostato <strong>su NULL</strong> passando un valore cbMax pari a 0 (zero). Tuttavia, per alcuni tipi, ad esempio <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, un valore di colonna può avere una lunghezza pari a 0 (zero) anziché <strong>NULL</strong>e questa opzione viene usata per distinguere tra la lunghezza <strong>NULL</strong> e la lunghezza 0 (zero).</p><p><strong>Nota:</strong>  In generale, se la colonna è una colonna a lunghezza fissa, questo bit viene ignorato e la colonna è impostata su <strong>NULL.</strong> Tuttavia, se la colonna è una colonna con tag a lunghezza fissa, la lunghezza della colonna viene impostata su 0. Quando la colonna con tag a lunghezza fissa è impostata su 0, i tentativi di recuperare la colonna con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> avranno esito positivo, ma la lunghezza effettiva restituita nel <em>parametro cbActual</em> è 0.</p> | 
| <p>JET_bitSetIntrinsicLV</p> | <p>Questa opzione viene usata per archiviare l'intero valore long nel record.</p> | 
| <p>JET_bitSetCompressed</p> | <p>Questa opzione viene usata per tentare la compressione dei dati durante l'archiviazione dei dati.</p><p><strong>Windows 7:</strong>  JET_bitSetCompressed è stato introdotto in Windows 7.</p> | 
| <p>JET_bitSetUncompressed</p> | <p>Questa opzione non viene usata per tentare la compressione durante l'archiviazione dei dati.</p><p><strong>Windows 7:</strong>  JET_bitSetUnCompressed è stato introdotto in Windows 7.</p> | 



*psetinfo*

Puntatore ai parametri di input facoltativi che possono essere impostati per questa funzione usando la [JET_SETINFO](./jet-setinfo-structure.md) di dati.

Se *psetinfo* viene specificato come **NULL,** la funzione si comporta come se fossero stati dati *itagSequence* pari a 1 e *ibLongValue* pari a 0 (zero). In questo modo il set di colonne imposta il primo valore di una colonna multivalore e imposta dati lunghi a partire dall'offset 0 (zero).

Per questo parametro è possibile impostare le opzioni seguenti:


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>ibLongValue</p> | <p>Offset binario in un valore di colonna long in cui devono iniziare i dati del set.</p> | 
| <p>itagSequence</p> | <p>Numero di sequenza del valore di colonna multivalore desiderato da impostare. Se <em>itagSequence</em> è impostato su 0 (zero), il valore fornito deve essere aggiunto alla fine della sequenza di valori multivalore. Se il numero di sequenza specificato è maggiore dell'ultimo valore multivalore esistente, il valore specificato viene aggiunto nuovamente alla fine della sequenza di valori. Se il numero di sequenza corrisponde a un valore esistente, tale valore viene sostituito con il valore specificato.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBadColumnId</p> | <p>L'ID colonna specificato non rientra nei limiti legali di un ID di colonna.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonna descritta da <em>columnid</em> specificato non esiste nella tabella.</p> | 
| <p>JET_errColumnNotUpdatable</p> | <p>Tentativo non valido di aggiornare un valore long durante un'operazione di inserimento dell'eliminazione dell'aggiornamento originale.</p> | 
| <p>JET_errColumnTooBig</p> | <p>I dati del valore di colonna specificato nel buffer di input superano la limitazione delle dimensioni naturale per una colonna a lunghezza fissa o configurata per colonne di testo o binarie a lunghezza fissa. Questo errore viene restituito anche quando si passano più di 1024 byte di dati per una colonna lunga e si imposta JET_bitSetIntrinsicLV flag .</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Le dimensioni dei dati del valore di colonna specificato non corrispondono a quanto è naturale per il tipo di dati a lunghezza fissa.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>È stato effettuato un tentativo non valido di aggiornare una colonna a incremento automatico durante un'operazione di inserimento o aggiornamento oppure di aggiornare una colonna della versione durante un'operazione di sostituzione.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Le opzioni fornite sono sconosciute o una combinazione non valida di impostazioni di bit note.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Il parametro psetinfo- &gt; cbStruct specificato non è una dimensione valida per <a href="gg294090(v=exchg.10).md">la JET_SETINFO</a> struttura.</p> | 
| <p>JET_errMultiValuedDuplicate</p> | <p>L'operazione set column ha tentato di creare un valore duplicato e ha specificato JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errNotInTransaction</p> | <p>È stato effettuato un tentativo non valido di aggiornare un valore di colonna long quando la sessione chiamante non era in una transazione.</p> | 
| <p>JET_errNullInvalid</p> | <p>È stato effettuato un tentativo non valido di impostare una colonna non<strong>NULL</strong> su <strong>NULL.</strong></p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Uguale a JET_errNullInvalid.</p> | 
| <p>JET_errRecordTooBig</p> | <p>Non è stato possibile impostare il valore della colonna sul valore nel buffer di input perché il record avrebbe superato il limite di dimensioni correlate alle dimensioni della pagina. Le colonne di <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> possono essere archiviate separatamente dai dati dei record rimanenti. Tuttavia, le altre colonne devono essere archiviate con il record e possono causare il superamento della limitazione delle dimensioni dei record. Anche le colonne lunghe richiedono 5 byte di spazio all'interno del record come collegamento e anche questo può causare la JET_errRecordTooBig restituita.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p>Il cursore non è attualmente in fase di inserimento di un nuovo record o di aggiornamento di un record esistente.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>Questo errore si verifica quando le dimensioni configurate dell'archivio versioni non sono sufficienti per contenere tutti gli aggiornamenti in sospeso.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Il valore della colonna nel buffer di input ha superato la lunghezza massima configurata per una colonna a lunghezza variabile ed è stato troncato.</p> | 



In caso di esito positivo, la parte desiderata di un valore di colonna per la colonna specificata viene impostata con i dati copiati dal buffer di input. È possibile che il set di dati sia stato troncato se supera la lunghezza massima specificata per una colonna a lunghezza variabile.

In caso di errore, la posizione del cursore rimane invariata e nel buffer di copia non viene aggiornato alcun valore di colonna.

#### <a name="remarks"></a>Commenti

L'impostazione di valori long, valori per colonne [JET_coltypLongBinary](./jet-coltyp.md) di tipo [JET_coltypLongText](./jet-coltyp.md) [o JET_coltypLongBinary](./jet-coltyp.md), deve essere eseguita solo quando la sessione chiamante si trova in una transazione. Se la sessione chiamante non è in una transazione, è possibile eseguire il commit completo delle modifiche ai valori long archiviati separatamente anche quando l'operazione di aggiornamento viene annullata in un secondo momento. Se la sessione chiamante si trova in una transazione, è possibile eseguire il rollback completo degli effetti dell'aggiornamento annullando l'aggiornamento e il rollback della transazione di sessione.

Gli aggiornamenti degli indici non vengono eseguiti in seguito a **operazioni JetSetColumn.** Gli indici vengono invece aggiornati solo dopo il completamento di tutte le modifiche alle colonne e la [chiamata di JetUpdate.](./jetupdate-function.md) Ciò consente l'aggiornamento più efficiente degli indici quando gli indici comportano la modifica di più di una colonna.

Le dimensioni di un record sono limitate in base alle dimensioni della pagina del database. Tutti i valori long del record maggiori di cinque byte verranno archiviati separatamente dal record se i dati nel record superano il limite in seguito a **un'operazione JetSetColumn.** L'errore JET_errRecordTooBig verrà restituito solo dopo che tutti i dati separabili della colonna del record sono stati archiviati separatamente dal record e il record supera ancora il limite di dimensioni del record.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[Oggetti JetSetColumns](./jetsetcolumns-function.md)
