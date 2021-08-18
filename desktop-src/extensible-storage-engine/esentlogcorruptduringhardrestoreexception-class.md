---
description: Altre informazioni sulla classe EsentLogCorruptDuringHardRestoreException
title: Classe EsentLogCorruptDuringHardRestoreException
TOCTitle: EsentLogCorruptDuringHardRestoreException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogcorruptduringhardrestoreexception(v=EXCHG.10)
ms:contentKeyID: 55102073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a11e072a3cef1c01041e52737186597e060c99877c96ad5b0c35964e4e0faa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115771"
---
# <a name="esentlogcorruptduringhardrestoreexception-class"></a>Classe EsentLogCorruptDuringHardRestoreException

Classe di base per JET_err. Eccezioni LogCorruptDuringHardRestore.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogCorruptDuringHardRestoreException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogCorruptDuringHardRestoreException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogCorruptDuringHardRestoreException : EsentCorruptionException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentLogCorruptDuringHardRestoreException](./esentlogcorruptduringhardrestoreexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
