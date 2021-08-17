---
description: Altre informazioni sulla classe EsentResource
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
ms.openlocfilehash: 2f29c322b112994159799fd34a7db7a149cf6e7593b132fe4925838335bccdd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119970931"
---
# <a name="esentresource-class"></a>Classe EsentResource

Si tratta della classe di base per tutti gli oggetti risorsa di esent. Le sottoclassi di questa classe possono allocare e rilasciare risorse non gestite.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  Microsoft.Isam.Esent.Interop.EsentResource  
    [Microsoft.Isam.Esent.Interop.Session](./session-class.md)  
    [Microsoft.Isam.Esent.Interop.Table](./table-class.md)  
    [Microsoft.Isam.Esent.Interop.Transaction](./transaction-class.md)  
    [Microsoft.Isam.Esent.Interop.Update](./update-class.md)  
    [Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback](./durablecommitcallback-class.md)  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
