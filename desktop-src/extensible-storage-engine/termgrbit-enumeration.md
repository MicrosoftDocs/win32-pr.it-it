---
description: 'Altre informazioni su: Enumerazione TermGrbit'
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
ms.openlocfilehash: 49b466b298a78d7bfd6822904aed977e7117b927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759086"
---
# <a name="termgrbit-enumeration"></a>Enumerazione TermGrbit

Opzioni per [JetTerm2 (JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Richiede che l'istanza venga arrestata in modo corretto. Eventuali operazioni di pulizia facoltative normalmente eseguite in background in fase di esecuzione vengono completate immediatamente.</td>
</tr>
<tr class="odd">
<td></td>
<td>Improvviso</td>
<td>Richiede che l'istanza venga arrestata nel minor tempo possibile. Qualsiasi lavoro facoltativo che normalmente verrebbe eseguito in background in fase di esecuzione viene abbandonato.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[Sporco](./windows7grbits.dirty-field.md)
