---
description: Altre informazioni sul metodo GuidColumnValue.GetValueFromBytes
title: Metodo GuidColumnValue.GetValueFromBytes
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.GuidColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.guidcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55107384
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5521289344ba114d7b1d3abcec50702762a082d0332a31c0ed35a3ce1f3571c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118077420"
---
# <a name="guidcolumnvaluegetvaluefrombytes-method"></a>Metodo GuidColumnValue.GetValueFromBytes

Dati recuperati da ESENT, decodificare i dati e impostare il valore nell'oggetto ColumnValue.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
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

[Classe GuidColumnValue](./guidcolumnvalue-class.md)

[Membri di GuidColumnValue](./guidcolumnvalue-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
