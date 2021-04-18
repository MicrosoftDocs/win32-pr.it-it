---
description: 'Altre informazioni su: Costruttore EsentException (String)'
title: Costruttore EsentException (String) (Microsoft. ISAM. ESENT)
TOCTitle: EsentException constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100720
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22a93625b7becbe083a42fbd6fcc71ad801173ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318449"
---
# <a name="esentexception-constructor-string"></a>Costruttore EsentException (String)

Inizializza una nuova istanza della classe EsentException con un messaggio di errore specificato.

**Spazio dei nomi:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Protected Sub New ( _
    message As String _
)
'Usage
Dim message As String

Dim instance As New EsentException(message)
```

``` csharp
protected EsentException(
    string message
)
```

#### <a name="parameters"></a>Parametri

  - message  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Messaggio in cui viene descritto l'errore.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe EsentException](./esentexception-class.md)

[Membri di EsentException](./esentexception-members.md)

[Overload EsentException](./esentexception-constructor.md)

[Spazio dei nomi Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)
