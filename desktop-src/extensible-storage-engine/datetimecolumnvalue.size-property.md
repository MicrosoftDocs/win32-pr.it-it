---
description: Altre informazioni sulla proprietà DateTimeColumnValue.Size
title: Proprietà DateTimeColumnValue.Size
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.DateTimeColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.datetimecolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55101209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.DateTimeColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b2aab09b2a758527944a901046403c4cc59efaa7de8e6a901984471edd5527b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982491"
---
# <a name="datetimecolumnvaluesize-property"></a>Proprietà DateTimeColumnValue.Size

Ottiene le dimensioni del valore nella colonna. Viene restituito 0 per le colonne con dimensioni variabili, ad esempio binarie e stringa.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe DateTimeColumnValue](./datetimecolumnvalue-class.md)

[Membri dateTimeColumnValue](./datetimecolumnvalue-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
