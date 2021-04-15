---
description: 'Altre informazioni su: classe EsentBadLogVersionException'
title: Classe EsentBadLogVersionException
TOCTitle: EsentBadLogVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadlogversionexception(v=EXCHG.10)
ms:contentKeyID: 55101079
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e1bdf96dd46fdd16a566c2a6cc5047f4a74fef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485724"
---
# <a name="esentbadlogversionexception-class"></a><span data-ttu-id="1a65a-103">Classe EsentBadLogVersionException</span><span class="sxs-lookup"><span data-stu-id="1a65a-103">EsentBadLogVersionException class</span></span>

<span data-ttu-id="1a65a-104">Classe di base per JET_err. Eccezioni BadLogVersion.</span><span class="sxs-lookup"><span data-stu-id="1a65a-104">Base class for JET_err.BadLogVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1a65a-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="1a65a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1a65a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1a65a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1a65a-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="1a65a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1a65a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="1a65a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1a65a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1a65a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1a65a-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="1a65a-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="1a65a-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="1a65a-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="1a65a-112">Microsoft. ISAM. esent. Interop. EsentBadLogVersionException</span><span class="sxs-lookup"><span data-stu-id="1a65a-112">Microsoft.Isam.Esent.Interop.EsentBadLogVersionException</span></span>  

<span data-ttu-id="1a65a-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a65a-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a65a-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1a65a-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a65a-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a65a-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadLogVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentBadLogVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadLogVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="1a65a-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="1a65a-116">Thread safety</span></span>

<span data-ttu-id="1a65a-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1a65a-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1a65a-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="1a65a-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a65a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a65a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a65a-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1a65a-120">Reference</span></span>

[<span data-ttu-id="1a65a-121">Membri di EsentBadLogVersionException</span><span class="sxs-lookup"><span data-stu-id="1a65a-121">EsentBadLogVersionException members</span></span>](./esentbadlogversionexception-members.md)

[<span data-ttu-id="1a65a-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1a65a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
