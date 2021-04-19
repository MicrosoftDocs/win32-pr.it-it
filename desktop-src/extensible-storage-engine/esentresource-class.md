---
description: 'Altre informazioni su: classe EsentResource'
title: Classe EsentResource
TOCTitle: EsentResource class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource(v=EXCHG.10)
ms:contentKeyID: 55102575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 607fb59d6f9f89c33e685ed411ae9dc95eaa6818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308042"
---
# <a name="esentresource-class"></a>Classe EsentResource

Si tratta della classe di base per tutti gli oggetti risorsa esent. Le sottoclassi di questa classe possono allocare e rilasciare le risorse non gestite.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  Microsoft. ISAM. esent. Interop. EsentResource  
    [Microsoft. ISAM. esent. Interop. Session](./session-class.md)  
    [Microsoft. ISAM. esent. Interop. Table](./table-class.md)  
    [Microsoft. ISAM. esent. Interop. Transaction](./transaction-class.md)  
    [Microsoft. ISAM. esent. Interop. Update](./update-class.md)  
    [Microsoft. ISAM. esent. Interop. Windows8. DurableCommitCallback](./durablecommitcallback-class.md)  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public MustInherit Class EsentResource _
    Implements IDisposable
'Usage
Dim instance As EsentResource
```

``` csharp
public abstract class EsentResource : IDisposable
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentResource](./esentresource-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
