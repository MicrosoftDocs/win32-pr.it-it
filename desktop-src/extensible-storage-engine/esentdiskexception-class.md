---
description: 'Altre informazioni su: classe EsentDiskException'
title: Classe EsentDiskException
TOCTitle: EsentDiskException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101517
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22c2e2e2f829b6fcc6967e6e58692613243549c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401765"
---
# <a name="esentdiskexception-class"></a><span data-ttu-id="40736-103">Classe EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="40736-103">EsentDiskException class</span></span>

<span data-ttu-id="40736-104">Classe di base per le eccezioni del disco.</span><span class="sxs-lookup"><span data-stu-id="40736-104">Base class for Disk exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="40736-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="40736-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="40736-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="40736-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="40736-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="40736-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="40736-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="40736-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="40736-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="40736-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="40736-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="40736-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="40736-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="40736-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="40736-112">Microsoft. ISAM. esent. Interop. EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="40736-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>  
              [<span data-ttu-id="40736-113">Microsoft. ISAM. esent. Interop. EsentDiskFullException</span><span class="sxs-lookup"><span data-stu-id="40736-113">Microsoft.Isam.Esent.Interop.EsentDiskFullException</span></span>](./esentdiskfullexception-class.md)  
              [<span data-ttu-id="40736-114">Microsoft. ISAM. esent. Interop. EsentLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="40736-114">Microsoft.Isam.Esent.Interop.EsentLogDiskFullException</span></span>](./esentlogdiskfullexception-class.md)  

<span data-ttu-id="40736-115">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40736-115">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="40736-116">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="40736-116">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40736-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40736-117">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDiskException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentDiskException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDiskException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="40736-118">Thread safety</span><span class="sxs-lookup"><span data-stu-id="40736-118">Thread safety</span></span>

<span data-ttu-id="40736-119">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="40736-119">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="40736-120">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="40736-120">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="40736-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40736-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40736-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="40736-122">Reference</span></span>

[<span data-ttu-id="40736-123">Membri di EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="40736-123">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="40736-124">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="40736-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
