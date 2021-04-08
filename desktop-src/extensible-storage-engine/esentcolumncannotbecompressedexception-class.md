---
description: 'Altre informazioni su: classe EsentColumnCannotBeCompressedException'
title: Classe EsentColumnCannotBeCompressedException
TOCTitle: EsentColumnCannotBeCompressedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumncannotbecompressedexception(v=EXCHG.10)
ms:contentKeyID: 55101403
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1159125aaa9f1c522e3e3d1374bda772ce6c5db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058260"
---
# <a name="esentcolumncannotbecompressedexception-class"></a>Classe EsentColumnCannotBeCompressedException

Classe di base per JET_err. Eccezioni ColumnCannotBeCompressed.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentColumnCannotBeCompressedException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnCannotBeCompressedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnCannotBeCompressedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnCannotBeCompressedException : EsentUsageException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentColumnCannotBeCompressedException](./esentcolumncannotbecompressedexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
