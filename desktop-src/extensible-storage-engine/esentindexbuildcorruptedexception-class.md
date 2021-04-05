---
description: 'Altre informazioni su: classe EsentIndexBuildCorruptedException'
title: Classe EsentIndexBuildCorruptedException
TOCTitle: EsentIndexBuildCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindexbuildcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55101803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4dc01c34f1e40d1f822ca21d3792984a07d0b62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885813"
---
# <a name="esentindexbuildcorruptedexception-class"></a><span data-ttu-id="d0d50-103">Classe EsentIndexBuildCorruptedException</span><span class="sxs-lookup"><span data-stu-id="d0d50-103">EsentIndexBuildCorruptedException class</span></span>

<span data-ttu-id="d0d50-104">Classe di base per JET_err. Eccezioni IndexBuildCorrupted.</span><span class="sxs-lookup"><span data-stu-id="d0d50-104">Base class for JET_err.IndexBuildCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d0d50-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="d0d50-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d0d50-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d0d50-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d0d50-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="d0d50-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d0d50-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d0d50-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d0d50-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d0d50-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d0d50-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="d0d50-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="d0d50-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="d0d50-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="d0d50-112">Microsoft. ISAM. esent. Interop. EsentIndexBuildCorruptedException</span><span class="sxs-lookup"><span data-stu-id="d0d50-112">Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException</span></span>  

<span data-ttu-id="d0d50-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0d50-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d0d50-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d0d50-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d50-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0d50-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexBuildCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentIndexBuildCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexBuildCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="d0d50-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="d0d50-116">Thread safety</span></span>

<span data-ttu-id="d0d50-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d0d50-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d0d50-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d0d50-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0d50-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0d50-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0d50-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d0d50-120">Reference</span></span>

[<span data-ttu-id="d0d50-121">Membri di EsentIndexBuildCorruptedException</span><span class="sxs-lookup"><span data-stu-id="d0d50-121">EsentIndexBuildCorruptedException members</span></span>](./esentindexbuildcorruptedexception-members.md)

[<span data-ttu-id="d0d50-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d0d50-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
