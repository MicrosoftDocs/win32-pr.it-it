---
description: 'Altre informazioni su: classe EsentFragmentationException'
title: Classe EsentFragmentationException
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 081198a696be9982e1fd8a7e4f1468e6d63d1c97
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320339"
---
# <a name="esentfragmentationexception-class"></a><span data-ttu-id="27d30-103">Classe EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="27d30-103">EsentFragmentationException class</span></span>

<span data-ttu-id="27d30-104">Classe di base per le eccezioni di frammentazione.</span><span class="sxs-lookup"><span data-stu-id="27d30-104">Base class for Fragmentation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="27d30-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="27d30-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="27d30-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="27d30-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="27d30-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="27d30-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="27d30-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="27d30-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="27d30-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="27d30-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="27d30-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="27d30-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="27d30-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="27d30-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            

<span data-ttu-id="27d30-112">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="27d30-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="27d30-113">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="27d30-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="27d30-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27d30-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="27d30-115">Thread safety</span><span class="sxs-lookup"><span data-stu-id="27d30-115">Thread safety</span></span>

<span data-ttu-id="27d30-116">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="27d30-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="27d30-117">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="27d30-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="27d30-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27d30-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="27d30-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="27d30-119">Reference</span></span>

[<span data-ttu-id="27d30-120">Membri di EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="27d30-120">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="27d30-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="27d30-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="27d30-122">Tipi derivati</span><span class="sxs-lookup"><span data-stu-id="27d30-122">Derived types</span></span>

[<span data-ttu-id="27d30-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="27d30-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="27d30-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="27d30-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="27d30-125">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="27d30-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="27d30-126">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="27d30-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="27d30-127">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="27d30-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="27d30-128">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="27d30-128">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            [<span data-ttu-id="27d30-129">Microsoft. ISAM. esent. Interop. EsentLogSectorSizeMismatchException</span><span class="sxs-lookup"><span data-stu-id="27d30-129">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchException</span></span>](./esentlogsectorsizemismatchexception-class.md)  
            [<span data-ttu-id="27d30-130">Microsoft. ISAM. esent. Interop. EsentLogSequenceEndDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="27d30-130">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException</span></span>](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [<span data-ttu-id="27d30-131">Microsoft. ISAM. esent. Interop. EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="27d30-131">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException</span></span>](./esentlogsequenceendexception-class.md)  
            [<span data-ttu-id="27d30-132">Microsoft. ISAM. esent. Interop. EsentOutOfAutoincrementValuesException</span><span class="sxs-lookup"><span data-stu-id="27d30-132">Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException</span></span>](./esentoutofautoincrementvaluesexception-class.md)  
            [<span data-ttu-id="27d30-133">Microsoft. ISAM. esent. Interop. EsentOutOfDbtimeValuesException</span><span class="sxs-lookup"><span data-stu-id="27d30-133">Microsoft.Isam.Esent.Interop.EsentOutOfDbtimeValuesException</span></span>](./esentoutofdbtimevaluesexception-class.md)  
            [<span data-ttu-id="27d30-134">Microsoft. ISAM. esent. Interop. EsentOutOfLongValueIDsException</span><span class="sxs-lookup"><span data-stu-id="27d30-134">Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException</span></span>](./esentoutoflongvalueidsexception-class.md)  
            [<span data-ttu-id="27d30-135">Microsoft. ISAM. esent. Interop. EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="27d30-135">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>](./esentoutofobjectidsexception-class.md)  
            [<span data-ttu-id="27d30-136">Microsoft. ISAM. esent. Interop. EsentOutOfSequentialIndexValuesException</span><span class="sxs-lookup"><span data-stu-id="27d30-136">Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException</span></span>](./esentoutofsequentialindexvaluesexception-class.md)