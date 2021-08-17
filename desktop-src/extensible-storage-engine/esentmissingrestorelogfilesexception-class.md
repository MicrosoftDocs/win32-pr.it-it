---
description: Altre informazioni sulla classe EsentMissingRestoreLogFilesException
title: Classe EsentMissingRestoreLogFilesException
TOCTitle: EsentMissingRestoreLogFilesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingrestorelogfilesexception(v=EXCHG.10)
ms:contentKeyID: 55102315
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7bce3b7a1323b90650efee124bd9a267831edc35e594d8e3bc32436bf1d2b1bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115431"
---
# <a name="esentmissingrestorelogfilesexception-class"></a>Classe EsentMissingRestoreLogFilesException

Classe di base per JET_err. Eccezioni MissingRestoreLogFiles.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingRestoreLogFilesException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingRestoreLogFilesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingRestoreLogFilesException : EsentInconsistentException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentMissingRestoreLogFilesException](./esentmissingrestorelogfilesexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
