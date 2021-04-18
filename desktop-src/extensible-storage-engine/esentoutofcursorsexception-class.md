---
description: 'Altre informazioni su: classe EsentOutOfCursorsException'
title: Classe EsentOutOfCursorsException
TOCTitle: EsentOutOfCursorsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofcursorsexception(v=EXCHG.10)
ms:contentKeyID: 55102451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14bbccde7e986768451c0e42c27527ab572c1660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310870"
---
# <a name="esentoutofcursorsexception-class"></a>Classe EsentOutOfCursorsException

Classe di base per JET_err. Eccezioni OutOfCursors.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMemoryException](./esentmemoryexception-class.md)  
              Microsoft. ISAM. esent. Interop. EsentOutOfCursorsException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfCursorsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfCursorsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfCursorsException : EsentMemoryException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentOutOfCursorsException](./esentoutofcursorsexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
