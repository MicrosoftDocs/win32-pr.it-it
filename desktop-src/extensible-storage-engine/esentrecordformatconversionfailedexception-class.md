---
description: 'Altre informazioni su: classe EsentRecordFormatConversionFailedException'
title: Classe EsentRecordFormatConversionFailedException
TOCTitle: EsentRecordFormatConversionFailedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordformatconversionfailedexception(v=EXCHG.10)
ms:contentKeyID: 55102564
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1895eb3e7068106cc73bedc967b0c113c5c109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319228"
---
# <a name="esentrecordformatconversionfailedexception-class"></a>Classe EsentRecordFormatConversionFailedException

Classe di base per JET_err. Eccezioni RecordFormatConversionFailed.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentRecordFormatConversionFailedException  

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordFormatConversionFailedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentRecordFormatConversionFailedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordFormatConversionFailedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentRecordFormatConversionFailedException](./esentrecordformatconversionfailedexception-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
