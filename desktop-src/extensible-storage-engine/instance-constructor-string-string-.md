---
description: 'Altre informazioni su: Costruttore di istanza (String, String)'
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
ms.openlocfilehash: 2d93a5799a646a90688261bdd55bc9dfe929ef6bd074a51e15cabdcee768ffa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116441"
---
# <a name="instance-constructor-string-string"></a>Costruttore di istanza (String, String)

Inizializza una nuova istanza della classe Instance. L'JET_INSTANCE sottostante viene allocata, ma non inizializzata.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nome dell’istanza. Questa stringa deve essere univoca all'interno di un determinato processo che ospita il motore di database.

<!-- end list -->

  - displayName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nome visualizzato per l'istanza di . Verrà usato nelle voci del registro eventi.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe di istanza](./instance-class.md)

[Membri dell'istanza](./instance-members.md)

[Overload dell'istanza](./instance-constructor.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
