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
ms.openlocfilehash: 0b2ffe6ff2a4b6af3234c9f5d85d577bae91a748ebb9224fef5a9d0d96864502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039319"
---
# <a name="jet_columnidlessthanorequal-operator"></a>JET_COLUMNID. Operatore LessThanOrEqual

Determinare se un columnid è precedente o uguale a un altro columnid.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Primo columnid da confrontare.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Secondo columnid da confrontare.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se lhs viene prima o è uguale a rhs.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_COLUMNID struttura](./jet-columnid-structure.md)

[JET_COLUMNID membri](./jet-columnid-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
