---
description: 'Altre informazioni su: classe EsentTaskDroppedException'
title: Classe EsentTaskDroppedException
TOCTitle: EsentTaskDroppedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttaskdroppedexception(v=EXCHG.10)
ms:contentKeyID: 55103022
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4770f405ff7ca8875e3e2a960dea846e2f34ff6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529185"
---
# <a name="esenttaskdroppedexception-class"></a>Classe EsentTaskDroppedException

Classe di base per JET_err. Eccezioni TaskDropped.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentTaskDroppedException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTaskDroppedException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentTaskDroppedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTaskDroppedException : EsentResourceException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentTaskDroppedException](./esenttaskdroppedexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
