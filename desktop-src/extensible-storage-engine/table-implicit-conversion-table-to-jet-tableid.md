---
description: 'Altre informazioni su: conversione implicita di tabella (tabella per JET_TABLEID)'
title: Conversione implicita di tabella (da tabella a JET_TABLEID)
TOCTitle: Implicit conversion (Table to JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.op_Implicit(Microsoft.Isam.Esent.Interop.Table)~Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104156
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table.Implicit
- Microsoft.Isam.Esent.Interop.Table.op_Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f5085ee09020730b36269255279836b31562a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315067"
---
# <a name="table-implicit-conversion-table-to-jet_tableid"></a>Conversione implicita di tabella (da tabella a JET_TABLEID)

Operatore di conversione implicito da una tabella a una JET_TABLEID. Ciò consente di usare una tabella con le API che prevedono un JET_TABLEID.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    table As Table _
) As JET_TABLEID
'Usage
Dim input As Table
Dim output As JET_TABLEID

output = CType(input, JET_TABLEID)
```

``` csharp
public static implicit operator JET_TABLEID (
    Table table
)
```

#### <a name="parameters"></a>Parametri

  - table  
    Tipo: [Microsoft. ISAM. esent. Interop. Table](./table-class.md)  
    
    Tabella da convertire.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
JET_TABLEID della tabella.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Table](./table-class.md)

[Membri della tabella](./table-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
