---
description: 'Altre informazioni su: Enumerazione TempTableGrbit'
title: Enumerazione TempTableGrbit
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306819"
---
# <a name="temptablegrbit-enumeration"></a><span data-ttu-id="3a34c-103">Enumerazione TempTableGrbit</span><span class="sxs-lookup"><span data-stu-id="3a34c-103">TempTableGrbit enumeration</span></span>

<span data-ttu-id="3a34c-104">Opzioni per la creazione di tabelle temporanee.</span><span class="sxs-lookup"><span data-stu-id="3a34c-104">Options for temporary table creation.</span></span>

<span data-ttu-id="3a34c-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="3a34c-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="3a34c-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3a34c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3a34c-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3a34c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3a34c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a34c-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
```

## <a name="members"></a><span data-ttu-id="3a34c-109">Members</span><span class="sxs-lookup"><span data-stu-id="3a34c-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="3a34c-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="3a34c-110">Member name</span></span></th>
<th><span data-ttu-id="3a34c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a34c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3a34c-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="3a34c-112">None</span></span></td>
<td><span data-ttu-id="3a34c-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="3a34c-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3a34c-114">Indicizzata</span><span class="sxs-lookup"><span data-stu-id="3a34c-114">Indexed</span></span></td>
<td><span data-ttu-id="3a34c-115">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di JetSeek per la ricerca di record in base alla chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="3a34c-115">This option requests that the temporary table be flexible enough to permit the use of JetSeek to lookup records by index key.</span></span> <span data-ttu-id="3a34c-116">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="3a34c-116">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="3a34c-117">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="3a34c-117">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3a34c-118">Univoco</span><span class="sxs-lookup"><span data-stu-id="3a34c-118">Unique</span></span></td>
<td><span data-ttu-id="3a34c-119">Questa opzione richiede che i record con chiavi di indice duplicate vengano rimossi dal set di record finale nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="3a34c-119">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span> <span data-ttu-id="3a34c-120">Prima di Windows Server 2003, il motore di database presuppone sempre che questa opzione sia attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci.</span><span class="sxs-lookup"><span data-stu-id="3a34c-120">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="3a34c-121">A partire da Windows Server 2003, è ora possibile creare una tabella temporanea che non rimuove i duplicati quando viene specificata anche l'opzione <a href="dn351284(v=exchg.10).md">ForwardOnly</a> .</span><span class="sxs-lookup"><span data-stu-id="3a34c-121">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the <a href="dn351284(v=exchg.10).md">ForwardOnly</a> option is also specified.</span></span> <span data-ttu-id="3a34c-122">Non è possibile stabilire quale duplicato avrà vinto e quali duplicati verranno eliminati in generale.</span><span class="sxs-lookup"><span data-stu-id="3a34c-122">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="3a34c-123">Tuttavia, quando viene richiesta l'opzione ErrorOnDuplicateInsertion, il primo record con una chiave di indice specificata da inserire nella tabella temporanea sarà sempre vincente.</span><span class="sxs-lookup"><span data-stu-id="3a34c-123">However, when the ErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3a34c-124">Aggiornabile</span><span class="sxs-lookup"><span data-stu-id="3a34c-124">Updatable</span></span></td>
<td><span data-ttu-id="3a34c-125">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile per consentire la modifica successiva dei record che sono stati inseriti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3a34c-125">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="3a34c-126">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="3a34c-126">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="3a34c-127">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="3a34c-127">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3a34c-128">Scorrimento</span><span class="sxs-lookup"><span data-stu-id="3a34c-128">Scrollable</span></span></td>
<td><span data-ttu-id="3a34c-129">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi dei record in ordine arbitrario e direzione usando <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="3a34c-129">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span> <span data-ttu-id="3a34c-130">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="3a34c-130">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="3a34c-131">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="3a34c-131">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3a34c-132">SortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="3a34c-132">SortNullsHigh</span></span></td>
<td><span data-ttu-id="3a34c-133">Questa opzione richiede che i valori della colonna chiave NULL siano ordinati più vicino alla fine dell'indice rispetto ai valori di colonna chiave non NULL.</span><span class="sxs-lookup"><span data-stu-id="3a34c-133">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3a34c-134">ForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="3a34c-134">ForceMaterialization</span></span></td>
<td><span data-ttu-id="3a34c-135">Questa opzione impone al gestore tabelle temporaneo di abbandonare qualsiasi tentativo di scegliere una strategia intelligente per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="3a34c-135">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3a34c-136">ErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="3a34c-136">ErrorOnDuplicateInsertion</span></span></td>
<td><span data-ttu-id="3a34c-137">Questa opzione richiede che qualsiasi tentativo di inserire un record con la stessa chiave di indice di un record inserito in precedenza avrà immediatamente esito negativo con il <a href="hh564840(v=exchg.10).md">duplicato</a>.</span><span class="sxs-lookup"><span data-stu-id="3a34c-137">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span></span> <span data-ttu-id="3a34c-138">Se questa opzione non è richiesta, è possibile che un duplicato venga rilevato immediatamente e non riesca o venga rimosso automaticamente in un secondo momento, a seconda della strategia scelta dal motore di database per implementare la tabella temporanea in base alla funzionalità richiesta.</span><span class="sxs-lookup"><span data-stu-id="3a34c-138">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span> <span data-ttu-id="3a34c-139">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="3a34c-139">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="3a34c-140">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="3a34c-140">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3a34c-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a34c-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3a34c-142">Riferimento</span><span class="sxs-lookup"><span data-stu-id="3a34c-142">Reference</span></span>

[<span data-ttu-id="3a34c-143">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3a34c-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="3a34c-144">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="3a34c-144">ForwardOnly</span></span>](./server2003grbits.forwardonly-field.md)

[<span data-ttu-id="3a34c-145">IntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="3a34c-145">IntrinsicLVsOnly</span></span>](./windows7grbits.intrinsiclvsonly-field.md)
