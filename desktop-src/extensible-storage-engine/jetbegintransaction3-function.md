---
description: Altre informazioni sulla funzione JetBeginTransaction3
title: Funzione JetBeginTransaction3
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 576f2a642fb68f0121828eb4f34e0bb59d507f3f4e67134da0d259405003dbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117892089"
---
# <a name="jetbegintransaction3-function"></a>Funzione JetBeginTransaction3


_**Si applica a:** Windows | Windows Server_

La **funzione JetBeginTransaction3** determina l'immissione di una transazione in una sessione e la creazione di un nuovo punto di salvataggio. Questa funzione può essere chiamata più volte in una singola sessione per creare punti di salvataggio aggiuntivi. Questi punti di salvataggio possono essere usati per mantenere o annullare le modifiche al database in modo selettivo.

La **funzione JetBeginTransaction3** è stata introdotta nel Windows 8 operativo.

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*trxid*

Identificatore facoltativo fornito dall'utente per identificare la transazione.

*grbit*

Gruppo di bit che specifica zero o più valori dell'opzione di chiamata elencati nella tabella seguente.

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
<td><p>JET_bitTransactionReadOnly</p></td>
<td><p>La transazione non modificherà il database. Se si tenta di eseguire un aggiornamento, l'operazione avrà esito negativo con JET_errTransReadOnly di risposta. Questa opzione viene ignorata a meno che non venga richiesta quando la sessione specificata non è già in una transazione. Questa opzione è disponibile nelle versioni del Windows operativo a partire da Windows XP.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti elencati nella tabella seguente. Per altre informazioni sui possibili errori ESE [(Extensible](./extensible-storage-engine-errors.md) Archiviazione Engine), vedere Extensible Archiviazione Engine Errors and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cessare in seguito a una chiamata alla <a href="gg269240(v=exchg.10).md">funzione JetStopService.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati.</p>
<p>Questo codice restituito viene restituito dalle versioni di Windows a partire da Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore viene restituito dalle versioni di Windows a partire da Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep</p></td>
<td><p>Non è possibile avviare una nuova transazione perché la sessione è già alla profondità massima del punto di salvataggio consentita dal motore di database.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, la sessione specificata si trova all'interno di una transazione. Se in precedenza la sessione era all'interno di una transazione, verrà creato un nuovo punto di salvataggio.

In caso di errore, lo stato transazionale della sessione rimarrà invariato. Non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Per altre informazioni sul funzionamento delle transazioni, vedere [JetBeginTransaction.](./jetbegintransaction-function.md)

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2012.</p></td>
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


#### <a name="see-also"></a>Vedi anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
