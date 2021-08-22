---
description: Altre informazioni sull'enumerazione JET_TblInfo'
title: JET_TblInfo enumerazione
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
ms.openlocfilehash: 0b2af9bfd69f81b518eba42f435a457c9baaa0d0ce8ddbac1424b997329a3ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832681"
---
# <a name="jet_tblinfo-enumeration"></a>JET_TblInfo enumerazione

Livelli di informazioni per il recupero di informazioni sulle tabelle con JetGetTableInfo.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Opzione predefinita. Recupera un <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> contenente informazioni sulla tabella. Usare questa opzione con <a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>Nome</td>
<td>Recupera il nome della tabella. Usare questa opzione con <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>Dbid</td>
<td>Recupera il <a href="hh596176(v=exchg.10).md">JET_DBID</a> del database contenente la tabella. Usare questa opzione con <a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceUsage</td>
<td>Il comportamento del metodo dipende dalle dimensioni della matrice passata al metodo . La matrice deve avere almeno due voci. La prima voce conterrà il numero di extent di proprietà nella tabella. La seconda voce conterrà il numero di extent disponibili nella tabella. Se la matrice contiene più di due voci, i byte rimanenti del buffer saranno costituiti da una matrice di strutture che rappresentano un elenco di extent. Questa struttura contiene due membri: l'ultimo numero di pagina nell'extent e il numero di pagine nell'extent. Usare questa opzione con <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAlloc</td>
<td>La matrice passata a JetGetTableInfo deve avere due voci. La prima voce verrà impostata sul numero di pagine nella tabella. La seconda voce verrà impostata sulla densità di destinazione delle pagine per la tabella. Usare questa opzione con <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceOwned</td>
<td>Ottiene il numero di pagine di proprietà nella tabella. Usare questa opzione con <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAvailable</td>
<td>Ottiene il numero di pagine disponibili nella tabella. Usare questa opzione con <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>TemplateTableName</td>
<td>Se la tabella è una tabella derivata, il risultato verrà compilato con il nome della tabella da cui la tabella derivata ha ereditato il DDL. Se la tabella non è una tabella derivata, il buffer sarà una stringa vuota. Usare questa opzione con <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
