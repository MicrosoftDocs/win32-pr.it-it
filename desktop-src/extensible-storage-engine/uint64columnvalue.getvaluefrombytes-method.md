---
description: 'Altre informazioni su: UInt64ColumnValue. GetValueFromBytes, metodo'
title: UInt64ColumnValue. GetValueFromBytes, metodo
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint64columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55104084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ccf4a0d85c6d712a81222f77b954d46f55a28df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308486"
---
# <a name="uint64columnvaluegetvaluefrombytes-method"></a>UInt64ColumnValue. GetValueFromBytes, metodo

Dato che i dati sono stati recuperati da ESENT, decodificano i dati e impostano il valore nell'oggetto ColumnValue.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Tipo \[\]  
    
    Matrice di byte.

<!-- end list -->

  - startIndex  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Posizione iniziale all'interno dei byte.

<!-- end list -->

  - count  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero di byte da decodificare.

<!-- end list -->

  - Err  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Errore restituito da ESENT.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe UInt64ColumnValue](./uint64columnvalue-class.md)

[Membri di UInt64ColumnValue](./uint64columnvalue-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
