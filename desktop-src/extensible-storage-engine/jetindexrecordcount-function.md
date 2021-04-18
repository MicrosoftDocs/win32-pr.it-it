---
description: 'Altre informazioni su: funzione JetIndexRecordCount'
title: JetIndexRecordCount (funzione)
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524966"
---
# <a name="jetindexrecordcount-function"></a>JetIndexRecordCount (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetindexrecordcount-function"></a>JetIndexRecordCount (funzione)

La funzione **JetIndexRecordCount** conta il numero di voci nell'indice corrente dalla posizione corrente in poi. La posizione corrente è inclusa nel conteggio. Il conteggio può essere maggiore del numero totale di record nella tabella se l'indice corrente è su una colonna multivalore e le istanze della colonna hanno più valori. Se la tabella è vuota, verrà restituito 0 per il conteggio.

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*pcrec*

Puntatore a un valore long senza segno per la ricezione del conteggio.

*crecMax*

Numero massimo di record da contare. Il valore 0 di *crecMax* indica che il conteggio è illimitato.

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
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Il cursore non si trova attualmente in un record e la tabella non è vuota.</p>
<p><strong>Windows XP, Windows server 2003, windows 2000 Server e windows 2000 Professional:</strong>  Se il cursore è posizionato in corrispondenza di un indice o di un intervallo di indici vuoti, <strong>JetIndexRecordCount</strong> restituisce erroneamente JET_errNoCurrentRecord.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, il numero esatto di voci di indice, inclusa la posizione corrente e fino a *crecMax* (se non è 0), viene restituito nella lunghezza senza segno a cui punta *pcrec*.

Se questa funzione ha esito negativo, non viene apportata alcuna modifica alla memoria allocata in *precpos*.

#### <a name="remarks"></a>Commenti

Se la tabella non è vuota, il cursore deve essere posizionato sul record dal quale iniziare il conteggio. Il conteggio includerà questo record e verrà conteggiato fino al limite specificato in *crecMax*. Se *crecMax* è 0, l'operazione continuerà a contare fino alla fine dell'indice.

Gli intervalli di indice possono essere utilizzati per creare limitazioni di fine Indice artificiali per il conteggio. In questo modo, è possibile conteggiare esattamente intervalli secondari di un indice. Il cursore deve essere posizionato sulla prima riga nell'intervallo. È necessario impostare la fine della chiave di intervallo, quindi utilizzare [JetSetIndexRange](./jetsetindexrange-function.md) per impostare l'intervallo superiore, in modo inclusivo o esclusivo. Infine, è necessario chiamare **JetIndexRecordCount** per contare esattamente l'intervallo.

**JetIndexRecordCount** rispetta la semantica delle transazioni e restituisce un conteggio accurato per questa particolare sessione nello stato transazionale corrente.

**JetIndexRecordCount** accede alle pagine foglia dell'indice per conteggiare esattamente le voci. Di conseguenza, può eseguire una grande quantità di operazioni di I/O e può essere lenta. Per evitare un carico eccessivo, è necessario utilizzare la limitazione *crecMax* . Se un intervallo è di grandi dimensioni, potrebbe essere possibile contare l'intervallo in modo approssimativo usando [JetGetRecordPosition](./jetgetrecordposition-function.md).

**Windows XP, Windows server 2003, windows 2000 Server e windows 2000 Professional:**  Se il cursore è posizionato in corrispondenza di un indice o di un intervallo di indici vuoti, **JetIndexRecordCount** restituisce erroneamente JET_errNoCurrentRecord anziché restituire un numero di record pari a zero. L'applicazione deve verificare se l'indice o l'intervallo di indici è vuoto in questo caso.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
