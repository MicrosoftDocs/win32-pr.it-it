---
description: 'Altre informazioni su: classe EsentPageSizeMismatchException'
title: Classe EsentPageSizeMismatchException
TOCTitle: EsentPageSizeMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpagesizemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55102466
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0573603fae445e1e5ae9d9768c3a0ffcf38f283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314063"
---
# <a name="esentpagesizemismatchexception-class"></a>Classe EsentPageSizeMismatchException

Classe di base per JET_err. Eccezioni PageSizeMismatch.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentPageSizeMismatchException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPageSizeMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentPageSizeMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPageSizeMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentPageSizeMismatchException](./esentpagesizemismatchexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
