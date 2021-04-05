---
description: 'Altre informazioni su: costruttore di istanza (String, String, TermGrbit)'
title: Costruttore di istanza (String, String, TermGrbit)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753303"
---
# <a name="instance-constructor-string-string-termgrbit"></a>Costruttore di istanza (String, String, TermGrbit)

Inizializza una nuova istanza della classe dell'istanza. Il JET_INSTANCE sottostante viene allocato, ma non inizializzato.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
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

<!-- end list -->

  - termGrbit  
    Tipo: [Microsoft. ISAM. esent. Interop. TermGrbit](./termgrbit-enumeration.md)  
    
    TermGrbit da utilizzare in fase di JetTerm.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe dell'istanza](./instance-class.md)

[Membri di istanza](./instance-members.md)

[Overload dell'istanza](./instance-constructor.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
