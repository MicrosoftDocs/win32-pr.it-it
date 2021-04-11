---
description: 'Altre informazioni su: funzione JetSetColumns'
title: Funzione JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128159"
---
# <a name="jetsetcolumns-function"></a>Funzione JetSetColumns


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetcolumns-function"></a>Funzione JetSetColumns

La funzione **JetSetColumns** ha un comportamento simile a [JetSetColumn](./jetsetcolumn-function.md) , ma consente a un'applicazione di impostare più valori di colonna in una singola operazione. Una matrice di strutture di [JET_SETCOLUMN](./jet-setcolumn-structure.md) viene utilizzata per descrivere il set di valori di colonna da impostare e per descrivere i buffer di input per ogni valore di colonna da impostare.

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*psetcolumn*

Puntatore a una matrice di una o più strutture di [JET_SETCOLUMN](./jet-setcolumn-structure.md) . Ogni struttura include le descrizioni del valore di colonna da impostare e da dove ottenere i dati della colonna da impostare.

*csetcolumn*

Numero di strutture di [JET_SETCOLUMN](./jet-setcolumn-structure.md) nella matrice specificata da *psetcolumn*.

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
<td><p>JET_errBadColumnId</p></td>
<td><p>L'ID di colonna specificato non rientra nei limiti validi di un ID di colonna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Uguale a JET_errNullInvalid.</p></td>
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
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
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
<td><p>È stato effettuato un tentativo non valido di impostare una colonna non NULL su NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Il valore della colonna non può essere impostato sul valore nel buffer di input perché avrebbe causato il superamento del limite di dimensioni relative alle dimensioni della pagina. Le colonne di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> possono essere archiviate separatamente dai dati rimanenti del record. Tuttavia, altre colonne devono essere archiviate con il record e possono causare il superamento del limite delle dimensioni del record. Anche le colonne lunghe richiedono 5 byte di spazio all'interno del record come collegamento e questo può comportare la restituzione di JET_errRecordTooBig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>Il cursore non è attualmente in fase di inserimento di un nuovo record o di aggiornamento di un record esistente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Il valore della colonna nel buffer di input supera la lunghezza massima configurata per una colonna a lunghezza variabile ed è stato troncato.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, per ogni colonna descritta in psetcolumns, la parte desiderata del valore della colonna viene impostata con i dati copiati dal buffer di input. Il set di dati della colonna potrebbe essere stato troncato se è stata superata la lunghezza massima specificata per una colonna a lunghezza variabile.

In caso di errore, la posizione del cursore viene lasciata invariata e nessun dato di valore di colonna viene aggiornato nel buffer di copia.

#### <a name="remarks"></a>Commenti

Se una singola operazione set Column restituisce un errore, l'intera operazione **JetSetColumns** restituirà un errore. Gli avvisi, in generale, vengono restituiti in psetcolumns- \> Error e non nel codice restituito da questa funzione. Tuttavia, se l'ultimo set di colonne presenta un avviso, questo avviso verrà restituito da **JetSetColumns** stesso.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
