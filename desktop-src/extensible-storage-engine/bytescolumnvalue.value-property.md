---
description: Altre informazioni sulla proprietà BytesColumnValue.Value
title: BytesColumnValue.Value - proprietà
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55107249
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Value
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffe33303a84f9a5726ae64ae08ba9de65e355d5bfd59f318dcb84baa8053b83f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117717099"
---
# <a name="bytescolumnvaluevalue-property"></a>BytesColumnValue.Value - proprietà

Ottiene o imposta il valore della colonna. Usare [SetColumns(JET_SESID, JET_TABLEID, \[ \] )](./api.setcolumns-method.md) per aggiornare un record con il valore della colonna.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property Value As Byte()
    Get
    Set
'Usage
Dim instance As BytesColumnValue
Dim value As Byte()

value = instance.Value

instance.Value = value
```

``` csharp
public byte[] Value { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

digitare: \[\]  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe BytesColumnValue](./bytescolumnvalue-class.md)

[Membri bytesColumnValue](./bytescolumnvalue-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
