---
description: Altre informazioni sull'enumerazione CommitTransactionGrbit
title: Enumerazione CommitTransactionGrbit
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec61d29a2bfc3fc502b532b83dbb02640a600a0a5034c9751caab7185f1b037c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117716650"
---
# <a name="committransactiongrbit-enumeration"></a>Enumerazione CommitTransactionGrbit

Opzioni per JetCommitTransaction.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a>Members

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
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
<td>LazyFlush</td>
<td>Il commit della transazione viene eseguito normalmente, ma questa API non attende lo scaricamento della transazione nel file di log delle transazioni prima di tornare al chiamante. In questo modo si riduce drasticamente la durata di un'operazione di commit a costo della durabilità. Qualsiasi transazione non scaricata nel log prima di un arresto anomalo del sistema verrà automaticamente interrotta durante il ripristino dell'arresto anomalo durante la chiamata successiva a JetInit. Se si specifica WaitLastLevel0Commit o WaitAllLevel0Commit, questa opzione viene ignorata.</td>
</tr>
<tr class="odd">
<td></td>
<td>WaitLastLevel0Commit</td>
<td>Se in precedenza la sessione ha eseguito il commit di transazioni e non sono ancora state scaricate nel file di log delle transazioni, devono essere scaricate immediatamente. Questa API attenderà che le transazioni siano state scaricate prima di tornare al chiamante. Ciò è utile se in precedenza l'applicazione ha eseguito il commit di diverse transazioni usando JET_bitCommitLazyFlush e ora vuole scaricarle tutte su disco.
<p>Questa opzione può essere usata anche se la sessione non è attualmente in una transazione. Questa opzione non può essere usata in combinazione con altre opzioni.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
