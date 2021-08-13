---
description: 'Altre informazioni su: Costruttore EsentException (SerializationInfo, StreamingContext)'
title: Costruttore EsentException (SerializationInfo, StreamingContext) (Microsoft.Isam.Esent)
TOCTitle: EsentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100719
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
ms.openlocfilehash: f190f4a77d13cb4bc1e8a123dd1ec0f0b07498f2821a07d93a00372ecfaf32cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118778993"
---
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a>Costruttore EsentException (SerializationInfo, StreamingContext)

Inizializza una nuova istanza della classe EsentException. Questo costruttore viene utilizzato per deserializzare un'eccezione serializzata.

**Spazio dei nomi:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentException(info, context)
```

``` csharp
protected EsentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Parametri

  - info  
    Tipo: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Dati necessari per deserializzare l'oggetto.

<!-- end list -->

  - contesto  
    Tipo: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    Contesto di deserializzazione.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe EsentException](./esentexception-class.md)

[Membri di EsentException](./esentexception-members.md)

[Overload di EsentException](./esentexception-constructor.md)

[Spazio dei nomi Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)
