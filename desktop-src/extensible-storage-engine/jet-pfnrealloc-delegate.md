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
# <a name="jet_pfnrealloc-delegate"></a><span data-ttu-id="049b6-103">Delegato JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="049b6-103">JET_PFNREALLOC delegate</span></span>

<span data-ttu-id="049b6-104">Callback utilizzato da JetEnumerateColumns per allocare memoria per i buffer di output.</span><span class="sxs-lookup"><span data-stu-id="049b6-104">Callback used by JetEnumerateColumns to allocate memory for its output buffers.</span></span>

<span data-ttu-id="049b6-105">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="049b6-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="049b6-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="049b6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="049b6-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="049b6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="049b6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="049b6-108">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="049b6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="049b6-109">Parameters</span></span>

  - <span data-ttu-id="049b6-110">contesto</span><span class="sxs-lookup"><span data-stu-id="049b6-110">context</span></span>  
    <span data-ttu-id="049b6-111">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="049b6-111">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="049b6-112">Contesto assegnato a JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="049b6-112">Context given to JetEnumerateColumns.</span></span>

<!-- end list -->

  - <span data-ttu-id="049b6-113">memoria</span><span class="sxs-lookup"><span data-stu-id="049b6-113">memory</span></span>  
    <span data-ttu-id="049b6-114">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="049b6-114">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="049b6-115">Se diverso da zero, puntatore a un blocco di memoria precedentemente allocato da questo callback.</span><span class="sxs-lookup"><span data-stu-id="049b6-115">If non-zero, a pointer to a memory block previously allocated by this callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="049b6-116">requestedSize</span><span class="sxs-lookup"><span data-stu-id="049b6-116">requestedSize</span></span>  
    <span data-ttu-id="049b6-117">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="049b6-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="049b6-118">Nuova dimensione del blocco di memoria (in byte).</span><span class="sxs-lookup"><span data-stu-id="049b6-118">The new size of the memory block (in bytes).</span></span> <span data-ttu-id="049b6-119">Se è 0 e viene specificato un blocco di memoria, il blocco di memoria verrà liberato.</span><span class="sxs-lookup"><span data-stu-id="049b6-119">If this is 0 and a memory block is specified, that memory block will be freed.</span></span>

#### <a name="return-value"></a><span data-ttu-id="049b6-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="049b6-120">Return value</span></span>

<span data-ttu-id="049b6-121">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="049b6-121">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
<span data-ttu-id="049b6-122">Puntatore alla memoria appena allocata.</span><span class="sxs-lookup"><span data-stu-id="049b6-122">A pointer to newly allocated memory.</span></span> <span data-ttu-id="049b6-123">Se non è stato possibile allocare la memoria, deve essere restituito [zero](/dotnet/api/system.intptr.zero) .</span><span class="sxs-lookup"><span data-stu-id="049b6-123">If memory could not be allocated then [Zero](/dotnet/api/system.intptr.zero) should be returned.</span></span>  

## <a name="see-also"></a><span data-ttu-id="049b6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="049b6-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="049b6-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="049b6-125">Reference</span></span>

[<span data-ttu-id="049b6-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="049b6-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
