---
description: Altre informazioni sulla classe EsentCannotIndexException
title: Classe EsentCannotIndexException
TOCTitle: EsentCannotIndexException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotIndexException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotindexexception(v=EXCHG.10)
ms:contentKeyID: 55101161
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotIndexException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotIndexException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23a40bc92f627d7601f1ca48bc9765d3015c915e3fec2659a7d9a806bfddb7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119116971"
---
# <a name="esentcannotindexexception-class"></a>Classe EsentCannotIndexException

Classe di base per JET_err. Eccezioni CannotIndex.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentCannotIndexException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotIndexException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotIndexException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotIndexException : EsentUsageException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentCannotIndexException](./esentcannotindexexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
