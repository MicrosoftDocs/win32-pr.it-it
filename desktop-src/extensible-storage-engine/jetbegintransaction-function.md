---
description: Altre informazioni sulla funzione JetBeginTransaction
title: Funzione JetBeginTransaction
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 991f80ab346ae039c6222a508374de806d0faf2c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479267"
---
# <a name="jetbegintransaction-function"></a>Funzione JetBeginTransaction


_**Si applica a:** Windows | Windows Server_

## <a name="jetbegintransaction-function"></a>Funzione JetBeginTransaction

La **funzione JetBeginTransaction** fa sì che una sessione immissione di una transazione e la creazione di un nuovo punto di salvataggio. Questa funzione può essere chiamata più volte in una singola sessione per causare la creazione di punti di salvataggio aggiuntivi. Questi punti di salvataggio possono essere usati per mantenere o rimuovere in modo selettivo le modifiche apportate allo stato del database.

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p><p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Non è possibile avviare una nuova transazione perché la sessione è già alla profondità massima del punto di salvataggio consentita dal motore di database.</p> | 



In caso di esito positivo, la sessione specificata si trova all'interno di una transazione. Se la sessione era in precedenza all'interno di una transazione, verrà creato un nuovo punto di salvataggio.

In caso di errore, lo stato transazionale della sessione rimarrà invariato. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Il motore di database fornisce un modello di isolamento dello snapshot per le relative transazioni. Ciò significa che, quando una sessione entra per la prima volta in uno stato transazionale, l'intero database verrà bloccato nel tempo all'inizio della transazione. Una sessione non deve leggere i dati di blocco perché può sempre accedere alla versione appropriata di questi dati. Ciò significa che una sessione che aggiorna i dati non bloccherà mai la lettura di tali dati da parte di una sessione diversa.

Un'altra implicazione dell'uso dell'isolamento dello snapshot è il modello di blocco usato per gli aggiornamenti. Il motore di database conferirà un blocco di scrittura per una determinata parte di dati alla prima sessione che lo richiede. Questo blocco di scrittura viene rilasciato quando viene eseguito il commit o l'interruzione completa della transazione in modo che la sessione non sia più in una transazione. Mentre una sessione contiene un blocco di scrittura, qualsiasi altra sessione che richiede lo stesso blocco di scrittura non si blocchi finché non è disponibile il blocco di scrittura. Al contrario, la seconda sessione avrà immediatamente esito negativo con JET_errWriteConflict. Per risolvere questo conflitto, la seconda sessione deve interrompere (o eseguire completamente il commit) della transazione, attendere un breve periodo di tempo per il commit o l'interruzione della prima sessione e quindi ricominciare da capo.

Per supportare l'isolamento dello snapshot, il motore di database archivia tutte le versioni di tutti i dati modificati in memoria dal momento in cui è stata avviata la transazione attiva meno recente in qualsiasi sessione. Ciò ha implicazioni importanti per l'applicazione. Qualsiasi comportamento che causa la compilazione [di](./extensible-storage-engine-system-parameters.md) un numero elevato di versioni in memoria può causare l'esaurimento delle dimensioni massime dell'archivio [versioni](./resource-parameters.md) dell'istanza (per altre informazioni, vedere JET_paramMaxVerPages in Parametri di sistema). Questo comportamento include, ma non è limitato agli aggiornamenti molto grandi in una singola transazione e alle transazioni con esecuzione molto lunga. Di conseguenza, è molto importante configurare correttamente le dimensioni dell'archivio delle versioni per il carico transazionale previsto dell'applicazione. È anche importante fare attenzione a limitare il numero di aggiornamenti eseguiti in una singola transazione. Inoltre, è importante rendere le transazioni il più brevi possibile in scenari con carico elevato.

È consigliabile che l'applicazione sia sempre nel contesto di una transazione quando si chiamano API ESE che recuperano o aggiornano i dati. Se questa operazione non viene eseguita, il motore di database esegue automaticamente il wrapping di ogni chiamata API ESE di questo tipo in una transazione per conto dell'applicazione. In alcuni casi, il costo di queste transazioni molto brevi può essere elevato rapidamente.

Il comportamento predefinito del motore è limitare l'uso di una sessione allo stesso thread dal momento in cui viene effettuata la prima chiamata a **JetBeginTransaction** fino al momento in cui viene effettuata la chiamata corrispondente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback.](./jetrollback-function.md) Questo comportamento può essere modificato per rimuovere questa restrizione impostando un contesto di sessione personalizzato usando [JetSetSessionContext](./jetsetsessioncontext-function.md) [e JetResetSessionContext](./jetresetsessioncontext-function.md).

Il motore di database supporta anche le modifiche dello schema transazionale. Ad esempio, è possibile avviare una nuova transazione, creare una tabella, aggiungere alcune colonne, creare uno o due indici e quindi interrompere la transazione. Gli elementi dello schema appena aggiunti verranno rimossi dal database. È anche possibile combinare le modifiche dello schema e gli aggiornamenti normali del database nella stessa transazione.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
