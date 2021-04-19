---
description: 'Altre informazioni su: classe EsentNullKeyDisallowedException'
title: Classe EsentNullKeyDisallowedException
TOCTitle: EsentNullKeyDisallowedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnullkeydisallowedexception(v=EXCHG.10)
ms:contentKeyID: 55102391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3b38e043572b1182cd099664cf09dfc229efc8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313633"
---
# <a name="esentnullkeydisallowedexception-class"></a><span data-ttu-id="89ad3-103">Classe EsentNullKeyDisallowedException</span><span class="sxs-lookup"><span data-stu-id="89ad3-103">EsentNullKeyDisallowedException class</span></span>

<span data-ttu-id="89ad3-104">Classe di base per JET_err. Eccezioni NullKeyDisallowed.</span><span class="sxs-lookup"><span data-stu-id="89ad3-104">Base class for JET_err.NullKeyDisallowed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="89ad3-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="89ad3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="89ad3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="89ad3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="89ad3-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="89ad3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="89ad3-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="89ad3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="89ad3-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="89ad3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="89ad3-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="89ad3-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="89ad3-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="89ad3-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="89ad3-112">Microsoft. ISAM. esent. Interop. EsentNullKeyDisallowedException</span><span class="sxs-lookup"><span data-stu-id="89ad3-112">Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException</span></span>  

<span data-ttu-id="89ad3-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89ad3-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89ad3-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89ad3-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89ad3-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89ad3-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNullKeyDisallowedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentNullKeyDisallowedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNullKeyDisallowedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="89ad3-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="89ad3-116">Thread safety</span></span>

<span data-ttu-id="89ad3-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="89ad3-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="89ad3-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="89ad3-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="89ad3-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89ad3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89ad3-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="89ad3-120">Reference</span></span>

[<span data-ttu-id="89ad3-121">Membri di EsentNullKeyDisallowedException</span><span class="sxs-lookup"><span data-stu-id="89ad3-121">EsentNullKeyDisallowedException members</span></span>](./esentnullkeydisallowedexception-members.md)

[<span data-ttu-id="89ad3-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="89ad3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
