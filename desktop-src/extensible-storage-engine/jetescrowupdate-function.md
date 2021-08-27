---
description: Altre informazioni sulla funzione JetEscrowUpdate
title: Funzione JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9f037b8c26829d7b1f3a10b05e1d4bd83bd186a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469798"
---
# <a name="jetescrowupdate-function"></a>Funzione JetEscrowUpdate


_**Si applica a:** Windows | Windows Server_

## <a name="jetescrowupdate-function"></a>Funzione JetEscrowUpdate

La **funzione JetEscrowUpdate** esegue un'operazione di addizione atomica in una colonna. Questa funzione consente a più sessioni di aggiornare lo stesso record contemporaneamente senza conflitti.

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*tableid*

Cursore da utilizzare per questa chiamata.

*columnid*

*Columnid* della colonna da aggiornare.

*Pv*

Puntatore a un buffer contenente l'oggetto addend per la colonna.

*cbMax*

Dimensione del buffer contenente l'addend.

*pvOld*

Buffer di output che riceverà il valore corrente della colonna come archiviato nel database (il controllo delle versioni viene ignorato).

*cbOldMax*

Dimensione massima del buffer di output che riceverà il valore corrente della colonna. Attualmente è JET_coltypLong supportato solo il buffer, quindi il buffer deve avere una lunghezza di 4 byte o 0 byte. Se *pvOld* è NULL, *cbOldMax* deve essere 0.

*pcbOldActual*

Riceve la quantità effettiva di dati di valore non elaborati ricevuti nel buffer di output.

*grbit*

Gruppo di bit che specifica zero o più delle opzioni seguenti.


| <p>valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitEscrowNoRollback</p> | <p>Anche se la sessione che esegue l'aggiornamento della garanzia ha il rollback della transazione, questo aggiornamento non verrà annullato. Si noti che poiché i record di log potrebbero non essere scaricati su disco, gli aggiornamenti di deposito recenti emersi con questo flag potrebbero andare persi in caso di arresto anomalo.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore Archiviazione estendibile](./extensible-storage-engine-errors.md) e Parametri [di gestione degli errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errAlreadyPrepared</p> | <p>Il cursore dispone di un aggiornamento preparato <a href="gg269339(v=exchg.10).md">con JetPrepareUpdate</a>.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>È stata passata una dimensione del buffer non valida. Attualmente è JET_coltypLong supportato, quindi il buffer deve essere di 4 byte.</p> | 
| <p>JET_errInvalidOperation</p> | <p>È stata specificata una colonna non valida. La colonna deve essere creata con JET_bitColumnEscrowUpdate specificato. Solo le colonne fisse JET_coltypLong possono essere specificate come aggiornabili a garanzia.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Il cursore deve essere posizionato su un record per aggiornare una colonna.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Gli aggiornamenti del deposito possono essere eseguiti solo dalle sessioni in una transazione.</p> | 
| <p>JET_errNotInitialized</p> | <p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Il cursore non può essere di sola lettura e aggiornare un record.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La stessa sessione non può essere usata da più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p> | 
| <p>JET_errTermInProgress</p> | <p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La sessione deve disporre delle autorizzazioni di scrittura per aggiornare un record.</p> | 
| <p>JET_errWriteConflict</p> | <p>Errore restituito quando viene richiesto un aggiornamento in conflitto.</p> | 



#### <a name="remarks"></a>Commenti

In genere, se due sessioni tentano di aggiornare un record contemporaneamente, la seconda sessione riceverà un errore JET_errWriteConflict a meno che le sessioni non siano completamente serializzate. Per serializzare due sessioni che aggiornano lo stesso record, la seconda sessione deve avviare la transazione dopo il commit della prima transazione. Per [altre informazioni, vedere JetBeginTransaction.](./jetbegintransaction-function.md)

È possibile aggiornare più colonne nello stesso record. Gli aggiornamenti non influiscono l'un l'altro.

Solo **le operazioni JetEscrowUpdate** sono compatibili tra loro. Se due sessioni diverse provano a preparare gli aggiornamenti o eliminare lo stesso record, verrà generato un conflitto di scrittura.


| <p></p> | <p></p> | <p>Sessione B<br /><strong>JetEscrowUpdate</strong></p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | 
|---------|---------|--------------------------------------------------------|---------------------------------------------------------------|--------------------------------------------------------|
| <p></p> | <p><strong>JetEscrowUpdate</strong></p> | <p>JET_errSuccess</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p></p> | <p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 
| <p>Sessione A</p> | <p><a href="gg269315(v=exchg.10).md">JetDelete</a></p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | <p>JET_errWriteConflict</p> | 



Le operazioni di deposito vengono con controllo delle versioni e vengono annullate usando [JetRollback](./jetrollback-function.md) (a meno JET_bitEscrowNoRollback specificato). **JetEscrowUpdate** restituisce il valore non elaborato della colonna archiviata nel database, perché un'applicazione potrebbe voler eseguire un'azione speciale quando viene raggiunto un valore sentinel. [JetRetrieveColumn](./jetretrievecolumn-function.md) restituisce la visualizzazione con versione corretta della colonna, ignorando gli aggiornamenti eseguiti da sessioni simultanee.

Date due sessioni che operano sulla stessa colonna dello stesso record, è possibile vedere come funziona. Si supponga che la colonna inizi con un valore pari a 0.


| <p>Sessione</p> | <p>Operazione</p> | <p>Valore archiviato</p> | <p>Valore restituito</p> | 
|----------------|------------------|---------------------|-----------------------|
| <p>A</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p></p> | 
| <p>A</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p> | <p></p> | <p>0</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (4)</p> | <p>4</p> | <p>0</p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p> | <p></p> | <p></p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>0</p> | 
| <p>B</p> | <p><strong>JetEscrowUpdate</strong> (3)</p> | <p>7</p> | <p>4</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (2)</p> | <p>9</p> | <p>7</p> | 
| <p>A</p> | <p><strong>JetEscrowUpdate</strong> (-7)</p> | <p>2</p> | <p>9</p> | 
| <p>B</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>3</p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 
| <p>B</p> | <p><a href="gg269273(v=exchg.10).md">JetRollback</a></p> | <p>-1</p> | <p></p> | 
| <p>A</p> | <p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p> | <p></p> | <p>-1</p> | 



Non è consigliabile sostituire un record nella stessa transazione che esegue gli aggiornamenti del deposito a un record. In [particolare,](./jet-tableid.md) se un aggiornamento di un record viene preparato con un [JET_TABLEID](./jet-tableid.md) e viene usato un JET_TABLEID diverso per l'aggiornamento del record, il deposito aggiornato andrà perso quando viene chiamato [JetUpdate.](./jetupdate-function.md) Ciò si verifica anche se la colonna di deposito non è stata impostata durante l'aggiornamento.

Quando una colonna aggiornabile con deposito a garanzia ha un valore pari a zero, è possibile attivare un comportamento speciale. Questo comportamento si verifica solo se **un'operazione JetEscrowUpdate** fa sì che la colonna abbia un valore pari a zero. L'azione non viene eseguita immediatamente, ma si verifica a volte dopo la transazione che ha causato il commit della colonna con un valore pari a zero. La colonna deve comunque avere un valore pari a zero, ovvero se nessuna altra sessione ha modificato la colonna. Se la colonna è stata creata con JET_bitColumnDeleteOnZero, il record contenente la colonna verrà eliminato. Se la colonna è stata creata con JET_bitColumnFinalize verrà generato un callback. Un arresto anomalo del sistema potrebbe causare la non esecuzione di queste azioni, ma la manutenzione online (tramite la [funzione JetDefragment)](./jetdefragment-function.md) ripulirà correttamente le azioni.

#### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
