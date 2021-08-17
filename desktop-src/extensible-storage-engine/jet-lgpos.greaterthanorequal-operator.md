---
description: 'Altre informazioni su: JET_LGPOS. Operatore GreaterThanOrEqual'
title: JET_LGPOS. Operatore GreaterThanOrEqual
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510730
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef9f6835d4c65d08eeb6b3765bd5f2319048986daac439b7b2059b02ecf9735a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119109268"
---
# <a name="jet_lgposgreaterthanorequal-operator"></a>JET_LGPOS. Operatore GreaterThanOrEqual

Determinare se una posizione del log è dopo o uguale a un'altra posizione del log.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a>Parametri

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Prima posizione del log da confrontare.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    Seconda posizione del log da confrontare.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se lhs viene dopo o è uguale a rhs.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_LGPOS struttura](./jet-lgpos-structure2.md)

[JET_LGPOS membri](./jet-lgpos-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
