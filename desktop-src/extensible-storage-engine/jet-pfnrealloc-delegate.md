---
description: 'Altre informazioni su: JET_PFNREALLOC delegate'
title: Delegato JET_PFNREALLOC
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968617"
---
# <a name="jet_pfnrealloc-delegate"></a>Delegato JET_PFNREALLOC

Callback utilizzato da JetEnumerateColumns per allocare memoria per i buffer di output.

Questa API non è conforme a CLS. 

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a>Parametri

  - contesto  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Contesto assegnato a JetEnumerateColumns.

<!-- end list -->

  - memoria  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Se diverso da zero, puntatore a un blocco di memoria precedentemente allocato da questo callback.

<!-- end list -->

  - requestedSize  
    Tipo: [System. UInt32](/dotnet/api/system.uint32)  
    
    Nuova dimensione del blocco di memoria (in byte). Se è 0 e viene specificato un blocco di memoria, il blocco di memoria verrà liberato.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
Puntatore alla memoria appena allocata. Se non è stato possibile allocare la memoria, deve essere restituito [zero](/dotnet/api/system.intptr.zero) .  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
