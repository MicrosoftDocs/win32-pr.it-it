---
description: Altre informazioni sulla funzione JetGetRecordPosition
title: Funzione JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd1e84b995485afd46119b78289c1cac23e19215
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982434"
---
# <a name="jetgetrecordposition-function"></a>Funzione JetGetRecordPosition


_**Si applica a:** Windows | Windows Server_

## <a name="jetgetrecordposition-function"></a>Funzione JetGetRecordPosition

La **funzione JetGetRecordPosition** restituisce la posizione frazionaria del record corrente nell'indice corrente sotto forma di JET_RECPOS [struttura.](./jet-recpos-structure.md) Questa struttura descrive le posizioni frazionarie in termini di un numero approssimativo di voci di indice prima del record corrente e di un numero totale approssimativo di voci nell'indice.

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*precpos*

Descrizione della frazione da utilizzare per ottenere la posizione del record corrente nell'indice corrente.

*cbRecpos*

Dimensione della memoria allocata *in corrispondenza di precpos*.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è stata ancora inizializzata.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossibile completare l'operazione perché l'istanza, associata alla sessione, ha rilevato un errore irreversibile. È necessario revocare l'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows 2000:</strong>  Questo errore non verrà restituito dal sistema operativo Windows 2000.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Le dimensioni della memoria allocata <em>in precpos</em> non sono sufficienti.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore non è attualmente in un record e non può restituire una posizione.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente.</p><p><strong>Windows 2000:</strong>  Questo errore non verrà restituito dal sistema operativo Windows 2000.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



In caso di esito positivo, il numero approssimativo di voci di indice che precedono il record corrente nell'indice viene restituito in precpos- \> centriesLT. 1 viene restituito in precpos- \> centriesInRange. Il numero approssimativo di voci nell'indice viene restituito in precpos- \> centriesTotal.

In caso di errore, non vengono apportate modifiche alla memoria allocata *in precpos*.

#### <a name="remarks"></a>Commenti

Questa operazione restituisce dati variabili quando gli aggiornamenti vengono eseguiti in modo continuo nella tabella. Le modifiche nei valori non corrisponderanno sempre alle aspettative in base alla conoscenza degli aggiornamenti, poiché i valori sono approssimazioni basate sulle proprietà fisiche dell'indice. L'isolamento transazionale non si applica alle posizioni **da JetGetRecordPosition** perché i valori dipendono dalle proprietà fisiche dell'indice che non sono isolate dalla transazione.

[JET_RECPOS](./jet-recpos-structure.md) deve essere usato per descrivere un record all'interno di una tabella o per riposizionare un record vicino a un record esistente. I segnalibri per un record esistente devono invece essere recuperati e quindi usati per riposizionare lo stesso record.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetGotoPosition](./jetgotoposition-function.md)  
[JetStopService](./jetstopservice-function.md)
