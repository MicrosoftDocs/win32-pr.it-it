---
description: 'Altre informazioni su: funzione JetRetrieveColumn'
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
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318084"
---
# <a name="jetretrievecolumn-function"></a>Funzione JetRetrieveColumn


_**Si applica a:** Windows | Windows Server_

## <a name="jetretrievecolumn-function"></a>Funzione JetRetrieveColumn

La funzione **JetRetrieveColumn** recupera un valore di colonna singola dal record corrente. Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore. In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore. Questa funzione può anche recuperare i dati di colonna da una voce di indice che fa riferimento al record corrente. Oltre a recuperare il valore della colonna effettivo, è possibile utilizzare **JetRetrieveColumn** anche per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.

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

*TableID*

Cursore da utilizzare per questa chiamata.

*ColumnID*

[JET_COLUMNID](./jet-columnid.md) della colonna da recuperare.

È possibile specificare un valore *ColumnID* pari a 0 (zero) che non si riferisce a una singola colonna. Quando viene specificato *ColumnID* 0 (zero), tutte le colonne con tag, le colonne di tipo sparse e quelle multivalore vengono considerate come una singola colonna. Ciò facilita il recupero di tutte le colonne di tipo sparse presenti in un record.

*pvData*

Buffer di output che riceve il valore della colonna.

*cbData*

Dimensione massima, in byte, del buffer di output.

*pcbActual*

Riceve le dimensioni effettive, in byte, del valore della colonna.

Se questo parametro è **null**, le dimensioni effettive del valore della colonna non verranno restituite.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti:

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
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Questo flag consente a retrieve Column di recuperare il valore modificato anziché il valore originale. Se il valore non è stato modificato, viene recuperato il valore originale. In questo modo, è possibile recuperare un valore che non è ancora stato inserito o aggiornato durante l'operazione di inserimento o aggiornamento di un record.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveFromIndex</p></td>
<td><p>Questa opzione viene utilizzata per recuperare i valori di colonna dall'indice, se possibile, senza accedere al record. In questo modo, è possibile evitare il caricamento di record superflui quando sono disponibili dati necessari dalle voci dell'indice. Nei casi in cui non è possibile recuperare il valore della colonna originale dall'indice a causa di trasformazioni irreversibili o troncamenti dei dati, il record sarà accessibile e i dati verranno recuperati normalmente. Si tratta di un'opzione relativa alle prestazioni e deve essere specificata solo quando è probabile che il valore della colonna possa essere recuperato dall'indice. Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster, perché le voci di indice per l'indice cluster o primario sono i record stessi. Non è possibile impostare questo bit se è stato impostato anche JET_bitRetrieveFromPrimaryBookmark.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveFromPrimaryBookmark</p></td>
<td><p>Questa opzione viene utilizzata per recuperare i valori di colonna dal segnalibro index e può variare dal valore di indice quando una colonna viene visualizzata sia nell'indice primario che nell'indice corrente. Questa opzione non deve essere specificata se l'indice corrente è l'indice cluster o primario. Non è possibile impostare questo bit se è stato impostato anche JET_bitRetrieveFromIndex.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveTag</p></td>
<td><p>Questa opzione viene utilizzata per recuperare il numero di sequenza di un valore di colonna multivalore in pretinfo- &gt; itagSequence. Il campo itagSequence è in genere un input per il recupero di valori di colonna multivalore da un record. Tuttavia, quando si recuperano i valori da un indice, è anche possibile associare la voce di indice a un determinato numero di sequenza e recuperare anche questo numero di sequenza. Il recupero del numero di sequenza può essere un'operazione costosa e deve essere eseguito solo se necessario.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveNull</p></td>
<td><p>Questa opzione viene utilizzata per recuperare i valori <strong>null</strong> della colonna multivalore. Se questa opzione non è specificata, i valori <strong>null</strong> della colonna multivalore verranno automaticamente ignorati.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveIgnoreDefault</p></td>
<td><p>Questa opzione ha effetto solo sulle colonne multivalore e causa la restituzione di un valore <strong>null</strong> quando il numero di sequenza richiesto è 1 e non sono presenti valori impostati per la colonna nel record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveLongId</p></td>
<td><p>Questo flag è solo per uso interno e non deve essere utilizzato nell'applicazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveLongValueRefCount</p></td>
<td><p>Questo flag è solo per uso interno e non deve essere utilizzato nell'applicazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveTuple</p></td>
<td><p>Questo flag consente il recupero di un segmento di tupla dell'indice. Questo bit deve essere specificato con JET_bitRetrieveFromIndex.</p></td>
</tr>
</tbody>
</table>


*pretinfo*

Se *pretinfo* viene fornito come **null** , la funzione si comporta come se fosse stato specificato un *itagSequence* di 1 e un *ibLongValue* di 0 (zero). In questo modo il recupero della colonna Recupera il primo valore di una colonna multivalore e recupera i dati lunghi in corrispondenza dell'offset 0 (zero).

Questo parametro viene usato per fornire uno o più degli elementi seguenti:

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
<td><p>ibLongValue</p></td>
<td><p>Restituisce un offset binario in un valore di colonna lungo durante il recupero di una parte di un valore di colonna.</p></td>
</tr>
<tr class="even">
<td><p>itagSequence</p></td>
<td><p>Indica il numero di sequenza del valore della colonna multivalore desiderato. Si noti che questo campo viene impostato solo se viene specificato il JET_bitRetrieveTag. In caso contrario, non sarà modificato.</p></td>
</tr>
<tr class="odd">
<td><p>columnidNextTagged</p></td>
<td><p>Restituisce l'ID di colonna del valore della colonna restituito durante il recupero di tutte le colonne con tag, di tipo sparse e multivalore, usando il passaggio di <em>ColumnID</em> di 0 (zero).</p></td>
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
<td><p>JET_errBadColumnId</p></td>
<td><p>L'ID di colonna specificato non rientra nei limiti validi di un ID di colonna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadItagSequence</p></td>
<td><p>È stato passato un valore del numero di sequenza di colonna multivalore non valido in pretinfo- &gt; itagSequence. I valori validi per i numeri di sequenza dei valori di colonna multivalore sono pari a 1 o superiore. Il valore 0 (zero) non è valido per questa funzione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonna descritta dal <em>ColumnID</em> specificato non esiste nella tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex</p></td>
<td><p>Le colonne indicizzate come sottostringhe non possono essere recuperate dall'indice, perché solo una piccola parte della colonna è in genere presente in ogni voce di indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>In alcuni casi, il buffer fornito per la colonna di recupero deve essere sufficientemente dimensionato per restituire qualsiasi quantità di valore della colonna. Ad esempio, le colonne aggiornabili con deposito sono regolate in modo da essere coerenti per il contesto transazionale della sessione chiamante e questa regolazione richiede il buffer fornito dal chiamante. Se viene fornito spazio sufficiente nel buffer, viene restituito JET_errInvalidBufferSize e non vengono restituiti dati di colonna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno o più parametri specificati non sono corretti. Questo problema può verificarsi se retinfo. cbStruct è più piccolo della dimensione del <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Le opzioni specificate sono sconosciute o una combinazione non valida di impostazioni di bit note.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore non è posizionato in corrispondenza di un record. I motivi possono essere diversi. Questa situazione si verifica, ad esempio, se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</p></td>
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
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Impossibile recuperare l'intero valore della colonna perché il buffer specificato è inferiore alle dimensioni della colonna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Il valore della colonna recuperato è <strong>null</strong>.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il valore della colonna per la colonna specificata viene copiato nel buffer specificato. Viene copiato un valore inferiore a quello di tutte le colonne con l'avviso JET_wrnBufferTruncated viene restituito. Se è stato specificato *pcbActual* , vengono restituite le dimensioni effettive del valore della colonna. Si noti che i valori **null** hanno una lunghezza pari a 0 (zero) e in questo modo le dimensioni restituite vengono impostate su 0 (zero). Se la colonna recuperata è una colonna multivalore e è stato specificato *pretinfo* e JET_bitReturnTag è stato impostato come opzione, il numero di sequenza del valore della colonna viene restituito in pretinfo- \> itagSequence.

In caso di errore, la posizione del cursore viene lasciata invariata e nessun dato viene copiato nel buffer fornito.

#### <a name="remarks"></a>Commenti

Questa chiamata viene utilizzata una sola volta per recuperare dati di dimensioni fisse o note per le colonne non multivalore. Tuttavia, quando i dati della colonna sono di dimensioni sconosciute, questa chiamata viene in genere utilizzata due volte. Viene chiamato per primo per determinare le dimensioni dei dati in modo da poter allocare lo spazio di archiviazione necessario. Viene quindi eseguita di nuovo la stessa chiamata per recuperare i dati della colonna. Quando il numero effettivo di valori è sconosciuto, perché una colonna è multivalore, la chiamata viene in genere utilizzata tre volte. Per prima cosa, ottenere il numero di valori e quindi due volte più per allocare spazio di archiviazione e recuperare i dati effettivi.

Il recupero di tutti i valori per una colonna multivalore può essere eseguito chiamando ripetutamente questa funzione con un valore pretinfo- \> itagSequence a partire da 1 e aumentando a ogni chiamata successiva. Il valore dell'ultima colonna è noto per essere recuperato quando una JET_wrnColumnNull viene restituita dalla funzione. Si noti che questo metodo non può essere eseguito se per la colonna multivalore sono impostati valori **null** espliciti nella sequenza di valori, perché questi valori verranno ignorati. Se un'applicazione desidera recuperare tutti i valori di colonna multivalore, inclusi quelli impostati in modo esplicito su **null**, è necessario utilizzare [JetRetrieveColumns](./jetretrievecolumns-function.md) anziché **JetRetrieveColumn**. Si noti che questa funzione non restituisce il numero di valori per una funzione multivalore quando viene specificato un valore *itagSequence* pari a 0 (zero). Solo [JetRetrieveColumns](./jetretrievecolumns-function.md) restituirà il numero di valori di un valore di colonna quando viene passato un valore *itagSequence* pari a 0 (zero).

Se questa funzione viene chiamata a livello di transazione 0 (zero), ad esempio, la sessione chiamante non si trova in una transazione, una transazione viene aperta e chiusa all'interno della funzione. Lo scopo è quello di restituire risultati coerenti nel caso in cui un valore Long estenda le pagine del database. Si noti che la transazione viene rilasciata tra le chiamate di funzione e una serie di chiamate a questa funzione quando la sessione non è in una transazione può restituire dati aggiornati dopo la prima chiamata a questa funzione.

Il valore predefinito della colonna verrà recuperato quando la colonna non è stata impostata in modo esplicito su un altro valore, a meno che non sia impostata l'opzione JET_bitRetrieveIgnoreDefault.

Il recupero del valore della colonna AutoIncrement dal buffer di copia prima dell'inserimento è un metodo comune per identificare in modo univoco un record per il collegamento quando si inseriscono dati normalizzati in più tabelle. Il valore di incremento automatico viene allocato all'inizio dell'operazione di inserimento e può essere recuperato dal buffer di copia in qualsiasi momento fino al completamento dell'aggiornamento.

Quando si recuperano tutte le colonne con tag, multivalore e di tipo sparse, impostando *ColumnID* su 0 (zero), le colonne vengono recuperate nell'ordine *ColumnID* dalla *ColumnID* più bassa alla *ColumnID* più alta. Viene restituito lo stesso ordine dei valori di colonna ogni volta che i valori delle colonne vengono recuperati. L'ordine è deterministico.

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JetSetColumn](./jetretrievekey-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
