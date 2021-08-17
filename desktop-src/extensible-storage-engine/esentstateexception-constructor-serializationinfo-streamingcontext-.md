---
description: 'Altre informazioni su: Costruttore EsentStateException (SerializationInfo, StreamingContext)'
title: Costruttore EsentStateException (SerializationInfo, StreamingContext)
TOCTitle: EsentStateException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentStateException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102710
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 935cf9cbe6120e305de3ed9578e607fb366d36b66d10ccbb33e17a3a2ce71153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118769664"
---
# <a name="esentstateexception-constructor-serializationinfo-streamingcontext"></a>Costruttore EsentStateException (SerializationInfo, StreamingContext)

Inizializza una nuova istanza della classe EsentStateException. Questo costruttore viene usato per deserializzare un'eccezione serializzata.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
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

Dim instance As New EsentStateException(info, context)
```

``` csharp
protected EsentStateException(
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

[Classe EsentStateException](./esentstateexception-class.md)

[Membri di EsentStateException](./esentstateexception-members.md)

[Overload di EsentStateException](./esentstateexception-constructor.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
