---
description: 'Altre informazioni su: Enumerazione JET_DbInfo'
title: Enumerazione JET_DbInfo
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39c6c3175c08e4f7644ad4f0b41137e12e84f71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306857"
---
# <a name="jet_dbinfo-enumeration"></a>Enumerazione JET_DbInfo

Livelli di informazioni per il recupero delle informazioni sul database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome del membro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Nome file</td>
<td>Restituisce il percorso del file di database (String).</td>
</tr>
<tr class="even">
<td></td>
<td>LCID</td>
<td>Restituisce l'identificatore delle impostazioni locali (LCID) associato a questo database (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Opzioni</td>
<td>Restituisce un <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>. Indica se il database è aperto in modalità esclusiva. Se il database è in modalità esclusiva, viene restituito <a href="hh579532(v=exchg.10).md">Exclusive</a> ; in caso contrario, viene restituito zero. Non vengono restituite altre opzioni di grbit del database per JetAttachDatabase e JetOpenDatabase.</td>
</tr>
<tr class="even">
<td></td>
<td>Transazioni</td>
<td>Restituisce un numero maggiore del livello massimo a cui è possibile annidare le transazioni. Se viene chiamato <a href="dn292105(v=exchg.10).md">JetBeginTransaction (JET_SESID)</a> (in un modo annidato, ovvero nella stessa sessione senza commit o rollback) il numero di volte in cui questo valore viene restituito, nell'ultima chiamata a <a href="hh564840(v=exchg.10).md">TransTooDeep</a> verrà restituito (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Versione</td>
<td>Restituisce la versione principale del motore di database (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>Filesize</td>
<td>Restituisce il Filesize del database, in pagine (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceOwned</td>
<td>Restituisce lo spazio di proprietà del database, in pagine (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAvailable</td>
<td>Restituisce lo spazio disponibile nel database, in pagine (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Varie</td>
<td>Restituisce un oggetto <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> .</td>
</tr>
<tr class="even">
<td></td>
<td>DBInUse</td>
<td>Restituisce un valore booleano che indica se il database è collegato (booleano).</td>
</tr>
<tr class="odd">
<td></td>
<td>PageSize</td>
<td>Restituisce le dimensioni di pagina del database (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>FileType</td>
<td>Restituisce il tipo di database (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
