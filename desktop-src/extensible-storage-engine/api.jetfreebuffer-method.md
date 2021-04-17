---
description: 'Altre informazioni su: metodo API. JetFreeBuffer'
title: API. JetFreeBuffer, metodo
TOCTitle: 'JetFreeBuffer method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer(System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetfreebuffer(v=EXCHG.10)
ms:contentKeyID: 55100694
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a584caf0f7c59c77e7d3c4a058a03780043e0f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306300"
---
# <a name="apijetfreebuffer-method"></a>API. JetFreeBuffer, metodo

Libera la memoria allocata da una chiamata al motore di database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetFreeBuffer ( _
    buffer As IntPtr _
)
'Usage
Dim buffer As IntPtrApi.JetFreeBuffer(buffer)
```

``` csharp
public static void JetFreeBuffer(
    IntPtr buffer
)
```

#### <a name="parameters"></a>Parametri

  - buffer  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Buffer allocato da una chiamata al motore di database. [Zero](/dotnet/api/system.intptr.zero) è accettabile e verrà ignorato.

## <a name="remarks"></a>Commenti

Questo metodo è interno perché non viene mai esposta la memoria allocata da ESENT ai chiamanti.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
