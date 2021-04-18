---
description: 'Altre informazioni su: funzione JetSetColumn'
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
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307808"
---
# <a name="jetsetcolumn-function"></a>Funzione JetSetColumn


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetcolumn-function"></a>Funzione JetSetColumn

La funzione **JetSetColumn** modifica un valore di colonna singolo in un record modificato da inserire o per aggiornare il record corrente. Può sovrascrivere un valore esistente, aggiungere un nuovo valore a una sequenza di valori in una colonna multivalore, rimuovere un valore da una sequenza di valori in una colonna multivalore o aggiornare tutto o parte di un valore Long, una colonna di tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md).

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

*TableID*

Cursore da utilizzare per questa chiamata.

*ColumnID*

[JET_COLUMNID](./jet-columnid.md) della colonna da recuperare. In alternativa, è possibile assegnare un valore *ColumnID* pari a 0 (zero). Quando viene specificato *ColumnID* 0 (zero), tutte le colonne con tag, le colonne di tipo sparse e multivalore vengono considerate come una singola colonna. Ciò facilita il recupero di tutte le colonne di tipo sparse presenti in un record.

*pvData*

Buffer di input contenente i dati da utilizzare per il valore della colonna.

*cbData*

Dimensioni in byte del buffer di input.

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
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Questa opzione consente di accodare i dati a una colonna di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. È possibile ottenere lo stesso comportamento determinando la dimensione del valore Long esistente e specificando <em>ibLongValue</em> in <em>psetinfo</em>. Tuttavia, è più semplice utilizzare questo <em>grbit</em> poiché la conoscenza delle dimensioni del valore della colonna esistente non è necessaria.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Questa opzione consente di sostituire il valore Long esistente con i dati appena forniti. Quando si utilizza questa opzione, è come se il valore Long esistente fosse stato impostato su 0 (zero) lunghezza prima dell'impostazione dei nuovi dati.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Questa opzione è applicabile solo per le colonne con tag, sparse o multivalore. Causa la restituzione del valore predefinito della colonna nelle successive operazioni di recupero della colonna. Tutti i valori di colonna esistenti vengono rimossi.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Questa opzione viene usata per forzare un valore Long, colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, da archiviare separatamente dal resto dei dati del record. Questa situazione si verifica in genere quando la dimensione del valore Long impedisce che venga archiviata con i dati dei record rimanenti. Tuttavia, questa opzione può essere usata per forzare l'archiviazione separata del valore Long. Si noti che non è possibile forzare la separazione dei valori long di quattro byte di dimensioni minori. In questi casi, l'opzione viene ignorata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Questa opzione viene usata per interpretare il buffer di input come numero intero di byte da impostare come lunghezza del valore Long descritto dal <em>ColumnID</em> specificato e, se specificato, il numero di sequenza in psetinfo- &gt; itagSequence. Se la dimensione specificata è maggiore del valore della colonna esistente, la colonna verrà estesa con 0. Se le dimensioni sono inferiori al valore della colonna esistente, il valore verrà troncato.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Questa opzione viene utilizzata per applicare che tutti i valori di una colonna multivalore sono distinti. Questa opzione consente di confrontare i dati della colonna di origine, senza alcuna trasformazione, con altri valori di colonna esistenti e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, non è possibile specificare anche JET_bitSetAppendLV JET_bitSetOverwriteLV e JET_bitSetSizeLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Questa opzione viene utilizzata per applicare che tutti i valori di una colonna multivalore sono distinti. Questa opzione Confronta la chiave di trasformazione normalizzata dei dati della colonna, ad altri valori di colonna esistenti trasformati in modo simile e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, non è possibile specificare anche JET_bitSetAppendLV JET_bitSetOverwriteLV e JET_bitSetSizeLV.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Questa opzione viene utilizzata per impostare un valore su una lunghezza pari a zero. In genere, un valore di colonna è impostato su <strong>null</strong> passando un cbMax di 0 (zero). Tuttavia, per alcuni tipi, ad esempio <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, un valore di colonna può essere 0 (zero) Length anziché <strong>null</strong>e questa opzione viene usata per distinguere tra <strong>null</strong> e 0 (zero) Length.</p>
<p><strong>Nota</strong>  In generale, se la colonna è una colonna a lunghezza fissa, questo bit viene ignorato e la colonna viene impostata su <strong>null</strong>. Tuttavia, se la colonna è una colonna con tag a lunghezza fissa, la lunghezza della colonna viene impostata su 0. Quando la colonna con tag a lunghezza fissa è impostata su 0, i tentativi di recuperare la colonna con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> riusciranno, ma la lunghezza effettiva restituita nel parametro <em>cbActual</em> è 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Questa opzione viene usata per archiviare l'intero valore lungo nel record.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetCompressed</p></td>
<td><p>Questa opzione viene usata per tentare la compressione dei dati durante l'archiviazione dei dati.</p>
<p><strong>Windows 7:</strong>  JET_bitSetCompressed è stato introdotto in Windows 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUncompressed</p></td>
<td><p>Questa opzione non consente di eseguire la compressione durante l'archiviazione dei dati.</p>
<p><strong>Windows 7:</strong>  JET_bitSetUnCompressed è stato introdotto in Windows 7.</p></td>
</tr>
</tbody>
</table>


*psetinfo*

Puntatore a parametri di input facoltativi che possono essere impostati per questa funzione utilizzando la struttura [JET_SETINFO](./jet-setinfo-structure.md) .

Se *psetinfo* viene specificato come **null** , la funzione si comporta come se venisse assegnato un *itagSequence* di 1 e un *ibLongValue* di 0 (zero). In questo modo column set imposta il primo valore di una colonna multivalore e imposta i dati lunghi a partire dall'offset 0 (zero).

Per questo parametro è possibile impostare le opzioni seguenti:

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
<td><p>Offset binario in un valore di colonna lungo in cui devono iniziare i dati impostati.</p></td>
</tr>
<tr class="even">
<td><p>itagSequence</p></td>
<td><p>Numero di sequenza del valore della colonna multivalore desiderato da impostare. Se <em>itagSequence</em> è impostato su 0 (zero), il valore specificato deve essere aggiunto alla fine della sequenza di valori multivalore. Se il numero di sequenza specificato è maggiore dell'ultimo valore multivalore esistente, il valore specificato viene aggiunto alla fine della sequenza di valori. Se il numero di sequenza corrisponde a un valore esistente, il valore viene sostituito con il valore specificato.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonna descritta dal <em>ColumnID</em> specificato non esiste nella tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable</p></td>
<td><p>È stato effettuato un tentativo non valido di aggiornare un valore Long durante un'operazione di eliminazione dell'aggiornamento originale della copia di inserimento.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig</p></td>
<td><p>I dati del valore di colonna specificati nel buffer di input superano il limite di dimensione naturale per una colonna a lunghezza fissa o sono configurati per colonne di tipo text o binary a lunghezza fissa. Questo errore viene restituito anche quando si passano più di 1024 byte di dati per una colonna estesa e si imposta il flag di JET_bitSetIntrinsicLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>La dimensione dei dati del valore della colonna specificata non corrisponde a quanto è naturale per il tipo di dati a lunghezza fissa.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>È stato effettuato un tentativo non valido di aggiornare una colonna con incremento automatico durante un'operazione di inserimento o aggiornamento oppure di aggiornare una colonna della versione durante un'operazione di sostituzione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Le opzioni specificate sono sconosciute o una combinazione non valida di impostazioni di bit note.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Il valore di psetinfo- &gt; cbStruct specificato non è una dimensione valida per la struttura <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate</p></td>
<td><p>L'operazione set Column ha tentato di creare un valore duplicato e ha specificato JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>È stato effettuato un tentativo non valido di aggiornare un valore di colonna lungo quando la sessione chiamante non era presente in una transazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>È stato effettuato un tentativo non valido di impostare una colonna non<strong>null</strong> su <strong>null</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Uguale a JET_errNullInvalid.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Il valore della colonna non può essere impostato sul valore nel buffer di input perché avrebbe causato il superamento del limite di dimensioni relative alle dimensioni della pagina. Le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> possono essere archiviate separatamente dai dati rimanenti del record. Tuttavia, altre colonne devono essere archiviate con il record e possono causare il superamento del limite delle dimensioni del record. Anche le colonne lunghe richiedono 5 byte di spazio all'interno del record come collegamento e questo può comportare la restituzione di JET_errRecordTooBig.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>Il cursore non è attualmente in fase di inserimento di un nuovo record o di aggiornamento di un record esistente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Questo errore si verifica quando le dimensioni configurate dell'archivio versioni non sono sufficienti per contenere tutti gli aggiornamenti in sospeso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Il valore della colonna nel buffer di input supera la lunghezza massima configurata per una colonna a lunghezza variabile ed è stato troncato.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, la parte desiderata di un valore di colonna per la colonna specificata viene impostata con i dati copiati dal buffer di input. Il set di dati potrebbe essere stato troncato se è stata superata la lunghezza massima specificata per una colonna a lunghezza variabile.

In caso di errore, la posizione del cursore viene lasciata invariata e nessun dato di valore di colonna viene aggiornato nel buffer di copia.

#### <a name="remarks"></a>Commenti

L'impostazione di valori Long, valori per le colonne [JET_coltypLongBinary](./jet-coltyp.md) di tipo [JET_coltypLongText](./jet-coltyp.md) o [JET_coltypLongBinary](./jet-coltyp.md), deve essere eseguita solo quando la sessione chiamante si trova in una transazione. Se la sessione chiamante non si trova in una transazione, è possibile eseguire il commit completo delle modifiche apportate ai valori Long archiviati separatamente, anche quando l'operazione di aggiornamento viene annullata in un secondo momento. Se la sessione chiamante si trova in una transazione, è possibile eseguire il rollback completo degli effetti dell'aggiornamento annullando l'aggiornamento ed eseguendo il rollback della transazione di sessione.

Gli aggiornamenti dell'indice non vengono eseguiti come risultato delle operazioni di **JetSetColumn** . Gli indici vengono invece aggiornati solo dopo il completamento di tutte le modifiche apportate alle colonne e viene chiamato [JetUpdate](./jetupdate-function.md) . Ciò consente di aggiornare più efficacemente gli indici quando gli indici coinvolgono più di una colonna da modificare.

Le dimensioni di un record sono limitate in base alle dimensioni della pagina del database. Tutti i valori Long nel record di dimensioni maggiori di cinque byte verranno archiviati separatamente dal record qualora i dati nel record superino il limite risultante da un'operazione **JetSetColumn** . Il JET_errRecordTooBig di errore viene restituito solo dopo che tutti i dati della colonna di record separabili sono stati archiviati separatamente dal record e il record supera ancora il limite delle dimensioni dei record.

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
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
