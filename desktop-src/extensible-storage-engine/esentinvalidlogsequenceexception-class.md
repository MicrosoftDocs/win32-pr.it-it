---
description: Altre informazioni sulla classe EsentInvalidLogSequenceException
title: Classe EsentInvalidLogSequenceException
TOCTitle: EsentInvalidLogSequenceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidlogsequenceexception(v=EXCHG.10)
ms:contentKeyID: 55107285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7877fb8b90f6fd37c502e0cc24321d37921f2575b0c5e5c88326239ffbc517f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972281"
---
# <a name="esentinvalidlogsequenceexception-class"></a>Classe EsentInvalidLogSequenceException

Classe di base per JET_err. Eccezioni InvalidLogSequence.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLogSequenceException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentInvalidLogSequenceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLogSequenceException : EsentCorruptionException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentInvalidLogSequenceException](./esentinvalidlogsequenceexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
