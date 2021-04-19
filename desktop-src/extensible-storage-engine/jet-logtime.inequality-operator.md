---
description: 'Altre informazioni su: JET_LOGTIME. Operatore di disuguaglianza'
title: JET_LOGTIME. Operatore di disuguaglianza
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Inequality(Microsoft.Isam.Esent.Interop.JET_LOGTIME,Microsoft.Isam.Esent.Interop.JET_LOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511232
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Inequality
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ba95b6306984fcee5749e4b97d969713541851f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319657"
---
# <a name="jet_logtimeinequality-operator"></a>JET_LOGTIME. Operatore di disuguaglianza

Determina se due istanze specificate di JET_LOGTIME non sono uguali.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_LOGTIME, _
    rhs As JET_LOGTIME _
) As Boolean
'Usage
Dim lhs As JET_LOGTIME
Dim rhs As JET_LOGTIME
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_LOGTIME lhs,
    JET_LOGTIME rhs
)
```

#### <a name="parameters"></a>Parametri

  - LHS  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  
    
    Prima istanza da confrontare.

<!-- end list -->

  - rhs  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  
    
    Seconda istanza da confrontare.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se le due istanze non sono uguali.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Struttura JET_LOGTIME](./jet-logtime-structure2.md)

[Membri JET_LOGTIME](./jet-logtime-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
