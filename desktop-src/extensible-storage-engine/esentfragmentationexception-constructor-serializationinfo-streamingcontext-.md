---
description: 'Altre informazioni su: Costruttore EsentFragmentationException (SerializationInfo, StreamingContext)'
title: Costruttore EsentFragmentationException (SerializationInfo, StreamingContext)
TOCTitle: EsentFragmentationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101633
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae29411554d8a734fc250c3d8c8a04b381b2013c79dcb5c2c7aad22ff34963cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838631"
---
# <a name="esentfragmentationexception-constructor-serializationinfo-streamingcontext"></a>Costruttore EsentFragmentationException (SerializationInfo, StreamingContext)

Inizializza una nuova istanza della classe EsentFragmentationException. Questo costruttore viene usato per deserializzare un'eccezione serializzata.

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

Dim instance As New EsentFragmentationException(info, context)
```

``` csharp
protected EsentFragmentationException(
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

[Classe EsentFragmentationException](./esentfragmentationexception-class.md)

[Membri di EsentFragmentationException](./esentfragmentationexception-members.md)

[Overload di EsentFragmentationException](./esentfragmentationexception-constructor.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
