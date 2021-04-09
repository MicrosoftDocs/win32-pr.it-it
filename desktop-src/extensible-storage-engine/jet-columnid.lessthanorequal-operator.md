---
description: 'Altre informazioni su: JET_COLUMNID. Operatore LessThanOrEqual'
title: JET_COLUMNID. Operatore LessThanOrEqual
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 39513688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9d6f98c5861a57fa4916ebca1b421c538d752d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753263"
---
# <a name="jet_columnidlessthanorequal-operator"></a>JET_COLUMNID. Operatore LessThanOrEqual

Determinare se un columnid è precedente o uguale a un altro ColumnID.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a>Parametri

  - LHS  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Primo ColumnID da confrontare.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Secondo ColumnID da confrontare.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se LHS precede o è uguale a RHS.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Struttura JET_COLUMNID](./jet-columnid-structure.md)

[Membri JET_COLUMNID](./jet-columnid-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
