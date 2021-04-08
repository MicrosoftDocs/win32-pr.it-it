---
description: 'Altre informazioni su: Proprietà JET_ENUMCOLUMN. cEnumColumnValue'
title: Proprietà JET_ENUMCOLUMN. cEnumColumnValue
TOCTitle: 'cEnumColumnValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.cenumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103498
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_cEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_cEnumColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee9649f7c546dee155dfcda35ece32dfe346c689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749874"
---
# <a name="jet_enumcolumncenumcolumnvalue-property"></a>Proprietà JET_ENUMCOLUMN. cEnumColumnValue

Ottiene il numero di valori di colonna enumerati per la colonna. Questo membro viene utilizzato solo se [Err](./jet-enumcolumn.err-property.md) non è [ColumnSingleValue](./jet-wrn-enumeration.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property cEnumColumnValue As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As Integer

value = instance.cEnumColumnValue
```

``` csharp
public int cEnumColumnValue { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_ENUMCOLUMN](./jet-enumcolumn-class.md)

[Membri JET_ENUMCOLUMN](./jet-enumcolumn-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
