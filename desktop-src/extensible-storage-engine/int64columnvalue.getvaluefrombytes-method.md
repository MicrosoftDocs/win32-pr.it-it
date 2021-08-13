---
description: Altre informazioni sul metodo Int64ColumnValue.GetValueFromBytes
title: Metodo Int64ColumnValue.GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int64columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103365
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3479b629c3c791edf5d921427b7728d29ac5ffdf7ead02d1fe493fe8b7fa88e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476081"
---
# <a name="int64columnvaluegetvaluefrombytes-method"></a>Metodo Int64ColumnValue.GetValueFromBytes

Dati recuperati da ESENT, decodificare i dati e impostare il valore nell'oggetto ColumnValue.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a>Parametri

  - Valore  
    digitare: \[\]  
    
    Matrice di byte.

<!-- end list -->

  - startIndex  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Posizione iniziale all'interno dei byte.

<!-- end list -->

  - count  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero di byte da decodificare.

<!-- end list -->

  - Err  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Errore restituito da ESENT.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Int64ColumnValue](./int64columnvalue-class.md)

[Membri Int64ColumnValue](./int64columnvalue-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
