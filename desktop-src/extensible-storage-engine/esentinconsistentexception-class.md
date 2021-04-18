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
# <a name="esentinconsistentexception-class"></a>Classe EsentInconsistentException

Classe di base per le eccezioni incoerenti.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentInconsistentException  
            

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

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

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentInconsistentException](./esentinconsistentexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipi derivati

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentInconsistentException  
            [Microsoft. ISAM. esent. Interop. EsentAttachedDatabaseMismatchException](./esentattacheddatabasemismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadCheckpointSignatureException](./esentbadcheckpointsignatureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadLogSignatureException](./esentbadlogsignatureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentBadLogVersionException](./esentbadlogversionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentCheckpointFileNotFoundException](./esentcheckpointfilenotfoundexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentConsistentTimeMismatchException](./esentconsistenttimemismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseDirtyShutdownException](./esentdatabasedirtyshutdownexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseIncompleteIncrementalReseedException](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDatabaseLogSetMismatchException](./esentdatabaselogsetmismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDbTimeTooNewException](./esentdbtimetoonewexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDbTimeTooOldException](./esentdbtimetoooldexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentEndingRestoreLogTooLowException](./esentendingrestorelogtoolowexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentExistingLogFileHasBadSignatureException](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentExistingLogFileIsNotContiguousException](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileInvalidTypeException](./esentfileinvalidtypeexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentGivenLogFileHasBadSignatureException](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentGivenLogFileIsNotContiguousException](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidCreateDbVersionException](./esentinvalidcreatedbversionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentInvalidDatabaseVersionException](./esentinvaliddatabaseversionexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogGenerationMismatchException](./esentloggenerationmismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMissingCurrentLogFilesException](./esentmissingcurrentlogfilesexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMissingFileToBackupException](./esentmissingfiletobackupexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMissingRestoreLogFilesException](./esentmissingrestorelogfilesexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentPageSizeMismatchException](./esentpagesizemismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentRequiredLogFilesMissingException](./esentrequiredlogfilesmissingexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentStartingRestoreLogTooHighException](./esentstartingrestorelogtoohighexception-class.md)