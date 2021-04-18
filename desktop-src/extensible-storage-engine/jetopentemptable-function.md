---
description: 'Altre informazioni su: funzione JetOpenTempTable'
title: Funzione JetOpenTempTable
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66c58abc5cff433bb4d944e39c283ba712d7cebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305731"
---
# <a name="jetopentemptable-function"></a><span data-ttu-id="b32c0-103">Funzione JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="b32c0-103">JetOpenTempTable Function</span></span>


<span data-ttu-id="b32c0-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b32c0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable-function"></a><span data-ttu-id="b32c0-105">Funzione JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="b32c0-105">JetOpenTempTable Function</span></span>

<span data-ttu-id="b32c0-106">La funzione **JetOpenTempTable** crea una tabella temporanea con un solo indice.</span><span class="sxs-lookup"><span data-stu-id="b32c0-106">The **JetOpenTempTable** function creates a temporary table with a single index.</span></span> <span data-ttu-id="b32c0-107">Una tabella temporanea archivia e recupera i record esattamente come una tabella ordinaria creata con [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="b32c0-107">A temporary table stores and retrieves records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="b32c0-108">Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile.</span><span class="sxs-lookup"><span data-stu-id="b32c0-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="b32c0-109">Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale.</span><span class="sxs-lookup"><span data-stu-id="b32c0-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="b32c0-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b32c0-110">Parameters</span></span>

<span data-ttu-id="b32c0-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b32c0-111">*sesid*</span></span>

<span data-ttu-id="b32c0-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b32c0-112">The session to use.</span></span>

<span data-ttu-id="b32c0-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="b32c0-113">*prgcolumndef*</span></span>

<span data-ttu-id="b32c0-114">Definizioni di colonna per le colonne create nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="b32c0-115">Sono presenti **importanti** limitazioni per le opzioni di definizione di colonna utilizzate con una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-115">**Important**   limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="b32c0-116">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b32c0-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="b32c0-117">Oltre alle normali opzioni di definizione di colonna, è possibile specificare anche zero o più delle opzioni seguenti che sono rilevanti solo nel contesto di una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b32c0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b32c0-118">Value</span></span></p></th>
<th><p><span data-ttu-id="b32c0-119">Significato</span><span class="sxs-lookup"><span data-stu-id="b32c0-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="b32c0-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="b32c0-121">Il tipo di ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente.</span><span class="sxs-lookup"><span data-stu-id="b32c0-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="b32c0-122">Se questa opzione viene specificata senza JET_bitColumnTTKey, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="b32c0-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="b32c0-124">La colonna sarà una colonna chiave per la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="b32c0-125">L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="b32c0-126">La prima definizione di colonna nella matrice con questo set di opzioni sarà la colonna chiave più significativa e così via.</span><span class="sxs-lookup"><span data-stu-id="b32c0-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="b32c0-127">Se sono richieste più colonne chiave che possono essere supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</span><span class="sxs-lookup"><span data-stu-id="b32c0-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b32c0-128">*CColumn*</span><span class="sxs-lookup"><span data-stu-id="b32c0-128">*ccolumn*</span></span>

<span data-ttu-id="b32c0-129">Vedere *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="b32c0-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="b32c0-130">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b32c0-130">*grbit*</span></span>

<span data-ttu-id="b32c0-131">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b32c0-131">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b32c0-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b32c0-132">Value</span></span></p></th>
<th><p><span data-ttu-id="b32c0-133">Significato</span><span class="sxs-lookup"><span data-stu-id="b32c0-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-134">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="b32c0-134">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="b32c0-135">Eventuali tentativi di inserire un record con la stessa chiave di indice di un record inserito in precedenza avranno immediatamente esito negativo con JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="b32c0-135">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="b32c0-136">Se questa opzione non è richiesta, un duplicato viene rilevato immediatamente e non riesce o viene rimosso automaticamente in un secondo momento, a seconda della strategia scelta dal motore di database per implementare la tabella temporanea, in base alla funzionalità richiesta.</span><span class="sxs-lookup"><span data-stu-id="b32c0-136">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="b32c0-137">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="b32c0-137">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="b32c0-138">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b32c0-138">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-139">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="b32c0-139">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="b32c0-140">Impone al gestore tabelle temporaneo di abbandonare la ricerca della strategia migliore per utilizzare la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b32c0-140">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-141">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="b32c0-141">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="b32c0-142">La tabella temporanea viene creata solo se Gestione tabelle temporanee è in grado di utilizzare l'implementazione ottimizzata per i risultati intermedi delle query.</span><span class="sxs-lookup"><span data-stu-id="b32c0-142">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="b32c0-143">Se una caratteristica della tabella temporanea impedisce l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="b32c0-143">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="b32c0-144">Un effetto collaterale di questa opzione consiste nel consentire alla tabella temporanea di contenere record con chiavi di indice duplicate.</span><span class="sxs-lookup"><span data-stu-id="b32c0-144">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="b32c0-145">Per ulteriori informazioni, vedere JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="b32c0-145">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="b32c0-146">Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b32c0-146">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-147">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="b32c0-147">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="b32c0-148">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di <a href="gg294103(v=exchg.10).md">JetSeek</a> per la ricerca di record in base alla chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="b32c0-148">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="b32c0-149">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="b32c0-149">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="b32c0-150">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b32c0-150">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-151">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="b32c0-151">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="b32c0-152">Richiede la rimozione dei record con chiavi di indice duplicate dal set di record finale nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-152">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="b32c0-153">Prima di Windows Server 2003, il motore di database presuppone sempre che questa opzione sia attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci.</span><span class="sxs-lookup"><span data-stu-id="b32c0-153">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="b32c0-154">A partire da Windows Server 2003, è ora possibile creare una tabella temporanea che non rimuove i duplicati quando viene specificata anche l'opzione JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="b32c0-154">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="b32c0-155">Non è possibile stabilire quale duplicato avrà esito positivo e quali duplicati verranno rimossi, in generale.</span><span class="sxs-lookup"><span data-stu-id="b32c0-155">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="b32c0-156">Tuttavia, quando viene richiesta l'opzione JET_bitTTErrorOnDuplicateInsertion, il primo record con una chiave di indice specificata da inserire nella tabella temporanea avrà sempre esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b32c0-156">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-157">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="b32c0-157">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="b32c0-158">Richiede che la tabella temporanea sia sufficientemente flessibile da consentire la modifica successiva dei record inseriti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b32c0-158">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="b32c0-159">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="b32c0-159">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="b32c0-160">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b32c0-160">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-161">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="b32c0-161">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="b32c0-162">Richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi arbitraria dei record in ordine e direzione arbitrari usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="b32c0-162">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="b32c0-163">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="b32c0-163">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="b32c0-164">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b32c0-164">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-165">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="b32c0-165">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="b32c0-166">Richiede che i valori della colonna chiave NULL siano ordinati più vicino alla fine dell'indice rispetto ai valori di colonna chiave non NULL.</span><span class="sxs-lookup"><span data-stu-id="b32c0-166">Requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-167">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="b32c0-167">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="b32c0-168">Richieste per consentire solo valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="b32c0-168">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="b32c0-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b32c0-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b32c0-170">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="b32c0-170">*ptableid*</span></span>

<span data-ttu-id="b32c0-171">Il buffer di output che riceve il nuovo cursore aperto nella tabella temporanea appena creata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-171">The output buffer that receives the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="b32c0-172">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="b32c0-172">*prgcolumnid*</span></span>

<span data-ttu-id="b32c0-173">Buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-173">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="b32c0-174">Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="b32c0-174">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="b32c0-175">Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione della matrice di input.</span><span class="sxs-lookup"><span data-stu-id="b32c0-175">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="b32c0-176">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b32c0-176">Return Value</span></span>

<span data-ttu-id="b32c0-177">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="b32c0-177">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b32c0-178">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="b32c0-178">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b32c0-179">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b32c0-179">Return code</span></span></p></th>
<th><p><span data-ttu-id="b32c0-180">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b32c0-180">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-181">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b32c0-181">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b32c0-182">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="b32c0-182">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-183">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="b32c0-183">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="b32c0-184"><strong>JetOpenTempTable</strong> non riuscito perché è stato specificato JET_bitTTForwardOnly e non è stato possibile creare la tabella temporanea specificata con l'ottimizzazione di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="b32c0-184"><strong>JetOpenTempTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="b32c0-185">Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b32c0-185">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-186">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b32c0-186">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b32c0-187">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b32c0-187">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-188">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="b32c0-188">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="b32c0-189">Impossibile creare l'indice perché è stata specificata una definizione di indice non valida.</span><span class="sxs-lookup"><span data-stu-id="b32c0-189">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="b32c0-190"><strong>JetOpenTempTable</strong> restituirà questo errore quando:</span><span class="sxs-lookup"><span data-stu-id="b32c0-190"><strong>JetOpenTempTable</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="b32c0-191">Le impostazioni locali indipendenti dalla lingua sono specificate.</span><span class="sxs-lookup"><span data-stu-id="b32c0-191">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="b32c0-192">È stato specificato un set di flag di normalizzazione non valido.</span><span class="sxs-lookup"><span data-stu-id="b32c0-192">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="b32c0-193">Questo errore verrà restituito solo da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b32c0-193">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b32c0-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b32c0-195">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="b32c0-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="b32c0-196">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b32c0-196">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-197">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="b32c0-197">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="b32c0-198">Il campo CP del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida.</span><span class="sxs-lookup"><span data-stu-id="b32c0-198">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="b32c0-199">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="b32c0-199">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="b32c0-200">Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="b32c0-200">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-201">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="b32c0-201">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="b32c0-202">Il campo <em>coltyp</em> del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su un tipo di colonna valido.</span><span class="sxs-lookup"><span data-stu-id="b32c0-202">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="b32c0-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="b32c0-204">Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un ID delle impostazioni locali non valido.</span><span class="sxs-lookup"><span data-stu-id="b32c0-204">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="b32c0-205">È possibile che l'ID delle impostazioni locali sia completamente non valido o che il Language Pack associato non sia installato.</span><span class="sxs-lookup"><span data-stu-id="b32c0-205">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-206">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="b32c0-206">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="b32c0-207">Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un set di flag di normalizzazione non valido.</span><span class="sxs-lookup"><span data-stu-id="b32c0-207">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="b32c0-208">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b32c0-208">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="b32c0-209">In Windows 2000, i flag di normalizzazione non validi comporteranno invece JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="b32c0-209">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-210">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="b32c0-210">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="b32c0-211">L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</span><span class="sxs-lookup"><span data-stu-id="b32c0-211">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="b32c0-212"><strong>Nota</strong>  Questo errore non viene restituito in tutte le circostanze.</span><span class="sxs-lookup"><span data-stu-id="b32c0-212"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="b32c0-213">Gli handle vengono convalidati solo in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="b32c0-213">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-214">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b32c0-214">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b32c0-215">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-215">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-216">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="b32c0-216">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="b32c0-217">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore.</span><span class="sxs-lookup"><span data-stu-id="b32c0-217">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="b32c0-218">Le risorse del cursore vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="b32c0-218">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-219">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="b32c0-219">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="b32c0-220">L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="b32c0-220">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="b32c0-221"><strong>JetOpenTempTable</strong> può restituire JET_errOutOfMemory se lo spazio degli indirizzi del processo host diventa troppo frammentato.</span><span class="sxs-lookup"><span data-stu-id="b32c0-221"><strong>JetOpenTempTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="b32c0-222">Il gestore tabelle temporanee allocherà sempre un blocco di spazio degli indirizzi pari a 1 MB per ogni tabella temporanea creata indipendentemente dalla quantità di dati da archiviare.</span><span class="sxs-lookup"><span data-stu-id="b32c0-222">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-223">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b32c0-223">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b32c0-224">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="b32c0-224">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-225">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b32c0-225">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b32c0-226">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="b32c0-226">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="b32c0-227">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b32c0-227">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-228">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b32c0-228">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b32c0-229">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-229">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-230">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="b32c0-230">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="b32c0-231">È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella.</span><span class="sxs-lookup"><span data-stu-id="b32c0-231">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="b32c0-232">Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="b32c0-232">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-233">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="b32c0-233">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="b32c0-234">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella.</span><span class="sxs-lookup"><span data-stu-id="b32c0-234">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="b32c0-235">Il numero di indici il cui schema può essere memorizzato nella cache viene configurato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="b32c0-235">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-236">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="b32c0-236">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="b32c0-237">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella.</span><span class="sxs-lookup"><span data-stu-id="b32c0-237">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="b32c0-238">Il numero di tabelle il cui schema può essere memorizzato nella cache viene configurato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="b32c0-238">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-239">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="b32c0-239">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="b32c0-240">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-240">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="b32c0-241">Le risorse della tabella temporanea vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="b32c0-241">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b32c0-242">In seguito all'esito positivo, verrà restituito un cursore aperto nella tabella temporanea appena creata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-242">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="b32c0-243">Lo stato del database temporaneo sarà pronto per contenere la nuova tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-243">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="b32c0-244">Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="b32c0-244">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="b32c0-245">In caso di errore, la tabella temporanea non verrà creata e non verrà restituito un cursore.</span><span class="sxs-lookup"><span data-stu-id="b32c0-245">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="b32c0-246">Lo stato del database temporaneo può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="b32c0-246">The state of the temporary database may be changed.</span></span> <span data-ttu-id="b32c0-247">Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="b32c0-247">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b32c0-248">Commenti</span><span class="sxs-lookup"><span data-stu-id="b32c0-248">Remarks</span></span>

<span data-ttu-id="b32c0-249">Le tabelle temporanee non supportano il complemento completo delle opzioni di definizione di colonna normalmente supportate dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="b32c0-249">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="b32c0-250">In realtà, sono supportati solo JET_bitColumnFixed e JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="b32c0-250">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="b32c0-251">Ciò significa che non è possibile creare un incremento automatico, una versione o una colonna multivalore in una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-251">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="b32c0-252">Infine, le colonne di aggiornamento del deposito a garanzia non sono supportate perché non sono utili in una tabella temporanea perché possono essere utilizzate solo da una sessione alla volta.</span><span class="sxs-lookup"><span data-stu-id="b32c0-252">Finally, escrow update columns are not supported because they are not useful in a temporary table since they can only be used by one session at a time.</span></span> <span data-ttu-id="b32c0-253">Se viene richiesta una qualsiasi di queste opzioni, queste verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="b32c0-253">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="b32c0-254">Le tabelle temporanee non supportano i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="b32c0-254">Temporary tables do not support default values.</span></span> <span data-ttu-id="b32c0-255">Se viene fornita una definizione di colonna contenente una specifica del valore predefinito, tale specifica verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-255">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="b32c0-256">Le tabelle temporanee vengono restituite al chiamante in seguito a numerose funzioni ESE diverse.</span><span class="sxs-lookup"><span data-stu-id="b32c0-256">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="b32c0-257">Ad esempio, [JetGetIndexInfo](./jetgetindexinfo-function.md) con l'opzione JET_IdxInfo impostata nel parametro *InfoLevel* restituirà una tabella temporanea contenente un elenco di tutte le colonne chiave di un indice specificato.</span><span class="sxs-lookup"><span data-stu-id="b32c0-257">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set in the *InfoLevel* parameter will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="b32c0-258">Le tabelle temporanee seguono le stesse regole del ciclo di vita delle tabelle temporanee comuni, come descritto qui.</span><span class="sxs-lookup"><span data-stu-id="b32c0-258">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="b32c0-259">Le tabelle temporanee vengono inoltre utilizzate internamente dal motore di database per molte attività.</span><span class="sxs-lookup"><span data-stu-id="b32c0-259">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="b32c0-260">La più importante di queste attività è la creazione di un indice su una tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="b32c0-260">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="b32c0-261">Una tabella temporanea verrà utilizzata per ordinare le chiavi di indice utilizzate per costruire tale indice.</span><span class="sxs-lookup"><span data-stu-id="b32c0-261">A temporary table will be used to sort the index keys used to construct that index.</span></span>

<span data-ttu-id="b32c0-262">Tutte le tabelle temporanee vengono archiviate nel database temporaneo.</span><span class="sxs-lookup"><span data-stu-id="b32c0-262">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="b32c0-263">Il database temporaneo è un file di database speciale mantenuto durante la durata di un'istanza ESE e viene eliminato quando l'istanza viene arrestata o riavviata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-263">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="b32c0-264">Il percorso del database temporaneo può essere configurato tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b32c0-264">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="b32c0-265">La posizione del database temporaneo su disco rispetto ai file di log delle transazioni e dei file di database può essere importante se l'applicazione usa in modo intensivo le tabelle temporanee o crea gli indici di frequente.</span><span class="sxs-lookup"><span data-stu-id="b32c0-265">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="b32c0-266">Il ciclo di vita di una tabella temporanea è associato ai cursori che vi fanno riferimento.</span><span class="sxs-lookup"><span data-stu-id="b32c0-266">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="b32c0-267">Se tutti i cursori che fanno riferimento a una tabella temporanea sono chiusi, in modo implicito o esplicito, la tabella temporanea verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-267">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="b32c0-268">Se una tabella temporanea viene creata all'interno di una transazione e successivamente viene eseguito il rollback della transazione, la tabella temporanea verrà eliminata perché i cursori che vi fanno riferimento in questo momento verranno chiusi in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="b32c0-268">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="b32c0-269">I nuovi cursori possono fare riferimento a una tabella temporanea solo tramite l'uso di [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="b32c0-269">New cursors may reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="b32c0-270">In questo caso, i nuovi cursori verranno posizionati sulla prima voce di indice della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-270">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="b32c0-271">[JetDupCursor](./jetdupcursor-function.md) funzionerà solo durante determinate fasi di utilizzo della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-271">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="b32c0-272">Per ulteriori informazioni, vedere le osservazioni relative alle funzionalità del cursore della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-272">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="b32c0-273">Non è possibile fare riferimento a una tabella temporanea da più di una sessione alla volta.</span><span class="sxs-lookup"><span data-stu-id="b32c0-273">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="b32c0-274">Si è verificato un problema importante in [JetDupCursor](./jetdupcursor-function.md) che influiscono sulle tabelle temporanee.</span><span class="sxs-lookup"><span data-stu-id="b32c0-274">There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="b32c0-275">Se viene effettuato un tentativo di duplicare una tabella temporanea in modalità di sola trasmissione, il cursore risultante non verrà creato correttamente e non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="b32c0-275">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="b32c0-276">È comunque possibile duplicare un cursore su una tabella temporanea materializzata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-276">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="b32c0-277">Il gestore tabelle temporaneo può scegliere di implementare una tabella temporanea in tre modi.</span><span class="sxs-lookup"><span data-stu-id="b32c0-277">The temporary table manager may choose to implement a temporary table in three ways.</span></span> <span data-ttu-id="b32c0-278">Il primo metodo consiste nel mantenere una tabella in memoria.</span><span class="sxs-lookup"><span data-stu-id="b32c0-278">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="b32c0-279">Questa strategia è la più veloce, ma può essere usata solo per semplici tabelle temporanee.</span><span class="sxs-lookup"><span data-stu-id="b32c0-279">This strategy is the fastest but can only be used for small, simple temporary tables.</span></span> <span data-ttu-id="b32c0-280">Il secondo metodo consiste nel creare un ordinamento basato su disco che può essere guidato utilizzando un iteratore di tipo "solo".</span><span class="sxs-lookup"><span data-stu-id="b32c0-280">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="b32c0-281">Questa strategia può essere utilizzata solo in determinate circostanze ed è il modo più rapido per ordinare e rimuovere i duplicati da un set di dati di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b32c0-281">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="b32c0-282">Il terzo metodo consiste nel creare un albero B + nel database temporaneo che contenga la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-282">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="b32c0-283">Questa strategia è la più lenta, ma la più versatile, ed è definita tabella temporanea materializzata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-283">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="b32c0-284">Queste strategie possono essere usate in combinazione per ottenere in definitiva la funzionalità richiesta della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-284">These strategies may be used in combination to ultimately achieve the functionality requested of the temporary table.</span></span>

<span data-ttu-id="b32c0-285">Quando la tabella temporanea non viene materializzata, viene utilizzata principalmente in due fasi principali.</span><span class="sxs-lookup"><span data-stu-id="b32c0-285">When the temporary table is not materialized then it is used in primarily two major phases.</span></span> <span data-ttu-id="b32c0-286">La prima fase è la fase di inserimento in cui la tabella viene popolata con il set di dati iniziale.</span><span class="sxs-lookup"><span data-stu-id="b32c0-286">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="b32c0-287">Durante questa fase, è consentito solo l'inserimento di dati.</span><span class="sxs-lookup"><span data-stu-id="b32c0-287">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="b32c0-288">Questa fase termina quando viene effettuato un tentativo di spostare il cursore utilizzando [JetMove](./jetmove-function.md) o [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="b32c0-288">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="b32c0-289">La seconda fase è la fase di estrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="b32c0-289">The second phase is the data extraction phase.</span></span> <span data-ttu-id="b32c0-290">Durante questa fase, i dati archiviati nella tabella temporanea possono essere estratti in base alle funzionalità richieste durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="b32c0-290">During this phase, the data stored in the temporary table may be extracted according to the capabilities requested when the temporary table was created.</span></span>

<span data-ttu-id="b32c0-291">**Funzionalità del cursore tabella temporanea**</span><span class="sxs-lookup"><span data-stu-id="b32c0-291">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="b32c0-292">Quando la tabella temporanea viene materializzata, il cursore presenta le funzionalità seguenti, ma può essere ulteriormente limitato dalle opzioni richieste:</span><span class="sxs-lookup"><span data-stu-id="b32c0-292">When the temporary table is materialized, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="b32c0-293">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b32c0-293">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="b32c0-294">JetDelete</span><span class="sxs-lookup"><span data-stu-id="b32c0-294">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="b32c0-295">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b32c0-295">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="b32c0-296">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="b32c0-296">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="b32c0-297">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="b32c0-297">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="b32c0-298">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="b32c0-298">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="b32c0-299">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="b32c0-299">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="b32c0-300">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="b32c0-300">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="b32c0-301">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="b32c0-301">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="b32c0-302">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="b32c0-302">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="b32c0-303">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="b32c0-303">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="b32c0-304">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b32c0-304">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="b32c0-305">JetMove</span><span class="sxs-lookup"><span data-stu-id="b32c0-305">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="b32c0-306">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="b32c0-306">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="b32c0-307">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="b32c0-307">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="b32c0-308">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="b32c0-308">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="b32c0-309">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="b32c0-309">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="b32c0-310">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b32c0-310">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="b32c0-311">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="b32c0-311">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="b32c0-312">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="b32c0-312">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="b32c0-313">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b32c0-313">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="b32c0-314">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="b32c0-314">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="b32c0-315">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="b32c0-315">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="b32c0-316">Quando la tabella temporanea non viene materializzata e si trova nella fase di inserimento, il cursore presenta le funzionalità seguenti, ma può essere ulteriormente limitato dalle opzioni richieste:</span><span class="sxs-lookup"><span data-stu-id="b32c0-316">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="b32c0-317">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b32c0-317">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="b32c0-318">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="b32c0-318">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="b32c0-319">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b32c0-319">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="b32c0-320">JetMove</span><span class="sxs-lookup"><span data-stu-id="b32c0-320">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="b32c0-321">**Nota**  Causa la transizione alla fase di estrazione.</span><span class="sxs-lookup"><span data-stu-id="b32c0-321">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="b32c0-322">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="b32c0-322">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="b32c0-323">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="b32c0-323">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="b32c0-324">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b32c0-324">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="b32c0-325">**Nota**  Causa la transizione alla fase di estrazione.</span><span class="sxs-lookup"><span data-stu-id="b32c0-325">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="b32c0-326">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="b32c0-326">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="b32c0-327">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="b32c0-327">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="b32c0-328">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="b32c0-328">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="b32c0-329">Quando la tabella temporanea non viene materializzata e si trova nella fase di estrazione, il cursore presenta le funzionalità seguenti, ma può essere ulteriormente limitato dalle opzioni richieste:</span><span class="sxs-lookup"><span data-stu-id="b32c0-329">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="b32c0-330">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b32c0-330">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="b32c0-331">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b32c0-331">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="b32c0-332">**Nota**  Se viene effettuato un tentativo di duplicare una tabella temporanea in modalità di sola trasmissione, il cursore risultante non verrà creato correttamente e non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="b32c0-332">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="b32c0-333">È comunque possibile duplicare un cursore su una tabella temporanea materializzata.</span><span class="sxs-lookup"><span data-stu-id="b32c0-333">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="b32c0-334">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="b32c0-334">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="b32c0-335">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="b32c0-335">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="b32c0-336">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="b32c0-336">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="b32c0-337">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="b32c0-337">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="b32c0-338">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="b32c0-338">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="b32c0-339">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="b32c0-339">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="b32c0-340">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="b32c0-340">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="b32c0-341">JetMove</span><span class="sxs-lookup"><span data-stu-id="b32c0-341">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="b32c0-342">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="b32c0-342">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="b32c0-343">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="b32c0-343">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="b32c0-344">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="b32c0-344">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="b32c0-345">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b32c0-345">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="b32c0-346">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b32c0-346">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="b32c0-347">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="b32c0-347">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="b32c0-348">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b32c0-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-349"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b32c0-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b32c0-350">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b32c0-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-351"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b32c0-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b32c0-352">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b32c0-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-353"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b32c0-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b32c0-354">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b32c0-354">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b32c0-355"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="b32c0-355"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b32c0-356">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b32c0-356">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b32c0-357"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b32c0-357"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b32c0-358">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b32c0-358">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b32c0-359">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b32c0-359">See Also</span></span>

[<span data-ttu-id="b32c0-360">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="b32c0-360">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="b32c0-361">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="b32c0-361">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="b32c0-362">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b32c0-362">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b32c0-363">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b32c0-363">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b32c0-364">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b32c0-364">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b32c0-365">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b32c0-365">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b32c0-366">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="b32c0-366">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="b32c0-367">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="b32c0-367">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="b32c0-368">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="b32c0-368">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="b32c0-369">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="b32c0-369">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="b32c0-370">JetMove</span><span class="sxs-lookup"><span data-stu-id="b32c0-370">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="b32c0-371">JetRollback</span><span class="sxs-lookup"><span data-stu-id="b32c0-371">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="b32c0-372">JetSeek</span><span class="sxs-lookup"><span data-stu-id="b32c0-372">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="b32c0-373">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="b32c0-373">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="b32c0-374">Parametri di database temporanei</span><span class="sxs-lookup"><span data-stu-id="b32c0-374">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
