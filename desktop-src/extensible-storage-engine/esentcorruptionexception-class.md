---
description: 'Altre informazioni su: classe EsentCorruptionException'
title: Classe EsentCorruptionException
TOCTitle: EsentCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6914c2bf133a1050e3e3800e5c113c6cac1a11f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234443"
---
# <a name="esentcorruptionexception-class"></a><span data-ttu-id="0b866-103">Classe EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="0b866-103">EsentCorruptionException class</span></span>

<span data-ttu-id="0b866-104">Classe di base per le eccezioni di danneggiamento.</span><span class="sxs-lookup"><span data-stu-id="0b866-104">Base class for Corruption exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0b866-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="0b866-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0b866-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0b866-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0b866-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0b866-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0b866-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0b866-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0b866-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0b866-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0b866-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0b866-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="0b866-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="0b866-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>  
            

<span data-ttu-id="0b866-112">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b866-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b866-113">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b866-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b866-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b866-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentCorruptionException _
    Inherits EsentDataException
'Usage
Dim instance As EsentCorruptionException
```

``` csharp
[SerializableAttribute]
public abstract class EsentCorruptionException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="0b866-115">Thread safety</span><span class="sxs-lookup"><span data-stu-id="0b866-115">Thread safety</span></span>

<span data-ttu-id="0b866-116">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0b866-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0b866-117">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0b866-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b866-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b866-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b866-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0b866-119">Reference</span></span>

[<span data-ttu-id="0b866-120">Membri di EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="0b866-120">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="0b866-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0b866-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="0b866-122">Tipi derivati</span><span class="sxs-lookup"><span data-stu-id="0b866-122">Derived types</span></span>

[<span data-ttu-id="0b866-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="0b866-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0b866-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0b866-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0b866-125">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0b866-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0b866-126">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0b866-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0b866-127">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0b866-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="0b866-128">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="0b866-128">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>  
            [<span data-ttu-id="0b866-129">Microsoft. ISAM. esent. Interop. EsentBadEmptyPageException</span><span class="sxs-lookup"><span data-stu-id="0b866-129">Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException</span></span>](./esentbademptypageexception-class.md)  
            [<span data-ttu-id="0b866-130">Microsoft. ISAM. esent. Interop. EsentBadPageLinkException</span><span class="sxs-lookup"><span data-stu-id="0b866-130">Microsoft.Isam.Esent.Interop.EsentBadPageLinkException</span></span>](./esentbadpagelinkexception-class.md)  
            [<span data-ttu-id="0b866-131">Microsoft. ISAM. esent. Interop. EsentBadParentPageLinkException</span><span class="sxs-lookup"><span data-stu-id="0b866-131">Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException</span></span>](./esentbadparentpagelinkexception-class.md)  
            [<span data-ttu-id="0b866-132">Microsoft. ISAM. esent. Interop. EsentCatalogCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-132">Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException</span></span>](./esentcatalogcorruptedexception-class.md)  
            [<span data-ttu-id="0b866-133">Microsoft. ISAM. esent. Interop. EsentCheckpointCorruptException</span><span class="sxs-lookup"><span data-stu-id="0b866-133">Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException</span></span>](./esentcheckpointcorruptexception-class.md)  
            [<span data-ttu-id="0b866-134">Microsoft. ISAM. esent. Interop. EsentCommittedLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="0b866-134">Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException</span></span>](./esentcommittedlogfilecorruptexception-class.md)  
            [<span data-ttu-id="0b866-135">Microsoft. ISAM. esent. Interop. EsentCommittedLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="0b866-135">Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException</span></span>](./esentcommittedlogfilesmissingexception-class.md)  
            [<span data-ttu-id="0b866-136">Microsoft. ISAM. esent. Interop. EsentDatabaseBufferDependenciesCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-136">Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException</span></span>](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [<span data-ttu-id="0b866-137">Microsoft. ISAM. esent. Interop. EsentDatabaseCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-137">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException</span></span>](./esentdatabasecorruptedexception-class.md)  
            [<span data-ttu-id="0b866-138">Microsoft. ISAM. esent. Interop. EsentDbTimeCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-138">Microsoft.Isam.Esent.Interop.EsentDbTimeCorruptedException</span></span>](./esentdbtimecorruptedexception-class.md)  
            [<span data-ttu-id="0b866-139">Microsoft. ISAM. esent. Interop. EsentDecompressionFailedException</span><span class="sxs-lookup"><span data-stu-id="0b866-139">Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException</span></span>](./esentdecompressionfailedexception-class.md)  
            [<span data-ttu-id="0b866-140">Microsoft. ISAM. esent. Interop. EsentDerivedColumnCorruptionException</span><span class="sxs-lookup"><span data-stu-id="0b866-140">Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException</span></span>](./esentderivedcolumncorruptionexception-class.md)  
            [<span data-ttu-id="0b866-141">Microsoft. ISAM. esent. Interop. EsentDiskReadVerificationFailureException</span><span class="sxs-lookup"><span data-stu-id="0b866-141">Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException</span></span>](./esentdiskreadverificationfailureexception-class.md)  
            [<span data-ttu-id="0b866-142">Microsoft. ISAM. esent. Interop. EsentFileIOBeyondEOFException</span><span class="sxs-lookup"><span data-stu-id="0b866-142">Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException</span></span>](./esentfileiobeyondeofexception-class.md)  
            [<span data-ttu-id="0b866-143">Microsoft. ISAM. esent. Interop. EsentFileSystemCorruptionException</span><span class="sxs-lookup"><span data-stu-id="0b866-143">Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException</span></span>](./esentfilesystemcorruptionexception-class.md)  
            [<span data-ttu-id="0b866-144">Microsoft. ISAM. esent. Interop. EsentIndexBuildCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-144">Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException</span></span>](./esentindexbuildcorruptedexception-class.md)  
            [<span data-ttu-id="0b866-145">Microsoft. ISAM. esent. Interop. EsentInvalidLogSequenceException</span><span class="sxs-lookup"><span data-stu-id="0b866-145">Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException</span></span>](./esentinvalidlogsequenceexception-class.md)  
            [<span data-ttu-id="0b866-146">Microsoft. ISAM. esent. Interop. EsentLogCorruptDuringHardRecoveryException</span><span class="sxs-lookup"><span data-stu-id="0b866-146">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException</span></span>](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [<span data-ttu-id="0b866-147">Microsoft. ISAM. esent. Interop. EsentLogCorruptDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="0b866-147">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException</span></span>](./esentlogcorruptduringhardrestoreexception-class.md)  
            [<span data-ttu-id="0b866-148">Microsoft. ISAM. esent. Interop. EsentLogCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-148">Microsoft.Isam.Esent.Interop.EsentLogCorruptedException</span></span>](./esentlogcorruptedexception-class.md)  
            [<span data-ttu-id="0b866-149">Microsoft. ISAM. esent. Interop. EsentLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="0b866-149">Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException</span></span>](./esentlogfilecorruptexception-class.md)  
            [<span data-ttu-id="0b866-150">Microsoft. ISAM. esent. Interop. EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="0b866-150">Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException</span></span>](./esentlogreadverifyfailureexception-class.md)  
            [<span data-ttu-id="0b866-151">Microsoft. ISAM. esent. Interop. EsentLogTornWriteDuringHardRecoveryException</span><span class="sxs-lookup"><span data-stu-id="0b866-151">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException</span></span>](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [<span data-ttu-id="0b866-152">Microsoft. ISAM. esent. Interop. EsentLogTornWriteDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="0b866-152">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException</span></span>](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [<span data-ttu-id="0b866-153">Microsoft. ISAM. esent. Interop. EsentLVCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-153">Microsoft.Isam.Esent.Interop.EsentLVCorruptedException</span></span>](./esentlvcorruptedexception-class.md)  
            [<span data-ttu-id="0b866-154">Microsoft. ISAM. esent. Interop. EsentMissingLogFileException</span><span class="sxs-lookup"><span data-stu-id="0b866-154">Microsoft.Isam.Esent.Interop.EsentMissingLogFileException</span></span>](./esentmissinglogfileexception-class.md)  
            [<span data-ttu-id="0b866-155">Microsoft. ISAM. esent. Interop. EsentMissingPreviousLogFileException</span><span class="sxs-lookup"><span data-stu-id="0b866-155">Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException</span></span>](./esentmissingpreviouslogfileexception-class.md)  
            [<span data-ttu-id="0b866-156">Microsoft. ISAM. esent. Interop. EsentPageNotInitializedException</span><span class="sxs-lookup"><span data-stu-id="0b866-156">Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException</span></span>](./esentpagenotinitializedexception-class.md)  
            [<span data-ttu-id="0b866-157">Microsoft. ISAM. esent. Interop. EsentPrimaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-157">Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException</span></span>](./esentprimaryindexcorruptedexception-class.md)  
            [<span data-ttu-id="0b866-158">Microsoft. ISAM. esent. Interop. EsentReadLostFlushVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="0b866-158">Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException</span></span>](./esentreadlostflushverifyfailureexception-class.md)  
            [<span data-ttu-id="0b866-159">Microsoft. ISAM. esent. Interop. EsentReadPgnoVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="0b866-159">Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException</span></span>](./esentreadpgnoverifyfailureexception-class.md)  
            [<span data-ttu-id="0b866-160">Microsoft. ISAM. esent. Interop. EsentReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="0b866-160">Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException</span></span>](./esentreadverifyfailureexception-class.md)  
            [<span data-ttu-id="0b866-161">Microsoft. ISAM. esent. Interop. EsentRecordFormatConversionFailedException</span><span class="sxs-lookup"><span data-stu-id="0b866-161">Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException</span></span>](./esentrecordformatconversionfailedexception-class.md)  
            [<span data-ttu-id="0b866-162">Microsoft. ISAM. esent. Interop. EsentRecoveryVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="0b866-162">Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException</span></span>](./esentrecoveryverifyfailureexception-class.md)  
            [<span data-ttu-id="0b866-163">Microsoft. ISAM. esent. Interop. EsentRedoAbruptEndedException</span><span class="sxs-lookup"><span data-stu-id="0b866-163">Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException</span></span>](./esentredoabruptendedexception-class.md)  
            [<span data-ttu-id="0b866-164">Microsoft. ISAM. esent. Interop. EsentSecondaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-164">Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException</span></span>](./esentsecondaryindexcorruptedexception-class.md)  
            [<span data-ttu-id="0b866-165">Microsoft. ISAM. esent. Interop. EsentSPAvailExtCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-165">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException</span></span>](./esentspavailextcorruptedexception-class.md)  
            [<span data-ttu-id="0b866-166">Microsoft. ISAM. esent. Interop. EsentSPOwnExtCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0b866-166">Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException</span></span>](./esentspownextcorruptedexception-class.md)