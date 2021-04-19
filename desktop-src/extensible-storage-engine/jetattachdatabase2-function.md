---
description: 'Altre informazioni su: funzione JetAttachDatabase2'
title: Funzione JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318103"
---
# <a name="jetattachdatabase2-function"></a>Funzione JetAttachDatabase2


_**Si applica a:** Windows | Windows Server_

## <a name="jetattachdatabase2-function"></a>Funzione JetAttachDatabase2

La funzione **JetAttachDatabase2** connette un file di database per l'utilizzo con un'istanza di database e specifica le dimensioni massime del database. Per utilizzare il database, sarà necessario aprirlo successivamente con [JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione del database che verrà usato per la chiamata API.

*szFilename*

Nome del database da aggiungere.

*cpgDatabaseSizeMax*

Dimensione massima delle pagine del database per il database. Le dimensioni predefinite della pagina del database sono di 4 kilobyte, che possono essere modificate utilizzando la funzione [JetSetSystemParameter](./jetsetsystemparameter-function.md) prima di creare un database.

Il passaggio di zero indica che non viene applicato alcun valore massimo dal motore di database.

*grbit*

Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti:

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
<td><p>JET_bitDbDeleteCorruptIndexes</p></td>
<td><p>Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> è stato impostato, verranno eliminati tutti gli indici sui dati Unicode. Per altre informazioni, vedere le sezione Osservazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbDeleteUnicodeIndexes</p></td>
<td><p>Tutti gli indici sui dati Unicode verranno eliminati, indipendentemente dall'impostazione di <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Per altre informazioni, vedere le sezione Osservazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbReadOnly</p></td>
<td><p>Impedisce le modifiche al database.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbUpgrade</p></td>
<td><p>Riservato per utilizzi futuri.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

La funzione restituisce uno dei codici di errore [JET_ERR](./jet-err.md) . Di seguito sono riportati i più comunemente restituiti. Per un elenco completo degli errori per questa API, vedere [codici di errore del motore di archiviazione estensibile](./extensible-storage-engine-error-codes.md).

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
<td><p>Il connessione di un database non è consentita durante un backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>Il file di database specificato da <em>szFileName</em> deve essere scrivibile. Non è necessario impostare l'attributo Read-Only e il processo in esecuzione deve disporre di privilegi sufficienti per la scrittura nel file.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Il file di database è già aperto da un altro processo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>È stato specificato un percorso non valido in <em>szFileName</em>. <em>szFileName</em> deve essere non null e fare riferimento a un percorso valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>Il file di database è già stato allegato da un'altra sessione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound</p></td>
<td><p>Il file specificato in <em>szFileName</em> non esiste.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Si è verificato un errore con l'indice primario. Questo problema può essere dovuto a un danneggiamento fisico, ad esempio un danneggiamento del disco o della memoria. Può anche essere restituito quando si collega un database modificato per ultimo in un sistema operativo precedente e l'indice primario si trova su una colonna con dati Unicode. Per ulteriori informazioni sugli indici sui dati Unicode, vedere la sezione Osservazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Si è verificato un errore con un indice secondario. Questo problema può essere dovuto a un danneggiamento fisico, ad esempio un danneggiamento del disco o della memoria. Può anche essere restituito quando si collega un database modificato per ultimo in un sistema operativo precedente e un indice secondario si trova su una colonna con dati Unicode. Per ulteriori informazioni sugli indici sui dati Unicode, vedere la sezione Osservazioni. Gli indici secondari vengono completamente ricompilati quando un database viene deframmentato con un'utilità offline usando il comando seguente: <strong>Esentutl-d</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Per ogni istanza è possibile collegare solo un numero finito di database. Il limite è attualmente di sette database per ogni istanza.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Avviso non irreversibile che indica che il file di database è già stato allegato da questa sessione.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Il file di database viene scollegato tramite [JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Vedere [JetAttachDatabase](./jetattachdatabase-function.md) per le note.

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
<td><p>Implementato come <strong>JetAttachDatabase2W</strong> (Unicode) e <strong>JetAttachDatabase2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
