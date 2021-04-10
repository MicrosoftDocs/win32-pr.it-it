---
description: 'Altre informazioni su: funzione JetMove'
title: Funzione JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225877"
---
# <a name="jetmove-function"></a>Funzione JetMove


_**Si applica a:** Windows | Windows Server_

## <a name="jetmove-function"></a>Funzione JetMove

La funzione **JetMove** posiziona un cursore all'inizio o alla fine di un indice e attraversa le voci dell'indice in avanti o indietro. È anche possibile spostare il cursore avanti o indietro sull'indice corrente in base a un numero specificato di voci di indice. Un altro approccio consiste nel limitare artificialmente le voci di indice che possono essere enumerate usando **JetMove** impostando un intervallo di indice sul cursore usando [JetSetIndexRange](./jetsetindexrange-function.md).

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*Corvo*

Offset arbitrario che indica lo spostamento desiderato del cursore sull'indice corrente.

Oltre agli offset standard, questo parametro può essere impostato anche con una delle opzioni seguenti.

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
<td><p>JET_MoveFirst</p></td>
<td><p>Sposta il cursore sulla prima voce di indice nell'indice (se presente).</p>
<p><strong>Nota</strong>   Il valore letterale di-2147483648 viene utilizzato per indicare questa opzione. Non usare questo valore come un offset normale o un comportamento imprevisto può verificarsi.</p></td>
</tr>
<tr class="even">
<td><p>JET_MoveLast</p></td>
<td><p>Sposta il cursore sull'ultima voce di indice nell'indice (se presente).</p>
<p><strong>Nota</strong>   Il valore letterale 2147483647 viene utilizzato per indicare questa opzione. Non usare questo valore come un offset normale o un comportamento imprevisto può verificarsi.</p></td>
</tr>
<tr class="odd">
<td><p>JET_MoveNext</p></td>
<td><p>Sposta il cursore sulla voce di indice successiva nell'indice (se presente). Questo valore è esattamente uguale a un offset normale di + 1.</p></td>
</tr>
<tr class="even">
<td><p>JET_MovePrevious</p></td>
<td><p>Sposta il cursore sulla voce di indice precedente nell'indice (se ne esiste uno).</p>
<p>Questo valore è esattamente uguale a un offset normale di-1 o 0 (zero).</p>
<p>Il cursore rimane in corrispondenza della posizione logica corrente e viene verificata l'esistenza della voce di indice corrispondente a tale posizione logica.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_bitMoveKeyNE</p></td>
<td><p>Sposta il cursore avanti o indietro per il numero di voci di indice necessarie per ignorare il numero richiesto di valori di chiave di indice rilevati nell'indice. Questo ha l'effetto di comprimere le voci di indice con valori di chiave duplicati in una singola voce di indice. In genere, un offset sposta il cursore in base al numero di voci di indice specificato indipendentemente dai valori di chiave.</p></td>
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
<td><p>Operazione riuscita. Per <strong>JetMove</strong>, ciò significa che è stata trovata una voce di indice in corrispondenza della posizione o dell'offset richiesto nell'indice corrente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore non è attualmente posizionato in corrispondenza di una voce di indice. Per <strong>JetMove</strong>, ciò significa che non è stata trovata una voce di indice nella posizione o nell'offset richiesto per l'indice corrente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Il cursore è attualmente posizionato logicamente su una voce di indice che corrisponde a un record che è stato eliminato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice che corrisponde alla posizione o all'offset richiesto. Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato. Se è attivo un intervallo di indici e JET_MoveFirst o JET_MoveLast è stato specificato, l'intervallo di indici verrà annullato. Non si verificherà alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, la posizione del cursore rimarrà invariata a meno che non venga restituito JET_errNoCurrentRecord. In tal caso, il cursore viene posizionato in corrispondenza del punto in cui la voce di indice corrispondente al percorso o all'offset richiesto è stata. Il cursore può essere spostato in relazione a tale posizione, ma non è ancora presente in una voce di indice valida. Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato. Se è attivo un intervallo di indici e JET_MoveFirst o JET_MoveLast è stato specificato, l'intervallo di indici verrà annullato. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

È possibile spostare un cursore in due posizioni speciali usando **JetMove**, prima e dopo l'ultimo. Se il cursore si trova nella prima voce di indice della tabella e **JetMove** viene chiamato con JET_MovePrevious, la chiamata avrà esito negativo con JET_errNoCurrentRecord e il cursore verrà posizionato logicamente prima della prima voce nell'indice. Questa posizione logica viene mantenuta anche se viene inserita un'altra voce di indice prima della prima voce nell'indice. Una situazione analoga si verifica per dopo l'ultimo rispetto alla fine dell'indice. Prima e dopo l'ultimo sono particolarmente utili quando si configura un intervallo di voci di indice da iterare usando **JetMove**, usando un modello iteratore che prevede di passare sempre all'elemento successivo (o precedente) prima di usare tale elemento.

Il set di voci di indice che possono essere visitate da **JetMove** può essere limitato impostando un intervallo di indice sul cursore. Questa operazione è utile per le applicazioni che enumerano un set di voci di indice che corrispondono a criteri semplici che possono essere espressi tramite una coppia di chiavi di ricerca compilate per l'indice. Per ulteriori informazioni, vedere [JetSetIndexRange](./jetsetindexrange-function.md).

Nelle versioni precedenti a Windows Server 2003 SP1, si verifica un problema in **JetMove** che si verifica in alcuni casi specifici, che influiscono sull'applicazione corretta di un intervallo di indice impostato dalla funzione [JetSetIndexRange](./jetsetindexrange-function.md) . Se il cursore si trova attualmente prima della prima voce di indice e un intervallo di indici è impostato con un limite superiore minore della prima voce di indice, la chiamata successiva a **JetMove** verrà erroneamente inviata a tale voce di indice invece di non avere esito positivo con JET_errNoCurrentRecord, come previsto. Lo stesso errore si verifica per la situazione analoga a partire dalla fine dell'indice. Questa situazione può verificarsi in un'applicazione che imposta un intervallo di indici e la sposta usando un iteratore che prevede l'avvio prima della prima voce di indice che è membro del set di voci da enumerare, anziché iniziare sulla prima voce di indice di tale set. Questa situazione si verifica anche nel caso analogo a partire dalla fine dell'indice. La soluzione alternativa consiste nell'applicazione per verificare manualmente che la voce di indice acquisita si trovi all'interno dell'intervallo di indici confrontando la chiave per la voce di indice corrente (recuperata utilizzando [JetRetrieveKey](./jetretrievekey-function.md)) con la chiave che rappresenta la fine dell'intervallo di indici corrente (recuperato utilizzando [JetRetrieveKey](./jetretrievekey-function.md) utilizzando JET_bitRetrieveCopy).

È importante prestare attenzione quando si passano gli offset calcolati a **JetMove**. Se l'offset calcolato è minore o uguale a JET_MoveFirst, tale offset deve essere suddiviso in più parti, ognuna delle quali viene passata a **JetMove** separatamente ma all'interno di una singola transazione per ottenere l'effetto desiderato. Lo stesso vale per gli offset maggiori o uguali a JET_MoveNext. È improbabile che un'applicazione venga sottoposta a questa situazione nel mondo reale, ma è bene avere una difesa contro questo caso, data la semantica molto diversa di JET_MoveFirst e JET_MoveLast da un offset normale.

Quando **JetMove** viene chiamato con un offset molto grande, ad esempio quando il parametro Crow è impostato su 1000, **JetMove** attraversa tutte le voci di indice 1000 per raggiungere la posizione finale. Attualmente, l'API ESE non fornisce un modo efficiente per passare direttamente a una voce di indice specificata per offset senza attraversare ogni voce di indice.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
