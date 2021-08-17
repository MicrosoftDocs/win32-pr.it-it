---
description: Altre informazioni sulla classe EsentSoftRecoveryOnBackupDatabaseException
title: Classe EsentSoftRecoveryOnBackupDatabaseException
TOCTitle: EsentSoftRecoveryOnBackupDatabaseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnBackupDatabaseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsoftrecoveryonbackupdatabaseexception(v=EXCHG.10)
ms:contentKeyID: 55102863
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnBackupDatabaseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnBackupDatabaseException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79a5c1991d58c2a03d6d45e54b341609bd99de5fc58c230b0ffa88c49a0ad496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118771030"
---
# <a name="esentsoftrecoveryonbackupdatabaseexception-class"></a>Classe EsentSoftRecoveryOnBackupDatabaseException

Classe di base per JET_err. Eccezioni SoftRecoveryOnBackupDatabase.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnBackupDatabaseException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSoftRecoveryOnBackupDatabaseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSoftRecoveryOnBackupDatabaseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSoftRecoveryOnBackupDatabaseException : EsentUsageException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentSoftRecoveryOnBackupDatabaseException](./esentsoftrecoveryonbackupdatabaseexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
