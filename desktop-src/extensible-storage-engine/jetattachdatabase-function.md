---
description: 'Altre informazioni su: funzione JetAttachDatabase'
title: Funzione JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225879"
---
# <a name="jetattachdatabase-function"></a>Funzione JetAttachDatabase


_**Si applica a:** Windows | Windows Server_

## <a name="jetattachdatabase-function"></a>Funzione JetAttachDatabase

La funzione **JetAttachDatabase** connette un file di database per l'utilizzo con un'istanza di database. Per utilizzare il database, sarà necessario aprirlo successivamente con [JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*szFilename*

Nome del database da aggiungere.

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
<td><p>JET_bitDbDeleteCorruptIndexes</p></td>
<td><p>Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> è stato impostato, verranno eliminati tutti gli indici sui dati Unicode. Per altre informazioni, vedere le sezione Osservazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbDeleteUnicodeIndexes</p></td>
<td><p>Tutti gli indici sui dati Unicode verranno eliminati, indipendentemente dall'impostazione di <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Per altre informazioni, vedere le sezione Osservazioni.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbUpgrade</p></td>
<td><p>Obsoleta. Non usare.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbReadOnly</p></td>
<td><p>Impedisce le modifiche al database.</p></td>
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
<td><p>JET_errFileAccessDenied</p></td>
<td><p>Il motore di database non è in grado di aprire il file di database. Il file potrebbe essere in uso da un altro processo oppure il chiamante potrebbe non disporre di privilegi sufficienti per aprire il file.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileNotFound</p></td>
<td><p>Il file specificato in <em>szFileName</em> non esiste.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted</p></td>
<td><p>Si è verificato un errore con l'indice primario. Questo problema può essere dovuto a un danneggiamento fisico, ad esempio un danneggiamento del disco o della memoria. Può anche essere restituito quando si collega un database modificato per ultimo in un sistema operativo precedente e l'indice primario si trova su una colonna con dati Unicode. Per ulteriori informazioni sugli indici sui dati Unicode, vedere la sezione Osservazioni.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted</p></td>
<td><p>Si è verificato un errore con un indice secondario. Questo problema può essere dovuto a un danneggiamento fisico, ad esempio un danneggiamento del disco o della memoria. Può anche essere restituito quando si collega un database modificato per ultimo in un sistema operativo precedente e un indice secondario si trova su una colonna con dati Unicode. Per ulteriori informazioni sugli indici sui dati Unicode, vedere la sezione Osservazioni. Gli indici secondari vengono completamente ricompilati quando un database viene deframmentato con un'utilità offline usando il comando seguente: <strong>Esentutl-d</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Per ogni istanza è possibile collegare solo un numero finito di database. Il limite è attualmente di sette database per ogni istanza.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Avviso non irreversibile che indica che il file di database è già stato allegato da questa sessione.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

La chiamata a **JetAttachDatabase** equivale alla chiamata a [JetAttachDatabase2](./jetattachdatabase2-function.md) e al passaggio di un valore pari a zero, ovvero non esiste alcun limite per il parametro *cpgDatabaseSizeMax* .

Se si connette un database scrivibile, ovvero se JET_bitDbReadOnly non è stato specificato nel parametro *grbit* , il file verrà aperto esclusivamente a livello di sistema operativo. Nessun altro processo sarà in grado di aprire il file. È possibile che più processi alleghino un singolo database aprendoli in modalità di sola lettura.

Il file di database viene scollegato tramite [JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Parametri di controllo degli indici

Diverse versioni di Windows normalizzano il testo Unicode in modi diversi. Ciò significa che gli indici compilati in una versione di Windows potrebbero non funzionare in altre versioni.

Prima di Windows Server 2003, quando la versione del sistema operativo è cambiata (inclusa l'installazione di un Service Pack), ogni indice sui dati Unicode si trovava in uno stato potenzialmente danneggiato.

Gli indici creati in Windows Server 2003 e versioni successive vengono contrassegnati con la versione di normalizzazione Unicode con cui sono stati compilati. Gli indici meno recenti non contengono informazioni sulla versione. La maggior parte delle modifiche di normalizzazione Unicode è costituita dall'aggiunta di nuovi caratteri, i punti di codice precedentemente non definiti sono ora definiti e normalizzati in modo diverso. Pertanto, se i dati binari vengono archiviati in una colonna Unicode, verranno normalizzati in modo diverso Man seconda che vengono definiti nuovi punti di codice.

A partire da Windows Server 2003, il motore di database ESE tiene traccia delle voci di indice Unicode contenenti punti di codice non definiti. Questi possono essere usati per correggere un indice quando viene modificato il set di caratteri Unicode definiti.

Questi parametri controllano cosa accade quando il motore di database ESE si connette a un database usato per l'ultima volta in una build diversa del sistema operativo. La versione del sistema operativo è contrassegnata nell'intestazione del database.

Se [JET_paramEnableIndexChecking](./database-parameters.md) è impostato su **true** e il database contiene indici potenzialmente danneggiati:

  - **JetAttachDatabase** eliminerà gli indici potenzialmente danneggiati se *grbit* contiene JET_bitDbDeleteCorruptIndexes

  - **JetAttachDatabase** restituirà un errore se *grbit* non contiene JET_bitDbDeleteCorruptIndexes e sono presenti indici che necessitano dell'eliminazione.

Se [JET_paramEnableIndexChecking](./database-parameters.md) è impostato su **false**:

  - **JetAttachDatabase** ignorerà gli indici potenzialmente danneggiati e restituirà JET_errSuccess (presupponendo che non siano presenti altri errori).

Windows Server 2003 e versioni successive: se [JET_paramEnableIndexChecking](./database-parameters.md) non è stato reimpostato, la tabella di correzione interna verrà utilizzata per la correzione delle voci di indice. Questa operazione potrebbe non correggere tutti i danneggiamenti dell'indice ma sarà trasparente per l'applicazione.

Se il database è stato collegato come di sola lettura, non è possibile correggere o eliminare l'indice. In questo caso, l'API restituirà invece un errore, ad esempio JET_errSecondaryIndexCorrupted o JET_errPrimaryIndexCorrupted.

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
<td><p>Implementato come <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[File del motore di archiviazione estendibile](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetDetachDatabase2](./jetdetachdatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
