---
description: 'Altre informazioni su: Enumerazione CommitTransactionGrbit'
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
ms.openlocfilehash: a93504d688d1eddfcde81ae23c87e62f70e0aab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319792"
---
# <a name="committransactiongrbit-enumeration"></a><span data-ttu-id="4ebca-103">Enumerazione CommitTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="4ebca-103">CommitTransactionGrbit enumeration</span></span>

<span data-ttu-id="4ebca-104">Opzioni per JetCommitTransaction.</span><span class="sxs-lookup"><span data-stu-id="4ebca-104">Options for JetCommitTransaction.</span></span>

<span data-ttu-id="4ebca-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="4ebca-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="4ebca-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ebca-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ebca-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ebca-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ebca-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="4ebca-109">Members</span><span class="sxs-lookup"><span data-stu-id="4ebca-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="4ebca-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="4ebca-110">Member name</span></span></th>
<th><span data-ttu-id="4ebca-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ebca-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4ebca-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="4ebca-112">None</span></span></td>
<td><span data-ttu-id="4ebca-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="4ebca-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4ebca-114">LazyFlush</span><span class="sxs-lookup"><span data-stu-id="4ebca-114">LazyFlush</span></span></td>
<td><span data-ttu-id="4ebca-115">Viene eseguito il commit della transazione in modo normale, ma questa API non attende che la transazione venga scaricata nel file di log delle transazioni prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="4ebca-115">The transaction is committed normally but this Api does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="4ebca-116">Questo riduce drasticamente la durata di un'operazione di commit al costo della durabilità.</span><span class="sxs-lookup"><span data-stu-id="4ebca-116">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="4ebca-117">Qualsiasi transazione non scaricata nel log prima di un arresto anomalo verrà automaticamente interrotta durante il ripristino dell'arresto anomalo durante la chiamata successiva a JetInit.</span><span class="sxs-lookup"><span data-stu-id="4ebca-117">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to JetInit.</span></span> <span data-ttu-id="4ebca-118">Se vengono specificati WaitLastLevel0Commit o WaitAllLevel0Commit, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="4ebca-118">If WaitLastLevel0Commit or WaitAllLevel0Commit are specified, this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4ebca-119">WaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="4ebca-119">WaitLastLevel0Commit</span></span></td>
<td><span data-ttu-id="4ebca-120">Se la sessione ha precedentemente eseguito il commit di tutte le transazioni che non sono ancora state scaricate nel file di log delle transazioni, è necessario scaricarle immediatamente.</span><span class="sxs-lookup"><span data-stu-id="4ebca-120">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="4ebca-121">Questa API resta in attesa fino a quando le transazioni non vengono scaricate prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="4ebca-121">This Api will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="4ebca-122">Questa operazione è utile se l'applicazione ha precedentemente eseguito il commit di più transazioni usando JET_bitCommitLazyFlush e ora vuole scaricarle tutte su disco.</span><span class="sxs-lookup"><span data-stu-id="4ebca-122">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span>
<p><span data-ttu-id="4ebca-123">Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="4ebca-123">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="4ebca-124">Questa opzione non può essere usata in combinazione con altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="4ebca-124">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="4ebca-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ebca-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ebca-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4ebca-126">Reference</span></span>

[<span data-ttu-id="4ebca-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4ebca-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
