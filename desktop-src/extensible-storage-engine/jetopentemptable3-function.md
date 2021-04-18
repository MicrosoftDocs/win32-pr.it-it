---
description: 'Altre informazioni su: funzione JetOpenTempTable3'
title: Funzione JetOpenTempTable3
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7820f90ef0192c1f700759835bf1572b187cf3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305730"
---
# <a name="jetopentemptable3-function"></a><span data-ttu-id="e558c-103">Funzione JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="e558c-103">JetOpenTempTable3 Function</span></span>


<span data-ttu-id="e558c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e558c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable3-function"></a><span data-ttu-id="e558c-105">Funzione JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="e558c-105">JetOpenTempTable3 Function</span></span>

<span data-ttu-id="e558c-106">La funzione **JetOpenTempTable3** crea una tabella temporanea con un solo indice che può essere usato per archiviare e recuperare record come una tabella ordinaria creata usando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="e558c-106">The **JetOpenTempTable3** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="e558c-107">Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile.</span><span class="sxs-lookup"><span data-stu-id="e558c-107">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="e558c-108">Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale.</span><span class="sxs-lookup"><span data-stu-id="e558c-108">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="e558c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e558c-109">Parameters</span></span>

<span data-ttu-id="e558c-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e558c-110">*sesid*</span></span>

<span data-ttu-id="e558c-111">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="e558c-111">The session to use for this call.</span></span>

<span data-ttu-id="e558c-112">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="e558c-112">*prgcolumndef*</span></span>

<span data-ttu-id="e558c-113">Identifica le definizioni di colonna delle colonne da creare nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-113">Identifies the column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="e558c-114">Per le opzioni di definizione di colonna che possono essere utilizzate con una tabella temporanea sono presenti importanti limitazioni.</span><span class="sxs-lookup"><span data-stu-id="e558c-114">Important limitations exist to the column definition options that may be used with a temporary table.</span></span> <span data-ttu-id="e558c-115">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e558c-115">See the Remarks section for more information.</span></span>

<span data-ttu-id="e558c-116">Oltre alle normali opzioni di definizione di colonna, è possibile specificare anche zero o più delle opzioni seguenti che sono rilevanti solo nel contesto di una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-116">In addition to the usual column definition options, zero or more of the following options may also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e558c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e558c-117">Value</span></span></p></th>
<th><p><span data-ttu-id="e558c-118">Significato</span><span class="sxs-lookup"><span data-stu-id="e558c-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e558c-119">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="e558c-119">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="e558c-120">Questa opzione indica che l'ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente.</span><span class="sxs-lookup"><span data-stu-id="e558c-120">This option indicates that the sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="e558c-121">Se questa opzione viene specificata senza JET_bitColumnTTKey, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="e558c-121">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-122">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="e558c-122">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="e558c-123">Questa opzione indica che la colonna sarà una colonna chiave per la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-123">This option indicates that the column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="e558c-124">L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-124">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="e558c-125">La prima definizione di colonna nella matrice con questo set di opzioni sarà la colonna chiave più significativa e così via.</span><span class="sxs-lookup"><span data-stu-id="e558c-125">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="e558c-126">Se sono richieste più colonne chiave che possono essere supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</span><span class="sxs-lookup"><span data-stu-id="e558c-126">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e558c-127">*CColumn*</span><span class="sxs-lookup"><span data-stu-id="e558c-127">*ccolumn*</span></span>

<span data-ttu-id="e558c-128">Vedere *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="e558c-128">See *prgcolumndef*.</span></span>

<span data-ttu-id="e558c-129">*pidxunicode*</span><span class="sxs-lookup"><span data-stu-id="e558c-129">*pidxunicode*</span></span>

<span data-ttu-id="e558c-130">ID delle impostazioni locali e flag di normalizzazione che verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-130">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="e558c-131">Quando questo parametro non è presente, viene utilizzato il valore LCID predefinito per confrontare eventuali colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-131">When this parameter is not present then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="e558c-132">Il valore LCID predefinito corrisponde alle impostazioni locali per l'inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="e558c-132">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="e558c-133">Quando questo parametro non è presente, i flag di normalizzazione predefiniti verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-133">When this parameter is not present then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="e558c-134">I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="e558c-134">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="e558c-135">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e558c-135">*grbit*</span></span>

<span data-ttu-id="e558c-136">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e558c-136">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e558c-137">Valore</span><span class="sxs-lookup"><span data-stu-id="e558c-137">Value</span></span></p></th>
<th><p><span data-ttu-id="e558c-138">Significato</span><span class="sxs-lookup"><span data-stu-id="e558c-138">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e558c-139">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="e558c-139">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="e558c-140">Questa opzione richiede che qualsiasi tentativo di inserire un record con la stessa chiave di indice di un record inserito in precedenza avrà immediatamente esito negativo con JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="e558c-140">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="e558c-141">Se questa opzione non è richiesta, è possibile che un duplicato venga rilevato immediatamente e non riesca o venga rimosso automaticamente in un secondo momento, a seconda della strategia scelta dal motore di database per implementare la tabella temporanea in base alla funzionalità richiesta.</span><span class="sxs-lookup"><span data-stu-id="e558c-141">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="e558c-142">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="e558c-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="e558c-143">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e558c-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-144">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="e558c-144">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="e558c-145">Questa opzione impone al gestore tabelle temporaneo di abbandonare qualsiasi tentativo di scegliere una strategia intelligente per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e558c-145">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-146">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="e558c-146">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="e558c-147">Questa opzione richiede che la tabella temporanea venga creata solo se Gestione tabelle temporanee è in grado di utilizzare l'implementazione ottimizzata per i risultati intermedi delle query.</span><span class="sxs-lookup"><span data-stu-id="e558c-147">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="e558c-148">Se una caratteristica della tabella temporanea impedisce l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="e558c-148">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="e558c-149">Un effetto collaterale di questa opzione consiste nel consentire alla tabella temporanea di contenere record con chiavi di indice duplicate.</span><span class="sxs-lookup"><span data-stu-id="e558c-149">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="e558c-150">Per ulteriori informazioni, vedere JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="e558c-150">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="e558c-151">Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e558c-151">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-152">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="e558c-152">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="e558c-153">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di <a href="gg294103(v=exchg.10).md">JetSeek</a> per la ricerca di record in base alla chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="e558c-153">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="e558c-154">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="e558c-154">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="e558c-155">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e558c-155">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-156">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="e558c-156">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="e558c-157">Questa opzione richiede che i record con chiavi di indice duplicate vengano rimossi dal set di record finale nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-157">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="e558c-158">Prima di Windows Server 2003, il motore di database presuppone sempre che questa opzione sia attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci.</span><span class="sxs-lookup"><span data-stu-id="e558c-158">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="e558c-159">A partire da Windows Server 2003, è ora possibile creare una tabella temporanea che non rimuove i duplicati quando viene specificata anche l'opzione JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="e558c-159">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="e558c-160">Non è possibile stabilire quale duplicato avrà vinto e quali duplicati verranno eliminati in generale.</span><span class="sxs-lookup"><span data-stu-id="e558c-160">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="e558c-161">Tuttavia, quando viene richiesta l'opzione JET_bitTTErrorOnDuplicateInsertion, il primo record con una chiave di indice specificata da inserire nella tabella temporanea sarà sempre vincente.</span><span class="sxs-lookup"><span data-stu-id="e558c-161">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-162">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="e558c-162">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="e558c-163">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile per consentire la modifica successiva dei record che sono stati inseriti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e558c-163">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="e558c-164">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="e558c-164">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="e558c-165">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e558c-165">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-166">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="e558c-166">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="e558c-167">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi dei record in ordine arbitrario e direzione usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="e558c-167">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="e558c-168">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="e558c-168">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="e558c-169">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e558c-169">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-170">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="e558c-170">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="e558c-171">Questa opzione richiede che i valori della colonna chiave NULL siano ordinati più vicino alla fine dell'indice rispetto ai valori di colonna chiave non NULL.</span><span class="sxs-lookup"><span data-stu-id="e558c-171">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-172">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="e558c-172">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="e558c-173">Richieste per consentire solo valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="e558c-173">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="e558c-174"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e558c-174"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e558c-175">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="e558c-175">*ptableid*</span></span>

<span data-ttu-id="e558c-176">Il buffer di output che riceverà il nuovo cursore aperto nella tabella temporanea appena creata.</span><span class="sxs-lookup"><span data-stu-id="e558c-176">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="e558c-177">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="e558c-177">*prgcolumnid*</span></span>

<span data-ttu-id="e558c-178">Buffer di output che riceverà la matrice di ID di colonna generati durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-178">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="e558c-179">Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="e558c-179">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="e558c-180">Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione della matrice di input.</span><span class="sxs-lookup"><span data-stu-id="e558c-180">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="e558c-181">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e558c-181">Return Value</span></span>

<span data-ttu-id="e558c-182">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="e558c-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e558c-183">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="e558c-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e558c-184">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e558c-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="e558c-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e558c-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e558c-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e558c-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e558c-187">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="e558c-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-188">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="e558c-188">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="e558c-189"><strong>JetOpenTempTable3</strong> non riuscito perché è stato specificato JET_bitTTForwardOnly e non è stato possibile creare la tabella temporanea specificata con l'ottimizzazione di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="e558c-189"><strong>JetOpenTempTable3</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="e558c-190">Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e558c-190">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-191">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e558c-191">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e558c-192">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e558c-192">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-193">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="e558c-193">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="e558c-194">Impossibile creare l'indice perché è stata specificata una definizione di indice non valida.</span><span class="sxs-lookup"><span data-stu-id="e558c-194">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="e558c-195"><strong>JetOpenTempTable3</strong> restituirà questo errore quando:</span><span class="sxs-lookup"><span data-stu-id="e558c-195"><strong>JetOpenTempTable3</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="e558c-196">Le impostazioni locali indipendenti dalla lingua sono specificate.</span><span class="sxs-lookup"><span data-stu-id="e558c-196">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="e558c-197">È stato specificato un set di flag di normalizzazione non valido.</span><span class="sxs-lookup"><span data-stu-id="e558c-197">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="e558c-198">Questo errore verrà restituito solo da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e558c-198">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-199">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e558c-199">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e558c-200">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="e558c-200">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e558c-201">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e558c-201">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-202">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="e558c-202">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="e558c-203">Il membro <strong>CP</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida.</span><span class="sxs-lookup"><span data-stu-id="e558c-203">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="e558c-204">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="e558c-204">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="e558c-205">Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="e558c-205">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-206">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="e558c-206">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="e558c-207">Il membro <strong>coltyp</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su un tipo di colonna valido.</span><span class="sxs-lookup"><span data-stu-id="e558c-207">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-208">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="e558c-208">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="e558c-209">Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un ID delle impostazioni locali non valido.</span><span class="sxs-lookup"><span data-stu-id="e558c-209">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="e558c-210">È possibile che l'ID delle impostazioni locali sia completamente non valido o che il Language Pack associato non sia installato.</span><span class="sxs-lookup"><span data-stu-id="e558c-210">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-211">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="e558c-211">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="e558c-212">Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un set di flag di normalizzazione non valido.</span><span class="sxs-lookup"><span data-stu-id="e558c-212">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="e558c-213">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e558c-213">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="e558c-214">In Windows 2000, i flag di normalizzazione non validi comporteranno invece JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="e558c-214">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-215">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="e558c-215">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="e558c-216">L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</span><span class="sxs-lookup"><span data-stu-id="e558c-216">The session handle is invalid or refers to a closed session.</span></span> <span data-ttu-id="e558c-217">Questo errore non viene restituito in tutte le circostanze.</span><span class="sxs-lookup"><span data-stu-id="e558c-217">This error is not returned under all circumstances.</span></span> <span data-ttu-id="e558c-218">Gli handle vengono convalidati solo in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="e558c-218">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-219">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e558c-219">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e558c-220">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="e558c-220">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-221">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="e558c-221">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="e558c-222">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore.</span><span class="sxs-lookup"><span data-stu-id="e558c-222">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="e558c-223">Le risorse del cursore vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="e558c-223">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-224">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="e558c-224">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="e558c-225">L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="e558c-225">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="e558c-226"><strong>JetOpenTempTable3</strong> può restituire JET_errOutOfMemory se lo spazio degli indirizzi del processo host diventa troppo frammentato.</span><span class="sxs-lookup"><span data-stu-id="e558c-226"><strong>JetOpenTempTable3</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="e558c-227">Il gestore tabelle temporanee allocherà sempre un blocco di spazio degli indirizzi pari a 1 MB per ogni tabella temporanea creata indipendentemente dalla quantità di dati da archiviare.</span><span class="sxs-lookup"><span data-stu-id="e558c-227">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e558c-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e558c-229">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="e558c-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e558c-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e558c-231">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="e558c-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="e558c-232">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e558c-232">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e558c-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e558c-234">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="e558c-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-235">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="e558c-235">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="e558c-236">È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella.</span><span class="sxs-lookup"><span data-stu-id="e558c-236">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="e558c-237">Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="e558c-237">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-238">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="e558c-238">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="e558c-239">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella.</span><span class="sxs-lookup"><span data-stu-id="e558c-239">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="e558c-240">Il numero di indici il cui schema può essere memorizzato nella cache viene configurato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="e558c-240">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-241">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="e558c-241">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="e558c-242">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella.</span><span class="sxs-lookup"><span data-stu-id="e558c-242">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="e558c-243">Il numero di tabelle il cui schema può essere memorizzato nella cache viene configurato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="e558c-243">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-244">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="e558c-244">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="e558c-245">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-245">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="e558c-246">Le risorse della tabella temporanea vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="e558c-246">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e558c-247">In seguito all'esito positivo, verrà restituito un cursore aperto nella tabella temporanea appena creata.</span><span class="sxs-lookup"><span data-stu-id="e558c-247">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="e558c-248">Lo stato del database temporaneo sarà pronto per contenere la nuova tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="e558c-248">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="e558c-249">Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="e558c-249">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="e558c-250">In caso di errore, la tabella temporanea non verrà creata e non verrà restituito un cursore.</span><span class="sxs-lookup"><span data-stu-id="e558c-250">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="e558c-251">Lo stato del database temporaneo può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="e558c-251">The state of the temporary database may be changed.</span></span> <span data-ttu-id="e558c-252">Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="e558c-252">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e558c-253">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e558c-253">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e558c-254"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e558c-254"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e558c-255">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e558c-255">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-256"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e558c-256"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e558c-257">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e558c-257">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-258"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="e558c-258"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e558c-259">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="e558c-259">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e558c-260"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="e558c-260"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e558c-261">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e558c-261">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e558c-262"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e558c-262"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e558c-263">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e558c-263">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e558c-264">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e558c-264">See Also</span></span>

[<span data-ttu-id="e558c-265">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="e558c-265">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="e558c-266">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="e558c-266">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="e558c-267">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="e558c-267">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="e558c-268">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e558c-268">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="e558c-269">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e558c-269">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e558c-270">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e558c-270">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e558c-271">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e558c-271">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e558c-272">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e558c-272">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e558c-273">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="e558c-273">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="e558c-274">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="e558c-274">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="e558c-275">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="e558c-275">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="e558c-276">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="e558c-276">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="e558c-277">JetMove</span><span class="sxs-lookup"><span data-stu-id="e558c-277">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="e558c-278">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="e558c-278">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="e558c-279">JetRollback</span><span class="sxs-lookup"><span data-stu-id="e558c-279">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="e558c-280">JetSeek</span><span class="sxs-lookup"><span data-stu-id="e558c-280">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="e558c-281">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="e558c-281">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="e558c-282">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="e558c-282">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
