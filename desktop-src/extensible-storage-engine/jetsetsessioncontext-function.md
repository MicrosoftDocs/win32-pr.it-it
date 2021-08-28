---
description: Altre informazioni sulla funzione JetSetSessionContext
title: Funzione JetSetSessionContext
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ac368caaff5ec652a6dc7ad490e7418e62888b7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986634"
---
# <a name="jetsetsessioncontext-function"></a>Funzione JetSetSessionContext


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetsessioncontext-function"></a>Funzione JetSetSessionContext

La **funzione JetSetSessionContext** associa una sessione al thread corrente usando l'handle di contesto specificato. Questa associazione sostituisce il requisito predefinito del motore che una transazione per una determinata sessione deve essere eseguita interamente nello stesso thread.

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*ulContext*

Identificatore univoco a cui verrà associata la sessione.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Uno dei parametri forniti conteneva un valore imprevisto oppure la combinazione di diversi valori di parametro ha restituito un risultato imprevisto. Questo errore verrà restituito <strong>da JetSetSessionContext</strong> nelle condizioni seguenti:</p><ul><li><p><em>ulContext</em> è NULL</p></li><li><p><em>ulContext</em> è -1</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Impossibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionContextAlreadySet</p> | <p>Impossibile associare la sessione al thread corrente perché è già stata associata a un thread.</p> | 
| <p>JET_errTermInProgress</p> | <p>Impossibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 



Se questa funzione ha esito positivo, la sessione verrà associata al thread corrente. Non verrà apportata alcuna modifica allo stato del database.

Se questa funzione ha esito negativo, lo stato della sessione rimarrà invariato. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Una sessione è in genere associata a un thread specifico per la durata di una transazione. Questo comportamento è progettato per consentire alle applicazioni di rilevare ed evitare la condivisione concettualmente sconsigliata di una singola sessione tra più thread. In alcuni casi, questo semplice controllo non funziona con l'architettura dell'applicazione. Ad esempio, se l'applicazione ospita oggetti sul lato server usando un pool di thread e le transazioni si estendono su più chiamate server a un determinato oggetto, questa protezione potrebbe causare l'esito negativo di alcune di queste chiamate con JET_errSessionSharingViolation anche se il modello di utilizzo è corretto. Questa situazione è comune per i server oggetti COM.

**JetSetSessionContext** e [JetResetSessionContext](./jetresetsessioncontext-function.md) risolvono questo problema rendendo il controllo di condivisione della sessione un po' più flessibile. Quando l'applicazione inizia a effettuare una serie di chiamate API ESE usando una sessione specifica, imposta innanzitutto il contesto della sessione su un valore specificato. Questa azione associa la sessione al thread chiamante. Nell'esempio specificato, questo contesto può essere l'indirizzo dell'oggetto che contiene l'handle di sessione JET. Dopo aver effettuato le chiamate API ESE, l'applicazione reimposta il contesto di sessione. Questa azione dissocia la sessione dal thread chiamante. L'oggetto e la relativa sessione possono quindi essere usati da un altro thread anche se la sessione ha una transazione attiva.

È importante notare che è necessario chiamare **JetSetSessionContext** prima di aprire una transazione in tale sessione oppure l'associazione non funzionerà.

**JetSetSessionContext** è thread-safe. Più thread possono provare a impostare un contesto di thread nella stessa sessione contemporaneamente e ne verrà vinto solo uno. Questo fatto può essere usato dall'applicazione come mezzo per allocare una sessione da un pool senza archiviare lo stato esterno sulla relativa allocazione.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
