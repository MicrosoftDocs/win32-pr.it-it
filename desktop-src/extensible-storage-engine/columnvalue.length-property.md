---
description: Altre informazioni sulla proprietà ColumnValue.Length
title: ColumnValue.Length - proprietà
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55101208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Length
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93ff15d348b2d47f76c680547d6e7939ebbd2c5faeaa240d9d18b1c3f523b93f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083664"
---
# <a name="columnvaluelength-property"></a>ColumnValue.Length - proprietà

Ottiene la lunghezza in byte di un valore di colonna, che è zero se column è Null. In caso contrario, corrisponde a Size per le colonne a dimensione fissa e rappresenta la lunghezza in byte del valore effettivo per le colonne di dimensioni variabili( binario e stringa). Per le stringhe, la lunghezza viene determinata presupponendo due byte per carattere.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public MustOverride ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public abstract int Length { get; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe ColumnValue](./columnvalue-class.md)

[Membri ColumnValue](./columnvalue-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
