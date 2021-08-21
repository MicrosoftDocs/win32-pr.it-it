---
description: 'Altre informazioni su: JET_HANDLE. Operatore di disuguaglianza'
title: JET_HANDLE. Operatore di disuguaglianza
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_HANDLE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c592845b40d6df7e160ff5907143fc652376a7fb47a20182acd782ff43cb101a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039249"
---
# <a name="jet_handleinequality-operator"></a>JET_HANDLE. Operatore di disuguaglianza

Determina se due istanze specificate di JET_HANDLE non sono uguali.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_HANDLE, _
    rhs As JET_HANDLE _
) As Boolean
'Usage
Dim lhs As JET_HANDLE
Dim rhs As JET_HANDLE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_HANDLE lhs,
    JET_HANDLE rhs
)
```

#### <a name="parameters"></a>Parametri

  - Lhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Prima istanza da confrontare.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Seconda istanza da confrontare.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se le due istanze non sono uguali.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_HANDLE struttura](./jet-handle-structure.md)

[JET_HANDLE membri](./jet-handle-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
