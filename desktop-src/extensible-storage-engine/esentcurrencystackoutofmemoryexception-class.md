---
description: Altre informazioni sulla classe EsentCurrencyStackOutOfMemoryException
title: Classe EsentCurrencyStackOutOfMemoryException
TOCTitle: EsentCurrencyStackOutOfMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcurrencystackoutofmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55101301
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 317067e55cef0a6079d319fc4a199f6d973421fe9f35fd4b5559e8d09967f728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119041659"
---
# <a name="esentcurrencystackoutofmemoryexception-class"></a>Classe EsentCurrencyStackOutOfMemoryException

Classe di base per JET_err. Eccezioni CurrencyStackOutOfMemory.

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException  

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCurrencyStackOutOfMemoryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentCurrencyStackOutOfMemoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCurrencyStackOutOfMemoryException : EsentObsoleteException
```

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di EsentCurrencyStackOutOfMemoryException](./esentcurrencystackoutofmemoryexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
