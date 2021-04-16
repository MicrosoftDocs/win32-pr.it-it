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
# <a name="esentobsoleteexception-class"></a>Classe EsentObsoleteException

Classe base per le eccezioni obsolete.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentObsoleteException  
            

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

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

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentObsoleteException](./esentobsoleteexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipi derivati

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentObsoleteException  
            [Microsoft. ISAM. esent. Interop. EsentAccessDeniedException](./esentaccessdeniedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadBackupDatabaseSizeException](./esentbadbackupdatabasesizeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadBookmarkException](./esentbadbookmarkexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadDbSignatureException](./esentbaddbsignatureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadPatchPageException](./esentbadpatchpageexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadSLVSignatureException](./esentbadslvsignatureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotAddFixedVarColumnToDerivedTableException](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotNestDistributedTransactionsException](./esentcannotnestdistributedtransactionsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnIndexedException](./esentcolumnindexedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnInRelationshipException](./esentcolumninrelationshipexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnLongException](./esentcolumnlongexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentContainerNotEmptyException](./esentcontainernotemptyexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCurrencyStackOutOfMemoryException](./esentcurrencystackoutofmemoryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabase200FormatException](./esentdatabase200formatexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabase400FormatException](./esentdatabase400formatexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabase500FormatException](./esentdatabase500formatexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseIdInUseException](./esentdatabaseidinuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabasePatchFileMismatchException](./esentdatabasepatchfilemismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabasesNotFromSameSnapshotException](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseStreamingFileMismatchException](./esentdatabasestreamingfilemismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseUnavailableException](./esentdatabaseunavailableexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDataHasChangedException](./esentdatahaschangedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDistributedTransactionAlreadyPreparedToCommitException](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDistributedTransactionNotYetPreparedToCommitException](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDTCCallbackUnexpectedErrorException](./esentdtccallbackunexpectederrorexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDTCMissingCallbackException](./esentdtcmissingcallbackexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDTCMissingCallbackOnRecoveryException](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileCloseException](./esentfilecloseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileIOAbortException](./esentfileioabortexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileIOFailException](./esentfileiofailexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileIORetryException](./esentfileioretryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileIOSparseException](./esentfileiosparseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexCantBuildException](./esentindexcantbuildexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexTuplesTooManyColumnsException](./esentindextuplestoomanycolumnsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidCountryException](./esentinvalidcountryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidFilenameException](./esentinvalidfilenameexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidLogDirectoryException](./esentinvalidlogdirectoryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidLoggedOperationException](./esentinvalidloggedoperationexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidObjectException](./esentinvalidobjectexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidOnSortException](./esentinvalidonsortexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidSystemPathException](./esentinvalidsystempathexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentKeyBoundaryException](./esentkeyboundaryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentKeyTooBigException](./esentkeytoobigexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLanguageNotSupportedException](./esentlanguagenotsupportedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLinkNotSupportedException](./esentlinknotsupportedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogBufferTooSmallException](./esentlogbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMissingPatchPageException](./esentmissingpatchpageexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMustCommitDistributedTransactionToLevel0Exception](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMustDisableLoggingForDbUpgradeException](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentNotInDistributedTransactionException](./esentnotindistributedtransactionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentObjectDuplicateException](./esentobjectduplicateexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentPageBoundaryException](./esentpageboundaryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentPatchFileMissingException](./esentpatchfilemissingexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRfsFailureException](./esentrfsfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRfsNotArmedException](./esentrfsnotarmedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRollbackRequiredException](./esentrollbackrequiredexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVBufferTooSmallException](./esentslvbuffertoosmallexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVColumnCannotDeleteException](./esentslvcolumncannotdeleteexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVColumnDefaultValueNotAllowedException](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVCorruptedException](./esentslvcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVDatabaseMissingException](./esentslvdatabasemissingexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVEAListCorruptException](./esentslvealistcorruptexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVEAListTooBigException](./esentslvealisttoobigexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVEAListZeroAllocationException](./esentslvealistzeroallocationexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVFileAccessDeniedException](./esentslvfileaccessdeniedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVFileInUseException](./esentslvfileinuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVFileInvalidPathException](./esentslvfileinvalidpathexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVFileIOException](./esentslvfileioexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVFileNotFoundException](./esentslvfilenotfoundexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVFileStaleException](./esentslvfilestaleexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVFileUnknownException](./esentslvfileunknownexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVHeaderBadChecksumException](./esentslvheaderbadchecksumexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVHeaderCorruptedException](./esentslvheadercorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVInvalidPathException](./esentslvinvalidpathexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVOwnerMapAlreadyExistsException](./esentslvownermapalreadyexistsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVOwnerMapCorruptedException](./esentslvownermapcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVOwnerMapPageNotFoundException](./esentslvownermappagenotfoundexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVPagesNotCommittedException](./esentslvpagesnotcommittedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVPagesNotDeletedException](./esentslvpagesnotdeletedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVPagesNotFreeException](./esentslvpagesnotfreeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVPagesNotReservedException](./esentslvpagesnotreservedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVProviderNotLoadedException](./esentslvprovidernotloadedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVProviderVersionMismatchException](./esentslvproviderversionmismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVReadVerifyFailureException](./esentslvreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVRootNotSpecifiedException](./esentslvrootnotspecifiedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVRootPathInvalidException](./esentslvrootpathinvalidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVRootStillOpenException](./esentslvrootstillopenexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVSpaceCorruptedException](./esentslvspacecorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVSpaceWriteConflictException](./esentslvspacewriteconflictexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileAlreadyExistsException](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileFullException](./esentslvstreamingfilefullexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileInUseException](./esentslvstreamingfileinuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileMissingException](./esentslvstreamingfilemissingexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileNotCreatedException](./esentslvstreamingfilenotcreatedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSLVStreamingFileReadOnlyException](./esentslvstreamingfilereadonlyexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSoftRecoveryOnSnapshotException](./esentsoftrecoveryonsnapshotexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSPAvailExtCacheOutOfMemoryException](./esentspavailextcacheoutofmemoryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSPAvailExtCacheOutOfSyncException](./esentspavailextcacheoutofsyncexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSQLLinkNotSupportedException](./esentsqllinknotsupportedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentStreamingDataNotLoggedException](./esentstreamingdatanotloggedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTaggedNotNULLException](./esenttaggednotnullexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTempFileOpenErrorException](./esenttempfileopenerrorexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTooManyOpenDatabasesException](./esenttoomanyopendatabasesexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTooManySplitsException](./esenttoomanysplitsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentUnicodeTranslationBufferTooSmallException](./esentunicodetranslationbuffertoosmallexception-class.md)