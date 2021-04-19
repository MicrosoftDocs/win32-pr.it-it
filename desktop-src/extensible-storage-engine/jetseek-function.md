---
description: 'Altre informazioni su: funzione JetSeek'
title: JetSeek (funzione)
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318082"
---
# <a name="jetseek-function"></a>JetSeek (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetseek-function"></a>JetSeek (funzione)

La funzione **JetSeek** posiziona in modo efficiente un cursore in una voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e alla disuguaglianza specificata. È necessario che una chiave di ricerca sia stata costruita in precedenza usando [JetMakeKey](./jetmakekey-function.md).

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per questa chiamata. *Grbit* deve essere diverso da zero e deve includere uno o più dei valori elencati nella tabella seguente.

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
<td><p>JET_bitCheckUniqueness</p></td>
<td><p>Viene restituito un codice di errore speciale, JET_wrnUniqueKey, se può essere determinato in modo economico che esiste esattamente una voce di indice che corrisponde alla chiave di ricerca.</p>
<p>Questa opzione viene ignorata a meno che non sia specificato anche JET_bitSeekEQ.</p>
<p>Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekEQ</p></td>
<td><p>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice che corrisponde esattamente alla chiave di ricerca. L'inizio dell'indice è la voce di indice trovata quando si passa al primo record in tale indice. L'inizio dell'indice non corrisponde alla parte inferiore dell'indice, che può variare a seconda del tipo di ordinamento delle colonne chiave nell'indice.</p>
<p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSeekGE</p></td>
<td><p>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice che è maggiore o uguale a una voce di indice che corrisponde esattamente ai criteri di ricerca. L'inizio dell'indice è la voce di indice trovata quando si passa al primo record in tale indice. L'inizio dell'indice non corrisponde alla parte inferiore dell'indice, che può variare a seconda del tipo di ordinamento delle colonne chiave nell'indice.</p>
<p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine alla fine dell'indice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekGT</p></td>
<td><p>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice maggiore di una voce di indice che corrisponde esattamente ai criteri di ricerca. L'inizio dell'indice è la voce di indice trovata quando si passa al primo record in tale indice. L'inizio dell'indice non corrisponde alla parte inferiore dell'indice, che può variare a seconda del tipo di ordinamento delle colonne chiave nell'indice.</p>
<p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine all'inizio dell'indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSeekLE</p></td>
<td><p>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina alla fine dell'indice che è minore o uguale a una voce di indice che corrisponde esattamente ai criteri di ricerca. La fine dell'indice è la voce di indice trovata quando si passa all'ultimo record in tale indice. La fine dell'indice non è uguale all'estremità superiore dell'indice, che può variare a seconda dell'ordinamento delle colonne chiave nell'indice.</p>
<p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine all'inizio dell'indice.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekLT</p></td>
<td><p>Il cursore verrà posizionato in corrispondenza della voce di indice più vicina alla fine dell'indice inferiore a una voce di indice che corrisponde esattamente ai criteri di ricerca. La fine dell'indice è la voce di indice trovata quando si passa all'ultimo record in tale indice. La fine dell'indice non è uguale all'estremità superiore dell'indice, che può variare a seconda dell'ordinamento delle colonne chiave nell'indice.</p>
<p>Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine alla fine dell'indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIndexRange</p></td>
<td><p>Un intervallo di indici verrà automaticamente configurato per tutte le chiavi che corrispondono esattamente alla chiave di ricerca. L'intervallo di indici risultante è identico a uno che altrimenti sarebbe stato creato da una chiamata a <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> con le opzioni JET_bitRangeInclusive e JET_bitRangeUpperLimit. Per ulteriori informazioni, vedere <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> .</p>
<p>Si tratta di un metodo pratico per individuare tutte le voci di indice che corrispondono agli stessi criteri di ricerca.</p>
<p>Questa opzione viene ignorata a meno che non sia specificato anche JET_bitSeekEQ.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione consente il ritorno di qualsiasi [JET_ERRs](./jet-err.md) definito in questa API. Per altre informazioni sugli errori di Jet, vedere [errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md) e [parametri di gestione degli](./error-handling-parameters.md)errori.

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
<p>Per <strong>JetSeek</strong>, ciò significa che è stata trovata una voce di indice che corrisponde esattamente ai criteri di ricerca.</p></td>
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
<td><p>JET_errKeyNotMade</p></td>
<td><p>Nessun tasto di ricerca corrente per il cursore. <strong>JetSeek</strong> richiede che il cursore disponga di una chiave di ricerca valida perché verrà utilizzata per i criteri di ricerca utilizzati per individuare le voci dell'indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNotFound</p></td>
<td><p>Non è stata trovata alcuna voce di indice corrispondente ai criteri di ricerca.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSeekNotEqual</p></td>
<td><p>È stata trovata una voce di indice corrispondente ai criteri di ricerca. Tale voce di indice, tuttavia, non era una corrispondenza esatta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnUniqueKey</p></td>
<td><p>È stata trovata esattamente una voce di indice che corrisponde esattamente ai criteri di ricerca. Questo errore viene restituito solo se JET_bitSeekCheckUniqueness è stato specificato ed è stato economico determinare che la voce di indice corrispondente era l'unica voce di indice che corrisponde esattamente ai criteri di ricerca.</p>
<p>Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice corrispondente ai criteri di ricerca. Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato. Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato. Se è stata creata una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata. Non si verificherà alcuna modifica allo stato del database. Quando più voci di indice hanno lo stesso valore, la voce più vicina all'inizio dell'indice è sempre selezionata.

In caso di errore, la posizione del cursore rimarrà invariata a meno che non venga restituito JET_errRecordNotFound. In tal caso, il cursore verrà posizionato in corrispondenza del punto in cui la voce di indice corrispondente ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e nella disuguaglianza specificata sarebbe stata. Il cursore può essere spostato in relazione a tale posizione, ma non è ancora presente in una voce di indice valida. Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato. Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato. Se è stata creata una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata. Non si verificherà alcuna modifica allo stato del database.

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
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
