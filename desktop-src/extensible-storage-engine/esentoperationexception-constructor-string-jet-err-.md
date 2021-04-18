---
description: 'Altre informazioni su: Costruttore EsentOperationException (String, JET_err)'
title: Costruttore EsentOperationException (String, JET_err)
TOCTitle: EsentOperationException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentOperationException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102376
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb25ea404e4581b369f9d81e772ba4b2e95f7fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310890"
---
# <a name="esentoperationexception-constructor-string-jet_err"></a>Costruttore EsentOperationException (String, JET_err)

Inizializza una nuova istanza della classe EsentOperationException.

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

Dim instance As New EsentOperationException(description, _
    err)
```

``` csharp
protected EsentOperationException(
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

[Classe EsentOperationException](./esentoperationexception-class.md)

[Membri di EsentOperationException](./esentoperationexception-members.md)

[Overload EsentOperationException](./esentoperationexception-constructor.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
