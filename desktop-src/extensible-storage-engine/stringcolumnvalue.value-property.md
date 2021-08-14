---
description: Altre informazioni sulla proprietà StringColumnValue.Value
title: StringColumnValue.Value - proprietà
TOCTitle: 'Value property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Value
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.value(v=EXCHG.10)
ms:contentKeyID: 55104098
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Value
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Value
- Microsoft.Isam.Esent.Interop.StringColumnValue.set_Value
- Microsoft.Isam.Esent.Interop.StringColumnValue.Value
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfc3167cc62faa2b7c25a670bc8ad1bc7cc31795a62361e36025c09f53ffbac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485383"
---
# <a name="stringcolumnvaluevalue-property"></a>StringColumnValue.Value - proprietà

Ottiene o imposta il valore della colonna. Usare [SetColumns(JET_SESID, JET_TABLEID, \[ \] )](./api.setcolumns-method.md) per aggiornare un record con il valore della colonna.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property Value As String
    Get
    Set
'Usage
Dim instance As StringColumnValue
Dim value As String

value = instance.Value

instance.Value = value
```

``` csharp
public string Value { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe StringColumnValue](./stringcolumnvalue-class.md)

[Membri di StringColumnValue](./stringcolumnvalue-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
