---
description: 'Altre informazioni su: Proprietà JET_ENUMCOLUMN. pvData'
title: Proprietà JET_ENUMCOLUMN. pvData
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
ms.openlocfilehash: b7d4c72a45d90fd8004af2011f9f6081a59cfabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484892"
---
# <a name="jet_enumcolumnpvdata-property"></a>Proprietà JET_ENUMCOLUMN. pvData

Ottiene il valore enumerato per la colonna. Questo membro viene utilizzato solo se [Err](./jet-enumcolumn.err-property.md) è uguale a [ColumnSingleValue](./jet-wrn-enumeration.md). Questo fa riferimento alla memoria allocata con il callback dell'allocatore [JET_PFNREALLOC](./jet-pfnrealloc-delegate.md) passato a [JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, \[ \] , Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md). Ricordarsi di rilasciare la memoria al termine dell'operazione.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [System. IntPtr](/dotnet/api/system.intptr)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_ENUMCOLUMN](./jet-enumcolumn-class.md)

[Membri JET_ENUMCOLUMN](./jet-enumcolumn-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
