---
description: 'Altre informazioni su: JET_INSTANCE. Metodo Equals (Object)'
title: JET_INSTANCE. Metodo Equals (Object)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39515717
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 490e5763aa1754387db67fcd52b6b2a5383affa5d061905b26bafb52acd35716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765665"
---
# <a name="jet_instanceequals-method-object"></a>JET_INSTANCE. Metodo Equals (Object)

Restituisce un valore che indica se questa istanza è uguale a un'altra istanza di .

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a>Parametri

  - obj  
    Tipo: [System.Object](/dotnet/api/system.object)  
    
    Oggetto da confrontare con l'istanza.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se le due istanze sono uguali.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_INSTANCE struttura](./jet-instance-structure.md)

[JET_INSTANCE membri](./jet-instance-members.md)

[Confronta l'overload](./jet-instance.equals-method.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
