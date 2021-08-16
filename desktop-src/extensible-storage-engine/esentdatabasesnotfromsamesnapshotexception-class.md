---
description: Altre informazioni sulla classe EsentDatabasesNotFromSameSnapshotException
title: Classe EsentDatabasesNotFromSameSnapshotException
TOCTitle: EsentDatabasesNotFromSameSnapshotException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasesnotfromsamesnapshotexception(v=EXCHG.10)
ms:contentKeyID: 55101443
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4a10d8a04c1b6d67ce7e388908ff996ca7db48a174998cd1c68da82c770315c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119116141"
---
# <a name="esentdatabasesnotfromsamesnapshotexception-class"></a>Classe EsentDatabasesNotFromSameSnapshotException

Classe di base per JET_err. Eccezioni DatabasesNotFromSameSnapshot.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException  

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabasesNotFromSameSnapshotException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabasesNotFromSameSnapshotException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabasesNotFromSameSnapshotException : EsentObsoleteException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentDatabasesNotFromSameSnapshotException](./esentdatabasesnotfromsamesnapshotexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
