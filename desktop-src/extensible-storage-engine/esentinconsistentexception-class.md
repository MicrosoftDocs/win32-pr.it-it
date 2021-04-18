---
description: 'Altre informazioni su: classe EsentInconsistentException'
title: Classe EsentInconsistentException
TOCTitle: EsentInconsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInconsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e62b963e5b0d3f400a860f7742bb76a183b67bd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320422"
---
# <a name="esentinconsistentexception-class"></a><span data-ttu-id="5a110-103">Classe EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="5a110-103">EsentInconsistentException class</span></span>

<span data-ttu-id="5a110-104">Classe di base per le eccezioni incoerenti.</span><span class="sxs-lookup"><span data-stu-id="5a110-104">Base class for Inconsistent exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5a110-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="5a110-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5a110-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5a110-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5a110-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="5a110-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5a110-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="5a110-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5a110-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="5a110-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5a110-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="5a110-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="5a110-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="5a110-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>  
            

<span data-ttu-id="5a110-112">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a110-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a110-113">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a110-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a110-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a110-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentInconsistentException _
    Inherits EsentDataException
'Usage
Dim instance As EsentInconsistentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentInconsistentException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="5a110-115">Thread safety</span><span class="sxs-lookup"><span data-stu-id="5a110-115">Thread safety</span></span>

<span data-ttu-id="5a110-116">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="5a110-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5a110-117">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="5a110-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a110-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a110-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a110-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="5a110-119">Reference</span></span>

[<span data-ttu-id="5a110-120">Membri di EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="5a110-120">EsentInconsistentException members</span></span>](./esentinconsistentexception-members.md)

[<span data-ttu-id="5a110-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5a110-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="5a110-122">Tipi derivati</span><span class="sxs-lookup"><span data-stu-id="5a110-122">Derived types</span></span>

[<span data-ttu-id="5a110-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="5a110-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5a110-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="5a110-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5a110-125">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="5a110-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5a110-126">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="5a110-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5a110-127">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="5a110-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="5a110-128">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="5a110-128">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>  
            [<span data-ttu-id="5a110-129">Microsoft. ISAM. esent. Interop. EsentAttachedDatabaseMismatchException</span><span class="sxs-lookup"><span data-stu-id="5a110-129">Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException</span></span>](./esentattacheddatabasemismatchexception-class.md)  
            [<span data-ttu-id="5a110-130">Microsoft. ISAM. esent. Interop. EsentBadCheckpointSignatureException</span><span class="sxs-lookup"><span data-stu-id="5a110-130">Microsoft.Isam.Esent.Interop.EsentBadCheckpointSignatureException</span></span>](./esentbadcheckpointsignatureexception-class.md)  
            [<span data-ttu-id="5a110-131">Microsoft. ISAM. esent. Interop. EsentBadLogSignatureException</span><span class="sxs-lookup"><span data-stu-id="5a110-131">Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException</span></span>](./esentbadlogsignatureexception-class.md)  
            [<span data-ttu-id="5a110-132">Microsoft. ISAM. esent. Interop. EsentBadLogVersionException</span><span class="sxs-lookup"><span data-stu-id="5a110-132">Microsoft.Isam.Esent.Interop.EsentBadLogVersionException</span></span>](./esentbadlogversionexception-class.md)  
            [<span data-ttu-id="5a110-133">Microsoft. ISAM. esent. Interop. EsentCheckpointFileNotFoundException</span><span class="sxs-lookup"><span data-stu-id="5a110-133">Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException</span></span>](./esentcheckpointfilenotfoundexception-class.md)  
            [<span data-ttu-id="5a110-134">Microsoft. ISAM. esent. Interop. EsentConsistentTimeMismatchException</span><span class="sxs-lookup"><span data-stu-id="5a110-134">Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException</span></span>](./esentconsistenttimemismatchexception-class.md)  
            [<span data-ttu-id="5a110-135">Microsoft. ISAM. esent. Interop. EsentDatabaseDirtyShutdownException</span><span class="sxs-lookup"><span data-stu-id="5a110-135">Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException</span></span>](./esentdatabasedirtyshutdownexception-class.md)  
            [<span data-ttu-id="5a110-136">Microsoft. ISAM. esent. Interop. EsentDatabaseIncompleteIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="5a110-136">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException</span></span>](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [<span data-ttu-id="5a110-137">Microsoft. ISAM. esent. Interop. EsentDatabaseLogSetMismatchException</span><span class="sxs-lookup"><span data-stu-id="5a110-137">Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException</span></span>](./esentdatabaselogsetmismatchexception-class.md)  
            [<span data-ttu-id="5a110-138">Microsoft. ISAM. esent. Interop. EsentDbTimeTooNewException</span><span class="sxs-lookup"><span data-stu-id="5a110-138">Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException</span></span>](./esentdbtimetoonewexception-class.md)  
            [<span data-ttu-id="5a110-139">Microsoft. ISAM. esent. Interop. EsentDbTimeTooOldException</span><span class="sxs-lookup"><span data-stu-id="5a110-139">Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException</span></span>](./esentdbtimetoooldexception-class.md)  
            [<span data-ttu-id="5a110-140">Microsoft. ISAM. esent. Interop. EsentEndingRestoreLogTooLowException</span><span class="sxs-lookup"><span data-stu-id="5a110-140">Microsoft.Isam.Esent.Interop.EsentEndingRestoreLogTooLowException</span></span>](./esentendingrestorelogtoolowexception-class.md)  
            [<span data-ttu-id="5a110-141">Microsoft. ISAM. esent. Interop. EsentExistingLogFileHasBadSignatureException</span><span class="sxs-lookup"><span data-stu-id="5a110-141">Microsoft.Isam.Esent.Interop.EsentExistingLogFileHasBadSignatureException</span></span>](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [<span data-ttu-id="5a110-142">Microsoft. ISAM. esent. Interop. EsentExistingLogFileIsNotContiguousException</span><span class="sxs-lookup"><span data-stu-id="5a110-142">Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException</span></span>](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [<span data-ttu-id="5a110-143">Microsoft. ISAM. esent. Interop. EsentFileInvalidTypeException</span><span class="sxs-lookup"><span data-stu-id="5a110-143">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>](./esentfileinvalidtypeexception-class.md)  
            [<span data-ttu-id="5a110-144">Microsoft. ISAM. esent. Interop. EsentGivenLogFileHasBadSignatureException</span><span class="sxs-lookup"><span data-stu-id="5a110-144">Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException</span></span>](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [<span data-ttu-id="5a110-145">Microsoft. ISAM. esent. Interop. EsentGivenLogFileIsNotContiguousException</span><span class="sxs-lookup"><span data-stu-id="5a110-145">Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException</span></span>](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [<span data-ttu-id="5a110-146">Microsoft. ISAM. esent. Interop. EsentInvalidCreateDbVersionException</span><span class="sxs-lookup"><span data-stu-id="5a110-146">Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException</span></span>](./esentinvalidcreatedbversionexception-class.md)  
            [<span data-ttu-id="5a110-147">Microsoft. ISAM. esent. Interop. EsentInvalidDatabaseVersionException</span><span class="sxs-lookup"><span data-stu-id="5a110-147">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException</span></span>](./esentinvaliddatabaseversionexception-class.md)  
            [<span data-ttu-id="5a110-148">Microsoft. ISAM. esent. Interop. EsentLogGenerationMismatchException</span><span class="sxs-lookup"><span data-stu-id="5a110-148">Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException</span></span>](./esentloggenerationmismatchexception-class.md)  
            [<span data-ttu-id="5a110-149">Microsoft. ISAM. esent. Interop. EsentMissingCurrentLogFilesException</span><span class="sxs-lookup"><span data-stu-id="5a110-149">Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException</span></span>](./esentmissingcurrentlogfilesexception-class.md)  
            [<span data-ttu-id="5a110-150">Microsoft. ISAM. esent. Interop. EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="5a110-150">Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException</span></span>](./esentmissingfiletobackupexception-class.md)  
            [<span data-ttu-id="5a110-151">Microsoft. ISAM. esent. Interop. EsentMissingRestoreLogFilesException</span><span class="sxs-lookup"><span data-stu-id="5a110-151">Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException</span></span>](./esentmissingrestorelogfilesexception-class.md)  
            [<span data-ttu-id="5a110-152">Microsoft. ISAM. esent. Interop. EsentPageSizeMismatchException</span><span class="sxs-lookup"><span data-stu-id="5a110-152">Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException</span></span>](./esentpagesizemismatchexception-class.md)  
            [<span data-ttu-id="5a110-153">Microsoft. ISAM. esent. Interop. EsentRequiredLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="5a110-153">Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException</span></span>](./esentrequiredlogfilesmissingexception-class.md)  
            [<span data-ttu-id="5a110-154">Microsoft. ISAM. esent. Interop. EsentStartingRestoreLogTooHighException</span><span class="sxs-lookup"><span data-stu-id="5a110-154">Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException</span></span>](./esentstartingrestorelogtoohighexception-class.md)