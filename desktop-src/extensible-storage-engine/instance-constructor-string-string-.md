---
description: 'Altre informazioni su: costruttore di istanze (String, String)'
title: Costruttore di istanza (String, String)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02cb629cdfaba17ce9a137b52eb1a6d6fdbaa56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344231"
---
# <a name="instance-constructor-string-string"></a>Costruttore di istanza (String, String)

Inizializza una nuova istanza della classe dell'istanza. Il JET_INSTANCE sottostante viene allocato, ma non inizializzato.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a>Parametri

  - name  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nome dell’istanza. Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.

<!-- end list -->

  - displayName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nome visualizzato per l'istanza di. Questa operazione verrà utilizzata nelle voci del registro eventi.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe dell'istanza](./instance-class.md)

[Membri di istanza](./instance-members.md)

[Overload dell'istanza](./instance-constructor.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
