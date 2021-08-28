---
description: 'Altre informazioni su: Funzione JetSetTableSequential'
title: Funzione JetSetTableSequential
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a8b49b112c9566b15226e8ffd52f4240cff2fb8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471717"
---
# <a name="jetsettablesequential-function"></a>Funzione JetSetTableSequential


_**Si applica a:** Windows | Windows Server_

## <a name="jetsettablesequential-function"></a>Funzione JetSetTableSequential

La **funzione JetSetTableSequential** notifica al motore di database che l'applicazione sta eseguendo l'analisi dell'intero indice corrente che contiene un determinato cursore. Di conseguenza, i metodi usati per accedere ai dati dell'indice verranno ottimizzati per rendere questo scenario il più veloce possibile.

**Windows XP:****JetSetTableSequential** è stato introdotto in Windows XP.  

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*grbit*

Gruppo di bit che specificano zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitPrereadForward</p> | <p>Questa opzione viene usata per indicizzare in avanti.</p><p><strong>Windows 7:</strong><strong>JET_bitPrereadForward</strong> è stato introdotto in Windows 7.  </p> | 
| <p>JET_bitPrereadBackward</p> | <p>Questa opzione viene usata per indicizzare in senso inverso.</p><p><strong>Windows 7:</strong><strong>JET_bitPrereadBackward</strong> è stato introdotto in Windows 7.  </p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state inattiva in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se questa funzione ha esito positivo, l'indice corrente del cursore viene ottimizzato per un'analisi sequenziale dell'intero indice. Non verrà apportata alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, non verrà apportata alcuna modifica alla configurazione del cursore. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Se l'applicazione deve analizzare in modo efficiente un subset noto di un indice, viene eseguita un'ottimizzazione simile anche ogni volta che viene stabilito un intervallo di indici tramite [JetSetIndexRange](./jetsetindexrange-function.md). Questa ottimizzazione è disponibile solo in Windows XP e versioni successive.

Se l'applicazione deve analizzare in modo efficiente un subset sconosciuto di un indice, non deve essere eseguita alcuna azione. Il motore può rilevare automaticamente il comportamento di analisi e recupererà i dati in anticipo. Questo comportamento, tuttavia, non è così aggressivo.

Questa ottimizzazione rende efficiente l'analisi dell'indice primario e rende efficiente solo l'analisi dei dati delle voci di indice in un indice secondario. Non rende efficiente l'analisi di un indice secondario durante il recupero dei dati dei record. Ciò è dovuto al fatto che il motore non esegue un read-ahead sui dati del record.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
