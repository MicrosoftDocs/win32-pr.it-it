---
description: 'Altre informazioni su: classe EsentTaskDroppedException'
title: Classe EsentTaskDroppedException
TOCTitle: EsentTaskDroppedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttaskdroppedexception(v=EXCHG.10)
ms:contentKeyID: 55103022
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4770f405ff7ca8875e3e2a960dea846e2f34ff6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529185"
---
# <a name="esenttaskdroppedexception-class"></a><span data-ttu-id="b30e7-103">Classe EsentTaskDroppedException</span><span class="sxs-lookup"><span data-stu-id="b30e7-103">EsentTaskDroppedException class</span></span>

<span data-ttu-id="b30e7-104">Classe di base per JET_err. Eccezioni TaskDropped.</span><span class="sxs-lookup"><span data-stu-id="b30e7-104">Base class for JET_err.TaskDropped exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b30e7-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="b30e7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b30e7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b30e7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b30e7-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b30e7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b30e7-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="b30e7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b30e7-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b30e7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b30e7-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="b30e7-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="b30e7-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="b30e7-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="b30e7-112">Microsoft. ISAM. esent. Interop. EsentTaskDroppedException</span><span class="sxs-lookup"><span data-stu-id="b30e7-112">Microsoft.Isam.Esent.Interop.EsentTaskDroppedException</span></span>  

<span data-ttu-id="b30e7-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b30e7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b30e7-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b30e7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b30e7-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b30e7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTaskDroppedException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentTaskDroppedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTaskDroppedException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="b30e7-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="b30e7-116">Thread safety</span></span>

<span data-ttu-id="b30e7-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b30e7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b30e7-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b30e7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b30e7-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b30e7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b30e7-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b30e7-120">Reference</span></span>

[<span data-ttu-id="b30e7-121">Membri di EsentTaskDroppedException</span><span class="sxs-lookup"><span data-stu-id="b30e7-121">EsentTaskDroppedException members</span></span>](./esenttaskdroppedexception-members.md)

[<span data-ttu-id="b30e7-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b30e7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
