---
description: Altre informazioni sulla classe EsentReadVerifyFailureException
title: Classe EsentReadVerifyFailureException
TOCTitle: EsentReadVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentreadverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102552
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad451f633f48ff11321bd35f27d867263d7f0080fdb5743cd1e491e846118363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971158"
---
# <a name="esentreadverifyfailureexception-class"></a>Classe EsentReadVerifyFailureException

Classe di base per JET_err. Eccezioni ReadVerifyFailure.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentReadVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentReadVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentReadVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentReadVerifyFailureException](./esentreadverifyfailureexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
