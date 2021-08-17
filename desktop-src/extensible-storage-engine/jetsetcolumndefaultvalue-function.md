---
description: Altre informazioni sulla funzione JetSetColumnDefaultValue
title: Funzione JetSetColumnDefaultValue
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
ms.openlocfilehash: ff0f704c30737d6cfc2d8bd823da8207e8d7d8c3fb4458687baf8bc400718304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117703849"
---
# <a name="jetsetcolumndefaultvalue-function"></a>Funzione JetSetColumnDefaultValue


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetcolumndefaultvalue-function"></a>Funzione JetSetColumnDefaultValue

La **funzione JetSetColumnDefaultValue** può essere usata per modificare il valore predefinito di una colonna esistente.

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

*Dbid*

Database da utilizzare per questa chiamata.

*szTableName*

Nome della tabella contenente la colonna che verrà interessata.

*szColumnName*

Nome della colonna il cui valore predefinito verrà modificato.

*pvData*

Buffer di input contenente il nuovo valore predefinito.

*cbData*

Dimensione del buffer di input contenente il nuovo valore predefinito.

*grbit*

Riservato per utilizzi futuri.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di](./extensible-storage-engine-errors.md) Archiviazione estendibile e Parametri di gestione [degli errori](./error-handling-parameters.md).

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
<td><p>Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono cesse a causa di una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Uguale a JET_errNullInvalid.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnInUse</p></td>
<td><p>Questa colonna specificata è attualmente in uso da un indice.</p>
<p><strong>JetSetColumnDefaultValue non</strong> può modificare il valore predefinito di una colonna a cui viene fatto riferimento nella definizione di un indice. Ciò è dovuto al fatto che questa operazione potrebbe modificare il contenuto dell'indice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Questa colonna specificata non esiste per questa tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede la revoca dell'accesso a tutti i dati per proteggere l'integrità di questi dati. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>L'ID database specificato non è valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Uno dei nomi di oggetto specificati non è valido. Tutti i nomi di oggetto devono essere conformi allo stesso set di regole. Le regole sono le seguenti:</p>
<ul>
<li><p>I nomi degli oggetti devono essere costituiti da caratteri ASCII.</p></li>
<li><p>I nomi degli oggetti devono avere almeno un carattere di lunghezza.</p></li>
<li><p>I nomi degli oggetti non possono superare JET_cbNameMost (64) caratteri.</p></li>
<li><p>I nomi degli oggetti non possono iniziare con uno spazio.</p></li>
<li><p>I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</p></li>
<li><p>I nomi degli oggetti non possono contenere un punto esclamativo (!), un punto (.), una parentesi quadra aperta ([) o una parentesi quadra chiusa (]).</p></li>
<li><p>Dopo la convalida, per il nome dell'oggetto verrà usata solo la parte della stringa fino al primo spazio (se presente). Ciò significa che anche i nomi degli oggetti non possono contenere uno spazio.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullInvalid</p></td>
<td><p>Impossibile impostare la colonna su NULL. Ciò si verifica per <strong>JetSetColumnDefaultValue</strong> quando:</p>
<ul>
<li><p><em>cbData</em> è zero.</p></li>
<li><p><strong>pvData</strong> è NULL.</p></li>
</ul>
<p>Pertanto, non è possibile impostare il valore predefinito di una colonna (indietro) su NULL o su un valore di lunghezza zero.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>La tabella specificata non esiste per questo database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza associata alla sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La stessa sessione non può essere usata per più thread contemporaneamente. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Questa tabella specificata è in uso da un'altra sessione.</p>
<p><strong>JetSetColumnDefaultValue</strong> richiede l'accesso esclusivo a una tabella per modificare il valore predefinito della colonna per le versioni precedenti a Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Non è valido tentare un aggiornamento all'interno dell'ambito di una transazione di sola lettura. Una transazione di sola lettura è una transazione avviata tramite una chiamata a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly. Questo errore verrà restituito solo da Windows XP e versioni successive.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Un'altra sessione ha bloccato in precedenza il record per l'aggiornamento. L'aggiornamento tentato da questa sessione avrà esito negativo.</p></td>
</tr>
</tbody>
</table>


In caso di esito positivo, il valore predefinito della colonna specificata nella tabella specificata nel database specificato viene modificato in modo permanente nel nuovo valore predefinito.

In caso di errore, non verrà apportata alcuna modifica allo stato del database.

#### <a name="remarks"></a>Commenti

Non è possibile modificare il valore predefinito di una colonna in una tabella modello.

Il motore di database tronca automaticamente il valore predefinito di una colonna a 255 byte per le colonne di testo lunghe e binarie lunghe.

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
