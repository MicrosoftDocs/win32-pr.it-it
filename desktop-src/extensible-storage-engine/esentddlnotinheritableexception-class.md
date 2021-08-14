---
description: Altre informazioni sulla classe EsentDDLNotInheritableException
title: Classe EsentDDLNotInheritableException
TOCTitle: EsentDDLNotInheritableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentddlnotinheritableexception(v=EXCHG.10)
ms:contentKeyID: 55101474
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 858c5c3898b77907ed053849a489b43de7ad948560afae1fe85e9849929b6369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117711722"
---
# <a name="esentddlnotinheritableexception-class"></a>Classe EsentDDLNotInheritableException

Classe di base per JET_err. Eccezioni DDLNotInheritable.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException  

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDDLNotInheritableException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDDLNotInheritableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDDLNotInheritableException : EsentUsageException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentDDLNotInheritableException](./esentddlnotinheritableexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
