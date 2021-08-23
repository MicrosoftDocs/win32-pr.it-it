---
description: Altre informazioni sulla classe EsentColumnNotUpdatableException
title: Classe EsentColumnNotUpdatableException
TOCTitle: EsentColumnNotUpdatableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnNotUpdatableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumnnotupdatableexception(v=EXCHG.10)
ms:contentKeyID: 55101338
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnNotUpdatableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnNotUpdatableException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00851b9e9e8f8c25b358b14783f1ddf7eaf05ee56eef85adfa7be74bc868fd22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119116614"
---
# <a name="esentcolumnnotupdatableexception-class"></a>Classe EsentColumnNotUpdatableException

Classe di base per JET_err. Eccezioni ColumnNotUpdatable.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentColumnNotUpdatableException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnNotUpdatableException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnNotUpdatableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnNotUpdatableException : EsentUsageException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentColumnNotUpdatableException](./esentcolumnnotupdatableexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
