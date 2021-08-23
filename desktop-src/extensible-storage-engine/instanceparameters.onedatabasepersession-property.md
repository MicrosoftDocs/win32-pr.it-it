---
description: 'Altre informazioni su: Proprietà InstanceParameters.OneDatabasePerSession'
title: InstanceParameters.OneDatabasePerSession - proprietà
TOCTitle: 'OneDatabasePerSession property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.onedatabasepersession(v=EXCHG.10)
ms:contentKeyID: 55103319
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_OneDatabasePerSession
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_OneDatabasePerSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3707f6e1cf960888f5f403f433ede3d3b82828e300ef59190bf5734e0e4c13b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618041"
---
# <a name="instanceparametersonedatabasepersession-property"></a>InstanceParameters.OneDatabasePerSession - proprietà

Ottiene o imposta un valore che indica se un solo database può essere aperto con JetOpenDatabase da una determinata sessione alla volta. Il database temporaneo è escluso da questa restrizione.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property OneDatabasePerSession As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.OneDatabasePerSession

instance.OneDatabasePerSession = value
```

``` csharp
public bool OneDatabasePerSession { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri instanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
