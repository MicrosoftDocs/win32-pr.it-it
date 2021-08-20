---
description: Altre informazioni sulla proprietà InstanceParameters.LogFileSize
title: InstanceParameters.LogFileSize - proprietà
TOCTitle: 'LogFileSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logfilesize(v=EXCHG.10)
ms:contentKeyID: 55103312
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogFileSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d605a62541ee8e338aedcbd4109a16661baa64ced420c4cb56b10f472e0d085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117705902"
---
# <a name="instanceparameterslogfilesize-property"></a>InstanceParameters.LogFileSize - proprietà

Ottiene o imposta le dimensioni dei file di log delle transazioni. Questo parametro deve essere impostato in unità di 1024 byte (ad esempio, un'impostazione di 2048 offrirà 2 MB di file di log).

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property LogFileSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogFileSize

instance.LogFileSize = value
```

``` csharp
public int LogFileSize { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri instanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
