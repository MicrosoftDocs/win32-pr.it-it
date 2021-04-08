---
description: 'Altre informazioni su: campo Server2003Grbits. WaitAllLevel0Commit'
title: Campo Server2003Grbits. WaitAllLevel0Commit (Microsoft. ISAM. esent. Interop. Server2003)
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
ms.openlocfilehash: 16390069adf81ead8e819bc5148a88e30900b508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882254"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a>Campo Server2003Grbits. WaitAllLevel0Commit

Tutte le transazioni di cui è stato eseguito il commit in precedenza da una sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente. Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante. Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione. Questa opzione non può essere usata in combinazione con altre opzioni.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
