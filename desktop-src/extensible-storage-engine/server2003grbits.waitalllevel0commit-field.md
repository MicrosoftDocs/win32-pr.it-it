---
description: Altre informazioni sul campo Server2003Grbits.WaitAllLevel0Commit
title: Campo Server2003Grbits.WaitAllLevel0Commit (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: WaitAllLevel0Commit field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.waitalllevel0commit(v=EXCHG.10)
ms:contentKeyID: 55104104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c6f3946d12b7614818545abc785d521e46b9c05ddedcffab09750846861782e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093171"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a>Campo Server2003Grbits.WaitAllLevel0Commit

Tutte le transazioni di cui è stato eseguito il commit in precedenza da qualsiasi sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente. Questa API attenderà che le transazioni siano state scaricate prima di tornare al chiamante. Questa opzione può essere usata anche se la sessione non è attualmente in una transazione. Questa opzione non può essere usata in combinazione con altre opzioni.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Const WaitAllLevel0Commit As CommitTransactionGrbit
'Usage
Dim value As CommitTransactionGrbit

value = Server2003Grbits.WaitAllLevel0Commit
```

``` csharp
public const CommitTransactionGrbit WaitAllLevel0Commit
```

## <a name="see-also"></a>Vedere anche

#### <a name="reference"></a>Riferimento

[Classe Server2003Grbits](./server2003grbits-class.md)

[Membri di Server2003Grbits](./server2003grbits-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
