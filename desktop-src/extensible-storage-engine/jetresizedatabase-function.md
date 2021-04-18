---
description: 'Altre informazioni su: funzione JetResizeDatabase'
title: JetResizeDatabase (funzione)
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dadaa7eaa310c5b3a6a2730d316218bc2607d100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319175"
---
# <a name="jetresizedatabase-function"></a>JetResizeDatabase (funzione)


_**Si applica a:** Windows | Windows Server_

La funzione **JetResizeDatabase** estende o compatta le dimensioni di un database attualmente aperto.

La funzione **JetResizeDatabase** è stata introdotta nel sistema operativo Windows 8.

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*dbid*

Database che verrà esteso.

*cpg*

Dimensioni richieste del database, in pagine.

*pcpgActual*

Puntatore a un numero che riceve le dimensioni del database, in pagine, dopo la chiamata API. Se la chiamata API ha esito negativo, il contenuto del parametro *pcpgActual* non è definito.

*grbit*

Gruppo di bit che specifica zero o più valori elencati nella tabella seguente.

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
<td><p>JET_bitResizeDatabaseOnlyGrow</p></td>
<td><p>Espandere solo il database. Se la chiamata di ridimensionamento riduce il database, non eseguire alcuna operazione.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente. Per ulteriori informazioni sui possibili errori di Extensible Storage Engine (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

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
<td><p>JET_errDiskFull</p></td>
<td><p>Lo spazio disponibile nel volume non è sufficiente per eseguire l'operazione di espansione.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO</p></td>
<td><p>È stato restituito un errore relativo al file dalla funzione <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> . Per ulteriori informazioni sugli altri errori correlati ai file che potrebbero essere restituiti, vedere <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Commenti

Se la funzione **JetResizeDatabase** viene chiamata prima dell'inserimento di grandi quantità di dati, il file di database verrà aumentato in un'unica operazione. In questo modo si ridurrà la probabilità che il file di database diventi frammentato a livello di file system e si ridurrà anche il numero di volte in cui il file di database deve essere aumentato. La crescita del file di database può essere più veloce rispetto alla crescita più volte.

Per impostare le dimensioni di un database non aperto, vedere [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

Le dimensioni del file potrebbero non corrispondere al numero di pagine restituite nel parametro *pcpgReal* . Due pagine riservate aggiuntive potrebbero non essere conteggiate nel parametro *pcpgReal* .

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2012.</p></td>
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


#### <a name="see-also"></a>Vedi anche

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
