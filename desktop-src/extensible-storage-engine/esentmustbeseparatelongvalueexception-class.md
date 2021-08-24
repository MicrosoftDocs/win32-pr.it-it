---
description: Altre informazioni sulla classe EsentMustBeSeparateLongValueException
title: Classe EsentMustBeSeparateLongValueException
TOCTitle: EsentMustBeSeparateLongValueException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMustBeSeparateLongValueException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmustbeseparatelongvalueexception(v=EXCHG.10)
ms:contentKeyID: 55102269
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMustBeSeparateLongValueException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMustBeSeparateLongValueException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d8611397e001e74eab15af8c0d45235e0806c0938cd703b37ee9358aead1e17d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722761"
---
# <a name="esentmustbeseparatelongvalueexception-class"></a>Classe EsentMustBeSeparateLongValueException

Classe di base per JET_err. Eccezioni MustBeSeparateLongValue.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMustBeSeparateLongValueException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMustBeSeparateLongValueException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMustBeSeparateLongValueException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMustBeSeparateLongValueException : EsentUsageException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentMustBeSeparateLongValueException](./esentmustbeseparatelongvalueexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
