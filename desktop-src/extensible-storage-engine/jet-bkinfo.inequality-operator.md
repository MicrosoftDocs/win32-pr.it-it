---
description: 'Altre informazioni su: JET_BKINFO. Operatore di disuguaglianza'
title: JET_BKINFO. Operatore di disuguaglianza
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Inequality(Microsoft.Isam.Esent.Interop.JET_BKINFO,Microsoft.Isam.Esent.Interop.JET_BKINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39513804
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e4279fb6dce692bdd6e5c7b73ae260521a8c1eaebebb8ea5a90671699f7eb0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118255595"
---
# <a name="jet_bkinfoinequality-operator"></a>JET_BKINFO. Operatore di disuguaglianza

Determina se due istanze specificate di JET_BKINFO non sono uguali.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_BKINFO, _
    rhs As JET_BKINFO _
) As Boolean
'Usage
Dim lhs As JET_BKINFO
Dim rhs As JET_BKINFO
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_BKINFO lhs,
    JET_BKINFO rhs
)
```

#### <a name="parameters"></a>Parametri

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)  
    
    Prima istanza da confrontare.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)  
    
    Seconda istanza da confrontare.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se le due istanze non sono uguali.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_BKINFO struttura](./jet-bkinfo-structure2.md)

[JET_BKINFO membri](./jet-bkinfo-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
