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
# <a name="begintransactiongrbit-enumeration"></a><span data-ttu-id="e2e5b-103">Enumerazione BeginTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="e2e5b-103">BeginTransactionGrbit enumeration</span></span>

<span data-ttu-id="e2e5b-104">Opzioni per [JetBeginTransaction2 (JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span><span class="sxs-lookup"><span data-stu-id="e2e5b-104">Options for [JetBeginTransaction2(JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span></span>

<span data-ttu-id="e2e5b-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="e2e5b-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="e2e5b-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2e5b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2e5b-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2e5b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e5b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2e5b-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="e2e5b-109">Members</span><span class="sxs-lookup"><span data-stu-id="e2e5b-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e2e5b-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="e2e5b-110">Member name</span></span></th>
<th><span data-ttu-id="e2e5b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2e5b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e2e5b-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="e2e5b-112">None</span></span></td>
<td><span data-ttu-id="e2e5b-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="e2e5b-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e2e5b-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e2e5b-114">ReadOnly</span></span></td>
<td><span data-ttu-id="e2e5b-115">Il database non viene modificato dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="e2e5b-115">The transaction will not modify the database.</span></span> <span data-ttu-id="e2e5b-116">Se si tenta di eseguire un aggiornamento, l'operazione avrà esito negativo con <a href="hh564840(v=exchg.10).md">transreadonly</a>.</span><span class="sxs-lookup"><span data-stu-id="e2e5b-116">If an update is attempted, that operation will fail with <a href="hh564840(v=exchg.10).md">TransReadOnly</a>.</span></span> <span data-ttu-id="e2e5b-117">Questa opzione viene ignorata a meno che non venga richiesta quando la sessione specificata non è già presente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="e2e5b-117">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e2e5b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2e5b-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2e5b-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e2e5b-119">Reference</span></span>

[<span data-ttu-id="e2e5b-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e2e5b-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
