---
description: 'Altre informazioni su: Proprietà InstanceParameters. WaypointLatency'
title: Proprietà InstanceParameters. WaypointLatency
TOCTitle: 'WaypointLatency property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.waypointlatency(v=EXCHG.10)
ms:contentKeyID: 55103325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_WaypointLatency
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d7d837d7fff804926529ec67780e319d85031f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319212"
---
# <a name="instanceparameterswaypointlatency-property"></a>Proprietà InstanceParameters. WaypointLatency

Ottiene o imposta il numero di registri per i quali ESENT rinvia gli scaricamenti del database. Questa operazione può essere utilizzata per aumentare la recuperabilità del database se gli errori determinano la perdita di file di registro. Supportato su Windows 7 e su. Ignorato in Windows XP, Windows Server 2003, Windows Vista e Windows Server 2008.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property WaypointLatency As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.WaypointLatency

instance.WaypointLatency = value
```

``` csharp
public int WaypointLatency { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri di InstanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
