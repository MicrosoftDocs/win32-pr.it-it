---
description: 'Altre informazioni su: Funzione JetRetrieveColumn'
title: Funzione JetRetrieveColumn
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8a9ce96be028329dea18f32459fbde88b80b75f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985624"
---
# <a name="jetretrievecolumn-function"></a>Funzione JetRetrieveColumn


_**Si applica a:** Windows | Windows Server_

## <a name="jetretrievecolumn-function"></a>Funzione JetRetrieveColumn

La **funzione JetRetrieveColumn** recupera un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore. In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore. Questa funzione può anche recuperare i dati della colonna da una voce di indice che fa riferimento al record corrente. Oltre a recuperare il valore effettivo della colonna, è anche possibile usare **JetRetrieveColumn** per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna stessa in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*columnid*

Valore [JET_COLUMNID](./jet-columnid.md) della colonna da recuperare.

È possibile specificare un valore *columnid* pari a 0 (zero) che non fa riferimento a una singola colonna. Quando *viene specificato columnid* 0 (zero), tutte le colonne contrassegnate, di tipo sparse e multivalore vengono considerate come una singola colonna. Ciò semplifica il recupero di tutte le colonne di tipo sparse presenti in un record.

*pvData*

Buffer di output che riceve il valore della colonna.

*cbData*

Dimensione massima, in byte, del buffer di output.

*pcbActual*

Riceve le dimensioni effettive, in byte, del valore della colonna.

Se questo parametro è **NULL,** le dimensioni effettive del valore della colonna non verranno restituite.

*grbit*

Gruppo di bit che contengono le opzioni da utilizzare per questa chiamata, che includono zero o più degli elementi seguenti:


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Questo flag fa in modo che il recupero della colonna recuperi il valore modificato anziché il valore originale. Se il valore non è stato modificato, viene recuperato il valore originale. In questo modo, un valore non ancora inserito o aggiornato può essere recuperato durante l'operazione di inserimento o aggiornamento di un record.</p> | 
| <p>JET_bitRetrieveFromIndex</p> | <p>Questa opzione viene utilizzata per recuperare i valori di colonna dall'indice, se possibile, senza accedere al record. In questo modo, è possibile evitare il caricamento non necessario dei record quando i dati necessari sono disponibili dalle voci di indice stesse. Nei casi in cui non è possibile recuperare il valore della colonna originale dall'indice, a causa di trasformazioni irreversibili o troncamento dei dati, si accede al record e i dati vengono recuperati come di consueto. Si tratta di un'opzione per le prestazioni e deve essere specificata solo quando è probabile che il valore della colonna possa essere recuperato dall'indice. Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster, poiché le voci di indice per l'indice cluster o primario sono i record stessi. Questo bit non può essere impostato se JET_bitRetrieveFromPrimaryBookmark è impostato anche .</p> | 
| <p>JET_bitRetrieveFromPrimaryBookmark</p> | <p>Questa opzione viene utilizzata per recuperare i valori di colonna dal segnalibro dell'indice e può differire dal valore dell'indice quando una colonna viene visualizzata sia nell'indice primario che nell'indice corrente. Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster o primario. Questo bit non può essere impostato se JET_bitRetrieveFromIndex è impostato.</p> | 
| <p>JET_bitRetrieveTag</p> | <p>Questa opzione viene usata per recuperare il numero di sequenza di un valore di colonna multivalore in pretinfo- &gt; itagSequence. Il campo itagSequence è in genere un input per il recupero di valori di colonna multivalore da un record. Tuttavia, quando si recuperano valori da un indice, è anche possibile associare la voce di indice a un numero di sequenza specifico e recuperare anche questo numero di sequenza. Il recupero del numero di sequenza può essere un'operazione dispersa e deve essere eseguito solo se necessario.</p> | 
| <p>JET_bitRetrieveNull</p> | <p>Questa opzione viene utilizzata per recuperare i valori NULL della colonna multivalore. <strong></strong> Se questa opzione non viene specificata, i valori <strong>NULL</strong> della colonna multivalore verranno ignorati automaticamente.</p> | 
| <p>JET_bitRetrieveIgnoreDefault</p> | <p>Questa opzione influisce solo sulle colonne multivalore e fa in modo che un valore <strong>NULL</strong> sia restituito quando il numero di sequenza richiesto è 1 e non sono presenti valori impostati per la colonna nel record.</p> | 
| <p>JET_bitRetrieveLongId</p> | <p>Questo flag è solo per uso interno e non deve essere usato nell'applicazione.</p> | 
| <p>JET_bitRetrieveLongValueRefCount</p> | <p>Questo flag è solo per uso interno e non deve essere usato nell'applicazione.</p> | 
| <p>JET_bitRetrieveTuple</p> | <p>Questo flag consentirà il recupero di un segmento di tupla dell'indice. Questo bit deve essere specificato con JET_bitRetrieveFromIndex.</p> | 



*pretinfo*

Se *pretinfo* viene specificato come **NULL,** la funzione si comporta come se fossero stati dati *itagSequence* pari a 1 e *ibLongValue* pari a 0 (zero). In questo modo il recupero della colonna recupera il primo valore di una colonna multivalore e recupera i dati long in corrispondenza dell'offset 0 (zero).

Questo parametro viene usato per fornire uno o più degli elementi seguenti:


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>ibLongValue</p> | <p>Fornisce un offset binario in un valore di colonna long durante il recupero di una parte di un valore di colonna.</p> | 
| <p>itagSequence</p> | <p>Fornisce il numero di sequenza del valore di colonna multivalore desiderato. Si noti che questo campo viene impostato solo se JET_bitRetrieveTag specificato. In caso contrario, non viene modificato.</p> | 
| <p>columnidNextTagged</p> | <p>Restituisce l'ID della colonna restituita quando si recuperano tutte le colonne contrassegnate, di tipo sparse e multivalore che usano il passaggio <em>di columnid</em> pari a 0 (zero).</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBadColumnId</p> | <p>L'ID di colonna specificato non rientra nei limiti legali di un ID di colonna.</p> | 
| <p>JET_errBadItagSequence</p> | <p>È stato passato un valore di numero di sequenza di colonna multivalore non valido in pretinfo- &gt; itagSequence. I valori validi per i numeri di sequenza di valori di colonna multivalore sono 1 o superiori. Il valore 0 (zero) non è valido per questa funzione.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonna descritta dal <em>valore columnid</em> specificato non esiste nella tabella.</p> | 
| <p>JET_errIndexTuplesCannotRetrieveFromIndex</p> | <p>Le colonne indicizzate come sottostringhe non possono essere recuperate dall'indice, poiché solo una piccola parte della colonna è in genere presente in ogni voce di indice.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>In alcuni casi, il buffer specificato per la colonna di recupero deve essere sufficientemente ridimensionato per restituire qualsiasi quantità del valore della colonna. Ad esempio, le colonne aggiornabili del deposito vengono modificate in modo da essere coerenti per il contesto transazionale della sessione chiamante e questa modifica richiede il buffer fornito dal chiamante. Se viene specificato spazio nel buffer insufficiente, JET_errInvalidBufferSize viene restituito un valore e non viene restituito alcun dato di colonna.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno o più parametri specificati non sono corretti. Questo problema può verificarsi se retinfo.cbStruct è inferiore alle dimensioni <a href="gg294049(v=exchg.10).md">di JET_RETINFO</a>.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Le opzioni fornite sono sconosciute o una combinazione non valida di impostazioni di bit note.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore non è posizionato su un record. I motivi possono essere diversi. Ad esempio, ciò si verifica se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Non è stato possibile recuperare l'intero valore della colonna perché il buffer specificato è inferiore alle dimensioni della colonna.</p> | 
| <p>JET_wrnColumnNull</p> | <p>Il valore della colonna recuperato è <strong>NULL.</strong></p> | 



In caso di esito positivo, il valore della colonna per la colonna specificata viene copiato nel buffer specificato. Minore di tutto il valore della colonna viene copiato con l'avviso JET_wrnBufferTruncated viene restituito. Se è *stato specificato pcbActual,* vengono restituite le dimensioni effettive del valore della colonna. Si noti **che i valori NULL** hanno una lunghezza pari a 0 (zero) e pertanto impostano le dimensioni restituite su 0 (zero). Se la colonna recuperata è una colonna multivalore ed è stato specificato *pretinfo* e JET_bitReturnTag è stato impostato come opzione, il numero di sequenza del valore della colonna viene restituito in pretinfo- \> itagSequence.

In caso di errore, la posizione del cursore rimane invariata e non vengono copiati dati nel buffer specificato.

#### <a name="remarks"></a>Commenti

Questa chiamata viene usata una sola volta per recuperare dati di dimensioni fisse o note per le colonne non multivalore. Tuttavia, quando i dati della colonna sono di dimensioni sconosciute, questa chiamata viene in genere usata due volte. Viene chiamato per primo per determinare le dimensioni dei dati in modo da poter allocare lo spazio di archiviazione necessario. Viene quindi effettuata di nuovo la stessa chiamata per recuperare i dati della colonna. Quando il numero effettivo di valori è sconosciuto, perché una colonna è multivalore, la chiamata viene in genere usata tre volte. Prima di tutto per ottenere il numero di valori e quindi due volte di più per allocare spazio di archiviazione e recuperare i dati effettivi.

Il recupero di tutti i valori per una colonna multivalore può essere eseguito chiamando ripetutamente questa funzione con un valore pretinfo- itagSequence a partire da 1 e aumentando a ogni chiamata \> successiva. È noto che l'ultimo valore di colonna viene recuperato quando JET_wrnColumnNull viene restituito dalla funzione . Si noti che questo metodo non può essere eseguito se nella sequenza di valori della colonna multivalore sono impostati valori **NULL** espliciti, poiché questi valori verrebbero ignorati. Se un'applicazione desidera recuperare tutti i valori di colonna multivalore, inclusi quelli impostati in modo esplicito su **NULL,** è necessario usare [JetRetrieveColumns](./jetretrievecolumns-function.md) anziché **JetRetrieveColumn**. Si noti che questa funzione non restituisce il numero di valori per una funzione multivalore quando viene specificato un valore *itagSequence* pari a 0 (zero). Solo [JetRetrieveColumns](./jetretrievecolumns-function.md) restituirà il numero di valori di un valore di colonna quando viene passato un valore *itagSequence* pari a 0 (zero).

Se questa funzione viene chiamata a livello di transazione 0 (zero), ad esempio, la sessione chiamante non si trova in una transazione, una transazione viene aperta e chiusa all'interno della funzione. Lo scopo di questa operazione è restituire risultati coerenti nel caso in cui un valore long si estendono su più pagine del database. Si noti che la transazione viene rilasciata tra le chiamate di funzione e una serie di chiamate a questa funzione quando la sessione non si trova in una transazione può restituire dati aggiornati dopo la prima chiamata a questa funzione.

Il valore predefinito della colonna verrà recuperato quando la colonna non è stata impostata in modo esplicito su un altro valore, a meno che non sia impostata l JET_bitRetrieveIgnoreDefault predefinita.

Il recupero del valore della colonna di incrementale automatico dal buffer di copia prima dell'inserimento è un mezzo comune per identificare un record in modo univoco per il collegamento quando si inseriscono dati normalizzati in più tabelle. Il valore di incrementale automatico viene allocato all'inizio dell'operazione di inserimento e può essere recuperato dal buffer di copia in qualsiasi momento fino al completamento dell'aggiornamento.

Quando si recuperano tutte le colonne con tag, multivalore e di tipo sparse, impostando *columnid* su 0 (zero), le colonne vengono recuperate in ordine *columnid* dal *columnid* più basso a quello più *alto.* Ogni volta che i valori delle colonne vengono recuperati, viene restituito lo stesso ordine dei valori di colonna. L'ordine è deterministico.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JetSetColumn](./jetretrievekey-function.md)  
[Oggetti JetRetrieveColumns](./jetretrievecolumns-function.md)
