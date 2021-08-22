---
description: Altre informazioni sulla classe EsentMemoryException
title: Classe EsentMemoryException
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ae3f11109ec025c0b0b0c1d907c09be3ca9393e39bd56f7b7cd190bdbb9acc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119040779"
---
# <a name="esentmemoryexception-class"></a>Classe EsentMemoryException

Classe di base per le eccezioni di memoria.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentResourceException](./esentresourceexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMemoryException  
              

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentMemoryException](./esentmemoryexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipi derivati

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentResourceException](./esentresourceexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMemoryException  
              [Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException](./esentoutofbuffersexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException](./esentoutofcursorsexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException](./esentoutoffilehandlesexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException](./esentoutofmemoryexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException](./esentoutofsessionsexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException](./esentoutofthreadsexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException](./esenttoomanymempoolentriesexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException](./esenttoomanyopenindexesexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentTooManySortsException](./esenttoomanysortsexception-class.md)