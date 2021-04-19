---
description: 'Altre informazioni su: classe EsentRunningInOneInstanceModeException'
title: Classe EsentRunningInOneInstanceModeException
TOCTitle: EsentRunningInOneInstanceModeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrunninginoneinstancemodeexception(v=EXCHG.10)
ms:contentKeyID: 55102675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b764bd604076ee4dae1d3ee21d52c1d3b923407e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317446"
---
# <a name="esentrunninginoneinstancemodeexception-class"></a>Classe EsentRunningInOneInstanceModeException

Classe di base per JET_err. Eccezioni RunningInOneInstanceMode.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentRunningInOneInstanceModeException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRunningInOneInstanceModeException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRunningInOneInstanceModeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRunningInOneInstanceModeException : EsentUsageException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentRunningInOneInstanceModeException](./esentrunninginoneinstancemodeexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
