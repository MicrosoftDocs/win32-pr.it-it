---
description: 'Altre informazioni su: Metodo Transaction. Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)'
title: Metodo Transaction. Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
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
ms.openlocfilehash: 18df363e4320a4b1a53c34e15fcf68939fce96ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057999"
---
# <a name="transactioncommit-method-committransactiongrbit-timespan-jet_commit_id"></a><span data-ttu-id="83161-103">Metodo Transaction. Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</span><span class="sxs-lookup"><span data-stu-id="83161-103">Transaction.Commit method (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</span></span>

<span data-ttu-id="83161-104">Eseguire il commit di una transazione.</span><span class="sxs-lookup"><span data-stu-id="83161-104">Commit a transaction.</span></span> <span data-ttu-id="83161-105">Questo oggetto deve trovarsi in una transazione.</span><span class="sxs-lookup"><span data-stu-id="83161-105">This object should be in a transaction.</span></span>

<span data-ttu-id="83161-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="83161-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="83161-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="83161-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="83161-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83161-108">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="83161-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="83161-109">Parameters</span></span>

  - <span data-ttu-id="83161-110">grbit</span><span class="sxs-lookup"><span data-stu-id="83161-110">grbit</span></span>  
    <span data-ttu-id="83161-111">Tipo: [Microsoft. ISAM. esent. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="83161-111">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="83161-112">Opzioni di JetCommitTransaction.</span><span class="sxs-lookup"><span data-stu-id="83161-112">JetCommitTransaction options.</span></span>

<!-- end list -->

  - <span data-ttu-id="83161-113">durableCommit</span><span class="sxs-lookup"><span data-stu-id="83161-113">durableCommit</span></span>  
    <span data-ttu-id="83161-114">Tipo: [System. TimeSpan](/dotnet/api/system.timespan)</span><span class="sxs-lookup"><span data-stu-id="83161-114">Type: [System.TimeSpan](/dotnet/api/system.timespan)</span></span>  
    
    <span data-ttu-id="83161-115">Durata del commit di transazioni Lazy.</span><span class="sxs-lookup"><span data-stu-id="83161-115">Duration for committing lazy transactions.</span></span>

<!-- end list -->

  - <span data-ttu-id="83161-116">commitId</span><span class="sxs-lookup"><span data-stu-id="83161-116">commitId</span></span>  
    <span data-ttu-id="83161-117">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="83161-117">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="83161-118">Commit-ID per il record di commit.</span><span class="sxs-lookup"><span data-stu-id="83161-118">Commit-id for this commit record.</span></span>

## <a name="see-also"></a><span data-ttu-id="83161-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83161-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="83161-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="83161-120">Reference</span></span>

[<span data-ttu-id="83161-121">Transaction (classe)</span><span class="sxs-lookup"><span data-stu-id="83161-121">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="83161-122">Membri transazione</span><span class="sxs-lookup"><span data-stu-id="83161-122">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="83161-123">Overload commit</span><span class="sxs-lookup"><span data-stu-id="83161-123">Commit overload</span></span>](./transaction.commit-method.md)

[<span data-ttu-id="83161-124">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="83161-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
