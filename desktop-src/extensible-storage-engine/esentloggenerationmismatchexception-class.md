---
description: 'Altre informazioni su: classe EsentLogGenerationMismatchException'
title: Classe EsentLogGenerationMismatchException
TOCTitle: EsentLogGenerationMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentloggenerationmismatchexception(v=EXCHG.10)
ms:contentKeyID: 55102125
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a878330a00147e1d4f24e7882776ad827d97a50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131815"
---
# <a name="esentloggenerationmismatchexception-class"></a><span data-ttu-id="e7b75-103">Classe EsentLogGenerationMismatchException</span><span class="sxs-lookup"><span data-stu-id="e7b75-103">EsentLogGenerationMismatchException class</span></span>

<span data-ttu-id="e7b75-104">Classe di base per JET_err. Eccezioni LogGenerationMismatch.</span><span class="sxs-lookup"><span data-stu-id="e7b75-104">Base class for JET_err.LogGenerationMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e7b75-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="e7b75-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e7b75-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e7b75-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e7b75-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e7b75-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e7b75-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="e7b75-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e7b75-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e7b75-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e7b75-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="e7b75-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="e7b75-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="e7b75-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="e7b75-112">Microsoft. ISAM. esent. Interop. EsentLogGenerationMismatchException</span><span class="sxs-lookup"><span data-stu-id="e7b75-112">Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException</span></span>  

<span data-ttu-id="e7b75-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e7b75-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e7b75-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e7b75-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b75-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7b75-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogGenerationMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentLogGenerationMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogGenerationMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="e7b75-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="e7b75-116">Thread safety</span></span>

<span data-ttu-id="e7b75-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e7b75-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e7b75-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e7b75-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7b75-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7b75-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e7b75-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e7b75-120">Reference</span></span>

[<span data-ttu-id="e7b75-121">Membri di EsentLogGenerationMismatchException</span><span class="sxs-lookup"><span data-stu-id="e7b75-121">EsentLogGenerationMismatchException members</span></span>](./esentloggenerationmismatchexception-members.md)

[<span data-ttu-id="e7b75-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e7b75-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
