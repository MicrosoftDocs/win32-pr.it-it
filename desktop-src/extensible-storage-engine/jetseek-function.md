---
description: 'Altre informazioni su: funzione JetSeek'
title: JetSeek (funzione)
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318082"
---
# <a name="jetseek-function"></a><span data-ttu-id="b8235-103">JetSeek (funzione)</span><span class="sxs-lookup"><span data-stu-id="b8235-103">JetSeek Function</span></span>


<span data-ttu-id="b8235-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b8235-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetseek-function"></a><span data-ttu-id="b8235-105">JetSeek (funzione)</span><span class="sxs-lookup"><span data-stu-id="b8235-105">JetSeek Function</span></span>

<span data-ttu-id="b8235-106">La funzione **JetSeek** posiziona in modo efficiente un cursore in una voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e alla disuguaglianza specificata.</span><span class="sxs-lookup"><span data-stu-id="b8235-106">The **JetSeek** function efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="b8235-107">È necessario che una chiave di ricerca sia stata costruita in precedenza usando [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="b8235-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b8235-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8235-108">Parameters</span></span>

<span data-ttu-id="b8235-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b8235-109">*sesid*</span></span>

<span data-ttu-id="b8235-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="b8235-110">The session to use for this call.</span></span>

<span data-ttu-id="b8235-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="b8235-111">*tableid*</span></span>

<span data-ttu-id="b8235-112">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="b8235-112">The cursor to use for this call.</span></span>

<span data-ttu-id="b8235-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b8235-113">*grbit*</span></span>

<span data-ttu-id="b8235-114">Gruppo di bit che contiene le opzioni da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="b8235-114">A group of bits that contain the options to be used for this call.</span></span> <span data-ttu-id="b8235-115">*Grbit* deve essere diverso da zero e deve includere uno o più dei valori elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b8235-115">*Grbit* must be nonzero and must include one or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8235-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b8235-116">Value</span></span></p></th>
<th><p><span data-ttu-id="b8235-117">Significato</span><span class="sxs-lookup"><span data-stu-id="b8235-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8235-118">JET_bitCheckUniqueness</span><span class="sxs-lookup"><span data-stu-id="b8235-118">JET_bitCheckUniqueness</span></span></p></td>
<td><p><span data-ttu-id="b8235-119">Viene restituito un codice di errore speciale, JET_wrnUniqueKey, se può essere determinato in modo economico che esiste esattamente una voce di indice che corrisponde alla chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-119">A special error code, JET_wrnUniqueKey, will be returned if it can be cheaply determined that there is exactly one index entry that matches the search key.</span></span></p>
<p><span data-ttu-id="b8235-120">Questa opzione viene ignorata a meno che non sia specificato anche JET_bitSeekEQ.</span><span class="sxs-lookup"><span data-stu-id="b8235-120">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p>
<p><span data-ttu-id="b8235-121">Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b8235-121">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8235-122">JET_bitSeekEQ</span><span class="sxs-lookup"><span data-stu-id="b8235-122">JET_bitSeekEQ</span></span></p></td>
<td><p><span data-ttu-id="b8235-123">Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice che corrisponde esattamente alla chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-123">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span> <span data-ttu-id="b8235-124">L'inizio dell'indice è la voce di indice trovata quando si passa al primo record in tale indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-124">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="b8235-125">L'inizio dell'indice non corrisponde alla parte inferiore dell'indice, che può variare a seconda del tipo di ordinamento delle colonne chiave nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-125">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="b8235-126">Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="b8235-126">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8235-127">JET_bitSeekGE</span><span class="sxs-lookup"><span data-stu-id="b8235-127">JET_bitSeekGE</span></span></p></td>
<td><p><span data-ttu-id="b8235-128">Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice che è maggiore o uguale a una voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-128">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="b8235-129">L'inizio dell'indice è la voce di indice trovata quando si passa al primo record in tale indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-129">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="b8235-130">L'inizio dell'indice non corrisponde alla parte inferiore dell'indice, che può variare a seconda del tipo di ordinamento delle colonne chiave nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-130">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="b8235-131">Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine alla fine dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-131">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8235-132">JET_bitSeekGT</span><span class="sxs-lookup"><span data-stu-id="b8235-132">JET_bitSeekGT</span></span></p></td>
<td><p><span data-ttu-id="b8235-133">Il cursore verrà posizionato in corrispondenza della voce di indice più vicina all'inizio dell'indice maggiore di una voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-133">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="b8235-134">L'inizio dell'indice è la voce di indice trovata quando si passa al primo record in tale indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-134">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="b8235-135">L'inizio dell'indice non corrisponde alla parte inferiore dell'indice, che può variare a seconda del tipo di ordinamento delle colonne chiave nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-135">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="b8235-136">Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine all'inizio dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-136">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8235-137">JET_bitSeekLE</span><span class="sxs-lookup"><span data-stu-id="b8235-137">JET_bitSeekLE</span></span></p></td>
<td><p><span data-ttu-id="b8235-138">Il cursore verrà posizionato in corrispondenza della voce di indice più vicina alla fine dell'indice che è minore o uguale a una voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-138">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="b8235-139">La fine dell'indice è la voce di indice trovata quando si passa all'ultimo record in tale indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-139">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="b8235-140">La fine dell'indice non è uguale all'estremità superiore dell'indice, che può variare a seconda dell'ordinamento delle colonne chiave nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-140">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="b8235-141">Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine all'inizio dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-141">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8235-142">JET_bitSeekLT</span><span class="sxs-lookup"><span data-stu-id="b8235-142">JET_bitSeekLT</span></span></p></td>
<td><p><span data-ttu-id="b8235-143">Il cursore verrà posizionato in corrispondenza della voce di indice più vicina alla fine dell'indice inferiore a una voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-143">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="b8235-144">La fine dell'indice è la voce di indice trovata quando si passa all'ultimo record in tale indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-144">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="b8235-145">La fine dell'indice non è uguale all'estremità superiore dell'indice, che può variare a seconda dell'ordinamento delle colonne chiave nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-145">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="b8235-146">Non è significativo usare questa opzione con una chiave di ricerca costruita usando <a href="gg269329(v=exchg.10).md">JetMakeKey</a> usando un'opzione con caratteri jolly per trovare le voci di indice più vicine alla fine dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-146">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8235-147">JET_bitSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b8235-147">JET_bitSetIndexRange</span></span></p></td>
<td><p><span data-ttu-id="b8235-148">Un intervallo di indici verrà automaticamente configurato per tutte le chiavi che corrispondono esattamente alla chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-148">An index range will automatically be setup for all keys that exactly match the search key.</span></span> <span data-ttu-id="b8235-149">L'intervallo di indici risultante è identico a uno che altrimenti sarebbe stato creato da una chiamata a <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> con le opzioni JET_bitRangeInclusive e JET_bitRangeUpperLimit.</span><span class="sxs-lookup"><span data-stu-id="b8235-149">The resulting index range is identical to one that would have otherwise been created by a call to <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> with the JET_bitRangeInclusive and JET_bitRangeUpperLimit options.</span></span> <span data-ttu-id="b8235-150">Per ulteriori informazioni, vedere <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> .</span><span class="sxs-lookup"><span data-stu-id="b8235-150">See <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> for more information.</span></span></p>
<p><span data-ttu-id="b8235-151">Si tratta di un metodo pratico per individuare tutte le voci di indice che corrispondono agli stessi criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-151">This is a convenient method for discovering all the index entries that match the same search criteria.</span></span></p>
<p><span data-ttu-id="b8235-152">Questa opzione viene ignorata a meno che non sia specificato anche JET_bitSeekEQ.</span><span class="sxs-lookup"><span data-stu-id="b8235-152">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b8235-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8235-153">Return Value</span></span>

<span data-ttu-id="b8235-154">Questa funzione consente il ritorno di qualsiasi [JET_ERRs](./jet-err.md) definito in questa API.</span><span class="sxs-lookup"><span data-stu-id="b8235-154">This function allows for the return of any [JET_ERRs](./jet-err.md) that are defined in this API.</span></span> <span data-ttu-id="b8235-155">Per altre informazioni sugli errori di Jet, vedere [errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md) e [parametri di gestione degli](./error-handling-parameters.md)errori.</span><span class="sxs-lookup"><span data-stu-id="b8235-155">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8235-156">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b8235-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="b8235-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8235-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8235-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b8235-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b8235-159">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="b8235-159">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="b8235-160">Per <strong>JetSeek</strong>, ciò significa che è stata trovata una voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-160">For <strong>JetSeek</strong>, this means that an index entry was found that exactly matched the search criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8235-161">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b8235-161">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b8235-162">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b8235-162">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8235-163">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b8235-163">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b8235-164">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="b8235-164">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="b8235-165">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b8235-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8235-166">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="b8235-166">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="b8235-167">Nessun tasto di ricerca corrente per il cursore.</span><span class="sxs-lookup"><span data-stu-id="b8235-167">There is no current search key for the cursor.</span></span> <span data-ttu-id="b8235-168"><strong>JetSeek</strong> richiede che il cursore disponga di una chiave di ricerca valida perché verrà utilizzata per i criteri di ricerca utilizzati per individuare le voci dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8235-168"><strong>JetSeek</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8235-169">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b8235-169">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b8235-170">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="b8235-170">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8235-171">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="b8235-171">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="b8235-172">Non è stata trovata alcuna voce di indice corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-172">No index entry was found that matched the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8235-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b8235-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b8235-174">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="b8235-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8235-175">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="b8235-175">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="b8235-176">È stata trovata una voce di indice corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-176">An index entry was found that matched the search criteria.</span></span> <span data-ttu-id="b8235-177">Tale voce di indice, tuttavia, non era una corrispondenza esatta.</span><span class="sxs-lookup"><span data-stu-id="b8235-177">However, that index entry was not an exact match.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8235-178">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b8235-178">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b8235-179">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="b8235-179">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="b8235-180">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b8235-180">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8235-181">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b8235-181">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b8235-182">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="b8235-182">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8235-183">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="b8235-183">JET_wrnUniqueKey</span></span></p></td>
<td><p><span data-ttu-id="b8235-184">È stata trovata esattamente una voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-184">Exactly one index entry was found that exactly matched the search criteria.</span></span> <span data-ttu-id="b8235-185">Questo errore viene restituito solo se JET_bitSeekCheckUniqueness è stato specificato ed è stato economico determinare che la voce di indice corrispondente era l'unica voce di indice che corrisponde esattamente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-185">This error will only be returned if JET_bitSeekCheckUniqueness was specified and it was cheap to determine that the matching index entry was the only index entry that exactly matches the search criteria.</span></span></p>
<p><span data-ttu-id="b8235-186">Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b8235-186">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b8235-187">In seguito all'esito positivo, il cursore verrà posizionato in corrispondenza di una voce di indice corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b8235-187">On success, the cursor will be positioned at an index entry that matches the search criteria.</span></span> <span data-ttu-id="b8235-188">Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="b8235-188">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="b8235-189">Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="b8235-189">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="b8235-190">Se è stata creata una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="b8235-190">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="b8235-191">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="b8235-191">No change to the database state will occur.</span></span> <span data-ttu-id="b8235-192">Quando più voci di indice hanno lo stesso valore, la voce più vicina all'inizio dell'indice è sempre selezionata.</span><span class="sxs-lookup"><span data-stu-id="b8235-192">When multiple index entries have the same value, the entry closest to the start of the index is always selected.</span></span>

<span data-ttu-id="b8235-193">In caso di errore, la posizione del cursore rimarrà invariata a meno che non venga restituito JET_errRecordNotFound.</span><span class="sxs-lookup"><span data-stu-id="b8235-193">On failure, the position of the cursor will remain unchanged unless JET_errRecordNotFound was returned.</span></span> <span data-ttu-id="b8235-194">In tal caso, il cursore verrà posizionato in corrispondenza del punto in cui la voce di indice corrispondente ai criteri di ricerca specificati dalla chiave di ricerca nel cursore e nella disuguaglianza specificata sarebbe stata.</span><span class="sxs-lookup"><span data-stu-id="b8235-194">In that case, the cursor will be positioned where the index entry that matched the search criteria specified by the search key in that cursor and the specified inequality would have been.</span></span> <span data-ttu-id="b8235-195">Il cursore può essere spostato in relazione a tale posizione, ma non è ancora presente in una voce di indice valida.</span><span class="sxs-lookup"><span data-stu-id="b8235-195">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="b8235-196">Se un record è stato preparato per l'aggiornamento, l'aggiornamento verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="b8235-196">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="b8235-197">Se è attivo un intervallo di indici, l'intervallo di indici verrà annullato.</span><span class="sxs-lookup"><span data-stu-id="b8235-197">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="b8235-198">Se è stata creata una chiave di ricerca per il cursore, la chiave di ricerca verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="b8235-198">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="b8235-199">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="b8235-199">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b8235-200">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8235-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8235-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b8235-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b8235-202">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b8235-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8235-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b8235-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b8235-204">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b8235-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8235-205"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b8235-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b8235-206">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b8235-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8235-207"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="b8235-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b8235-208">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b8235-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8235-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b8235-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b8235-210">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b8235-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b8235-211">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b8235-211">See Also</span></span>

[<span data-ttu-id="b8235-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b8235-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b8235-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b8235-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b8235-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b8235-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b8235-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b8235-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b8235-216">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b8235-216">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="b8235-217">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b8235-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="b8235-218">JetStopService</span><span class="sxs-lookup"><span data-stu-id="b8235-218">JetStopService</span></span>](./jetstopservice-function.md)
