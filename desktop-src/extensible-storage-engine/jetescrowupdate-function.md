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
ms.openlocfilehash: d244bf16ab02d0bfd6f975f63c2ece32ed40119b30c178e4674037d36f519508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667421"
---
# <a name="jetescrowupdate-function"></a>Funzione JetEscrowUpdate


_**Si applica a:** Windows | Windows Server_

## <a name="jetescrowupdate-function"></a>Funzione JetEscrowUpdate

La **funzione JetEscrowUpdate** esegue un'operazione di addizione atomica su una colonna. Questa funzione consente a più sessioni di aggiornare lo stesso record contemporaneamente senza conflitti.

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

Puntatore a un buffer contenente il componente aggiuntivo per la colonna.

*cbMax*

Dimensione del buffer contenente il componente aggiuntivo.

*pvOld*

Buffer di output che riceverà il valore corrente della colonna come archiviato nel database (il controllo delle versioni viene ignorato).

*cbOldMax*

Dimensione massima del buffer di output che riceverà il valore corrente della colonna. Attualmente è JET_coltypLong supportato solo il buffer, quindi la lunghezza del buffer deve essere di 4 byte o 0 byte. Se *pvOld* è NULL, *cbOldMax* deve essere 0.

*pcbOldActual*

Riceve la quantità effettiva di dati di valore non elaborati ricevuti nel buffer di output.

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
<td><p>Anche se la sessione che esegue l'aggiornamento del deposito ha eseguito il rollback delle transazioni, questo aggiornamento non verrà annullato. Si noti che poiché i record di log potrebbero non essere scaricati su disco, gli aggiornamenti recenti del deposito emersi con questo flag potrebbero andare persi in caso di arresto anomalo.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>Il cursore dispone di un aggiornamento preparato <a href="gg269339(v=exchg.10).md">con JetPrepareUpdate</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>È stata passata una dimensione del buffer non valida. Attualmente è JET_coltypLong supportato solo il buffer, quindi il buffer deve essere di 4 byte.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOperation</p></td>
<td><p>È stata specificata una colonna non valida. La colonna deve essere creata con JET_bitColumnEscrowUpdate specificato. Solo le colonne fisse JET_coltypLong possono essere specificate come aggiornabili per il deposito.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Per aggiornare una colonna, il cursore deve essere posizionato su un record.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Gli aggiornamenti del deposito possono essere eseguiti solo dalle sessioni in una transazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è stata ancora inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Il cursore non può essere di sola lettura e aggiornare un record.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La stessa sessione non può essere usata da più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
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

In genere, se due sessioni tentano di aggiornare un record contemporaneamente, la seconda sessione riceverà un errore JET_errWriteConflict a meno che le sessioni non siano completamente serializzate. Per serializzare due sessioni che aggiornano lo stesso record, la seconda sessione deve avviare la transazione dopo che la prima transazione ha eseguito il commit della transazione. Per [altre informazioni, vedere JetBeginTransaction.](./jetbegintransaction-function.md)

È possibile aggiornare il deposito di più colonne nello stesso record. Gli aggiornamenti non influiscono l'uno sull'altro.

Solo **le operazioni JetEscrowUpdate** sono compatibili tra loro. Se due sessioni diverse tentano di preparare gli aggiornamenti o eliminare lo stesso record, verrà generato un conflitto di scrittura.

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


Le operazioni di deposito sono con controllo delle versioni e vengono annullate usando [JetRollback](./jetrollback-function.md) (a meno JET_bitEscrowNoRollback specificato). **JetEscrowUpdate** restituisce il valore non elaborato della colonna archiviata nel database, perché un'applicazione potrebbe voler eseguire un'azione speciale quando viene raggiunto un valore sentinel. [JetRetrieveColumn](./jetretrievecolumn-function.md) restituisce la visualizzazione con versione corretta della colonna, ignorando gli aggiornamenti eseguiti da sessioni simultanee.

Date due sessioni che operano sulla stessa colonna dello stesso record, è possibile vedere come funziona. Si supponga che la colonna inizi con un valore pari a 0.

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


Non è consigliabile sostituire un record nella stessa transazione che esegue gli aggiornamenti del deposito a un record. In [particolare,](./jet-tableid.md) se un aggiornamento di un record viene preparato con un [JET_TABLEID](./jet-tableid.md) e viene usato un JET_TABLEID diverso per l'aggiornamento del record, il deposito aggiornato andrà perso quando viene chiamato [JetUpdate.](./jetupdate-function.md) Ciò si verifica anche se la colonna di deposito non è stata impostata durante l'aggiornamento.

Quando una colonna aggiornabile con deposito a garanzia ha un valore pari a zero, è possibile attivare un comportamento speciale. Questo comportamento si verifica solo se **un'operazione JetEscrowUpdate** fa sì che la colonna abbia un valore pari a zero. L'azione non viene eseguita immediatamente, ma si verifica a volte dopo la transazione che ha causato il commit della colonna con un valore pari a zero. La colonna deve comunque avere un valore pari a zero, ovvero se nessuna altra sessione ha modificato la colonna. Se la colonna è stata creata con JET_bitColumnDeleteOnZero, il record contenente la colonna verrà eliminato. Se la colonna è stata creata con JET_bitColumnFinalize verrà generato un callback. Un arresto anomalo del sistema può causare la non esecuzione di queste azioni, ma la manutenzione online (tramite la [funzione JetDefragment)](./jetdefragment-function.md) ripristina correttamente le azioni.

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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
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
