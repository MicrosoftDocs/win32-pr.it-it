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
# <a name="apijetfreebuffer-method"></a><span data-ttu-id="9fdd8-103">API. JetFreeBuffer, metodo</span><span class="sxs-lookup"><span data-stu-id="9fdd8-103">Api.JetFreeBuffer method</span></span>

<span data-ttu-id="9fdd8-104">Libera la memoria allocata da una chiamata al motore di database.</span><span class="sxs-lookup"><span data-stu-id="9fdd8-104">Frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="9fdd8-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9fdd8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9fdd8-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9fdd8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9fdd8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fdd8-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="9fdd8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fdd8-108">Parameters</span></span>

  - <span data-ttu-id="9fdd8-109">buffer</span><span class="sxs-lookup"><span data-stu-id="9fdd8-109">buffer</span></span>  
    <span data-ttu-id="9fdd8-110">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="9fdd8-110">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="9fdd8-111">Buffer allocato da una chiamata al motore di database.</span><span class="sxs-lookup"><span data-stu-id="9fdd8-111">The buffer allocated by a call to the database engine.</span></span> <span data-ttu-id="9fdd8-112">[Zero](/dotnet/api/system.intptr.zero) è accettabile e verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="9fdd8-112">[Zero](/dotnet/api/system.intptr.zero) is acceptable, and will be ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fdd8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fdd8-113">Remarks</span></span>

<span data-ttu-id="9fdd8-114">Questo metodo è interno perché non viene mai esposta la memoria allocata da ESENT ai chiamanti.</span><span class="sxs-lookup"><span data-stu-id="9fdd8-114">This method is internal because we never expose the memory allocated by ESENT to our callers.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fdd8-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fdd8-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9fdd8-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9fdd8-116">Reference</span></span>

[<span data-ttu-id="9fdd8-117">Classe API</span><span class="sxs-lookup"><span data-stu-id="9fdd8-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9fdd8-118">Membri API</span><span class="sxs-lookup"><span data-stu-id="9fdd8-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9fdd8-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9fdd8-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
