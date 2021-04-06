---
description: 'Altre informazioni su: Enumerazione BeginTransactionGrbit'
title: Enumerazione BeginTransactionGrbit
TOCTitle: BeginTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.begintransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39515115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5f407c54b7b6e76ab63dcfb97d1307458ba15277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758969"
---
# <a name="begintransactiongrbit-enumeration"></a>Enumerazione BeginTransactionGrbit

Opzioni per [JetBeginTransaction2 (JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginTransactionGrbit
'Usage
Dim instance As BeginTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginTransactionGrbit
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
<td>Il database non viene modificato dalla transazione. Se si tenta di eseguire un aggiornamento, l'operazione avrà esito negativo con <a href="hh564840(v=exchg.10).md">transreadonly</a>. Questa opzione viene ignorata a meno che non venga richiesta quando la sessione specificata non è già presente in una transazione.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
