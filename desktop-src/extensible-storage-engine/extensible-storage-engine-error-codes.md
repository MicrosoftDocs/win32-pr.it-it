---
description: 'Altre informazioni su: codici di errore Extensible Storage Engine'
title: Codici di errore di Extensible Storage Engine
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317417"
---
# <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="171e1-103">Codici di errore di Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="171e1-103">Extensible Storage Engine Error Codes</span></span>


<span data-ttu-id="171e1-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="171e1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-error-codes"></a><span data-ttu-id="171e1-105">Codici di errore di Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="171e1-105">Extensible Storage Engine Error Codes</span></span>

<span data-ttu-id="171e1-106">I codici di errore (flag) seguenti vengono usati dalle funzioni nell'API del motore di archiviazione estendibile.</span><span class="sxs-lookup"><span data-stu-id="171e1-106">The following error codes (flags) are used by functions in the Extensible Storage Engine API.</span></span>

<span data-ttu-id="171e1-107">Un [JET_ERR](./jet-err.md) valore pari a zero deve essere interpretato come operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="171e1-107">A [JET_ERR](./jet-err.md) value of zero should be interpreted as success.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="171e1-108">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="171e1-108">Success</span></span></p></th>
<th><p><span data-ttu-id="171e1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="171e1-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="171e1-110">JET_errSuccess 0</span><span class="sxs-lookup"><span data-stu-id="171e1-110">JET_errSuccess 0</span></span></p></td>
<td><p><span data-ttu-id="171e1-111">Funzione completata.</span><span class="sxs-lookup"><span data-stu-id="171e1-111">The function succeeded.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="171e1-112">Un valore [JET_ERR](./jet-err.md) maggiore di zero deve essere interpretato come un avviso.</span><span class="sxs-lookup"><span data-stu-id="171e1-112">A [JET_ERR](./jet-err.md) value that is greater than zero should be interpreted as a warning.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="171e1-113">Avvisi</span><span class="sxs-lookup"><span data-stu-id="171e1-113">Warnings</span></span></p></th>
<th><p><span data-ttu-id="171e1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="171e1-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="171e1-115">JET_wrnRemainingVersions</span><span class="sxs-lookup"><span data-stu-id="171e1-115">JET_wrnRemainingVersions</span></span><br />
<span data-ttu-id="171e1-116">321</span><span class="sxs-lookup"><span data-stu-id="171e1-116">321</span></span></p></td>
<td><p><span data-ttu-id="171e1-117">L'archivio versione è ancora attivo.</span><span class="sxs-lookup"><span data-stu-id="171e1-117">The version store is still active.</span></span> <span data-ttu-id="171e1-118">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-118">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-119">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="171e1-119">JET_wrnUniqueKey</span></span><br />
<span data-ttu-id="171e1-120">345</span><span class="sxs-lookup"><span data-stu-id="171e1-120">345</span></span></p></td>
<td><p><span data-ttu-id="171e1-121">Una ricerca in un indice non univoco ha restituito una chiave univoca.</span><span class="sxs-lookup"><span data-stu-id="171e1-121">A seek on a non-unique index yielded a unique key.</span></span> <span data-ttu-id="171e1-122">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-122">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-123">JET_wrnSeparateLongValue</span><span class="sxs-lookup"><span data-stu-id="171e1-123">JET_wrnSeparateLongValue</span></span><br />
<span data-ttu-id="171e1-124">406</span><span class="sxs-lookup"><span data-stu-id="171e1-124">406</span></span></p></td>
<td><p><span data-ttu-id="171e1-125">Una colonna di database è un valore Long separato.</span><span class="sxs-lookup"><span data-stu-id="171e1-125">A database column is a separated long value.</span></span> <span data-ttu-id="171e1-126">Questo errore viene restituito da Gestione record.</span><span class="sxs-lookup"><span data-stu-id="171e1-126">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-127">JET_wrnExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="171e1-127">JET_wrnExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="171e1-128">558</span><span class="sxs-lookup"><span data-stu-id="171e1-128">558</span></span></p></td>
<td><p><span data-ttu-id="171e1-129">Firma non valida per il file di log esistente.</span><span class="sxs-lookup"><span data-stu-id="171e1-129">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-130">JET_wrnExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="171e1-130">JET_wrnExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="171e1-131">559</span><span class="sxs-lookup"><span data-stu-id="171e1-131">559</span></span></p></td>
<td><p><span data-ttu-id="171e1-132">Il file di log esistente non è contiguo.</span><span class="sxs-lookup"><span data-stu-id="171e1-132">The existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-133">JET_wrnSkipThisRecord</span><span class="sxs-lookup"><span data-stu-id="171e1-133">JET_wrnSkipThisRecord</span></span><br />
<span data-ttu-id="171e1-134">564</span><span class="sxs-lookup"><span data-stu-id="171e1-134">564</span></span></p></td>
<td><p><span data-ttu-id="171e1-135">Questo errore è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="171e1-135">This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-136">JET_wrnTargetInstanceRunning</span><span class="sxs-lookup"><span data-stu-id="171e1-136">JET_wrnTargetInstanceRunning</span></span><br />
<span data-ttu-id="171e1-137">578</span><span class="sxs-lookup"><span data-stu-id="171e1-137">578</span></span></p></td>
<td><p><span data-ttu-id="171e1-138">Il TargetInstance specificato per il ripristino è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="171e1-138">The TargetInstance specified for the restore is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-139">JET_wrnDatabaseRepaired</span><span class="sxs-lookup"><span data-stu-id="171e1-139">JET_wrnDatabaseRepaired</span></span><br />
<span data-ttu-id="171e1-140">595</span><span class="sxs-lookup"><span data-stu-id="171e1-140">595</span></span></p></td>
<td><p><span data-ttu-id="171e1-141">Il danneggiamento del database è stato ripristinato.</span><span class="sxs-lookup"><span data-stu-id="171e1-141">The database corruption has been repaired.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-142">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="171e1-142">JET_wrnColumnNull</span></span><br />
<span data-ttu-id="171e1-143">1004</span><span class="sxs-lookup"><span data-stu-id="171e1-143">1004</span></span></p></td>
<td><p><span data-ttu-id="171e1-144">Il valore della colonna è <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="171e1-144">The column has a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-145">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="171e1-145">JET_wrnBufferTruncated</span></span><br />
<span data-ttu-id="171e1-146">1006</span><span class="sxs-lookup"><span data-stu-id="171e1-146">1006</span></span></p></td>
<td><p><span data-ttu-id="171e1-147">Il buffer è troppo piccolo per i dati.</span><span class="sxs-lookup"><span data-stu-id="171e1-147">The buffer is too small for the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-148">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="171e1-148">JET_wrnDatabaseAttached</span></span><br />
<span data-ttu-id="171e1-149">1007</span><span class="sxs-lookup"><span data-stu-id="171e1-149">1007</span></span></p></td>
<td><p><span data-ttu-id="171e1-150">Il database è già collegato.</span><span class="sxs-lookup"><span data-stu-id="171e1-150">The database is already attached.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-151">JET_wrnSortOverflow</span><span class="sxs-lookup"><span data-stu-id="171e1-151">JET_wrnSortOverflow</span></span><br />
<span data-ttu-id="171e1-152">1009</span><span class="sxs-lookup"><span data-stu-id="171e1-152">1009</span></span></p></td>
<td><p><span data-ttu-id="171e1-153">L'ordinamento che si sta tentando non dispone di memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="171e1-153">The sort that is being attempted does not have enough memory to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-154">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="171e1-154">JET_wrnSeekNotEqual</span></span><br />
<span data-ttu-id="171e1-155">1039</span><span class="sxs-lookup"><span data-stu-id="171e1-155">1039</span></span></p></td>
<td><p><span data-ttu-id="171e1-156">Non è stata trovata una corrispondenza esatta durante una ricerca.</span><span class="sxs-lookup"><span data-stu-id="171e1-156">An exact match was not found during a seek.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-157">JET_wrnRecordFoundGreater</span><span class="sxs-lookup"><span data-stu-id="171e1-157">JET_wrnRecordFoundGreater</span></span><br />
<span data-ttu-id="171e1-158">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="171e1-158">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="171e1-159">Non è stata trovata una corrispondenza esatta durante una ricerca.</span><span class="sxs-lookup"><span data-stu-id="171e1-159">An exact match was not found during a seek.</span></span> <span data-ttu-id="171e1-160">Questo errore viene restituito da Gestione record.</span><span class="sxs-lookup"><span data-stu-id="171e1-160">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-161">JET_wrnRecordFoundLess</span><span class="sxs-lookup"><span data-stu-id="171e1-161">JET_wrnRecordFoundLess</span></span><br />
<span data-ttu-id="171e1-162">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="171e1-162">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="171e1-163">Non è stata trovata una corrispondenza esatta durante una ricerca.</span><span class="sxs-lookup"><span data-stu-id="171e1-163">An exact match was not found during a seek.</span></span> <span data-ttu-id="171e1-164">Questo errore viene restituito da Gestione record.</span><span class="sxs-lookup"><span data-stu-id="171e1-164">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-165">JET_wrnNoErrorInfo</span><span class="sxs-lookup"><span data-stu-id="171e1-165">JET_wrnNoErrorInfo</span></span><br />
<span data-ttu-id="171e1-166">1055</span><span class="sxs-lookup"><span data-stu-id="171e1-166">1055</span></span></p></td>
<td><p><span data-ttu-id="171e1-167">Non sono presenti informazioni estese sull'errore.</span><span class="sxs-lookup"><span data-stu-id="171e1-167">There is no extended error information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-168">JET_wrnNoIdleActivity</span><span class="sxs-lookup"><span data-stu-id="171e1-168">JET_wrnNoIdleActivity</span></span><br />
<span data-ttu-id="171e1-169">1058</span><span class="sxs-lookup"><span data-stu-id="171e1-169">1058</span></span></p></td>
<td><p><span data-ttu-id="171e1-170">Non è stata eseguita alcuna attività inattiva.</span><span class="sxs-lookup"><span data-stu-id="171e1-170">No idle activity occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-171">JET_wrnNoWriteLock</span><span class="sxs-lookup"><span data-stu-id="171e1-171">JET_wrnNoWriteLock</span></span><br />
<span data-ttu-id="171e1-172">1067</span><span class="sxs-lookup"><span data-stu-id="171e1-172">1067</span></span></p></td>
<td><p><span data-ttu-id="171e1-173">Non esiste un blocco di scrittura a livello di transazione 0.</span><span class="sxs-lookup"><span data-stu-id="171e1-173">There is a no write lock at transaction level 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-174">JET_wrnColumnSetNull</span><span class="sxs-lookup"><span data-stu-id="171e1-174">JET_wrnColumnSetNull</span></span><br />
<span data-ttu-id="171e1-175">1068</span><span class="sxs-lookup"><span data-stu-id="171e1-175">1068</span></span></p></td>
<td><p><span data-ttu-id="171e1-176">La colonna è impostata su un valore <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="171e1-176">The column is set to a <strong>NULL</strong> value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-177">JET_wrnTableEmpty</span><span class="sxs-lookup"><span data-stu-id="171e1-177">JET_wrnTableEmpty</span></span><br />
<span data-ttu-id="171e1-178">1301</span><span class="sxs-lookup"><span data-stu-id="171e1-178">1301</span></span></p></td>
<td><p><span data-ttu-id="171e1-179">È stata aperta una tabella vuota.</span><span class="sxs-lookup"><span data-stu-id="171e1-179">An empty table was opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-180">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="171e1-180">JET_wrnTableInUseBySystem</span></span><br />
<span data-ttu-id="171e1-181">1327</span><span class="sxs-lookup"><span data-stu-id="171e1-181">1327</span></span></p></td>
<td><p><span data-ttu-id="171e1-182">Per la pulizia del sistema è presente un cursore aperto sulla tabella.</span><span class="sxs-lookup"><span data-stu-id="171e1-182">The system cleanup has a cursor open on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-183">JET_wrnCorruptIndexDeleted</span><span class="sxs-lookup"><span data-stu-id="171e1-183">JET_wrnCorruptIndexDeleted</span></span><br />
<span data-ttu-id="171e1-184">1415</span><span class="sxs-lookup"><span data-stu-id="171e1-184">1415</span></span></p></td>
<td><p><span data-ttu-id="171e1-185">L'indice non aggiornato deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="171e1-185">The out-of-date index must be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-186">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="171e1-186">JET_wrnColumnMaxTruncated</span></span><br />
<span data-ttu-id="171e1-187">1512</span><span class="sxs-lookup"><span data-stu-id="171e1-187">1512</span></span></p></td>
<td><p><span data-ttu-id="171e1-188">La lunghezza massima è troppo grande ed è stata troncata.</span><span class="sxs-lookup"><span data-stu-id="171e1-188">The Max length is too large and has been truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-189">JET_wrnCopyLongValue</span><span class="sxs-lookup"><span data-stu-id="171e1-189">JET_wrnCopyLongValue</span></span><br />
<span data-ttu-id="171e1-190">1520</span><span class="sxs-lookup"><span data-stu-id="171e1-190">1520</span></span></p></td>
<td><p><span data-ttu-id="171e1-191">Un valore BLOB è stato spostato dal record in una risorsa di archiviazione separata di BLOB di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="171e1-191">A BLOB value has been moved from the record into a separate storage of large BLOBs.</span></span></p>
<p><span data-ttu-id="171e1-192"><strong>Nota</strong> Questo errore è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="171e1-192"><strong>Note</strong> This error is for internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-193">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="171e1-193">JET_wrnColumnSkipped</span></span><br />
<span data-ttu-id="171e1-194">1531</span><span class="sxs-lookup"><span data-stu-id="171e1-194">1531</span></span></p></td>
<td><p><span data-ttu-id="171e1-195">I valori della colonna non sono stati restituiti perché l'ID di colonna o il membro <em>itagSequence</em> corrispondente della struttura <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> richiesta per l'enumerazione è null.</span><span class="sxs-lookup"><span data-stu-id="171e1-195">The column values were not returned because the corresponding column ID or <em>itagSequence</em> member from the <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> structure that was requested for enumeration was null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-196">JET_wrnColumnNotLocal</span><span class="sxs-lookup"><span data-stu-id="171e1-196">JET_wrnColumnNotLocal</span></span><br />
<span data-ttu-id="171e1-197">1532</span><span class="sxs-lookup"><span data-stu-id="171e1-197">1532</span></span></p></td>
<td><p><span data-ttu-id="171e1-198">I valori della colonna non sono stati restituiti perché non è stato possibile ricostruire i dati esistenti.</span><span class="sxs-lookup"><span data-stu-id="171e1-198">The column values were not returned because they could not be reconstructed from the existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-199">JET_wrnColumnMoreTags</span><span class="sxs-lookup"><span data-stu-id="171e1-199">JET_wrnColumnMoreTags</span></span><br />
<span data-ttu-id="171e1-200">1533</span><span class="sxs-lookup"><span data-stu-id="171e1-200">1533</span></span></p></td>
<td><p><span data-ttu-id="171e1-201">I valori di colonna esistenti non sono stati richiesti per l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="171e1-201">The existing column values were not requested for enumeration.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-202">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="171e1-202">JET_wrnColumnTruncated</span></span><br />
<span data-ttu-id="171e1-203">1534</span><span class="sxs-lookup"><span data-stu-id="171e1-203">1534</span></span></p></td>
<td><p><span data-ttu-id="171e1-204">Il valore della colonna è stato troncato al limite delle dimensioni richiesto durante l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="171e1-204">The column value was truncated at the requested size limit during enumeration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-205">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="171e1-205">JET_wrnColumnPresent</span></span><br />
<span data-ttu-id="171e1-206">1535</span><span class="sxs-lookup"><span data-stu-id="171e1-206">1535</span></span></p></td>
<td><p><span data-ttu-id="171e1-207">I valori della colonna esistono ma non sono stati restituiti dalla richiesta.</span><span class="sxs-lookup"><span data-stu-id="171e1-207">The column values exist but were not returned by the request.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-208">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="171e1-208">JET_wrnColumnSingleValue</span></span><br />
<span data-ttu-id="171e1-209">1536</span><span class="sxs-lookup"><span data-stu-id="171e1-209">1536</span></span></p></td>
<td><p><span data-ttu-id="171e1-210">Il valore della colonna è stato restituito in JET_COLUMNENUM come risultato della JET_bitEnumerateCompressOutput da impostare.</span><span class="sxs-lookup"><span data-stu-id="171e1-210">The column value was returned in JET_COLUMNENUM as a result of the JET_bitEnumerateCompressOutput being set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-211">JET_wrnColumnDefault</span><span class="sxs-lookup"><span data-stu-id="171e1-211">JET_wrnColumnDefault</span></span><br />
<span data-ttu-id="171e1-212">1537</span><span class="sxs-lookup"><span data-stu-id="171e1-212">1537</span></span></p></td>
<td><p><span data-ttu-id="171e1-213">Il valore della colonna viene impostato sul valore predefinito della colonna.</span><span class="sxs-lookup"><span data-stu-id="171e1-213">The column value is set to the default value of the column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-214">JET_wrnDataHasChanged</span><span class="sxs-lookup"><span data-stu-id="171e1-214">JET_wrnDataHasChanged</span></span><br />
<span data-ttu-id="171e1-215">1610</span><span class="sxs-lookup"><span data-stu-id="171e1-215">1610</span></span></p></td>
<td><p><span data-ttu-id="171e1-216">I dati sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="171e1-216">The data has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-217">JET_wrnKeyChanged</span><span class="sxs-lookup"><span data-stu-id="171e1-217">JET_wrnKeyChanged</span></span><br />
<span data-ttu-id="171e1-218">1618</span><span class="sxs-lookup"><span data-stu-id="171e1-218">1618</span></span></p></td>
<td><p><span data-ttu-id="171e1-219">Viene utilizzata una nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="171e1-219">A new key is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-220">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="171e1-220">JET_wrnFileOpenReadOnly</span></span><br />
<span data-ttu-id="171e1-221">1813</span><span class="sxs-lookup"><span data-stu-id="171e1-221">1813</span></span></p></td>
<td><p><span data-ttu-id="171e1-222">Il file di database è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="171e1-222">The database file is read only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-223">JET_wrnIdleFull</span><span class="sxs-lookup"><span data-stu-id="171e1-223">JET_wrnIdleFull</span></span><br />
<span data-ttu-id="171e1-224">1908</span><span class="sxs-lookup"><span data-stu-id="171e1-224">1908</span></span></p></td>
<td><p><span data-ttu-id="171e1-225">Il registro di sistema inattivo è pieno.</span><span class="sxs-lookup"><span data-stu-id="171e1-225">The idle registry is full.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-226">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="171e1-226">JET_wrnDefragAlreadyRunning</span></span><br />
<span data-ttu-id="171e1-227">2000</span><span class="sxs-lookup"><span data-stu-id="171e1-227">2000</span></span></p></td>
<td><p><span data-ttu-id="171e1-228">Una deframmentazione in linea è già in esecuzione nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="171e1-228">There was an online defragmentation already running on the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-229">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="171e1-229">JET_wrnDefragNotRunning</span></span><br />
<span data-ttu-id="171e1-230">2001</span><span class="sxs-lookup"><span data-stu-id="171e1-230">2001</span></span></p></td>
<td><p><span data-ttu-id="171e1-231">Una deframmentazione in linea non è in esecuzione nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="171e1-231">An online defragmentation is not running on the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-232">JET_wrnCallbackNotRegistered</span><span class="sxs-lookup"><span data-stu-id="171e1-232">JET_wrnCallbackNotRegistered</span></span><br />
<span data-ttu-id="171e1-233">2100</span><span class="sxs-lookup"><span data-stu-id="171e1-233">2100</span></span></p></td>
<td><p><span data-ttu-id="171e1-234">È stata annullata la registrazione di una funzione di callback non esistente.</span><span class="sxs-lookup"><span data-stu-id="171e1-234">A non-existent callback function was unregistered.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="171e1-235">Un [JET_ERR](./jet-err.md) valore minore di zero deve essere interpretato come un errore.</span><span class="sxs-lookup"><span data-stu-id="171e1-235">A [JET_ERR](./jet-err.md) value that is less than zero should be interpreted as an error.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="171e1-236">Errors</span><span class="sxs-lookup"><span data-stu-id="171e1-236">Errors</span></span></p></th>
<th><p><span data-ttu-id="171e1-237">Descrizione</span><span class="sxs-lookup"><span data-stu-id="171e1-237">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="171e1-238">JET_wrnNyi</span><span class="sxs-lookup"><span data-stu-id="171e1-238">JET_wrnNyi</span></span><br />
<span data-ttu-id="171e1-239">-1</span><span class="sxs-lookup"><span data-stu-id="171e1-239">-1</span></span></p></td>
<td><p><span data-ttu-id="171e1-240">La funzione non è ancora implementata.</span><span class="sxs-lookup"><span data-stu-id="171e1-240">The function is not yet implemented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-241">JET_errRfsFailure</span><span class="sxs-lookup"><span data-stu-id="171e1-241">JET_errRfsFailure</span></span><br />
<span data-ttu-id="171e1-242">-100</span><span class="sxs-lookup"><span data-stu-id="171e1-242">-100</span></span></p></td>
<td><p><span data-ttu-id="171e1-243">Il simulatore di errore delle risorse non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="171e1-243">The Resource Failure Simulator failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-244">JET_errRfsNotArmed</span><span class="sxs-lookup"><span data-stu-id="171e1-244">JET_errRfsNotArmed</span></span><br />
<span data-ttu-id="171e1-245">-101</span><span class="sxs-lookup"><span data-stu-id="171e1-245">-101</span></span></p></td>
<td><p><span data-ttu-id="171e1-246">Il simulatore di errore delle risorse non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="171e1-246">The Resource Failure Simulator has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-247">JET_errFileClose</span><span class="sxs-lookup"><span data-stu-id="171e1-247">JET_errFileClose</span></span><br />
<span data-ttu-id="171e1-248">-102</span><span class="sxs-lookup"><span data-stu-id="171e1-248">-102</span></span></p></td>
<td><p><span data-ttu-id="171e1-249">Non è stato possibile chiudere il file.</span><span class="sxs-lookup"><span data-stu-id="171e1-249">The file could not be closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-250">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="171e1-250">JET_errOutOfThreads</span></span><br />
<span data-ttu-id="171e1-251">-103</span><span class="sxs-lookup"><span data-stu-id="171e1-251">-103</span></span></p></td>
<td><p><span data-ttu-id="171e1-252">Impossibile avviare il thread.</span><span class="sxs-lookup"><span data-stu-id="171e1-252">The thread could not be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-253">JET_errTooManyIO</span><span class="sxs-lookup"><span data-stu-id="171e1-253">JET_errTooManyIO</span></span><br />
<span data-ttu-id="171e1-254">-105</span><span class="sxs-lookup"><span data-stu-id="171e1-254">-105</span></span></p></td>
<td><p><span data-ttu-id="171e1-255">Il sistema è occupato a causa di un numero eccessivo di IOs.</span><span class="sxs-lookup"><span data-stu-id="171e1-255">The system is busy due to too many IOs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-256">JET_errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="171e1-256">JET_errTaskDropped</span></span><br />
<span data-ttu-id="171e1-257">-106</span><span class="sxs-lookup"><span data-stu-id="171e1-257">-106</span></span></p></td>
<td><p><span data-ttu-id="171e1-258">Non è stato possibile eseguire l'attività asincrona richiesta.</span><span class="sxs-lookup"><span data-stu-id="171e1-258">The requested asynchronous task could not be executed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-259">JET_errInternalError</span><span class="sxs-lookup"><span data-stu-id="171e1-259">JET_errInternalError</span></span><br />
<span data-ttu-id="171e1-260">-107</span><span class="sxs-lookup"><span data-stu-id="171e1-260">-107</span></span></p></td>
<td><p><span data-ttu-id="171e1-261">Si è verificato un errore interno irreversibile.</span><span class="sxs-lookup"><span data-stu-id="171e1-261">There was a fatal internal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-262">JET_errDatabaseBufferDependenciesCorrupted</span><span class="sxs-lookup"><span data-stu-id="171e1-262">JET_errDatabaseBufferDependenciesCorrupted</span></span><br />
<span data-ttu-id="171e1-263">-255</span><span class="sxs-lookup"><span data-stu-id="171e1-263">-255</span></span></p></td>
<td><p><span data-ttu-id="171e1-264">Le dipendenze del buffer sono state impostate in modo errato e si è verificato un errore di ripristino.</span><span class="sxs-lookup"><span data-stu-id="171e1-264">The buffer dependencies were set improperly and there was a recovery failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-265">JET_errPreviousVersion</span><span class="sxs-lookup"><span data-stu-id="171e1-265">JET_errPreviousVersion</span></span><br />
<span data-ttu-id="171e1-266">-322</span><span class="sxs-lookup"><span data-stu-id="171e1-266">-322</span></span></p></td>
<td><p><span data-ttu-id="171e1-267">La versione esisteva già e si è verificato un errore di ripristino.</span><span class="sxs-lookup"><span data-stu-id="171e1-267">The version already existed and there was a recovery failure.</span></span> <span data-ttu-id="171e1-268">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-268">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-269">JET_errPageBoundary</span><span class="sxs-lookup"><span data-stu-id="171e1-269">JET_errPageBoundary</span></span><br />
<span data-ttu-id="171e1-270">-323</span><span class="sxs-lookup"><span data-stu-id="171e1-270">-323</span></span></p></td>
<td><p><span data-ttu-id="171e1-271">È stato raggiunto il limite della pagina.</span><span class="sxs-lookup"><span data-stu-id="171e1-271">The page boundary has been reached.</span></span> <span data-ttu-id="171e1-272">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-272">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-273">JET_errKeyBoundary</span><span class="sxs-lookup"><span data-stu-id="171e1-273">JET_errKeyBoundary</span></span><br />
<span data-ttu-id="171e1-274">-324</span><span class="sxs-lookup"><span data-stu-id="171e1-274">-324</span></span></p></td>
<td><p><span data-ttu-id="171e1-275">È stato raggiunto il limite della chiave.</span><span class="sxs-lookup"><span data-stu-id="171e1-275">The key boundary has been reached.</span></span> <span data-ttu-id="171e1-276">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-276">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-277">JET_errBadPageLink</span><span class="sxs-lookup"><span data-stu-id="171e1-277">JET_errBadPageLink</span></span><br />
<span data-ttu-id="171e1-278">-327</span><span class="sxs-lookup"><span data-stu-id="171e1-278">-327</span></span></p></td>
<td><p><span data-ttu-id="171e1-279">Il database è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="171e1-279">The database is corrupt.</span></span> <span data-ttu-id="171e1-280">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-280">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-281">JET_errBadBookmark</span><span class="sxs-lookup"><span data-stu-id="171e1-281">JET_errBadBookmark</span></span><br />
<span data-ttu-id="171e1-282">-328</span><span class="sxs-lookup"><span data-stu-id="171e1-282">-328</span></span></p></td>
<td><p><span data-ttu-id="171e1-283">Il segnalibro non ha alcun indirizzo corrispondente nel database.</span><span class="sxs-lookup"><span data-stu-id="171e1-283">The bookmark has no corresponding address in the database.</span></span> <span data-ttu-id="171e1-284">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-284">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-285">JET_errNTSystemCallFailed</span><span class="sxs-lookup"><span data-stu-id="171e1-285">JET_errNTSystemCallFailed</span></span><br />
<span data-ttu-id="171e1-286">-334</span><span class="sxs-lookup"><span data-stu-id="171e1-286">-334</span></span></p></td>
<td><p><span data-ttu-id="171e1-287">La chiamata al sistema operativo non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="171e1-287">The call to the operating system failed.</span></span> <span data-ttu-id="171e1-288">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-288">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-289">JET_errBadParentPageLink</span><span class="sxs-lookup"><span data-stu-id="171e1-289">JET_errBadParentPageLink</span></span><br />
<span data-ttu-id="171e1-290">-338</span><span class="sxs-lookup"><span data-stu-id="171e1-290">-338</span></span></p></td>
<td><p><span data-ttu-id="171e1-291">Un database padre è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="171e1-291">A parent database is corrupt.</span></span> <span data-ttu-id="171e1-292">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-292">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-293">JET_errSPAvailExtCacheOutOfSync</span><span class="sxs-lookup"><span data-stu-id="171e1-293">JET_errSPAvailExtCacheOutOfSync</span></span><br />
<span data-ttu-id="171e1-294">-340</span><span class="sxs-lookup"><span data-stu-id="171e1-294">-340</span></span></p></td>
<td><p><span data-ttu-id="171e1-295">La cache AvailExt non corrisponde all'albero B +.</span><span class="sxs-lookup"><span data-stu-id="171e1-295">The AvailExt cache does not match the B+ tree.</span></span> <span data-ttu-id="171e1-296">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-296">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-297">JET_errSPAvailExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="171e1-297">JET_errSPAvailExtCorrupted</span></span><br />
<span data-ttu-id="171e1-298">-341</span><span class="sxs-lookup"><span data-stu-id="171e1-298">-341</span></span></p></td>
<td><p><span data-ttu-id="171e1-299">L'albero dello spazio AllAvailExt è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="171e1-299">The AllAvailExt space tree is corrupt.</span></span> <span data-ttu-id="171e1-300">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-300">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-301">JET_errSPAvailExtCacheOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="171e1-301">JET_errSPAvailExtCacheOutOfMemory</span></span><br />
<span data-ttu-id="171e1-302">-342</span><span class="sxs-lookup"><span data-stu-id="171e1-302">-342</span></span></p></td>
<td><p><span data-ttu-id="171e1-303">Si è verificato un errore di memoria insufficiente durante l'allocazione di un nodo della cache AvailExt.</span><span class="sxs-lookup"><span data-stu-id="171e1-303">An out of memory error occurred while allocating an AvailExt cache node.</span></span> <span data-ttu-id="171e1-304">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-304">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-305">JET_errSPOwnExtCorrupted</span><span class="sxs-lookup"><span data-stu-id="171e1-305">JET_errSPOwnExtCorrupted</span></span><br />
<span data-ttu-id="171e1-306">-343</span><span class="sxs-lookup"><span data-stu-id="171e1-306">-343</span></span></p></td>
<td><p><span data-ttu-id="171e1-307">L'albero dello spazio OwnExt è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="171e1-307">The OwnExt space tree is corrupt.</span></span> <span data-ttu-id="171e1-308">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-308">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-309">JET_errDbTimeCorrupted</span><span class="sxs-lookup"><span data-stu-id="171e1-309">JET_errDbTimeCorrupted</span></span><br />
<span data-ttu-id="171e1-310">-344</span><span class="sxs-lookup"><span data-stu-id="171e1-310">-344</span></span></p></td>
<td><p><span data-ttu-id="171e1-311">Dbtime nella pagina corrente è maggiore del valore di dbtime del database globale.</span><span class="sxs-lookup"><span data-stu-id="171e1-311">The Dbtime on the current page is greater than the global database dbtime.</span></span> <span data-ttu-id="171e1-312">Questo errore viene restituito da gestione directory.</span><span class="sxs-lookup"><span data-stu-id="171e1-312">This error is returned by the directory manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-313">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="171e1-313">JET_errKeyTruncated</span></span><br />
<span data-ttu-id="171e1-314">-346</span><span class="sxs-lookup"><span data-stu-id="171e1-314">-346</span></span></p></td>
<td><p><span data-ttu-id="171e1-315">Il tentativo di creare una chiave per una voce di indice non è riuscito perché la chiave sarebbe stata troncata e la definizione dell'indice non consentiva il troncamento della chiave.</span><span class="sxs-lookup"><span data-stu-id="171e1-315">An attempt to create a key for an index entry failed because the key would have been truncated and the index definition disallows key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-316">JET_errKeyTooBig</span><span class="sxs-lookup"><span data-stu-id="171e1-316">JET_errKeyTooBig</span></span><br />
<span data-ttu-id="171e1-317">-408</span><span class="sxs-lookup"><span data-stu-id="171e1-317">-408</span></span></p></td>
<td><p><span data-ttu-id="171e1-318">Chiave troppo grande.</span><span class="sxs-lookup"><span data-stu-id="171e1-318">The key is too large.</span></span> <span data-ttu-id="171e1-319">Questo errore viene restituito da Gestione record.</span><span class="sxs-lookup"><span data-stu-id="171e1-319">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-320">JET_errInvalidLoggedOperation</span><span class="sxs-lookup"><span data-stu-id="171e1-320">JET_errInvalidLoggedOperation</span></span><br />
<span data-ttu-id="171e1-321">-500</span><span class="sxs-lookup"><span data-stu-id="171e1-321">-500</span></span></p></td>
<td><p><span data-ttu-id="171e1-322">Impossibile ripetere l'operazione registrata.</span><span class="sxs-lookup"><span data-stu-id="171e1-322">The logged operation cannot be redone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-323">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="171e1-323">JET_errLogFileCorrupt</span></span><br />
<span data-ttu-id="171e1-324">-501</span><span class="sxs-lookup"><span data-stu-id="171e1-324">-501</span></span></p></td>
<td><p><span data-ttu-id="171e1-325">Il file di log è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="171e1-325">The log file is corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-326">JET_errNoBackupDirectory</span><span class="sxs-lookup"><span data-stu-id="171e1-326">JET_errNoBackupDirectory</span></span><br />
<span data-ttu-id="171e1-327">-503</span><span class="sxs-lookup"><span data-stu-id="171e1-327">-503</span></span></p></td>
<td><p><span data-ttu-id="171e1-328">Non è stata specificata una directory di backup.</span><span class="sxs-lookup"><span data-stu-id="171e1-328">A backup directory was not given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-329">JET_errBackupDirectoryNotEmpty</span><span class="sxs-lookup"><span data-stu-id="171e1-329">JET_errBackupDirectoryNotEmpty</span></span><br />
<span data-ttu-id="171e1-330">-504</span><span class="sxs-lookup"><span data-stu-id="171e1-330">-504</span></span></p></td>
<td><p><span data-ttu-id="171e1-331">La directory di backup non è vuota.</span><span class="sxs-lookup"><span data-stu-id="171e1-331">The backup directory is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-332">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="171e1-332">JET_errBackupInProgress</span></span><br />
<span data-ttu-id="171e1-333">-505</span><span class="sxs-lookup"><span data-stu-id="171e1-333">-505</span></span></p></td>
<td><p><span data-ttu-id="171e1-334">Il backup è già attivo.</span><span class="sxs-lookup"><span data-stu-id="171e1-334">The backup is active already.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-335">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="171e1-335">JET_errRestoreInProgress</span></span><br />
<span data-ttu-id="171e1-336">-506</span><span class="sxs-lookup"><span data-stu-id="171e1-336">-506</span></span></p></td>
<td><p><span data-ttu-id="171e1-337">È in corso un ripristino.</span><span class="sxs-lookup"><span data-stu-id="171e1-337">A restore is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-338">JET_errMissingPreviousLogFile</span><span class="sxs-lookup"><span data-stu-id="171e1-338">JET_errMissingPreviousLogFile</span></span><br />
<span data-ttu-id="171e1-339">-509</span><span class="sxs-lookup"><span data-stu-id="171e1-339">-509</span></span></p></td>
<td><p><span data-ttu-id="171e1-340">Il file di log non è presente per il punto di controllo.</span><span class="sxs-lookup"><span data-stu-id="171e1-340">The log file is missing for the check point.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-341">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="171e1-341">JET_errLogWriteFail</span></span><br />
<span data-ttu-id="171e1-342">-510</span><span class="sxs-lookup"><span data-stu-id="171e1-342">-510</span></span></p></td>
<td><p><span data-ttu-id="171e1-343">Si è verificato un errore durante la scrittura nel file di log.</span><span class="sxs-lookup"><span data-stu-id="171e1-343">There was a failure writing to the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-344">JET_errLogDisabledDueToRecoveryFailure</span><span class="sxs-lookup"><span data-stu-id="171e1-344">JET_errLogDisabledDueToRecoveryFailure</span></span><br />
<span data-ttu-id="171e1-345">-511</span><span class="sxs-lookup"><span data-stu-id="171e1-345">-511</span></span></p></td>
<td><p><span data-ttu-id="171e1-346">Il tentativo di scrittura nel log dopo il ripristino non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="171e1-346">The attempt to write to the log after recovery failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-347">JET_errCannotLogDuringRecoveryRedo</span><span class="sxs-lookup"><span data-stu-id="171e1-347">JET_errCannotLogDuringRecoveryRedo</span></span><br />
<span data-ttu-id="171e1-348">-512</span><span class="sxs-lookup"><span data-stu-id="171e1-348">-512</span></span></p></td>
<td><p><span data-ttu-id="171e1-349">Tentativo di scrittura nel log durante il ripristino del ripristino non riuscito.</span><span class="sxs-lookup"><span data-stu-id="171e1-349">The attempt to write to the log during the recovery redo failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-350">JET_errLogGenerationMismatch</span><span class="sxs-lookup"><span data-stu-id="171e1-350">JET_errLogGenerationMismatch</span></span><br />
<span data-ttu-id="171e1-351">-513</span><span class="sxs-lookup"><span data-stu-id="171e1-351">-513</span></span></p></td>
<td><p><span data-ttu-id="171e1-352">Il nome del file di log non corrisponde al numero di generazione interno.</span><span class="sxs-lookup"><span data-stu-id="171e1-352">The name of of the log file does not match the internal generation number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-353">JET_errBadLogVersion</span><span class="sxs-lookup"><span data-stu-id="171e1-353">JET_errBadLogVersion</span></span><br />
<span data-ttu-id="171e1-354">-514</span><span class="sxs-lookup"><span data-stu-id="171e1-354">-514</span></span></p></td>
<td><p><span data-ttu-id="171e1-355">La versione del file di registro non è compatibile con la versione ESE.</span><span class="sxs-lookup"><span data-stu-id="171e1-355">The version of the log file is not compatible with the ESE version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-356">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="171e1-356">JET_errInvalidLogSequence</span></span><br />
<span data-ttu-id="171e1-357">-515</span><span class="sxs-lookup"><span data-stu-id="171e1-357">-515</span></span></p></td>
<td><p><span data-ttu-id="171e1-358">Il timestamp nel log successivo non corrisponde al timestamp previsto.</span><span class="sxs-lookup"><span data-stu-id="171e1-358">The timestamp in the next log does not match the expected timestamp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-359">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="171e1-359">JET_errLoggingDisabled</span></span><br />
<span data-ttu-id="171e1-360">-516</span><span class="sxs-lookup"><span data-stu-id="171e1-360">-516</span></span></p></td>
<td><p><span data-ttu-id="171e1-361">Il log non è attivo.</span><span class="sxs-lookup"><span data-stu-id="171e1-361">The log is not active.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-362">JET_errLogBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="171e1-362">JET_errLogBufferTooSmall</span></span><br />
<span data-ttu-id="171e1-363">-517</span><span class="sxs-lookup"><span data-stu-id="171e1-363">-517</span></span></p></td>
<td><p><span data-ttu-id="171e1-364">Il buffer del log è troppo piccolo per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="171e1-364">The log buffer is too small for recovery.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-365">JET_errLogSequenceEnd</span><span class="sxs-lookup"><span data-stu-id="171e1-365">JET_errLogSequenceEnd</span></span><br />
<span data-ttu-id="171e1-366">-519</span><span class="sxs-lookup"><span data-stu-id="171e1-366">-519</span></span></p></td>
<td><p><span data-ttu-id="171e1-367">È stato superato il numero massimo di file di log.</span><span class="sxs-lookup"><span data-stu-id="171e1-367">The maximum log file number has been exceeded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-368">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="171e1-368">JET_errNoBackup</span></span><br />
<span data-ttu-id="171e1-369">-520</span><span class="sxs-lookup"><span data-stu-id="171e1-369">-520</span></span></p></td>
<td><p><span data-ttu-id="171e1-370">Nessun backup in corso.</span><span class="sxs-lookup"><span data-stu-id="171e1-370">There is no backup in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-371">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="171e1-371">JET_errInvalidBackupSequence</span></span><br />
<span data-ttu-id="171e1-372">-521</span><span class="sxs-lookup"><span data-stu-id="171e1-372">-521</span></span></p></td>
<td><p><span data-ttu-id="171e1-373">La chiamata di backup è fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="171e1-373">The backup call is out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-374">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="171e1-374">JET_errBackupNotAllowedYet</span></span><br />
<span data-ttu-id="171e1-375">-523</span><span class="sxs-lookup"><span data-stu-id="171e1-375">-523</span></span></p></td>
<td><p><span data-ttu-id="171e1-376">Non è possibile eseguire un backup in questo momento.</span><span class="sxs-lookup"><span data-stu-id="171e1-376">A backup cannot be done at this time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-377">JET_errDeleteBackupFileFail</span><span class="sxs-lookup"><span data-stu-id="171e1-377">JET_errDeleteBackupFileFail</span></span><br />
<span data-ttu-id="171e1-378">-524</span><span class="sxs-lookup"><span data-stu-id="171e1-378">-524</span></span></p></td>
<td><p><span data-ttu-id="171e1-379">Non è stato possibile eliminare un file di backup.</span><span class="sxs-lookup"><span data-stu-id="171e1-379">A backup file could not be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-380">JET_errMakeBackupDirectoryFail</span><span class="sxs-lookup"><span data-stu-id="171e1-380">JET_errMakeBackupDirectoryFail</span></span><br />
<span data-ttu-id="171e1-381">-525</span><span class="sxs-lookup"><span data-stu-id="171e1-381">-525</span></span></p></td>
<td><p><span data-ttu-id="171e1-382">Non è stato possibile creare la directory temporanea di backup.</span><span class="sxs-lookup"><span data-stu-id="171e1-382">The backup temporary directory could not be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-383">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="171e1-383">JET_errInvalidBackup</span></span><br />
<span data-ttu-id="171e1-384">-526</span><span class="sxs-lookup"><span data-stu-id="171e1-384">-526</span></span></p></td>
<td><p><span data-ttu-id="171e1-385">Registrazione circolare abilitata; non è possibile eseguire un backup incrementale.</span><span class="sxs-lookup"><span data-stu-id="171e1-385">Circular logging is enabled; an incremental backup cannot be performed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-386">JET_errRecoveredWithErrors</span><span class="sxs-lookup"><span data-stu-id="171e1-386">JET_errRecoveredWithErrors</span></span><br />
<span data-ttu-id="171e1-387">-527</span><span class="sxs-lookup"><span data-stu-id="171e1-387">-527</span></span></p></td>
<td><p><span data-ttu-id="171e1-388">I dati sono stati ripristinati con errori.</span><span class="sxs-lookup"><span data-stu-id="171e1-388">The data was restored with errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-389">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="171e1-389">JET_errMissingLogFile</span></span><br />
<span data-ttu-id="171e1-390">-528</span><span class="sxs-lookup"><span data-stu-id="171e1-390">-528</span></span></p></td>
<td><p><span data-ttu-id="171e1-391">Manca il file di registro corrente.</span><span class="sxs-lookup"><span data-stu-id="171e1-391">The current log file is missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-392">JET_errLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="171e1-392">JET_errLogDiskFull</span></span><br />
<span data-ttu-id="171e1-393">-529</span><span class="sxs-lookup"><span data-stu-id="171e1-393">-529</span></span></p></td>
<td><p><span data-ttu-id="171e1-394">Disco di registro pieno.</span><span class="sxs-lookup"><span data-stu-id="171e1-394">The log disk is full.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-395">JET_errBadLogSignature</span><span class="sxs-lookup"><span data-stu-id="171e1-395">JET_errBadLogSignature</span></span><br />
<span data-ttu-id="171e1-396">-530</span><span class="sxs-lookup"><span data-stu-id="171e1-396">-530</span></span></p></td>
<td><p><span data-ttu-id="171e1-397">Firma non valida per un file di log.</span><span class="sxs-lookup"><span data-stu-id="171e1-397">There is a bad signature for a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-398">JET_errBadDbSignature</span><span class="sxs-lookup"><span data-stu-id="171e1-398">JET_errBadDbSignature</span></span><br />
<span data-ttu-id="171e1-399">-531</span><span class="sxs-lookup"><span data-stu-id="171e1-399">-531</span></span></p></td>
<td><p><span data-ttu-id="171e1-400">Firma non valida per un file di database.</span><span class="sxs-lookup"><span data-stu-id="171e1-400">There is a bad signature for a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-401">JET_errBadCheckpointSignature</span><span class="sxs-lookup"><span data-stu-id="171e1-401">JET_errBadCheckpointSignature</span></span><br />
<span data-ttu-id="171e1-402">-532</span><span class="sxs-lookup"><span data-stu-id="171e1-402">-532</span></span></p></td>
<td><p><span data-ttu-id="171e1-403">Firma non valida per un file del checkpoint.</span><span class="sxs-lookup"><span data-stu-id="171e1-403">There is a bad signature for a checkpoint file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-404">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="171e1-404">JET_errCheckpointCorrupt</span></span><br />
<span data-ttu-id="171e1-405">-533</span><span class="sxs-lookup"><span data-stu-id="171e1-405">-533</span></span></p></td>
<td><p><span data-ttu-id="171e1-406">Il file del checkpoint non è stato trovato o è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="171e1-406">The checkpoint file was not found or was corrupt.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-407">JET_errMissingPatchPage</span><span class="sxs-lookup"><span data-stu-id="171e1-407">JET_errMissingPatchPage</span></span><br />
<span data-ttu-id="171e1-408">-534</span><span class="sxs-lookup"><span data-stu-id="171e1-408">-534</span></span></p></td>
<td><p><span data-ttu-id="171e1-409">Impossibile trovare la pagina file della patch del database durante il ripristino.</span><span class="sxs-lookup"><span data-stu-id="171e1-409">The database patch file page was not found during recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-410">JET_errBadPatchPage</span><span class="sxs-lookup"><span data-stu-id="171e1-410">JET_errBadPatchPage</span></span><br />
<span data-ttu-id="171e1-411">-535</span><span class="sxs-lookup"><span data-stu-id="171e1-411">-535</span></span></p></td>
<td><p><span data-ttu-id="171e1-412">La pagina del file di patch del database non è valida.</span><span class="sxs-lookup"><span data-stu-id="171e1-412">The database patch file page is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-413">JET_errRedoAbruptEnded</span><span class="sxs-lookup"><span data-stu-id="171e1-413">JET_errRedoAbruptEnded</span></span><br />
<span data-ttu-id="171e1-414">-536</span><span class="sxs-lookup"><span data-stu-id="171e1-414">-536</span></span></p></td>
<td><p><span data-ttu-id="171e1-415">Il rollforward si è improvvisamente interrotto a causa di un errore improvviso durante la lettura dei log dal file di log.</span><span class="sxs-lookup"><span data-stu-id="171e1-415">The redo abruptly ended due to a sudden failure while reading logs from the log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-416">JET_errBadSLVSignature</span><span class="sxs-lookup"><span data-stu-id="171e1-416">JET_errBadSLVSignature</span></span><br />
<span data-ttu-id="171e1-417">-537</span><span class="sxs-lookup"><span data-stu-id="171e1-417">-537</span></span></p></td>
<td><p><span data-ttu-id="171e1-418">Questo flag è riservato.</span><span class="sxs-lookup"><span data-stu-id="171e1-418">This flag is reserved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-419">JET_errPatchFileMissing</span><span class="sxs-lookup"><span data-stu-id="171e1-419">JET_errPatchFileMissing</span></span><br />
<span data-ttu-id="171e1-420">-538</span><span class="sxs-lookup"><span data-stu-id="171e1-420">-538</span></span></p></td>
<td><p><span data-ttu-id="171e1-421">Il ripristino hardware ha rilevato che nel set di backup manca un file di patch del database.</span><span class="sxs-lookup"><span data-stu-id="171e1-421">The hard restore detected that a database patch file is missing from the backup set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-422">JET_errDatabaseLogSetMismatch</span><span class="sxs-lookup"><span data-stu-id="171e1-422">JET_errDatabaseLogSetMismatch</span></span><br />
<span data-ttu-id="171e1-423">-539</span><span class="sxs-lookup"><span data-stu-id="171e1-423">-539</span></span></p></td>
<td><p><span data-ttu-id="171e1-424">Il database non appartiene al set di file di log corrente.</span><span class="sxs-lookup"><span data-stu-id="171e1-424">The database does not belong with the current set of log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-425">JET_errDatabaseStreamingFileMismatch</span><span class="sxs-lookup"><span data-stu-id="171e1-425">JET_errDatabaseStreamingFileMismatch</span></span><br />
<span data-ttu-id="171e1-426">-540</span><span class="sxs-lookup"><span data-stu-id="171e1-426">-540</span></span></p></td>
<td><p><span data-ttu-id="171e1-427">Questo flag è riservato.</span><span class="sxs-lookup"><span data-stu-id="171e1-427">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-428">JET_errLogFileSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="171e1-428">JET_errLogFileSizeMismatch</span></span><br />
<span data-ttu-id="171e1-429">-541</span><span class="sxs-lookup"><span data-stu-id="171e1-429">-541</span></span></p></td>
<td><p><span data-ttu-id="171e1-430">Le dimensioni effettive del file di log non corrispondono <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="171e1-430">The actual log file size does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-431">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="171e1-431">JET_errCheckpointFileNotFound</span></span><br />
<span data-ttu-id="171e1-432">-542</span><span class="sxs-lookup"><span data-stu-id="171e1-432">-542</span></span></p></td>
<td><p><span data-ttu-id="171e1-433">Impossibile trovare il file del checkpoint.</span><span class="sxs-lookup"><span data-stu-id="171e1-433">The checkpoint file could not be located.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-434">JET_errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="171e1-434">JET_errRequiredLogFilesMissing</span></span><br />
<span data-ttu-id="171e1-435">-543</span><span class="sxs-lookup"><span data-stu-id="171e1-435">-543</span></span></p></td>
<td><p><span data-ttu-id="171e1-436">Mancano i file di log necessari per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="171e1-436">The required log files for recovery are missing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-437">JET_errSoftRecoveryOnBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="171e1-437">JET_errSoftRecoveryOnBackupDatabase</span></span><br />
<span data-ttu-id="171e1-438">-544</span><span class="sxs-lookup"><span data-stu-id="171e1-438">-544</span></span></p></td>
<td><p><span data-ttu-id="171e1-439">Un ripristino soft sta per essere utilizzato in un database di backup quando è necessario utilizzare un ripristino.</span><span class="sxs-lookup"><span data-stu-id="171e1-439">A soft recovery is about to be used on a backup database when a restore should be used instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-440">JET_errLogFileSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="171e1-440">JET_errLogFileSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="171e1-441">-545</span><span class="sxs-lookup"><span data-stu-id="171e1-441">-545</span></span></p></td>
<td><p><span data-ttu-id="171e1-442">I database sono stati ripristinati, ma le dimensioni del file di log utilizzate durante il ripristino non corrispondono <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span><span class="sxs-lookup"><span data-stu-id="171e1-442">The databases have been recovered, but the log file size used during recovery does not match <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-443">JET_errLogSectorSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="171e1-443">JET_errLogSectorSizeMismatch</span></span><br />
<span data-ttu-id="171e1-444">-546</span><span class="sxs-lookup"><span data-stu-id="171e1-444">-546</span></span></p></td>
<td><p><span data-ttu-id="171e1-445">Le dimensioni del settore del file di log non corrispondono a quelle del volume corrente.</span><span class="sxs-lookup"><span data-stu-id="171e1-445">The log file sector size does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="171e1-446">JET_errLogSectorSizeMismatchDatabasesConsistent</span></span><br />
<span data-ttu-id="171e1-447">-547</span><span class="sxs-lookup"><span data-stu-id="171e1-447">-547</span></span></p></td>
<td><p><span data-ttu-id="171e1-448">I database sono stati ripristinati, ma le dimensioni del settore del file di log (usate durante il ripristino) non corrispondono alle dimensioni del settore del volume corrente.</span><span class="sxs-lookup"><span data-stu-id="171e1-448">The databases have been recovered, but the log file sector size (used during recovery) does not match the sector size of the current volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-449">JET_errLogSequenceEndDatabasesConsistent</span><span class="sxs-lookup"><span data-stu-id="171e1-449">JET_errLogSequenceEndDatabasesConsistent</span></span><br />
<span data-ttu-id="171e1-450">-548</span><span class="sxs-lookup"><span data-stu-id="171e1-450">-548</span></span></p></td>
<td><p><span data-ttu-id="171e1-451">I database sono stati ripristinati, ma sono state usate tutte le generazioni di log possibili nella sequenza corrente.</span><span class="sxs-lookup"><span data-stu-id="171e1-451">The databases have been recovered, but all possible log generations in the current sequence have been used.</span></span> <span data-ttu-id="171e1-452">Prima di continuare, è necessario eliminare tutti i file di registro e il file del checkpoint e il backup dei database.</span><span class="sxs-lookup"><span data-stu-id="171e1-452">All log files and the checkpoint file must be deleted and databases must be backed up before continuing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-453">JET_errStreamingDataNotLogged</span><span class="sxs-lookup"><span data-stu-id="171e1-453">JET_errStreamingDataNotLogged</span></span><br />
<span data-ttu-id="171e1-454">-549</span><span class="sxs-lookup"><span data-stu-id="171e1-454">-549</span></span></p></td>
<td><p><span data-ttu-id="171e1-455">Si è verificato un tentativo non valido di riprodurre un'operazione di streaming di file in cui i dati non sono stati registrati.</span><span class="sxs-lookup"><span data-stu-id="171e1-455">There was an illegal attempt to replay a streaming file operation where the data was not logged.</span></span> <span data-ttu-id="171e1-456">Questo è probabilmente causato da un tentativo di rollforward con la registrazione circolare abilitata.</span><span class="sxs-lookup"><span data-stu-id="171e1-456">This is probably caused by an attempt to rollforward with circular logging enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-457">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="171e1-457">JET_errDatabaseDirtyShutdown</span></span><br />
<span data-ttu-id="171e1-458">-550</span><span class="sxs-lookup"><span data-stu-id="171e1-458">-550</span></span></p></td>
<td><p><span data-ttu-id="171e1-459">Il database non è stato arrestato in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="171e1-459">The database was not shutdown cleanly.</span></span> <span data-ttu-id="171e1-460">È innanzitutto necessario eseguire un ripristino per completare correttamente le operazioni di database per l'arresto precedente.</span><span class="sxs-lookup"><span data-stu-id="171e1-460">A recovery must first be run to properly complete database operations for the previous shutdown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-461">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="171e1-461">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="171e1-462">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="171e1-462">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="171e1-463">Questo errore è obsoleto ed è stato sostituito da JET_errDatabaseDirtyShutdown.</span><span class="sxs-lookup"><span data-stu-id="171e1-463">This error is obsolete and has been replaced by JET_errDatabaseDirtyShutdown.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-464">JET_errConsistentTimeMismatch</span><span class="sxs-lookup"><span data-stu-id="171e1-464">JET_errConsistentTimeMismatch</span></span><br />
<span data-ttu-id="171e1-465">-551</span><span class="sxs-lookup"><span data-stu-id="171e1-465">-551</span></span></p></td>
<td><p><span data-ttu-id="171e1-466">Non è stata confrontata l'ora dell'ultimo coerente per il database.</span><span class="sxs-lookup"><span data-stu-id="171e1-466">The last consistent time for the database has not been matched.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-467">JET_errDatabasePatchFileMismatch</span><span class="sxs-lookup"><span data-stu-id="171e1-467">JET_errDatabasePatchFileMismatch</span></span><br />
<span data-ttu-id="171e1-468">-552</span><span class="sxs-lookup"><span data-stu-id="171e1-468">-552</span></span></p></td>
<td><p><span data-ttu-id="171e1-469">Il file di patch del database non viene generato da questo backup.</span><span class="sxs-lookup"><span data-stu-id="171e1-469">The database patch file is not generated from this backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-470">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="171e1-470">JET_errEndingRestoreLogTooLow</span></span><br />
<span data-ttu-id="171e1-471">-553</span><span class="sxs-lookup"><span data-stu-id="171e1-471">-553</span></span></p></td>
<td><p><span data-ttu-id="171e1-472">Il numero di log iniziale è troppo basso per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="171e1-472">The starting log number is too low for the restore.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-473">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="171e1-473">JET_errStartingRestoreLogTooHigh</span></span><br />
<span data-ttu-id="171e1-474">-554</span><span class="sxs-lookup"><span data-stu-id="171e1-474">-554</span></span></p></td>
<td><p><span data-ttu-id="171e1-475">Il numero di log iniziale è troppo elevato per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="171e1-475">The starting log number is too high for the restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-476">JET_errGivenLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="171e1-476">JET_errGivenLogFileHasBadSignature</span></span><br />
<span data-ttu-id="171e1-477">-555</span><span class="sxs-lookup"><span data-stu-id="171e1-477">-555</span></span></p></td>
<td><p><span data-ttu-id="171e1-478">La firma del file di log di ripristino non è valida.</span><span class="sxs-lookup"><span data-stu-id="171e1-478">The restore log file has a bad signature.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-479">JET_errGivenLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="171e1-479">JET_errGivenLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="171e1-480">-556</span><span class="sxs-lookup"><span data-stu-id="171e1-480">-556</span></span></p></td>
<td><p><span data-ttu-id="171e1-481">Il file di log di ripristino non è contiguo.</span><span class="sxs-lookup"><span data-stu-id="171e1-481">The restore log file is not contiguous.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-482">JET_errMissingRestoreLogFiles</span><span class="sxs-lookup"><span data-stu-id="171e1-482">JET_errMissingRestoreLogFiles</span></span><br />
<span data-ttu-id="171e1-483">-557</span><span class="sxs-lookup"><span data-stu-id="171e1-483">-557</span></span></p></td>
<td><p><span data-ttu-id="171e1-484">Alcuni file di log di ripristino risultano mancanti.</span><span class="sxs-lookup"><span data-stu-id="171e1-484">Some restore log files are missing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-485">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="171e1-485">JET_errMissingFullBackup</span></span><br />
<span data-ttu-id="171e1-486">-560</span><span class="sxs-lookup"><span data-stu-id="171e1-486">-560</span></span></p></td>
<td><p><span data-ttu-id="171e1-487">Il database ha perso un backup completo precedente prima di provare a eseguire un backup incrementale.</span><span class="sxs-lookup"><span data-stu-id="171e1-487">The database missed a previous full backup before attempting to perform an incremental backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-488">JET_errBadBackupDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="171e1-488">JET_errBadBackupDatabaseSize</span></span><br />
<span data-ttu-id="171e1-489">-561</span><span class="sxs-lookup"><span data-stu-id="171e1-489">-561</span></span></p></td>
<td><p><span data-ttu-id="171e1-490">Le dimensioni del database di backup non sono un multiplo delle dimensioni della pagina del database.</span><span class="sxs-lookup"><span data-stu-id="171e1-490">The backup database size is not a multiple of the database page size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-491">JET_errDatabaseAlreadyUpgraded</span><span class="sxs-lookup"><span data-stu-id="171e1-491">JET_errDatabaseAlreadyUpgraded</span></span><br />
<span data-ttu-id="171e1-492">-562</span><span class="sxs-lookup"><span data-stu-id="171e1-492">-562</span></span></p></td>
<td><p><span data-ttu-id="171e1-493">Il tentativo corrente di aggiornare un database è stato interrotto perché il database è già aggiornato.</span><span class="sxs-lookup"><span data-stu-id="171e1-493">The current attempt to upgrade a database has been stopped because the database is already current.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-494">JET_errDatabaseIncompleteUpgrade</span><span class="sxs-lookup"><span data-stu-id="171e1-494">JET_errDatabaseIncompleteUpgrade</span></span><br />
<span data-ttu-id="171e1-495">-563</span><span class="sxs-lookup"><span data-stu-id="171e1-495">-563</span></span></p></td>
<td><p><span data-ttu-id="171e1-496">Il database è stato convertito solo parzialmente nel formato corrente.</span><span class="sxs-lookup"><span data-stu-id="171e1-496">The database was only partially converted to the current format.</span></span> <span data-ttu-id="171e1-497">È necessario ripristinare il database dal backup.</span><span class="sxs-lookup"><span data-stu-id="171e1-497">The database must be restored from backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-498">JET_errMissingCurrentLogFiles</span><span class="sxs-lookup"><span data-stu-id="171e1-498">JET_errMissingCurrentLogFiles</span></span><br />
<span data-ttu-id="171e1-499">-565</span><span class="sxs-lookup"><span data-stu-id="171e1-499">-565</span></span></p></td>
<td><p><span data-ttu-id="171e1-500">Alcuni file di registro correnti risultano mancanti per il ripristino continuo.</span><span class="sxs-lookup"><span data-stu-id="171e1-500">Some current log files are missing for continuous restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-501">JET_errDbTimeTooOld</span><span class="sxs-lookup"><span data-stu-id="171e1-501">JET_errDbTimeTooOld</span></span><br />
<span data-ttu-id="171e1-502">-566</span><span class="sxs-lookup"><span data-stu-id="171e1-502">-566</span></span></p></td>
<td><p><span data-ttu-id="171e1-503">Il valore di dbtime in una pagina è inferiore a quello di dbtimeBefore nel record.</span><span class="sxs-lookup"><span data-stu-id="171e1-503">The dbtime on a page is smaller than the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-504">JET_errDbTimeTooNew</span><span class="sxs-lookup"><span data-stu-id="171e1-504">JET_errDbTimeTooNew</span></span><br />
<span data-ttu-id="171e1-505">-567</span><span class="sxs-lookup"><span data-stu-id="171e1-505">-567</span></span></p></td>
<td><p><span data-ttu-id="171e1-506">Il dbtime in una pagina è in anticipo di dbtimeBefore nel record.</span><span class="sxs-lookup"><span data-stu-id="171e1-506">The dbtime on a page is in advance of the dbtimeBefore that is in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-507">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="171e1-507">JET_errMissingFileToBackup</span></span><br />
<span data-ttu-id="171e1-508">-569</span><span class="sxs-lookup"><span data-stu-id="171e1-508">-569</span></span></p></td>
<td><p><span data-ttu-id="171e1-509">Alcuni file di patch del database o di log mancanti durante il backup.</span><span class="sxs-lookup"><span data-stu-id="171e1-509">Some log or database patch files were missing during the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-510">JET_errLogTornWriteDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="171e1-510">JET_errLogTornWriteDuringHardRestore</span></span><br />
<span data-ttu-id="171e1-511">-570</span><span class="sxs-lookup"><span data-stu-id="171e1-511">-570</span></span></p></td>
<td><p><span data-ttu-id="171e1-512">È stata rilevata una scrittura incompleta in un backup impostato durante un ripristino a freddo.</span><span class="sxs-lookup"><span data-stu-id="171e1-512">A torn write was detected in a backup that was set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-513">JET_errLogTornWriteDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="171e1-513">JET_errLogTornWriteDuringHardRecovery</span></span><br />
<span data-ttu-id="171e1-514">-571</span><span class="sxs-lookup"><span data-stu-id="171e1-514">-571</span></span></p></td>
<td><p><span data-ttu-id="171e1-515">È stata rilevata una scrittura incompleta durante un ripristino rigido (il log non faceva parte di un set di backup).</span><span class="sxs-lookup"><span data-stu-id="171e1-515">A torn write was detected during a hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-516">JET_errLogCorruptDuringHardRestore</span><span class="sxs-lookup"><span data-stu-id="171e1-516">JET_errLogCorruptDuringHardRestore</span></span><br />
<span data-ttu-id="171e1-517">-573</span><span class="sxs-lookup"><span data-stu-id="171e1-517">-573</span></span></p></td>
<td><p><span data-ttu-id="171e1-518">Il danneggiamento è stato rilevato in un set di backup durante un ripristino a freddo.</span><span class="sxs-lookup"><span data-stu-id="171e1-518">Corruption was detected in a backup set during a hard restore.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-519">JET_errLogCorruptDuringHardRecovery</span><span class="sxs-lookup"><span data-stu-id="171e1-519">JET_errLogCorruptDuringHardRecovery</span></span><br />
<span data-ttu-id="171e1-520">-574</span><span class="sxs-lookup"><span data-stu-id="171e1-520">-574</span></span></p></td>
<td><p><span data-ttu-id="171e1-521">Il danneggiamento è stato rilevato durante il ripristino rigido (il log non faceva parte di un set di backup).</span><span class="sxs-lookup"><span data-stu-id="171e1-521">Corruption was detected during hard recovery (the log was not part of a backup set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-522">JET_errMustDisableLoggingForDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="171e1-522">JET_errMustDisableLoggingForDbUpgrade</span></span><br />
<span data-ttu-id="171e1-523">-575</span><span class="sxs-lookup"><span data-stu-id="171e1-523">-575</span></span></p></td>
<td><p><span data-ttu-id="171e1-524">Non è possibile abilitare la registrazione durante il tentativo di aggiornamento di un database.</span><span class="sxs-lookup"><span data-stu-id="171e1-524">Logging cannot be enabled while attempting to upgrade a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-525">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="171e1-525">JET_errBadRestoreTargetInstance</span></span><br />
<span data-ttu-id="171e1-526">-577</span><span class="sxs-lookup"><span data-stu-id="171e1-526">-577</span></span></p></td>
<td><p><span data-ttu-id="171e1-527">Il TargetInstance specificato per il ripristino non è stato trovato o i file di log non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="171e1-527">Either the TargetInstance that was specified for restore has not been found or the log files do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-528">JET_errRecoveredWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="171e1-528">JET_errRecoveredWithoutUndo</span></span><br />
<span data-ttu-id="171e1-529">-579</span><span class="sxs-lookup"><span data-stu-id="171e1-529">-579</span></span></p></td>
<td><p><span data-ttu-id="171e1-530">Il motore di database ha rieseguito correttamente tutte le operazioni nel log delle transazioni per eseguire un ripristino di arresto anomalo, ma il chiamante ha scelto di arrestare il ripristino senza eseguire il rollback degli aggiornamenti non sottoposti a commit.</span><span class="sxs-lookup"><span data-stu-id="171e1-530">The database engine successfully replayed all operations in the transaction log to perform a crash recovery but the caller elected to stop recovery without rolling back uncommitted updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-531">JET_errDatabasesNotFromSameSnapshot</span><span class="sxs-lookup"><span data-stu-id="171e1-531">JET_errDatabasesNotFromSameSnapshot</span></span><br />
<span data-ttu-id="171e1-532">-580</span><span class="sxs-lookup"><span data-stu-id="171e1-532">-580</span></span></p></td>
<td><p><span data-ttu-id="171e1-533">I database da ripristinare non appartengono allo stesso backup della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="171e1-533">The databases to be restored are not from the same shadow copy backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-534">JET_errSoftRecoveryOnSnapshot</span><span class="sxs-lookup"><span data-stu-id="171e1-534">JET_errSoftRecoveryOnSnapshot</span></span><br />
<span data-ttu-id="171e1-535">-581</span><span class="sxs-lookup"><span data-stu-id="171e1-535">-581</span></span></p></td>
<td><p><span data-ttu-id="171e1-536">Il ripristino di un database da un set di backup di copie shadow prevede un ripristino soft.</span><span class="sxs-lookup"><span data-stu-id="171e1-536">There is a soft recovery on a database from a shadow copy backup set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-537">JET_errUnicodeTranslationBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="171e1-537">JET_errUnicodeTranslationBufferTooSmall</span></span><br />
<span data-ttu-id="171e1-538">-601</span><span class="sxs-lookup"><span data-stu-id="171e1-538">-601</span></span></p></td>
<td><p><span data-ttu-id="171e1-539">Il buffer della traduzione Unicode è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="171e1-539">The Unicode translation buffer is too small.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-540">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="171e1-540">JET_errUnicodeTranslationFail</span></span><br />
<span data-ttu-id="171e1-541">-602</span><span class="sxs-lookup"><span data-stu-id="171e1-541">-602</span></span></p></td>
<td><p><span data-ttu-id="171e1-542">La normalizzazione Unicode non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="171e1-542">The Unicode normalization failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-543">JET_errUnicodeNormalizationNotSupported</span><span class="sxs-lookup"><span data-stu-id="171e1-543">JET_errUnicodeNormalizationNotSupported</span></span><br />
<span data-ttu-id="171e1-544">-603</span><span class="sxs-lookup"><span data-stu-id="171e1-544">-603</span></span></p></td>
<td><p><span data-ttu-id="171e1-545">Il sistema operativo non fornisce il supporto per la normalizzazione Unicode e non è stato specificato un callback di normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="171e1-545">The operating system does not provide support for Unicode normalization and a normalization callback was not specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-546">JET_errExistingLogFileHasBadSignature</span><span class="sxs-lookup"><span data-stu-id="171e1-546">JET_errExistingLogFileHasBadSignature</span></span><br />
<span data-ttu-id="171e1-547">-610</span><span class="sxs-lookup"><span data-stu-id="171e1-547">-610</span></span></p></td>
<td><p><span data-ttu-id="171e1-548">Firma non valida per il file di log esistente.</span><span class="sxs-lookup"><span data-stu-id="171e1-548">The existing log file has a bad signature.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-549">JET_errExistingLogFileIsNotContiguous</span><span class="sxs-lookup"><span data-stu-id="171e1-549">JET_errExistingLogFileIsNotContiguous</span></span><br />
<span data-ttu-id="171e1-550">-611</span><span class="sxs-lookup"><span data-stu-id="171e1-550">-611</span></span></p></td>
<td><p><span data-ttu-id="171e1-551">Un file di log esistente non è contiguo.</span><span class="sxs-lookup"><span data-stu-id="171e1-551">An existing log file is not contiguous.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-552">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="171e1-552">JET_errLogReadVerifyFailure</span></span><br />
<span data-ttu-id="171e1-553">-612</span><span class="sxs-lookup"><span data-stu-id="171e1-553">-612</span></span></p></td>
<td><p><span data-ttu-id="171e1-554">Si è verificato un errore di checksum nel file di log durante il backup.</span><span class="sxs-lookup"><span data-stu-id="171e1-554">A checksum error was found in the log file during backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-555">JET_errSLVReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="171e1-555">JET_errSLVReadVerifyFailure</span></span><br />
<span data-ttu-id="171e1-556">-613</span><span class="sxs-lookup"><span data-stu-id="171e1-556">-613</span></span></p></td>
<td><p><span data-ttu-id="171e1-557">Questo flag è riservato.</span><span class="sxs-lookup"><span data-stu-id="171e1-557">This flag is reserved.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-558">JET_errCheckpointDepthTooDeep</span><span class="sxs-lookup"><span data-stu-id="171e1-558">JET_errCheckpointDepthTooDeep</span></span><br />
<span data-ttu-id="171e1-559">-614</span><span class="sxs-lookup"><span data-stu-id="171e1-559">-614</span></span></p></td>
<td><p><span data-ttu-id="171e1-560">Troppe generazioni in attesa tra il checkpoint e la generazione corrente.</span><span class="sxs-lookup"><span data-stu-id="171e1-560">There are too many outstanding generations between the checkpoint and the current generation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-561">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="171e1-561">JET_errRestoreOfNonBackupDatabase</span></span><br />
<span data-ttu-id="171e1-562">-615</span><span class="sxs-lookup"><span data-stu-id="171e1-562">-615</span></span></p></td>
<td><p><span data-ttu-id="171e1-563">Si è tentato di eseguire un ripristino rigido in un database che non era un database di backup.</span><span class="sxs-lookup"><span data-stu-id="171e1-563">A hard recovery was attempted on a database that was not a backup database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-564">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="171e1-564">JET_errInvalidGrbit</span></span><br />
<span data-ttu-id="171e1-565">-900</span><span class="sxs-lookup"><span data-stu-id="171e1-565">-900</span></span></p></td>
<td><p><span data-ttu-id="171e1-566">Parametro grbit non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-566">There is an invalid grbit parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-567">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="171e1-567">JET_errTermInProgress</span></span><br />
<span data-ttu-id="171e1-568">-1000</span><span class="sxs-lookup"><span data-stu-id="171e1-568">-1000</span></span></p></td>
<td><p><span data-ttu-id="171e1-569">Terminazione in corso.</span><span class="sxs-lookup"><span data-stu-id="171e1-569">Termination is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-570">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="171e1-570">JET_errFeatureNotAvailable</span></span><br />
<span data-ttu-id="171e1-571">-1001</span><span class="sxs-lookup"><span data-stu-id="171e1-571">-1001</span></span></p></td>
<td><p><span data-ttu-id="171e1-572">Questo elemento API non è supportato.</span><span class="sxs-lookup"><span data-stu-id="171e1-572">This API element is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-573">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="171e1-573">JET_errInvalidName</span></span><br />
<span data-ttu-id="171e1-574">-1002</span><span class="sxs-lookup"><span data-stu-id="171e1-574">-1002</span></span></p></td>
<td><p><span data-ttu-id="171e1-575">È in uso un nome non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-575">An invalid name is being used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-576">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="171e1-576">JET_errInvalidParameter</span></span><br />
<span data-ttu-id="171e1-577">-1003</span><span class="sxs-lookup"><span data-stu-id="171e1-577">-1003</span></span></p></td>
<td><p><span data-ttu-id="171e1-578">Viene usato un parametro API non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-578">An invalid API parameter is being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-579">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="171e1-579">JET_errDatabaseFileReadOnly</span></span><br />
<span data-ttu-id="171e1-580">-1008</span><span class="sxs-lookup"><span data-stu-id="171e1-580">-1008</span></span></p></td>
<td><p><span data-ttu-id="171e1-581">Tentativo di connessione a un file di database di sola lettura per operazioni di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="171e1-581">There was an attempt to attach to a read-only database file for read/write operations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-582">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="171e1-582">JET_errInvalidDatabaseId</span></span><br />
<span data-ttu-id="171e1-583">-1010</span><span class="sxs-lookup"><span data-stu-id="171e1-583">-1010</span></span></p></td>
<td><p><span data-ttu-id="171e1-584">ID database non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-584">There is an invalid database ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-585">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="171e1-585">JET_errOutOfMemory</span></span><br />
<span data-ttu-id="171e1-586">-1011</span><span class="sxs-lookup"><span data-stu-id="171e1-586">-1011</span></span></p></td>
<td><p><span data-ttu-id="171e1-587">Memoria insufficiente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="171e1-587">The system is out of memory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-588">JET_errOutOfDatabaseSpace</span><span class="sxs-lookup"><span data-stu-id="171e1-588">JET_errOutOfDatabaseSpace</span></span><br />
<span data-ttu-id="171e1-589">-1012</span><span class="sxs-lookup"><span data-stu-id="171e1-589">-1012</span></span></p></td>
<td><p><span data-ttu-id="171e1-590">È stata raggiunta la dimensione massima del database.</span><span class="sxs-lookup"><span data-stu-id="171e1-590">The maximum database size has been reached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-591">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="171e1-591">JET_errOutOfCursors</span></span><br />
<span data-ttu-id="171e1-592">-1013</span><span class="sxs-lookup"><span data-stu-id="171e1-592">-1013</span></span></p></td>
<td><p><span data-ttu-id="171e1-593">La tabella non è presente nei cursori.</span><span class="sxs-lookup"><span data-stu-id="171e1-593">The table is out of cursors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-594">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="171e1-594">JET_errOutOfBuffers</span></span><br />
<span data-ttu-id="171e1-595">-1014</span><span class="sxs-lookup"><span data-stu-id="171e1-595">-1014</span></span></p></td>
<td><p><span data-ttu-id="171e1-596">Il database è esterno ai buffer di pagina.</span><span class="sxs-lookup"><span data-stu-id="171e1-596">The database is out of page buffers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-597">JET_errTooManyIndexes</span><span class="sxs-lookup"><span data-stu-id="171e1-597">JET_errTooManyIndexes</span></span><br />
<span data-ttu-id="171e1-598">-1015</span><span class="sxs-lookup"><span data-stu-id="171e1-598">-1015</span></span></p></td>
<td><p><span data-ttu-id="171e1-599">Troppi indici.</span><span class="sxs-lookup"><span data-stu-id="171e1-599">There are too many indexes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-600">JET_errTooManyKeys</span><span class="sxs-lookup"><span data-stu-id="171e1-600">JET_errTooManyKeys</span></span><br />
<span data-ttu-id="171e1-601">-1016</span><span class="sxs-lookup"><span data-stu-id="171e1-601">-1016</span></span></p></td>
<td><p><span data-ttu-id="171e1-602">Il numero di colonne in un indice è eccessivo.</span><span class="sxs-lookup"><span data-stu-id="171e1-602">There are too many columns in an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-603">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="171e1-603">JET_errRecordDeleted</span></span><br />
<span data-ttu-id="171e1-604">-1017</span><span class="sxs-lookup"><span data-stu-id="171e1-604">-1017</span></span></p></td>
<td><p><span data-ttu-id="171e1-605">Il record è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="171e1-605">The record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-606">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="171e1-606">JET_errReadVerifyFailure</span></span><br />
<span data-ttu-id="171e1-607">-1018</span><span class="sxs-lookup"><span data-stu-id="171e1-607">-1018</span></span></p></td>
<td><p><span data-ttu-id="171e1-608">Si è verificato un errore di checksum in una pagina del database.</span><span class="sxs-lookup"><span data-stu-id="171e1-608">There is a checksum error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-609">JET_errPageNotInitialized</span><span class="sxs-lookup"><span data-stu-id="171e1-609">JET_errPageNotInitialized</span></span><br />
<span data-ttu-id="171e1-610">-1019</span><span class="sxs-lookup"><span data-stu-id="171e1-610">-1019</span></span></p></td>
<td><p><span data-ttu-id="171e1-611">È presente una pagina di database vuota.</span><span class="sxs-lookup"><span data-stu-id="171e1-611">There is a blank database page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-612">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="171e1-612">JET_errOutOfFileHandles</span></span><br />
<span data-ttu-id="171e1-613">-1020</span><span class="sxs-lookup"><span data-stu-id="171e1-613">-1020</span></span></p></td>
<td><p><span data-ttu-id="171e1-614">Nessun handle di file.</span><span class="sxs-lookup"><span data-stu-id="171e1-614">There are no file handles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-615">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="171e1-615">JET_errDiskIO</span></span><br />
<span data-ttu-id="171e1-616">-1022</span><span class="sxs-lookup"><span data-stu-id="171e1-616">-1022</span></span></p></td>
<td><p><span data-ttu-id="171e1-617">Si è verificato un errore di i/o del disco.</span><span class="sxs-lookup"><span data-stu-id="171e1-617">There is a disk IO error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-618">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="171e1-618">JET_errInvalidPath</span></span><br />
<span data-ttu-id="171e1-619">-1023</span><span class="sxs-lookup"><span data-stu-id="171e1-619">-1023</span></span></p></td>
<td><p><span data-ttu-id="171e1-620">Percorso di file non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-620">There is an invalid file path.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-621">JET_errInvalidSystemPath</span><span class="sxs-lookup"><span data-stu-id="171e1-621">JET_errInvalidSystemPath</span></span><br />
<span data-ttu-id="171e1-622">-1024</span><span class="sxs-lookup"><span data-stu-id="171e1-622">-1024</span></span></p></td>
<td><p><span data-ttu-id="171e1-623">Il percorso di sistema non è valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-623">There is an invalid system path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-624">JET_errInvalidLogDirectory</span><span class="sxs-lookup"><span data-stu-id="171e1-624">JET_errInvalidLogDirectory</span></span><br />
<span data-ttu-id="171e1-625">-1025</span><span class="sxs-lookup"><span data-stu-id="171e1-625">-1025</span></span></p></td>
<td><p><span data-ttu-id="171e1-626">Directory log non valida.</span><span class="sxs-lookup"><span data-stu-id="171e1-626">There is an invalid log directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-627">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="171e1-627">JET_errRecordTooBig</span></span><br />
<span data-ttu-id="171e1-628">-1026</span><span class="sxs-lookup"><span data-stu-id="171e1-628">-1026</span></span></p></td>
<td><p><span data-ttu-id="171e1-629">Il record è più grande della dimensione massima.</span><span class="sxs-lookup"><span data-stu-id="171e1-629">The record is larger than maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-630">JET_errTooManyOpenDatabases</span><span class="sxs-lookup"><span data-stu-id="171e1-630">JET_errTooManyOpenDatabases</span></span><br />
<span data-ttu-id="171e1-631">-1027</span><span class="sxs-lookup"><span data-stu-id="171e1-631">-1027</span></span></p></td>
<td><p><span data-ttu-id="171e1-632">Troppi database aperti.</span><span class="sxs-lookup"><span data-stu-id="171e1-632">There are too many open databases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-633">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="171e1-633">JET_errInvalidDatabase</span></span><br />
<span data-ttu-id="171e1-634">-1028</span><span class="sxs-lookup"><span data-stu-id="171e1-634">-1028</span></span></p></td>
<td><p><span data-ttu-id="171e1-635">Non si tratta di un file di database.</span><span class="sxs-lookup"><span data-stu-id="171e1-635">This is not a database file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-636">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="171e1-636">JET_errNotInitialized</span></span><br />
<span data-ttu-id="171e1-637">-1029</span><span class="sxs-lookup"><span data-stu-id="171e1-637">-1029</span></span></p></td>
<td><p><span data-ttu-id="171e1-638">Il motore di database non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="171e1-638">The database engine has not been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-639">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="171e1-639">JET_errAlreadyInitialized</span></span><br />
<span data-ttu-id="171e1-640">-1030</span><span class="sxs-lookup"><span data-stu-id="171e1-640">-1030</span></span></p></td>
<td><p><span data-ttu-id="171e1-641">Il motore di database è già inizializzato.</span><span class="sxs-lookup"><span data-stu-id="171e1-641">The database engine is already initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-642">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="171e1-642">JET_errInitInProgress</span></span><br />
<span data-ttu-id="171e1-643">-1031</span><span class="sxs-lookup"><span data-stu-id="171e1-643">-1031</span></span></p></td>
<td><p><span data-ttu-id="171e1-644">È in corso l'inizializzazione del motore di database.</span><span class="sxs-lookup"><span data-stu-id="171e1-644">The database engine is being initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-645">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="171e1-645">JET_errFileAccessDenied</span></span><br />
<span data-ttu-id="171e1-646">-1032</span><span class="sxs-lookup"><span data-stu-id="171e1-646">-1032</span></span></p></td>
<td><p><span data-ttu-id="171e1-647">Non è possibile accedere al file perché il file è bloccato o in uso.</span><span class="sxs-lookup"><span data-stu-id="171e1-647">The file cannot be accessed because the file is locked or in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-648">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="171e1-648">JET_errBufferTooSmall</span></span><br />
<span data-ttu-id="171e1-649">-1038</span><span class="sxs-lookup"><span data-stu-id="171e1-649">-1038</span></span></p></td>
<td><p><span data-ttu-id="171e1-650">Il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="171e1-650">The buffer is too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-651">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="171e1-651">JET_errTooManyColumns</span></span><br />
<span data-ttu-id="171e1-652">-1040</span><span class="sxs-lookup"><span data-stu-id="171e1-652">-1040</span></span></p></td>
<td><p><span data-ttu-id="171e1-653">Sono state definite troppe colonne.</span><span class="sxs-lookup"><span data-stu-id="171e1-653">Too many columns are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-654">JET_errContainerNotEmpty</span><span class="sxs-lookup"><span data-stu-id="171e1-654">JET_errContainerNotEmpty</span></span><br />
<span data-ttu-id="171e1-655">-1043</span><span class="sxs-lookup"><span data-stu-id="171e1-655">-1043</span></span></p></td>
<td><p><span data-ttu-id="171e1-656">Il contenitore non è vuoto.</span><span class="sxs-lookup"><span data-stu-id="171e1-656">The container is not empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-657">JET_errInvalidFilename</span><span class="sxs-lookup"><span data-stu-id="171e1-657">JET_errInvalidFilename</span></span><br />
<span data-ttu-id="171e1-658">-1044</span><span class="sxs-lookup"><span data-stu-id="171e1-658">-1044</span></span></p></td>
<td><p><span data-ttu-id="171e1-659">Il nome file non è valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-659">The filename is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-660">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="171e1-660">JET_errInvalidBookmark</span></span><br />
<span data-ttu-id="171e1-661">-1045</span><span class="sxs-lookup"><span data-stu-id="171e1-661">-1045</span></span></p></td>
<td><p><span data-ttu-id="171e1-662">Segnalibro non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-662">There is an invalid bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-663">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="171e1-663">JET_errColumnInUse</span></span><br />
<span data-ttu-id="171e1-664">-1046</span><span class="sxs-lookup"><span data-stu-id="171e1-664">-1046</span></span></p></td>
<td><p><span data-ttu-id="171e1-665">La colonna utilizzata si trova in un indice.</span><span class="sxs-lookup"><span data-stu-id="171e1-665">The column used is in an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-666">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="171e1-666">JET_errInvalidBufferSize</span></span><br />
<span data-ttu-id="171e1-667">-1047</span><span class="sxs-lookup"><span data-stu-id="171e1-667">-1047</span></span></p></td>
<td><p><span data-ttu-id="171e1-668">Il buffer di dati non corrisponde alle dimensioni della colonna.</span><span class="sxs-lookup"><span data-stu-id="171e1-668">The data buffer does not match the column size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-669">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="171e1-669">JET_errColumnNotUpdatable</span></span><br />
<span data-ttu-id="171e1-670">-1048</span><span class="sxs-lookup"><span data-stu-id="171e1-670">-1048</span></span></p></td>
<td><p><span data-ttu-id="171e1-671">Impossibile impostare il valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="171e1-671">The column value cannot be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-672">JET_errIndexInUse</span><span class="sxs-lookup"><span data-stu-id="171e1-672">JET_errIndexInUse</span></span><br />
<span data-ttu-id="171e1-673">-1051</span><span class="sxs-lookup"><span data-stu-id="171e1-673">-1051</span></span></p></td>
<td><p><span data-ttu-id="171e1-674">L'indice è in uso.</span><span class="sxs-lookup"><span data-stu-id="171e1-674">The index is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-675">JET_errLinkNotSupported</span><span class="sxs-lookup"><span data-stu-id="171e1-675">JET_errLinkNotSupported</span></span><br />
<span data-ttu-id="171e1-676">-1052</span><span class="sxs-lookup"><span data-stu-id="171e1-676">-1052</span></span></p></td>
<td><p><span data-ttu-id="171e1-677">Il supporto del collegamento non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="171e1-677">The link support is unavailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-678">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="171e1-678">JET_errNullKeyDisallowed</span></span><br />
<span data-ttu-id="171e1-679">-1053</span><span class="sxs-lookup"><span data-stu-id="171e1-679">-1053</span></span></p></td>
<td><p><span data-ttu-id="171e1-680">Chiavi null non consentite in un indice.</span><span class="sxs-lookup"><span data-stu-id="171e1-680">Null keys are not allowed on an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-681">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="171e1-681">JET_errNotInTransaction</span></span><br />
<span data-ttu-id="171e1-682">-1054</span><span class="sxs-lookup"><span data-stu-id="171e1-682">-1054</span></span></p></td>
<td><p><span data-ttu-id="171e1-683">L'operazione deve essere eseguita all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="171e1-683">The operation must occur within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-684">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="171e1-684">JET_errTooManyActiveUsers</span></span><br />
<span data-ttu-id="171e1-685">-1059</span><span class="sxs-lookup"><span data-stu-id="171e1-685">-1059</span></span></p></td>
<td><p><span data-ttu-id="171e1-686">Troppi utenti di database attivi</span><span class="sxs-lookup"><span data-stu-id="171e1-686">There are too many active database users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-687">JET_errInvalidCountry</span><span class="sxs-lookup"><span data-stu-id="171e1-687">JET_errInvalidCountry</span></span><br />
<span data-ttu-id="171e1-688">-1061</span><span class="sxs-lookup"><span data-stu-id="171e1-688">-1061</span></span></p></td>
<td><p><span data-ttu-id="171e1-689">È presente un codice paese non valido o sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="171e1-689">There is an invalid or unknown country code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-690">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="171e1-690">JET_errInvalidLanguageId</span></span><br />
<span data-ttu-id="171e1-691">-1062</span><span class="sxs-lookup"><span data-stu-id="171e1-691">-1062</span></span></p></td>
<td><p><span data-ttu-id="171e1-692">ID lingua non valido o sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="171e1-692">There is an invalid or unknown language ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-693">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="171e1-693">JET_errInvalidCodePage</span></span><br />
<span data-ttu-id="171e1-694">-1063</span><span class="sxs-lookup"><span data-stu-id="171e1-694">-1063</span></span></p></td>
<td><p><span data-ttu-id="171e1-695">Tabella codici non valida o sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="171e1-695">There is an invalid or unknown code page.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-696">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="171e1-696">JET_errInvalidLCMapStringFlags</span></span><br />
<span data-ttu-id="171e1-697">-1064</span><span class="sxs-lookup"><span data-stu-id="171e1-697">-1064</span></span></p></td>
<td><p><span data-ttu-id="171e1-698">Flag non validi utilizzati per <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span><span class="sxs-lookup"><span data-stu-id="171e1-698">There are invalid flags being used for <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-699">JET_errVersionStoreEntryTooBig</span><span class="sxs-lookup"><span data-stu-id="171e1-699">JET_errVersionStoreEntryTooBig</span></span><br />
<span data-ttu-id="171e1-700">-1065</span><span class="sxs-lookup"><span data-stu-id="171e1-700">-1065</span></span></p></td>
<td><p><span data-ttu-id="171e1-701">Si è tentato di creare una voce dell'archivio versioni (RCE) più grande di un bucket di versione.</span><span class="sxs-lookup"><span data-stu-id="171e1-701">There was an attempt to create a version store entry (RCE) that was larger than a version bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="171e1-702">JET_errVersionStoreOutOfMemoryAndCleanupTimedOut</span></span><br />
<span data-ttu-id="171e1-703">-1066</span><span class="sxs-lookup"><span data-stu-id="171e1-703">-1066</span></span></p></td>
<td><p><span data-ttu-id="171e1-704">Memoria esaurita per l'archivio versioni. Impossibile completare il tentativo di pulizia.</span><span class="sxs-lookup"><span data-stu-id="171e1-704">The version store is out of memory and the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-705">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="171e1-705">JET_errVersionStoreOutOfMemory</span></span><br />
<span data-ttu-id="171e1-706">-1069</span><span class="sxs-lookup"><span data-stu-id="171e1-706">-1069</span></span></p></td>
<td><p><span data-ttu-id="171e1-707">Memoria insufficiente nell'archivio versioni ed è già stato effettuato un tentativo di pulizia.</span><span class="sxs-lookup"><span data-stu-id="171e1-707">The version store is out of memory and a cleanup was already attempted).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-708">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="171e1-708">JET_errCannotIndex</span></span><br />
<span data-ttu-id="171e1-709">-1071</span><span class="sxs-lookup"><span data-stu-id="171e1-709">-1071</span></span></p></td>
<td><p><span data-ttu-id="171e1-710">Non è possibile indicizzare le colonne escrow e SLV.</span><span class="sxs-lookup"><span data-stu-id="171e1-710">The escrow and SLV columns cannot be indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-711">JET_errRecordNotDeleted</span><span class="sxs-lookup"><span data-stu-id="171e1-711">JET_errRecordNotDeleted</span></span><br />
<span data-ttu-id="171e1-712">-1072</span><span class="sxs-lookup"><span data-stu-id="171e1-712">-1072</span></span></p></td>
<td><p><span data-ttu-id="171e1-713">Il record non è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="171e1-713">The record has not been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-714">JET_errTooManyMempoolEntries</span><span class="sxs-lookup"><span data-stu-id="171e1-714">JET_errTooManyMempoolEntries</span></span><br />
<span data-ttu-id="171e1-715">-1073</span><span class="sxs-lookup"><span data-stu-id="171e1-715">-1073</span></span></p></td>
<td><p><span data-ttu-id="171e1-716">Sono state richieste troppe voci mempool.</span><span class="sxs-lookup"><span data-stu-id="171e1-716">Too many mempool entries have been requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-717">JET_errOutOfObjectIDs</span><span class="sxs-lookup"><span data-stu-id="171e1-717">JET_errOutOfObjectIDs</span></span><br />
<span data-ttu-id="171e1-718">-1074</span><span class="sxs-lookup"><span data-stu-id="171e1-718">-1074</span></span></p></td>
<td><p><span data-ttu-id="171e1-719">Il database non è presente nell'albero B + ObjectID, quindi è necessario eseguire una deframmentazione non in linea per recuperare ObjectID liberati o non usati.</span><span class="sxs-lookup"><span data-stu-id="171e1-719">The database is out of B+ tree ObjectIDs so an offline defragmentation must be performed to reclaim freed or unused ObjectIds.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-720">JET_errOutOfLongValueIDs</span><span class="sxs-lookup"><span data-stu-id="171e1-720">JET_errOutOfLongValueIDs</span></span><br />
<span data-ttu-id="171e1-721">-1075</span><span class="sxs-lookup"><span data-stu-id="171e1-721">-1075</span></span></p></td>
<td><p><span data-ttu-id="171e1-722">Il contatore ID valore Long ha raggiunto il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="171e1-722">The Long-value ID counter has reached the maximum value.</span></span> <span data-ttu-id="171e1-723">È necessario eseguire una deframmentazione non in linea per recuperare la LongValueIDs gratuita o inutilizzata.</span><span class="sxs-lookup"><span data-stu-id="171e1-723">An offline defragmentation must be performed to reclaim free or unused LongValueIDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-724">JET_errOutOfAutoincrementValues</span><span class="sxs-lookup"><span data-stu-id="171e1-724">JET_errOutOfAutoincrementValues</span></span><br />
<span data-ttu-id="171e1-725">-1076</span><span class="sxs-lookup"><span data-stu-id="171e1-725">-1076</span></span></p></td>
<td><p><span data-ttu-id="171e1-726">Il contatore di incremento automatico ha raggiunto il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="171e1-726">The auto-increment counter has reached the maximum value.</span></span> <span data-ttu-id="171e1-727">Una deframmentazione non in linea non sarà in grado di recuperare i valori di incremento automatico gratuiti o non usati.</span><span class="sxs-lookup"><span data-stu-id="171e1-727">An offline defragmentation will not be able to reclaim free or unused auto-increment values).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-728">JET_errOutOfDbtimeValues</span><span class="sxs-lookup"><span data-stu-id="171e1-728">JET_errOutOfDbtimeValues</span></span><br />
<span data-ttu-id="171e1-729">-1077</span><span class="sxs-lookup"><span data-stu-id="171e1-729">-1077</span></span></p></td>
<td><p><span data-ttu-id="171e1-730">Il contatore dbtime ha raggiunto il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="171e1-730">The Dbtime counter has reached the maximum value.</span></span> <span data-ttu-id="171e1-731">È necessario eseguire una deframmentazione non in linea per recuperare i valori dbtime liberi o inutilizzati.</span><span class="sxs-lookup"><span data-stu-id="171e1-731">An offline defragmentation must be performed to reclaim free or unused Dbtime values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-732">JET_errOutOfSequentialIndexValues</span><span class="sxs-lookup"><span data-stu-id="171e1-732">JET_errOutOfSequentialIndexValues</span></span><br />
<span data-ttu-id="171e1-733">-1078</span><span class="sxs-lookup"><span data-stu-id="171e1-733">-1078</span></span></p></td>
<td><p><span data-ttu-id="171e1-734">Un contatore di indice sequenziale ha raggiunto il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="171e1-734">A sequential index counter has reached the maximum value.</span></span> <span data-ttu-id="171e1-735">È necessario eseguire una deframmentazione non in linea per recuperare i valori SequentialIndex liberi o inutilizzati.</span><span class="sxs-lookup"><span data-stu-id="171e1-735">An offline defragmentation must be performed to reclaim free or unused SequentialIndex values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-736">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="171e1-736">JET_errRunningInOneInstanceMode</span></span><br />
<span data-ttu-id="171e1-737">-1080</span><span class="sxs-lookup"><span data-stu-id="171e1-737">-1080</span></span></p></td>
<td><p><span data-ttu-id="171e1-738">Questa chiamata a istanze diverse ha la modalità a istanza singola abilitata.</span><span class="sxs-lookup"><span data-stu-id="171e1-738">This multi-instance call has the single-instance mode enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-739">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="171e1-739">JET_errRunningInMultiInstanceMode</span></span><br />
<span data-ttu-id="171e1-740">-1081</span><span class="sxs-lookup"><span data-stu-id="171e1-740">-1081</span></span></p></td>
<td><p><span data-ttu-id="171e1-741">Per questa chiamata a istanza singola è abilitata la modalità a istanze diverse.</span><span class="sxs-lookup"><span data-stu-id="171e1-741">This single-instance call has the multi-instance mode enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-742">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="171e1-742">JET_errSystemParamsAlreadySet</span></span><br />
<span data-ttu-id="171e1-743">-1082</span><span class="sxs-lookup"><span data-stu-id="171e1-743">-1082</span></span></p></td>
<td><p><span data-ttu-id="171e1-744">I parametri di sistema globali sono già stati impostati.</span><span class="sxs-lookup"><span data-stu-id="171e1-744">The global system parameters have already been set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-745">JET_errSystemPathInUse</span><span class="sxs-lookup"><span data-stu-id="171e1-745">JET_errSystemPathInUse</span></span><br />
<span data-ttu-id="171e1-746">-1083</span><span class="sxs-lookup"><span data-stu-id="171e1-746">-1083</span></span></p></td>
<td><p><span data-ttu-id="171e1-747">Il percorso di sistema è già in uso da un'altra istanza del database.</span><span class="sxs-lookup"><span data-stu-id="171e1-747">The system path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-748">JET_errLogFilePathInUse</span><span class="sxs-lookup"><span data-stu-id="171e1-748">JET_errLogFilePathInUse</span></span><br />
<span data-ttu-id="171e1-749">-1084</span><span class="sxs-lookup"><span data-stu-id="171e1-749">-1084</span></span></p></td>
<td><p><span data-ttu-id="171e1-750">Il percorso del file di log è già in uso da un'altra istanza del database.</span><span class="sxs-lookup"><span data-stu-id="171e1-750">The log file path is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-751">JET_errTempPathInUse</span><span class="sxs-lookup"><span data-stu-id="171e1-751">JET_errTempPathInUse</span></span><br />
<span data-ttu-id="171e1-752">-1085</span><span class="sxs-lookup"><span data-stu-id="171e1-752">-1085</span></span></p></td>
<td><p><span data-ttu-id="171e1-753">Il percorso del database temporaneo è già in uso da un'altra istanza di database.</span><span class="sxs-lookup"><span data-stu-id="171e1-753">The path to the temporary database is already being used by another database instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-754">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="171e1-754">JET_errInstanceNameInUse</span></span><br />
<span data-ttu-id="171e1-755">-1086</span><span class="sxs-lookup"><span data-stu-id="171e1-755">-1086</span></span></p></td>
<td><p><span data-ttu-id="171e1-756">Il nome dell'istanza è già in uso.</span><span class="sxs-lookup"><span data-stu-id="171e1-756">The instance name is already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-757">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="171e1-757">JET_errInstanceUnavailable</span></span><br />
<span data-ttu-id="171e1-758">-1090</span><span class="sxs-lookup"><span data-stu-id="171e1-758">-1090</span></span></p></td>
<td><p><span data-ttu-id="171e1-759">Impossibile utilizzare questa istanza perché si è verificato un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="171e1-759">This instance cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-760">JET_errDatabaseUnavailable</span><span class="sxs-lookup"><span data-stu-id="171e1-760">JET_errDatabaseUnavailable</span></span><br />
<span data-ttu-id="171e1-761">-1091</span><span class="sxs-lookup"><span data-stu-id="171e1-761">-1091</span></span></p></td>
<td><p><span data-ttu-id="171e1-762">Impossibile utilizzare il database perché si è verificato un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="171e1-762">This database cannot be used because it encountered a fatal error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span><span class="sxs-lookup"><span data-stu-id="171e1-763">JET_errInstanceUnavailableDueToFatalLogDiskFull</span></span><br />
<span data-ttu-id="171e1-764">-1092</span><span class="sxs-lookup"><span data-stu-id="171e1-764">-1092</span></span></p></td>
<td><p><span data-ttu-id="171e1-765">Non è possibile usare questa istanza perché si è verificato un errore di log-Disk-Full durante l'esecuzione di un'operazione, ad esempio un rollback di transazione, che non è in grado di tollerare l'errore.</span><span class="sxs-lookup"><span data-stu-id="171e1-765">This instance cannot be used because it encountered a log-disk-full error while performing an operation (such as a transaction rollback) that could not tolerate failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-766">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="171e1-766">JET_errOutOfSessions</span></span><br />
<span data-ttu-id="171e1-767">-1101</span><span class="sxs-lookup"><span data-stu-id="171e1-767">-1101</span></span></p></td>
<td><p><span data-ttu-id="171e1-768">Il database non è presente nelle sessioni.</span><span class="sxs-lookup"><span data-stu-id="171e1-768">The database is out of sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-769">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="171e1-769">JET_errWriteConflict</span></span><br />
<span data-ttu-id="171e1-770">-1102</span><span class="sxs-lookup"><span data-stu-id="171e1-770">-1102</span></span></p></td>
<td><p><span data-ttu-id="171e1-771">Il blocco di scrittura non è riuscito a causa dell'esistenza di un blocco di scrittura in attesa.</span><span class="sxs-lookup"><span data-stu-id="171e1-771">The write lock failed due to the existence of an outstanding write lock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-772">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="171e1-772">JET_errTransTooDeep</span></span><br />
<span data-ttu-id="171e1-773">-1103</span><span class="sxs-lookup"><span data-stu-id="171e1-773">-1103</span></span></p></td>
<td><p><span data-ttu-id="171e1-774">Le transazioni sono annidate troppo profondamente.</span><span class="sxs-lookup"><span data-stu-id="171e1-774">The transactions are nested too deeply.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-775">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="171e1-775">JET_errInvalidSesid</span></span><br />
<span data-ttu-id="171e1-776">-1104</span><span class="sxs-lookup"><span data-stu-id="171e1-776">-1104</span></span></p></td>
<td><p><span data-ttu-id="171e1-777">Handle di sessione non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-777">There is an invalid session handle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-778">JET_errWriteConflictPrimaryIndex</span><span class="sxs-lookup"><span data-stu-id="171e1-778">JET_errWriteConflictPrimaryIndex</span></span><br />
<span data-ttu-id="171e1-779">-1105</span><span class="sxs-lookup"><span data-stu-id="171e1-779">-1105</span></span></p></td>
<td><p><span data-ttu-id="171e1-780">Si è tentato di eseguire un aggiornamento su un indice primario non sottoposta a commit.</span><span class="sxs-lookup"><span data-stu-id="171e1-780">An update was attempted on an uncommitted primary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-781">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="171e1-781">JET_errInTransaction</span></span><br />
<span data-ttu-id="171e1-782">-1108</span><span class="sxs-lookup"><span data-stu-id="171e1-782">-1108</span></span></p></td>
<td><p><span data-ttu-id="171e1-783">Operazione non consentita all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="171e1-783">The operation is not allowed within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-784">JET_errRollbackRequired</span><span class="sxs-lookup"><span data-stu-id="171e1-784">JET_errRollbackRequired</span></span><br />
<span data-ttu-id="171e1-785">-1109</span><span class="sxs-lookup"><span data-stu-id="171e1-785">-1109</span></span></p></td>
<td><p><span data-ttu-id="171e1-786">È necessario eseguire il rollback della transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="171e1-786">The current transaction must be rolled back.</span></span> <span data-ttu-id="171e1-787">Non è possibile eseguire il commit e non è possibile avviarne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="171e1-787">It cannot be committed and a new one cannot be started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-788">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="171e1-788">JET_errTransReadOnly</span></span><br />
<span data-ttu-id="171e1-789">-1110</span><span class="sxs-lookup"><span data-stu-id="171e1-789">-1110</span></span></p></td>
<td><p><span data-ttu-id="171e1-790">Una transazione di sola lettura ha tentato di modificare il database.</span><span class="sxs-lookup"><span data-stu-id="171e1-790">A read-only transaction tried to modify the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-791">JET_errSessionWriteConflict</span><span class="sxs-lookup"><span data-stu-id="171e1-791">JET_errSessionWriteConflict</span></span><br />
<span data-ttu-id="171e1-792">-1111</span><span class="sxs-lookup"><span data-stu-id="171e1-792">-1111</span></span></p></td>
<td><p><span data-ttu-id="171e1-793">Si è tentato di sostituire lo stesso record con due cursori diversi nella stessa sessione.</span><span class="sxs-lookup"><span data-stu-id="171e1-793">There was an attempt to replace the same record by two different cursors in the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-794">JET_errRecordTooBigForBackwardCompatibility</span><span class="sxs-lookup"><span data-stu-id="171e1-794">JET_errRecordTooBigForBackwardCompatibility</span></span><br />
<span data-ttu-id="171e1-795">-1112</span><span class="sxs-lookup"><span data-stu-id="171e1-795">-1112</span></span></p></td>
<td><p><span data-ttu-id="171e1-796">Il record sarebbe troppo grande se rappresentato in un formato di database da una versione precedente di Jet.</span><span class="sxs-lookup"><span data-stu-id="171e1-796">The record would be too big if represented in a database format from a previous version of Jet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-797">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="171e1-797">JET_errCannotMaterializeForwardOnlySort</span></span><br />
<span data-ttu-id="171e1-798">-1113</span><span class="sxs-lookup"><span data-stu-id="171e1-798">-1113</span></span></p></td>
<td><p><span data-ttu-id="171e1-799">Non è stato possibile creare la tabella temporanea a causa di parametri che sono in conflitto con JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="171e1-799">The temporary table could not be created due to parameters that conflict with JET_bitTTForwardOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-800">JET_errSesidTableIdMismatch</span><span class="sxs-lookup"><span data-stu-id="171e1-800">JET_errSesidTableIdMismatch</span></span><br />
<span data-ttu-id="171e1-801">-1114</span><span class="sxs-lookup"><span data-stu-id="171e1-801">-1114</span></span></p></td>
<td><p><span data-ttu-id="171e1-802">Non è possibile usare l'handle di sessione con l'ID tabella perché non è stato usato per crearlo.</span><span class="sxs-lookup"><span data-stu-id="171e1-802">The session handle cannot be used with the table id because it was not used to create it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-803">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="171e1-803">JET_errInvalidInstance</span></span><br />
<span data-ttu-id="171e1-804">-1115</span><span class="sxs-lookup"><span data-stu-id="171e1-804">-1115</span></span></p></td>
<td><p><span data-ttu-id="171e1-805">L'handle dell'istanza non è valido o fa riferimento a un'istanza di che è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="171e1-805">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-806">JET_errReadLostFlushVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="171e1-806">JET_errReadLostFlushVerifyFailure</span></span><br />
<span data-ttu-id="171e1-807">-1119</span><span class="sxs-lookup"><span data-stu-id="171e1-807">-1119</span></span></p></td>
<td><p><span data-ttu-id="171e1-808">La lettura della pagina del database dal disco presenta una scrittura precedente non rappresentata nella pagina.</span><span class="sxs-lookup"><span data-stu-id="171e1-808">The database page read from disk had a previous write not represented on the page.</span></span> <span data-ttu-id="171e1-809">Disponibile in Windows 8 e versioni successive per il client e Windows Server 2012 e versioni successive per il server.</span><span class="sxs-lookup"><span data-stu-id="171e1-809">Available on Windows 8 and later for client, and Windows Server 2012 and later for server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-810">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="171e1-810">JET_errDatabaseDuplicate</span></span><br />
<span data-ttu-id="171e1-811">-1201</span><span class="sxs-lookup"><span data-stu-id="171e1-811">-1201</span></span></p></td>
<td><p><span data-ttu-id="171e1-812">Il database esiste già.</span><span class="sxs-lookup"><span data-stu-id="171e1-812">The database already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-813">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="171e1-813">JET_errDatabaseInUse</span></span><br />
<span data-ttu-id="171e1-814">-1202</span><span class="sxs-lookup"><span data-stu-id="171e1-814">-1202</span></span></p></td>
<td><p><span data-ttu-id="171e1-815">Database in uso.</span><span class="sxs-lookup"><span data-stu-id="171e1-815">The database in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-816">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="171e1-816">JET_errDatabaseNotFound</span></span><br />
<span data-ttu-id="171e1-817">-1203</span><span class="sxs-lookup"><span data-stu-id="171e1-817">-1203</span></span></p></td>
<td><p><span data-ttu-id="171e1-818">Nessun database di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="171e1-818">There is no such database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-819">JET_errDatabaseInvalidName</span><span class="sxs-lookup"><span data-stu-id="171e1-819">JET_errDatabaseInvalidName</span></span><br />
<span data-ttu-id="171e1-820">-1204</span><span class="sxs-lookup"><span data-stu-id="171e1-820">-1204</span></span></p></td>
<td><p><span data-ttu-id="171e1-821">Il nome del database non è valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-821">The database name is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-822">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="171e1-822">JET_errDatabaseInvalidPages</span></span><br />
<span data-ttu-id="171e1-823">-1205</span><span class="sxs-lookup"><span data-stu-id="171e1-823">-1205</span></span></p></td>
<td><p><span data-ttu-id="171e1-824">Numero di pagine non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-824">There are an invalid number of pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-825">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="171e1-825">JET_errDatabaseCorrupted</span></span><br />
<span data-ttu-id="171e1-826">-1206</span><span class="sxs-lookup"><span data-stu-id="171e1-826">-1206</span></span></p></td>
<td><p><span data-ttu-id="171e1-827">È presente un file non di database o un database danneggiato.</span><span class="sxs-lookup"><span data-stu-id="171e1-827">There is a non-database file or corrupt database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-828">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="171e1-828">JET_errDatabaseLocked</span></span><br />
<span data-ttu-id="171e1-829">-1207</span><span class="sxs-lookup"><span data-stu-id="171e1-829">-1207</span></span></p></td>
<td><p><span data-ttu-id="171e1-830">Il database è bloccato in modo esclusivo.</span><span class="sxs-lookup"><span data-stu-id="171e1-830">The database is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-831">JET_errCannotDisableVersioning</span><span class="sxs-lookup"><span data-stu-id="171e1-831">JET_errCannotDisableVersioning</span></span><br />
<span data-ttu-id="171e1-832">-1208</span><span class="sxs-lookup"><span data-stu-id="171e1-832">-1208</span></span></p></td>
<td><p><span data-ttu-id="171e1-833">Non è possibile disabilitare il controllo delle versioni per questo database.</span><span class="sxs-lookup"><span data-stu-id="171e1-833">The versioning for this database cannot be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-834">JET_errInvalidDatabaseVersion</span><span class="sxs-lookup"><span data-stu-id="171e1-834">JET_errInvalidDatabaseVersion</span></span><br />
<span data-ttu-id="171e1-835">-1209</span><span class="sxs-lookup"><span data-stu-id="171e1-835">-1209</span></span></p></td>
<td><p><span data-ttu-id="171e1-836">Il motore di database non è compatibile con il database.</span><span class="sxs-lookup"><span data-stu-id="171e1-836">The database engine is incompatible with the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-837">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="171e1-837">JET_errDatabase200Format</span></span><br />
<span data-ttu-id="171e1-838">-1210</span><span class="sxs-lookup"><span data-stu-id="171e1-838">-1210</span></span></p></td>
<td><p><span data-ttu-id="171e1-839">Il database è in un formato precedente (200).</span><span class="sxs-lookup"><span data-stu-id="171e1-839">The database is in an older (200) format.</span></span> <span data-ttu-id="171e1-840">Questo errore viene restituito da <a href="gg294068(v=exchg.10).md">JetInit</a> se è impostato <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> .</span><span class="sxs-lookup"><span data-stu-id="171e1-840">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="171e1-841">Solo client Windows NT.</span><span class="sxs-lookup"><span data-stu-id="171e1-841">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-842">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="171e1-842">JET_errDatabase400Format</span></span><br />
<span data-ttu-id="171e1-843">-1211</span><span class="sxs-lookup"><span data-stu-id="171e1-843">-1211</span></span></p></td>
<td><p><span data-ttu-id="171e1-844">Il database è in un formato precedente (400).</span><span class="sxs-lookup"><span data-stu-id="171e1-844">The database is in an older (400) format.</span></span> <span data-ttu-id="171e1-845">Questo errore viene restituito da <a href="gg294068(v=exchg.10).md">JetInit</a> se è impostato <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> .</span><span class="sxs-lookup"><span data-stu-id="171e1-845">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="171e1-846">Solo client Windows NT.</span><span class="sxs-lookup"><span data-stu-id="171e1-846">Windows NT client only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-847">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="171e1-847">JET_errDatabase500Format</span></span><br />
<span data-ttu-id="171e1-848">-1212</span><span class="sxs-lookup"><span data-stu-id="171e1-848">-1212</span></span></p></td>
<td><p><span data-ttu-id="171e1-849">Il database è in un formato precedente (500).</span><span class="sxs-lookup"><span data-stu-id="171e1-849">The database is in an older (500) format.</span></span> <span data-ttu-id="171e1-850">Questo errore viene restituito da <a href="gg294068(v=exchg.10).md">JetInit</a> se è impostato <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> .</span><span class="sxs-lookup"><span data-stu-id="171e1-850">This error is returned by <a href="gg294068(v=exchg.10).md">JetInit</a> if <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> is set.</span></span> <span data-ttu-id="171e1-851">Solo client Windows NT.</span><span class="sxs-lookup"><span data-stu-id="171e1-851">Windows NT client only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-852">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="171e1-852">JET_errPageSizeMismatch</span></span><br />
<span data-ttu-id="171e1-853">-1213</span><span class="sxs-lookup"><span data-stu-id="171e1-853">-1213</span></span></p></td>
<td><p><span data-ttu-id="171e1-854">Le dimensioni della pagina del database non corrispondono a quelle del motore.</span><span class="sxs-lookup"><span data-stu-id="171e1-854">The database page size does not match the engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-855">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="171e1-855">JET_errTooManyInstances</span></span><br />
<span data-ttu-id="171e1-856">-1214</span><span class="sxs-lookup"><span data-stu-id="171e1-856">-1214</span></span></p></td>
<td><p><span data-ttu-id="171e1-857">Non è possibile avviare altre istanze di database.</span><span class="sxs-lookup"><span data-stu-id="171e1-857">No more database instances can be started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-858">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="171e1-858">JET_errDatabaseSharingViolation</span></span><br />
<span data-ttu-id="171e1-859">-1215</span><span class="sxs-lookup"><span data-stu-id="171e1-859">-1215</span></span></p></td>
<td><p><span data-ttu-id="171e1-860">In un'istanza di database diversa viene utilizzato questo database.</span><span class="sxs-lookup"><span data-stu-id="171e1-860">A different database instance is using this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-861">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="171e1-861">JET_errAttachedDatabaseMismatch</span></span><br />
<span data-ttu-id="171e1-862">-1216</span><span class="sxs-lookup"><span data-stu-id="171e1-862">-1216</span></span></p></td>
<td><p><span data-ttu-id="171e1-863">È stato rilevato un allegato del database in attesa all'inizio o alla fine del ripristino, ma il database è mancante o non corrisponde alle informazioni sugli allegati.</span><span class="sxs-lookup"><span data-stu-id="171e1-863">An outstanding database attachment has been detected at the start or end of the recovery, but the database is missing or does not match attachment info.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-864">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="171e1-864">JET_errDatabaseInvalidPath</span></span><br />
<span data-ttu-id="171e1-865">-1217</span><span class="sxs-lookup"><span data-stu-id="171e1-865">-1217</span></span></p></td>
<td><p><span data-ttu-id="171e1-866">Il percorso specificato per il file di database non è valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-866">The specified path to the database file is illegal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-867">JET_errDatabaseIdInUse</span><span class="sxs-lookup"><span data-stu-id="171e1-867">JET_errDatabaseIdInUse</span></span><br />
<span data-ttu-id="171e1-868">-1218</span><span class="sxs-lookup"><span data-stu-id="171e1-868">-1218</span></span></p></td>
<td><p><span data-ttu-id="171e1-869">A un database viene assegnato un ID già in uso.</span><span class="sxs-lookup"><span data-stu-id="171e1-869">A database is being assigned an ID that is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-870">JET_errForceDetachNotAllowed</span><span class="sxs-lookup"><span data-stu-id="171e1-870">JET_errForceDetachNotAllowed</span></span><br />
<span data-ttu-id="171e1-871">-1219</span><span class="sxs-lookup"><span data-stu-id="171e1-871">-1219</span></span></p></td>
<td><p><span data-ttu-id="171e1-872">Lo scollegamento forzato è consentito solo dopo l'arresto della normale scollegamento a causa di un errore.</span><span class="sxs-lookup"><span data-stu-id="171e1-872">The force detach is allowed only after the normal detach was stopped due to an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-873">JET_errCatalogCorrupted</span><span class="sxs-lookup"><span data-stu-id="171e1-873">JET_errCatalogCorrupted</span></span><br />
<span data-ttu-id="171e1-874">-1220</span><span class="sxs-lookup"><span data-stu-id="171e1-874">-1220</span></span></p></td>
<td><p><span data-ttu-id="171e1-875">È stato rilevato un danneggiamento nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="171e1-875">Corruption was detected in the catalog.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-876">JET_errPartiallyAttachedDB</span><span class="sxs-lookup"><span data-stu-id="171e1-876">JET_errPartiallyAttachedDB</span></span><br />
<span data-ttu-id="171e1-877">-1221</span><span class="sxs-lookup"><span data-stu-id="171e1-877">-1221</span></span></p></td>
<td><p><span data-ttu-id="171e1-878">Il database è collegato solo parzialmente e non è possibile completare l'operazione di connessione.</span><span class="sxs-lookup"><span data-stu-id="171e1-878">The database is only partially attached and the attach operation cannot be completed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-879">JET_errDatabaseSignInUse</span><span class="sxs-lookup"><span data-stu-id="171e1-879">JET_errDatabaseSignInUse</span></span><br />
<span data-ttu-id="171e1-880">-1222</span><span class="sxs-lookup"><span data-stu-id="171e1-880">-1222</span></span></p></td>
<td><p><span data-ttu-id="171e1-881">Il database con la stessa firma è già in uso.</span><span class="sxs-lookup"><span data-stu-id="171e1-881">The database with the same signature is already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-882">JET_errDatabaseCorruptedNoRepair</span><span class="sxs-lookup"><span data-stu-id="171e1-882">JET_errDatabaseCorruptedNoRepair</span></span><br />
<span data-ttu-id="171e1-883">-1224</span><span class="sxs-lookup"><span data-stu-id="171e1-883">-1224</span></span></p></td>
<td><p><span data-ttu-id="171e1-884">Il database è danneggiato ma non è consentito un ripristino.</span><span class="sxs-lookup"><span data-stu-id="171e1-884">The database is corrupted but a repair is not allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-885">JET_errInvalidCreateDbVersion</span><span class="sxs-lookup"><span data-stu-id="171e1-885">JET_errInvalidCreateDbVersion</span></span><br />
<span data-ttu-id="171e1-886">-1225</span><span class="sxs-lookup"><span data-stu-id="171e1-886">-1225</span></span></p></td>
<td><p><span data-ttu-id="171e1-887">Il motore di database ha tentato di riprodurre un'operazione di creazione database dal log delle transazioni, ma non è riuscito a causa di una versione incompatibile di tale operazione.</span><span class="sxs-lookup"><span data-stu-id="171e1-887">The database engine attempted to replay a Create Database operation from the transaction log but failed due to an incompatible version of that operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-888">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="171e1-888">JET_errTableLocked</span></span><br />
<span data-ttu-id="171e1-889">-1302</span><span class="sxs-lookup"><span data-stu-id="171e1-889">-1302</span></span></p></td>
<td><p><span data-ttu-id="171e1-890">La tabella è bloccata in modo esclusivo.</span><span class="sxs-lookup"><span data-stu-id="171e1-890">The table is exclusively locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-891">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="171e1-891">JET_errTableDuplicate</span></span><br />
<span data-ttu-id="171e1-892">-1303</span><span class="sxs-lookup"><span data-stu-id="171e1-892">-1303</span></span></p></td>
<td><p><span data-ttu-id="171e1-893">La tabella esiste già.</span><span class="sxs-lookup"><span data-stu-id="171e1-893">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-894">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="171e1-894">JET_errTableInUse</span></span><br />
<span data-ttu-id="171e1-895">-1304</span><span class="sxs-lookup"><span data-stu-id="171e1-895">-1304</span></span></p></td>
<td><p><span data-ttu-id="171e1-896">La tabella è in uso e non può essere bloccata.</span><span class="sxs-lookup"><span data-stu-id="171e1-896">The table is in use and cannot be locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-897">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="171e1-897">JET_errObjectNotFound</span></span><br />
<span data-ttu-id="171e1-898">-1305</span><span class="sxs-lookup"><span data-stu-id="171e1-898">-1305</span></span></p></td>
<td><p><span data-ttu-id="171e1-899">Non esiste una tabella o un oggetto di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="171e1-899">There is no such table or object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-900">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="171e1-900">JET_errDensityInvalid</span></span><br />
<span data-ttu-id="171e1-901">-1307</span><span class="sxs-lookup"><span data-stu-id="171e1-901">-1307</span></span></p></td>
<td><p><span data-ttu-id="171e1-902">La densità di un file o un indice non è valida.</span><span class="sxs-lookup"><span data-stu-id="171e1-902">There is a bad file or index density.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-903">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="171e1-903">JET_errTableNotEmpty</span></span><br />
<span data-ttu-id="171e1-904">-1308</span><span class="sxs-lookup"><span data-stu-id="171e1-904">-1308</span></span></p></td>
<td><p><span data-ttu-id="171e1-905">La tabella non è vuota.</span><span class="sxs-lookup"><span data-stu-id="171e1-905">The table is not empty.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-906">JET_errInvalidTableId</span><span class="sxs-lookup"><span data-stu-id="171e1-906">JET_errInvalidTableId</span></span><br />
<span data-ttu-id="171e1-907">-1310</span><span class="sxs-lookup"><span data-stu-id="171e1-907">-1310</span></span></p></td>
<td><p><span data-ttu-id="171e1-908">ID di tabella non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-908">The table ID is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-909">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="171e1-909">JET_errTooManyOpenTables</span></span><br />
<span data-ttu-id="171e1-910">-1311</span><span class="sxs-lookup"><span data-stu-id="171e1-910">-1311</span></span></p></td>
<td><p><span data-ttu-id="171e1-911">Non è possibile aprire altre tabelle, neanche dopo l'esecuzione dell'attività di pulizia interna.</span><span class="sxs-lookup"><span data-stu-id="171e1-911">No more tables can be opened, even after the internal cleanup task has run.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-912">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="171e1-912">JET_errIllegalOperation</span></span><br />
<span data-ttu-id="171e1-913">-1312</span><span class="sxs-lookup"><span data-stu-id="171e1-913">-1312</span></span></p></td>
<td><p><span data-ttu-id="171e1-914">Operazione non supportata nella tabella.</span><span class="sxs-lookup"><span data-stu-id="171e1-914">The operation is not supported on the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span><span class="sxs-lookup"><span data-stu-id="171e1-915">JET_errTooManyOpenTablesAndCleanupTimedOut</span></span><br />
<span data-ttu-id="171e1-916">-1313</span><span class="sxs-lookup"><span data-stu-id="171e1-916">-1313</span></span></p></td>
<td><p><span data-ttu-id="171e1-917">Non è possibile aprire altre tabelle perché il tentativo di pulizia non è stato completato.</span><span class="sxs-lookup"><span data-stu-id="171e1-917">No more tables can be opened because the cleanup attempt failed to complete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-918">JET_errObjectDuplicate</span><span class="sxs-lookup"><span data-stu-id="171e1-918">JET_errObjectDuplicate</span></span><br />
<span data-ttu-id="171e1-919">-1314</span><span class="sxs-lookup"><span data-stu-id="171e1-919">-1314</span></span></p></td>
<td><p><span data-ttu-id="171e1-920">Il nome della tabella o dell'oggetto è in uso.</span><span class="sxs-lookup"><span data-stu-id="171e1-920">The table or object name is in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-921">JET_errInvalidObject</span><span class="sxs-lookup"><span data-stu-id="171e1-921">JET_errInvalidObject</span></span><br />
<span data-ttu-id="171e1-922">-1316</span><span class="sxs-lookup"><span data-stu-id="171e1-922">-1316</span></span></p></td>
<td><p><span data-ttu-id="171e1-923">L'oggetto non è valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="171e1-923">The object is invalid for operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-924">JET_errCannotDeleteTempTable</span><span class="sxs-lookup"><span data-stu-id="171e1-924">JET_errCannotDeleteTempTable</span></span><br />
<span data-ttu-id="171e1-925">-1317</span><span class="sxs-lookup"><span data-stu-id="171e1-925">-1317</span></span></p></td>
<td><p><span data-ttu-id="171e1-926">Per eliminare una tabella temporanea, è necessario usare <a href="gg294087(v=exchg.10).md">JetCloseTable</a> anziché <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> .</span><span class="sxs-lookup"><span data-stu-id="171e1-926"><a href="gg294087(v=exchg.10).md">JetCloseTable</a> must be used instead of <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> to delete a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-927">JET_errCannotDeleteSystemTable</span><span class="sxs-lookup"><span data-stu-id="171e1-927">JET_errCannotDeleteSystemTable</span></span><br />
<span data-ttu-id="171e1-928">-1318</span><span class="sxs-lookup"><span data-stu-id="171e1-928">-1318</span></span></p></td>
<td><p><span data-ttu-id="171e1-929">Si è verificato un tentativo non valido di eliminare una tabella di sistema.</span><span class="sxs-lookup"><span data-stu-id="171e1-929">There was an illegal attempt to delete a system table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-930">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="171e1-930">JET_errCannotDeleteTemplateTable</span></span><br />
<span data-ttu-id="171e1-931">-1319</span><span class="sxs-lookup"><span data-stu-id="171e1-931">-1319</span></span></p></td>
<td><p><span data-ttu-id="171e1-932">Si è verificato un tentativo non valido di eliminare una tabella del modello.</span><span class="sxs-lookup"><span data-stu-id="171e1-932">There was an illegal attempt to delete a template table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-933">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="171e1-933">JET_errExclusiveTableLockRequired</span></span><br />
<span data-ttu-id="171e1-934">-1322</span><span class="sxs-lookup"><span data-stu-id="171e1-934">-1322</span></span></p></td>
<td><p><span data-ttu-id="171e1-935">Per la tabella deve essere presente un blocco esclusivo.</span><span class="sxs-lookup"><span data-stu-id="171e1-935">There must be an exclusive lock on the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-936">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="171e1-936">JET_errFixedDDL</span></span><br />
<span data-ttu-id="171e1-937">-1323</span><span class="sxs-lookup"><span data-stu-id="171e1-937">-1323</span></span></p></td>
<td><p><span data-ttu-id="171e1-938">Le operazioni DDL non sono consentite in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="171e1-938">DDL operations are prohibited on this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-939">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="171e1-939">JET_errFixedInheritedDDL</span></span><br />
<span data-ttu-id="171e1-940">-1324</span><span class="sxs-lookup"><span data-stu-id="171e1-940">-1324</span></span></p></td>
<td><p><span data-ttu-id="171e1-941">In una tabella derivata, le operazioni DDL non sono consentite sulla parte ereditata del DDL.</span><span class="sxs-lookup"><span data-stu-id="171e1-941">On a derived table, DDL operations are prohibited on the inherited portion of the DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-942">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="171e1-942">JET_errCannotNestDDL</span></span><br />
<span data-ttu-id="171e1-943">-1325</span><span class="sxs-lookup"><span data-stu-id="171e1-943">-1325</span></span></p></td>
<td><p><span data-ttu-id="171e1-944">La nidificazione della DDL gerarchica non è attualmente supportata.</span><span class="sxs-lookup"><span data-stu-id="171e1-944">Nesting the hierarchical DDL is not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-945">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="171e1-945">JET_errDDLNotInheritable</span></span><br />
<span data-ttu-id="171e1-946">-1326</span><span class="sxs-lookup"><span data-stu-id="171e1-946">-1326</span></span></p></td>
<td><p><span data-ttu-id="171e1-947">Tentativo di ereditare un DDL da una tabella non contrassegnata come tabella modello.</span><span class="sxs-lookup"><span data-stu-id="171e1-947">There was an attempt to inherit a DDL from a table that is not marked as a template table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-948">JET_errInvalidSettings</span><span class="sxs-lookup"><span data-stu-id="171e1-948">JET_errInvalidSettings</span></span><br />
<span data-ttu-id="171e1-949">-1328</span><span class="sxs-lookup"><span data-stu-id="171e1-949">-1328</span></span></p></td>
<td><p><span data-ttu-id="171e1-950">I parametri di sistema sono stati impostati in modo errato.</span><span class="sxs-lookup"><span data-stu-id="171e1-950">The system parameters were set improperly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-951">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="171e1-951">JET_errClientRequestToStopJetService</span></span><br />
<span data-ttu-id="171e1-952">-1329</span><span class="sxs-lookup"><span data-stu-id="171e1-952">-1329</span></span></p></td>
<td><p><span data-ttu-id="171e1-953">Il client ha richiesto l'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="171e1-953">The client has requested that the service be stopped.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-954">JET_errCannotAddFixedVarColumnToDerivedTable</span><span class="sxs-lookup"><span data-stu-id="171e1-954">JET_errCannotAddFixedVarColumnToDerivedTable</span></span><br />
<span data-ttu-id="171e1-955">-1330</span><span class="sxs-lookup"><span data-stu-id="171e1-955">-1330</span></span></p></td>
<td><p><span data-ttu-id="171e1-956">La tabella modello è stata creata con il flag NoFixedVarColumnsInDerivedTables impostato.</span><span class="sxs-lookup"><span data-stu-id="171e1-956">The Template table was created with the NoFixedVarColumnsInDerivedTables flag set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-957">JET_errIndexCantBuild</span><span class="sxs-lookup"><span data-stu-id="171e1-957">JET_errIndexCantBuild</span></span><br />
<span data-ttu-id="171e1-958">-1401</span><span class="sxs-lookup"><span data-stu-id="171e1-958">-1401</span></span></p></td>
<td><p><span data-ttu-id="171e1-959">Compilazione dell'indice non riuscita.</span><span class="sxs-lookup"><span data-stu-id="171e1-959">The index build failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-960">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="171e1-960">JET_errIndexHasPrimary</span></span><br />
<span data-ttu-id="171e1-961">-1402</span><span class="sxs-lookup"><span data-stu-id="171e1-961">-1402</span></span></p></td>
<td><p><span data-ttu-id="171e1-962">L'indice primario è già definito.</span><span class="sxs-lookup"><span data-stu-id="171e1-962">The primary index is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-963">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="171e1-963">JET_errIndexDuplicate</span></span><br />
<span data-ttu-id="171e1-964">-1403</span><span class="sxs-lookup"><span data-stu-id="171e1-964">-1403</span></span></p></td>
<td><p><span data-ttu-id="171e1-965">L'indice è già definito.</span><span class="sxs-lookup"><span data-stu-id="171e1-965">The index is already defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-966">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="171e1-966">JET_errIndexNotFound</span></span><br />
<span data-ttu-id="171e1-967">-1404</span><span class="sxs-lookup"><span data-stu-id="171e1-967">-1404</span></span></p></td>
<td><p><span data-ttu-id="171e1-968">Non esiste alcun indice di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="171e1-968">There is no such index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-969">JET_errIndexMustStay</span><span class="sxs-lookup"><span data-stu-id="171e1-969">JET_errIndexMustStay</span></span><br />
<span data-ttu-id="171e1-970">-1405</span><span class="sxs-lookup"><span data-stu-id="171e1-970">-1405</span></span></p></td>
<td><p><span data-ttu-id="171e1-971">Impossibile eliminare l'indice cluster.</span><span class="sxs-lookup"><span data-stu-id="171e1-971">The clustered index cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-972">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="171e1-972">JET_errIndexInvalidDef</span></span><br />
<span data-ttu-id="171e1-973">-1406</span><span class="sxs-lookup"><span data-stu-id="171e1-973">-1406</span></span></p></td>
<td><p><span data-ttu-id="171e1-974">La definizione dell'indice non è valida.</span><span class="sxs-lookup"><span data-stu-id="171e1-974">The index definition is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-975">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="171e1-975">JET_errInvalidCreateIndex</span></span><br />
<span data-ttu-id="171e1-976">-1409</span><span class="sxs-lookup"><span data-stu-id="171e1-976">-1409</span></span></p></td>
<td><p><span data-ttu-id="171e1-977">La creazione della descrizione dell'indice non è valida.</span><span class="sxs-lookup"><span data-stu-id="171e1-977">The creation of the index description was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-978">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="171e1-978">JET_errTooManyOpenIndexes</span></span><br />
<span data-ttu-id="171e1-979">-1410</span><span class="sxs-lookup"><span data-stu-id="171e1-979">-1410</span></span></p></td>
<td><p><span data-ttu-id="171e1-980">Il database non è presente nei blocchi di descrizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="171e1-980">The database is out of index description blocks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-981">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="171e1-981">JET_errMultiValuedIndexViolation</span></span><br />
<span data-ttu-id="171e1-982">-1411</span><span class="sxs-lookup"><span data-stu-id="171e1-982">-1411</span></span></p></td>
<td><p><span data-ttu-id="171e1-983">Per un indice multivalore sono state generate chiavi di indice inter-record non univoche.</span><span class="sxs-lookup"><span data-stu-id="171e1-983">Non-unique inter-record index keys have been generated for a multi-valued index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-984">JET_errIndexBuildCorrupted</span><span class="sxs-lookup"><span data-stu-id="171e1-984">JET_errIndexBuildCorrupted</span></span><br />
<span data-ttu-id="171e1-985">-1412</span><span class="sxs-lookup"><span data-stu-id="171e1-985">-1412</span></span></p></td>
<td><p><span data-ttu-id="171e1-986">Non è stato possibile compilare un indice secondario che riflette correttamente l'indice primario.</span><span class="sxs-lookup"><span data-stu-id="171e1-986">A secondary index that properly reflects the primary index failed to build.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-987">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="171e1-987">JET_errPrimaryIndexCorrupted</span></span><br />
<span data-ttu-id="171e1-988">-1413</span><span class="sxs-lookup"><span data-stu-id="171e1-988">-1413</span></span></p></td>
<td><p><span data-ttu-id="171e1-989">L'indice primario è danneggiato e il database deve essere deframmentato.</span><span class="sxs-lookup"><span data-stu-id="171e1-989">The primary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-990">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="171e1-990">JET_errSecondaryIndexCorrupted</span></span><br />
<span data-ttu-id="171e1-991">-1414</span><span class="sxs-lookup"><span data-stu-id="171e1-991">-1414</span></span></p></td>
<td><p><span data-ttu-id="171e1-992">L'indice secondario è danneggiato e il database deve essere deframmentato.</span><span class="sxs-lookup"><span data-stu-id="171e1-992">The secondary index is corrupt and the database must be defragmented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-993">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="171e1-993">JET_errInvalidIndexId</span></span><br />
<span data-ttu-id="171e1-994">-1416</span><span class="sxs-lookup"><span data-stu-id="171e1-994">-1416</span></span></p></td>
<td><p><span data-ttu-id="171e1-995">ID di indice non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-995">The index ID is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-996">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="171e1-996">JET_errIndexTuplesSecondaryIndexOnly</span></span><br />
<span data-ttu-id="171e1-997">-1430</span><span class="sxs-lookup"><span data-stu-id="171e1-997">-1430</span></span></p></td>
<td><p><span data-ttu-id="171e1-998">L'indice della tupla può essere impostato solo su un indice secondario.</span><span class="sxs-lookup"><span data-stu-id="171e1-998">The tuple index can only be set on a secondary index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-999">JET_errIndexTuplesTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="171e1-999">JET_errIndexTuplesTooManyColumns</span></span><br />
<span data-ttu-id="171e1-1000">-1431</span><span class="sxs-lookup"><span data-stu-id="171e1-1000">-1431</span></span></p></td>
<td><p><span data-ttu-id="171e1-1001">La definizione dell'indice per l'indice tupla contiene più colonne chiave che possono essere supportate dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="171e1-1001">The index definition for the tuple index contains more key columns that the database engine can support.</span></span></p>
<p><span data-ttu-id="171e1-1002"><strong>Nota  </strong> Il JET_errIndexTuplesOneColumnOnly errore è obsoleto ed è stato sostituito da JET_errIndexTuplesTooManyColumns.</span><span class="sxs-lookup"><span data-stu-id="171e1-1002"><strong>Note  </strong>The JET_errIndexTuplesOneColumnOnly error is obsolete and has been replaced by JET_errIndexTuplesTooManyColumns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1003">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="171e1-1003">JET_errIndexTuplesNonUniqueOnly</span></span><br />
<span data-ttu-id="171e1-1004">-1432</span><span class="sxs-lookup"><span data-stu-id="171e1-1004">-1432</span></span></p></td>
<td><p><span data-ttu-id="171e1-1005">L'indice della tupla deve essere un indice non univoco.</span><span class="sxs-lookup"><span data-stu-id="171e1-1005">The tuple index must be a non-unique index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="171e1-1006">JET_errIndexTuplesTextBinaryColumnsOnly</span></span><br />
<span data-ttu-id="171e1-1007">-1433</span><span class="sxs-lookup"><span data-stu-id="171e1-1007">-1433</span></span></p></td>
<td><p><span data-ttu-id="171e1-1008">Una definizione di indice tupla può contenere solo colonne chiave con tipi di colonna di testo o binari.</span><span class="sxs-lookup"><span data-stu-id="171e1-1008">A tuple index definition can only contain key columns that have text or binary column types.</span></span></p>
<p><span data-ttu-id="171e1-1009"><strong>Nota  </strong> Il JET_errIndexTuplesTextColumnsOnly errore è obsoleto ed è stato sostituito da JET_errIndexTuplesTextBinaryColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="171e1-1009"><strong>Note  </strong>The JET_errIndexTuplesTextColumnsOnly error is obsolete and has been replaced by JET_errIndexTuplesTextBinaryColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1010">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="171e1-1010">JET_errIndexTuplesVarSegMacNotAllowed</span></span><br />
<span data-ttu-id="171e1-1011">-1434</span><span class="sxs-lookup"><span data-stu-id="171e1-1011">-1434</span></span></p></td>
<td><p><span data-ttu-id="171e1-1012">L'indice della tupla non consente l'impostazione di cbVarSegMac.</span><span class="sxs-lookup"><span data-stu-id="171e1-1012">The tuple index does not allow setting cbVarSegMac.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1013">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="171e1-1013">JET_errIndexTuplesInvalidLimits</span></span><br />
<span data-ttu-id="171e1-1014">-1435</span><span class="sxs-lookup"><span data-stu-id="171e1-1014">-1435</span></span></p></td>
<td><p><span data-ttu-id="171e1-1015">La lunghezza minima o massima della tupla o il numero massimo di caratteri specificati per un indice non sono validi.</span><span class="sxs-lookup"><span data-stu-id="171e1-1015">The minimum/maximum tuple length or the maximum number of characters that are specified for an index are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="171e1-1016">JET_errIndexTuplesCannotRetrieveFromIndex</span></span><br />
<span data-ttu-id="171e1-1017">-1436</span><span class="sxs-lookup"><span data-stu-id="171e1-1017">-1436</span></span></p></td>
<td><p><span data-ttu-id="171e1-1018">Impossibile chiamare <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> con il flag di JET_bitRetrieveFromIndex impostato durante il recupero di una colonna in un indice di tupla.</span><span class="sxs-lookup"><span data-stu-id="171e1-1018"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> cannot be called with the JET_bitRetrieveFromIndex flag set while retrieving a column on a tuple index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1019">JET_errIndexTuplesKeyTooSmall</span><span class="sxs-lookup"><span data-stu-id="171e1-1019">JET_errIndexTuplesKeyTooSmall</span></span><br />
<span data-ttu-id="171e1-1020">-1437</span><span class="sxs-lookup"><span data-stu-id="171e1-1020">-1437</span></span></p></td>
<td><p><span data-ttu-id="171e1-1021">La chiave specificata non soddisfa la lunghezza minima della tupla.</span><span class="sxs-lookup"><span data-stu-id="171e1-1021">The specified key does not meet the minimum tuple length.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1022">JET_errColumnLong</span><span class="sxs-lookup"><span data-stu-id="171e1-1022">JET_errColumnLong</span></span><br />
<span data-ttu-id="171e1-1023">-1501</span><span class="sxs-lookup"><span data-stu-id="171e1-1023">-1501</span></span></p></td>
<td><p><span data-ttu-id="171e1-1024">Il valore della colonna è Long.</span><span class="sxs-lookup"><span data-stu-id="171e1-1024">The column value is long.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1025">JET_errColumnNoChunk</span><span class="sxs-lookup"><span data-stu-id="171e1-1025">JET_errColumnNoChunk</span></span><br />
<span data-ttu-id="171e1-1026">-1502</span><span class="sxs-lookup"><span data-stu-id="171e1-1026">-1502</span></span></p></td>
<td><p><span data-ttu-id="171e1-1027">Non esiste un blocco di questo tipo in un valore Long.</span><span class="sxs-lookup"><span data-stu-id="171e1-1027">There is no such chunk in a long value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1028">JET_errColumnDoesNotFit</span><span class="sxs-lookup"><span data-stu-id="171e1-1028">JET_errColumnDoesNotFit</span></span><br />
<span data-ttu-id="171e1-1029">-1503</span><span class="sxs-lookup"><span data-stu-id="171e1-1029">-1503</span></span></p></td>
<td><p><span data-ttu-id="171e1-1030">Il campo non rientrerà nel record.</span><span class="sxs-lookup"><span data-stu-id="171e1-1030">The field will not fit in the record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1031">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="171e1-1031">JET_errNullInvalid</span></span><br />
<span data-ttu-id="171e1-1032">-1504</span><span class="sxs-lookup"><span data-stu-id="171e1-1032">-1504</span></span></p></td>
<td><p><span data-ttu-id="171e1-1033">Null non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-1033">Null is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1034">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="171e1-1034">JET_errColumnIllegalNull</span></span><br />
<span data-ttu-id="171e1-1035">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="171e1-1035">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="171e1-1036">Null non valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-1036">Null is not valid.</span></span> <span data-ttu-id="171e1-1037">Questo errore viene restituito da Gestione record.</span><span class="sxs-lookup"><span data-stu-id="171e1-1037">This error is returned by the record manager.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1038">JET_errColumnIndexed-1505</span><span class="sxs-lookup"><span data-stu-id="171e1-1038">JET_errColumnIndexed -1505</span></span></p></td>
<td><p><span data-ttu-id="171e1-1039">La colonna è indicizzata e non può essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="171e1-1039">The column is indexed and cannot be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1040">JET_errColumnTooBig-1506</span><span class="sxs-lookup"><span data-stu-id="171e1-1040">JET_errColumnTooBig -1506</span></span></p></td>
<td><p><span data-ttu-id="171e1-1041">La lunghezza del campo è maggiore della lunghezza massima consentita.</span><span class="sxs-lookup"><span data-stu-id="171e1-1041">The field length is greater than maximum allowed length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1042">JET_errColumnNotFound-1507</span><span class="sxs-lookup"><span data-stu-id="171e1-1042">JET_errColumnNotFound -1507</span></span></p></td>
<td><p><span data-ttu-id="171e1-1043">Non esiste alcuna colonna di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="171e1-1043">There is no such column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1044">JET_errColumnDuplicate-1508</span><span class="sxs-lookup"><span data-stu-id="171e1-1044">JET_errColumnDuplicate -1508</span></span></p></td>
<td><p><span data-ttu-id="171e1-1045">Questo campo è già definito.</span><span class="sxs-lookup"><span data-stu-id="171e1-1045">This field is already defined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1046">JET_errMultiValuedColumnMustBeTagged-1509</span><span class="sxs-lookup"><span data-stu-id="171e1-1046">JET_errMultiValuedColumnMustBeTagged -1509</span></span></p></td>
<td><p><span data-ttu-id="171e1-1047">È stato effettuato un tentativo di creare una colonna multivalore, ma la colonna non è stata contrassegnata con tag.</span><span class="sxs-lookup"><span data-stu-id="171e1-1047">An attempt was made to create a multi-valued column, but the column was not tagged.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1048">JET_errColumnRedundant-1510</span><span class="sxs-lookup"><span data-stu-id="171e1-1048">JET_errColumnRedundant -1510</span></span></p></td>
<td><p><span data-ttu-id="171e1-1049">È presente una seconda colonna con incremento automatico o versione.</span><span class="sxs-lookup"><span data-stu-id="171e1-1049">There was a second auto-increment or version column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1050">JET_errInvalidColumnType-1511</span><span class="sxs-lookup"><span data-stu-id="171e1-1050">JET_errInvalidColumnType -1511</span></span></p></td>
<td><p><span data-ttu-id="171e1-1051">Il tipo di dati della colonna non è valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-1051">The column data type is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1052">JET_errTaggedNotNULL-1514</span><span class="sxs-lookup"><span data-stu-id="171e1-1052">JET_errTaggedNotNULL -1514</span></span></p></td>
<td><p><span data-ttu-id="171e1-1053">Non sono presenti colonne con tag non NULL.</span><span class="sxs-lookup"><span data-stu-id="171e1-1053">There are no non-NULL tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1054">JET_errNoCurrentIndex-1515</span><span class="sxs-lookup"><span data-stu-id="171e1-1054">JET_errNoCurrentIndex -1515</span></span></p></td>
<td><p><span data-ttu-id="171e1-1055">Il database non è valido perché non contiene un indice corrente.</span><span class="sxs-lookup"><span data-stu-id="171e1-1055">The database is invalid because it does not contain a current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1056">JET_errKeyIsMade-1516</span><span class="sxs-lookup"><span data-stu-id="171e1-1056">JET_errKeyIsMade -1516</span></span></p></td>
<td><p><span data-ttu-id="171e1-1057">La chiave è stata completata.</span><span class="sxs-lookup"><span data-stu-id="171e1-1057">The key is completely made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1058">JET_errBadColumnId-1517</span><span class="sxs-lookup"><span data-stu-id="171e1-1058">JET_errBadColumnId -1517</span></span></p></td>
<td><p><span data-ttu-id="171e1-1059">ID di colonna non corretto.</span><span class="sxs-lookup"><span data-stu-id="171e1-1059">The column ID is incorrect.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1060">JET_errBadItagSequence-1518</span><span class="sxs-lookup"><span data-stu-id="171e1-1060">JET_errBadItagSequence -1518</span></span></p></td>
<td><p><span data-ttu-id="171e1-1061">ItagSequence non valido per la colonna con tag.</span><span class="sxs-lookup"><span data-stu-id="171e1-1061">There is a bad itagSequence for the tagged column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1062">JET_errColumnInRelationship-1519</span><span class="sxs-lookup"><span data-stu-id="171e1-1062">JET_errColumnInRelationship -1519</span></span></p></td>
<td><p><span data-ttu-id="171e1-1063">Una colonna non può essere eliminata perché fa parte di una relazione.</span><span class="sxs-lookup"><span data-stu-id="171e1-1063">A column cannot be deleted because it is part of a relationship.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1064">JET_errCannotBeTagged-1521</span><span class="sxs-lookup"><span data-stu-id="171e1-1064">JET_errCannotBeTagged -1521</span></span></p></td>
<td><p><span data-ttu-id="171e1-1065">Impossibile contrassegnare l'incremento automatico e la versione.</span><span class="sxs-lookup"><span data-stu-id="171e1-1065">The auto increment and version cannot be tagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1066">JET_errDefaultValueTooBig-1524</span><span class="sxs-lookup"><span data-stu-id="171e1-1066">JET_errDefaultValueTooBig -1524</span></span></p></td>
<td><p><span data-ttu-id="171e1-1067">Il valore predefinito supera la dimensione massima.</span><span class="sxs-lookup"><span data-stu-id="171e1-1067">The default value exceeds the maximum size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1068">JET_errMultiValuedDuplicate-1525</span><span class="sxs-lookup"><span data-stu-id="171e1-1068">JET_errMultiValuedDuplicate -1525</span></span></p></td>
<td><p><span data-ttu-id="171e1-1069">È stato rilevato un valore duplicato in una colonna multivalore univoca.</span><span class="sxs-lookup"><span data-stu-id="171e1-1069">A duplicate value was detected on a unique multi-valued column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1070">JET_errLVCorrupted-1526</span><span class="sxs-lookup"><span data-stu-id="171e1-1070">JET_errLVCorrupted -1526</span></span></p></td>
<td><p><span data-ttu-id="171e1-1071">È stato rilevato un danneggiamento in un albero con valori Long.</span><span class="sxs-lookup"><span data-stu-id="171e1-1071">Corruption was encountered in a long-value tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1072">JET_errMultiValuedDuplicateAfterTruncation-1528</span><span class="sxs-lookup"><span data-stu-id="171e1-1072">JET_errMultiValuedDuplicateAfterTruncation -1528</span></span></p></td>
<td><p><span data-ttu-id="171e1-1073">È stato rilevato un valore duplicato in una colonna univoca multivalore dopo che i dati sono stati normalizzati e la normalizzazione dei dati è stata troncata prima del confronto.</span><span class="sxs-lookup"><span data-stu-id="171e1-1073">A duplicate value was detected on a unique multi-valued column after the data was normalized, and it is normalizing truncated the data before comparison.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1074">JET_errDerivedColumnCorruption-1529</span><span class="sxs-lookup"><span data-stu-id="171e1-1074">JET_errDerivedColumnCorruption -1529</span></span></p></td>
<td><p><span data-ttu-id="171e1-1075">Colonna non valida nella tabella derivata.</span><span class="sxs-lookup"><span data-stu-id="171e1-1075">There is an invalid column in derived table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1076">JET_errInvalidPlaceholderColumn-1530</span><span class="sxs-lookup"><span data-stu-id="171e1-1076">JET_errInvalidPlaceholderColumn -1530</span></span></p></td>
<td><p><span data-ttu-id="171e1-1077">È stato effettuato un tentativo di convertire una colonna in un segnaposto di indice primario, ma la colonna non soddisfa i criteri necessari.</span><span class="sxs-lookup"><span data-stu-id="171e1-1077">An attempt was made to convert a column to a primary index placeholder, but the column does not meet the necessary criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1078">JET_errRecordNotFound-1601</span><span class="sxs-lookup"><span data-stu-id="171e1-1078">JET_errRecordNotFound -1601</span></span></p></td>
<td><p><span data-ttu-id="171e1-1079">Chiave non trovata.</span><span class="sxs-lookup"><span data-stu-id="171e1-1079">The key was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1080">JET_errRecordNoCopy-1602</span><span class="sxs-lookup"><span data-stu-id="171e1-1080">JET_errRecordNoCopy -1602</span></span></p></td>
<td><p><span data-ttu-id="171e1-1081">Nessun buffer funzionante.</span><span class="sxs-lookup"><span data-stu-id="171e1-1081">There is no working buffer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1082">JET_errNoCurrentRecord-1603</span><span class="sxs-lookup"><span data-stu-id="171e1-1082">JET_errNoCurrentRecord -1603</span></span></p></td>
<td><p><span data-ttu-id="171e1-1083">Non è presente nessun record corrente.</span><span class="sxs-lookup"><span data-stu-id="171e1-1083">There is no current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1084">JET_errRecordPrimaryChanged-1604</span><span class="sxs-lookup"><span data-stu-id="171e1-1084">JET_errRecordPrimaryChanged -1604</span></span></p></td>
<td><p><span data-ttu-id="171e1-1085">È possibile che la chiave primaria non venga modificata.</span><span class="sxs-lookup"><span data-stu-id="171e1-1085">The primary key might not change.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1086">JET_errKeyDuplicate-1605</span><span class="sxs-lookup"><span data-stu-id="171e1-1086">JET_errKeyDuplicate -1605</span></span></p></td>
<td><p><span data-ttu-id="171e1-1087">Chiave duplicata non valida.</span><span class="sxs-lookup"><span data-stu-id="171e1-1087">There is an illegal duplicate key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1088">JET_errAlreadyPrepared-1607</span><span class="sxs-lookup"><span data-stu-id="171e1-1088">JET_errAlreadyPrepared -1607</span></span></p></td>
<td><p><span data-ttu-id="171e1-1089">È stato effettuato un tentativo di aggiornare un record mentre era già in corso un aggiornamento del record.</span><span class="sxs-lookup"><span data-stu-id="171e1-1089">An attempt was made to update a record while a record update was already in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1090">JET_errKeyNotMade-1608</span><span class="sxs-lookup"><span data-stu-id="171e1-1090">JET_errKeyNotMade -1608</span></span></p></td>
<td><p><span data-ttu-id="171e1-1091">Non è stata effettuata alcuna chiamata a <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span><span class="sxs-lookup"><span data-stu-id="171e1-1091">A call was not made to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1092">JET_errUpdateNotPrepared-1609</span><span class="sxs-lookup"><span data-stu-id="171e1-1092">JET_errUpdateNotPrepared -1609</span></span></p></td>
<td><p><span data-ttu-id="171e1-1093">Non è stata effettuata alcuna chiamata a <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="171e1-1093">A call was not made to <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1094">JET_errDataHasChanged-1611</span><span class="sxs-lookup"><span data-stu-id="171e1-1094">JET_errDataHasChanged -1611</span></span></p></td>
<td><p><span data-ttu-id="171e1-1095">I dati sono stati modificati e l'operazione è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="171e1-1095">The data has changed and the operation was aborted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1096">JET_errLanguageNotSupported-1619</span><span class="sxs-lookup"><span data-stu-id="171e1-1096">JET_errLanguageNotSupported -1619</span></span></p></td>
<td><p><span data-ttu-id="171e1-1097">Questa installazione di Windows non supporta la lingua selezionata.</span><span class="sxs-lookup"><span data-stu-id="171e1-1097">This Windows installation does not support the selected language.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1098">JET_errTooManySorts-1701</span><span class="sxs-lookup"><span data-stu-id="171e1-1098">JET_errTooManySorts -1701</span></span></p></td>
<td><p><span data-ttu-id="171e1-1099">Troppi processi di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="171e1-1099">There are too many sort processes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1100">JET_errInvalidOnSort-1702</span><span class="sxs-lookup"><span data-stu-id="171e1-1100">JET_errInvalidOnSort -1702</span></span></p></td>
<td><p><span data-ttu-id="171e1-1101">Si è verificata un'operazione non valida durante un ordinamento.</span><span class="sxs-lookup"><span data-stu-id="171e1-1101">An invalid operation occurred during a sort.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1102">JET_errTempFileOpenError-1803</span><span class="sxs-lookup"><span data-stu-id="171e1-1102">JET_errTempFileOpenError -1803</span></span></p></td>
<td><p><span data-ttu-id="171e1-1103">Non è stato possibile aprire il file temporaneo.</span><span class="sxs-lookup"><span data-stu-id="171e1-1103">The temporary file could not be opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1104">JET_errTooManyAttachedDatabases-1805</span><span class="sxs-lookup"><span data-stu-id="171e1-1104">JET_errTooManyAttachedDatabases -1805</span></span></p></td>
<td><p><span data-ttu-id="171e1-1105">Troppi database aperti.</span><span class="sxs-lookup"><span data-stu-id="171e1-1105">Too many databases are open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1106">JET_errDiskFull-1808</span><span class="sxs-lookup"><span data-stu-id="171e1-1106">JET_errDiskFull -1808</span></span></p></td>
<td><p><span data-ttu-id="171e1-1107">Spazio su disco insufficiente.</span><span class="sxs-lookup"><span data-stu-id="171e1-1107">There is no space left on disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1108">JET_errPermissionDenied-1809</span><span class="sxs-lookup"><span data-stu-id="171e1-1108">JET_errPermissionDenied -1809</span></span></p></td>
<td><p><span data-ttu-id="171e1-1109">Autorizzazione negata.</span><span class="sxs-lookup"><span data-stu-id="171e1-1109">Permission is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1110">JET_errFileNotFound-1811</span><span class="sxs-lookup"><span data-stu-id="171e1-1110">JET_errFileNotFound -1811</span></span></p></td>
<td><p><span data-ttu-id="171e1-1111">Impossibile trovare il file.</span><span class="sxs-lookup"><span data-stu-id="171e1-1111">The file was not found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1112">JET_errFileInvalidType-1812</span><span class="sxs-lookup"><span data-stu-id="171e1-1112">JET_errFileInvalidType -1812</span></span></p></td>
<td><p><span data-ttu-id="171e1-1113">Il tipo di file non è valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-1113">The file type is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1114">JET_errAfterInitialization-1850</span><span class="sxs-lookup"><span data-stu-id="171e1-1114">JET_errAfterInitialization -1850</span></span></p></td>
<td><p><span data-ttu-id="171e1-1115">Non è possibile avviare un ripristino dopo l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="171e1-1115">A restore cannot be started after initialization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1116">JET_errLogCorrupted-1852</span><span class="sxs-lookup"><span data-stu-id="171e1-1116">JET_errLogCorrupted -1852</span></span></p></td>
<td><p><span data-ttu-id="171e1-1117">Non è stato possibile interpretare i log.</span><span class="sxs-lookup"><span data-stu-id="171e1-1117">The logs could not be interpreted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1118">JET_errInvalidOperation-1906</span><span class="sxs-lookup"><span data-stu-id="171e1-1118">JET_errInvalidOperation -1906</span></span></p></td>
<td><p><span data-ttu-id="171e1-1119">Operazione non valida.</span><span class="sxs-lookup"><span data-stu-id="171e1-1119">The operation is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1120">JET_errAccessDenied-1907</span><span class="sxs-lookup"><span data-stu-id="171e1-1120">JET_errAccessDenied -1907</span></span></p></td>
<td><p><span data-ttu-id="171e1-1121">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="171e1-1121">Access is denied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1122">JET_errTooManySplits-1909</span><span class="sxs-lookup"><span data-stu-id="171e1-1122">JET_errTooManySplits -1909</span></span></p></td>
<td><p><span data-ttu-id="171e1-1123">Divisione infinita.</span><span class="sxs-lookup"><span data-stu-id="171e1-1123">An infinite split.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1124">JET_errSessionSharingViolation-1910</span><span class="sxs-lookup"><span data-stu-id="171e1-1124">JET_errSessionSharingViolation -1910</span></span></p></td>
<td><p><span data-ttu-id="171e1-1125">Più thread utilizzano la stessa sessione.</span><span class="sxs-lookup"><span data-stu-id="171e1-1125">Multiple threads are using the same session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1126">JET_errEntryPointNotFound-1911</span><span class="sxs-lookup"><span data-stu-id="171e1-1126">JET_errEntryPointNotFound -1911</span></span></p></td>
<td><p><span data-ttu-id="171e1-1127">Impossibile trovare un punto di ingresso in una DLL obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="171e1-1127">An entry point in a required DLL could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1128">JET_errSessionContextAlreadySet-1912</span><span class="sxs-lookup"><span data-stu-id="171e1-1128">JET_errSessionContextAlreadySet -1912</span></span></p></td>
<td><p><span data-ttu-id="171e1-1129">Per la sessione specificata è già impostato un contesto di sessione.</span><span class="sxs-lookup"><span data-stu-id="171e1-1129">The specified session already has a session context set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1130">JET_errSessionContextNotSetByThisThread-1913</span><span class="sxs-lookup"><span data-stu-id="171e1-1130">JET_errSessionContextNotSetByThisThread -1913</span></span></p></td>
<td><p><span data-ttu-id="171e1-1131">È stato eseguito un tentativo di reimpostare il contesto della sessione, ma il thread corrente non è quello originale che ha impostato il contesto della sessione.</span><span class="sxs-lookup"><span data-stu-id="171e1-1131">An attempt was made to reset the session context, but the current thread was not the original one that set the session context.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1132">JET_errSessionInUse-1914</span><span class="sxs-lookup"><span data-stu-id="171e1-1132">JET_errSessionInUse -1914</span></span></p></td>
<td><p><span data-ttu-id="171e1-1133">È stato effettuato un tentativo di terminare la sessione attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="171e1-1133">An attempt was made to terminate the session currently in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1134">JET_errRecordFormatConversionFailed-1915</span><span class="sxs-lookup"><span data-stu-id="171e1-1134">JET_errRecordFormatConversionFailed -1915</span></span></p></td>
<td><p><span data-ttu-id="171e1-1135">Si è verificato un errore interno durante una conversione del formato di record dinamico.</span><span class="sxs-lookup"><span data-stu-id="171e1-1135">An internal error occurred during a dynamic record format conversion.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1136">JET_errOneDatabasePerSession-1916</span><span class="sxs-lookup"><span data-stu-id="171e1-1136">JET_errOneDatabasePerSession -1916</span></span></p></td>
<td><p><span data-ttu-id="171e1-1137">È consentito un solo database utente aperto per sessione, come indicato impostando il flag di <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> durante la creazione del database.</span><span class="sxs-lookup"><span data-stu-id="171e1-1137">Only one open user database per session is allowed (as indicated by setting the <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> flag during database creation).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1138">JET_errRollbackError-1917</span><span class="sxs-lookup"><span data-stu-id="171e1-1138">JET_errRollbackError -1917</span></span></p></td>
<td><p><span data-ttu-id="171e1-1139">Si è verificato un errore durante il rollback.</span><span class="sxs-lookup"><span data-stu-id="171e1-1139">There was an error during rollback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1140">JET_errCallbackFailed-2101</span><span class="sxs-lookup"><span data-stu-id="171e1-1140">JET_errCallbackFailed -2101</span></span></p></td>
<td><p><span data-ttu-id="171e1-1141">Chiamata di funzione di callback non riuscita.</span><span class="sxs-lookup"><span data-stu-id="171e1-1141">A callback function call failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1142">JET_errCallbackNotResolved-2102</span><span class="sxs-lookup"><span data-stu-id="171e1-1142">JET_errCallbackNotResolved -2102</span></span></p></td>
<td><p><span data-ttu-id="171e1-1143">Una funzione di callback non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="171e1-1143">A callback function could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1144">JET_errOSSnapshotInvalidSequence-2401</span><span class="sxs-lookup"><span data-stu-id="171e1-1144">JET_errOSSnapshotInvalidSequence -2401</span></span></p></td>
<td><p><span data-ttu-id="171e1-1145">L'API copia shadow del sistema operativo è stata usata in una sequenza non valida.</span><span class="sxs-lookup"><span data-stu-id="171e1-1145">The operating system shadow copy API was used in an invalid sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1146">JET_errOSSnapshotTimeOut-2402</span><span class="sxs-lookup"><span data-stu-id="171e1-1146">JET_errOSSnapshotTimeOut -2402</span></span></p></td>
<td><p><span data-ttu-id="171e1-1147">La copia shadow del sistema operativo è terminata con un timeout.</span><span class="sxs-lookup"><span data-stu-id="171e1-1147">The operating system shadow copy ended with a time-out.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1148">JET_errOSSnapshotNotAllowed-2403</span><span class="sxs-lookup"><span data-stu-id="171e1-1148">JET_errOSSnapshotNotAllowed -2403</span></span></p></td>
<td><p><span data-ttu-id="171e1-1149">La copia shadow del sistema operativo non è consentita perché è stato eseguito un backup o un ripristino in.</span><span class="sxs-lookup"><span data-stu-id="171e1-1149">The operating system shadow copy is not allowed because a backup or recovery in is progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1150">JET_errOSSnapshotInvalidSnapId-2404</span><span class="sxs-lookup"><span data-stu-id="171e1-1150">JET_errOSSnapshotInvalidSnapId -2404</span></span></p></td>
<td><p><span data-ttu-id="171e1-1151">L'operazione non è riuscita perché l'handle di copia shadow del sistema operativo specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="171e1-1151">The operation failed because the specified operating system shadow copy handle was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1152">JET_errLSCallbackNotSpecified-3000</span><span class="sxs-lookup"><span data-stu-id="171e1-1152">JET_errLSCallbackNotSpecified -3000</span></span></p></td>
<td><p><span data-ttu-id="171e1-1153">È stato effettuato un tentativo di usare l'archiviazione locale senza una funzione di callback specificata.</span><span class="sxs-lookup"><span data-stu-id="171e1-1153">An attempt was made to use local storage without a callback function being specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1154">JET_errLSAlreadySet-3001</span><span class="sxs-lookup"><span data-stu-id="171e1-1154">JET_errLSAlreadySet -3001</span></span></p></td>
<td><p><span data-ttu-id="171e1-1155">È stato effettuato un tentativo di impostare l'archiviazione locale per un oggetto per cui è già stato impostato.</span><span class="sxs-lookup"><span data-stu-id="171e1-1155">An attempt was made to set the local storage for an object which already had it set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1156">JET_errLSNotSet-3002</span><span class="sxs-lookup"><span data-stu-id="171e1-1156">JET_errLSNotSet -3002</span></span></p></td>
<td><p><span data-ttu-id="171e1-1157">È stato effettuato un tentativo di recuperare l'archiviazione locale da un oggetto che non è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="171e1-1157">An attempt was made to retrieve local storage from an object which did not have it set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1158">JET_errFileIOSparse-4000</span><span class="sxs-lookup"><span data-stu-id="171e1-1158">JET_errFileIOSparse -4000</span></span></p></td>
<td><p><span data-ttu-id="171e1-1159">Un'operazione di I/O non è riuscita perché è stata tentata in un'area non allocata di un file.</span><span class="sxs-lookup"><span data-stu-id="171e1-1159">An I/O operation failed because it was attempted against an unallocated region of a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1160">JET_errFileIOBeyondEOF-4001</span><span class="sxs-lookup"><span data-stu-id="171e1-1160">JET_errFileIOBeyondEOF -4001</span></span></p></td>
<td><p><span data-ttu-id="171e1-1161">Una lettura è stata rilasciata in una posizione successiva alla EOF (le Scritture espanderanno il file).</span><span class="sxs-lookup"><span data-stu-id="171e1-1161">A read was issued to a location beyond the EOF (writes will expand the file).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1162">JET_errFileIOAbort-4002</span><span class="sxs-lookup"><span data-stu-id="171e1-1162">JET_errFileIOAbort -4002</span></span></p></td>
<td><p><span data-ttu-id="171e1-1163">Questo flag indica al chiamante del JET_ABORTRETRYFAILCALLBACK di interrompere l'i/O specificato.</span><span class="sxs-lookup"><span data-stu-id="171e1-1163">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to abort the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1164">JET_errFileIORetry-4003</span><span class="sxs-lookup"><span data-stu-id="171e1-1164">JET_errFileIORetry -4003</span></span></p></td>
<td><p><span data-ttu-id="171e1-1165">Questo flag indica al chiamante del JET_ABORTRETRYFAILCALLBACK di ritentare l'i/O specificato.</span><span class="sxs-lookup"><span data-stu-id="171e1-1165">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to retry the specified I/O.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1166">JET_errFileIOFail-4004</span><span class="sxs-lookup"><span data-stu-id="171e1-1166">JET_errFileIOFail -4004</span></span></p></td>
<td><p><span data-ttu-id="171e1-1167">Questo flag indica al chiamante del JET_ABORTRETRYFAILCALLBACK di non eseguire l'i/O specificato.</span><span class="sxs-lookup"><span data-stu-id="171e1-1167">This flag instructs the JET_ABORTRETRYFAILCALLBACK caller to fail the specified I/O.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1168">JET_errFileCompressed-4005</span><span class="sxs-lookup"><span data-stu-id="171e1-1168">JET_errFileCompressed -4005</span></span></p></td>
<td><p><span data-ttu-id="171e1-1169">L'accesso in lettura/scrittura non è supportato nei file compressi.</span><span class="sxs-lookup"><span data-stu-id="171e1-1169">Read/write access is not supported on compressed files.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="171e1-1170">Commenti</span><span class="sxs-lookup"><span data-stu-id="171e1-1170">Remarks</span></span>

<span data-ttu-id="171e1-1171">In generale, un valore maggiore di zero deve essere interpretato come un avviso, un valore pari a zero deve essere interpretato come esito positivo e un valore minore di zero deve essere interpretato come un errore.</span><span class="sxs-lookup"><span data-stu-id="171e1-1171">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="171e1-1172">Nessun altro modello in questi valori, ad esempio intervalli di valori, deve essere basato su un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="171e1-1172">No other patterns in these values, such as ranges of values, should be relied upon by an application.</span></span>

### <a name="requirements"></a><span data-ttu-id="171e1-1173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="171e1-1173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1174"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="171e1-1174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="171e1-1175">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="171e1-1175">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="171e1-1176"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="171e1-1176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="171e1-1177">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="171e1-1177">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="171e1-1178"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="171e1-1178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="171e1-1179">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="171e1-1179">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="171e1-1180">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="171e1-1180">See Also</span></span>

[<span data-ttu-id="171e1-1181">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="171e1-1181">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="171e1-1182">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="171e1-1182">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="171e1-1183">File del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="171e1-1183">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)
