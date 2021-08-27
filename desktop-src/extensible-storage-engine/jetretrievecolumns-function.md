---
description: 'Altre informazioni su: Funzione JetRetrieveColumns'
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
ms.openlocfilehash: ad6e1d39797c9a9ff965644ceea7858cb4af1a56
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472497"
---
# <a name="jetretrievecolumns-function"></a>Funzione JetRetrieveColumns


_**Si applica a:** Windows | Windows Server_

## <a name="jetretrievecolumns-function"></a>Funzione JetRetrieveColumns

La **funzione JetRetrieveColumns** recupera più valori di colonna dal record corrente in una singola operazione. Una matrice di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) viene usata per descrivere il set di valori di colonna da recuperare e per descrivere i buffer di output per ogni valore di colonna da recuperare.

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

*tableid*

Cursore da utilizzare per questa chiamata.

*pretrievecolumn*

Puntatore a una matrice di una o [più JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) struttura . Ogni struttura include descrizioni del valore della colonna da recuperare e della posizione in cui archiviare i dati restituiti.

*cretrievecolumn*

Numero di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) nella matrice specificata da *pretrievecolumn*.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBadItagSequence</p> | <p>È stato passato un valore di numero di sequenza di colonna multivalore non valido in pretinfo- &gt; itagSequence. I valori validi per i numeri di sequenza di valori di colonna multivalore sono 1 o superiori. Il valore 0 (zero) è valido per questa funzione, ma non è valido <a href="gg269198(v=exchg.10).md">per JetRetrieveColumn</a>.</p> | 
| <p>JET_errBadColumnId</p> | <p>L'ID di colonna specificato non rientra nei limiti legali di un ID di colonna.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonna descritta dal <em>valore columnid</em> specificato non esiste nella tabella.</p> | 
| <p>JET_errIndexTuplesCannotRetrieveFromIndex</p> | <p>Le colonne indicizzate come sottostringhe non possono essere recuperate dall'indice, poiché solo una piccola parte della colonna è in genere presente in ogni voce di indice.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>In alcuni casi, il buffer specificato per la colonna di recupero deve essere sufficientemente ridimensionato per restituire qualsiasi quantità del valore della colonna. Ad esempio, le colonne aggiornabili del deposito vengono modificate in modo da essere coerenti per il contesto transazionale della sessione chiamante e questa modifica richiede il buffer fornito dal chiamante. Se viene specificato spazio nel buffer insufficiente, JET_errInvalidBufferSize viene restituito un valore e non viene restituito alcun dato di colonna.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Le opzioni fornite sono sconosciute o una combinazione non valida di impostazioni di bit note.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno o più parametri specificati non sono corretti. Questo problema può verificarsi se retinfo.cbStruct è inferiore alle dimensioni <a href="gg294049(v=exchg.10).md">di JET_RETINFO</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore non è posizionato su un record. I motivi possono essere diversi. Ad esempio, ciò si verifica se il cursore è attualmente posizionato dopo l'ultimo record nell'indice corrente.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Non è stato possibile recuperare l'intero valore della colonna perché il buffer specificato è inferiore alle dimensioni della colonna.</p> | 



In caso di esito positivo, i dati e le dimensioni delle colonne vengono restituiti nei buffer forniti descritti nella matrice [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) strutture. Se *un oggetto itagSequence* è stato impostato su 0 (zero) per indicare che il numero di istanze di un campo multivalore è desiderato anziché i dati della colonna, il numero di istanze di una colonna multivalore viene restituito nel campo *itagSequence* stesso. Ogni [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) ha un campo di errore che contiene avvisi per la colonna recuperata. Se la colonna ha **valore NULL,** il codice di errore verrà impostato su JET_wrnColumnNull.

In caso di errore, la posizione del cursore rimane invariata e non vengono copiati dati nel buffer specificato.

#### <a name="remarks"></a>Commenti

**JetRetrieveColumns** supporta una funzionalità non disponibile [in JetRetrieveColumn.](./jetretrievecolumn-function.md) Questa è la possibilità di recuperare il numero di istanze di una colonna multivalore. Lo scopo di questa funzionalità è consentire a un'applicazione di recuperare tutti i valori di una colonna. Questa operazione può essere eseguita determinando innanzitutto il numero di valori di una colonna. Successivamente, le relative lunghezze possono essere determinate chiamando nuovamente [](./jet-retrievecolumn-structure.md) **JetRetrieveColumns** con una JET_RETRIEVECOLUMN allocata per ogni valore per determinare la lunghezza dei dati della colonna. Questa operazione può essere eseguita passando puntatori _NULL pvData_ con *cbMax* pari a 0 (zero) e recuperando la lunghezza della colonna in *cbActual*. La terza e l'ultima chiamata possono essere effettuate con memoria allocata per i dati del valore della colonna.

Se una colonna recuperata viene troncata a causa di un buffer di lunghezza insufficiente, l'API restituirà JET_wrnBufferTruncated. Tuttavia, altri errori, JET_wrnColumnNull vengono restituiti solo nel campo dell'errore in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). Il motivo è che le applicazioni spesso vogliono assicurarsi che tutti i dati siano stati recuperati e la restituzione di questo errore **da JetRetrieveColumns** facilita questa comprensione.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[Oggetti JetSetColumns](./jetsetcolumns-function.md)
