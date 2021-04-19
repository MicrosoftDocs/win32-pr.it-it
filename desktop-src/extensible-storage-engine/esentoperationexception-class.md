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
# <a name="esentoperationexception-class"></a>Classe EsentOperationException

Classe di base per le eccezioni dell'operazione.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        Microsoft. ISAM. esent. Interop. EsentOperationException  
          

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

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

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentOperationException](./esentoperationexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipi derivati

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        Microsoft. ISAM. esent. Interop. EsentOperationException  
          [Microsoft. ISAM. esent. Interop. EsentBackupAbortByServerException](./esentbackupabortbyserverexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentCheckpointDepthTooDeepException](./esentcheckpointdepthtoodeepexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentClientRequestToStopJetServiceException](./esentclientrequesttostopjetserviceexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentFatalException](./esentfatalexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentInitInProgressException](./esentinitinprogressexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentInternalErrorException](./esentinternalerrorexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentIOException](./esentioexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentNTSystemCallFailedException](./esentntsystemcallfailedexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentOSSnapshotTimeOutException](./esentossnapshottimeoutexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentRecordNotDeletedException](./esentrecordnotdeletedexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentTermInProgressException](./esentterminprogressexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUnicodeLanguageValidationFailureException](./esentunicodelanguagevalidationfailureexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUnicodeTranslationFailException](./esentunicodetranslationfailexception-class.md)