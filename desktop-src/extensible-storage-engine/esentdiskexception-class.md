---
description: 'Altre informazioni su: classe EsentDiskException'
title: Classe EsentDiskException
TOCTitle: EsentDiskException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101517
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22c2e2e2f829b6fcc6967e6e58692613243549c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401765"
---
# <a name="esentdiskexception-class"></a>Classe EsentDiskException

Classe di base per le eccezioni del disco.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentDiskException  
              [Microsoft. ISAM. esent. Interop. EsentDiskFullException](./esentdiskfullexception-class.md)  
              [Microsoft. ISAM. esent. Interop. EsentLogDiskFullException](./esentlogdiskfullexception-class.md)  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDiskException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentDiskException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDiskException : EsentResourceException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentDiskException](./esentdiskexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
