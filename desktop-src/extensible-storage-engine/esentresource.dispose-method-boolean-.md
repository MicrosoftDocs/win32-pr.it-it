---
description: 'Altre informazioni su: Metodo EsentResource.Dispose (booleano)'
title: Metodo EsentResource.Dispose (Boolean)
TOCTitle: Dispose method (Boolean)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResource.Dispose(System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource.dispose(v=EXCHG.10)
ms:contentKeyID: 55102624
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource.Dispose
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cc2f9fab375e2ae2b9a27611192c3db9e3bba4eb272de1dfca243d13bf7766f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119477331"
---
# <a name="esentresourcedispose-method-boolean"></a>Metodo EsentResource.Dispose (Boolean)

Chiamato da Dispose e dal finalizzatore.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Protected Overridable Sub Dispose ( _
    isDisposing As Boolean _
)
'Usage
Dim isDisposing As Boolean

Me.Dispose(isDisposing)
```

``` csharp
protected virtual void Dispose(
    bool isDisposing
)
```

#### <a name="parameters"></a>Parametri

  - isDisposing  
    Tipo: [System.Boolean](/dotnet/api/system.boolean)  
    
    True se viene chiamato da Dispose.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe EsentResource](./esentresource-class.md)

[Membri di EsentResource](./esentresource-members.md)

[Overload dispose](./esentresource.dispose-method.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
