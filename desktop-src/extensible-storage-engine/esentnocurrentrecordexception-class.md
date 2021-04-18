---
description: 'Altre informazioni su: classe EsentNoCurrentRecordException'
title: Classe EsentNoCurrentRecordException
TOCTitle: EsentNoCurrentRecordException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnocurrentrecordexception(v=EXCHG.10)
ms:contentKeyID: 55102290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed58890ccd410101ecc6e6f38fafa0d254f4c2d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319239"
---
# <a name="esentnocurrentrecordexception-class"></a>Classe EsentNoCurrentRecordException

Classe di base per JET_err. Eccezioni NoCurrentRecord.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentStateException](./esentstateexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentNoCurrentRecordException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNoCurrentRecordException _
    Inherits EsentStateException
'Usage
Dim instance As EsentNoCurrentRecordException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNoCurrentRecordException : EsentStateException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentNoCurrentRecordException](./esentnocurrentrecordexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
