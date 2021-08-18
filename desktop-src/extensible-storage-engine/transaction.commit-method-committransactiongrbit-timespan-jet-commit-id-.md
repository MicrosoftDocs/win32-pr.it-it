---
description: 'Altre informazioni su: Metodo Transaction.Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)'
title: Metodo Transaction.Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
TOCTitle: Commit method (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104166
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 90fd53fd7097db98ab84148b3f32710c369c948ed64c3606d0018cc8e79c877a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890514"
---
# <a name="transactioncommit-method-committransactiongrbit-timespan-jet_commit_id"></a>Metodo Transaction.Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)

Eseguire il commit di una transazione. Questo oggetto deve essere in una transazione.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_ID

instance.Commit(grbit, durableCommit, _
    commitId)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a>Parametri

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)  
    
    Opzioni di JetCommitTransaction.

<!-- end list -->

  - durableCommit  
    Tipo: [System.TimeSpan](/dotnet/api/system.timespan)  
    
    Durata per il commit di transazioni lazy.

<!-- end list -->

  - id commit  
    Tipo: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Commit-id per questo record di commit.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Transaction (classe)](./transaction-class.md)

[Membri della transazione](./transaction-members.md)

[Overload del commit](./transaction.commit-method.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
