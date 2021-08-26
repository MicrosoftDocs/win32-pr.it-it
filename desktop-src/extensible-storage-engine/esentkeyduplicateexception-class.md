---
description: Altre informazioni sulla classe EsentKeyDuplicateException
title: Classe EsentKeyDuplicateException
TOCTitle: EsentKeyDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeyduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102039
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5a93ad69d045cda0658ff8298d635b2efc5016e2850023ad9c4be16450b92a83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971929"
---
# <a name="esentkeyduplicateexception-class"></a>Classe EsentKeyDuplicateException

Classe di base per JET_err. Eccezioni KeyDuplicate.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentKeyDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyDuplicateException : EsentStateException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentKeyDuplicateException](./esentkeyduplicateexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
