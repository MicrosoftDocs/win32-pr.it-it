---
description: 'Altre informazioni su: funzione JetSetIndexRange'
title: Funzione JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883085633bebf25180c82f0f8917f6fa31fe7304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226249"
---
# <a name="jetsetindexrange-function"></a>Funzione JetSetIndexRange


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetindexrange-function"></a>Funzione JetSetIndexRange

La funzione **JetSetIndexRange** limita temporaneamente il set di voci di indice che il cursore può utilizzare [JetMove](./jetmove-function.md) a quelle a partire dalla voce di indice corrente e termina in corrispondenza della voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e ai criteri associati specificati. È necessario che una chiave di ricerca sia stata costruita in precedenza usando [JetMakeKey](./jetmakekey-function.md).

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableidSrc*

Cursore da utilizzare per questa chiamata.

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
<td><p>JET_bitRangeInclusive</p></td>
<td><p>Questa presenza o assenza di questa opzione indica i criteri limite dell'intervallo di indici. Quando è presente, questa opzione indica che il limite dell'intervallo di indici è incluso. Se assente, questa opzione indica che il limite dell'intervallo di indici è esclusivo. Quando il limite dell'intervallo di indici è incluso, le voci di indice che corrispondono esattamente ai criteri di ricerca sono incluse nell'intervallo.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRangeInstantDuration</p></td>
<td><p>Questa opzione richiede che l'intervallo di indici venga rimosso non appena è stato stabilito. Tutti gli altri aspetti dell'operazione restano invariati. Questa operazione è utile per verificare l'esistenza di voci di indice che corrispondono ai criteri di ricerca.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRangeRemove</p></td>
<td><p>Questa opzione richiede che un intervallo di indice esistente nel cursore venga annullato. Una volta annullato l'intervallo di indici, sarà possibile passare oltre la fine dell'intervallo di indici utilizzando <a href="gg294117(v=exchg.10).md">JetMove</a>. Se non è già attivo un intervallo di indici, <strong>JetSetIndexRange</strong> avrà esito negativo con JET_errInvalidOperation.</p>
<p>Quando si specifica questa opzione, tutte le altre opzioni vengono ignorate.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRangeUpperLimit</p></td>
<td><p>Se si utilizza questa opzione, la chiave di ricerca nel cursore rappresenta i criteri di ricerca per la voce di indice più vicina alla fine dell'indice che corrisponderà all'intervallo di indici. L'intervallo di indici verrà stabilito tra la posizione corrente del cursore e questa voce di indice, in modo che tutte le corrispondenze possano essere individuate procedendo in avanti sull'indice utilizzando <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MoveNext o un offset positivo.</p>
<p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine all'inizio dell'indice.</p>
<p>Se questa opzione viene omessa, la chiave di ricerca nel cursore rappresenta i criteri di ricerca per la voce di indice più vicina all'inizio dell'indice che corrisponderà all'intervallo di indici. L'intervallo di indici verrà stabilito tra la posizione corrente del cursore e questa voce di indice, in modo che tutte le corrispondenze possano essere rilevate tornando indietro sull'indice utilizzando <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MovePrevious o un offset negativo.</p>
<p>Non è significativo omettere questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine alla fine dell'indice.</p></td>
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
<td><p>Operazione riuscita.</p>
<p>Per <strong>JetSetIndexRange</strong>, ciò significa che un intervallo di indici esistente è stato annullato o che è presente almeno una voce di indice all'interno dell'intervallo di indice.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOperation</p></td>
<td><p>Questo errore viene restituito da <strong>JetSetIndexRange</strong> quando JET_bitRangeRemove è stato specificato e non è attivo alcun intervallo di indici.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade</p></td>
<td><p>Nessun tasto di ricerca corrente per il cursore. <strong>JetSetIndexRange</strong> richiede che il cursore disponga di una chiave di ricerca valida perché verrà utilizzata per i criteri di ricerca utilizzati per individuare le voci dell'indice.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>Nessun indice corrente per il cursore. Questo problema si verifica per <strong>JetSetIndexRange</strong> se il cursore si trova nell'indice cluster di una tabella, non è stato definito un indice primario. L'impostazione di un intervallo di indice su un indice di questo tipo non è supportata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Questo errore viene restituito da <strong>JetSetIndexRange</strong> per indicare che non sono presenti voci di indice nell'intervallo di indici.</p></td>
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
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, se viene specificato JET_bitRangeRemove, l'intervallo di indici attualmente in vigore viene annullato. Se JET_bitRangeRemove non è specificato e viene specificato JET_bitRangeInstantDuration, non è attivo alcun intervallo di indici. Se non viene specificato né JET_bitRangeRemove né JET_bitRangeInstantDuration, viene applicato un nuovo intervallo di indice. Questo intervallo di indici limita temporaneamente il set di voci di indice che il cursore può utilizzare [JetMove](./jetmove-function.md) a quelle a partire dalla voce di indice corrente e termina in corrispondenza della voce di indice corrispondente ai criteri di ricerca. La posizione del cursore rimarrà invariata. Se è stata creata una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata. Non si verificherà alcuna modifica allo stato del database.

In caso di errore, se non viene restituito JET_errNoCurrentRecord, non è attivo alcun intervallo di indici. Se viene restituito JET_errNoCurrentRecord, viene applicato un nuovo intervallo di indice. Questo intervallo di indici limita temporaneamente il set di voci di indice che il cursore può utilizzare [JetMove](./jetmove-function.md) a quelle a partire dalla voce di indice corrente e termina in corrispondenza della voce di indice corrispondente ai criteri di ricerca. La posizione del cursore rimarrà invariata. Se JET_errNoCurrentRecord è stato restituito ed è stata costruita una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata. Non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Un intervallo di indice è volatile e verrà annullato automaticamente se nel cursore viene eseguita una navigazione diversa da [JetMove](./jetmove-function.md) .

Gli intervalli di indice funzionano solo in una direzione. Se viene stabilito un limite superiore, viene impedito solo il movimento in diretta usando [JetMove](./jetmove-function.md) con JET_MoveNext o un offset positivo dopo che è stata raggiunta la fine dell'intervallo di indici. In questo caso è comunque possibile lasciare l'intervallo di indici utilizzando [JetMove](./jetmove-function.md) con JET_MovePrevious o un offset negativo. Una situazione analoga si verifica per un limite inferiore.

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
[JetMakeKey](./jetmakekey-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetIndexRange]()  
[JetStopService](./jetstopservice-function.md)
