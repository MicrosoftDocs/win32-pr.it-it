---
description: 'Altre informazioni su: Enumerazione CreateIndexGrbit'
title: Enumerazione CreateIndexGrbit
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318812"
---
# <a name="createindexgrbit-enumeration"></a><span data-ttu-id="26a9e-103">Enumerazione CreateIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="26a9e-103">CreateIndexGrbit enumeration</span></span>

<span data-ttu-id="26a9e-104">Opzioni per JetCreateIndex.</span><span class="sxs-lookup"><span data-stu-id="26a9e-104">Options for JetCreateIndex.</span></span>

<span data-ttu-id="26a9e-105">Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.</span><span class="sxs-lookup"><span data-stu-id="26a9e-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="26a9e-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="26a9e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="26a9e-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="26a9e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="26a9e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26a9e-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
```

## <a name="members"></a><span data-ttu-id="26a9e-109">Members</span><span class="sxs-lookup"><span data-stu-id="26a9e-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="26a9e-110">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="26a9e-110">Member name</span></span></th>
<th><span data-ttu-id="26a9e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26a9e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="26a9e-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="26a9e-112">None</span></span></td>
<td><span data-ttu-id="26a9e-113">Opzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="26a9e-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="26a9e-114">IndexUnique</span><span class="sxs-lookup"><span data-stu-id="26a9e-114">IndexUnique</span></span></td>
<td><span data-ttu-id="26a9e-115">Le voci di indice (chiavi) duplicate non sono consentite.</span><span class="sxs-lookup"><span data-stu-id="26a9e-115">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="26a9e-116">Questa operazione viene applicata quando viene chiamato JetUpdate, non quando viene chiamato JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="26a9e-116">This is enforced when JetUpdate is called, not when JetSetColumn is called.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="26a9e-117">IndexPrimary</span><span class="sxs-lookup"><span data-stu-id="26a9e-117">IndexPrimary</span></span></td>
<td><span data-ttu-id="26a9e-118">L'indice è un indice primario (cluster).</span><span class="sxs-lookup"><span data-stu-id="26a9e-118">The index is a primary (clustered) index.</span></span> <span data-ttu-id="26a9e-119">Ogni tabella deve avere esattamente un indice primario.</span><span class="sxs-lookup"><span data-stu-id="26a9e-119">Every table must have exactly one primary index.</span></span> <span data-ttu-id="26a9e-120">Se nessun indice primario viene definito in modo esplicito su una tabella, il motore di database creerà il proprio indice primario.</span><span class="sxs-lookup"><span data-stu-id="26a9e-120">If no primary index is explicitly defined over a table, then the database engine will create its own primary index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="26a9e-121">IndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="26a9e-121">IndexDisallowNull</span></span></td>
<td><span data-ttu-id="26a9e-122">Nessuna delle colonne in cui viene creato l'indice può contenere un valore NULL.</span><span class="sxs-lookup"><span data-stu-id="26a9e-122">None of the columns over which the index is created may contain a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="26a9e-123">IndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="26a9e-123">IndexIgnoreNull</span></span></td>
<td><span data-ttu-id="26a9e-124">Non aggiungere una voce di indice per una riga se tutte le colonne indicizzate sono NULL.</span><span class="sxs-lookup"><span data-stu-id="26a9e-124">Do not add an index entry for a row if all of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="26a9e-125">IndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="26a9e-125">IndexIgnoreAnyNull</span></span></td>
<td><span data-ttu-id="26a9e-126">Non aggiungere una voce di indice per una riga se una delle colonne indicizzate è NULL.</span><span class="sxs-lookup"><span data-stu-id="26a9e-126">Do not add an index entry for a row if any of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="26a9e-127">IndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="26a9e-127">IndexIgnoreFirstNull</span></span></td>
<td><span data-ttu-id="26a9e-128">Non aggiungere una voce di indice per una riga se la prima colonna indicizzata è NULL.</span><span class="sxs-lookup"><span data-stu-id="26a9e-128">Do not add an index entry for a row if the first column being indexed is NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="26a9e-129">IndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="26a9e-129">IndexLazyFlush</span></span></td>
<td><span data-ttu-id="26a9e-130">Specifica che le operazioni sugli indici verranno registrate in modalità differita.</span><span class="sxs-lookup"><span data-stu-id="26a9e-130">Specifies that the index operations will be logged lazily.</span></span> <span data-ttu-id="26a9e-131">JET_bitIndexLazyFlush non influisce sulla pigrizia degli aggiornamenti dei dati.</span><span class="sxs-lookup"><span data-stu-id="26a9e-131">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="26a9e-132">Se le operazioni di indicizzazione vengono interrotte dalla terminazione del processo, il ripristino soft sarà comunque in grado di ottenere il database in uno stato coerente, ma l'indice potrebbe non essere presente.</span><span class="sxs-lookup"><span data-stu-id="26a9e-132">If the indexing operations is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="26a9e-133">IndexEmpty</span><span class="sxs-lookup"><span data-stu-id="26a9e-133">IndexEmpty</span></span></td>
<td><span data-ttu-id="26a9e-134">Non tentare di compilare l'indice perché tutte le voci restituiscono NULL.</span><span class="sxs-lookup"><span data-stu-id="26a9e-134">Do not attempt to build the index, because all entries would evaluate to NULL.</span></span> <span data-ttu-id="26a9e-135">grbit deve inoltre specificare JET_bitIgnoreAnyNull quando viene passato JET_bitIndexEmpty.</span><span class="sxs-lookup"><span data-stu-id="26a9e-135">grbit MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="26a9e-136">Si tratta di un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="26a9e-136">This is a performance enhancement.</span></span> <span data-ttu-id="26a9e-137">Se, ad esempio, viene aggiunta una nuova colonna a una tabella, viene creato un indice sulla colonna appena aggiunta, tutti i record della tabella verranno analizzati anche se non vengono mai aggiunti all'indice.</span><span class="sxs-lookup"><span data-stu-id="26a9e-137">For example if a new column is added to a table, then an index is created over this newly added column, all of the records in the table would be scanned even though they would never get added to the index anyway.</span></span> <span data-ttu-id="26a9e-138">La specifica di JET_bitIndexEmpty ignora l'analisi della tabella, che potrebbe richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="26a9e-138">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="26a9e-139">IndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="26a9e-139">IndexUnversioned</span></span></td>
<td><span data-ttu-id="26a9e-140">Causa la visibilità della creazione dell'indice in altre transazioni.</span><span class="sxs-lookup"><span data-stu-id="26a9e-140">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="26a9e-141">In genere, una sessione in una transazione non sarà in grado di visualizzare un'operazione di creazione dell'indice in un'altra sessione.</span><span class="sxs-lookup"><span data-stu-id="26a9e-141">Normally a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="26a9e-142">Questo flag può essere utile se è probabile che un'altra transazione crei lo stesso indice, in modo che la seconda creazione dell'indice avrà esito negativo anziché causare potenzialmente molte operazioni di database non necessarie.</span><span class="sxs-lookup"><span data-stu-id="26a9e-142">This flag can be useful if another transaction is likely to create the same index, so that the second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="26a9e-143">La seconda transazione potrebbe non essere in grado di utilizzare immediatamente l'indice.</span><span class="sxs-lookup"><span data-stu-id="26a9e-143">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="26a9e-144">È necessario completare l'operazione di creazione dell'indice prima che sia utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="26a9e-144">The index creation operation needs to complete before it is usable.</span></span> <span data-ttu-id="26a9e-145">La sessione non deve attualmente trovarsi in una transazione per creare un indice senza informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="26a9e-145">The session must not currently be in a transaction to create an index without version information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="26a9e-146">IndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="26a9e-146">IndexSortNullsHigh</span></span></td>
<td><span data-ttu-id="26a9e-147">Se si specifica questo flag, i valori NULL verranno ordinati dopo i dati per tutte le colonne dell'indice.</span><span class="sxs-lookup"><span data-stu-id="26a9e-147">Specifying this flag causes NULL values to be sorted after data for all columns in the index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="26a9e-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26a9e-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="26a9e-149">Riferimento</span><span class="sxs-lookup"><span data-stu-id="26a9e-149">Reference</span></span>

[<span data-ttu-id="26a9e-150">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="26a9e-150">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
