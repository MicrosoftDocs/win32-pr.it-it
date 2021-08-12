---
description: 'Altre informazioni su: JET_ENUMCOLUMN.pvData'
title: JET_ENUMCOLUMN.pvData
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103500
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df79d838277a849c99ea49af2a8ca12e77cb3667d4750b141f0b9247b46b9232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254694"
---
# <a name="jet_enumcolumnpvdata-property"></a>JET_ENUMCOLUMN.pvData

Ottiene il valore enumerato per la colonna. Questo membro viene usato solo se [err](./jet-enumcolumn.err-property.md) è uguale a [ColumnSingleValue](./jet-wrn-enumeration.md). Punta alla memoria allocata con il callback dell'allocatore JET_PFNREALLOC passato [a](./jet-pfnrealloc-delegate.md) [JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[ \] , Int32, \[ \] JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md). Ricordarsi di rilasciare la memoria al termine.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property pvData As IntPtr
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As IntPtr

value = instance.pvData
```

``` csharp
public IntPtr pvData { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.IntPtr](/dotnet/api/system.intptr)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_ENUMCOLUMN classe](./jet-enumcolumn-class.md)

[JET_ENUMCOLUMN membri](./jet-enumcolumn-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
