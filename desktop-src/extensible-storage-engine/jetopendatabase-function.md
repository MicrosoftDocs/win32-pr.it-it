---
description: 'Altre informazioni su: funzione JetOpenDatabase'
title: Funzione JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760538"
---
# <a name="jetopendatabase-function"></a>Funzione JetOpenDatabase


_**Si applica a:** Windows | Windows Server_

## <a name="jetopendatabase-function"></a>Funzione JetOpenDatabase

La funzione **JetOpenDatabase** apre un database precedentemente collegato, usando le funzioni [JetAttachDatabase](./jetattachdatabase-function.md) o [JetAttachDatabase2](./jetattachdatabase2-function.md) , da usare con una sessione di database. Questa funzione può essere chiamata più volte per lo stesso database.

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*szFilename*

Nome del database da aprire.

*szConnect*

Riservato. Impostata su NULL.

*pdbid*

Puntatore a un buffer che, in una chiamata con esito positivo, contiene l'identificatore del database. Se la chiamata ha esito negativo, il valore non è definito.

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
<td><p>JET_bitDbExclusive</p></td>
<td><p>Consente la connessione di un database a una singola sessione. In genere, diverse sessioni possono aprire un database.</p></td>
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
<td><p>JET_errDatabaseInUse</p></td>
<td><p>L'accesso esclusivo è stato richiesto, ma non è stato possibile concederlo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>È stato specificato un percorso non valido in <em>szFileName</em>. <em>szFileName</em> deve essere diverso da null e fare riferimento a un file valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Un'altra sessione ha già aperto il database in modo esclusivo (usando JET_bitDbExclusive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>Il database non è stato collegato in precedenza (vedere <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>È stato effettuato un tentativo di aprire un file che non è un file di database valido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>È stato effettuato un tentativo di aprire più di un database e <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> è stato impostato. Per ulteriori informazioni, vedere <a href="gg294139(v=exchg.10).md">parametri di sistema</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>Il file è stato collegato come di sola lettura, ma <strong>JetOpenDatabase</strong> non ha superato JET_bitDbReadOnly. Il database viene ancora aperto con accesso in sola lettura.</p></td>
</tr>
</tbody>
</table>


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
<td><p>Implementato come <strong>JetOpenDatabaseW</strong> (Unicode) e <strong>JetOpenDatabaseA</strong> (ANSI).</p></td>
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
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
