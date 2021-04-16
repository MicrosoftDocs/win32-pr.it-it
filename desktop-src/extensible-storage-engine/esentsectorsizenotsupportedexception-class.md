---
description: 'Altre informazioni su: classe EsentSectorSizeNotSupportedException'
title: Classe EsentSectorSizeNotSupportedException
TOCTitle: EsentSectorSizeNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsectorsizenotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55107328
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2320c46869308296b697298f1e957f0cea8ca915
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530187"
---
# <a name="esentsectorsizenotsupportedexception-class"></a>Classe EsentSectorSizeNotSupportedException

Classe di base per JET_err. Eccezioni SectorSizeNotSupported.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentFatalException](./esentfatalexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentSectorSizeNotSupportedException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSectorSizeNotSupportedException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentSectorSizeNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSectorSizeNotSupportedException : EsentFatalException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentSectorSizeNotSupportedException](./esentsectorsizenotsupportedexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
