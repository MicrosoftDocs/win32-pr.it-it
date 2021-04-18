---
description: 'Altre informazioni su: Proprietà InstanceParameters. PageTempDBMin'
title: Proprietà InstanceParameters. PageTempDBMin
TOCTitle: 'PageTempDBMin property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.pagetempdbmin(v=EXCHG.10)
ms:contentKeyID: 55103558
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06825762485ad52743d585ce0fed86bd1739cd21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313558"
---
# <a name="instanceparameterspagetempdbmin-property"></a>Proprietà InstanceParameters. PageTempDBMin

Ottiene o imposta le dimensioni iniziali del database temporaneo. Le dimensioni sono le pagine del database. Una dimensione pari a zero indica che devono essere utilizzate le dimensioni predefinite di un database normale. È spesso consigliabile che le piccole applicazioni configurino il database temporaneo in modo che sia il più piccolo possibile. L'impostazione di questo parametro su [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) consente di ottenere il database temporaneo più piccolo possibile.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property PageTempDBMin As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PageTempDBMin

instance.PageTempDBMin = value
```

``` csharp
public int PageTempDBMin { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri di InstanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
