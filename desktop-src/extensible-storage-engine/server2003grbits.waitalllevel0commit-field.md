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
# <a name="server2003grbitswaitalllevel0commit-field"></a><span data-ttu-id="024d2-103">Campo Server2003Grbits. WaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="024d2-103">Server2003Grbits.WaitAllLevel0Commit field</span></span>

<span data-ttu-id="024d2-104">Tutte le transazioni di cui è stato eseguito il commit in precedenza da una sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente.</span><span class="sxs-lookup"><span data-stu-id="024d2-104">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="024d2-105">Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="024d2-105">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="024d2-106">Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="024d2-106">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="024d2-107">Questa opzione non può essere usata in combinazione con altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="024d2-107">This option cannot be used in combination with any other option.</span></span>

<span data-ttu-id="024d2-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="024d2-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="024d2-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="024d2-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="024d2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="024d2-110">Syntax</span></span>

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

## <a name="see-also"></a><span data-ttu-id="024d2-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="024d2-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="024d2-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="024d2-112">Reference</span></span>

[<span data-ttu-id="024d2-113">Classe Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="024d2-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="024d2-114">Membri di Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="024d2-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="024d2-115">Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="024d2-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
