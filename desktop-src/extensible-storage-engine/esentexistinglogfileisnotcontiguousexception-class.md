---
description: 'Altre informazioni su: classe EsentExistingLogFileIsNotContiguousException'
title: Classe EsentExistingLogFileIsNotContiguousException
TOCTitle: EsentExistingLogFileIsNotContiguousException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentexistinglogfileisnotcontiguousexception(v=EXCHG.10)
ms:contentKeyID: 55101598
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bacebf1ffadc1eb76208eb4bffdedaa7aa00e973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308078"
---
# <a name="esentexistinglogfileisnotcontiguousexception-class"></a><span data-ttu-id="0e1ab-103">Classe EsentExistingLogFileIsNotContiguousException</span><span class="sxs-lookup"><span data-stu-id="0e1ab-103">EsentExistingLogFileIsNotContiguousException class</span></span>

<span data-ttu-id="0e1ab-104">Classe di base per JET_err. Eccezioni ExistingLogFileIsNotContiguous.</span><span class="sxs-lookup"><span data-stu-id="0e1ab-104">Base class for JET_err.ExistingLogFileIsNotContiguous exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0e1ab-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="0e1ab-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0e1ab-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0e1ab-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0e1ab-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0e1ab-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0e1ab-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0e1ab-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0e1ab-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0e1ab-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0e1ab-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0e1ab-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="0e1ab-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="0e1ab-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="0e1ab-112">Microsoft. ISAM. esent. Interop. EsentExistingLogFileIsNotContiguousException</span><span class="sxs-lookup"><span data-stu-id="0e1ab-112">Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException</span></span>  

<span data-ttu-id="0e1ab-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0e1ab-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0e1ab-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0e1ab-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0e1ab-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e1ab-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentExistingLogFileIsNotContiguousException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentExistingLogFileIsNotContiguousException
```

``` csharp
[SerializableAttribute]
public sealed class EsentExistingLogFileIsNotContiguousException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="0e1ab-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="0e1ab-116">Thread safety</span></span>

<span data-ttu-id="0e1ab-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0e1ab-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0e1ab-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0e1ab-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e1ab-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e1ab-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e1ab-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0e1ab-120">Reference</span></span>

[<span data-ttu-id="0e1ab-121">Membri di EsentExistingLogFileIsNotContiguousException</span><span class="sxs-lookup"><span data-stu-id="0e1ab-121">EsentExistingLogFileIsNotContiguousException members</span></span>](./esentexistinglogfileisnotcontiguousexception-members.md)

[<span data-ttu-id="0e1ab-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0e1ab-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
