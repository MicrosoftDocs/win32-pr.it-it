---
description: 'Altre informazioni su: classe EsentReadVerifyFailureException'
title: Classe EsentReadVerifyFailureException
TOCTitle: EsentReadVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentreadverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102552
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e7a66cd94fc956947e08a919287aec7f04b07ea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309665"
---
# <a name="esentreadverifyfailureexception-class"></a><span data-ttu-id="a7ae3-103">Classe EsentReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="a7ae3-103">EsentReadVerifyFailureException class</span></span>

<span data-ttu-id="a7ae3-104">Classe di base per JET_err. Eccezioni ReadVerifyFailure.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-104">Base class for JET_err.ReadVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a7ae3-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="a7ae3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a7ae3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a7ae3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a7ae3-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a7ae3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a7ae3-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="a7ae3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a7ae3-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a7ae3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a7ae3-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="a7ae3-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="a7ae3-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="a7ae3-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="a7ae3-112">Microsoft. ISAM. esent. Interop. EsentReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="a7ae3-112">Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException</span></span>  

<span data-ttu-id="a7ae3-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a7ae3-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a7ae3-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a7ae3-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ae3-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7ae3-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentReadVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentReadVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentReadVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="a7ae3-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="a7ae3-116">Thread safety</span></span>

<span data-ttu-id="a7ae3-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a7ae3-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a7ae3-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7ae3-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7ae3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7ae3-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a7ae3-120">Reference</span></span>

[<span data-ttu-id="a7ae3-121">Membri di EsentReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="a7ae3-121">EsentReadVerifyFailureException members</span></span>](./esentreadverifyfailureexception-members.md)

[<span data-ttu-id="a7ae3-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a7ae3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
