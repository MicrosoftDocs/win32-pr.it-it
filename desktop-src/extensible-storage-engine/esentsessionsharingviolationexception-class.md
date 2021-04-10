---
description: 'Altre informazioni su: classe EsentSessionSharingViolationException'
title: Classe EsentSessionSharingViolationException
TOCTitle: EsentSessionSharingViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessionsharingviolationexception(v=EXCHG.10)
ms:contentKeyID: 55102713
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1303792b8d45ec169211c1e176d913db682c850b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968729"
---
# <a name="esentsessionsharingviolationexception-class"></a><span data-ttu-id="e0e24-103">Classe EsentSessionSharingViolationException</span><span class="sxs-lookup"><span data-stu-id="e0e24-103">EsentSessionSharingViolationException class</span></span>

<span data-ttu-id="e0e24-104">Classe di base per JET_err. Eccezioni SessionSharingViolation.</span><span class="sxs-lookup"><span data-stu-id="e0e24-104">Base class for JET_err.SessionSharingViolation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e0e24-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="e0e24-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e0e24-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e0e24-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e0e24-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e0e24-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e0e24-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="e0e24-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e0e24-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e0e24-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e0e24-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="e0e24-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e0e24-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="e0e24-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e0e24-112">Microsoft. ISAM. esent. Interop. EsentSessionSharingViolationException</span><span class="sxs-lookup"><span data-stu-id="e0e24-112">Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException</span></span>  

<span data-ttu-id="e0e24-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e0e24-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e0e24-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e0e24-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e24-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0e24-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionSharingViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionSharingViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionSharingViolationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e0e24-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="e0e24-116">Thread safety</span></span>

<span data-ttu-id="e0e24-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e0e24-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e0e24-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e0e24-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0e24-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0e24-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e0e24-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e0e24-120">Reference</span></span>

[<span data-ttu-id="e0e24-121">Membri di EsentSessionSharingViolationException</span><span class="sxs-lookup"><span data-stu-id="e0e24-121">EsentSessionSharingViolationException members</span></span>](./esentsessionsharingviolationexception-members.md)

[<span data-ttu-id="e0e24-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e0e24-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
