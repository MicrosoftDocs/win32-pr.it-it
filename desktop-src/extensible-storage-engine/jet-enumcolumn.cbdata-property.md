---
description: 'Altre informazioni su: Proprietà JET_ENUMCOLUMN. cbData'
title: Proprietà JET_ENUMCOLUMN. cbData
TOCTitle: 'cbData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.cbdata(v=EXCHG.10)
ms:contentKeyID: 55103617
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_cbData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_cbData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b38d6c8433cc9792ebdd7e04e72027c6e1477e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129082"
---
# <a name="jet_enumcolumncbdata-property"></a>Proprietà JET_ENUMCOLUMN. cbData

Ottiene la dimensione del valore enumerato per la colonna. Questo membro viene utilizzato solo se [Err](./jet-enumcolumn.err-property.md) è uguale a [ColumnSingleValue](./jet-wrn-enumeration.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property cbData As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As Integer

value = instance.cbData
```

``` csharp
public int cbData { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_ENUMCOLUMN](./jet-enumcolumn-class.md)

[Membri JET_ENUMCOLUMN](./jet-enumcolumn-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
