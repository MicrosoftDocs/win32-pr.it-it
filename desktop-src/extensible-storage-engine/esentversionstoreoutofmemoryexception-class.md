---
description: 'Altre informazioni su: classe EsentVersionStoreOutOfMemoryException'
title: Classe EsentVersionStoreOutOfMemoryException
TOCTitle: EsentVersionStoreOutOfMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversionstoreoutofmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55103197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1780826cb9b4578a4acfd14c53a38589eca42d84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319219"
---
# <a name="esentversionstoreoutofmemoryexception-class"></a>Classe EsentVersionStoreOutOfMemoryException

Classe di base per JET_err. Eccezioni VersionStoreOutOfMemory.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentQuotaException](./esentquotaexception-class.md)  
              Microsoft. ISAM. esent. Interop. EsentVersionStoreOutOfMemoryException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentVersionStoreOutOfMemoryException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentVersionStoreOutOfMemoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentVersionStoreOutOfMemoryException : EsentQuotaException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentVersionStoreOutOfMemoryException](./esentversionstoreoutofmemoryexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
