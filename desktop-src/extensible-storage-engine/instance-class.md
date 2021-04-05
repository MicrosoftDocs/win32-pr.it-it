---
description: 'Altre informazioni su: classe di istanze'
title: Classe dell'istanza
TOCTitle: Instance class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance(v=EXCHG.10)
ms:contentKeyID: 55103260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b717286a9d07b7eb17b87354cbe0896cf182f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753314"
---
# <a name="instance-class"></a>Classe dell'istanza

Classe che incapsula un [JET_INSTANCE](./jet-instance-structure.md) in un oggetto eliminabile. L'istanza deve essere chiusa per ultima e la chiusura dell'istanza rilascia tutte le altre risorse per l'istanza.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Runtime. ConstrainedExecution. CriticalFinalizerObject](/dotnet/api/system.runtime.constrainedexecution.criticalfinalizerobject)  
    [System.Runtime.InteropServices.SafeHandle](/dotnet/api/system.runtime.interopservices.safehandle)  
      [Microsoft. Win32. SafeHandles. SafeHandleZeroOrMinusOneIsInvalid](/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid)  
        Microsoft. ISAM. esent. Interop. Instance  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Class Instance _
    Inherits SafeHandleZeroOrMinusOneIsInvalid
'Usage
Dim instance As Instance
```

``` csharp
public class Instance : SafeHandleZeroOrMinusOneIsInvalid
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di istanza](./instance-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
