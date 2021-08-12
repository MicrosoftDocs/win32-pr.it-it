---
description: Altre informazioni sulla classe EsentGivenLogFileIsNotContiguousException
title: Classe EsentGivenLogFileIsNotContiguousException
TOCTitle: EsentGivenLogFileIsNotContiguousException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentgivenlogfileisnotcontiguousexception(v=EXCHG.10)
ms:contentKeyID: 55101788
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e1ed504581d47c4c20072aed320080351ca2f42cc15296d42aac1386a1a86f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118268308"
---
# <a name="esentgivenlogfileisnotcontiguousexception-class"></a>Classe EsentGivenLogFileIsNotContiguousException

Classe di base per JET_err. Eccezioni GivenLogFileIsNotContiguous.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentGivenLogFileIsNotContiguousException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentGivenLogFileIsNotContiguousException
```

``` csharp
[SerializableAttribute]
public sealed class EsentGivenLogFileIsNotContiguousException : EsentInconsistentException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentGivenLogFileIsNotContiguousException](./esentgivenlogfileisnotcontiguousexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
