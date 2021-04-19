---
description: 'Altre informazioni su: Enumerazione JET_IdxInfo'
title: Enumerazione JET_IdxInfo
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1f2cb50537ed492a428c82fd9a6f6541c5fad2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318135"
---
# <a name="jet_idxinfo-enumeration"></a>Enumerazione JET_IdxInfo

Livelli di informazioni per il recupero delle informazioni sugli indici con JetGetIndexInfo. e JetGetTableIndexInfo.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
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
<td>Restituisce una struttura di <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> con informazioni sull'indice.</td>
</tr>
<tr class="even">
<td></td>
<td>Elenco</td>
<td>Restituisce una struttura di <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> con informazioni sull'indice.</td>
</tr>
<tr class="odd">
<td></td>
<td>SysTabCursor</td>
<td><strong>Obsoleto.</strong> SysTabCursor è obsoleto.</td>
</tr>
<tr class="even">
<td></td>
<td>OLC</td>
<td><strong>Obsoleto.</strong> OLC è obsoleto.</td>
</tr>
<tr class="odd">
<td></td>
<td>ResetOLC</td>
<td><strong>Obsoleto.</strong> Reset OLC è obsoleto.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAlloc</td>
<td>Restituisce un integer con l'utilizzo dello spazio dell'indice.</td>
</tr>
<tr class="odd">
<td></td>
<td>LCID</td>
<td>Restituisce un integer con l'LCID dell'indice.</td>
</tr>
<tr class="even">
<td></td>
<td>LangID</td>
<td><strong>Obsoleto.</strong> LangID è obsoleto. In alternativa, utilizzare LCID.</td>
</tr>
<tr class="odd">
<td></td>
<td>Conteggio</td>
<td>Restituisce un integer con il conteggio degli indici nella tabella.</td>
</tr>
<tr class="even">
<td></td>
<td>VarSegMac</td>
<td>Restituisce un ushort con il valore di cbVarSegMac con cui è stato creato l'indice.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexId</td>
<td>Restituisce un <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> che identifica l'indice.</td>
</tr>
<tr class="even">
<td></td>
<td>Per la maggior parte</td>
<td>Introdotta in Windows Vista. Restituisce un ushort con il valore di cbKeyMost con cui è stato creato l'indice.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
