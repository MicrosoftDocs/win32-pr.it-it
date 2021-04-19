---
description: "Altre informazioni su: conversione implicita dell'istanza (istanza JET_INSTANCE)"
title: Conversione implicita dell'istanza (istanza JET_INSTANCE)
TOCTitle: Implicit conversion (Instance to JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.op_Implicit(Microsoft.Isam.Esent.Interop.Instance)~Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55103290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Implicit
- Microsoft.Isam.Esent.Interop.Instance.op_Implicit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c7dbac9f0b5736970cf51aef9e99f2877cfd488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309151"
---
# <a name="instance-implicit-conversion-instance-to-jet_instance"></a>Conversione implicita dell'istanza (istanza JET_INSTANCE)

Fornire la conversione implicita di un oggetto istanza a una struttura JET_INSTANCE. Questa operazione viene eseguita in modo che un'istanza possa essere utilizzata ovunque sia necessario un JET_INSTANCE.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    instance As Instance _
) As JET_INSTANCE
'Usage
Dim input As Instance
Dim output As JET_INSTANCE

output = CType(input, JET_INSTANCE)
```

``` csharp
public static implicit operator JET_INSTANCE (
    Instance instance
)
```

#### <a name="parameters"></a>Parametri

  - instance  
    Tipo: [Microsoft. ISAM. esent. Interop. Instance](./instance-class.md)  
    
    Istanza di da convertire.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
JET_INSTANCE di cui è stato eseguito il wrapper dall'istanza di.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe dell'istanza](./instance-class.md)

[Membri di istanza](./instance-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
