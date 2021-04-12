---
description: 'Altre informazioni su: funzione JetEnumerateColumns'
title: Funzione JetEnumerateColumns
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232557"
---
# <a name="jetenumeratecolumns-function"></a>Funzione JetEnumerateColumns


_**Si applica a:** Windows | Windows Server_

## <a name="jetenumeratecolumns-function"></a>Funzione JetEnumerateColumns

La funzione **JetEnumerateColumns** recupera in modo efficiente un set di colonne e i relativi valori dal record corrente di un cursore o dal buffer di copia del cursore. Le colonne e i valori recuperati possono essere limitati da un elenco di ID di colonna, numeri *itagSequence* e altre caratteristiche. Questa API di recupero colonne è univoca in quanto restituisce informazioni nella memoria allocata in modo dinamico, ottenuta usando un callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito dall'utente. Questa nuova flessibilità consente di recuperare in modo efficiente i dati delle colonne con caratteristiche specifiche, ad esempio le dimensioni e la molteplicità, sconosciute al chiamante. In questo modo si elimina la necessità di usare le modalità di individuazione di [JetRetrieveColumn](./jetretrievecolumn-function.md) per determinare tali caratteristiche per configurare una chiamata finale a [JetRetrieveColumn](./jetretrievecolumn-function.md) che recupererà correttamente i dati desiderati.

**Windows XP: JetEnumerateColumns** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*cEnumColumnId*

Matrice di ID di colonna, ognuno con una matrice facoltativa di numeri *itagSequence* da enumerare.

Se *cEnumColumnId* è 0 (zero), *rgEnumColumnId* viene ignorato e tutti i valori di colonna vengono enumerati e restituiti al chiamante. Se un elemento della matrice di ID di colonna fa riferimento a un ID di colonna pari a 0 (zero), l'enumerazione di tale colonna viene ignorata e viene generato uno slot corrispondente nell'output con lo stato della colonna JET_wrnColumnSkipped.

Se *ctagSequence* è 0 (zero) per un determinato elemento della matrice di ID di colonna, *rgtagSequence* viene ignorato e tutti i valori di colonna per l'ID di tale colonna vengono enumerati e restituiti al chiamante. Se un elemento di una matrice di numeri *itagSequence* fa riferimento a un numero *itagSequence* pari a 0 (zero), l'enumerazione di tale numero *itagSequence* viene ignorata e viene generato uno slot corrispondente nell'output con lo stato del valore della colonna JET_wrnColumnSkipped.

*rgEnumColumnId*

Vedere *cEnumColumnId*.

*pcEnumColumn*

Restituisce la matrice enumerata di colonne e i relativi valori nella memoria allocata tramite il callback compatibile con *itagSequence* fornito.

Se per l'input viene richiesta una matrice di ID di colonna, l'ordine e le dimensioni della matrice di output riflettono l'ordine e le dimensioni della matrice di input. Analogamente, se viene richiesta una matrice di numeri *itagSequence* per un determinato ID di colonna nell'input, l'ordine e le dimensioni della matrice di output dei valori di colonna per tale colonna rifletteranno l'ordine e le dimensioni della matrice di input.

I parametri di output vengono impostati su 0 (zero) e **null** in caso di errore, ad eccezione di JET_errBadColumnId e JET_errColumnNotFound. Quando vengono restituiti questi errori, i dati di output sono validi e completi per tutti gli ID di colonna interessati. Il codice di stato per ogni ID di colonna interessato viene impostato su uno di questi errori, in modo che il chiamante possa determinare quali ID di colonna erano negativi e potenzialmente eseguire un'azione correttiva.

*prgEnumColumn*

Vedere *pcEnumColumn*.

*pfnRealloc*

Identifica un callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) e un puntatore di contesto facoltativo usato per allocare memoria per la matrice di output di colonne e i relativi valori.

*pvReallocContext*

Vedere *pfnRealloc*.

*cbDataMost*

Imposta un limite per la quantità di dati da restituire da un testo lungo o una colonna binaria di tipo Long.

Questo parametro può essere utilizzato per impedire l'enumerazione di un valore di colonna estremamente grande. In genere, tale enumerazione potrebbe non riuscire a eseguire la chiamata API con JET_errOutOfMemory. Se un valore di colonna di grandi dimensioni viene troncato in questo modo, lo stato del valore della colonna sarà JET_wrnColumnTruncated.

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
<td><p>JET_bitEnumerateCompressOutput</p></td>
<td><p>Quando si enumerano i valori di colonna, tutte le colonne per cui si recuperano tutti i valori e con un solo valore di colonna non NULL possono essere restituite in formato compresso. Lo stato di tali colonne verrà impostato su JET_wrnColumnSingleValue e la dimensione del valore della colonna e della memoria che contiene il valore della colonna verrà restituita direttamente nella struttura di <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> . Non è garantito che tutte le colonne idonee vengano compresse in questo modo. Per ulteriori informazioni, vedere <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateCopy</p></td>
<td><p>Questa opzione indica che è necessario enumerare i valori di colonna modificati del record anziché i valori di colonna originali. Se il valore di una colonna non è stato modificato, il valore della colonna originale viene enumerato. In questo modo, è possibile enumerare un valore di colonna che non è ancora stato inserito o aggiornato durante l'inserimento o l'aggiornamento di un record.</p>
<p>Questa opzione è identica a JET_bitRetrieveCopy se utilizzata con <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> o <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumerateIgnoreDefault</p></td>
<td><p>Se una colonna specificata non è presente nel record, non verrà restituito alcun valore di colonna. In genere, il valore predefinito per la colonna, se presente, verrebbe restituito in questo caso. Si garantisce che se la colonna è impostata su un valore diverso da quello predefinito, verrà restituito un valore diverso, ovvero se una colonna con un valore predefinito viene impostata in modo esplicito su <strong>null</strong> , verrà restituito un valore <strong>null</strong> come valore per la colonna. Si noti che, anche se questa opzione è richiesta, è comunque possibile visualizzare un valore di colonna che corrisponde al valore predefinito. Non viene effettuato alcun tentativo di rimuovere i valori di colonna che corrispondono ai valori predefiniti.</p>
<p>È importante notare che questa opzione influisca sull'output di <strong>JetEnumerateColumns</strong> quando viene usato con JET_bitEnumeratePresenceOnly o JET_bitEnumerateTaggedOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateIgnoreUserDefinedDefault</p></td>
<td><p>Se una colonna specificata non è presente nel record e presenta un valore predefinito definito dall'utente, non verrà restituito alcun valore di colonna. Questa opzione impedisce al callback che calcola il valore predefinito definito dall'utente per la colonna di essere chiamato durante l'enumerazione dei valori per la colonna.</p>
<p><strong>Windows Server 2003 e versioni precedenti:  </strong> Per Windows Server 2003 e versioni precedenti, l'operazione avrà esito negativo con JET_errCallbackFailed.</p>
<p><strong>Windows Server 2003 SP1:  </strong> Questo possibile valore è disponibile solo per i sistemi operativi Windows Server 2003 SP1 e versioni successive. Se questo valore può essere specificato e la tabella contiene una colonna con un valore predefinito definito dall'utente, l'operazione avrà esito negativo con JET_errCallbackFailed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumeratePresenceOnly</p></td>
<td><p>Se è presente un valore non NULL per il valore della colonna o della colonna richiesta, i dati associati non vengono restituiti. Lo stato associato per quel valore di colonna o colonna verrà invece impostato su JET_wrnColumnPresent. Se il valore della colonna o della colonna è <strong>null</strong> , JET_wrnColumnNull verrà restituito come di consueto.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateTaggedOnly</p></td>
<td><p>Quando si enumerano tutti i valori di colonna nel record, ad esempio quando <em>cEnumColumnId</em> è zero, verranno restituiti solo i valori delle colonne con tag. Questa opzione non è consentita durante l'enumerazione di una matrice di ID di colonna specifica.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumerateInRecordOnly</p></td>
<td><p><strong>Windows 7:  </strong> JET_bitEnumerateInRecordOnly è stato introdotto in Windows 7.</p></td>
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
<td><p>L'ID di colonna specificato non rientra nei limiti validi di un ID di colonna. Questo errore viene restituito da <strong>JetEnumerateColumns</strong> se sono stati richiesti ID di colonna specifici, uno di questi ID di colonna non è valido e il primo ID di colonna non è riuscito con questo errore per il codice di stato della colonna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonna descritta dall'ID colonna specificato non esiste nella tabella. Questo errore viene restituito da <strong>JetEnumerateColumns</strong> se sono stati richiesti ID di colonna specifici, uno di questi ID di colonna non è valido e il primo ID di colonna non è riuscito con questo errore per il codice di stato della colonna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:  </strong> Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una delle opzioni richieste non è valida o non è stata implementata. Questo errore viene restituito da <strong>JetEnumerateColumns</strong> quando:</p>
<ul>
<li><p>JET_bitEnumerateLocal specificato.</p></li>
<li><p>È stato specificato un <em>grbit</em> non valido.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo errore viene restituito da <strong>JetEnumerateColumns</strong> quando:</p>
<ul>
<li><p><em>pcEnumColumn</em> è <strong>null</strong>.</p></li>
<li><p><em>prgEnumColumn</em> è <strong>null</strong>.</p></li>
<li><p><em>pfnRealloc</em> è <strong>null</strong>.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore non è posizionato in corrispondenza di un record. I motivi possono essere diversi. Questa situazione si verifica, ad esempio, se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Il cursore è posizionato in corrispondenza di un record che è stato eliminato. I motivi possono essere diversi. Il motivo più comune è che la sessione non è in una transazione, il cursore è stato posizionato in corrispondenza di un record, tale record è stato eliminato e quindi il cursore ha tentato di fare riferimento a tale record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:  </strong> Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, i dati richiesti verranno restituiti nei buffer di output. È responsabilità del chiamante liberare la memoria allocata da questo callback e restituita nei buffer di output. Tale memoria deve essere liberata tramite il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito. Non si verificherà alcuna modifica allo stato del database.

In caso di errore, non verrà restituito alcun dato richiesto. Qualsiasi memoria allocata durante la chiamata verrà liberata automaticamente utilizzando il callback compatibile con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fornito. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Se si enumerano tutti i valori di colonna nel record e non è stato specificato JET_bitEnumerateIgnoreDefaults, non è possibile presupporre che non venga mai visualizzato un valore di colonna o di colonna con un codice di stato JET_wrnColumnNull. Questo codice di stato può essere visualizzato se una colonna ha un valore predefinito ed è stata impostata in modo esplicito su **null** o se la colonna è una colonna non di tipo sparse, ad esempio una colonna fissa o variabile.

Il parametro *cbDataMost* non è applicabile a tutti i valori di colonna. Questo parametro consente di troncare solo i valori long text e long Column Binary che sono così grandi che sono stati archiviati separatamente dal record.

Se **JetEnumerateColumns** restituisce i dati nei parametri di output, il chiamante è responsabile della liberazione della memoria nell'array e della memoria a cui fanno riferimento i puntatori incorporati nella matrice.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JET_PFNREALLOC](./jet-pfnrealloc-callback-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
