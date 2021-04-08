---
description: 'Altre informazioni su: Proprietà JET_COLUMNBASE. cbMax'
title: Proprietà JET_COLUMNBASE. cbMax
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103464
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d539df352119d24e1c8ddf7df816b8715f659417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058290"
---
# <a name="jet_columnbasecbmax-property"></a>Proprietà JET_COLUMNBASE. cbMax

Ottiene la lunghezza massima della colonna. Questa operazione è significativa solo per le colonne di tipo [Text](./jet-coltyp-enumeration.md), [LONGTEXT](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) e [LongBinary](./jet-coltyp-enumeration.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As Integer

value = instance.cbMax
```

``` csharp
public int cbMax { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_COLUMNBASE](./jet-columnbase-class.md)

[Membri JET_COLUMNBASE](./jet-columnbase-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
