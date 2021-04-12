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
# <a name="esentcorruptionexception-class"></a>Classe EsentCorruptionException

Classe di base per le eccezioni di danneggiamento.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentCorruptionException  
            

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipi derivati

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentCorruptionException  
            [Microsoft. ISAM. esent. Interop. EsentBadEmptyPageException](./esentbademptypageexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadPageLinkException](./esentbadpagelinkexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadParentPageLinkException](./esentbadparentpagelinkexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCatalogCorruptedException](./esentcatalogcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCheckpointCorruptException](./esentcheckpointcorruptexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCommittedLogFileCorruptException](./esentcommittedlogfilecorruptexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCommittedLogFilesMissingException](./esentcommittedlogfilesmissingexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseBufferDependenciesCorruptedException](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseCorruptedException](./esentdatabasecorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDbTimeCorruptedException](./esentdbtimecorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDecompressionFailedException](./esentdecompressionfailedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDerivedColumnCorruptionException](./esentderivedcolumncorruptionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDiskReadVerificationFailureException](./esentdiskreadverificationfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileIOBeyondEOFException](./esentfileiobeyondeofexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileSystemCorruptionException](./esentfilesystemcorruptionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentIndexBuildCorruptedException](./esentindexbuildcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidLogSequenceException](./esentinvalidlogsequenceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogCorruptDuringHardRecoveryException](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogCorruptDuringHardRestoreException](./esentlogcorruptduringhardrestoreexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogCorruptedException](./esentlogcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogFileCorruptException](./esentlogfilecorruptexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogReadVerifyFailureException](./esentlogreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogTornWriteDuringHardRecoveryException](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogTornWriteDuringHardRestoreException](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLVCorruptedException](./esentlvcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMissingLogFileException](./esentmissinglogfileexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMissingPreviousLogFileException](./esentmissingpreviouslogfileexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentPageNotInitializedException](./esentpagenotinitializedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentPrimaryIndexCorruptedException](./esentprimaryindexcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentReadLostFlushVerifyFailureException](./esentreadlostflushverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentReadPgnoVerifyFailureException](./esentreadpgnoverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentReadVerifyFailureException](./esentreadverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecordFormatConversionFailedException](./esentrecordformatconversionfailedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRecoveryVerifyFailureException](./esentrecoveryverifyfailureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRedoAbruptEndedException](./esentredoabruptendedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSecondaryIndexCorruptedException](./esentsecondaryindexcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSPAvailExtCorruptedException](./esentspavailextcorruptedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentSPOwnExtCorruptedException](./esentspownextcorruptedexception-class.md)