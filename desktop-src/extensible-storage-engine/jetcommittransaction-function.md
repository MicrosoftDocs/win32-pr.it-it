---
description: 'Altre informazioni su: funzione JetCommitTransaction'
title: Funzione JetCommitTransaction
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2fe42891aa916a428d63fb68c99f42f38e78993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968433"
---
# <a name="jetcommittransaction-function"></a>Funzione JetCommitTransaction


_**Si applica a:** Windows | Windows Server_

## <a name="jetcommittransaction-function"></a>Funzione JetCommitTransaction

La funzione **JetCommitTransaction** esegue il commit delle modifiche apportate allo stato del database durante il punto di salvataggio corrente e ne esegue la migrazione al punto di salvataggio precedente. Se viene eseguito il commit del punto di salvataggio più esterno, verrà eseguito il commit delle modifiche apportate durante tale punto di salvataggio nello stato del database e la sessione uscirà dalla transazione.

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

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
<td><p>JET_bitCommitLazyFlush</p></td>
<td><p>Viene eseguito il commit della transazione in modo normale, ma questa API non attende che la transazione venga scaricata nel file di log delle transazioni prima di tornare al chiamante. Questo riduce drasticamente la durata di un'operazione di commit al costo della durabilità. Qualsiasi transazione non scaricata nel log prima di un arresto anomalo verrà automaticamente interrotta durante il ripristino dell'arresto anomalo durante la chiamata successiva a <a href="gg294068(v=exchg.10).md">JetInit</a>.</p>
<p>Se si specifica JET_bitWaitLastLevel0Commit o JET_bitWaitAllLevel0Commit, questa opzione viene ignorata.</p>
<p>Se la chiamata a <strong>JetCommitTransaction</strong> non corrisponde alla prima chiamata a <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> per questa sessione, questa opzione viene ignorata. Ciò è dovuto al fatto che l'azione finale che si verifica nel punto di salvataggio più esterno è il fattore determinante se l'intera transazione è effettivamente vincolata al disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWaitAllLevel0Commit</p></td>
<td><p>Tutte le transazioni di cui è stato eseguito il commit in precedenza da una sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente. Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante.</p>
<p>Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</p>
<p>Questa opzione non può essere usata in combinazione con altre opzioni.</p>
<p>Questa opzione è disponibile solo a partire da Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitWaitLastLevel0Commit</p></td>
<td><p>Se la sessione ha precedentemente eseguito il commit di tutte le transazioni che non sono ancora state scaricate nel file di log delle transazioni, è necessario scaricarle immediatamente. Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante. Questa operazione è utile se l'applicazione ha precedentemente eseguito il commit di più transazioni usando JET_bitCommitLazyFlush e ora vuole scaricarle tutte su disco.</p>
<p>Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</p>
<p>Questa opzione non può essere usata in combinazione con altre opzioni.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Una delle opzioni richieste non è valida o non è stata implementata. Questo errore viene restituito da <strong>JetCommitTransaction</strong> quando:</p>
<ul>
<li><p>È stato specificato un <em>grbit</em> non valido.</p></li>
<li><p>JET_bitWaitLastLevel0Commit è stato specificato insieme a un altro <em>grbit</em>.</p></li>
<li><p>JET_bitWaitAllLevel0Commit è stato specificato insieme a un altro <em>grbit</em>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Operazione non riuscita perché la sessione specificata non è in una transazione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p>Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, verrà eseguito il commit di tutte le modifiche apportate al database durante il punto di salvataggio corrente per la sessione specificata e il punto di salvataggio verrà terminato. Se l'ultimo punto di salvataggio per la sessione è stato terminato, la transazione verrà scaricata facoltativamente nel file di log delle transazioni e la sessione uscirà dalla transazione.

In caso di errore, lo stato transazionale della sessione rimarrà invariato. Non si verificherà alcuna modifica allo stato del database. L'applicazione deve chiamare [JetRollback](./jetrollback-function.md) per interrompere la transazione.

#### <a name="remarks"></a>Commenti

È necessario che una chiamata a **JetCommitTransaction** o [JetRollback](./jetrollback-function.md) corrisponda a ogni chiamata a [JetBeginTransaction](./jetbegintransaction-function.md) per una determinata sessione.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction]()  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
