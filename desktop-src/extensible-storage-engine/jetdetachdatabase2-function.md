---
description: 'Altre informazioni su: funzione JetDetachDatabase2'
title: Funzione JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7688df9a18d8e13a85e4a244fc8502a7147e154f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315621"
---
# <a name="jetdetachdatabase2-function"></a>Funzione JetDetachDatabase2


_**Si applica a:** Windows | Windows Server_

## <a name="jetdetachdatabase2-function"></a>Funzione JetDetachDatabase2

La funzione **JetDetachDatabase2** rilascia un file di database precedentemente collegato a una sessione di database.

**Windows XP:**  **JetDetachDatabase2** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*szFilename*

Nome del database da scollegare. Se *szFileName* è **null** o una stringa vuota, tutti i database collegati a *sesid* verranno scollegati.

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
<td><p>JET_bitForceCloseAndDetach</p></td>
<td><p>Impone la chiusura e lo scollegamento del database. Se JET_bitForceCloseAndDetach non è supportato, verrà restituito JET_errForceDetachNotAllowed.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitForceDetach</p></td>
<td><p>Forza la disconnessione del database. Se JET_bitForceDetach non è supportato, verrà restituito JET_errForceDetachNotAllowed.</p></td>
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
<td><p>JET_errBackupInProgress</p></td>
<td><p>È in corso il backup del database e non è possibile scollegarlo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Il database è stato aperto da <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>. Prima dello scollegamento, è necessario chiudere i database.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> o <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errForceDetachNotAllowed</p></td>
<td><p>JET_bitForceDetach non è supportato.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>È stato effettuato un tentativo di scollegamento di un database in una transazione.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Se un database collegato è stato aperto (con [JetAttachDatabase](./jetattachdatabase-function.md)), è necessario chiuderlo con [JetCloseDatabase](./jetclosedatabase-function.md) prima di disconnetterlo.

Solo Windows 2000: i database che non sono stati scollegati prima della chiamata a [JetTerm](./jetterm-function.md) verranno automaticamente ricollegati al successivo chiamata di [JetInit](./jetinit-function.md) .

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
<td><p>Implementato come <strong>JetDetachDatabase2W</strong> (Unicode) e <strong>JetDetachDatabase2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetInit](./jetinit-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetTerm](./jetterm-function.md)
