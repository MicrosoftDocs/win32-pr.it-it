---
description: 'Altre informazioni su: <T> classe ColumnValueOfStruct'
title: Classe ColumnValueOfStruct (T)
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351091"
---
# <a name="columnvalueofstructt-class"></a>\<T\>Classe ColumnValueOfStruct

Impostare una colonna di tipo struct (ad esempio, Int32/GUID).

## <a name="inheritance-hierarchy"></a>Gerarchia di ereditarietà

[System.Object](/dotnet/api/system.object)  
  [Microsoft. ISAM. esent. Interop. ColumnValue](./columnvalue-class.md)  
    Microsoft. ISAM. esent. Interop. ColumnValueOfStruct\<T\>  
      

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a>Parametri di tipo

  - T  
    Tipo da impostare.

## <a name="thread-safety"></a>Thread safety

I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe. Non è invece garantita la sicurezza dei membri dell'istanza.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Membri di ColumnValueOfStruct \<T\>](./columnvalueofstruct-t-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Tipi derivati

[System.Object](/dotnet/api/system.object)  
  [Microsoft. ISAM. esent. Interop. ColumnValue](./columnvalue-class.md)  
    Microsoft. ISAM. esent. Interop. ColumnValueOfStruct\<T\>  
      [Microsoft. ISAM. esent. Interop. BoolColumnValue](./boolcolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. ByteColumnValue](./bytecolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. DateTimeColumnValue](./datetimecolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. DoubleColumnValue](./doublecolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. FloatColumnValue](./floatcolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. GuidColumnValue](./guidcolumnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. Int16ColumnValue](./int16columnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. Int32ColumnValue](./int32columnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. Int64ColumnValue](./int64columnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. UInt16ColumnValue](./uint16columnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. UInt32ColumnValue](./uint32columnvalue-class.md)  
      [Microsoft. ISAM. esent. Interop. UInt64ColumnValue](./uint64columnvalue-class.md)