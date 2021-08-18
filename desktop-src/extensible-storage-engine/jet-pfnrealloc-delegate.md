---
description: 'Altre informazioni su: JET_PFNREALLOC delegato'
title: JET_PFNREALLOC delegato
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
ms.openlocfilehash: 445cd4084ff187fba0b94e210d587b04660c0fb4dfe9e882e0c5696bfd5392df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730421"
---
# <a name="jet_pfnrealloc-delegate"></a>JET_PFNREALLOC delegato

Callback utilizzato da JetEnumerateColumns per allocare memoria per i buffer di output.

Questa API non è conforme a CLS. 

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Contesto assegnato a JetEnumerateColumns.

<!-- end list -->

  - memoria  
    Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Se diverso da zero, puntatore a un blocco di memoria allocato in precedenza da questo callback.

<!-- end list -->

  - requestedSize  
    Tipo: [System.UInt32](/dotnet/api/system.uint32)  
    
    Nuova dimensione del blocco di memoria (in byte). Se è 0 e viene specificato un blocco di memoria, tale blocco di memoria verrà liberato.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
Puntatore alla memoria appena allocata. Se non è stato possibile allocare memoria, deve essere [restituito zero.](/dotnet/api/system.intptr.zero)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
