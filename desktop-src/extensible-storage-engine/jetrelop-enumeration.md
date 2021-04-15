---
description: 'Altre informazioni su: Enumerazione JetRelop'
title: Enumerazione JetRelop (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JetRelop enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JetRelop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jetrelop(v=EXCHG.10)
ms:contentKeyID: 55104456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7839e0223eb9dd773ca9a5d10b5210b10b0a944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350416"
---
# <a name="jetrelop-enumeration"></a>Enumerazione JetRelop

Operazione di confronto per il filtro definito come [JET_INDEX_COLUMN](./jet-index-column-class.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Enumeration JetRelop
'Usage
Dim instance As JetRelop
```

``` csharp
public enum JetRelop
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
<td>Uguale a</td>
<td>Accetta solo le righe il cui valore di colonna è uguale al valore specificato.</td>
</tr>
<tr class="even">
<td></td>
<td>PrefixEquals</td>
<td>Accetta solo righe con colonne il cui prefisso corrisponde al valore specificato.</td>
</tr>
<tr class="odd">
<td></td>
<td>NotEquals</td>
<td>Accettare solo le righe il cui valore di colonna non è uguale al valore specificato.</td>
</tr>
<tr class="even">
<td></td>
<td>LessThanOrEqual</td>
<td>Accetta solo le righe il cui valore di colonna è minore o uguale a un valore specificato.</td>
</tr>
<tr class="odd">
<td></td>
<td>LessThan</td>
<td>Accetta solo righe il cui valore di colonna è minore di un valore specificato.</td>
</tr>
<tr class="even">
<td></td>
<td>GreaterThanOrEqual</td>
<td>Accetta solo righe il cui valore di colonna è maggiore o uguale a un valore specificato.</td>
</tr>
<tr class="odd">
<td></td>
<td>GreaterThan</td>
<td>Accetta solo righe il cui valore di colonna è maggiore di un valore specificato.</td>
</tr>
<tr class="even">
<td></td>
<td>BitmaskEqualsZero</td>
<td>Accetta solo le righe con valore di colonna individuato con una maschera di maschera specificata che restituisce zero.</td>
</tr>
<tr class="odd">
<td></td>
<td>BitmaskNotEqualsZero</td>
<td>Accetta solo le righe con valore di colonna individuato con una maschera di bit specificata che restituisce un valore diverso da zero.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
