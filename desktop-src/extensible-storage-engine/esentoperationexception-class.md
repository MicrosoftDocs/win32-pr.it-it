---
description: 'Altre informazioni su: classe EsentOperationException'
title: Classe EsentOperationException
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314ae88a674f6bd59b0111d40ff3ca5a9eab8a2f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320326"
---
# <a name="esentoperationexception-class"></a><span data-ttu-id="c5ab9-103">Classe EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-103">EsentOperationException class</span></span>

<span data-ttu-id="c5ab9-104">Classe di base per le eccezioni dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c5ab9-104">Base class for Operation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c5ab9-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="c5ab9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c5ab9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c5ab9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c5ab9-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c5ab9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c5ab9-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c5ab9-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="c5ab9-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>  
          

<span data-ttu-id="c5ab9-111">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c5ab9-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c5ab9-112">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c5ab9-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ab9-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5ab9-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="c5ab9-114">Thread safety</span><span class="sxs-lookup"><span data-stu-id="c5ab9-114">Thread safety</span></span>

<span data-ttu-id="c5ab9-115">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c5ab9-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c5ab9-116">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c5ab9-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5ab9-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5ab9-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5ab9-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c5ab9-118">Reference</span></span>

[<span data-ttu-id="c5ab9-119">Membri di EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-119">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="c5ab9-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c5ab9-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="c5ab9-121">Tipi derivati</span><span class="sxs-lookup"><span data-stu-id="c5ab9-121">Derived types</span></span>

[<span data-ttu-id="c5ab9-122">System.Object</span><span class="sxs-lookup"><span data-stu-id="c5ab9-122">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c5ab9-123">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c5ab9-123">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c5ab9-124">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-124">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c5ab9-125">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-125">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="c5ab9-126">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-126">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>  
          [<span data-ttu-id="c5ab9-127">Microsoft. ISAM. esent. Interop. EsentBackupAbortByServerException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-127">Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException</span></span>](./esentbackupabortbyserverexception-class.md)  
          [<span data-ttu-id="c5ab9-128">Microsoft. ISAM. esent. Interop. EsentCheckpointDepthTooDeepException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-128">Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException</span></span>](./esentcheckpointdepthtoodeepexception-class.md)  
          [<span data-ttu-id="c5ab9-129">Microsoft. ISAM. esent. Interop. EsentClientRequestToStopJetServiceException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-129">Microsoft.Isam.Esent.Interop.EsentClientRequestToStopJetServiceException</span></span>](./esentclientrequesttostopjetserviceexception-class.md)  
          [<span data-ttu-id="c5ab9-130">Microsoft. ISAM. esent. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-130">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
          [<span data-ttu-id="c5ab9-131">Microsoft. ISAM. esent. Interop. EsentInitInProgressException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-131">Microsoft.Isam.Esent.Interop.EsentInitInProgressException</span></span>](./esentinitinprogressexception-class.md)  
          [<span data-ttu-id="c5ab9-132">Microsoft. ISAM. esent. Interop. EsentInternalErrorException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-132">Microsoft.Isam.Esent.Interop.EsentInternalErrorException</span></span>](./esentinternalerrorexception-class.md)  
          [<span data-ttu-id="c5ab9-133">Microsoft. ISAM. esent. Interop. EsentIOException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-133">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
          [<span data-ttu-id="c5ab9-134">Microsoft. ISAM. esent. Interop. EsentNTSystemCallFailedException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-134">Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException</span></span>](./esentntsystemcallfailedexception-class.md)  
          [<span data-ttu-id="c5ab9-135">Microsoft. ISAM. esent. Interop. EsentOSSnapshotTimeOutException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-135">Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException</span></span>](./esentossnapshottimeoutexception-class.md)  
          [<span data-ttu-id="c5ab9-136">Microsoft. ISAM. esent. Interop. EsentRecordNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-136">Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException</span></span>](./esentrecordnotdeletedexception-class.md)  
          [<span data-ttu-id="c5ab9-137">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-137">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
          [<span data-ttu-id="c5ab9-138">Microsoft. ISAM. esent. Interop. EsentTermInProgressException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-138">Microsoft.Isam.Esent.Interop.EsentTermInProgressException</span></span>](./esentterminprogressexception-class.md)  
          [<span data-ttu-id="c5ab9-139">Microsoft. ISAM. esent. Interop. EsentUnicodeLanguageValidationFailureException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-139">Microsoft.Isam.Esent.Interop.EsentUnicodeLanguageValidationFailureException</span></span>](./esentunicodelanguagevalidationfailureexception-class.md)  
          [<span data-ttu-id="c5ab9-140">Microsoft. ISAM. esent. Interop. EsentUnicodeTranslationFailException</span><span class="sxs-lookup"><span data-stu-id="c5ab9-140">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationFailException</span></span>](./esentunicodetranslationfailexception-class.md)