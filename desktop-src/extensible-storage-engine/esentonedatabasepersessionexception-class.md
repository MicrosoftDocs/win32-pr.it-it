---
description: 'Altre informazioni su: classe EsentOneDatabasePerSessionException'
title: Classe EsentOneDatabasePerSessionException
TOCTitle: EsentOneDatabasePerSessionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentonedatabasepersessionexception(v=EXCHG.10)
ms:contentKeyID: 55102432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b5f8c69397c9105eed8b0788faf3fe24af744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310893"
---
# <a name="esentonedatabasepersessionexception-class"></a><span data-ttu-id="e6dee-103">Classe EsentOneDatabasePerSessionException</span><span class="sxs-lookup"><span data-stu-id="e6dee-103">EsentOneDatabasePerSessionException class</span></span>

<span data-ttu-id="e6dee-104">Classe di base per JET_err. Eccezioni OneDatabasePerSession.</span><span class="sxs-lookup"><span data-stu-id="e6dee-104">Base class for JET_err.OneDatabasePerSession exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e6dee-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="e6dee-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e6dee-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e6dee-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e6dee-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e6dee-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e6dee-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="e6dee-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e6dee-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e6dee-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e6dee-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="e6dee-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e6dee-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="e6dee-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e6dee-112">Microsoft. ISAM. esent. Interop. EsentOneDatabasePerSessionException</span><span class="sxs-lookup"><span data-stu-id="e6dee-112">Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException</span></span>  

<span data-ttu-id="e6dee-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6dee-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e6dee-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6dee-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6dee-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6dee-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOneDatabasePerSessionException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentOneDatabasePerSessionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOneDatabasePerSessionException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e6dee-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="e6dee-116">Thread safety</span></span>

<span data-ttu-id="e6dee-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e6dee-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e6dee-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e6dee-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6dee-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6dee-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6dee-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e6dee-120">Reference</span></span>

[<span data-ttu-id="e6dee-121">Membri di EsentOneDatabasePerSessionException</span><span class="sxs-lookup"><span data-stu-id="e6dee-121">EsentOneDatabasePerSessionException members</span></span>](./esentonedatabasepersessionexception-members.md)

[<span data-ttu-id="e6dee-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e6dee-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
