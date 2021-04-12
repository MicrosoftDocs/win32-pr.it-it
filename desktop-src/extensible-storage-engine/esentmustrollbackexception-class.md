---
description: 'Altre informazioni su: classe EsentMustRollbackException'
title: Classe EsentMustRollbackException
TOCTitle: EsentMustRollbackException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMustRollbackException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmustrollbackexception(v=EXCHG.10)
ms:contentKeyID: 55102335
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMustRollbackException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMustRollbackException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f7b5399db919b497579e25fae86de14003852fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528410"
---
# <a name="esentmustrollbackexception-class"></a><span data-ttu-id="69b06-103">Classe EsentMustRollbackException</span><span class="sxs-lookup"><span data-stu-id="69b06-103">EsentMustRollbackException class</span></span>

<span data-ttu-id="69b06-104">Classe di base per JET_err. Eccezioni MustRollback.</span><span class="sxs-lookup"><span data-stu-id="69b06-104">Base class for JET_err.MustRollback exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="69b06-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="69b06-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="69b06-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="69b06-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="69b06-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="69b06-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="69b06-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="69b06-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="69b06-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="69b06-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="69b06-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="69b06-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="69b06-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="69b06-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="69b06-112">Microsoft. ISAM. esent. Interop. EsentMustRollbackException</span><span class="sxs-lookup"><span data-stu-id="69b06-112">Microsoft.Isam.Esent.Interop.EsentMustRollbackException</span></span>  

<span data-ttu-id="69b06-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69b06-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69b06-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69b06-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69b06-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69b06-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMustRollbackException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMustRollbackException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMustRollbackException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="69b06-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="69b06-116">Thread safety</span></span>

<span data-ttu-id="69b06-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="69b06-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="69b06-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="69b06-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="69b06-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69b06-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69b06-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="69b06-120">Reference</span></span>

[<span data-ttu-id="69b06-121">Membri di EsentMustRollbackException</span><span class="sxs-lookup"><span data-stu-id="69b06-121">EsentMustRollbackException members</span></span>](./esentmustrollbackexception-members.md)

[<span data-ttu-id="69b06-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="69b06-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
