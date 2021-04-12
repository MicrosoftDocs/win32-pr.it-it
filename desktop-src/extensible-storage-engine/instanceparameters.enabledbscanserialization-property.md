---
description: 'Altre informazioni su: Proprietà InstanceParameters. EnableDBScanSerialization'
title: Proprietà InstanceParameters. EnableDBScanSerialization
TOCTitle: 'EnableDBScanSerialization property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enabledbscanserialization(v=EXCHG.10)
ms:contentKeyID: 55103555
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableDBScanSerialization
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableDBScanSerialization
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c514218b43d1f291abc01d384cdb47f339163cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344431"
---
# <a name="instanceparametersenabledbscanserialization-property"></a>Proprietà InstanceParameters. EnableDBScanSerialization

Ottiene o imposta un valore che indica se la serializzazione della manutenzione del database è abilitata per i database che condividono lo stesso disco.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property EnableDBScanSerialization As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.EnableDBScanSerialization

instance.EnableDBScanSerialization = value
```

``` csharp
public bool EnableDBScanSerialization { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri di InstanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
