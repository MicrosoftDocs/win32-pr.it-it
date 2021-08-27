---
description: Altre informazioni sulla funzione JetSetColumns
title: Funzione JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4cf9639ded8774be2b46c3a62bc97c6b56b9f15e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465668"
---
# <a name="jetsetcolumns-function"></a>Funzione JetSetColumns


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetcolumns-function"></a>Funzione JetSetColumns

La **funzione JetSetColumns** ha un comportamento simile a [JetSetColumn,](./jetsetcolumn-function.md) ma consente a un'applicazione di impostare più valori di colonna in una singola operazione. Una matrice di [JET_SETCOLUMN](./jet-setcolumn-structure.md) per descrivere il set di valori di colonna da impostare e per descrivere i buffer di input per ogni valore di colonna da impostare.

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*psetcolumn*

Puntatore a una matrice di una o [più JET_SETCOLUMN](./jet-setcolumn-structure.md) struttura . Ogni struttura include descrizioni del valore della colonna da impostare e da dove ottenere i dati della colonna da impostare.

*csetcolumn*

Numero di [JET_SETCOLUMN](./jet-setcolumn-structure.md) nella matrice specificata da *psetcolumn*.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errBadColumnId</p> | <p>L'ID colonna specificato non rientra nei limiti legali di un ID di colonna.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errColumnIllegalNull</p> | <p>Uguale a JET_errNullInvalid.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonna descritta da <em>columnid</em> specificato non esiste nella tabella.</p> | 
| <p>JET_errColumnNotUpdatable</p> | <p>Tentativo non valido di aggiornare un valore long durante un'operazione di inserimento dell'eliminazione dell'aggiornamento originale.</p> | 
| <p>JET_errColumnTooBig</p> | <p>I dati del valore di colonna specificato nel buffer di input superano la limitazione delle dimensioni naturale per una colonna a lunghezza fissa o configurata per colonne di testo o binarie a lunghezza fissa. Questo errore viene restituito anche quando si passano più di 1024 byte di dati per una colonna lunga e si imposta JET_bitSetIntrinsicLV flag.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>La dimensione dei dati del valore di colonna specificata non corrisponde a quella naturale per il tipo di dati a lunghezza fissa.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Tentativo non valido di aggiornare una colonna con incremento automatico durante un'operazione di inserimento o aggiornamento oppure di aggiornare una colonna di versione durante un'operazione di sostituzione.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Le opzioni fornite sono sconosciute o una combinazione non valida di impostazioni di bit note.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L'oggetto psetinfo- cbStruct specificato non è una dimensione valida per la &gt; <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> struttura.</p> | 
| <p>JET_errMultiValuedDuplicate</p> | <p>L'operazione set column ha tentato di creare un valore duplicato e ha specificato JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errNotInTransaction</p> | <p>È stato effettuato un tentativo non valido di aggiornare un valore di colonna long quando la sessione chiamante non era in una transazione.</p> | 
| <p>JET_errNullInvalid</p> | <p>Tentativo non valido di impostare una colonna non NULL su NULL.</p> | 
| <p>JET_errRecordTooBig</p> | <p>Non è stato possibile impostare il valore della colonna sul valore nel buffer di input perché il record avrebbe superato la limitazione delle dimensioni della pagina correlata. Le colonne di <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> possono essere archiviate separatamente dai dati dei record rimanenti. Tuttavia, altre colonne devono essere archiviate con il record e possono causare il superamento della limitazione delle dimensioni del record. Anche le colonne lunghe richiedono 5 byte di spazio all'interno del record come collegamento e anche questo può JET_errRecordTooBig restituito.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p>Il cursore non è attualmente in fase di inserimento di un nuovo record o di aggiornamento di un record esistente.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Il valore della colonna nel buffer di input ha superato la lunghezza massima configurata per una colonna a lunghezza variabile ed è stato troncato.</p> | 



In caso di esito positivo, per ogni colonna descritta in psetcolumns, la parte desiderata del valore della colonna viene impostata con i dati copiati dal buffer di input. Il set di dati della colonna potrebbe essere stato troncato se ha superato la lunghezza massima specificata per una colonna a lunghezza variabile.

In caso di errore, la posizione del cursore rimane invariata e nel buffer di copia non viene aggiornato alcun valore di colonna.

#### <a name="remarks"></a>Commenti

Se una singola operazione di colonna set restituisce un errore, **l'intera operazione JetSetColumns** restituirà un errore. Gli avvisi, in generale, vengono restituiti nell'errore psetcolumns- e non nel codice \> restituito da questa funzione. Tuttavia, se l'ultimo set di colonne contiene un avviso, questo avviso verrà restituito da **JetSetColumns** stesso.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
