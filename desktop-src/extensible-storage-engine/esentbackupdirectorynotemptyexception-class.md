---
description: Altre informazioni sulla classe EsentBackupDirectoryNotEmptyException
title: Classe EsentBackupDirectoryNotEmptyException
TOCTitle: EsentBackupDirectoryNotEmptyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupdirectorynotemptyexception(v=EXCHG.10)
ms:contentKeyID: 55101028
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7147fc0bec897fda4119edc8be5f56c28af9037b413a8d786dd33c0e79542f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737471"
---
# <a name="esentbackupdirectorynotemptyexception-class"></a>Classe EsentBackupDirectoryNotEmptyException

Classe di base per JET_err. Eccezioni BackupDirectoryNotEmpty.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException  

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupDirectoryNotEmptyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentBackupDirectoryNotEmptyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupDirectoryNotEmptyException : EsentUsageException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentBackupDirectoryNotEmptyException](./esentbackupdirectorynotemptyexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
