---
description: 'Altre informazioni su: struttura JET_OPENTEMPORARYTABLE'
title: Struttura JET_OPENTEMPORARYTABLE
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345856"
---
# <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="2ca9d-103">Struttura JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="2ca9d-103">JET_OPENTEMPORARYTABLE Structure</span></span>


<span data-ttu-id="2ca9d-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2ca9d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="2ca9d-105">Struttura JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="2ca9d-105">JET_OPENTEMPORARYTABLE Structure</span></span>

<span data-ttu-id="2ca9d-106">La struttura **JET_OPENTEMPORARYTABLE** contiene una raccolta di parametri facilmente estendibile per la funzione di **JET_OPENTEMPORARYTABLE** .</span><span class="sxs-lookup"><span data-stu-id="2ca9d-106">The **JET_OPENTEMPORARYTABLE** structure contains an easily extensible collection of parameters for the **JET_OPENTEMPORARYTABLE** function.</span></span> <span data-ttu-id="2ca9d-107">Questa struttura è la tabella temporanea equivalente della struttura [JET_TABLECREATE](./jet-tablecreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="2ca9d-107">This structure is the temporary table equivalent of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure.</span></span>

<span data-ttu-id="2ca9d-108">**Windows Vista:** La struttura **JET_OPENTEMPORARYTABLE** è stata introdotta in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-108">**Windows Vista:** The **JET_OPENTEMPORARYTABLE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a><span data-ttu-id="2ca9d-109">Membri</span><span class="sxs-lookup"><span data-stu-id="2ca9d-109">Members</span></span>

<span data-ttu-id="2ca9d-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-110">**cbStruct**</span></span>

<span data-ttu-id="2ca9d-111">Dimensioni in byte della struttura (per l'espansione futura).</span><span class="sxs-lookup"><span data-stu-id="2ca9d-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="2ca9d-112">Deve essere impostato su sizeof (JET_TABLECREATE) in byte.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-112">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="2ca9d-113">**prgcolumndef**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-113">**prgcolumndef**</span></span>

<span data-ttu-id="2ca9d-114">Definizioni di colonna per le colonne create nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="2ca9d-115">Sono presenti **importanti** limitazioni per le opzioni di definizione di colonna utilizzate con una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-115">**Important** limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="2ca9d-116">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="2ca9d-117">Oltre alle normali opzioni di definizione di colonna, è possibile specificare anche zero o più delle opzioni seguenti che sono rilevanti solo nel contesto di una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ca9d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2ca9d-118">Value</span></span></p></th>
<th><p><span data-ttu-id="2ca9d-119">Significato</span><span class="sxs-lookup"><span data-stu-id="2ca9d-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ca9d-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="2ca9d-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="2ca9d-121">Il tipo di ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="2ca9d-122">Se questa opzione viene specificata senza JET_bitColumnTTKey, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca9d-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="2ca9d-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="2ca9d-124">La colonna sarà una colonna chiave per la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="2ca9d-125">L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="2ca9d-126">La prima definizione di colonna nella matrice con questo set di opzioni sarà la colonna chiave più significativa e così via.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="2ca9d-127">Se sono richieste più colonne chiave che possono essere supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ca9d-128">**CColumn**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-128">**ccolumn**</span></span>

<span data-ttu-id="2ca9d-129">Vedere *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="2ca9d-130">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-130">**pidxunicode**</span></span>

<span data-ttu-id="2ca9d-131">ID delle impostazioni locali e flag di normalizzazione da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-131">The locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="2ca9d-132">Quando questo parametro non è presente e quando il parametro *LCID* non è presente, viene utilizzato il valore LCID predefinito per confrontare eventuali colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-132">When this parameter is not present and when the *lcid* parameter is not present, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="2ca9d-133">Il valore LCID predefinito corrisponde alle impostazioni locali per l'inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="2ca9d-133">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="2ca9d-134">Quando questo parametro non è presente, i flag di normalizzazione predefiniti verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-134">When this parameter is not present, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="2ca9d-135">I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-135">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="2ca9d-136">**grbit**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-136">**grbit**</span></span>

<span data-ttu-id="2ca9d-137">Gruppo di bit che specifica zero o più delle opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-137">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ca9d-138">Valore</span><span class="sxs-lookup"><span data-stu-id="2ca9d-138">Value</span></span></p></th>
<th><p><span data-ttu-id="2ca9d-139">Significato</span><span class="sxs-lookup"><span data-stu-id="2ca9d-139">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ca9d-140">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="2ca9d-140">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="2ca9d-141">Questa opzione richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'uso di <a href="gg294103(v=exchg.10).md">JetSeek</a> per la ricerca di record in base alla chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-141">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="2ca9d-142">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="2ca9d-143">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca9d-144">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="2ca9d-144">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="2ca9d-145">Richiede la rimozione dei record con chiavi di indice duplicate dal set di record finale nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-145">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="2ca9d-146">Prima di Windows Server 2003, il motore di database presuppone sempre che questa opzione sia attiva a causa del fatto che anche tutti gli indici cluster devono essere una chiave primaria e pertanto devono essere univoci.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-146">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="2ca9d-147">A partire da Windows Server 2003, è ora possibile creare una tabella temporanea che non rimuove i duplicati quando viene specificata anche l'opzione JET_bitTTForwardOnly.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-147">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="2ca9d-148">Non è possibile stabilire quale duplicato avrà esito positivo e quali duplicati verranno rimossi, in generale.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-148">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="2ca9d-149">Tuttavia, quando viene richiesta l'opzione JET_bitTTErrorOnDuplicateInsertion, il primo record con una chiave di indice specificata da inserire nella tabella temporanea avrà sempre esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-149">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ca9d-150">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="2ca9d-150">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="2ca9d-151">Richiede che la tabella temporanea sia sufficientemente flessibile da consentire la modifica successiva dei record inseriti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-151">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="2ca9d-152">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-152">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="2ca9d-153">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-153">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca9d-154">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="2ca9d-154">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="2ca9d-155">Richiede che la tabella temporanea sia sufficientemente flessibile da consentire l'analisi arbitraria dei record in ordine e direzione arbitrari usando <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-155">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="2ca9d-156">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-156">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="2ca9d-157">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-157">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ca9d-158">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="2ca9d-158">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="2ca9d-159">Richiede che i valori della colonna chiave <strong>null</strong> siano ordinati più vicino alla fine dell'indice rispetto ai valori di colonna chiave non null.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-159">Requests that <strong>NULL</strong> key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca9d-160">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="2ca9d-160">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="2ca9d-161">Impone al gestore tabelle temporaneo di abbandonare la ricerca della strategia migliore per utilizzare la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-161">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ca9d-162">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="2ca9d-162">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="2ca9d-163">Eventuali tentativi di inserire un record con la stessa chiave di indice di un record inserito in precedenza avranno immediatamente esito negativo con JET_errKeyDuplicate.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-163">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="2ca9d-164">Se questa opzione non è richiesta, un duplicato viene rilevato immediatamente e non riesce o viene rimosso automaticamente in un secondo momento, a seconda della strategia scelta dal motore di database per implementare la tabella temporanea, in base alla funzionalità richiesta.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-164">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="2ca9d-165">Se questa funzionalità non è necessaria, è consigliabile non richiederla.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-165">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="2ca9d-166">Se questa funzionalità non è richiesta, il gestore tabelle temporaneo potrebbe essere in grado di scegliere una strategia per la gestione della tabella temporanea che comporterà un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-166">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca9d-167">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="2ca9d-167">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="2ca9d-168">La tabella temporanea viene creata solo se Gestione tabelle temporanee è in grado di utilizzare l'implementazione ottimizzata per i risultati intermedi delle query.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-168">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="2ca9d-169">Se una caratteristica della tabella temporanea impedisce l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-169">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="2ca9d-170">Un effetto collaterale di questa opzione consiste nel consentire alla tabella temporanea di contenere record con chiavi di indice duplicate.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-170">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="2ca9d-171">Per ulteriori informazioni, vedere JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-171">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="2ca9d-172"><strong>Windows Server 2003:  </strong> Questa opzione è disponibile solo in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-172"><strong>Windows Server 2003:  </strong>This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ca9d-173">**prgcolumnid**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-173">**prgcolumnid**</span></span>

<span data-ttu-id="2ca9d-174">Buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-174">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="2ca9d-175">Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-175">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="2ca9d-176">Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione della matrice di input.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-176">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

<span data-ttu-id="2ca9d-177">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-177">**cbKeyMost**</span></span>

<span data-ttu-id="2ca9d-178">Dimensione massima di una chiave che rappresenta una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-178">The maximum size for a key representing a given row.</span></span>

<span data-ttu-id="2ca9d-179">È possibile impostare la dimensione massima della chiave per controllare la modalità di troncamento delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-179">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="2ca9d-180">Il troncamento della chiave è importante perché può influire sul fatto che le righe siano considerate distinte.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-180">Key truncation is important because it can affect when rows are considered to be distinct.</span></span>

<span data-ttu-id="2ca9d-181">Se questo parametro è impostato su 0 o JET_cbKeyMostMin (255), le dimensioni massime della chiave e la relativa semantica rimarranno identiche alle dimensioni massime della chiave supportate da Windows Server 2003 e dalle versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-181">If this parameter is set to 0 or JET_cbKeyMostMin (255) then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003 and previous releases.</span></span> <span data-ttu-id="2ca9d-182">Questo parametro può essere impostato anche su un valore maggiore come funzione delle dimensioni della pagina del database per l'istanza (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="2ca9d-182">This parameter may also be set to a larger value as a function of the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="2ca9d-183">Per ulteriori informazioni, vedere JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-183">See JET_paramKeyMost for more information.</span></span>

<span data-ttu-id="2ca9d-184">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-184">**cbVarSegMac**</span></span>

<span data-ttu-id="2ca9d-185">Quantità massima di dati che verranno utilizzati da qualsiasi colonna a lunghezza variabile per costruire una chiave per una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-185">The maximum amount of data that will be used from any variable length column to construct a key for a given row.</span></span>

<span data-ttu-id="2ca9d-186">Questo parametro può essere utilizzato per controllare la quantità di spazio chiave utilizzata da una determinata colonna chiave.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-186">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="2ca9d-187">Questo limite è in byte.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-187">This limit is in bytes.</span></span> <span data-ttu-id="2ca9d-188">Se questo parametro è zero o è uguale al parametro *cbKeyMost* , non è attivo alcun limite.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-188">If this parameter is zero or is the same as the *cbKeyMost* parameter then no limit is in effect.</span></span>

<span data-ttu-id="2ca9d-189">**TableID**</span><span class="sxs-lookup"><span data-stu-id="2ca9d-189">**tableid**</span></span>

<span data-ttu-id="2ca9d-190">Handle di tabella per la tabella temporanea creata in seguito a una chiamata riuscita a [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="2ca9d-190">The table handle for the temporary table created as a result of a successful call to [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="2ca9d-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ca9d-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ca9d-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2ca9d-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2ca9d-193">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-193">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ca9d-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2ca9d-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2ca9d-195">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-195">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ca9d-196"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="2ca9d-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2ca9d-197">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="2ca9d-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2ca9d-198">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2ca9d-198">See Also</span></span>

[<span data-ttu-id="2ca9d-199">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="2ca9d-199">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="2ca9d-200">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="2ca9d-200">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="2ca9d-201">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="2ca9d-201">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="2ca9d-202">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2ca9d-202">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2ca9d-203">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="2ca9d-203">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="2ca9d-204">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2ca9d-204">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2ca9d-205">JetOpenTemporaryTable</span><span class="sxs-lookup"><span data-stu-id="2ca9d-205">JetOpenTemporaryTable</span></span>](./jetopentemporarytable-function.md)  
[<span data-ttu-id="2ca9d-206">Parametri di sistema Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="2ca9d-206">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
