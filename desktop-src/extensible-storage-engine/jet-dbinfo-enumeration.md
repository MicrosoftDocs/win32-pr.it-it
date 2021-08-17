---
description: 'Altre informazioni su: enumerazione JET_DbInfo dati'
title: JET_DbInfo enumerazione
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
ms.openlocfilehash: c364b89ccb50542130c988a643fed594a34e370e5adb5e9d0a13f77eab5b04d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112230"
---
# <a name="jet_dbinfo-enumeration"></a>JET_DbInfo enumerazione

Livelli di informazioni per il recupero di informazioni sul database.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Restituisce il percorso del file di database (stringa).</td>
</tr>
<tr class="even">
<td></td>
<td>LCID</td>
<td>Restituisce l'identificatore delle impostazioni locali (LCID) associato al database (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Opzioni</td>
<td>Restituisce un <a href="hh579532(v=exchg.10).md">oggetto OpenDatabaseGrbit.</a> Indica se il database viene aperto in modalità esclusiva. Se il database è in modalità esclusiva, <a href="hh579532(v=exchg.10).md">verrà restituito Exclusive,</a> in caso contrario viene restituito zero. Non vengono restituite altre opzioni grbit del database per JetAttachDatabase e JetOpenDatabase.</td>
</tr>
<tr class="even">
<td></td>
<td>Transazioni</td>
<td>Restituisce un numero uno maggiore del livello massimo a cui è possibile annidare le transazioni. Se <a href="dn292105(v=exchg.10).md">jetBeginTransaction(JET_SESID)</a> viene chiamato (in modo annidamento, ovvero nella stessa sessione, senza commit o rollback) quante volte questo valore, nell'ultima chiamata <a href="hh564840(v=exchg.10).md">verrà restituito TransTooDeep</a> (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Versione</td>
<td>Restituisce la versione principale del motore di database (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>Dimensione</td>
<td>Restituisce la dimensione del file del database, in pagine (Int32).</td>
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
<td>Restituisce un <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> oggetto .</td>
</tr>
<tr class="even">
<td></td>
<td>DBInUse</td>
<td>Restituisce un valore booleano che indica se il database è collegato (booleano).</td>
</tr>
<tr class="odd">
<td></td>
<td>PageSize</td>
<td>Restituisce le dimensioni della pagina del database (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>FileType</td>
<td>Restituisce il tipo del database (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
