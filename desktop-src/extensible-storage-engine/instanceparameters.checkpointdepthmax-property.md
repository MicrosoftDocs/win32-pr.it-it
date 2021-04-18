---
description: 'Altre informazioni su: Proprietà InstanceParameters. CheckpointDepthMax'
title: Proprietà InstanceParameters. CheckpointDepthMax
TOCTitle: 'CheckpointDepthMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.checkpointdepthmax(v=EXCHG.10)
ms:contentKeyID: 55103294
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3addab0356206577eda22119ddce81721e9c2bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309150"
---
# <a name="instanceparameterscheckpointdepthmax-property"></a>Proprietà InstanceParameters. CheckpointDepthMax

Ottiene o imposta la soglia in byte per informazioni sul numero di file di log delle transazioni che dovranno essere riprodotti dopo un arresto anomalo del sistema. Se la registrazione circolare è abilitata usando CircularLog, questo parametro controllerà anche la quantità approssimativa di file di log delle transazioni che verranno conservati su disco.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property CheckpointDepthMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CheckpointDepthMax

instance.CheckpointDepthMax = value
```

``` csharp
public int CheckpointDepthMax { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri di InstanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
