---
description: 'Altre informazioni su: classe EsentResource'
title: Classe EsentResource
TOCTitle: EsentResource class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource(v=EXCHG.10)
ms:contentKeyID: 55102575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 607fb59d6f9f89c33e685ed411ae9dc95eaa6818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308042"
---
# <a name="esentresource-class"></a><span data-ttu-id="d3a08-103">Classe EsentResource</span><span class="sxs-lookup"><span data-stu-id="d3a08-103">EsentResource class</span></span>

<span data-ttu-id="d3a08-104">Si tratta della classe di base per tutti gli oggetti risorsa esent.</span><span class="sxs-lookup"><span data-stu-id="d3a08-104">This is the base class for all esent resource objects.</span></span> <span data-ttu-id="d3a08-105">Le sottoclassi di questa classe possono allocare e rilasciare le risorse non gestite.</span><span class="sxs-lookup"><span data-stu-id="d3a08-105">Subclasses of this class can allocate and release unmanaged resources.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d3a08-106">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="d3a08-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="d3a08-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="d3a08-107">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="d3a08-108">Microsoft. ISAM. esent. Interop. EsentResource</span><span class="sxs-lookup"><span data-stu-id="d3a08-108">Microsoft.Isam.Esent.Interop.EsentResource</span></span>  
    [<span data-ttu-id="d3a08-109">Microsoft. ISAM. esent. Interop. Session</span><span class="sxs-lookup"><span data-stu-id="d3a08-109">Microsoft.Isam.Esent.Interop.Session</span></span>](./session-class.md)  
    [<span data-ttu-id="d3a08-110">Microsoft. ISAM. esent. Interop. Table</span><span class="sxs-lookup"><span data-stu-id="d3a08-110">Microsoft.Isam.Esent.Interop.Table</span></span>](./table-class.md)  
    [<span data-ttu-id="d3a08-111">Microsoft. ISAM. esent. Interop. Transaction</span><span class="sxs-lookup"><span data-stu-id="d3a08-111">Microsoft.Isam.Esent.Interop.Transaction</span></span>](./transaction-class.md)  
    [<span data-ttu-id="d3a08-112">Microsoft. ISAM. esent. Interop. Update</span><span class="sxs-lookup"><span data-stu-id="d3a08-112">Microsoft.Isam.Esent.Interop.Update</span></span>](./update-class.md)  
    [<span data-ttu-id="d3a08-113">Microsoft. ISAM. esent. Interop. Windows8. DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="d3a08-113">Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback</span></span>](./durablecommitcallback-class.md)  

<span data-ttu-id="d3a08-114">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d3a08-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d3a08-115">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d3a08-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a08-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3a08-116">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class EsentResource _
    Implements IDisposable
'Usage
Dim instance As EsentResource
```

``` csharp
public abstract class EsentResource : IDisposable
```

## <a name="thread-safety"></a><span data-ttu-id="d3a08-117">Thread safety</span><span class="sxs-lookup"><span data-stu-id="d3a08-117">Thread safety</span></span>

<span data-ttu-id="d3a08-118">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d3a08-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d3a08-119">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d3a08-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3a08-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3a08-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d3a08-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d3a08-121">Reference</span></span>

[<span data-ttu-id="d3a08-122">Membri di EsentResource</span><span class="sxs-lookup"><span data-stu-id="d3a08-122">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="d3a08-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d3a08-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
