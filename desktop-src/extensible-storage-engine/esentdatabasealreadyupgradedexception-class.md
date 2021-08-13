---
description: Altre informazioni sulla classe EsentDatabaseAlreadyUpgradedException
title: Classe EsentDatabaseAlreadyUpgradedException
TOCTitle: EsentDatabaseAlreadyUpgradedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasealreadyupgradedexception(v=EXCHG.10)
ms:contentKeyID: 55101322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8a187ad99281b048616eaf3889c4dcc56c4f4ddb22463575cb44d4e1c4a2096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118781515"
---
# <a name="esentdatabasealreadyupgradedexception-class"></a>Classe EsentDatabaseAlreadyUpgradedException

Classe di base per JET_err. Eccezioni DatabaseAlreadyUpgraded.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseAlreadyUpgradedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseAlreadyUpgradedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseAlreadyUpgradedException : EsentStateException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentDatabaseAlreadyUpgradedException](./esentdatabasealreadyupgradedexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
