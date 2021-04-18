---
description: 'Altre informazioni su: funzione JetEscrowUpdate'
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
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316453"
---
# <a name="jetescrowupdate-function"></a>Funzione JetEscrowUpdate


_**Si applica a:** Windows | Windows Server_

## <a name="jetescrowupdate-function"></a>Funzione JetEscrowUpdate

La funzione **JetEscrowUpdate** esegue un'operazione di addizione atomica su una colonna. Questa funzione consente a più sessioni di aggiornare simultaneamente lo stesso record senza conflitti.

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

*TableID*

Cursore da utilizzare per questa chiamata.

*ColumnID*

*ColumnID* della colonna da aggiornare.

*PV*

Puntatore a un buffer contenente Addend per la colonna.

*cbMax*

Dimensioni del buffer che contiene Addend.

*pvOld*

Il buffer di output che riceverà il valore corrente della colonna archiviato nel database (il controllo delle versioni viene ignorato).

*cbOldMax*

Dimensione massima del buffer di output che riceverà il valore corrente della colonna. Attualmente è supportata solo JET_coltypLong, quindi il buffer deve avere una lunghezza di 4 byte o di 0 byte. Se *pvOld* è null, *cbOldMax* deve essere 0.

*pcbOldActual*

Riceve la quantità effettiva di dati del valore non elaborato ricevuti nel buffer di output.

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
<td><p>JET_bitEscrowNoRollback</p></td>
<td><p>Anche se la sessione che esegue l'aggiornamento del deposito a garanzia ha il rollback della transazione, questo aggiornamento non verrà annullato. Si noti che, poiché è possibile che i record del log non vengano scaricati su disco, gli aggiornamenti del deposito recenti eseguiti con questo flag potrebbero andare persi in caso di arresto anomalo del sistema.</p></td>
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
<td><p>JET_errAlreadyPrepared</p></td>
<td><p>Per il cursore è stato preparato un aggiornamento con <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>È stata passata una dimensione del buffer non valida. Attualmente è supportata solo JET_coltypLong, quindi il buffer deve essere di 4 byte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOperation</p></td>
<td><p>È stata specificata una colonna non valida. La colonna deve essere creata con JET_bitColumnEscrowUpdate specificato. È possibile specificare solo colonne fisse di JET_coltypLong come aggiornabili con deposito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Per aggiornare una colonna, è necessario che il cursore si trovi in un record.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Gli aggiornamenti del deposito possono essere eseguiti solo da sessioni in una transazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Il cursore non può essere di sola lettura e aggiornare un record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione da più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La sessione deve disporre delle autorizzazioni di scrittura per aggiornare un record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Errore restituito quando viene richiesto un aggiornamento in conflitto.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

In genere, se due sessioni tentano di aggiornare contemporaneamente un record, la seconda sessione riceverà un errore di JET_errWriteConflict, a meno che le sessioni non siano completamente serializzate. Per serializzare due sessioni che aggiornano lo stesso record, la seconda sessione deve avviare la relativa transazione dopo che la prima transazione ha eseguito il commit della transazione. Per ulteriori informazioni, vedere [JetBeginTransaction](./jetbegintransaction-function.md) .

È possibile aggiornare più colonne nello stesso record. Gli aggiornamenti non interessano.

Solo le operazioni **JetEscrowUpdate** sono compatibili tra loro. Se due diverse sessioni tentano di preparare gli aggiornamenti o di eliminare lo stesso record, verrà generato un conflitto di scrittura.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p>Sessione B<br />
<strong>JetEscrowUpdate</strong></p></th>
<th><p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></p></th>
<th><p><a href="gg269315(v=exchg.10).md">JetDelete</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>JetEscrowUpdate</strong></p></td>
<td><p>JET_errSuccess</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><a href="gg269288(v=exchg.10).md">JetUpdate</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="odd">
<td><p>Sessione A</p></td>
<td><p><a href="gg269315(v=exchg.10).md">JetDelete</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
</tbody>
</table>


Le operazioni di deposito con versione vengono annullate con [JetRollback](./jetrollback-function.md) , a meno che non sia stato specificato JET_bitEscrowNoRollback. **JetEscrowUpdate** restituisce il valore non elaborato della colonna archiviata nel database, perché un'applicazione potrebbe voler eseguire un'azione speciale quando viene raggiunto un valore sentinel. [JetRetrieveColumn](./jetretrievecolumn-function.md) restituisce la visualizzazione con versione corretta della colonna ignorando gli aggiornamenti effettuati dalle sessioni simultanee.

Date due sessioni che operano sulla stessa colonna dello stesso record, possiamo vedere come funziona. Si supponga che la colonna inizi con un valore pari a 0.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Sessione</p></th>
<th><p>Operazione</p></th>
<th><p>Valore archiviato</p></th>
<th><p>Valore restituito</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>A</p></td>
<td><p><strong>JetEscrowUpdate</strong> (4)</p></td>
<td><p>4</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><strong>JetEscrowUpdate</strong> (3)</p></td>
<td><p>7</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p>A</p></td>
<td><p><strong>JetEscrowUpdate</strong> (2)</p></td>
<td><p>9</p></td>
<td><p>7</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><strong>JetEscrowUpdate</strong> (-7)</p></td>
<td><p>2</p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269273(v=exchg.10).md">JetRollback</a></p></td>
<td><p>-1</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
</tbody>
</table>


La sostituzione di un record nella stessa transazione che esegue gli aggiornamenti del deposito a un record non è consigliata. In particolare, se un aggiornamento su un record viene preparato con una [JET_TABLEID](./jet-tableid.md) e un [JET_TABLEID](./jet-tableid.md) diverso viene usato per l'aggiornamento del record, il deposito verrà perso quando viene chiamato [JetUpdate](./jetupdate-function.md) . Ciò si verifica anche se la colonna escrow non è stata impostata durante l'aggiornamento.

Quando una colonna aggiornabile del deposito ha un valore pari a zero, è possibile attivare un comportamento speciale. Questo comportamento si verifica solo se un'operazione **JetEscrowUpdate** fa sì che la colonna abbia un valore pari a zero. L'azione non viene eseguita immediatamente, ma si verifica talvolta dopo la transazione che ha causato la presenza di un valore pari a zero commit per la colonna. La colonna deve avere ancora un valore pari a zero (ovvero se nessuna altra sessione ha modificato la colonna). Se la colonna è stata creata con JET_bitColumnDeleteOnZero, il record contenente la colonna verrà eliminato. Se la colonna è stata creata con JET_bitColumnFinalize, verrà emesso un callback. Un arresto anomalo del sistema può causare la mancata verifica di queste azioni, ma la manutenzione in linea (tramite la funzione [JetDefragment](./jetdefragment-function.md) ) ripeterà correttamente le azioni.

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
