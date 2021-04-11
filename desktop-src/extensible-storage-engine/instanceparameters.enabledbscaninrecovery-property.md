---
description: 'Altre informazioni su: Proprietà InstanceParameters. EnableDbScanInRecovery'
title: Proprietà InstanceParameters. EnableDbScanInRecovery
TOCTitle: 'EnableDbScanInRecovery property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enabledbscaninrecovery(v=EXCHG.10)
ms:contentKeyID: 55107448
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDbScanInRecovery
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableDbScanInRecovery
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableDbScanInRecovery
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c6d492b2c101305b3038c300c77467d14dc480e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884206"
---
# <a name="instanceparametersenabledbscaninrecovery-property"></a>Proprietà InstanceParameters. EnableDbScanInRecovery

Ottiene o imposta un valore che indica se è necessario eseguire la manutenzione del database durante il ripristino.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property EnableDbScanInRecovery As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.EnableDbScanInRecovery

instance.EnableDbScanInRecovery = value
```

``` csharp
public int EnableDbScanInRecovery { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri di InstanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
