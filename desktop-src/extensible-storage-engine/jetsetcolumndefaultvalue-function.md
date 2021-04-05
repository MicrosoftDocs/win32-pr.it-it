---
description: 'Altre informazioni su: funzione JetSetColumnDefaultValue'
title: JetSetColumnDefaultValue (funzione)
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f50d30b2edeca716895d8dd2339d659f0e1382f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878841"
---
# <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue (funzione)

La funzione **JetSetColumnDefaultValue** può essere utilizzata per modificare il valore predefinito di una colonna esistente.

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

*dbid*

Database da utilizzare per questa chiamata.

*szTableName*

Nome della tabella contenente la colonna interessata.

*szColumnName*

Nome della colonna il cui valore predefinito verrà modificato.

*pvData*

Buffer di input contenente il nuovo valore predefinito.

*cbData*

Dimensioni del buffer di input contenente il nuovo valore predefinito.

*grbit*

Riservato per utilizzi futuri.

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
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Uguale a JET_errNullInvalid.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnInUse</p></td>
<td><p>Questa colonna specificata è attualmente utilizzata da un indice.</p>
<p><strong>JetSetColumnDefaultValue</strong> non è in grado di modificare il valore predefinito di una colonna a cui si fa riferimento nella definizione di un indice. Ciò è dovuto al fatto che questa operazione potrebbe modificare il contenuto dell'indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Questa colonna specificata non esiste per questa tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>L'ID database specificato non è valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Uno dei nomi di oggetto specificati non è valido. Tutti i nomi di oggetto devono essere conformi allo stesso set di regole. Le regole sono le seguenti:</p>
<ul>
<li><p>I nomi degli oggetti devono essere composti da caratteri ASCII.</p></li>
<li><p>I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</p></li>
<li><p>I nomi degli oggetti non possono superare la lunghezza di JET_cbNameMost (64) caratteri.</p></li>
<li><p>I nomi degli oggetti non possono iniziare con uno spazio.</p></li>
<li><p>I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</p></li>
<li><p>I nomi degli oggetti non possono contenere punti esclamativi (!), punti (.), parentesi quadra aperta ([) o parentesi quadra chiusa (]).</p></li>
<li><p>Una volta convalidata, solo la parte della stringa fino al primo spazio (se presente) verrà utilizzata per il nome dell'oggetto. Ciò significa che i nomi degli oggetti non possono contenere uno spazio.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullInvalid</p></td>
<td><p>Impossibile impostare la colonna su NULL. Questo errore si verifica per <strong>JetSetColumnDefaultValue</strong> quando:</p>
<ul>
<li><p><em>cbData</em> è zero.</p></li>
<li><p><strong>pvData</strong> è null.</p></li>
</ul>
<p>Pertanto, non è possibile impostare il valore predefinito di una colonna (indietro) su NULL o su un valore di lunghezza zero.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>La tabella specificata non esiste per questo database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Non è possibile usare la stessa sessione per più di un thread nello stesso momento. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Questa tabella specificata è utilizzata da un'altra sessione.</p>
<p><strong>JetSetColumnDefaultValue</strong> richiede l'accesso esclusivo a una tabella per poter modificare il valore predefinito della colonna per le versioni precedenti a Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Non è consentito tentare un aggiornamento quando si trova all'interno dell'ambito di una transazione di sola lettura. Una transazione di sola lettura è una transazione che è stata avviata utilizzando una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Un'altra sessione ha bloccato in precedenza il record per l'aggiornamento. Il tentativo di aggiornamento da questa sessione avrà esito negativo.</p></td>
</tr>
</tbody>
</table>


In seguito all'esito positivo, il valore predefinito della colonna specificata nella tabella specificata nel database specificato verrà modificato in modo permanente sul nuovo valore predefinito.

In caso di errore, non si verificherà alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Non è possibile modificare il valore predefinito di una colonna in una tabella del modello.

Il motore di database tronca automaticamente il valore predefinito di una colonna a 255 byte per il testo lungo e le colonne binarie lunghe.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetSetColumnDefaultValueW</strong> (Unicode) e <strong>JetSetColumnDefaultValueA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[JetStopService](./jetstopservice-function.md)
