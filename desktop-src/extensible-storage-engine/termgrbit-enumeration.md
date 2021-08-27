---
description: Altre informazioni sull'enumerazione TermGrbit
title: Enumerazione TermGrbit
TOCTitle: TermGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TermGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.termgrbit(v=EXCHG.10)
ms:contentKeyID: 39511147
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TermGrbit.None
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83bf60be88aa1db7bac30c96c0c438d453c6fc24279b18502205ce96e60b9f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978371"
---
# <a name="termgrbit-enumeration"></a>Enumerazione TermGrbit

Opzioni per [JetTerm2(JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TermGrbit
'Usage
Dim instance As TermGrbit
```

``` csharp
[FlagsAttribute]
public enum TermGrbit
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
<td>Operazione completata</td>
<td>Richiede che l'istanza sia arrestata in modo pulito. Tutte le operazioni di pulizia facoltative che normalmente vengono eseguite in background in fase di esecuzione vengono completate immediatamente.</td>
</tr>
<tr class="odd">
<td></td>
<td>Brusco</td>
<td>Richiede che l'istanza sia arrestata il più rapidamente possibile. Tutte le operazioni facoltative che in genere vengono eseguite in background in fase di esecuzione vengono abbandonate.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

[Sporco](./windows7grbits.dirty-field.md)
