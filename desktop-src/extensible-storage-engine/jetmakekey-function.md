---
description: 'Altre informazioni su: funzione JetMakeKey'
title: Funzione JetMakeKey
TOCTitle: JetMakeKey Function
ms:assetid: 8c1cff2f-2f24-4990-a9d8-fb4f822e50b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269329(v=EXCHG.10)
ms:contentKeyID: 32765619
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMakeKey
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3d121ed83f096baad249aab8677bb9f5e72e301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233355"
---
# <a name="jetmakekey-function"></a>Funzione JetMakeKey


_**Si applica a:** Windows | Windows Server_

## <a name="jetmakekey-function"></a>Funzione JetMakeKey

La funzione **JetMakeKey** costruisce chiavi di ricerca che possono essere usate per trovare un set di voci in un indice in base ad alcuni criteri di ricerca semplici sui rispettivi valori della colonna chiave. Una chiave di ricerca è anche una delle proprietà intrinseche di un cursore e viene utilizzata dalle operazioni [JetSeek](./jetseek-function.md) e [JetSetIndexRange](./jetsetindexrange-function.md) per individuare le voci di indice corrispondenti a questi criteri di ricerca nell'indice corrente del cursore. Una chiave di ricerca completa è incorporata in una serie di chiamate **JetMakeKey** , in cui ogni chiamata viene utilizzata per caricare il valore della colonna chiave successiva dell'indice corrente di un cursore. È anche possibile caricare una chiave di ricerca costruita in precedenza che è stata recuperata dal cursore usando [JetRetrieveKey](./jetretrievekey-function.md).

```cpp
    JET_ERR JET_API JetMakeKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*pvData*

Buffer di input contenente i dati della colonna chiave corrente dell'indice corrente del cursore per il quale viene costruita la chiave di ricerca.

Il tipo di dati dei dati della colonna nel buffer di input deve corrispondere esattamente al tipo di dati e ad altre proprietà della definizione di colonna della colonna chiave corrente. Non viene eseguita alcuna coercizione dei tipi sui dati della colonna.

Se JET_bitNormalizedKey viene specificato nel parametro *grbit* , il buffer di input deve contenere una chiave di ricerca costruita in precedenza. Tali chiavi vengono ottenute utilizzando una chiamata a [JetRetrieveKey](./jetretrievekey-function.md).

*cbData*

Dimensioni in byte dei dati della colonna forniti nel buffer di input.

Se JET_bitNormalizedKey viene specificato nel parametro *grbit* , si tratta della dimensione della chiave di ricerca fornita nel buffer di input.

Se le dimensioni dei dati della colonna sono pari a zero, il contenuto del buffer di input viene ignorato. Se JET_bitKeyDataZeroLength viene specificato nel parametro *grbit* e la colonna chiave corrente dell'indice corrente del cursore è una colonna a lunghezza variabile, i dati della colonna di input vengono considerati come valori di lunghezza zero. In caso contrario, si presume che i dati della colonna di input siano un valore NULL.

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
<td><p>JET_bitFullColumnEndLimit</p></td>
<td><p>La chiave di ricerca deve essere costruita in modo tale che tutte le colonne chiave che si trovano dopo la colonna chiave corrente siano considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare la corrispondenza con le voci di indice con le seguenti:</p>
<ul>
<li><p>Valori esatti della colonna specificati per questa colonna chiave e per tutte le colonne chiave precedenti.</p></li>
<li><p>Tutti i valori di colonna necessari per le colonne chiave successive.</p></li>
</ul>
<p>Questa opzione deve essere utilizzata per la compilazione di chiavi di ricerca con caratteri jolly da utilizzare per la ricerca di voci di indice più vicine alla fine di un indice. La fine dell'indice è la voce di indice trovata quando si passa all'ultimo record in tale indice. La fine dell'indice non è uguale all'estremità superiore dell'indice, che può variare a seconda dell'ordinamento delle colonne chiave nell'indice.</p>
<p>Questa opzione è disponibile solo in Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JETbitFullColumnStartLimit</p></td>
<td><p>La chiave di ricerca deve essere costruita in modo tale che tutte le colonne chiave che vengono dopo la colonna chiave corrente devono essere considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare la corrispondenza con le voci di indice con le seguenti:</p>
<ul>
<li><p>Valori esatti della colonna specificati per questa colonna chiave e per tutte le colonne chiave precedenti.</p></li>
<li><p>Tutti i valori di colonna necessari per le colonne chiave successive.</p></li>
</ul>
<p>Questa opzione deve essere utilizzata per la compilazione di chiavi di ricerca con caratteri jolly da utilizzare per la ricerca di voci di indice più vicine all'inizio di un indice. L'inizio dell'indice è la voce di indice trovata quando si passa al primo record in tale indice. L'inizio dell'indice non corrisponde alla parte inferiore dell'indice, che può variare a seconda del tipo di ordinamento delle colonne chiave nell'indice.</p>
<p>Questa opzione è disponibile solo in Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitKeyDataZeroLength</p></td>
<td><p>Se la dimensione del buffer di input è zero e la colonna chiave corrente è una colonna a lunghezza variabile, questa opzione indica che il buffer di input contiene un valore di lunghezza zero. In caso contrario, una dimensione del buffer di input pari a zero indicherebbe un valore NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNewKey</p></td>
<td><p>È necessario costruire una nuova chiave di ricerca. Qualsiasi chiave di ricerca precedentemente esistente viene eliminata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitNormalizedKey</p></td>
<td><p>Quando si specifica questa opzione, tutte le altre opzioni vengono ignorate, qualsiasi chiave di ricerca già esistente viene eliminata e il contenuto del buffer di input viene caricato come nuova chiave di ricerca.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitPartialColumnEndLimit</p></td>
<td><p>La chiave di ricerca deve essere costruita in modo che la colonna chiave corrente sia considerata come un carattere jolly di prefisso e che tutte le colonne chiave successive alla colonna chiave corrente siano considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare la corrispondenza con le voci di indice con le seguenti:</p>
<ul>
<li><p>Valori esatti della colonna specificati per questa colonna chiave e per tutte le colonne chiave precedenti.</p></li>
<li><p>Tutti i valori di colonna necessari per le colonne chiave successive.</p></li>
</ul>
<p>Questa opzione deve essere utilizzata per la compilazione di chiavi di ricerca con caratteri jolly da utilizzare per la ricerca di voci di indice più vicine alla fine di un indice. La fine dell'indice è la voce di indice trovata quando si passa all'ultimo record in tale indice. La fine dell'indice non è uguale all'estremità superiore dell'indice, che può variare a seconda dell'ordinamento delle colonne chiave nell'indice.</p>
<p>Questa opzione non può essere utilizzata quando la colonna chiave corrente non è una colonna di testo o una colonna binaria variabile. L'operazione avrà esito negativo con JET_errInvalidgrbit se si tenta di eseguire questa operazione.</p>
<p>Questa opzione è disponibile solo in Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitPartialColumnStartLimit</p></td>
<td><p>Questa opzione indica che la chiave di ricerca deve essere costruita in modo tale che la colonna chiave corrente venga considerata come un carattere jolly di prefisso e che tutte le colonne chiave che preentrano nella colonna chiave corrente siano considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare la corrispondenza con le voci di indice con le seguenti:</p>
<ul>
<li><p>Valori esatti della colonna specificati per questa colonna chiave e per tutte le colonne chiave precedenti.</p></li>
<li><p>Tutti i valori di colonna necessari per le colonne chiave successive.</p></li>
</ul>
<p>Questa opzione deve essere utilizzata per la compilazione di chiavi di ricerca con caratteri jolly da utilizzare per la ricerca di voci di indice più vicine all'inizio di un indice. L'inizio dell'indice è la voce di indice trovata quando si passa al primo record in tale indice. L'inizio dell'indice non corrisponde alla parte inferiore dell'indice, che può variare a seconda del tipo di ordinamento delle colonne chiave nell'indice.</p>
<p>Questa opzione non può essere utilizzata quando la colonna chiave corrente non è una colonna di testo o una colonna binaria variabile. L'operazione avrà esito negativo con JET_errInvalidgrbit se si tenta di eseguire questa operazione.</p>
<p>Questa opzione è disponibile solo in Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStrLimit</p></td>
<td><p>Questa opzione indica che la chiave di ricerca deve essere costruita in modo tale che tutte le colonne chiave che vengono dopo la colonna chiave corrente devono essere considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare la corrispondenza con le voci di indice con le seguenti:</p>
<ul>
<li><p>Valori esatti della colonna specificati per questa colonna chiave e per tutte le colonne chiave precedenti.</p></li>
<li><p>Tutti i valori di colonna necessari per le colonne chiave successive.</p></li>
</ul>
<p>Questa opzione deve essere utilizzata per la compilazione di chiavi di ricerca con caratteri jolly da utilizzare per la ricerca di voci di indice più vicine alla fine di un indice. La fine dell'indice è la voce di indice trovata quando si passa all'ultimo record in tale indice. La fine dell'indice non è uguale all'estremità superiore dell'indice, che può variare a seconda dell'ordinamento delle colonne chiave nell'indice.</p>
<p>Quando questa opzione viene specificata in combinazione con JET_bitSubStrLimit e la colonna chiave corrente è una colonna di testo, questa opzione verrà ignorata. Questo comportamento consente di dedurre il tipo della colonna chiave corrente quando si compila la chiave di ricerca.</p>
<p>Se si desidera compilare una chiave di ricerca simile per l'inizio di un indice, è necessario effettuare una chiamata analoga a <strong>JetMakeKey</strong> per l'ultima colonna chiave che non è un carattere jolly, ma senza alcuna opzione con caratteri jolly specificata. La chiave di ricerca si trova quindi nello stato appropriato da usare per una ricerca di questo tipo. Questa operazione è analoga all'uso di JET_bitFullColumnStartLimit, ad eccezione del fatto che la chiave di ricerca non è stata completata in modo corretto, perché si trova dopo l'uso di un'opzione con caratteri jolly.</p>
<p>Questa opzione è stata deprecata per Windows XP e versioni successive per risolvere questa semantica scomoda. È necessario utilizzare JET_bitFullColumnStartLimit e JET_bitFullColumnEndLimit laddove possibile.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSubStrLimit</p></td>
<td><p>Questa opzione indica che la chiave di ricerca deve essere costruita in modo tale che la colonna chiave corrente venga considerata come un carattere jolly di prefisso e che tutte le colonne chiave che preentrano nella colonna chiave corrente siano considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare la corrispondenza con le voci di indice con le seguenti:</p>
<ul>
<li><p>Valori esatti della colonna specificati per tutte le colonne chiave precedenti.</p></li>
<li><p>Dati della colonna specificati come prefisso del valore della colonna chiave corrente.</p></li>
<li><p>Qualsiasi valore di colonna per le colonne chiave successive.</p></li>
</ul>
<p>Questa opzione deve essere utilizzata per la compilazione di chiavi di ricerca con caratteri jolly da utilizzare per la ricerca di voci di indice più vicine alla fine di un indice. La fine dell'indice è la voce di indice trovata quando si passa all'ultimo record in tale indice. La fine dell'indice non è uguale all'estremità superiore dell'indice, che può variare a seconda dell'ordinamento delle colonne chiave nell'indice.</p>
<p>Quando questa opzione viene specificata in combinazione con JET_bitStrLimit e la colonna chiave corrente è una colonna di testo, questa opzione avrà la precedenza. Questa opzione viene ignorata quando la colonna chiave corrente non è una colonna di testo. Questo comportamento consente di dedurre il tipo della colonna chiave corrente quando si compila la chiave di ricerca.</p>
<p>Se si desidera compilare una chiave di ricerca simile per l'inizio di un indice, è necessario effettuare una chiamata analoga a <strong>JetMakeKey</strong> per la colonna chiave che deve essere il carattere jolly del prefisso, ma senza che sia stata specificata alcuna opzione con caratteri jolly. La chiave di ricerca si trova quindi nello stato appropriato da usare per una ricerca di questo tipo. Questa operazione è analoga all'uso di JET_bitPartialColumnStartLimit, ad eccezione del fatto che la chiave di ricerca non è stata completata in modo corretto, perché si trova dopo l'uso di un'opzione con caratteri jolly.</p>
<p>Questa opzione è stata deprecata per Windows XP e versioni successive per risolvere questa semantica scomoda. In alternativa, è consigliabile usare JET_bitPartialColumnStartLimit e JET_bitPartialColumnEndLimit, quando possibile.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesKeyTooSmall</p></td>
<td><p>I dati della colonna specificati erano troppo piccoli per compilare una chiave valida per l'indice corrente perché tale indice è un indice di tupla e le dimensioni minime della tupla erano maggiori dei dati della colonna specificati. Per ulteriori informazioni sugli indici di tuple, vedere <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> . Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>I dati della colonna specificati non corrispondono alle dimensioni richieste dalla definizione di colonna. Questo problema può verificarsi se il tipo di dati della colonna è intrinsecamente di una determinata dimensione. Questo problema può verificarsi anche se il tipo di dati della colonna non è intrinsecamente una determinata dimensione, ma la definizione della colonna ne dichiara la lunghezza fissa. Un'eccezione è che questo errore non si verifica quando vengono forniti dati troppo piccoli per una colonna di testo a lunghezza fissa, perché i dati mancanti verranno automaticamente riempiti con spazi. Una seconda eccezione è che questo errore non si verifica quando vengono forniti dati troppo piccoli per una colonna binaria a lunghezza fissa, perché i dati mancanti verranno automaticamente riempiti con zeri.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una delle opzioni richieste non è valida, è stata usata in modo non valido o non è stata implementata. Questo problema può verificarsi per <strong>JetMakeKey</strong> quando:</p>
<ul>
<li><p>Vengono specificati JET_bitPartialColumnStartLimit o JET_bitPartialColumnEndLimit e la colonna chiave corrispondente non è una colonna di testo e non è una colonna binaria di lunghezza variabile. Questo caso si verifica solo in Windows XP e versioni successive.</p></li>
<li><p>Si è tentato di utilizzare più di una delle seguenti opzioni insieme: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit e JET_bitFullColumnEndLimit. Questo caso si verifica solo in Windows XP e versioni successive.</p></li>
<li><p>Viene effettuato un tentativo di utilizzare JET_bitStrLimit o JET_bitSubStrLimit quando viene utilizzata una delle opzioni seguenti: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit e JET_bitFullColumnEndLimit. Questo caso si verifica solo in Windows XP e versioni successive.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</p>
<p>Questo problema può verificarsi per <strong>JetMakeKey</strong> quando è stato specificato JET_bitNormalizedKey e il valore specificato nel buffer di input è troppo grande per essere una chiave di ricerca valida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyIsMade</p></td>
<td><p>I dati della colonna forniti a <strong>JetMakeKey</strong> sono stati rifiutati perché i dati della colonna sono già stati specificati per tutte le colonne chiave dell'indice corrente. Questa operazione può essere eseguita in tre modi. Il primo consiste nel fare in modo che i dati della colonna vengano specificati per ogni colonna chiave nell'indice corrente. Il secondo consiste nel caso in cui i dati della colonna siano stati specificati per almeno una colonna chiave ed è stata scelta un'opzione con caratteri jolly per l'ultima chiamata. Il terzo metodo è se una chiave di ricerca costruita in precedenza è stata fornita utilizzando JET_bitNormalizedKey, che copre tutte le colonne chiave.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade</p></td>
<td><p>Nessun tasto di ricerca corrente per il cursore. Questa operazione viene eseguita per <strong>JetMakeKey</strong> se non si specifica JET_bitNewKey e non è stata creata una chiave di ricerca per questo cursore utilizzando una chiamata precedente a <strong>JetMakeKey</strong>. La chiave di ricerca verrà eliminata da una chiamata precedente a qualsiasi API di spostamento sul cursore diverso da <a href="gg294117(v=exchg.10).md">JetMove</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>Nessun indice corrente per il cursore. Questa operazione viene eseguita per <strong>JetMakeKey</strong> se il cursore si trova nell'indice cluster di una tabella, non è stato definito un indice primario e non è stato specificato JET_bitNormalizedKey. Non è possibile costruire una chiave di ricerca se il cursore si trova in un indice che non contiene colonne chiave, a meno che non venga fornita una chiave di ricerca costruita in precedenza.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, se non sono stati specificati JET_bitNormalizedKey e JET_bitNewKey, la chiave di ricerca sarà compilata in base ai criteri di ricerca di una colonna chiave nell'indice corrente. Se JET_bitNormalizedKey non è stato specificato ed è stato specificato JET_bitNewKey, qualsiasi chiave di ricerca precedentemente esistente è stata eliminata e ne è stata creata una nuova in base ai criteri di ricerca per la prima colonna chiave dell'indice corrente. Se JET_bitNormalizedKey è stato specificato, qualsiasi chiave di ricerca precedentemente esistente è stata eliminata e ne è stata caricata una nuova dal buffer di input. In ogni caso, non si verificherà alcuna modifica allo stato del database.

In caso di errore, se è stato specificato JET_bitNormalizedKey o JET_bitNewKey, lo stato della chiave di ricerca non è definito. Se non si specifica né JET_bitNormalizedKey né JET_bitNewKey, non si verificherà alcuna modifica allo stato della chiave di ricerca. In ogni caso, non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Le chiavi devono essere considerate come blocchi opachi di dati. Non è necessario effettuare alcun tentativo di sfruttare la struttura interna di questi dati. Tuttavia, di seguito sono riportate informazioni su tutte le chiavi di ESENT:

  - Le chiavi possono essere confrontate tra loro utilizzando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire l'ordine relativo nell'indice di origine sulla tabella delle voci dell'indice di origine.

  - Non è significativo confrontare le chiavi di voci di indice da indici diversi tra loro.

  - Una chiave è sempre minore o uguale a JET_cbKeyMost (255) byte di lunghezza prima di Windows Vista. In Windows Vista e versioni successive, le chiavi possono essere più grandi. La dimensione massima di una chiave è uguale al valore corrente di JET_paramKeyMost.

I tasti di ricerca possono avere un byte più lungo se è stata usata un'opzione con caratteri jolly. In tal caso, la chiave di ricerca sarà JET_cbLimitKeyMost (256) byte per le versioni precedenti a Windows Vista e JET_paramKeyMost + 1 byte per Windows Vista e versioni successive.

Questa dimensione massima della chiave è molto importante. Ogni volta che è presente una voce di indice con valori di colonna sufficientemente grandi da provocare la generazione di una chiave per tale indice che altrimenti sarebbe maggiore di quella massima, la chiave viene troncata automaticamente a tale dimensione massima. Ciò provoca due effetti:

  - Per le voci in un indice univoco, le voci che altrimenti sarebbero univoche verranno dichiarate come duplicati.

  - Per le voci in tutti gli indici, il troncamento delle chiavi provocherà le voci di indice che altrimenti non corrisponderanno ai criteri di ricerca di una chiave di ricerca specificata da dichiarare come corrispondenze.

Le applicazioni devono prevedere questo troncamento ed evitare o compensare gli effetti. In Windows Vista è stato aggiunto un nuovo flag di indice, JET_bitIndexDisallowTruncation, che consente alle applicazioni di evitare i troncamenti di chiave in modo più semplice. Per ulteriori informazioni su questa opzione di indicizzazione, vedere la struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

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
[JetCreateIndex](./jetcreateindex-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
