---
description: 'Altre informazioni su: Enumerazione AttachDatabaseGrbit'
title: Enumerazione AttachDatabaseGrbit
TOCTitle: AttachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.attachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81525e97f1b6266ba15baab50168404566bd7bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319280"
---
# <a name="attachdatabasegrbit-enumeration"></a>Enumerazione AttachDatabaseGrbit

Opzioni per JetAttachDatabase.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration AttachDatabaseGrbit
'Usage
Dim instance As AttachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum AttachDatabaseGrbit
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
<td>ReadOnly</td>
<td>Impedisce le modifiche al database.</td>
</tr>
<tr class="odd">
<td></td>
<td>DeleteCorruptIndexes</td>
<td>Se JET_paramEnableIndexChecking è stato impostato, verranno eliminati tutti gli indici sui dati Unicode.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
