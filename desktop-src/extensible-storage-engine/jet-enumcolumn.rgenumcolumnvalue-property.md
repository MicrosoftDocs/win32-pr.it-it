---
description: 'Altre informazioni su: JET_ENUMCOLUMN.rgEnumColumnValue'
title: JET_ENUMCOLUMN.rgEnumColumnValue
TOCTitle: 'rgEnumColumnValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.rgenumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103505
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_rgEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_rgEnumColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 32322cf1952b6ce2ff8a3496cd5058e4915d86739c20e6c4baaab9577ed15488
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617231"
---
# <a name="jet_enumcolumnrgenumcolumnvalue-property"></a>JET_ENUMCOLUMN.rgEnumColumnValue

Ottiene i valori di colonna enumerati per la colonna. Questo membro viene usato solo se [err](./jet-enumcolumn.err-property.md) non è [ColumnSingleValue](./jet-wrn-enumeration.md).

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property rgEnumColumnValue As JET_ENUMCOLUMNVALUE()
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As JET_ENUMCOLUMNVALUE()

value = instance.rgEnumColumnValue
```

``` csharp
public JET_ENUMCOLUMNVALUE[] rgEnumColumnValue { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

digitare: \[\]  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_ENUMCOLUMN classe](./jet-enumcolumn-class.md)

[JET_ENUMCOLUMN membri](./jet-enumcolumn-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
