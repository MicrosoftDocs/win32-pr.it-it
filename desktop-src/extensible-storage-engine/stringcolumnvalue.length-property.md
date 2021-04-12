---
description: 'Altre informazioni su: Proprietà StringColumnValue. length'
title: Proprietà StringColumnValue. length
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55104090
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Length
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7313f66bd25653a66ebd8567a21c0ad5431ec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232738"
---
# <a name="stringcolumnvaluelength-property"></a>Proprietà StringColumnValue. length

Ottiene la lunghezza in byte di un valore di colonna, che è zero se la colonna è null; in caso contrario, corrisponde alla lunghezza in byte del valore stringa. La lunghezza in byte è determinata dal presupposto di due byte per carattere.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As StringColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe StringColumnValue](./stringcolumnvalue-class.md)

[Membri di StringColumnValue](./stringcolumnvalue-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
