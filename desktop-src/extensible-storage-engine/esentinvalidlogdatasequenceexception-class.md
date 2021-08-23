---
description: Altre informazioni sulla classe EsentInvalidLogDataSequenceException
title: Classe EsentInvalidLogDataSequenceException
TOCTitle: EsentInvalidLogDataSequenceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidlogdatasequenceexception(v=EXCHG.10)
ms:contentKeyID: 55101973
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a37553555f5c89b191257fa84a7a751b11ad11ffae37ea0bc21ba06f249f5ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982263"
---
# <a name="esentinvalidlogdatasequenceexception-class"></a>Classe EsentInvalidLogDataSequenceException

Classe di base per JET_err. Eccezioni InvalidLogDataSequence.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException  

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLogDataSequenceException _
    Inherits EsentStateException
'Usage
Dim instance As EsentInvalidLogDataSequenceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLogDataSequenceException : EsentStateException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentInvalidLogDataSequenceException](./esentinvalidlogdatasequenceexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
