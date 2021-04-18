---
description: 'Altre informazioni su: funzione JetOpenTempTable2'
title: Funzione JetOpenTempTable2
TOCTitle: JetOpenTempTable2 Function
ms:assetid: 788ec4f9-b0c3-409b-850c-7567dec47024
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269302(v=EXCHG.10)
ms:contentKeyID: 32765594
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 324bcde75c0ba9376c8ad9f5e98df585b1d341e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315619"
---
# <a name="jetopentemptable2-function"></a><span data-ttu-id="be572-103">Funzione JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="be572-103">JetOpenTempTable2 Function</span></span>


<span data-ttu-id="be572-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="be572-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable2-function"></a><span data-ttu-id="be572-105">Funzione JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="be572-105">JetOpenTempTable2 Function</span></span>

<span data-ttu-id="be572-106">La funzione **JetOpenTempTable2** crea una tabella temporanea con un solo indice che può essere usato per archiviare e recuperare record come una tabella ordinaria creata usando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="be572-106">The **JetOpenTempTable2** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="be572-107">Questa funzione dispone inoltre di un ID delle impostazioni locali che può essere utilizzato per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-107">This function also has a Locale ID that can be used to compare Unicode key column data in the temporary table.</span></span> <span data-ttu-id="be572-108">Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile.</span><span class="sxs-lookup"><span data-stu-id="be572-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="be572-109">Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale.</span><span class="sxs-lookup"><span data-stu-id="be572-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable2(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          unsigned long lcid,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="be572-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="be572-110">Parameters</span></span>

<span data-ttu-id="be572-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="be572-111">*sesid*</span></span>

<span data-ttu-id="be572-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="be572-112">The session to use.</span></span>

<span data-ttu-id="be572-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="be572-113">*prgcolumndef*</span></span>

<span data-ttu-id="be572-114">Definizioni di colonna delle colonne da creare nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-114">The column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="be572-115">Sono presenti importanti limitazioni per le opzioni di definizione di colonna utilizzate con una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-115">Important limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="be572-116">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="be572-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="be572-117">Oltre alle normali opzioni di definizione di colonna, è possibile specificare anche zero o più delle opzioni seguenti che sono rilevanti solo nel contesto di una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be572-118">Valore</span><span class="sxs-lookup"><span data-stu-id="be572-118">Value</span></span></p></th>
<th><p><span data-ttu-id="be572-119">Significato</span><span class="sxs-lookup"><span data-stu-id="be572-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be572-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="be572-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="be572-121">Il tipo di ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente.</span><span class="sxs-lookup"><span data-stu-id="be572-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="be572-122">Se questa opzione viene specificata senza JET_bitColumnTTKey, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="be572-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="be572-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="be572-124">La colonna sarà una colonna chiave per la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="be572-125">L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="be572-126">La prima definizione di colonna nella matrice con questo set di opzioni sarà la colonna chiave più significativa e così via.</span><span class="sxs-lookup"><span data-stu-id="be572-126">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="be572-127">Se sono richieste più colonne chiave che possono essere supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</span><span class="sxs-lookup"><span data-stu-id="be572-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be572-128">*CColumn*</span><span class="sxs-lookup"><span data-stu-id="be572-128">*ccolumn*</span></span>

<span data-ttu-id="be572-129">Vedere *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="be572-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="be572-130">*lcid*</span><span class="sxs-lookup"><span data-stu-id="be572-130">*lcid*</span></span>

<span data-ttu-id="be572-131">ID delle impostazioni locali da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-131">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="be572-132">Le impostazioni locali possono essere usate purché nel computer sia installato il Language Pack appropriato.</span><span class="sxs-lookup"><span data-stu-id="be572-132">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="be572-133">L'unica eccezione è che le impostazioni locali indipendenti dalla lingua (LCID di zero) non sono valide.</span><span class="sxs-lookup"><span data-stu-id="be572-133">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="be572-134">In Windows Server 2003 e versioni successive, se per questo parametro vengono specificate le impostazioni locali indipendenti dalla lingua, verrà usato l'ID delle impostazioni locali predefinito (Inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="be572-134">On Windows Server 2003 and later, if the Language Neutral locale is specified for this parameter then the default locale ID (U.S. English) will be used instead.</span></span> <span data-ttu-id="be572-135">Questo consente a un valore pari a zero di indicare l'impostazione predefinita anziché un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="be572-135">This is to allow a value of zero to signify the default rather than an illegal value.</span></span>

<span data-ttu-id="be572-136">Quando questo parametro non è presente e quando il parametro *pidxunicode* non è presente, viene usato il valore LCID predefinito per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-136">When this parameter is not present and when the *pidxunicode* parameter is not present, then the default LCID will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="be572-137">Il valore LCID predefinito corrisponde alle impostazioni locali per l'inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="be572-137">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="be572-138">*grbit*</span><span class="sxs-lookup"><span data-stu-id="be572-138">*grbit*</span></span>

<span data-ttu-id="be572-139">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="be572-139">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be572-140">Valore</span><span class="sxs-lookup"><span data-stu-id="be572-140">Value</span></span></p></th>
<th><p><span data-ttu-id="be572-141">Significato</span><span class="sxs-lookup"><span data-stu-id="be572-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be572-142">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="be572-142">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="be572-143">Questa opzione richiede che qualsiasi tentativo di inserire un record con la stessa chiave di indice di un record inserito in precedenza avrà immediatamente esito negativo con JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="be572-143">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="be572-144">Se questa opzione non è richiesta, è possibile che un duplicato venga rilevato immediatamente e non riesca o venga rimosso automaticamente in un secondo momento, a seconda della strategia scelta dal motore di database per implementare la tabella temporanea in base alla funzionalità richiesta.</span><span class="sxs-lookup"><span data-stu-id="be572-144">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="be572-145">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="be572-145">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="be572-146">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="be572-146">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-147">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="be572-147">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="be572-148">Questa opzione impone al gestore tabelle temporaneo di abbandonare qualsiasi tentativo di scegliere una strategia intelligente per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="be572-148">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-149">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="be572-149">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="be572-150">Questa opzione richiede che la tabella temporanea venga creata solo se Gestione tabelle temporanee è in grado di utilizzare l'implementazione ottimizzata per i risultati intermedi delle query.</span><span class="sxs-lookup"><span data-stu-id="be572-150">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="be572-151">Se una caratteristica della tabella temporanea impedisce l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="be572-151">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="be572-152">Un effetto collaterale di questa opzione consiste nel consentire alla tabella temporanea di contenere record con chiavi di indice duplicate.</span><span class="sxs-lookup"><span data-stu-id="be572-152">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="be572-153">Per ulteriori informazioni, vedere JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="be572-153">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="be572-154">Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="be572-154">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-155">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="be572-155">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="be572-156">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di <a href="gg294103(v=exchg.10).md">JetSeek</a> per la ricerca di record in base alla chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="be572-156">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="be572-157">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="be572-157">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="be572-158">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="be572-158">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-159">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="be572-159">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="be572-160">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi dei record in ordine arbitrario e direzione usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="be572-160">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="be572-161">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="be572-161">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="be572-162">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="be572-162">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-163">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="be572-163">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="be572-164">Questa opzione richiede che i valori della colonna chiave NULL siano ordinati più vicino alla fine dell'indice rispetto ai valori di colonna chiave non NULL.</span><span class="sxs-lookup"><span data-stu-id="be572-164">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-165">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="be572-165">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="be572-166">Questa opzione richiede che i record con chiavi di indice duplicate vengano rimossi dal set di record finale nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-166">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="be572-167">Prima di Windows Server 2003, il motore di database presuppone sempre che questa opzione sia attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci.</span><span class="sxs-lookup"><span data-stu-id="be572-167">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="be572-168">A partire da Windows Server 2003, è ora possibile creare una tabella temporanea che non rimuove i duplicati quando viene specificata anche l'opzione JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="be572-168">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="be572-169">Non è possibile stabilire quale duplicato avrà vinto e quali duplicati verranno eliminati in generale.</span><span class="sxs-lookup"><span data-stu-id="be572-169">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="be572-170">Tuttavia, quando viene richiesta l'opzione JET_bitTTErrorOnDuplicateInsertion, il primo record con una chiave di indice specificata da inserire nella tabella temporanea sarà sempre vincente.</span><span class="sxs-lookup"><span data-stu-id="be572-170">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-171">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="be572-171">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="be572-172">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile per consentire la modifica successiva dei record che sono stati inseriti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="be572-172">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="be572-173">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="be572-173">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="be572-174">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="be572-174">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-175">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="be572-175">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="be572-176">Richieste per consentire solo valori Long intrinseci.</span><span class="sxs-lookup"><span data-stu-id="be572-176">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="be572-177"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="be572-177"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be572-178">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="be572-178">*ptableid*</span></span>

<span data-ttu-id="be572-179">Il buffer di output che riceverà il nuovo cursore aperto nella tabella temporanea appena creata.</span><span class="sxs-lookup"><span data-stu-id="be572-179">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="be572-180">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="be572-180">*prgcolumnid*</span></span>

<span data-ttu-id="be572-181">Buffer di output che riceverà la matrice di ID di colonna generati durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-181">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="be572-182">Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="be572-182">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="be572-183">Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione della matrice di input.</span><span class="sxs-lookup"><span data-stu-id="be572-183">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="be572-184">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be572-184">Return Value</span></span>

<span data-ttu-id="be572-185">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="be572-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="be572-186">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="be572-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be572-187">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="be572-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="be572-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be572-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be572-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="be572-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="be572-190">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="be572-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-191">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="be572-191">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="be572-192"><strong>JetOpenTempTable2</strong> non riuscito perché è stato specificato JET_bitTTForwardOnly e non è stato possibile creare la tabella temporanea specificata con l'ottimizzazione di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="be572-192"><strong>JetOpenTempTable2</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="be572-193">Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="be572-193">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-194">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="be572-194">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="be572-195">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="be572-195">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-196">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="be572-196">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="be572-197">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="be572-197">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="be572-198">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="be572-198">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-199">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="be572-199">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="be572-200">Il campo CP del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida.</span><span class="sxs-lookup"><span data-stu-id="be572-200">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="be572-201">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="be572-201">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="be572-202">Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="be572-202">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-203">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="be572-203">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="be572-204">Il campo <em>coltyp</em> del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su un tipo di colonna valido.</span><span class="sxs-lookup"><span data-stu-id="be572-204">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-205">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="be572-205">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="be572-206">Impossibile creare l'indice perché è stata specificata una definizione di indice non valida.</span><span class="sxs-lookup"><span data-stu-id="be572-206">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="be572-207"><strong>JetOpenTempTable2</strong> restituirà questo errore quando:</span><span class="sxs-lookup"><span data-stu-id="be572-207"><strong>JetOpenTempTable2</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="be572-208">Le impostazioni locali indipendenti dalla lingua sono specificate.</span><span class="sxs-lookup"><span data-stu-id="be572-208">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="be572-209">È stato specificato un set di flag di normalizzazione non valido.</span><span class="sxs-lookup"><span data-stu-id="be572-209">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="be572-210">Questo errore verrà restituito solo da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="be572-210">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-211">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="be572-211">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="be572-212">Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un ID delle impostazioni locali non valido.</span><span class="sxs-lookup"><span data-stu-id="be572-212">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="be572-213">È possibile che l'ID delle impostazioni locali sia completamente non valido o che il Language Pack associato non sia installato.</span><span class="sxs-lookup"><span data-stu-id="be572-213">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-214">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="be572-214">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="be572-215">Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un set di flag di normalizzazione non valido.</span><span class="sxs-lookup"><span data-stu-id="be572-215">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="be572-216">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="be572-216">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="be572-217">In Windows 2000, i flag di normalizzazione non validi comporteranno invece JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="be572-217">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-218">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="be572-218">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="be572-219">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="be572-219">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-220">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="be572-220">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="be572-221">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore.</span><span class="sxs-lookup"><span data-stu-id="be572-221">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="be572-222">Le risorse del cursore vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="be572-222">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-223">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="be572-223">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="be572-224">L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="be572-224">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="be572-225"><strong>JetOpenTempTable2</strong> può restituire JET_errOutOfMemory se lo spazio degli indirizzi del processo host diventa troppo frammentato.</span><span class="sxs-lookup"><span data-stu-id="be572-225"><strong>JetOpenTempTable2</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="be572-226">Il gestore tabelle temporanee allocherà sempre un blocco di spazio degli indirizzi pari a 1 MB per ogni tabella temporanea creata indipendentemente dalla quantità di dati da archiviare.</span><span class="sxs-lookup"><span data-stu-id="be572-226">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-227">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="be572-227">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="be572-228">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="be572-228">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-229">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="be572-229">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="be572-230">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="be572-230">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="be572-231">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="be572-231">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-232">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="be572-232">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="be572-233">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="be572-233">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-234">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="be572-234">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="be572-235">È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella.</span><span class="sxs-lookup"><span data-stu-id="be572-235">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="be572-236">Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="be572-236">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-237">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="be572-237">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="be572-238">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella.</span><span class="sxs-lookup"><span data-stu-id="be572-238">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="be572-239">Il numero di indici il cui schema può essere memorizzato nella cache viene configurato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="be572-239">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-240">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="be572-240">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="be572-241">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella.</span><span class="sxs-lookup"><span data-stu-id="be572-241">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="be572-242">Il numero di tabelle il cui schema può essere memorizzato nella cache viene configurato utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="be572-242">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-243">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="be572-243">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="be572-244">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-244">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="be572-245">Le risorse della tabella temporanea vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="be572-245">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be572-246">In seguito all'esito positivo, verrà restituito un cursore aperto nella tabella temporanea appena creata.</span><span class="sxs-lookup"><span data-stu-id="be572-246">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="be572-247">Lo stato del database temporaneo sarà pronto per contenere la nuova tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="be572-247">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="be572-248">Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="be572-248">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="be572-249">In caso di errore, la tabella temporanea non verrà creata e non verrà restituito un cursore.</span><span class="sxs-lookup"><span data-stu-id="be572-249">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="be572-250">Lo stato del database temporaneo può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="be572-250">The state of the temporary database may be changed.</span></span> <span data-ttu-id="be572-251">Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="be572-251">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="be572-252">Commenti</span><span class="sxs-lookup"><span data-stu-id="be572-252">Remarks</span></span>

<span data-ttu-id="be572-253">Vedere [JetOpenTempTable](./jetopentemptable-function.md).</span><span class="sxs-lookup"><span data-stu-id="be572-253">See [JetOpenTempTable](./jetopentemptable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="be572-254">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be572-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be572-255"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="be572-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="be572-256">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="be572-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="be572-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="be572-258">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="be572-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-259"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="be572-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="be572-260">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="be572-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be572-261"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="be572-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="be572-262">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="be572-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be572-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="be572-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="be572-264">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="be572-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="be572-265">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="be572-265">See Also</span></span>

[<span data-ttu-id="be572-266">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="be572-266">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="be572-267">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="be572-267">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="be572-268">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="be572-268">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="be572-269">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="be572-269">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="be572-270">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="be572-270">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="be572-271">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="be572-271">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="be572-272">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="be572-272">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="be572-273">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="be572-273">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="be572-274">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="be572-274">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="be572-275">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="be572-275">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="be572-276">JetMove</span><span class="sxs-lookup"><span data-stu-id="be572-276">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="be572-277">JetRollback</span><span class="sxs-lookup"><span data-stu-id="be572-277">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="be572-278">JetSeek</span><span class="sxs-lookup"><span data-stu-id="be572-278">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="be572-279">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="be572-279">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="be572-280">Parametri di sistema</span><span class="sxs-lookup"><span data-stu-id="be572-280">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
