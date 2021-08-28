---
description: Altre informazioni sulla funzione JetMakeKey
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
ms.openlocfilehash: 1b0a7300a312bf5f34c2a60cc6ed3b3c95879dde
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983404"
---
# <a name="jetmakekey-function"></a>Funzione JetMakeKey


_**Si applica a:** Windows | Windows Server_

## <a name="jetmakekey-function"></a>Funzione JetMakeKey

La **funzione JetMakeKey** costruisce chiavi di ricerca che possono quindi essere usate per trovare un set di voci in un indice da alcuni semplici criteri di ricerca sui valori delle colonne chiave. Una chiave di ricerca è anche una delle proprietà intrinseche di un cursore e viene usata dalle operazioni [JetSeek](./jetseek-function.md) e [JetSetIndexRange](./jetsetindexrange-function.md) per individuare le voci di indice corrispondenti a questi criteri di ricerca nell'indice corrente del cursore. Una chiave di ricerca completa è compilata in una serie di chiamate **JetMakeKey** in cui ogni chiamata viene usata per caricare il valore della colonna chiave successiva dell'indice corrente di un cursore. È anche possibile caricare una chiave di ricerca costruita in precedenza recuperata dal cursore usando [JetRetrieveKey](./jetretrievekey-function.md).

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

*tableid*

Cursore da utilizzare per questa chiamata.

*pvData*

Buffer di input contenente i dati della colonna chiave corrente dell'indice corrente del cursore per cui viene costruita la chiave di ricerca.

Il tipo di dati dei dati della colonna nel buffer di input deve corrispondere esattamente al tipo di dati e ad altre proprietà della definizione di colonna della colonna chiave corrente. Non viene eseguita alcuna coercizione di tipo sui dati della colonna.

Se JET_bitNormalizedKey specificato nel parametro *grbit,* il buffer di input deve contenere una chiave di ricerca costruita in precedenza. Tali chiavi vengono ottenute usando una chiamata a [JetRetrieveKey](./jetretrievekey-function.md).

*cbData*

Dimensione in byte dei dati della colonna forniti nel buffer di input.

Se JET_bitNormalizedKey specificato nel *parametro grbit,* si tratta delle dimensioni della chiave di ricerca specificata nel buffer di input.

Se le dimensioni dei dati della colonna sono pari a zero, il contenuto del buffer di input viene ignorato. Se JET_bitKeyDataZeroLength specificato nel *parametro grbit* e la colonna chiave corrente dell'indice corrente del cursore è una colonna a lunghezza variabile, si presuppone che i dati della colonna di input siano un valore di lunghezza zero. In caso contrario, si presuppone che i dati della colonna di input siano un valore NULL.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitFullColumnEndLimit</p> | <p>La chiave di ricerca deve essere costruita in modo che tutte le colonne chiave che vengono dopo la colonna chiave corrente siano considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare corrispondenze tra le voci di indice con gli elementi seguenti:</p><ul><li><p>Valori di colonna esatti forniti per questa colonna chiave e per tutte le colonne chiave precedenti.</p></li><li><p>Tutti i valori di colonna necessari per le colonne chiave successive.</p></li></ul><p>Questa opzione deve essere usata quando si compilano chiavi di ricerca con caratteri jolly da usare per trovare le voci di indice più vicine alla fine di un indice. La fine dell'indice è la voce di indice trovata durante lo spostamento all'ultimo record di tale indice. La fine dell'indice non corrisponde all'estremità superiore dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Questa opzione è disponibile solo in Windows XP e versioni successive.</p> | 
| <p>JETbitFullColumnStartLimit</p> | <p>La chiave di ricerca deve essere costruita in modo che tutte le colonne chiave che vengono dopo la colonna chiave corrente siano considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare corrispondenze tra le voci di indice con gli elementi seguenti:</p><ul><li><p>Valori di colonna esatti forniti per questa colonna chiave e per tutte le colonne chiave precedenti.</p></li><li><p>Tutti i valori di colonna necessari per le colonne chiave successive.</p></li></ul><p>Questa opzione deve essere usata quando si compilano chiavi di ricerca con caratteri jolly da usare per trovare le voci di indice più vicine all'inizio di un indice. L'inizio dell'indice è la voce di indice trovata durante lo spostamento al primo record in tale indice. L'inizio dell'indice non corrisponde all'estremità bassa dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Questa opzione è disponibile solo in Windows XP e versioni successive.</p> | 
| <p>JET_bitKeyDataZeroLength</p> | <p>Se la dimensione del buffer di input è zero e la colonna chiave corrente è una colonna a lunghezza variabile, questa opzione indica che il buffer di input contiene un valore di lunghezza zero. In caso contrario, una dimensione del buffer di input pari a zero indicherà un valore NULL.</p> | 
| <p>JET_bitNewKey</p> | <p>Deve essere costruita una nuova chiave di ricerca. Qualsiasi chiave di ricerca esistente in precedenza viene eliminata.</p> | 
| <p>JET_bitNormalizedKey</p> | <p>Quando si specifica questa opzione, tutte le altre opzioni vengono ignorate, qualsiasi chiave di ricerca esistente in precedenza viene eliminata e il contenuto del buffer di input viene caricato come nuova chiave di ricerca.</p> | 
| <p>JET_bitPartialColumnEndLimit</p> | <p>La chiave di ricerca deve essere costruita in modo che la colonna chiave corrente sia considerata un carattere jolly di prefisso e che tutte le colonne chiave che vengono dopo la colonna chiave corrente siano considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare corrispondenze tra le voci di indice con gli elementi seguenti:</p><ul><li><p>Valori di colonna esatti forniti per questa colonna chiave e per tutte le colonne chiave precedenti.</p></li><li><p>Tutti i valori di colonna necessari per le colonne chiave successive.</p></li></ul><p>Questa opzione deve essere usata quando si compilano chiavi di ricerca con caratteri jolly da usare per trovare le voci di indice più vicine alla fine di un indice. La fine dell'indice è la voce di indice trovata durante lo spostamento all'ultimo record di tale indice. La fine dell'indice non corrisponde all'estremità superiore dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Questa opzione non può essere usata quando la colonna chiave corrente non è una colonna di testo o una colonna binaria variabile. L'operazione avrà esito negativo JET_errInvalidgrbit se viene tentata.</p><p>Questa opzione è disponibile solo in Windows XP e versioni successive.</p> | 
| <p>JET_bitPartialColumnStartLimit</p> | <p>Questa opzione indica che la chiave di ricerca deve essere costruita in modo che la colonna chiave corrente sia considerata un carattere jolly di prefisso e che tutte le colonne chiave che vengono dopo la colonna chiave corrente devono essere considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare corrispondenze tra le voci di indice con gli elementi seguenti:</p><ul><li><p>Valori di colonna esatti forniti per questa colonna chiave e per tutte le colonne chiave precedenti.</p></li><li><p>Tutti i valori di colonna necessari per le colonne chiave successive.</p></li></ul><p>Questa opzione deve essere usata quando si compilano chiavi di ricerca con caratteri jolly da usare per trovare le voci di indice più vicine all'inizio di un indice. L'inizio dell'indice è la voce di indice trovata durante lo spostamento al primo record in tale indice. L'inizio dell'indice non corrisponde all'estremità bassa dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Questa opzione non può essere usata quando la colonna chiave corrente non è una colonna di testo o una colonna binaria variabile. L'operazione avrà esito negativo JET_errInvalidgrbit se viene tentata.</p><p>Questa opzione è disponibile solo in Windows XP e versioni successive.</p> | 
| <p>JET_bitStrLimit</p> | <p>Questa opzione indica che la chiave di ricerca deve essere costruita in modo che tutte le colonne chiave che arrivano dopo la colonna chiave corrente siano considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare corrispondenze tra le voci di indice con gli elementi seguenti:</p><ul><li><p>Valori di colonna esatti forniti per questa colonna chiave e per tutte le colonne chiave precedenti.</p></li><li><p>Tutti i valori di colonna necessari per le colonne chiave successive.</p></li></ul><p>Questa opzione deve essere usata quando si compilano chiavi di ricerca con caratteri jolly da usare per trovare le voci di indice più vicine alla fine di un indice. La fine dell'indice è la voce di indice trovata durante lo spostamento all'ultimo record di tale indice. La fine dell'indice non corrisponde all'estremità superiore dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Quando questa opzione viene specificata in combinazione con JET_bitSubStrLimit e la colonna chiave corrente è una colonna di testo, questa opzione verrà ignorata. Questo comportamento consente di dedurre il tipo della colonna chiave corrente durante la compilazione della chiave di ricerca.</p><p>Se si vuole creare una chiave di ricerca simile per l'inizio di un indice, è necessario eseguire una chiamata simile a <strong>JetMakeKey</strong> per l'ultima colonna chiave che non è un carattere jolly, ma senza opzioni con caratteri jolly specificate. La chiave di ricerca è quindi in uno stato appropriato da usare per tale ricerca. Ciò è analogo all'uso JET_bitFullColumnStartLimit, ad eccezione del fatto che la chiave di ricerca non viene completata in modo pulito come dopo l'uso di un'opzione con caratteri jolly.</p><p>Questa opzione è stata deprecata per Windows XP e versioni successive per risolvere questa semantica difficile. JET_bitFullColumnStartLimit e JET_bitFullColumnEndLimit devono essere usati laddove possibile.</p> | 
| <p>JET_bitSubStrLimit</p> | <p>Questa opzione indica che la chiave di ricerca deve essere costruita in modo che la colonna chiave corrente sia considerata un carattere jolly di prefisso e che tutte le colonne chiave che vengono dopo la colonna chiave corrente devono essere considerate caratteri jolly. Ciò significa che la chiave di ricerca costruita può essere usata per trovare corrispondenze tra le voci di indice con gli elementi seguenti:</p><ul><li><p>Valori di colonna esatti forniti per tutte le colonne chiave precedenti.</p></li><li><p>I dati della colonna specificati come prefisso del relativo valore di colonna per la colonna chiave corrente.</p></li><li><p>Qualsiasi valore di colonna per le colonne chiave successive.</p></li></ul><p>Questa opzione deve essere usata quando si compilano chiavi di ricerca con caratteri jolly da usare per trovare le voci di indice più vicine alla fine di un indice. La fine dell'indice è la voce di indice trovata durante lo spostamento all'ultimo record dell'indice. La fine dell'indice non corrisponde all'estremità superiore dell'indice, che può cambiare a seconda dell'ordinamento delle colonne chiave nell'indice.</p><p>Quando questa opzione viene specificata in combinazione con JET_bitStrLimit e la colonna chiave corrente è una colonna di testo, questa opzione avrà la precedenza. Questa opzione viene ignorata quando la colonna chiave corrente non è una colonna di testo. Questo comportamento consente di dedurre il tipo della colonna chiave corrente durante la compilazione della chiave di ricerca.</p><p>Se si vuole compilare una chiave di ricerca simile per l'inizio di un indice, è necessario effettuare una chiamata simile a <strong>JetMakeKey</strong> per la colonna chiave che deve essere il carattere jolly del prefisso, ma senza specificare opzioni con caratteri jolly. La chiave di ricerca è quindi in uno stato appropriato da usare per tale ricerca. Ciò è analogo all'uso JET_bitPartialColumnStartLimit, ad eccezione del fatto che la chiave di ricerca non viene completata in modo pulito come dopo l'uso di un'opzione con caratteri jolly.</p><p>Questa opzione è stata deprecata per Windows XP e versioni successive per risolvere questa semantica difficile. JET_bitPartialColumnStartLimit e JET_bitPartialColumnEndLimit devono essere usati, quando possibile.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errIndexTuplesKeyTooSmall</p> | <p>I dati della colonna forniti sono troppo piccoli per compilare una chiave valida per l'indice corrente perché tale indice è un indice di tupla e le dimensioni minime della tupla sono maggiori dei dati della colonna specificati. Per altre informazioni sugli indici di tupla, vedere <a href="gg294099(v=exchg.10).md">JetCreateIndex.</a> Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>I dati della colonna forniti non corrispondono alle dimensioni richieste dalla definizione della colonna. Ciò può verificarsi se il tipo di dati della colonna è intrinsecamente di una determinata dimensione. Ciò può verificarsi anche se il tipo di dati della colonna non è intrinsecamente di una determinata dimensione, ma la definizione della colonna lo dichiara come a lunghezza fissa. Un'eccezione è che questo errore non si verifica quando vengono forniti dati troppo piccoli per una colonna di testo a lunghezza fissa perché tutti i dati mancanti verranno riempiti automaticamente con spazi. Una seconda eccezione è che questo errore non si verifica quando vengono forniti dati troppo piccoli per una colonna binaria a lunghezza fissa perché tutti i dati mancanti verranno riempiti automaticamente con zeri.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Una delle opzioni richieste non è valida, usata in modo non valido o non è implementata. Questa operazione può verificarsi <strong>per JetMakeKey</strong> quando:</p><ul><li><p>JET_bitPartialColumnStartLimit o JET_bitPartialColumnEndLimit e la colonna chiave corrispondente non è una colonna di testo e non è una colonna binaria di lunghezza variabile. Questo caso si verifica solo in Windows XP e versioni successive.</p></li><li><p>Si è tentato di usare contemporaneamente più di una delle opzioni seguenti: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit e JET_bitFullColumnEndLimit. Questo caso si verifica solo in Windows XP e versioni successive.</p></li><li><p>Si tenta di usare JET_bitStrLimit o JET_bitSubStrLimit quando si usa una delle opzioni seguenti: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit e JET_bitFullColumnEndLimit. Questo caso si verifica solo in Windows XP e versioni successive.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</p><p>Questo problema può verificarsi <strong>per JetMakeKey</strong> quando JET_bitNormalizedKey è stato specificato un valore e il valore specificato nel buffer di input è troppo grande per essere una chiave di ricerca valida.</p> | 
| <p>JET_errKeyIsMade</p> | <p>I dati della colonna forniti <strong>a JetMakeKey</strong> sono stati rifiutati perché i dati della colonna sono già stati forniti per tutte le colonne chiave nell'indice corrente. Questa operazione può verificarsi in tre modi. Il primo modo è se vengono forniti dati di colonna per ogni colonna chiave nell'indice corrente. Il secondo modo è se sono stati forniti dati di colonna per almeno una colonna chiave ed è stata scelta un'opzione con caratteri jolly per l'ultima chiamata. Il terzo modo è se è stata fornita una chiave di ricerca costruita in precedenza usando JET_bitNormalizedKey, che copre tutte le colonne chiave.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Non è presente alcuna chiave di ricerca corrente per il cursore. Questa operazione si verifica per <strong>JetMakeKey</strong> se JET_bitNewKey non è specificato e non è stata costruita una chiave di ricerca per questo cursore usando una chiamata precedente a <strong>JetMakeKey.</strong> La chiave di ricerca verrà eliminata da una chiamata precedente a qualsiasi API di navigazione sul cursore diversa <a href="gg294117(v=exchg.10).md">da JetMove.</a></p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Non esiste alcun indice corrente per il cursore. Questa operazione si verifica per <strong>JetMakeKey</strong> se il cursore si trova nell'indice cluster di una tabella, se non è stato definito un indice primario e JET_bitNormalizedKey non è stato specificato. Non è possibile costruire una chiave di ricerca se il cursore si trova su un indice che non contiene colonne chiave, a meno che non venga fornita una chiave di ricerca costruita in precedenza.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, se JET_bitNormalizedKey e JET_bitNewKey non sono stati specificati, la chiave di ricerca sarà stata compilata dai criteri di ricerca per un'altra colonna chiave nell'indice corrente. Se JET_bitNormalizedKey non è stato specificato ed è stato specificato JET_bitNewKey, qualsiasi chiave di ricerca esistente in precedenza è stata rimossa e ne verrà creata una nuova in base ai criteri di ricerca per la prima colonna chiave nell'indice corrente. Se JET_bitNormalizedKey stato specificato, qualsiasi chiave di ricerca esistente in precedenza è stata eliminata e ne è stata caricata una nuova dal buffer di input. In ogni caso, non verrà apportata alcuna modifica allo stato del database.

In caso di errore, JET_bitNormalizedKey o JET_bitNewKey stato specificato, lo stato della chiave di ricerca non è definito. Se non JET_bitNormalizedKey o JET_bitNewKey specificati, non verrà apportata alcuna modifica allo stato della chiave di ricerca. In ogni caso, non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Le chiavi devono essere considerate come blocchi di dati opachi. Non è consigliabile tentare di sfruttare la struttura interna di questi dati. Tuttavia, le informazioni seguenti sono note su tutte le chiavi ESENT:

  - Le chiavi possono essere confrontate tra loro usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) per stabilire il relativo ordinamento nell'indice di origine sulla tabella delle voci dell'indice di origine.

  - È inutile confrontare le chiavi delle voci di indice di indici diversi l'una rispetto all'altra.

  - Una chiave è sempre minore o uguale a JET_cbKeyMost (255) byte prima di Windows Vista. In Windows Vista e versioni successive, le chiavi possono essere più grandi. La dimensione massima di una chiave è uguale al valore corrente di JET_paramKeyMost.

Le chiavi di ricerca possono essere più lunghe di un byte se è stata usata un'opzione con caratteri jolly. In tal caso, la chiave di ricerca sarà fino a JET_cbLimitKeyMost (256) byte per le versioni precedenti a Windows Vista e JET_paramKeyMost + 1 byte per Windows Vista e versioni successive.

Questa dimensione massima della chiave è molto importante. Ogni volta che è presente una voce di indice con valori di colonna sufficientemente grandi da generare una chiave per tale indice che altrimenti sarebbe maggiore di questa dimensione massima, tale chiave viene troncata automaticamente a tale dimensione massima. Ciò causa due effetti:

  - Per le voci in un indice univoco, le voci che altrimenti sarebbero univoche verranno dichiarate come duplicate.

  - Per le voci in tutti gli indici, il troncamento delle chiavi causerà la dichiarazione di corrispondenze per le voci di indice che altrimenti non corrisponderebbero ai criteri di ricerca di una determinata chiave di ricerca.

Le applicazioni devono prevedere questo troncamento ed evitarlo o compensarne gli effetti. In Windows Vista è stato aggiunto un nuovo flag di indice, JET_bitIndexDisallowTruncation, per consentire alle applicazioni di evitare troncamenti delle chiavi. Per altre [informazioni su questa opzione di](./jet-indexcreate-structure.md) indicizzazione, vedere la struttura JET_INDEXCREATE di indicizzazione.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
