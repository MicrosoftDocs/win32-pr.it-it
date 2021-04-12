---
description: 'Altre informazioni su: Enumerazione DetachDatabaseGrbit'
title: Enumerazione DetachDatabaseGrbit
TOCTitle: DetachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.detachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55100985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e67962420ee0179571da8262f17ea5279f59016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233774"
---
# <a name="detachdatabasegrbit-enumeration"></a>Enumerazione DetachDatabaseGrbit

Opzioni per [JetDetachDatabase2 (JET_SESID, String, DetachDatabaseGrbit)](./api.jetdetachdatabase2-method.md).

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DetachDatabaseGrbit
'Usage
Dim instance As DetachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum DetachDatabaseGrbit
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
<td>nessuno</td>
<td>Opzioni predefinite.</td>
</tr>
<tr class="even">
<td></td>
<td>ForceDetach</td>
<td><strong>Obsoleto.</strong> Se si usa ForceDetach, viene restituito <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> .</td>
</tr>
<tr class="odd">
<td></td>
<td>Chiusura forzata</td>
<td><strong>Obsoleto.</strong> Chiusura forzata non viene più utilizzato.</td>
</tr>
<tr class="even">
<td></td>
<td>ForceCloseAndDetach</td>
<td><strong>Obsoleto.</strong> Se si usa ForceCloseAndDetach, viene restituito <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> .</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
