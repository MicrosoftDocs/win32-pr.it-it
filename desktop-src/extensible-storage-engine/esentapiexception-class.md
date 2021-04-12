---
description: 'Altre informazioni su: classe EsentApiException'
title: Classe EsentApiException
TOCTitle: EsentApiException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentApiException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101032
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentApiException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b01747d2ecb197ce99617b8c9206d4fada8c2a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233773"
---
# <a name="esentapiexception-class"></a><span data-ttu-id="c3a0e-103">Classe EsentApiException</span><span class="sxs-lookup"><span data-stu-id="c3a0e-103">EsentApiException class</span></span>

<span data-ttu-id="c3a0e-104">Classe di base per le eccezioni API.</span><span class="sxs-lookup"><span data-stu-id="c3a0e-104">Base class for API exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c3a0e-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="c3a0e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c3a0e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c3a0e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c3a0e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c3a0e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c3a0e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c3a0e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c3a0e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c3a0e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="c3a0e-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="c3a0e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>  
          [<span data-ttu-id="c3a0e-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="c3a0e-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
          [<span data-ttu-id="c3a0e-112">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="c3a0e-112">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
          [<span data-ttu-id="c3a0e-113">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="c3a0e-113">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  

<span data-ttu-id="c3a0e-114">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3a0e-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3a0e-115">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3a0e-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a0e-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3a0e-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentApiException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentApiException
```

``` csharp
[SerializableAttribute]
public abstract class EsentApiException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="c3a0e-117">Thread safety</span><span class="sxs-lookup"><span data-stu-id="c3a0e-117">Thread safety</span></span>

<span data-ttu-id="c3a0e-118">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c3a0e-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c3a0e-119">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c3a0e-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3a0e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3a0e-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3a0e-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c3a0e-121">Reference</span></span>

[<span data-ttu-id="c3a0e-122">Membri di EsentApiException</span><span class="sxs-lookup"><span data-stu-id="c3a0e-122">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="c3a0e-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c3a0e-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
