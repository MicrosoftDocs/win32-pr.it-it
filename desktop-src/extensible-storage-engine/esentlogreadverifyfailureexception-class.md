---
description: 'Altre informazioni su: classe EsentLogReadVerifyFailureException'
title: Classe EsentLogReadVerifyFailureException
TOCTitle: EsentLogReadVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogreadverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102142
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 937d3fa0b721b66d072817ba12c2cf8ba97d5cdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319731"
---
# <a name="esentlogreadverifyfailureexception-class"></a><span data-ttu-id="d9275-103">Classe EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="d9275-103">EsentLogReadVerifyFailureException class</span></span>

<span data-ttu-id="d9275-104">Classe di base per JET_err. Eccezioni LogReadVerifyFailure.</span><span class="sxs-lookup"><span data-stu-id="d9275-104">Base class for JET_err.LogReadVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d9275-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="d9275-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d9275-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d9275-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d9275-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="d9275-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d9275-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d9275-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d9275-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d9275-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d9275-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="d9275-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="d9275-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="d9275-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="d9275-112">Microsoft. ISAM. esent. Interop. EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="d9275-112">Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException</span></span>  

<span data-ttu-id="d9275-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9275-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9275-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d9275-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9275-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9275-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogReadVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogReadVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogReadVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="d9275-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="d9275-116">Thread safety</span></span>

<span data-ttu-id="d9275-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d9275-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d9275-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d9275-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9275-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9275-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9275-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d9275-120">Reference</span></span>

[<span data-ttu-id="d9275-121">Membri di EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="d9275-121">EsentLogReadVerifyFailureException members</span></span>](./esentlogreadverifyfailureexception-members.md)

[<span data-ttu-id="d9275-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d9275-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
