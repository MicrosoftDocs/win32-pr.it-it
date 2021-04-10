---
description: 'Altre informazioni su: classe EsentMultiValuedDuplicateAfterTruncationException'
title: Classe EsentMultiValuedDuplicateAfterTruncationException
TOCTitle: EsentMultiValuedDuplicateAfterTruncationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedduplicateaftertruncationexception(v=EXCHG.10)
ms:contentKeyID: 55102259
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4354bc53349d7c9ee4625c085b983e90b06a747f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966850"
---
# <a name="esentmultivaluedduplicateaftertruncationexception-class"></a><span data-ttu-id="f0172-103">Classe EsentMultiValuedDuplicateAfterTruncationException</span><span class="sxs-lookup"><span data-stu-id="f0172-103">EsentMultiValuedDuplicateAfterTruncationException class</span></span>

<span data-ttu-id="f0172-104">Classe di base per JET_err. Eccezioni MultiValuedDuplicateAfterTruncation.</span><span class="sxs-lookup"><span data-stu-id="f0172-104">Base class for JET_err.MultiValuedDuplicateAfterTruncation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f0172-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="f0172-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f0172-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f0172-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f0172-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f0172-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f0172-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f0172-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f0172-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f0172-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f0172-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="f0172-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f0172-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="f0172-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="f0172-112">Microsoft. ISAM. esent. Interop. EsentMultiValuedDuplicateAfterTruncationException</span><span class="sxs-lookup"><span data-stu-id="f0172-112">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException</span></span>  

<span data-ttu-id="f0172-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f0172-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f0172-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f0172-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f0172-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0172-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedDuplicateAfterTruncationException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMultiValuedDuplicateAfterTruncationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedDuplicateAfterTruncationException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="f0172-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="f0172-116">Thread safety</span></span>

<span data-ttu-id="f0172-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f0172-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f0172-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f0172-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0172-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0172-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f0172-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f0172-120">Reference</span></span>

[<span data-ttu-id="f0172-121">Membri di EsentMultiValuedDuplicateAfterTruncationException</span><span class="sxs-lookup"><span data-stu-id="f0172-121">EsentMultiValuedDuplicateAfterTruncationException members</span></span>](./esentmultivaluedduplicateaftertruncationexception-members.md)

[<span data-ttu-id="f0172-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f0172-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
