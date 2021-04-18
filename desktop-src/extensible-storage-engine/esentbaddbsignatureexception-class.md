---
description: 'Altre informazioni su: classe EsentBadDbSignatureException'
title: Classe EsentBadDbSignatureException
TOCTitle: EsentBadDbSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbaddbsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55107255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c0adf077cf0665c6bee2246c66af882a397c46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314085"
---
# <a name="esentbaddbsignatureexception-class"></a>Classe EsentBadDbSignatureException

Classe di base per JET_err. Eccezioni BadDbSignature.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentBadDbSignatureException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadDbSignatureException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentBadDbSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadDbSignatureException : EsentObsoleteException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentBadDbSignatureException](./esentbaddbsignatureexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
