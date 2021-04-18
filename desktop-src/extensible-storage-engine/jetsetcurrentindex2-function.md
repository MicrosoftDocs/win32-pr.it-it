---
description: 'Altre informazioni su: funzione JetSetCurrentIndex2'
title: Funzione JetSetCurrentIndex2
TOCTitle: JetSetCurrentIndex2 Function
ms:assetid: da94465e-bd35-45c2-9ccc-1d2e8c34aa9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294110(v=EXCHG.10)
ms:contentKeyID: 32765725
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex2W
- JetSetCurrentIndex2A
- JetSetCurrentIndex2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c95e665b549fff82e0beaaca9682329217ebb0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305727"
---
# <a name="jetsetcurrentindex2-function"></a>Funzione JetSetCurrentIndex2


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetcurrentindex2-function"></a>Funzione JetSetCurrentIndex2

La funzione **JetSetCurrentIndex2** imposta l'indice corrente di un cursore che definisce quali record di una tabella sono visibili a tale cursore e l'ordine in cui vengono visualizzati selezionando il set di voci di indice da utilizzare per esporre tali record.

```cpp
    JET_ERR JET_API JetSetCurrentIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*szIndexName*

Nome dell'indice da selezionare per il cursore.

Se questo parametro è NULL o una stringa vuota, verrà selezionato l'indice cluster. Se viene definito un indice primario per la tabella, l'indice verrà selezionato perché corrisponde all'indice cluster. Se per la tabella non è definito alcun indice primario, verrà selezionato l'indice sequenziale. La definizione dell'indice sequenziale non è stata completata. Per ulteriori informazioni, vedere [JetCreateIndex](./jetcreateindex-function.md) .

Se *pIndexID* non è null, il nome dell'indice verrà ignorato e l'indice verrà selezionato in base al relativo ID di indice.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.

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
<td><p>JET_bitMoveFirst</p></td>
<td><p>Questa opzione indica che il cursore deve essere posizionato sulla prima voce dell'indice specificato. Se viene selezionato l'indice cluster (indice primario o sequenziale) e l'indice corrente è un indice secondario, viene utilizzato JET_bitMoveFirst. Se viene selezionato l'indice corrente, questa opzione viene ignorata e non viene apportata alcuna modifica alla posizione del cursore.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNoMove</p></td>
<td><p>Questa opzione indica che il cursore deve essere posizionato sulla voce di indice del nuovo indice che corrisponde al record associato alla voce di indice in corrispondenza della posizione corrente del cursore sull'indice precedente.</p>
<p>Se la definizione del nuovo indice contiene almeno una colonna chiave multivalore, la voce dell'indice di destinazione è ambigua. In questo caso, l'oggetto <em>itagSequence</em> specificato viene utilizzato per selezionare il multivalore della colonna chiave multivalore più significativa utilizzata per posizionare il cursore. È necessario passare un solo <em>itagSequence</em> , anche nel caso di più colonne chiave multivalore perché il motore espande solo tutti i valori per la colonna chiave multivalore più significativa. Per ulteriori informazioni, vedere <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> .</p>
<p>Se viene specificato JET_bitMoveFirst, questa opzione viene ignorata.</p>
<p>Se viene selezionato l'indice corrente, questa opzione viene ignorata e non viene apportata alcuna modifica alla posizione del cursore. Se questo parametro non è presente, il relativo valore si presume che sia JET_bitMoveFirst.</p></td>
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
<td><p>JET_errBadItagSequence</p></td>
<td><p>È stato selezionato un indice secondario con l'opzione JET_bitNoMove e non è presente alcun valore per la prima colonna chiave multivalore nella nuova definizione per l'indice che corrisponde al numero di sequenza specificato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidIndexId</p></td>
<td><p>Il contenuto dell'ID di indice non è valido o è scaduto e deve essere aggiornato. Questo problema può verificarsi per <strong>JetSetCurrentIndex2</strong> quando:</p>
<ul>
<li><p>pIndexID- &gt; cbStruct non è della dimensione prevista (Windows Server 2003 e versioni successive).</p></li>
<li><p>Il motore è stato arrestato perché è stato recuperato l'ID dell'indice.</p></li>
<li><p>Tutti i cursori che fanno riferimento alla tabella contenente l'indice corrispondente all'ID dell'indice sono stati chiusi e il motore ha eliminato la definizione per l'indice dalla cache dello schema.</p></li>
<li><p>L'ID di indice viene utilizzato con un cursore aperto nella tabella errata.</p></li>
<li><p>L'indice è stato eliminato o non è ancora visibile alla sessione.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Uno dei nomi di oggetto specificati non è valido. Tutti i nomi di oggetto devono essere conformi allo stesso set di regole. Le regole sono le seguenti:</p>
<ul>
<li><p>I nomi degli oggetti devono essere composti da caratteri ASCII.</p></li>
<li><p>I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</p></li>
<li><p>I nomi degli oggetti non possono superare la lunghezza di JET_cbNameMost (64) caratteri.</p></li>
<li><p>I nomi degli oggetti non possono iniziare con uno spazio.</p></li>
<li><p>I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</p></li>
<li><p>I nomi degli oggetti non possono contenere punti esclamativi (!), punti (.), parentesi quadra aperta ([) o parentesi quadra chiusa (]).</p></li>
<li><p>Una volta convalidata, solo la parte della stringa fino al primo spazio (se presente) verrà utilizzata per il nome dell'oggetto. Ciò significa che i nomi degli oggetti non possono contenere uno spazio.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo problema può verificarsi per <strong>JetSetCurrentIndex2</strong> quando <em>PINDEXID</em> non è null e pIndexID- &gt; cbStruct non è della dimensione prevista (Windows XP e versioni precedenti).</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Un indice secondario viene selezionato con l'opzione JET_bitNoMove e non è presente alcuna voce di indice nel nuovo indice che corrisponde al record associato alla voce di indice nella posizione corrente del cursore sull'indice precedente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Il motore ha esaurito il pool di risorse utilizzate per aprire i cursori. Il numero massimo di cursori che è possibile aprire in qualsiasi momento viene controllato utilizzando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>. Per ulteriori informazioni, vedere <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> . Questo problema può verificarsi per <strong>JetSetCurrentIndex2</strong> quando è stato selezionato un indice secondario e il motore non è in grado di aprire un cursore interno per utilizzare tale indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, l'indice corrente del cursore viene impostato sull'indice richiesto. È ora possibile cercare le voci di indice usando [JetSeek](./jetseek-function.md) in base alla definizione dell'indice dell'indice richiesto. È inoltre possibile enumerare le voci di indice utilizzando [JetMove](./jetmove-function.md) nell'ordine specificato dalla definizione di tale indice. La posizione corrente del cursore viene impostata sulla prima voce di indice nell'indice (JET_bitMoveFirst) o su una voce di indice specifica correlata alla posizione corrente del cursore sull'indice precedente (JET_bitNoMove). Non si verificherà alcuna modifica allo stato del database.

In caso di errore, l'indice corrente e la posizione corrente del cursore sono in uno stato non definito. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Se l'hint ID dell'indice non è aggiornato, l'API ha semplicemente esito negativo. In questo caso, non esiste alcun fallback al nome di testo dell'indice, come si può prevedere. Questo fallback deve essere eseguito manualmente dal chiamante dell'API.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetSetCurrentIndex2W</strong> (Unicode) e <strong>JetSetCurrentIndex2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetGetCurrentIndex](./jetgetcurrentindex-function.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetSeek](./jetseek-function.md)  
[JetStopService](./jetstopservice-function.md)
