---
description: 'Altre informazioni su: classe EsentOutOfMemoryException'
title: Classe EsentOutOfMemoryException
TOCTitle: EsentOutOfMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d766bdfa115db7e43cbee6242e41a5c7cdb281b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226292"
---
# <a name="esentoutofmemoryexception-class"></a><span data-ttu-id="bd04a-103">Classe EsentOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="bd04a-103">EsentOutOfMemoryException class</span></span>

<span data-ttu-id="bd04a-104">Classe di base per JET_err. Eccezioni OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="bd04a-104">Base class for JET_err.OutOfMemory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="bd04a-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="bd04a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="bd04a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="bd04a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="bd04a-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="bd04a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="bd04a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="bd04a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="bd04a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="bd04a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="bd04a-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="bd04a-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="bd04a-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="bd04a-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="bd04a-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="bd04a-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="bd04a-113">Microsoft. ISAM. esent. Interop. EsentOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="bd04a-113">Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException</span></span>  

<span data-ttu-id="bd04a-114">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bd04a-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bd04a-115">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bd04a-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bd04a-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd04a-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfMemoryException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfMemoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfMemoryException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="bd04a-117">Thread safety</span><span class="sxs-lookup"><span data-stu-id="bd04a-117">Thread safety</span></span>

<span data-ttu-id="bd04a-118">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="bd04a-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="bd04a-119">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="bd04a-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd04a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd04a-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bd04a-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="bd04a-121">Reference</span></span>

[<span data-ttu-id="bd04a-122">Membri di EsentOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="bd04a-122">EsentOutOfMemoryException members</span></span>](./esentoutofmemoryexception-members.md)

[<span data-ttu-id="bd04a-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bd04a-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
