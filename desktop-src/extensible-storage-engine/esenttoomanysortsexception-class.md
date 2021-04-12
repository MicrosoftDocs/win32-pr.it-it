---
description: 'Altre informazioni su: classe EsentTooManySortsException'
title: Classe EsentTooManySortsException
TOCTitle: EsentTooManySortsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManySortsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanysortsexception(v=EXCHG.10)
ms:contentKeyID: 55103099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManySortsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManySortsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9048d2c7c65906ba6f093f21c604f25adfcf16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344441"
---
# <a name="esenttoomanysortsexception-class"></a><span data-ttu-id="b4fce-103">Classe EsentTooManySortsException</span><span class="sxs-lookup"><span data-stu-id="b4fce-103">EsentTooManySortsException class</span></span>

<span data-ttu-id="b4fce-104">Classe di base per JET_err. Eccezioni TooManySorts.</span><span class="sxs-lookup"><span data-stu-id="b4fce-104">Base class for JET_err.TooManySorts exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b4fce-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="b4fce-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b4fce-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b4fce-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b4fce-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b4fce-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b4fce-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="b4fce-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b4fce-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b4fce-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b4fce-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="b4fce-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="b4fce-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="b4fce-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="b4fce-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="b4fce-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="b4fce-113">Microsoft. ISAM. esent. Interop. EsentTooManySortsException</span><span class="sxs-lookup"><span data-stu-id="b4fce-113">Microsoft.Isam.Esent.Interop.EsentTooManySortsException</span></span>  

<span data-ttu-id="b4fce-114">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b4fce-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b4fce-115">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b4fce-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fce-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4fce-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManySortsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManySortsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManySortsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="b4fce-117">Thread safety</span><span class="sxs-lookup"><span data-stu-id="b4fce-117">Thread safety</span></span>

<span data-ttu-id="b4fce-118">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b4fce-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b4fce-119">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b4fce-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4fce-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4fce-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4fce-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b4fce-121">Reference</span></span>

[<span data-ttu-id="b4fce-122">Membri di EsentTooManySortsException</span><span class="sxs-lookup"><span data-stu-id="b4fce-122">EsentTooManySortsException members</span></span>](./esenttoomanysortsexception-members.md)

[<span data-ttu-id="b4fce-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b4fce-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
