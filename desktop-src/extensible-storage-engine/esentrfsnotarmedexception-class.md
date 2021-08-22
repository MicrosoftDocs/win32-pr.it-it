---
description: Altre informazioni sulla classe EsentRfsNotArmedException
title: Classe EsentRfsNotArmedException
TOCTitle: EsentRfsNotArmedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrfsnotarmedexception(v=EXCHG.10)
ms:contentKeyID: 55102660
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c03fa4eff0d38fdb8f703e76b47c46882e901364d92e9f9fc041a7e42b94b228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619624"
---
# <a name="esentrfsnotarmedexception-class"></a>Classe EsentRfsNotArmedException

Classe di base per JET_err. Eccezioni RfsNotArmed.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRfsNotArmedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentRfsNotArmedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRfsNotArmedException : EsentObsoleteException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentRfsNotArmedException](./esentrfsnotarmedexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
