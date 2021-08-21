---
description: Altre informazioni sulla proprietà ColumnValue.ValueAsObject
title: Proprietà ColumnValue.ValueAsObject
TOCTitle: 'ValueAsObject property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.ValueAsObject
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.valueasobject(v=EXCHG.10)
ms:contentKeyID: 55101198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.ValueAsObject
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.get_ValueAsObject
- Microsoft.Isam.Esent.Interop.ColumnValue.ValueAsObject
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c7b5117f75fb195fe065493d942cee6c244f56eed1fe6170bdd53fd243143d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083654"
---
# <a name="columnvaluevalueasobject-property"></a>Proprietà ColumnValue.ValueAsObject

Ottiene l'ultimo valore impostato o recuperato della colonna. Il valore viene restituito come oggetto generico.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public MustOverride ReadOnly Property ValueAsObject As Object
    Get
'Usage
Dim instance As ColumnValue
Dim value As Object

value = instance.ValueAsObject
```

``` csharp
public abstract Object ValueAsObject { get; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.Object](/dotnet/api/system.object)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe ColumnValue](./columnvalue-class.md)

[Membri ColumnValue](./columnvalue-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
