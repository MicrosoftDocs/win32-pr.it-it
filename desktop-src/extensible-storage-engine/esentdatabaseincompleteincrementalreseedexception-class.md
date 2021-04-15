---
description: 'Altre informazioni su: classe EsentDatabaseIncompleteIncrementalReseedException'
title: Classe EsentDatabaseIncompleteIncrementalReseedException
TOCTitle: EsentDatabaseIncompleteIncrementalReseedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseincompleteincrementalreseedexception(v=EXCHG.10)
ms:contentKeyID: 55101478
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 65d660c28f9b876e0cb2016631a4a8108a52b6dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526641"
---
# <a name="esentdatabaseincompleteincrementalreseedexception-class"></a><span data-ttu-id="ccf23-103">Classe EsentDatabaseIncompleteIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="ccf23-103">EsentDatabaseIncompleteIncrementalReseedException class</span></span>

<span data-ttu-id="ccf23-104">Classe di base per JET_err. Eccezioni DatabaseIncompleteIncrementalReseed.</span><span class="sxs-lookup"><span data-stu-id="ccf23-104">Base class for JET_err.DatabaseIncompleteIncrementalReseed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ccf23-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="ccf23-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ccf23-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ccf23-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ccf23-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ccf23-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ccf23-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="ccf23-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ccf23-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ccf23-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ccf23-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="ccf23-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="ccf23-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="ccf23-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="ccf23-112">Microsoft. ISAM. esent. Interop. EsentDatabaseIncompleteIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="ccf23-112">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException</span></span>  

<span data-ttu-id="ccf23-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ccf23-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ccf23-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ccf23-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf23-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccf23-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIncompleteIncrementalReseedException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDatabaseIncompleteIncrementalReseedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIncompleteIncrementalReseedException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="ccf23-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="ccf23-116">Thread safety</span></span>

<span data-ttu-id="ccf23-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ccf23-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ccf23-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="ccf23-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ccf23-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccf23-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ccf23-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ccf23-120">Reference</span></span>

[<span data-ttu-id="ccf23-121">Membri di EsentDatabaseIncompleteIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="ccf23-121">EsentDatabaseIncompleteIncrementalReseedException members</span></span>](./esentdatabaseincompleteincrementalreseedexception-members.md)

[<span data-ttu-id="ccf23-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ccf23-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
