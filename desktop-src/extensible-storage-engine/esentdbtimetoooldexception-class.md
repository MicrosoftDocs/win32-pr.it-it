---
description: Altre informazioni sulla classe EsentDbTimeTooOldException
title: Classe EsentDbTimeTooOldException
TOCTitle: EsentDbTimeTooOldException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdbtimetoooldexception(v=EXCHG.10)
ms:contentKeyID: 55101581
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 11f719399b496dae9c42d8a1ac6a0755919d63b8cc1b45cda4aad319d3a45ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481671"
---
# <a name="esentdbtimetoooldexception-class"></a>Classe EsentDbTimeTooOldException

Classe di base per JET_err. Eccezioni DbTimeTooOld.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDbTimeTooOldException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDbTimeTooOldException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDbTimeTooOldException : EsentInconsistentException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentDbTimeTooOldException](./esentdbtimetoooldexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
