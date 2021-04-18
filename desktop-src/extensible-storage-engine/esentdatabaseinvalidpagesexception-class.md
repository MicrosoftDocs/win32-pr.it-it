---
description: 'Altre informazioni su: classe EsentDatabaseInvalidPagesException'
title: Classe EsentDatabaseInvalidPagesException
TOCTitle: EsentDatabaseInvalidPagesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPagesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseinvalidpagesexception(v=EXCHG.10)
ms:contentKeyID: 55101388
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPagesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPagesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5725a20026aed8c7252218360d98ce6ce1f47a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318457"
---
# <a name="esentdatabaseinvalidpagesexception-class"></a>Classe EsentDatabaseInvalidPagesException

Classe di base per JET_err. Eccezioni DatabaseInvalidPages.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentDatabaseInvalidPagesException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseInvalidPagesException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseInvalidPagesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseInvalidPagesException : EsentUsageException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentDatabaseInvalidPagesException](./esentdatabaseinvalidpagesexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
