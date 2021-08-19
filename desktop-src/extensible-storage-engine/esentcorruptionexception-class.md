---
description: Altre informazioni sulla classe EsentCorruptionException
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
ms.openlocfilehash: f0ac3d1884f41602490af23e3d63a388cd4d28e56fe92d80055ad8aaf462e0ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020901"
---
# <a name="esentcorruptionexception-class"></a>Classe EsentCorruptionException

Classe di base per le eccezioni di danneggiamento.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentCorruptionException  
            

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

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

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentCorruptionException](./esentcorruptionexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipi derivati

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentCorruptionException  
            [Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException](./esentbademptypageexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentBadPageLinkException](./esentbadpagelinkexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException](./esentbadparentpagelinkexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException](./esentcatalogcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException](./esentcheckpointcorruptexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException](./esentcommittedlogfilecorruptexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException](./esentcommittedlogfilesmissingexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException](./esentdatabasecorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDbTimeCorruptedException](./esentdbtimecorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException](./esentdecompressionfailedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException](./esentderivedcolumncorruptionexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException](./esentdiskreadverificationfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException](./esentfileiobeyondeofexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException](./esentfilesystemcorruptionexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException](./esentindexbuildcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException](./esentinvalidlogsequenceexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException](./esentlogcorruptduringhardrestoreexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogCorruptedException](./esentlogcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException](./esentlogfilecorruptexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException](./esentlogreadverifyfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentLVCorruptedException](./esentlvcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMissingLogFileException](./esentmissinglogfileexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException](./esentmissingpreviouslogfileexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException](./esentpagenotinitializedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException](./esentprimaryindexcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException](./esentreadlostflushverifyfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException](./esentreadpgnoverifyfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException](./esentreadverifyfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException](./esentrecordformatconversionfailedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException](./esentrecoveryverifyfailureexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException](./esentredoabruptendedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException](./esentsecondaryindexcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException](./esentspavailextcorruptedexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException](./esentspownextcorruptedexception-class.md)