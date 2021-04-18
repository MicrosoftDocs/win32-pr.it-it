---
description: 'Altre informazioni su: funzione JetIntersectIndexes'
title: Funzione JetIntersectIndexes
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305733"
---
# <a name="jetintersectindexes-function"></a><span data-ttu-id="a0b6a-103">Funzione JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="a0b6a-103">JetIntersectIndexes Function</span></span>


<span data-ttu-id="a0b6a-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a0b6a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetintersectindexes-function"></a><span data-ttu-id="a0b6a-105">Funzione JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="a0b6a-105">JetIntersectIndexes Function</span></span>

<span data-ttu-id="a0b6a-106">La funzione **JetIntersectIndexes** calcola l'intersezione tra più set di voci di indice provenienti da indici secondari diversi nella stessa tabella.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-106">The **JetIntersectIndexes** function computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="a0b6a-107">Questa operazione è utile per trovare il set di record in una tabella che corrisponde a due o più criteri che possono essere espressi utilizzando intervalli di indice.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-107">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span>

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a0b6a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0b6a-108">Parameters</span></span>

<span data-ttu-id="a0b6a-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a0b6a-109">*sesid*</span></span>

<span data-ttu-id="a0b6a-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-110">The session to use for this call.</span></span>

<span data-ttu-id="a0b6a-111">*rgindexrange*</span><span class="sxs-lookup"><span data-stu-id="a0b6a-111">*rgindexrange*</span></span>

<span data-ttu-id="a0b6a-112">Puntatore a una matrice di strutture di [JET_IndexRange](./jet-indexrange-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b6a-112">A pointer to an array of [JET_IndexRange](./jet-indexrange-structure.md) structures.</span></span> <span data-ttu-id="a0b6a-113">Ogni struttura include una [JET_TABLEID](./jet-tableid.md) configurata per contenere uno degli intervalli di indice da intersecare.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-113">Each structure includes a [JET_TABLEID](./jet-tableid.md) that has been set up to hold one of the index ranges to be intersected.</span></span> <span data-ttu-id="a0b6a-114">Per ulteriori informazioni, vedere [JET_IndexRange](./jet-indexrange-structure.md).</span><span class="sxs-lookup"><span data-stu-id="a0b6a-114">For more information, see [JET_IndexRange](./jet-indexrange-structure.md).</span></span>

<span data-ttu-id="a0b6a-115">*cindexrange*</span><span class="sxs-lookup"><span data-stu-id="a0b6a-115">*cindexrange*</span></span>

<span data-ttu-id="a0b6a-116">Numero di strutture di [JET_IndexRange](./jet-indexrange-structure.md) nella matrice contenuta nel parametro *rgindexrange* .</span><span class="sxs-lookup"><span data-stu-id="a0b6a-116">The number of [JET_IndexRange](./jet-indexrange-structure.md) structures in the array that is contained in the *rgindexrange* parameter.</span></span>

<span data-ttu-id="a0b6a-117">*precordore*</span><span class="sxs-lookup"><span data-stu-id="a0b6a-117">*precordlist*</span></span>

<span data-ttu-id="a0b6a-118">Puntatore a una struttura [JET_RECORDLIST](./jet-recordlist-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b6a-118">Pointer to a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="a0b6a-119">Questa struttura verrà popolata con informazioni sufficienti per attraversare la tabella temporanea con i risultati di **JetIntersectIndexes**.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-119">This structure will be populated with enough information to traverse the temporary table with the results from **JetIntersectIndexes**.</span></span>

<span data-ttu-id="a0b6a-120">Buffer di output che riceve una struttura [JET_RECORDLIST](./jet-recordlist-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b6a-120">The output buffer that receives a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="a0b6a-121">La struttura contiene una descrizione del set di risultati dell'intersezione.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-121">The structure contains a description of the result set of the intersection.</span></span>

<span data-ttu-id="a0b6a-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a0b6a-122">*grbit*</span></span>

<span data-ttu-id="a0b6a-123">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-123">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="a0b6a-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0b6a-124">Return Value</span></span>

<span data-ttu-id="a0b6a-125">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a0b6a-126">Per ulteriori informazioni sugli errori ESE, vedere [errori del motore di archiviazione estendibile](./extensible-storage-engine-errors.md) e [parametri di gestione degli](./error-handling-parameters.md)errori.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-126">For more information about ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0b6a-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a0b6a-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="a0b6a-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0b6a-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a0b6a-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-130">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b6a-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a0b6a-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-132">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a0b6a-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-134">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a0b6a-135"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-135"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b6a-136">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="a0b6a-136">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-137">Una delle opzioni richieste non è valida, è stata usata in modo errato o non è stata implementata.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-137">One of the options requested was invalid, used incorrectly, or not implemented.</span></span></p>
<p><span data-ttu-id="a0b6a-138">Questo errore viene restituito da <strong>JetIntersectIndexes</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="a0b6a-138">This error is returned by <strong>JetIntersectIndexes</strong> when:</span></span></p>
<p><span data-ttu-id="a0b6a-139">Il <em>grbit</em> contenuto nella struttura <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> a cui punta qualsiasi elemento nella matrice <em>rgindexrange</em> non è uguale a JET_bitRecordInIndex.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-139">The <em>grbit</em> contained in the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure pointed to by any element in the <em>rgindexrange</em> array is not equal to JET_bitRecordInIndex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-140">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a0b6a-140">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-141">Uno dei parametri forniti contiene un valore imprevisto o un valore non coerente se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-141">One of the parameters provided contains an unexpected value or a value that is inconsistent when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="a0b6a-142">Questo errore viene restituito da <strong>JetIntersectIndexes</strong> per i motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0b6a-142">This error is returned by <strong>JetIntersectIndexes</strong> for of the following reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="a0b6a-143">Il parametro <em>precordname</em> è null.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-143">The <em>precordlist</em> parameter is NULL.</span></span></p></li>
<li><p><span data-ttu-id="a0b6a-144">Il membro <strong>cbStruct</strong> della struttura <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> specificata nel parametro <em>precordon</em> non è uguale alla dimensione della struttura di <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="a0b6a-144">The <strong>cbStruct</strong> member of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure specified in the <em>precordlist</em> parameter is not equal to size of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="a0b6a-145">Il parametro <em>cindexrange</em> è zero.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-145">The <em>cindexrange</em> parameter is zero.</span></span></p></li>
<li><p><span data-ttu-id="a0b6a-146">Il parametro <em>cindexrange</em> è maggiore di 64.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-146">The <em>cindexrange</em> parameter is greater than 64.</span></span></p></li>
<li><p><span data-ttu-id="a0b6a-147">Il membro <strong>cbStruct</strong> per qualsiasi elemento nella matrice specificata dal parametro <em>rgindexrange</em> non è uguale alla dimensione della struttura <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> .</span><span class="sxs-lookup"><span data-stu-id="a0b6a-147">The <strong>cbStruct</strong> member for any element in the array specified by the <em>rgindexrange</em> parameter is not equal to the size of the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="a0b6a-148">Gli elementi nella matrice <em>rgindexrange</em> contengono <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s da tabelle diverse.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-148">The elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s from different tables.</span></span></p></li>
<li><p><span data-ttu-id="a0b6a-149">Un elemento nella matrice <em>rgindexrange</em> contiene un <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> che non è posizionato in corrispondenza di un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-149">An element in the <em>rgindexrange</em> array contains a <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> that is not positioned on a secondary index.</span></span></p></li>
<li><p><span data-ttu-id="a0b6a-150">Uno o più elementi nella matrice <em>rgindexrange</em> contengono <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s posizionati nello stesso indice secondario.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-150">One or more of the elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s positioned on the same secondary index.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b6a-151">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="a0b6a-151">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-152">L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-152">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="a0b6a-153">Questo errore non viene restituito in tutte le circostanze.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-153">This error is not returned under all circumstances.</span></span> <span data-ttu-id="a0b6a-154">Gli handle vengono convalidati solo in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-154">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-155">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a0b6a-155">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-156">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-156">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b6a-157">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="a0b6a-157">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-158">Operazione non riuscita perché il motore non è stato in grado di allocare le risorse necessarie per aprire un nuovo cursore.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-158">The operation failed because the engine could not allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="a0b6a-159">Le risorse del cursore vengono configurate chiamando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxCursors</em> specificato nel parametro <em>Paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="a0b6a-159">Cursor resources are configured by calling <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxCursors</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a0b6a-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-161">L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="a0b6a-162"><strong>JetIntersectIndexes</strong> può restituire JET_errOutOfMemory se lo spazio degli indirizzi del processo host diventa troppo frammentato.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-162"><strong>JetIntersectIndexes</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="a0b6a-163">Il gestore tabelle temporanee allocherà sempre un blocco di spazio degli indirizzi pari a 1 MB per ogni tabella temporanea creata indipendentemente dalla quantità di dati da archiviare.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-163">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span> <span data-ttu-id="a0b6a-164"><strong>JetIntersectIndexes</strong> creerà una tabella temporanea per ogni <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> specificato nel parametro <em>rgindexrange</em> e una tabella temporanea per l'output in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-164"><strong>JetIntersectIndexes</strong> will create one temporary table for each <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> specified in the <em>rgindexrange</em> parameter, and one temporary table for the output in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b6a-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a0b6a-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-166">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a0b6a-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-168">Non è consentito usare la stessa sessione da più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-168">It is illegal to use the same session from more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a0b6a-169"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-169"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b6a-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a0b6a-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-171">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-172">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="a0b6a-172">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-173">L'operazione non è riuscita perché il motore non è stato in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-173">The operation failed because the engine could not allocate the resources required to cache the indices of the table.</span></span> <span data-ttu-id="a0b6a-174">Il numero di indici il cui schema può essere memorizzato nella cache viene configurato usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxOpenTables</em> specificato nel parametro <em>Paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="a0b6a-174">The number of indices whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b6a-175">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="a0b6a-175">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-176">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-176">The operation failed because the engine could not allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="a0b6a-177">Il numero di tabelle il cui schema può essere memorizzato nella cache viene configurato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxOpenTables</em> specificato nel parametro <em>Paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="a0b6a-177">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-178">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="a0b6a-178">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="a0b6a-179">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-179">The operation failed because the engine could not allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="a0b6a-180">Le risorse della tabella temporanea vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con JET_paramMaxTemporaryTables specificato nel parametro <em>Paramid</em> .</span><span class="sxs-lookup"><span data-stu-id="a0b6a-180">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with JET_paramMaxTemporaryTables specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0b6a-181">In seguito all'esito positivo, viene restituita una nuova tabella temporanea che contiene i segnalibri dei record che corrispondono ai criteri rappresentati da ognuna delle descrizioni degli intervalli degli indici di input.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-181">On success, a new temporary table is returned that contains the bookmarks of the records that match the criteria represented by each of the input index range descriptions.</span></span>

<span data-ttu-id="a0b6a-182">In caso di errore, la tabella temporanea contenente i risultati non verrà creata.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-182">On failure, the temporary table containing the results will not be created.</span></span> <span data-ttu-id="a0b6a-183">Lo stato del database temporaneo può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-183">The state of the temporary database may be changed.</span></span> <span data-ttu-id="a0b6a-184">Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-184">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span> <span data-ttu-id="a0b6a-185">È possibile modificare la posizione corrente del [JET_TABLEID](./jet-tableid.md)s fornita a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-185">The current position of the [JET_TABLEID](./jet-tableid.md)s provided to this function may be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a0b6a-186">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0b6a-186">Remarks</span></span>

<span data-ttu-id="a0b6a-187">**JetIntersectIndexes** può essere usato per filtrare in modo efficiente i record in una tabella in base a più criteri se tali criteri possono essere espressi in termini di indici secondari sulla tabella.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-187">**JetIntersectIndexes** can be used to efficiently filter the records in a table by multiple criteria if those criteria can be expressed in terms of the secondary indices over that table.</span></span> <span data-ttu-id="a0b6a-188">Si supponga, ad esempio, di disporre di una tabella di grandi dimensioni contenente persone.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-188">For example, consider that you have a very large table containing people.</span></span> <span data-ttu-id="a0b6a-189">La tabella può includere colonne per l'ID utente, il nome, il cognome e così via.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-189">The table can have columns for their user id, first name, last name, and so on.</span></span> <span data-ttu-id="a0b6a-190">Si supponga che ciascuna di queste colonne venga indicizzata separatamente e che l'indice primario della tabella sia superiore all'ID utente. Se si desidera trovare tutti gli utenti il cui nome inizia con un oggetto e il cui cognome inizia con G, è necessario eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0b6a-190">Suppose that each of these columns is indexed separately and that the primary index of the table is over user id. If you wanted to find everyone whose first name starts with an A and whose last name starts with G, you would perform the following steps:</span></span>

1.  <span data-ttu-id="a0b6a-191">Aprire un nuovo cursore sulla tabella e impostare tale cursore per utilizzare l'indice sulla colonna "First Name".</span><span class="sxs-lookup"><span data-stu-id="a0b6a-191">Open a new cursor on the table, and set that cursor to use the index over the "first name" column.</span></span> <span data-ttu-id="a0b6a-192">Configurare quindi un intervallo di indici per tutte le persone il cui "nome" inizia con "A" e compilare un [JET_IndexRange](./jet-indexrange-structure.md) struct che contiene il cursore.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-192">Then setup an index range for all people whose "first name" started with 'A', and build a [JET_IndexRange](./jet-indexrange-structure.md) struct that contains this cursor.</span></span>

2.  <span data-ttu-id="a0b6a-193">Ripetere il passaggio 1 con un nuovo cursore sull'indice "Last Name" per tutte le persone il cui "cognome" è stato avviato con "G".</span><span class="sxs-lookup"><span data-stu-id="a0b6a-193">Repeat step 1 with a new cursor on the "last name" index for all people whose "last name" started with 'G'.</span></span>

3.  <span data-ttu-id="a0b6a-194">Passare questi criteri a **JetIntersectIndexes** per calcolare il risultato in una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-194">Pass these criteria to **JetIntersectIndexes** to compute the result into a temporary table.</span></span>

4.  <span data-ttu-id="a0b6a-195">Attraversare la tabella temporanea e recuperare tutti i record che passano i criteri tramite segnalibro.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-195">Traverse the temporary table and retrieve each of the records that pass the criteria by bookmark.</span></span>

<span data-ttu-id="a0b6a-196">La tabella temporanea contenente il set di risultati è una tabella semplice con una colonna che contiene il segnalibro di ogni record che ha superato tutti i criteri utilizzati per calcolare l'intersezione.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-196">The temporary table containing the result set is a simple table with one column that contains the bookmark of each record that passed all the criteria used to compute the intersection.</span></span> <span data-ttu-id="a0b6a-197">Il set di risultati viene ordinato in base allo stesso ordine dell'indice primario e non contiene voci duplicate.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-197">The result set is sorted in the same order as the primary index and contains no duplicate entries.</span></span> <span data-ttu-id="a0b6a-198">L'applicazione può enumerare i risultati dell'intersezione enumerando le righe nella tabella temporanea, recuperando il segnalibro per ogni risultato utilizzando [JetRetrieveColumn](./jetretrievecolumn-function.md)e quindi visitando il record nel database chiamando [JetGotoBookmark](./jetgotobookmark-function.md) con tale segnalibro su un cursore posizionato sull'indice primario.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-198">The application can enumerate the results of the intersection by enumerating the rows in the temporary table, retrieving the bookmark for each result using [JetRetrieveColumn](./jetretrievecolumn-function.md), and then visiting the record in the database by calling [JetGotoBookmark](./jetgotobookmark-function.md) with that bookmark on a cursor positioned on the primary index.</span></span>

<span data-ttu-id="a0b6a-199">La tabella temporanea restituita da **JetIntersectIndexes** può essere analizzata solo in avanti.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-199">The temporary table returned by **JetIntersectIndexes** can only be scanned in a forward direction.</span></span> <span data-ttu-id="a0b6a-200">Deve anche essere chiuso tramite [JetCloseTable](./jetclosetable-function.md) al termine dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-200">It should also be closed via [JetCloseTable](./jetclosetable-function.md) when the scan has been completed.</span></span> <span data-ttu-id="a0b6a-201">Per ulteriori informazioni sulle tabelle temporanee e sul relativo funzionamento, vedere [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="a0b6a-201">For more information about temporary tables and how they work, see [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

<span data-ttu-id="a0b6a-202">**JetIntersectIndexes** è in genere un modo efficiente e pratico per filtrare i record in base a più criteri indicizzati.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-202">**JetIntersectIndexes** is generally an efficient and convenient way to filter records based on multiple indexed criteria.</span></span> <span data-ttu-id="a0b6a-203">Tuttavia, esistono alcuni suggerimenti importanti da seguire per ottimizzare l'utilità di questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-203">However, there are some important tips that should be followed to maximize the usefulness of this feature.</span></span> <span data-ttu-id="a0b6a-204">Se si sa che uno dei criteri è talmente restrittivo che l'intervallo di indici risultante ha pochissimi record, probabilmente è preferibile semplicemente esaminare l'intervallo di indici e filtrare i record a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-204">If you know that one of the criteria is so restrictive that the resulting index range has very few records then it is probably better to simply walk that index range and filter the records at the application level.</span></span> <span data-ttu-id="a0b6a-205">Inoltre, se si è certi di disporre di criteri molto meno restrittivi rispetto ad altri criteri nell'intersezione, è possibile prendere in considerazione l'eliminazione di criteri molto meno restrittivi dall'intersezione.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-205">Further, if you know that you have criteria that are much less restrictive than other criteria in your intersection then you might consider dropping those much less restrictive criteria from the intersection.</span></span> <span data-ttu-id="a0b6a-206">Infine, se si sa che uno dei criteri non è strettamente restrittivo, in modo che l'intervallo di indici risultante sia quasi così elevato rispetto all'indice primario, è improbabile che l'intersezione con tale intervallo possa trarre vantaggio (ridurre le dimensioni del set di risultati).</span><span class="sxs-lookup"><span data-stu-id="a0b6a-206">Finally, if you know that one of the criteria is not at all restrictive such that the resulting index range is almost as large as the primary index then it is unlikely that intersecting with that index range will benefit (reduce the size of) the result set.</span></span> <span data-ttu-id="a0b6a-207">In tutti i casi, è necessario selezionare i criteri in modo che consentano il minor numero possibile di voci di indice nell'input e generano il set più specifico di segnalibri nell'output per ottenere le massime prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-207">In all cases, you should be selecting criteria in a manner that will take the fewest possible index entries on input and generate the most specific set of bookmarks on output for maximum performance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a0b6a-208">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0b6a-208">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-209"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a0b6a-209"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a0b6a-210">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-210">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b6a-211"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a0b6a-211"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a0b6a-212">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-212">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-213"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="a0b6a-213"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a0b6a-214">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-214">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0b6a-215"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="a0b6a-215"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a0b6a-216">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-216">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0b6a-217"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a0b6a-217"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a0b6a-218">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a0b6a-218">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a0b6a-219">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a0b6a-219">See Also</span></span>

[<span data-ttu-id="a0b6a-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a0b6a-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a0b6a-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a0b6a-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a0b6a-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a0b6a-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a0b6a-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a0b6a-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a0b6a-224">JET_IndexRange</span><span class="sxs-lookup"><span data-stu-id="a0b6a-224">JET_IndexRange</span></span>](./jet-indexrange-structure.md)  
[<span data-ttu-id="a0b6a-225">JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="a0b6a-225">JET_RECORDLIST</span></span>](./jet-recordlist-structure.md)  
[<span data-ttu-id="a0b6a-226">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="a0b6a-226">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="a0b6a-227">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="a0b6a-227">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="a0b6a-228">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="a0b6a-228">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
