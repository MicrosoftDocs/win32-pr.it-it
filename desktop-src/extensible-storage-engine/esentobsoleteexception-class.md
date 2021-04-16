---
description: 'Altre informazioni su: classe EsentObsoleteException'
title: Classe EsentObsoleteException
TOCTitle: EsentObsoleteException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObsoleteException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9d9597c3022d18ba0c6d476710f1c43430babc2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530438"
---
# <a name="esentobsoleteexception-class"></a><span data-ttu-id="d73d2-103">Classe EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="d73d2-103">EsentObsoleteException class</span></span>

<span data-ttu-id="d73d2-104">Classe base per le eccezioni obsolete.</span><span class="sxs-lookup"><span data-stu-id="d73d2-104">Base class for Obsolete exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d73d2-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="d73d2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d73d2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d73d2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d73d2-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="d73d2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d73d2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d73d2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d73d2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d73d2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d73d2-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d73d2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="d73d2-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="d73d2-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            

<span data-ttu-id="d73d2-112">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d73d2-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d73d2-113">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d73d2-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d73d2-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d73d2-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentObsoleteException _
    Inherits EsentApiException
'Usage
Dim instance As EsentObsoleteException
```

``` csharp
[SerializableAttribute]
public abstract class EsentObsoleteException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="d73d2-115">Thread safety</span><span class="sxs-lookup"><span data-stu-id="d73d2-115">Thread safety</span></span>

<span data-ttu-id="d73d2-116">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d73d2-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d73d2-117">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d73d2-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d73d2-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d73d2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d73d2-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d73d2-119">Reference</span></span>

[<span data-ttu-id="d73d2-120">Membri di EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="d73d2-120">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="d73d2-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d73d2-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="d73d2-122">Tipi derivati</span><span class="sxs-lookup"><span data-stu-id="d73d2-122">Derived types</span></span>

[<span data-ttu-id="d73d2-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="d73d2-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d73d2-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="d73d2-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d73d2-125">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d73d2-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d73d2-126">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d73d2-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d73d2-127">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d73d2-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="d73d2-128">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="d73d2-128">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            [<span data-ttu-id="d73d2-129">Microsoft. ISAM. esent. Interop. EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-129">Microsoft.Isam.Esent.Interop.EsentAccessDeniedException</span></span>](./esentaccessdeniedexception-class.md)  
            [<span data-ttu-id="d73d2-130">Microsoft. ISAM. esent. Interop. EsentBadBackupDatabaseSizeException</span><span class="sxs-lookup"><span data-stu-id="d73d2-130">Microsoft.Isam.Esent.Interop.EsentBadBackupDatabaseSizeException</span></span>](./esentbadbackupdatabasesizeexception-class.md)  
            [<span data-ttu-id="d73d2-131">Microsoft. ISAM. esent. Interop. EsentBadBookmarkException</span><span class="sxs-lookup"><span data-stu-id="d73d2-131">Microsoft.Isam.Esent.Interop.EsentBadBookmarkException</span></span>](./esentbadbookmarkexception-class.md)  
            [<span data-ttu-id="d73d2-132">Microsoft. ISAM. esent. Interop. EsentBadDbSignatureException</span><span class="sxs-lookup"><span data-stu-id="d73d2-132">Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException</span></span>](./esentbaddbsignatureexception-class.md)  
            [<span data-ttu-id="d73d2-133">Microsoft. ISAM. esent. Interop. EsentBadPatchPageException</span><span class="sxs-lookup"><span data-stu-id="d73d2-133">Microsoft.Isam.Esent.Interop.EsentBadPatchPageException</span></span>](./esentbadpatchpageexception-class.md)  
            [<span data-ttu-id="d73d2-134">Microsoft. ISAM. esent. Interop. EsentBadSLVSignatureException</span><span class="sxs-lookup"><span data-stu-id="d73d2-134">Microsoft.Isam.Esent.Interop.EsentBadSLVSignatureException</span></span>](./esentbadslvsignatureexception-class.md)  
            [<span data-ttu-id="d73d2-135">Microsoft. ISAM. esent. Interop. EsentCannotAddFixedVarColumnToDerivedTableException</span><span class="sxs-lookup"><span data-stu-id="d73d2-135">Microsoft.Isam.Esent.Interop.EsentCannotAddFixedVarColumnToDerivedTableException</span></span>](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [<span data-ttu-id="d73d2-136">Microsoft. ISAM. esent. Interop. EsentCannotNestDistributedTransactionsException</span><span class="sxs-lookup"><span data-stu-id="d73d2-136">Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException</span></span>](./esentcannotnestdistributedtransactionsexception-class.md)  
            [<span data-ttu-id="d73d2-137">Microsoft. ISAM. esent. Interop. EsentColumnIndexedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-137">Microsoft.Isam.Esent.Interop.EsentColumnIndexedException</span></span>](./esentcolumnindexedexception-class.md)  
            [<span data-ttu-id="d73d2-138">Microsoft. ISAM. esent. Interop. EsentColumnInRelationshipException</span><span class="sxs-lookup"><span data-stu-id="d73d2-138">Microsoft.Isam.Esent.Interop.EsentColumnInRelationshipException</span></span>](./esentcolumninrelationshipexception-class.md)  
            [<span data-ttu-id="d73d2-139">Microsoft. ISAM. esent. Interop. EsentColumnLongException</span><span class="sxs-lookup"><span data-stu-id="d73d2-139">Microsoft.Isam.Esent.Interop.EsentColumnLongException</span></span>](./esentcolumnlongexception-class.md)  
            [<span data-ttu-id="d73d2-140">Microsoft. ISAM. esent. Interop. EsentContainerNotEmptyException</span><span class="sxs-lookup"><span data-stu-id="d73d2-140">Microsoft.Isam.Esent.Interop.EsentContainerNotEmptyException</span></span>](./esentcontainernotemptyexception-class.md)  
            [<span data-ttu-id="d73d2-141">Microsoft. ISAM. esent. Interop. EsentCurrencyStackOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="d73d2-141">Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException</span></span>](./esentcurrencystackoutofmemoryexception-class.md)  
            [<span data-ttu-id="d73d2-142">Microsoft. ISAM. esent. Interop. EsentDatabase200FormatException</span><span class="sxs-lookup"><span data-stu-id="d73d2-142">Microsoft.Isam.Esent.Interop.EsentDatabase200FormatException</span></span>](./esentdatabase200formatexception-class.md)  
            [<span data-ttu-id="d73d2-143">Microsoft. ISAM. esent. Interop. EsentDatabase400FormatException</span><span class="sxs-lookup"><span data-stu-id="d73d2-143">Microsoft.Isam.Esent.Interop.EsentDatabase400FormatException</span></span>](./esentdatabase400formatexception-class.md)  
            [<span data-ttu-id="d73d2-144">Microsoft. ISAM. esent. Interop. EsentDatabase500FormatException</span><span class="sxs-lookup"><span data-stu-id="d73d2-144">Microsoft.Isam.Esent.Interop.EsentDatabase500FormatException</span></span>](./esentdatabase500formatexception-class.md)  
            [<span data-ttu-id="d73d2-145">Microsoft. ISAM. esent. Interop. EsentDatabaseIdInUseException</span><span class="sxs-lookup"><span data-stu-id="d73d2-145">Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException</span></span>](./esentdatabaseidinuseexception-class.md)  
            [<span data-ttu-id="d73d2-146">Microsoft. ISAM. esent. Interop. EsentDatabasePatchFileMismatchException</span><span class="sxs-lookup"><span data-stu-id="d73d2-146">Microsoft.Isam.Esent.Interop.EsentDatabasePatchFileMismatchException</span></span>](./esentdatabasepatchfilemismatchexception-class.md)  
            [<span data-ttu-id="d73d2-147">Microsoft. ISAM. esent. Interop. EsentDatabasesNotFromSameSnapshotException</span><span class="sxs-lookup"><span data-stu-id="d73d2-147">Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException</span></span>](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [<span data-ttu-id="d73d2-148">Microsoft. ISAM. esent. Interop. EsentDatabaseStreamingFileMismatchException</span><span class="sxs-lookup"><span data-stu-id="d73d2-148">Microsoft.Isam.Esent.Interop.EsentDatabaseStreamingFileMismatchException</span></span>](./esentdatabasestreamingfilemismatchexception-class.md)  
            [<span data-ttu-id="d73d2-149">Microsoft. ISAM. esent. Interop. EsentDatabaseUnavailableException</span><span class="sxs-lookup"><span data-stu-id="d73d2-149">Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException</span></span>](./esentdatabaseunavailableexception-class.md)  
            [<span data-ttu-id="d73d2-150">Microsoft. ISAM. esent. Interop. EsentDataHasChangedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-150">Microsoft.Isam.Esent.Interop.EsentDataHasChangedException</span></span>](./esentdatahaschangedexception-class.md)  
            [<span data-ttu-id="d73d2-151">Microsoft. ISAM. esent. Interop. EsentDistributedTransactionAlreadyPreparedToCommitException</span><span class="sxs-lookup"><span data-stu-id="d73d2-151">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException</span></span>](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [<span data-ttu-id="d73d2-152">Microsoft. ISAM. esent. Interop. EsentDistributedTransactionNotYetPreparedToCommitException</span><span class="sxs-lookup"><span data-stu-id="d73d2-152">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException</span></span>](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [<span data-ttu-id="d73d2-153">Microsoft. ISAM. esent. Interop. EsentDTCCallbackUnexpectedErrorException</span><span class="sxs-lookup"><span data-stu-id="d73d2-153">Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException</span></span>](./esentdtccallbackunexpectederrorexception-class.md)  
            [<span data-ttu-id="d73d2-154">Microsoft. ISAM. esent. Interop. EsentDTCMissingCallbackException</span><span class="sxs-lookup"><span data-stu-id="d73d2-154">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException</span></span>](./esentdtcmissingcallbackexception-class.md)  
            [<span data-ttu-id="d73d2-155">Microsoft. ISAM. esent. Interop. EsentDTCMissingCallbackOnRecoveryException</span><span class="sxs-lookup"><span data-stu-id="d73d2-155">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackOnRecoveryException</span></span>](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [<span data-ttu-id="d73d2-156">Microsoft. ISAM. esent. Interop. EsentFileCloseException</span><span class="sxs-lookup"><span data-stu-id="d73d2-156">Microsoft.Isam.Esent.Interop.EsentFileCloseException</span></span>](./esentfilecloseexception-class.md)  
            [<span data-ttu-id="d73d2-157">Microsoft. ISAM. esent. Interop. EsentFileIOAbortException</span><span class="sxs-lookup"><span data-stu-id="d73d2-157">Microsoft.Isam.Esent.Interop.EsentFileIOAbortException</span></span>](./esentfileioabortexception-class.md)  
            [<span data-ttu-id="d73d2-158">Microsoft. ISAM. esent. Interop. EsentFileIOFailException</span><span class="sxs-lookup"><span data-stu-id="d73d2-158">Microsoft.Isam.Esent.Interop.EsentFileIOFailException</span></span>](./esentfileiofailexception-class.md)  
            [<span data-ttu-id="d73d2-159">Microsoft. ISAM. esent. Interop. EsentFileIORetryException</span><span class="sxs-lookup"><span data-stu-id="d73d2-159">Microsoft.Isam.Esent.Interop.EsentFileIORetryException</span></span>](./esentfileioretryexception-class.md)  
            [<span data-ttu-id="d73d2-160">Microsoft. ISAM. esent. Interop. EsentFileIOSparseException</span><span class="sxs-lookup"><span data-stu-id="d73d2-160">Microsoft.Isam.Esent.Interop.EsentFileIOSparseException</span></span>](./esentfileiosparseexception-class.md)  
            [<span data-ttu-id="d73d2-161">Microsoft. ISAM. esent. Interop. EsentIndexCantBuildException</span><span class="sxs-lookup"><span data-stu-id="d73d2-161">Microsoft.Isam.Esent.Interop.EsentIndexCantBuildException</span></span>](./esentindexcantbuildexception-class.md)  
            [<span data-ttu-id="d73d2-162">Microsoft. ISAM. esent. Interop. EsentIndexTuplesTooManyColumnsException</span><span class="sxs-lookup"><span data-stu-id="d73d2-162">Microsoft.Isam.Esent.Interop.EsentIndexTuplesTooManyColumnsException</span></span>](./esentindextuplestoomanycolumnsexception-class.md)  
            [<span data-ttu-id="d73d2-163">Microsoft. ISAM. esent. Interop. EsentInvalidCountryException</span><span class="sxs-lookup"><span data-stu-id="d73d2-163">Microsoft.Isam.Esent.Interop.EsentInvalidCountryException</span></span>](./esentinvalidcountryexception-class.md)  
            [<span data-ttu-id="d73d2-164">Microsoft. ISAM. esent. Interop. EsentInvalidFilenameException</span><span class="sxs-lookup"><span data-stu-id="d73d2-164">Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException</span></span>](./esentinvalidfilenameexception-class.md)  
            [<span data-ttu-id="d73d2-165">Microsoft. ISAM. esent. Interop. EsentInvalidLogDirectoryException</span><span class="sxs-lookup"><span data-stu-id="d73d2-165">Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException</span></span>](./esentinvalidlogdirectoryexception-class.md)  
            [<span data-ttu-id="d73d2-166">Microsoft. ISAM. esent. Interop. EsentInvalidLoggedOperationException</span><span class="sxs-lookup"><span data-stu-id="d73d2-166">Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException</span></span>](./esentinvalidloggedoperationexception-class.md)  
            [<span data-ttu-id="d73d2-167">Microsoft. ISAM. esent. Interop. EsentInvalidObjectException</span><span class="sxs-lookup"><span data-stu-id="d73d2-167">Microsoft.Isam.Esent.Interop.EsentInvalidObjectException</span></span>](./esentinvalidobjectexception-class.md)  
            [<span data-ttu-id="d73d2-168">Microsoft. ISAM. esent. Interop. EsentInvalidOnSortException</span><span class="sxs-lookup"><span data-stu-id="d73d2-168">Microsoft.Isam.Esent.Interop.EsentInvalidOnSortException</span></span>](./esentinvalidonsortexception-class.md)  
            [<span data-ttu-id="d73d2-169">Microsoft. ISAM. esent. Interop. EsentInvalidSystemPathException</span><span class="sxs-lookup"><span data-stu-id="d73d2-169">Microsoft.Isam.Esent.Interop.EsentInvalidSystemPathException</span></span>](./esentinvalidsystempathexception-class.md)  
            [<span data-ttu-id="d73d2-170">Microsoft. ISAM. esent. Interop. EsentKeyBoundaryException</span><span class="sxs-lookup"><span data-stu-id="d73d2-170">Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException</span></span>](./esentkeyboundaryexception-class.md)  
            [<span data-ttu-id="d73d2-171">Microsoft. ISAM. esent. Interop. EsentKeyTooBigException</span><span class="sxs-lookup"><span data-stu-id="d73d2-171">Microsoft.Isam.Esent.Interop.EsentKeyTooBigException</span></span>](./esentkeytoobigexception-class.md)  
            [<span data-ttu-id="d73d2-172">Microsoft. ISAM. esent. Interop. EsentLanguageNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-172">Microsoft.Isam.Esent.Interop.EsentLanguageNotSupportedException</span></span>](./esentlanguagenotsupportedexception-class.md)  
            [<span data-ttu-id="d73d2-173">Microsoft. ISAM. esent. Interop. EsentLinkNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-173">Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException</span></span>](./esentlinknotsupportedexception-class.md)  
            [<span data-ttu-id="d73d2-174">Microsoft. ISAM. esent. Interop. EsentLogBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="d73d2-174">Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException</span></span>](./esentlogbuffertoosmallexception-class.md)  
            [<span data-ttu-id="d73d2-175">Microsoft. ISAM. esent. Interop. EsentMissingPatchPageException</span><span class="sxs-lookup"><span data-stu-id="d73d2-175">Microsoft.Isam.Esent.Interop.EsentMissingPatchPageException</span></span>](./esentmissingpatchpageexception-class.md)  
            [<span data-ttu-id="d73d2-176">Microsoft. ISAM. esent. Interop. EsentMustCommitDistributedTransactionToLevel0Exception</span><span class="sxs-lookup"><span data-stu-id="d73d2-176">Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception</span></span>](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [<span data-ttu-id="d73d2-177">Microsoft. ISAM. esent. Interop. EsentMustDisableLoggingForDbUpgradeException</span><span class="sxs-lookup"><span data-stu-id="d73d2-177">Microsoft.Isam.Esent.Interop.EsentMustDisableLoggingForDbUpgradeException</span></span>](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [<span data-ttu-id="d73d2-178">Microsoft. ISAM. esent. Interop. EsentNotInDistributedTransactionException</span><span class="sxs-lookup"><span data-stu-id="d73d2-178">Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException</span></span>](./esentnotindistributedtransactionexception-class.md)  
            [<span data-ttu-id="d73d2-179">Microsoft. ISAM. esent. Interop. EsentObjectDuplicateException</span><span class="sxs-lookup"><span data-stu-id="d73d2-179">Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException</span></span>](./esentobjectduplicateexception-class.md)  
            [<span data-ttu-id="d73d2-180">Microsoft. ISAM. esent. Interop. EsentPageBoundaryException</span><span class="sxs-lookup"><span data-stu-id="d73d2-180">Microsoft.Isam.Esent.Interop.EsentPageBoundaryException</span></span>](./esentpageboundaryexception-class.md)  
            [<span data-ttu-id="d73d2-181">Microsoft. ISAM. esent. Interop. EsentPatchFileMissingException</span><span class="sxs-lookup"><span data-stu-id="d73d2-181">Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException</span></span>](./esentpatchfilemissingexception-class.md)  
            [<span data-ttu-id="d73d2-182">Microsoft. ISAM. esent. Interop. EsentRfsFailureException</span><span class="sxs-lookup"><span data-stu-id="d73d2-182">Microsoft.Isam.Esent.Interop.EsentRfsFailureException</span></span>](./esentrfsfailureexception-class.md)  
            [<span data-ttu-id="d73d2-183">Microsoft. ISAM. esent. Interop. EsentRfsNotArmedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-183">Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException</span></span>](./esentrfsnotarmedexception-class.md)  
            [<span data-ttu-id="d73d2-184">Microsoft. ISAM. esent. Interop. EsentRollbackRequiredException</span><span class="sxs-lookup"><span data-stu-id="d73d2-184">Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException</span></span>](./esentrollbackrequiredexception-class.md)  
            [<span data-ttu-id="d73d2-185">Microsoft. ISAM. esent. Interop. EsentSLVBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="d73d2-185">Microsoft.Isam.Esent.Interop.EsentSLVBufferTooSmallException</span></span>](./esentslvbuffertoosmallexception-class.md)  
            [<span data-ttu-id="d73d2-186">Microsoft. ISAM. esent. Interop. EsentSLVColumnCannotDeleteException</span><span class="sxs-lookup"><span data-stu-id="d73d2-186">Microsoft.Isam.Esent.Interop.EsentSLVColumnCannotDeleteException</span></span>](./esentslvcolumncannotdeleteexception-class.md)  
            [<span data-ttu-id="d73d2-187">Microsoft. ISAM. esent. Interop. EsentSLVColumnDefaultValueNotAllowedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-187">Microsoft.Isam.Esent.Interop.EsentSLVColumnDefaultValueNotAllowedException</span></span>](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [<span data-ttu-id="d73d2-188">Microsoft. ISAM. esent. Interop. EsentSLVCorruptedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-188">Microsoft.Isam.Esent.Interop.EsentSLVCorruptedException</span></span>](./esentslvcorruptedexception-class.md)  
            [<span data-ttu-id="d73d2-189">Microsoft. ISAM. esent. Interop. EsentSLVDatabaseMissingException</span><span class="sxs-lookup"><span data-stu-id="d73d2-189">Microsoft.Isam.Esent.Interop.EsentSLVDatabaseMissingException</span></span>](./esentslvdatabasemissingexception-class.md)  
            [<span data-ttu-id="d73d2-190">Microsoft. ISAM. esent. Interop. EsentSLVEAListCorruptException</span><span class="sxs-lookup"><span data-stu-id="d73d2-190">Microsoft.Isam.Esent.Interop.EsentSLVEAListCorruptException</span></span>](./esentslvealistcorruptexception-class.md)  
            [<span data-ttu-id="d73d2-191">Microsoft. ISAM. esent. Interop. EsentSLVEAListTooBigException</span><span class="sxs-lookup"><span data-stu-id="d73d2-191">Microsoft.Isam.Esent.Interop.EsentSLVEAListTooBigException</span></span>](./esentslvealisttoobigexception-class.md)  
            [<span data-ttu-id="d73d2-192">Microsoft. ISAM. esent. Interop. EsentSLVEAListZeroAllocationException</span><span class="sxs-lookup"><span data-stu-id="d73d2-192">Microsoft.Isam.Esent.Interop.EsentSLVEAListZeroAllocationException</span></span>](./esentslvealistzeroallocationexception-class.md)  
            [<span data-ttu-id="d73d2-193">Microsoft. ISAM. esent. Interop. EsentSLVFileAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-193">Microsoft.Isam.Esent.Interop.EsentSLVFileAccessDeniedException</span></span>](./esentslvfileaccessdeniedexception-class.md)  
            [<span data-ttu-id="d73d2-194">Microsoft. ISAM. esent. Interop. EsentSLVFileInUseException</span><span class="sxs-lookup"><span data-stu-id="d73d2-194">Microsoft.Isam.Esent.Interop.EsentSLVFileInUseException</span></span>](./esentslvfileinuseexception-class.md)  
            [<span data-ttu-id="d73d2-195">Microsoft. ISAM. esent. Interop. EsentSLVFileInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="d73d2-195">Microsoft.Isam.Esent.Interop.EsentSLVFileInvalidPathException</span></span>](./esentslvfileinvalidpathexception-class.md)  
            [<span data-ttu-id="d73d2-196">Microsoft. ISAM. esent. Interop. EsentSLVFileIOException</span><span class="sxs-lookup"><span data-stu-id="d73d2-196">Microsoft.Isam.Esent.Interop.EsentSLVFileIOException</span></span>](./esentslvfileioexception-class.md)  
            [<span data-ttu-id="d73d2-197">Microsoft. ISAM. esent. Interop. EsentSLVFileNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d73d2-197">Microsoft.Isam.Esent.Interop.EsentSLVFileNotFoundException</span></span>](./esentslvfilenotfoundexception-class.md)  
            [<span data-ttu-id="d73d2-198">Microsoft. ISAM. esent. Interop. EsentSLVFileStaleException</span><span class="sxs-lookup"><span data-stu-id="d73d2-198">Microsoft.Isam.Esent.Interop.EsentSLVFileStaleException</span></span>](./esentslvfilestaleexception-class.md)  
            [<span data-ttu-id="d73d2-199">Microsoft. ISAM. esent. Interop. EsentSLVFileUnknownException</span><span class="sxs-lookup"><span data-stu-id="d73d2-199">Microsoft.Isam.Esent.Interop.EsentSLVFileUnknownException</span></span>](./esentslvfileunknownexception-class.md)  
            [<span data-ttu-id="d73d2-200">Microsoft. ISAM. esent. Interop. EsentSLVHeaderBadChecksumException</span><span class="sxs-lookup"><span data-stu-id="d73d2-200">Microsoft.Isam.Esent.Interop.EsentSLVHeaderBadChecksumException</span></span>](./esentslvheaderbadchecksumexception-class.md)  
            [<span data-ttu-id="d73d2-201">Microsoft. ISAM. esent. Interop. EsentSLVHeaderCorruptedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-201">Microsoft.Isam.Esent.Interop.EsentSLVHeaderCorruptedException</span></span>](./esentslvheadercorruptedexception-class.md)  
            [<span data-ttu-id="d73d2-202">Microsoft. ISAM. esent. Interop. EsentSLVInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="d73d2-202">Microsoft.Isam.Esent.Interop.EsentSLVInvalidPathException</span></span>](./esentslvinvalidpathexception-class.md)  
            [<span data-ttu-id="d73d2-203">Microsoft. ISAM. esent. Interop. EsentSLVOwnerMapAlreadyExistsException</span><span class="sxs-lookup"><span data-stu-id="d73d2-203">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapAlreadyExistsException</span></span>](./esentslvownermapalreadyexistsexception-class.md)  
            [<span data-ttu-id="d73d2-204">Microsoft. ISAM. esent. Interop. EsentSLVOwnerMapCorruptedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-204">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapCorruptedException</span></span>](./esentslvownermapcorruptedexception-class.md)  
            [<span data-ttu-id="d73d2-205">Microsoft. ISAM. esent. Interop. EsentSLVOwnerMapPageNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d73d2-205">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapPageNotFoundException</span></span>](./esentslvownermappagenotfoundexception-class.md)  
            [<span data-ttu-id="d73d2-206">Microsoft. ISAM. esent. Interop. EsentSLVPagesNotCommittedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-206">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotCommittedException</span></span>](./esentslvpagesnotcommittedexception-class.md)  
            [<span data-ttu-id="d73d2-207">Microsoft. ISAM. esent. Interop. EsentSLVPagesNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-207">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotDeletedException</span></span>](./esentslvpagesnotdeletedexception-class.md)  
            [<span data-ttu-id="d73d2-208">Microsoft. ISAM. esent. Interop. EsentSLVPagesNotFreeException</span><span class="sxs-lookup"><span data-stu-id="d73d2-208">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotFreeException</span></span>](./esentslvpagesnotfreeexception-class.md)  
            [<span data-ttu-id="d73d2-209">Microsoft. ISAM. esent. Interop. EsentSLVPagesNotReservedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-209">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotReservedException</span></span>](./esentslvpagesnotreservedexception-class.md)  
            [<span data-ttu-id="d73d2-210">Microsoft. ISAM. esent. Interop. EsentSLVProviderNotLoadedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-210">Microsoft.Isam.Esent.Interop.EsentSLVProviderNotLoadedException</span></span>](./esentslvprovidernotloadedexception-class.md)  
            [<span data-ttu-id="d73d2-211">Microsoft. ISAM. esent. Interop. EsentSLVProviderVersionMismatchException</span><span class="sxs-lookup"><span data-stu-id="d73d2-211">Microsoft.Isam.Esent.Interop.EsentSLVProviderVersionMismatchException</span></span>](./esentslvproviderversionmismatchexception-class.md)  
            [<span data-ttu-id="d73d2-212">Microsoft. ISAM. esent. Interop. EsentSLVReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="d73d2-212">Microsoft.Isam.Esent.Interop.EsentSLVReadVerifyFailureException</span></span>](./esentslvreadverifyfailureexception-class.md)  
            [<span data-ttu-id="d73d2-213">Microsoft. ISAM. esent. Interop. EsentSLVRootNotSpecifiedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-213">Microsoft.Isam.Esent.Interop.EsentSLVRootNotSpecifiedException</span></span>](./esentslvrootnotspecifiedexception-class.md)  
            [<span data-ttu-id="d73d2-214">Microsoft. ISAM. esent. Interop. EsentSLVRootPathInvalidException</span><span class="sxs-lookup"><span data-stu-id="d73d2-214">Microsoft.Isam.Esent.Interop.EsentSLVRootPathInvalidException</span></span>](./esentslvrootpathinvalidexception-class.md)  
            [<span data-ttu-id="d73d2-215">Microsoft. ISAM. esent. Interop. EsentSLVRootStillOpenException</span><span class="sxs-lookup"><span data-stu-id="d73d2-215">Microsoft.Isam.Esent.Interop.EsentSLVRootStillOpenException</span></span>](./esentslvrootstillopenexception-class.md)  
            [<span data-ttu-id="d73d2-216">Microsoft. ISAM. esent. Interop. EsentSLVSpaceCorruptedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-216">Microsoft.Isam.Esent.Interop.EsentSLVSpaceCorruptedException</span></span>](./esentslvspacecorruptedexception-class.md)  
            [<span data-ttu-id="d73d2-217">Microsoft. ISAM. esent. Interop. EsentSLVSpaceWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="d73d2-217">Microsoft.Isam.Esent.Interop.EsentSLVSpaceWriteConflictException</span></span>](./esentslvspacewriteconflictexception-class.md)  
            [<span data-ttu-id="d73d2-218">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileAlreadyExistsException</span><span class="sxs-lookup"><span data-stu-id="d73d2-218">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileAlreadyExistsException</span></span>](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [<span data-ttu-id="d73d2-219">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileFullException</span><span class="sxs-lookup"><span data-stu-id="d73d2-219">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileFullException</span></span>](./esentslvstreamingfilefullexception-class.md)  
            [<span data-ttu-id="d73d2-220">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileInUseException</span><span class="sxs-lookup"><span data-stu-id="d73d2-220">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileInUseException</span></span>](./esentslvstreamingfileinuseexception-class.md)  
            [<span data-ttu-id="d73d2-221">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileMissingException</span><span class="sxs-lookup"><span data-stu-id="d73d2-221">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileMissingException</span></span>](./esentslvstreamingfilemissingexception-class.md)  
            [<span data-ttu-id="d73d2-222">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileNotCreatedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-222">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileNotCreatedException</span></span>](./esentslvstreamingfilenotcreatedexception-class.md)  
            [<span data-ttu-id="d73d2-223">Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileReadOnlyException</span><span class="sxs-lookup"><span data-stu-id="d73d2-223">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileReadOnlyException</span></span>](./esentslvstreamingfilereadonlyexception-class.md)  
            [<span data-ttu-id="d73d2-224">Microsoft. ISAM. esent. Interop. EsentSoftRecoveryOnSnapshotException</span><span class="sxs-lookup"><span data-stu-id="d73d2-224">Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException</span></span>](./esentsoftrecoveryonsnapshotexception-class.md)  
            [<span data-ttu-id="d73d2-225">Microsoft. ISAM. esent. Interop. EsentSPAvailExtCacheOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="d73d2-225">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfMemoryException</span></span>](./esentspavailextcacheoutofmemoryexception-class.md)  
            [<span data-ttu-id="d73d2-226">Microsoft. ISAM. esent. Interop. EsentSPAvailExtCacheOutOfSyncException</span><span class="sxs-lookup"><span data-stu-id="d73d2-226">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfSyncException</span></span>](./esentspavailextcacheoutofsyncexception-class.md)  
            [<span data-ttu-id="d73d2-227">Microsoft. ISAM. esent. Interop. EsentSQLLinkNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-227">Microsoft.Isam.Esent.Interop.EsentSQLLinkNotSupportedException</span></span>](./esentsqllinknotsupportedexception-class.md)  
            [<span data-ttu-id="d73d2-228">Microsoft. ISAM. esent. Interop. EsentStreamingDataNotLoggedException</span><span class="sxs-lookup"><span data-stu-id="d73d2-228">Microsoft.Isam.Esent.Interop.EsentStreamingDataNotLoggedException</span></span>](./esentstreamingdatanotloggedexception-class.md)  
            [<span data-ttu-id="d73d2-229">Microsoft. ISAM. esent. Interop. EsentTaggedNotNULLException</span><span class="sxs-lookup"><span data-stu-id="d73d2-229">Microsoft.Isam.Esent.Interop.EsentTaggedNotNULLException</span></span>](./esenttaggednotnullexception-class.md)  
            [<span data-ttu-id="d73d2-230">Microsoft. ISAM. esent. Interop. EsentTempFileOpenErrorException</span><span class="sxs-lookup"><span data-stu-id="d73d2-230">Microsoft.Isam.Esent.Interop.EsentTempFileOpenErrorException</span></span>](./esenttempfileopenerrorexception-class.md)  
            [<span data-ttu-id="d73d2-231">Microsoft. ISAM. esent. Interop. EsentTooManyOpenDatabasesException</span><span class="sxs-lookup"><span data-stu-id="d73d2-231">Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException</span></span>](./esenttoomanyopendatabasesexception-class.md)  
            [<span data-ttu-id="d73d2-232">Microsoft. ISAM. esent. Interop. EsentTooManySplitsException</span><span class="sxs-lookup"><span data-stu-id="d73d2-232">Microsoft.Isam.Esent.Interop.EsentTooManySplitsException</span></span>](./esenttoomanysplitsexception-class.md)  
            [<span data-ttu-id="d73d2-233">Microsoft. ISAM. esent. Interop. EsentUnicodeTranslationBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="d73d2-233">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationBufferTooSmallException</span></span>](./esentunicodetranslationbuffertoosmallexception-class.md)