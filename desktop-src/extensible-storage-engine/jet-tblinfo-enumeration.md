---
description: 'Altre informazioni su: Enumerazione JET_TblInfo'
title: Enumerazione JET_TblInfo
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313107"
---
# <a name="jet_tblinfo-enumeration"></a>Enumerazione JET_TblInfo

Livelli di informazioni per il recupero delle informazioni sulla tabella con JetGetTableInfo.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
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
<td>Predefinito</td>
<td>Opzione predefinita. Recupera un <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> contenente le informazioni sulla tabella. Usare questa opzione con <a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>Nome</td>
<td>Recupera il nome della tabella. Usare questa opzione con <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>Dbid</td>
<td>Recupera la <a href="hh596176(v=exchg.10).md">JET_DBID</a> del database che contiene la tabella. Usare questa opzione con <a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceUsage</td>
<td>Il comportamento del metodo dipende dalla dimensione della matrice passata al metodo. La matrice deve contenere almeno due voci. La prima voce conterrà il numero di extent di proprietà nella tabella. La seconda voce conterrà il numero di extent disponibili nella tabella. Se la matrice contiene più di due voci, i byte rimanenti del buffer sono costituiti da una matrice di strutture che rappresentano un elenco di extent. Questa struttura contiene due membri: l'ultimo numero di pagina nell'extent e il numero di pagine nell'extent. Usare questa opzione con <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [] JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAlloc</td>
<td>La matrice passata a JetGetTableInfo deve avere due voci. La prima voce verrà impostata sul numero di pagine della tabella. La seconda voce verrà impostata sulla densità di destinazione delle pagine per la tabella. Usare questa opzione con <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [] JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceOwned</td>
<td>Ottiene il numero di pagine di proprietà nella tabella. Usare questa opzione con <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAvailable</td>
<td>Ottiene il numero di pagine disponibili nella tabella. Usare questa opzione con <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>TemplateTableName</td>
<td>Se la tabella è una tabella derivata, il risultato verrà compilato con il nome della tabella da cui la tabella derivata eredita la DDL. Se la tabella non è una tabella derivata, il buffer sarà una stringa vuota. Usare questa opzione con <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
