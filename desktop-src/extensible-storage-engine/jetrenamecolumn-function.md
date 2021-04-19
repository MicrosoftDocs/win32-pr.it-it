---
description: 'Altre informazioni su: funzione JetRenameColumn'
title: JetRenameColumn (funzione)
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317342"
---
# <a name="jetrenamecolumn-function"></a>JetRenameColumn (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetrenamecolumn-function"></a>JetRenameColumn (funzione)

La funzione **JetRenameColumn** può essere utilizzata per modificare il nome di una colonna esistente in una tabella.

**Windows XP:**  **JetRenameColumn** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*TableID*

Cursore da utilizzare per questa chiamata.

*szName*

Nome corrente della colonna che verrà rinominata.

*szNameNew*

Nuovo nome per la colonna che verrà rinominata.

*grbit*

Questo parametro deve essere 0.

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
<td><p>JET_errColumnNotFound</p></td>
<td><p>Questa colonna specificata non esiste per questa tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Uno dei nomi di oggetto specificati non è valido. Tutti i nomi di oggetto devono essere conformi allo stesso set di regole. Le regole sono le seguenti:</p>
<ul>
<li><p>I nomi degli oggetti devono essere composti da caratteri ASCII.</p></li>
<li><p>I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</p></li>
<li><p>I nomi degli oggetti non possono superare la lunghezza di JET_cbNameMost (64) caratteri.</p></li>
<li><p>I nomi degli oggetti non possono iniziare con un nome di oggetto spazio. non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</p></li>
<li><p>I nomi degli oggetti non possono contenere punti esclamativi (!), punti (.), parentesi quadra aperta ([) o parentesi quadra chiusa (]).</p></li>
<li><p>Una volta convalidata, solo la parte della stringa fino al primo spazio (se presente) verrà utilizzata per il nome dell'oggetto. Ciò significa che i nomi degli oggetti non possono contenere uno spazio.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro. Questo problema può verificarsi per <strong>JetRenameColumn</strong> quando:</p>
<ul>
<li><p><em>szName</em> è null.</p></li>
<li><p><em>szNameNew</em> è null.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Questa operazione può essere eseguita solo quando la sessione non si trova attualmente all'interno di una transazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Non è possibile eseguire un aggiornamento all'interno dell'ambito di una transazione di sola lettura. Una transazione di sola lettura è una transazione che è stata avviata utilizzando una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il nome della colonna specificata nella tabella associata al cursore viene impostato in modo permanente sul nuovo nome. Verranno aggiornati anche tutti gli indici che fanno riferimento a tale colonna.

In caso di errore, non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

L'operazione di ridenominazione delle colonne è insolita perché, a differenza di altre operazioni dello schema, non viene eseguita come transazione. Quando una colonna in una determinata tabella viene rinominata in una sessione, qualsiasi altra sessione che utilizza tale tabella visualizzerà immediatamente la modifica, anche se si trovano in una transazione che impedisce a tale sessione di visualizzare le altre modifiche apportate dalla sessione durante l'operazione di ridenominazione.

L'ID di colonna di una colonna non è influenzato dall'operazione di ridenominazione.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetRenameColumnW</strong> (Unicode) e <strong>JetRenameColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
