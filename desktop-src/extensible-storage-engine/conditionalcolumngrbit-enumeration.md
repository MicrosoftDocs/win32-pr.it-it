---
description: Altre informazioni sull'enumerazione ConditionalColumnGrbit
title: Enumerazione ConditionalColumnGrbit
TOCTitle: ConditionalColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conditionalcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39513009
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b838728ca956b104b850cac4cf1741398c3015b03df7ed427f71c1f109b0c038
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737941"
---
# <a name="conditionalcolumngrbit-enumeration"></a>Enumerazione ConditionalColumnGrbit

Opzioni per la JET_CONDITIONALCOLUMN struttura.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ConditionalColumnGrbit
'Usage
Dim instance As ConditionalColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum ConditionalColumnGrbit
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
<td>ColumnMustBeNull</td>
<td>La colonna deve essere Null perché una voce di indice venga visualizzata nell'indice.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnMustBeNonNull</td>
<td>La colonna deve essere non Null perché una voce di indice venga visualizzata nell'indice.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
