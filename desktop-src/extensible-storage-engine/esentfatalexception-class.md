---
description: 'Altre informazioni su: classe EsentFatalException'
title: Classe EsentFatalException
TOCTitle: EsentFatalException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFatalException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFatalException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c38df447f2eb816772713ba930204e75aa38a88c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234442"
---
# <a name="esentfatalexception-class"></a><span data-ttu-id="f9382-103">Classe EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="f9382-103">EsentFatalException class</span></span>

<span data-ttu-id="f9382-104">Classe di base per le eccezioni irreversibili.</span><span class="sxs-lookup"><span data-stu-id="f9382-104">Base class for Fatal exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f9382-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="f9382-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f9382-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f9382-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f9382-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f9382-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f9382-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f9382-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f9382-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f9382-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f9382-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="f9382-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="f9382-111">Microsoft. ISAM. esent. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="f9382-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            

<span data-ttu-id="f9382-112">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f9382-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f9382-113">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f9382-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f9382-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9382-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFatalException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentFatalException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFatalException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="f9382-115">Thread safety</span><span class="sxs-lookup"><span data-stu-id="f9382-115">Thread safety</span></span>

<span data-ttu-id="f9382-116">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f9382-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f9382-117">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f9382-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9382-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9382-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f9382-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f9382-119">Reference</span></span>

[<span data-ttu-id="f9382-120">Membri di EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="f9382-120">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="f9382-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f9382-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="f9382-122">Tipi derivati</span><span class="sxs-lookup"><span data-stu-id="f9382-122">Derived types</span></span>

[<span data-ttu-id="f9382-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="f9382-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f9382-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f9382-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f9382-125">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f9382-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f9382-126">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f9382-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f9382-127">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="f9382-127">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="f9382-128">Microsoft. ISAM. esent. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="f9382-128">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            [<span data-ttu-id="f9382-129">Microsoft. ISAM. esent. Interop. EsentInstanceUnavailableDueToFatalLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="f9382-129">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableDueToFatalLogDiskFullException</span></span>](./esentinstanceunavailableduetofatallogdiskfullexception-class.md)  
            [<span data-ttu-id="f9382-130">Microsoft. ISAM. esent. Interop. EsentInstanceUnavailableException</span><span class="sxs-lookup"><span data-stu-id="f9382-130">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException</span></span>](./esentinstanceunavailableexception-class.md)  
            [<span data-ttu-id="f9382-131">Microsoft. ISAM. esent. Interop. EsentLogDisabledDueToRecoveryFailureException</span><span class="sxs-lookup"><span data-stu-id="f9382-131">Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException</span></span>](./esentlogdisabledduetorecoveryfailureexception-class.md)  
            [<span data-ttu-id="f9382-132">Microsoft. ISAM. esent. Interop. EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="f9382-132">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>](./esentrollbackerrorexception-class.md)  
            [<span data-ttu-id="f9382-133">Microsoft. ISAM. esent. Interop. EsentSectorSizeNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="f9382-133">Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException</span></span>](./esentsectorsizenotsupportedexception-class.md)  
            [<span data-ttu-id="f9382-134">Microsoft. ISAM. esent. Interop. EsentUnloadableOSFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="f9382-134">Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException</span></span>](./esentunloadableosfunctionalityexception-class.md)