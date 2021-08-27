---
description: Altre informazioni sulla funzione JetPrepareUpdate
title: Funzione JetPrepareUpdate
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98b14688b42c3e29bbbbab5b96466ad6c97f98e3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477547"
---
# <a name="jetprepareupdate-function"></a>Funzione JetPrepareUpdate


_**Si applica a:** Windows | Windows Server_

## <a name="jetprepareupdate-function"></a>Funzione JetPrepareUpdate

La **funzione JetPrepareUpdate** è la prima operazione nell'esecuzione di un aggiornamento, allo scopo di inserire un nuovo record o sostituire un record esistente con nuovi valori. Gli aggiornamenti vengono evasi chiamando **JetPrepareUpdate**, quindi chiamando [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) zero o più volte e infine chiamando [JetUpdate](./jetupdate-function.md) per completare l'operazione. **JetPrepareUpdate** e [JetUpdate](./jetupdate-function.md) impostano i limiti per un'operazione di aggiornamento e sono importanti per avere solo lo stato di aggiornamento finale di un record immesso negli indici. Si tratta di un'operazione più efficiente, ma necessaria anche nei casi in cui i dati devono corrispondere a uno stato valido tramite più operazioni di colonna impostata.

Esistono alcune opzioni diverse per l'inserimento o la sostituzione dei record e sono descritte più dettagliatamente di seguito.

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*Preparazione*

Opzioni che possono essere usate per preparare un aggiornamento, tra cui le seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_prepCancel</p> | <p>Questo flag fa sì <strong>che JetPrepareUpdate</strong> annulli l'aggiornamento per questo cursore.</p> | 
| <p>JET_prepInsert</p> | <p>Questo flag fa sì che il cursore si prepari per l'inserimento di un nuovo record. Tutti i dati vengono inizializzati allo stato predefinito per il record. Se la tabella include una colonna a incremento automatico, a questo record viene assegnato un nuovo valore indipendentemente dal fatto che l'aggiornamento abbia esito positivo, negativo o annullato.</p> | 
| <p>JET_prepInsertCopy</p> | <p>Questo flag fa sì che il cursore si prepari per l'inserimento di una copia del record esistente. Se si usa questa opzione, deve essere presente un record corrente. Lo stato iniziale del nuovo record viene copiato dal record corrente. I valori lunghi archiviati fuori record vengono copiati virtualmente.</p> | 
| <p>JET_prepInsertCopyDeleteOriginal</p> | <p>Questo flag fa sì che il cursore si prepari per un inserimento dello stesso record e un'eliminazione o il record originale. Viene usato nei casi in cui la chiave primaria è stata modificata.</p> | 
| <p>JET_prepReplace</p> | <p>Questo flag fa sì che il cursore si prepari per una sostituzione del record corrente. Se la tabella include una colonna version, la colonna version viene impostata sul valore successivo nella relativa sequenza. Se l'aggiornamento non viene completato, il valore della versione nel record non verrà interessato. Viene effettuato un blocco di aggiornamento sul record per impedire ad altre sessioni di aggiornare questo record prima del completamento della sessione.</p> | 
| <p>JET_prepReplaceNoLock</p> | <p>Questo flag è simile a JET_prepReplace, ma non viene effettuato alcun blocco per impedire ad altre sessioni di aggiornare questo record. Al contrario, questa sessione potrebbe ricevere JET_errWriteConflict quando chiama <a href="gg269288(v=exchg.10).md">JetUpdate</a> per completare l'aggiornamento.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errAlreadyPrepared</p> | <p><strong>JetPrepareUpdate è</strong> stato chiamato con un flag valido per la preparazione, ma non JET_prepCancel e il cursore era già nello stato preparato.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Il flag di preparazione specificato non è un flag valido.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errNotInTransaction</p> | <p><strong>JetPrepareUpdate è</strong> stato chiamato per sostituire un record con colonne SLV. Colonne SLV. Si noti che le colonne SLV sono una funzionalità non destinata all'utilizzo generale. Questa funzionalità viene usata per supportare l'infrastruttura Exchange Microsoft e non deve essere usata nell'applicazione.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errRollbackError</p> | <p><strong>JetPrepareUpdate</strong> è stato chiamato con JET_prepCancel ma non è stato possibile eseguire il rollback di tutte le modifiche apportate alle colonne di tipo JET_coltypLongText e/o colonne di tipo JET_coltypLongBinary.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Questo flag non può essere usato con la stessa sessione da più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p><strong>JetPrepareUpdate è</strong> stato chiamato con JET_prepCancel ma il cursore non era nello stato preparato.</p> | 



In caso di esito positivo, il cursore viene modificato nello stato preparato allo scopo dell'aggiornamento desiderato oppure, nel caso di JET_prepCancel, il cursore viene ripristinato allo stato non preparato e le modifiche vengono eliminate.

In caso di errore, lo stato del cursore rimane invariato. Se l'errore JET_errRollbackError lo stato del cursore viene modificato nello stato non preparato, ma non tutte le modifiche sono state ripristinate.

#### <a name="remarks"></a>Commenti

L'inserimento di una copia di un record è un'ottimizzazione importante quando i record condividono dati di tipo JET_coltypLongText e/o JET_coltypLongBinary. Questi dati vengono archiviati al di fuori dei record quando sono di grandi dimensioni ed è possibile che più record condino la stessa rappresentazione fisica dei dati. In questo caso, i dati possono essere aggiornati da uno dei due record, ma in questo modo i dati verranno burst in modo che ogni record abbia una propria copia. Non è possibile modificare i dati in un record mediante una modifica da un altro record. Inoltre, non è possibile bloccare un aggiornamento di un record da un aggiornamento di un altro record. Si tratta di una funzionalità centrale di ESE ed è nota come blocco a livello di record.

[Le operazioni JetUpdate](./jetupdate-function.md) che non riescono lasciano il cursore nello stato preparato per l'aggiornamento. In questo modo è possibile correggere alcuni errori, ad esempio un valore di colonna errato, senza richiedere la ricreazione dello stato di aggiornamento. Ciò significa che in tutti i casi in cui un cursore abbandona un aggiornamento, deve chiamare in modo **esplicito JetPrepareUpdate** con JET_prepCancel.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
