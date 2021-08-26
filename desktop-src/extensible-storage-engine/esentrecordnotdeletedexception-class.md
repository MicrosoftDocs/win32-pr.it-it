---
description: Altre informazioni sulla classe EsentRecordNotDeletedException
title: Classe EsentRecordNotDeletedException
TOCTitle: EsentRecordNotDeletedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordnotdeletedexception(v=EXCHG.10)
ms:contentKeyID: 55102578
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d17fcf87dbe014efa51bbff65b44d3c00c963736c0161cbf83e42a77a1cc0004
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018811"
---
# <a name="esentrecordnotdeletedexception-class"></a>Classe EsentRecordNotDeletedException

Classe di base per JET_err. Eccezioni RecordNotDeleted.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException  

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordNotDeletedException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentRecordNotDeletedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordNotDeletedException : EsentOperationException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentRecordNotDeletedException](./esentrecordnotdeletedexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
