---
description: 'Altre informazioni su: classe EsentLSCallbackNotSpecifiedException'
title: Classe EsentLSCallbackNotSpecifiedException
TOCTitle: EsentLSCallbackNotSpecifiedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLSCallbackNotSpecifiedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlscallbacknotspecifiedexception(v=EXCHG.10)
ms:contentKeyID: 55102179
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLSCallbackNotSpecifiedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLSCallbackNotSpecifiedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6096410a8e0ca15539bac4a52412d2f61611ddbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131419"
---
# <a name="esentlscallbacknotspecifiedexception-class"></a>Classe EsentLSCallbackNotSpecifiedException

Classe di base per JET_err. Eccezioni LSCallbackNotSpecified.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentLSCallbackNotSpecifiedException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLSCallbackNotSpecifiedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentLSCallbackNotSpecifiedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLSCallbackNotSpecifiedException : EsentUsageException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentLSCallbackNotSpecifiedException](./esentlscallbacknotspecifiedexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
