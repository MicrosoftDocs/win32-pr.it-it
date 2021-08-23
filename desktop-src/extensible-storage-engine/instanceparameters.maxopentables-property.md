---
description: Altre informazioni sulla proprietà InstanceParameters.MaxOpenTables
title: InstanceParameters.MaxOpenTables - proprietà
TOCTitle: 'MaxOpenTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxopentables(v=EXCHG.10)
ms:contentKeyID: 55107442
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxOpenTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxOpenTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30129e66a05116bfaab28fe737584c89b8b74fb0c8722b3d772c643f5165cffe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039389"
---
# <a name="instanceparametersmaxopentables-property"></a>InstanceParameters.MaxOpenTables - proprietà

Ottiene o imposta il numero di risorse albero B+ riservate per questa istanza.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property MaxOpenTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxOpenTables

instance.MaxOpenTables = value
```

``` csharp
public int MaxOpenTables { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri instanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
