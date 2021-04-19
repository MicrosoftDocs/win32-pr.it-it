---
description: 'Altre informazioni su: classe EsentQuotaException'
title: Classe EsentQuotaException
TOCTitle: EsentQuotaException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentQuotaException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102495
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53b108a4d55553788a6c2d316f93f4f8efc76035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317449"
---
# <a name="esentquotaexception-class"></a><span data-ttu-id="f4a6f-103">Classe EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-103">EsentQuotaException class</span></span>

<span data-ttu-id="f4a6f-104">Classe di base per le eccezioni di quota.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-104">Base class for Quota exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f4a6f-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="f4a6f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f4a6f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f4a6f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f4a6f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f4a6f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f4a6f-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f4a6f-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f4a6f-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="f4a6f-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="f4a6f-112">Microsoft. ISAM. esent. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>  
              [<span data-ttu-id="f4a6f-113">Microsoft. ISAM. esent. Interop. EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-113">Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException</span></span>](./esentoutofdatabasespaceexception-class.md)  
              [<span data-ttu-id="f4a6f-114">Microsoft. ISAM. esent. Interop. EsentTooManyInstancesException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-114">Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException</span></span>](./esenttoomanyinstancesexception-class.md)  
              [<span data-ttu-id="f4a6f-115">Microsoft. ISAM. esent. Interop. EsentTooManyOpenTablesException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-115">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException</span></span>](./esenttoomanyopentablesexception-class.md)  
              [<span data-ttu-id="f4a6f-116">Microsoft. ISAM. esent. Interop. EsentVersionStoreOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-116">Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException</span></span>](./esentversionstoreoutofmemoryexception-class.md)  

<span data-ttu-id="f4a6f-117">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f4a6f-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f4a6f-118">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f4a6f-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a6f-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4a6f-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentQuotaException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentQuotaException
```

``` csharp
[SerializableAttribute]
public abstract class EsentQuotaException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="f4a6f-120">Thread safety</span><span class="sxs-lookup"><span data-stu-id="f4a6f-120">Thread safety</span></span>

<span data-ttu-id="f4a6f-121">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f4a6f-122">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f4a6f-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4a6f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4a6f-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f4a6f-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f4a6f-124">Reference</span></span>

[<span data-ttu-id="f4a6f-125">Membri di EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="f4a6f-125">EsentQuotaException members</span></span>](./esentquotaexception-members.md)

[<span data-ttu-id="f4a6f-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f4a6f-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
