---
description: 'Altre informazioni su: Costruttore EsentApiException (SerializationInfo, StreamingContext)'
title: Costruttore EsentApiException (SerializationInfo, StreamingContext)
TOCTitle: EsentApiException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101059
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a00204c254378956521a1ae5fe02480dd879c832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485876"
---
# <a name="esentapiexception-constructor-serializationinfo-streamingcontext"></a>Costruttore EsentApiException (SerializationInfo, StreamingContext)

Inizializza una nuova istanza della classe EsentApiException. Questo costruttore viene utilizzato per deserializzare un'eccezione serializzata.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Dim instance As New EsentApiException(info, context)
```

``` csharp
protected EsentApiException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Parametri

  - info  
    Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Dati necessari per deserializzare l'oggetto.

<!-- end list -->

  - contesto  
    Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    Contesto di deserializzazione.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe EsentApiException](./esentapiexception-class.md)

[Membri di EsentApiException](./esentapiexception-members.md)

[Overload EsentApiException](./esentapiexception-constructor.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
