---
description: 'Altre informazioni su: Enumerazione JET_dbstate'
title: Enumerazione JET_dbstate
TOCTitle: JET_dbstate enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbstate(v=EXCHG.10)
ms:contentKeyID: 39511841
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_dbstate
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a83c8a4313e5e6f21ee885ee7936c90503bfbd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749882"
---
# <a name="jet_dbstate-enumeration"></a>Enumerazione JET_dbstate

Stati del database (utilizzati in [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Enumeration JET_dbstate
'Usage
Dim instance As JET_dbstate
```

``` csharp
public enum JET_dbstate
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome del membro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Blue Water Corporation</td>
<td>Il database è stato appena creato.</td>
</tr>
<tr class="even">
<td></td>
<td>DirtyShutdown</td>
<td>Database di chiusura Dirty (non coerente).</td>
</tr>
<tr class="odd">
<td></td>
<td>CleanShutdown</td>
<td>Database di chiusura normale (coerente).</td>
</tr>
<tr class="even">
<td></td>
<td>BeingConverted</td>
<td>È in corso la conversione del database.</td>
</tr>
<tr class="odd">
<td></td>
<td>ForceDetach</td>
<td>Il database è stato scollegato forzatamente.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
