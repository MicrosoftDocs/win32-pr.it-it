---
description: 'Altre informazioni su: Costruttore EsentDiskException (String, JET_err)'
title: Costruttore EsentDiskException (String, JET_err)
TOCTitle: EsentDiskException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDiskException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101616
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de3c9fd996c318a3df3445afbf1a7a0054ed3253c669a837c62c23e35159d9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065664"
---
# <a name="esentdiskexception-constructor-string-jet_err"></a>Costruttore EsentDiskException (String, JET_err)

Inizializza una nuova istanza della classe EsentDiskException.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Dim instance As New EsentDiskException(description, _
    err)
```

``` csharp
protected EsentDiskException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a>Parametri

  - description  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Descrizione dell'errore.

<!-- end list -->

  - Err  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)  
    
    Codice di errore dell'eccezione.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe EsentDiskException](./esentdiskexception-class.md)

[Membri di EsentDiskException](./esentdiskexception-members.md)

[Overload di EsentDiskException](./esentdiskexception-constructor.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
