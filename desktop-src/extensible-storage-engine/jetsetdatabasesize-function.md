---
description: Altre informazioni sulla funzione JetSetDatabaseSize
title: Funzione JetSetDatabaseSize
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6759508e42b380f0c1987c2f69b422baf4025d58b0de3c503fdae6d55c15df09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071956"
---
# <a name="jetsetdatabasesize-function"></a>Funzione JetSetDatabaseSize


_**Si applica a:** Windows | Windows Server_

## <a name="jetsetdatabasesize-function"></a>Funzione JetSetDatabaseSize

La **funzione JetSetDatabaseSize** imposta le dimensioni di un file di database non aperto.

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Identifica il contesto della sessione di database da usare per la chiamata API.

*szDatabaseName*

Identifica il nome del file di database di cui modificare le dimensioni.

*Cpg*

Specifica le dimensioni desiderate del database, in pagine.

*pcpgReal*

Puntatore a un numero che riceve le dimensioni del database, in pagine, dopo la chiamata API. Se la chiamata API non è riuscita, il contenuto di *pcpgReal* non è definito.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>JET_errDatabaseInconsistent e JET_errDatabaseDirtyShutdown sono lo stesso valore numerico. Il database le cui dimensioni devono essere modificate deve essere in un arresto pulito, noto come stato coerente. Un database incoerente non è danneggiato, ma richiede la riproduzione dei file di log.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p><em>szDatabaseName</em> non deve essere una stringa vuota non NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>Lo spazio disponibile nel volume non è sufficiente per eseguire l'operazione di crescita. <strong>JetSetDatabaseSize</strong> può anche restituire molti errori correlati ai file, tra cui, ma non solo:</p>
<ul>
<li><p>JET_errDiskIO</p></li>
<li><p>JET_errFileNotFound</p></li>
<li><p>JET_errInvalidPath</p></li>
<li><p>JET_errFileAccessDenied</p></li>
<li><p>JET_errOutOfFileHandles</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno dei motivi per cui questo errore può essere restituito è se <em>cpg</em> soddisfa le dimensioni minime del database. Le dimensioni minime correnti del database sono di 256 pagine.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Le risorse di memoria del sistema sono limitate.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Se **jetSetDatabaseSize viene** chiamato prima di inserire grandi quantità di dati, il file di database verrà aumentato in un'unica operazione. In questo modo si riduce la probabilità che il file di database diventi frammentato a livello di file system e si riduce anche il numero di volte in cui è necessario aumentare le dimensioni del file di database. L'aumento delle dimensioni del file di database una volta può essere più veloce rispetto all'aumento delle dimensioni più volte.

Attualmente è supportata solo l'aumento delle dimensioni del file. Per compattare un file, utilizzare la funzionalità di deframmentazione del programma esentutl.exe utilità .

Se *cpg* è inferiore alle dimensioni correnti del database, l'operazione verrà ignorata. Se *cpg* è inferiore alle dimensioni minime del database (attualmente 256 pagine), restituirà JET_errInvalidParameter.

Per impostare le dimensioni di un database aperto, vedere [JetGrowDatabase](./jetgrowdatabase-function.md).

Le dimensioni del file potrebbero non corrispondere al numero di pagine restituite in *pcpgReal.* Esistono due pagine riservate aggiuntive che potrebbero non essere conteggiate in *pcpgReal.*

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
<td><p>Implementato come <strong>JetSetDatabaseSizeW</strong> (Unicode) e <strong>JetSetDatabaseSizeA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetGrowDatabase](./jetgrowdatabase-function.md)
