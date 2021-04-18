---
description: 'Altre informazioni su: funzione JetIntersectIndexes'
title: Funzione JetIntersectIndexes
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305733"
---
# <a name="jetintersectindexes-function"></a>Funzione JetIntersectIndexes


_**Si applica a:** Windows | Windows Server_

## <a name="jetintersectindexes-function"></a>Funzione JetIntersectIndexes

La funzione **JetIntersectIndexes** calcola l'intersezione tra più set di voci di indice provenienti da indici secondari diversi nella stessa tabella. Questa operazione è utile per trovare il set di record in una tabella che corrisponde a due o più criteri che possono essere espressi utilizzando intervalli di indice.

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*rgindexrange*

Puntatore a una matrice di strutture di [JET_IndexRange](./jet-indexrange-structure.md) . Ogni struttura include una [JET_TABLEID](./jet-tableid.md) configurata per contenere uno degli intervalli di indice da intersecare. Per ulteriori informazioni, vedere [JET_IndexRange](./jet-indexrange-structure.md).

*cindexrange*

Numero di strutture di [JET_IndexRange](./jet-indexrange-structure.md) nella matrice contenuta nel parametro *rgindexrange* .

*precordore*

Puntatore a una struttura [JET_RECORDLIST](./jet-recordlist-structure.md) . Questa struttura verrà popolata con informazioni sufficienti per attraversare la tabella temporanea con i risultati di **JetIntersectIndexes**.

Buffer di output che riceve una struttura [JET_RECORDLIST](./jet-recordlist-structure.md) . La struttura contiene una descrizione del set di risultati dell'intersezione.

*grbit*

Riservato per utilizzi futuri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE, vedere [errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md) e [parametri di gestione degli](./error-handling-parameters.md)errori.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una delle opzioni richieste non è valida, è stata usata in modo errato o non è stata implementata.</p>
<p>Questo errore viene restituito da <strong>JetIntersectIndexes</strong> quando:</p>
<p>Il <em>grbit</em> contenuto nella struttura <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> a cui punta qualsiasi elemento nella matrice <em>rgindexrange</em> non è uguale a JET_bitRecordInIndex.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o un valore non coerente se combinato con il valore di un altro parametro.</p>
<p>Questo errore viene restituito da <strong>JetIntersectIndexes</strong> per i motivi seguenti:</p>
<ul>
<li><p>Il parametro <em>precordname</em> è null.</p></li>
<li><p>Il membro <strong>cbStruct</strong> della struttura <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> specificata nel parametro <em>precordon</em> non è uguale alla dimensione della struttura di <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> .</p></li>
<li><p>Il parametro <em>cindexrange</em> è zero.</p></li>
<li><p>Il parametro <em>cindexrange</em> è maggiore di 64.</p></li>
<li><p>Il membro <strong>cbStruct</strong> per qualsiasi elemento nella matrice specificata dal parametro <em>rgindexrange</em> non è uguale alla dimensione della struttura <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> .</p></li>
<li><p>Gli elementi nella matrice <em>rgindexrange</em> contengono <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s da tabelle diverse.</p></li>
<li><p>Un elemento nella matrice <em>rgindexrange</em> contiene un <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> che non è posizionato in corrispondenza di un indice secondario.</p></li>
<li><p>Uno o più elementi nella matrice <em>rgindexrange</em> contengono <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s posizionati nello stesso indice secondario.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</p>
<p>Questo errore non viene restituito in tutte le circostanze. Gli handle vengono convalidati solo in base al massimo sforzo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Operazione non riuscita perché il motore non è stato in grado di allocare le risorse necessarie per aprire un nuovo cursore. Le risorse del cursore vengono configurate chiamando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxCursors</em> specificato nel parametro <em>Paramid</em> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</p>
<p><strong>JetIntersectIndexes</strong> può restituire JET_errOutOfMemory se lo spazio degli indirizzi del processo host diventa troppo frammentato. Il gestore tabelle temporanee allocherà sempre un blocco di spazio degli indirizzi pari a 1 MB per ogni tabella temporanea creata indipendentemente dalla quantità di dati da archiviare. <strong>JetIntersectIndexes</strong> creerà una tabella temporanea per ogni <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> specificato nel parametro <em>rgindexrange</em> e una tabella temporanea per l'output in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è consentito usare la stessa sessione da più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>L'operazione non è riuscita perché il motore non è stato in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella. Il numero di indici il cui schema può essere memorizzato nella cache viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxOpenTables</em> specificato nel parametro <em>Paramid</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella. Il numero di tabelle il cui schema può essere memorizzato nella cache viene configurato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxOpenTables</em> specificato nel parametro <em>Paramid</em> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea. Le risorse della tabella temporanea vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con JET_paramMaxTemporaryTables specificato nel parametro <em>Paramid</em> .</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, viene restituita una nuova tabella temporanea che contiene i segnalibri dei record che corrispondono ai criteri rappresentati da ognuna delle descrizioni degli intervalli degli indici di input.

In caso di errore, la tabella temporanea contenente i risultati non verrà creata. Lo stato del database temporaneo può essere modificato. Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato. È possibile modificare la posizione corrente del [JET_TABLEID](./jet-tableid.md)s fornita a questa funzione.

#### <a name="remarks"></a>Commenti

**JetIntersectIndexes** può essere usato per filtrare in modo efficiente i record in una tabella in base a più criteri se tali criteri possono essere espressi in termini di indici secondari sulla tabella. Si supponga, ad esempio, di disporre di una tabella di grandi dimensioni contenente persone. La tabella può includere colonne per l'ID utente, il nome, il cognome e così via. Si supponga che ciascuna di queste colonne venga indicizzata separatamente e che l'indice primario della tabella sia superiore all'ID utente. Se si desidera trovare tutti gli utenti il cui nome inizia con un oggetto e il cui cognome inizia con G, è necessario eseguire i passaggi seguenti:

1.  Aprire un nuovo cursore sulla tabella e impostare tale cursore per utilizzare l'indice sulla colonna "First Name". Configurare quindi un intervallo di indici per tutte le persone il cui "nome" inizia con "A" e compilare un [JET_IndexRange](./jet-indexrange-structure.md) struct che contiene il cursore.

2.  Ripetere il passaggio 1 con un nuovo cursore sull'indice "Last Name" per tutte le persone il cui "cognome" è stato avviato con "G".

3.  Passare questi criteri a **JetIntersectIndexes** per calcolare il risultato in una tabella temporanea.

4.  Attraversare la tabella temporanea e recuperare tutti i record che passano i criteri tramite segnalibro.

La tabella temporanea contenente il set di risultati è una tabella semplice con una colonna che contiene il segnalibro di ogni record che ha superato tutti i criteri utilizzati per calcolare l'intersezione. Il set di risultati viene ordinato in base allo stesso ordine dell'indice primario e non contiene voci duplicate. L'applicazione può enumerare i risultati dell'intersezione enumerando le righe nella tabella temporanea, recuperando il segnalibro per ogni risultato utilizzando [JetRetrieveColumn](./jetretrievecolumn-function.md)e quindi visitando il record nel database chiamando [JetGotoBookmark](./jetgotobookmark-function.md) con tale segnalibro su un cursore posizionato sull'indice primario.

La tabella temporanea restituita da **JetIntersectIndexes** può essere analizzata solo in avanti. Deve anche essere chiuso tramite [JetCloseTable](./jetclosetable-function.md) al termine dell'analisi. Per ulteriori informazioni sulle tabelle temporanee e sul relativo funzionamento, vedere [JetOpenTemporaryTable](./jetopentemporarytable-function.md).

**JetIntersectIndexes** è in genere un modo efficiente e pratico per filtrare i record in base a più criteri indicizzati. Tuttavia, esistono alcuni suggerimenti importanti da seguire per ottimizzare l'utilità di questa funzionalità. Se si sa che uno dei criteri è talmente restrittivo che l'intervallo di indici risultante ha pochissimi record, probabilmente è preferibile semplicemente esaminare l'intervallo di indici e filtrare i record a livello di applicazione. Inoltre, se si è certi di disporre di criteri molto meno restrittivi rispetto ad altri criteri nell'intersezione, è possibile prendere in considerazione l'eliminazione di criteri molto meno restrittivi dall'intersezione. Infine, se si sa che uno dei criteri non è strettamente restrittivo, in modo che l'intervallo di indici risultante sia quasi così elevato rispetto all'indice primario, è improbabile che l'intersezione con tale intervallo possa trarre vantaggio (ridurre le dimensioni del set di risultati). In tutti i casi, è necessario selezionare i criteri in modo che consentano il minor numero possibile di voci di indice nell'input e generano il set più specifico di segnalibri nell'output per ottenere le massime prestazioni.

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
[JET_IndexRange](./jet-indexrange-structure.md)  
[JET_RECORDLIST](./jet-recordlist-structure.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
