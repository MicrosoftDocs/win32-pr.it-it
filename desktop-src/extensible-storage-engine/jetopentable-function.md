---
description: 'Altre informazioni su: funzione JetOpenTable'
title: Funzione JetOpenTable
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749706"
---
# <a name="jetopentable-function"></a>Funzione JetOpenTable


_**Si applica a:** Windows | Windows Server_

## <a name="jetopentable-function"></a>Funzione JetOpenTable

La funzione **JetOpenTable** apre un cursore su una tabella creata in precedenza.

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da utilizzare.

*dbid*

Identificatore del database da utilizzare per trovare la tabella.

*szTableName*

Nome della tabella da aprire.

*pvParameters*

Deprecato. Impostare su **null**.

*cbParameters*

Deprecato. Impostare su 0 (zero).

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
<td><p>JET_bitTableDenyRead</p></td>
<td><p>Non è possibile aprire la tabella per l'accesso in lettura da parte di un'altra sessione di database.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableDenyWrite</p></td>
<td><p>Non è possibile aprire la tabella per l'accesso in scrittura da parte di un'altra sessione di database.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableNoCache</p></td>
<td><p>Non memorizzare nella cache le pagine per questa tabella.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTablePermitDDL</p></td>
<td><p>Consente la modifica DDL nelle tabelle contrassegnate come FixedDDL. Questa opzione deve essere utilizzata con l'opzione JET_bitTableDenyRead.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTablePreread</p></td>
<td><p>Fornisce un suggerimento che la tabella non è probabilmente nella cache del buffer e che la pre-lettura può essere utile per le prestazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableReadOnly</p></td>
<td><p>Richiede l'accesso in sola lettura alla tabella.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableSequential</p></td>
<td><p>La tabella deve essere precaricata in modo molto aggressivo dal disco poiché verrà analizzata in sequenza dall'applicazione.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableUpdatable</p></td>
<td><p>Richiede l'accesso in scrittura alla tabella.</p></td>
</tr>
</tbody>
</table>


*pTableID*

In seguito all'esito positivo, punta all'identificatore della tabella. In caso di errore, il contenuto di *pTableID* non è definito.

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
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p><em>dbid</em> non è un identificatore di database valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>È stata passata una combinazione non valida di <em>grbit</em> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Il nome specificato in <em>szTableName</em> non è valido.</p>
<p>Per ulteriori informazioni sui nomi di tabella validi, vedere il parametro <em>szTableName</em> in <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>È stato effettuato un tentativo di aprire una tabella che non esiste nel database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore. Vedere la sezione relativa alle osservazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableInUse</p></td>
<td><p>La tabella è utilizzata da un'altra operazione di database.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>Avviso non irreversibile che indica che la tabella è utilizzata dal sistema.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>La tabella è bloccata da un'altra operazione di database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>È stato effettuato un tentativo di apertura di un numero eccessivo di tabelle univoche in una sola volta. Vedere la sezione relativa alle osservazioni.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Le tabelle aperte con **JetOpenTable** devono essere in genere chiuse con [JetCloseTable](./jetclosetable-function.md). L'eccezione a questa regola si verifica quando **JetOpenTable** viene chiamato in una transazione e viene eseguito il rollback della transazione (con [JetRollback](./jetrollback-function.md)). Quando si esegue il rollback di una transazione, la tabella viene chiusa automaticamente. In questo caso, è un errore chiudere la tabella con [JetCloseTable](./jetclosetable-function.md).

È lecito aprire le tabelle di sistema con **JetOpenTable** , ad esempio MSysObjects, MSysUnicodeFixup. È possibile che lo schema delle tabelle di sistema venga modificato, pertanto l'accesso alle tabelle di sistema è sconsigliato. Il numero di tabelle univoche che possono essere aperte contemporaneamente è interessato direttamente da *JET_paramMaxOpenTables*. Se la tabella è attualmente aperta, verrà creato un nuovo cursore nella tabella. Le risorse del cursore vengono configurate utilizzando [JetSetSystemParameter](./jetsetsystemparameter-function.md) con *JET_paramMaxCursors*. Vedere anche [JetDupCursor](./jetdupcursor-function.md).

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
<td><p>Implementato come <strong>JetOpenTableW</strong> (Unicode) e <strong>JetOpenTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri delle risorse](./resource-parameters.md)
