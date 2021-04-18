---
description: 'Altre informazioni su: classe EsentCallbackNotResolvedException'
title: Classe EsentCallbackNotResolvedException
TOCTitle: EsentCallbackNotResolvedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCallbackNotResolvedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcallbacknotresolvedexception(v=EXCHG.10)
ms:contentKeyID: 55107258
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCallbackNotResolvedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCallbackNotResolvedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a730ce6779f41fb348a7e9685dd9ffc132897824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305538"
---
# <a name="esentcallbacknotresolvedexception-class"></a><span data-ttu-id="eb16e-103">Classe EsentCallbackNotResolvedException</span><span class="sxs-lookup"><span data-stu-id="eb16e-103">EsentCallbackNotResolvedException class</span></span>

<span data-ttu-id="eb16e-104">Classe di base per JET_err. Eccezioni CallbackNotResolved.</span><span class="sxs-lookup"><span data-stu-id="eb16e-104">Base class for JET_err.CallbackNotResolved exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="eb16e-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="eb16e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="eb16e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="eb16e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="eb16e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="eb16e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="eb16e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="eb16e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="eb16e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="eb16e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="eb16e-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="eb16e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="eb16e-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="eb16e-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="eb16e-112">Microsoft. ISAM. esent. Interop. EsentCallbackNotResolvedException</span><span class="sxs-lookup"><span data-stu-id="eb16e-112">Microsoft.Isam.Esent.Interop.EsentCallbackNotResolvedException</span></span>  

<span data-ttu-id="eb16e-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb16e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eb16e-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb16e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb16e-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb16e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCallbackNotResolvedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCallbackNotResolvedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCallbackNotResolvedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="eb16e-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="eb16e-116">Thread safety</span></span>

<span data-ttu-id="eb16e-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="eb16e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="eb16e-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="eb16e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb16e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb16e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb16e-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="eb16e-120">Reference</span></span>

[<span data-ttu-id="eb16e-121">Membri di EsentCallbackNotResolvedException</span><span class="sxs-lookup"><span data-stu-id="eb16e-121">EsentCallbackNotResolvedException members</span></span>](./esentcallbacknotresolvedexception-members.md)

[<span data-ttu-id="eb16e-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="eb16e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
