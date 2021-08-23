---
description: 'Altre informazioni su: Costruttore InstanceParameters'
title: Costruttore InstanceParameters
TOCTitle: 'InstanceParameters constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.InstanceParameters.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.instanceparameters(v=EXCHG.10)
ms:contentKeyID: 55107431
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.InstanceParameters
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 147cc3c68856744dc904d9dc730e44ad5c83b8593723b345e317f9c9602512b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618201"
---
# <a name="instanceparameters-constructor"></a>Costruttore InstanceParameters

Inizializza una nuova istanza della classe InstanceParameters.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCE

Dim instance As New InstanceParameters(instance)
```

``` csharp
public InstanceParameters(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a>Parametri

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Istanza di su cui impostare i parametri. Se si tratta di JET_INSTANCE. Nil, quindi le impostazioni influiscono sulle impostazioni predefinite delle istanze future.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri instanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
