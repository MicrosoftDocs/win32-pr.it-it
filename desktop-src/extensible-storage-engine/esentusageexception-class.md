---
description: 'Altre informazioni su: classe EsentUsageException'
title: Classe EsentUsageException
TOCTitle: EsentUsageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUsageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103173
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUsageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0319ae3d6185e3075931fb601ec789aba70dfd82
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103885909"
---
# <a name="esentusageexception-class"></a>Classe EsentUsageException

Classe di base per le eccezioni di utilizzo.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentUsageException  
            

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentUsageException _
    Inherits EsentApiException
'Usage
Dim instance As EsentUsageException
```

``` csharp
[SerializableAttribute]
public abstract class EsentUsageException : EsentApiException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentUsageException](./esentusageexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipi derivati

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentUsageException  
            [Microsoft. ISAM. esent. Interop. EsentAfterInitializationException](./esentafterinitializationexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentAlreadyInitializedException](./esentalreadyinitializedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentAlreadyPreparedException](./esentalreadypreparedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBackupDirectoryNotEmptyException](./esentbackupdirectorynotemptyexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadColumnIdException](./esentbadcolumnidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadRestoreTargetInstanceException](./esentbadrestoretargetinstanceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCallbackNotResolvedException](./esentcallbacknotresolvedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotBeTaggedException](./esentcannotbetaggedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotDeleteSystemTableException](./esentcannotdeletesystemtableexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotDeleteTemplateTableException](./esentcannotdeletetemplatetableexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotDeleteTempTableException](./esentcannotdeletetemptableexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotDisableVersioningException](./esentcannotdisableversioningexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotIndexException](./esentcannotindexexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotMaterializeForwardOnlySortException](./esentcannotmaterializeforwardonlysortexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotNestDDLException](./esentcannotnestddlexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCannotSeparateIntrinsicLVException](./esentcannotseparateintrinsiclvexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnCannotBeCompressedException](./esentcolumncannotbecompressedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnDoesNotFitException](./esentcolumndoesnotfitexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnDuplicateException](./esentcolumnduplicateexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnInUseException](./esentcolumninuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnNoChunkException](./esentcolumnnochunkexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnNotFoundException](./esentcolumnnotfoundexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnNotUpdatableException](./esentcolumnnotupdatableexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnRedundantException](./esentcolumnredundantexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentColumnTooBigException](./esentcolumntoobigexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseAlreadyRunningMaintenanceException](./esentdatabasealreadyrunningmaintenanceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseCorruptedNoRepairException](./esentdatabasecorruptednorepairexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseDuplicateException](./esentdatabaseduplicateexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseFileReadOnlyException](./esentdatabasefilereadonlyexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseInUseException](./esentdatabaseinuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseInvalidIncrementalReseedException](./esentdatabaseinvalidincrementalreseedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseInvalidNameException](./esentdatabaseinvalidnameexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseInvalidPagesException](./esentdatabaseinvalidpagesexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseInvalidPathException](./esentdatabaseinvalidpathexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseLockedException](./esentdatabaselockedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseNotFoundException](./esentdatabasenotfoundexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseSharingViolationException](./esentdatabasesharingviolationexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseSignInUseException](./esentdatabasesigninuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDDLNotInheritableException](./esentddlnotinheritableexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDefaultValueTooBigException](./esentdefaultvaluetoobigexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDensityInvalidException](./esentdensityinvalidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDisabledFunctionalityException](./esentdisabledfunctionalityexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentEntryPointNotFoundException](./esententrypointnotfoundexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentExclusiveTableLockRequiredException](./esentexclusivetablelockrequiredexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFeatureNotAvailableException](./esentfeaturenotavailableexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileCompressedException](./esentfilecompressedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFilteredMoveNotSupportedException](./esentfilteredmovenotsupportedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFixedDDLException](./esentfixedddlexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFixedInheritedDDLException](./esentfixedinheritedddlexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentForceDetachNotAllowedException](./esentforcedetachnotallowedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIllegalOperationException](./esentillegaloperationexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexDuplicateException](./esentindexduplicateexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexHasPrimaryException](./esentindexhasprimaryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexInvalidDefException](./esentindexinvaliddefexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexMustStayException](./esentindexmuststayexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexTuplesCannotRetrieveFromIndexException](./esentindextuplescannotretrievefromindexexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexTuplesInvalidLimitsException](./esentindextuplesinvalidlimitsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexTuplesKeyTooSmallException](./esentindextupleskeytoosmallexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexTuplesNonUniqueOnlyException](./esentindextuplesnonuniqueonlyexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexTuplesSecondaryIndexOnlyException](./esentindextuplessecondaryindexonlyexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexTuplesTextBinaryColumnsOnlyException](./esentindextuplestextbinarycolumnsonlyexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexTuplesVarSegMacNotAllowedException](./esentindextuplesvarsegmacnotallowedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInstanceNameInUseException](./esentinstancenameinuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInTransactionException](./esentintransactionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidBackupException](./esentinvalidbackupexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidBackupSequenceException](./esentinvalidbackupsequenceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidBookmarkException](./esentinvalidbookmarkexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidCodePageException](./esentinvalidcodepageexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidColumnTypeException](./esentinvalidcolumntypeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidCreateIndexException](./esentinvalidcreateindexexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidDatabaseException](./esentinvaliddatabaseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidDatabaseIdException](./esentinvaliddatabaseidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidGrbitException](./esentinvalidgrbitexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidIndexIdException](./esentinvalidindexidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidInstanceException](./esentinvalidinstanceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidLanguageIdException](./esentinvalidlanguageidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidLCMapStringFlagsException](./esentinvalidlcmapstringflagsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidNameException](./esentinvalidnameexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidOperationException](./esentinvalidoperationexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidParameterException](./esentinvalidparameterexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidPathException](./esentinvalidpathexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidPlaceholderColumnException](./esentinvalidplaceholdercolumnexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidPrereadException](./esentinvalidprereadexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidSesidException](./esentinvalidsesidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidSettingsException](./esentinvalidsettingsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidTableIdException](./esentinvalidtableidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentKeyIsMadeException](./esentkeyismadeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentKeyNotMadeException](./esentkeynotmadeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogFileNotCopiedException](./esentlogfilenotcopiedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogFilePathInUseException](./esentlogfilepathinuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogFileSizeMismatchException](./esentlogfilesizemismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLoggingDisabledException](./esentloggingdisabledexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLSAlreadySetException](./esentlsalreadysetexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLSCallbackNotSpecifiedException](./esentlscallbacknotspecifiedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMultiValuedColumnMustBeTaggedException](./esentmultivaluedcolumnmustbetaggedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMultiValuedIndexViolationException](./esentmultivaluedindexviolationexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMustBeSeparateLongValueException](./esentmustbeseparatelongvalueexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMustRollbackException](./esentmustrollbackexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentNoBackupDirectoryException](./esentnobackupdirectoryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentNoCurrentIndexException](./esentnocurrentindexexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentNotInitializedException](./esentnotinitializedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentNotInTransactionException](./esentnotintransactionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentNullInvalidException](./esentnullinvalidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentNullKeyDisallowedException](./esentnullkeydisallowedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOneDatabasePerSessionException](./esentonedatabasepersessionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOSSnapshotInvalidSequenceException](./esentossnapshotinvalidsequenceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOSSnapshotInvalidSnapIdException](./esentossnapshotinvalidsnapidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentPartiallyAttachedDBException](./esentpartiallyattacheddbexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentPermissionDeniedException](./esentpermissiondeniedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentQueryNotSupportedException](./esentquerynotsupportedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecordNoCopyException](./esentrecordnocopyexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecordPrimaryChangedException](./esentrecordprimarychangedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRestoreOfNonBackupDatabaseException](./esentrestoreofnonbackupdatabaseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRunningInMultiInstanceModeException](./esentrunninginmultiinstancemodeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRunningInOneInstanceModeException](./esentrunninginoneinstancemodeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSesidTableIdMismatchException](./esentsesidtableidmismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSessionContextAlreadySetException](./esentsessioncontextalreadysetexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSessionContextNotSetByThisThreadException](./esentsessioncontextnotsetbythisthreadexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSessionInUseException](./esentsessioninuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSessionSharingViolationException](./esentsessionsharingviolationexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSessionWriteConflictException](./esentsessionwriteconflictexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSoftRecoveryOnBackupDatabaseException](./esentsoftrecoveryonbackupdatabaseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSpaceHintsInvalidException](./esentspacehintsinvalidexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSystemParamsAlreadySetException](./esentsystemparamsalreadysetexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSystemPathInUseException](./esentsystempathinuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTableLockedException](./esenttablelockedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTableNotEmptyException](./esenttablenotemptyexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTempPathInUseException](./esenttemppathinuseexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTooManyActiveUsersException](./esenttoomanyactiveusersexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTooManyAttachedDatabasesException](./esenttoomanyattacheddatabasesexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTooManyColumnsException](./esenttoomanycolumnsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTooManyIndexesException](./esenttoomanyindexesexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTooManyKeysException](./esenttoomanykeysexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTooManyOpenTablesAndCleanupTimedOutException](./esenttoomanyopentablesandcleanuptimedoutexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTooManyTestInjectionsException](./esenttoomanytestinjectionsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTransReadOnlyException](./esenttransreadonlyexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentTransTooDeepException](./esenttranstoodeepexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentUnicodeNormalizationNotSupportedException](./esentunicodenormalizationnotsupportedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentUpdateMustVersionException](./esentupdatemustversionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentUpdateNotPreparedException](./esentupdatenotpreparedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentVersionStoreOutOfMemoryAndCleanupTimedOutException](./esentversionstoreoutofmemoryandcleanuptimedoutexception-class.md)