---
description: Altre informazioni sulla proprietà InstanceParameters.CreatePathIfNotExist
title: Proprietà InstanceParameters.CreatePathIfNotExist
TOCTitle: 'CreatePathIfNotExist property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.createpathifnotexist(v=EXCHG.10)
ms:contentKeyID: 55103321
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CreatePathIfNotExist
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CreatePathIfNotExist
- Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cf48149548a21cc225816d307f65ac7c24bdaba4bfd090def9951e773f251c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112420"
---
# <a name="instanceparameterscreatepathifnotexist-property"></a>Proprietà InstanceParameters.CreatePathIfNotExist

Ottiene o imposta un valore che indica se ESENT creerà automaticamente le cartelle mancanti nei percorsi del file system.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property CreatePathIfNotExist As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CreatePathIfNotExist

instance.CreatePathIfNotExist = value
```

``` csharp
public bool CreatePathIfNotExist { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri di InstanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
