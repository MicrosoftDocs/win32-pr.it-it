---
description: 'Altre informazioni su: classe EsentRollbackRequiredException'
title: Classe EsentRollbackRequiredException
TOCTitle: EsentRollbackRequiredException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrollbackrequiredexception(v=EXCHG.10)
ms:contentKeyID: 55107325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12baa9d69400cfd84c54184132c45aba4095b427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754522"
---
# <a name="esentrollbackrequiredexception-class"></a><span data-ttu-id="2ab44-103">Classe EsentRollbackRequiredException</span><span class="sxs-lookup"><span data-stu-id="2ab44-103">EsentRollbackRequiredException class</span></span>

<span data-ttu-id="2ab44-104">Classe di base per JET_err. Eccezioni RollbackRequired.</span><span class="sxs-lookup"><span data-stu-id="2ab44-104">Base class for JET_err.RollbackRequired exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2ab44-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="2ab44-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2ab44-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2ab44-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2ab44-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2ab44-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2ab44-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="2ab44-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2ab44-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2ab44-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2ab44-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="2ab44-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2ab44-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="2ab44-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="2ab44-112">Microsoft. ISAM. esent. Interop. EsentRollbackRequiredException</span><span class="sxs-lookup"><span data-stu-id="2ab44-112">Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException</span></span>  

<span data-ttu-id="2ab44-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2ab44-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2ab44-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2ab44-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab44-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ab44-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRollbackRequiredException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentRollbackRequiredException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRollbackRequiredException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="2ab44-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="2ab44-116">Thread safety</span></span>

<span data-ttu-id="2ab44-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2ab44-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2ab44-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="2ab44-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ab44-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ab44-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ab44-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2ab44-120">Reference</span></span>

[<span data-ttu-id="2ab44-121">Membri di EsentRollbackRequiredException</span><span class="sxs-lookup"><span data-stu-id="2ab44-121">EsentRollbackRequiredException members</span></span>](./esentrollbackrequiredexception-members.md)

[<span data-ttu-id="2ab44-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2ab44-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
