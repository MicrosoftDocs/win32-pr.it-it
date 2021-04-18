---
description: 'Altre informazioni su: Costruttore EsentCorruptionException (String, JET_err)'
title: Costruttore EsentCorruptionException (String, JET_err)
TOCTitle: EsentCorruptionException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101380
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30ed98ea56fe791ed949edc82b548990371c9671
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525068"
---
# <a name="esentcorruptionexception-constructor-string-jet_err"></a>Costruttore EsentCorruptionException (String, JET_err)

Inizializza una nuova istanza della classe EsentCorruptionException.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentCorruptionException(description, _
    err)
```

``` csharp
protected EsentCorruptionException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a>Parametri

  - description  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Descrizione dell'errore.

<!-- end list -->

  - Err  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)  
    
    Codice di errore dell'eccezione.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe EsentCorruptionException](./esentcorruptionexception-class.md)

[Membri di EsentCorruptionException](./esentcorruptionexception-members.md)

[Overload EsentCorruptionException](./esentcorruptionexception-constructor.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
