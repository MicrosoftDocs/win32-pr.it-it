---
description: 'Altre informazioni su: funzione JetRetrieveColumns'
title: Funzione JetRetrieveColumns
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233633"
---
# <a name="jetretrievecolumns-function"></a>Funzione JetRetrieveColumns


_**Si applica a:** Windows | Windows Server_

## <a name="jetretrievecolumns-function"></a>Funzione JetRetrieveColumns

La funzione **JetRetrieveColumns** recupera più valori di colonna dal record corrente in un'unica operazione. Una matrice di strutture di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) viene utilizzata per descrivere il set di valori di colonna da recuperare e per descrivere i buffer di output per ogni valore di colonna da recuperare.

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*pretrievecolumn*

Puntatore a una matrice di una o più strutture di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) . Ogni struttura include le descrizioni del valore della colonna da recuperare e la posizione in cui archiviare i dati restituiti.

*cretrievecolumn*

Numero di strutture di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) nella matrice specificata da *pretrievecolumn*.

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
<td><p>JET_errBadItagSequence</p></td>
<td><p>È stato passato un valore del numero di sequenza di colonna multivalore non valido in pretinfo- &gt; itagSequence. I valori validi per i numeri di sequenza dei valori di colonna multivalore sono pari a 1 o superiore. Il valore 0 (zero) è valido per questa funzione ma non è valido per <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>L'ID di colonna specificato non rientra nei limiti validi di un ID di colonna.</p></td>
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
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>In alcuni casi, il buffer fornito per la colonna di recupero deve essere sufficientemente dimensionato per restituire qualsiasi quantità di valore della colonna. Ad esempio, le colonne aggiornabili con deposito sono regolate in modo da essere coerenti per il contesto transazionale della sessione chiamante e questa regolazione richiede il buffer fornito dal chiamante. Se viene fornito spazio sufficiente nel buffer, viene restituito JET_errInvalidBufferSize e non vengono restituiti dati di colonna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Le opzioni specificate sono sconosciute o una combinazione non valida di impostazioni di bit note.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno o più parametri specificati non sono corretti. Questo problema può verificarsi se retinfo. cbStruct è più piccolo della dimensione del <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
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
</tbody>
</table>


In seguito all'esito positivo, i dati delle colonne e le dimensioni della colonna vengono restituiti nei buffer forniti descritti in matrice di strutture di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) . Se un *itagSequence* è stato impostato su 0 (zero) per indicare che è stato richiesto il numero di istanze di un campo multivalore anziché i dati della colonna, il numero di istanze di una colonna multivalore viene restituito nel campo *itagSequence* . Ogni struttura [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) dispone di un campo di errore che contiene avvisi per la colonna recuperata. Se la colonna è di valore **null** , il codice di errore verrà impostato su JET_wrnColumnNull.

In caso di errore, la posizione del cursore viene lasciata invariata e nessun dato viene copiato nel buffer fornito.

#### <a name="remarks"></a>Commenti

**JetRetrieveColumns** supporta una funzionalità che non è supportata da [JetRetrieveColumn](./jetretrievecolumn-function.md) . Si tratta della possibilità di recuperare il numero di istanze di una colonna multivalore. Lo scopo di questa funzionalità è quello di consentire a un'applicazione di recuperare tutti i valori di una colonna. Questa operazione può essere eseguita determinando innanzitutto il numero di valori di una colonna. Successivamente, è possibile determinare la loro lunghezza chiamando di nuovo **JetRetrieveColumns** con una struttura [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) allocata per ogni valore per determinare la lunghezza dei dati della colonna. Questa operazione può essere eseguita passando i puntatori _PvData_ **null** con *cbMax* 0 (zero) e recuperando la lunghezza della colonna in *cbActual*. La terza e ultima chiamata può essere effettuata con la memoria allocata per i dati del valore della colonna.

Se una colonna recuperata viene troncata a causa di un buffer di lunghezza insufficiente, l'API restituirà JET_wrnBufferTruncated. Tuttavia, altri errori JET_wrnColumnNull vengono restituiti solo nel campo errore [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). Il motivo è che le applicazioni spesso vogliono garantire che tutti i dati siano stati recuperati e la restituzione di questo errore da **JetRetrieveColumns** facilita questa comprensione.

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

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
