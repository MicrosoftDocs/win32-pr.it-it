---
description: 'Altre informazioni su: JET_COMMIT_ID. LessThanOrEqual operator'
title: Operatore JET_COMMIT_ID. LessThanOrEqual (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 55104413
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_LessThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 872ded299fc36295ea56500605f23af37feb0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757943"
---
# <a name="jet_commit_idlessthanorequal-operator"></a>Operatore JET_COMMIT_ID. LessThanOrEqual

Determinare se un commitid è precedente a un altro commitid.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a>Parametri

  - LHS  
    Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Primo oggetto commitid da confrontare.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Secondo oggetto commitid da confrontare.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se LHS precede o è uguale a RHS.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_COMMIT_ID](./jet-commit-id-class.md)

[Membri JET_COMMIT_ID](./jet-commit-id-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
