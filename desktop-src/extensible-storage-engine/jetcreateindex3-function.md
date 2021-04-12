---
description: 'Altre informazioni su: funzione JetCreateIndex3'
title: Funzione JetCreateIndex3
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4f3331a903d4885499ff6c2cd2cad0d8b8534a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346966"
---
# <a name="jetcreateindex3-function"></a><span data-ttu-id="ef50c-103">Funzione JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="ef50c-103">JetCreateIndex3 Function</span></span>


<span data-ttu-id="ef50c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ef50c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex3-function"></a><span data-ttu-id="ef50c-105">Funzione JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="ef50c-105">JetCreateIndex3 Function</span></span>

<span data-ttu-id="ef50c-106">La funzione **JetCreateIndex3** crea indici sui dati in un database ESE, che possono essere utilizzati per individuare rapidamente dati specifici.</span><span class="sxs-lookup"><span data-stu-id="ef50c-106">The **JetCreateIndex3** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="ef50c-107">**Windows 7: JetCreateIndex3** è stato introdotto nel sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ef50c-107">**Windows 7:  JetCreateIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE2* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="ef50c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef50c-108">Parameters</span></span>

<span data-ttu-id="ef50c-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ef50c-109">*sesid*</span></span>

<span data-ttu-id="ef50c-110">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="ef50c-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="ef50c-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="ef50c-111">*tableid*</span></span>

<span data-ttu-id="ef50c-112">Tabella in cui verrà creato l'indice.</span><span class="sxs-lookup"><span data-stu-id="ef50c-112">The table on which the index will be created.</span></span>

<span data-ttu-id="ef50c-113">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="ef50c-113">*pindexcreate*</span></span>

<span data-ttu-id="ef50c-114">Matrice di strutture di [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , ognuna delle quali definisce un indice da creare.</span><span class="sxs-lookup"><span data-stu-id="ef50c-114">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="ef50c-115">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="ef50c-115">*cIndexCreate*</span></span>

<span data-ttu-id="ef50c-116">Numero di elementi nella matrice *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="ef50c-116">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="ef50c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef50c-117">Return Value</span></span>

<span data-ttu-id="ef50c-118">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="ef50c-118">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="ef50c-119">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ef50c-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ef50c-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ef50c-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="ef50c-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef50c-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ef50c-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ef50c-123">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="ef50c-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-124">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="ef50c-124">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="ef50c-125">È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna di aggiornamento del deposito o di una colonna SLV. si noti che le colonne SLV sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="ef50c-125">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-126">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="ef50c-126">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="ef50c-127">È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna non esistente.</span><span class="sxs-lookup"><span data-stu-id="ef50c-127">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="ef50c-128">Il tentativo di eseguire l'indicizzazione condizionale su una colonna inesistente può anche generare questo errore.</span><span class="sxs-lookup"><span data-stu-id="ef50c-128">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-129">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="ef50c-129">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="ef50c-130">Questo errore viene restituito se il membro <strong>ulDensity</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su un numero minore di 20 o maggiore di 100.</span><span class="sxs-lookup"><span data-stu-id="ef50c-130">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-131">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="ef50c-131">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="ef50c-132">È stato eseguito un tentativo di definire due indici identici.</span><span class="sxs-lookup"><span data-stu-id="ef50c-132">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-133">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="ef50c-133">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="ef50c-134">È stato effettuato un tentativo di specificare più di un indice primario per una tabella.</span><span class="sxs-lookup"><span data-stu-id="ef50c-134">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="ef50c-135">Una tabella deve avere esattamente un indice primario.</span><span class="sxs-lookup"><span data-stu-id="ef50c-135">A table must have exactly one primary index.</span></span> <span data-ttu-id="ef50c-136">Se non viene specificato alcun indice primario, il motore di database ne creerà uno in modo trasparente.</span><span class="sxs-lookup"><span data-stu-id="ef50c-136">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-137">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="ef50c-137">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="ef50c-138">È stata specificata una definizione di indice non valida.</span><span class="sxs-lookup"><span data-stu-id="ef50c-138">An invalid index definition was specified.</span></span> <span data-ttu-id="ef50c-139">Di seguito sono riportate alcune possibili cause per la ricezione di questo errore:</span><span class="sxs-lookup"><span data-stu-id="ef50c-139">The following are some possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef50c-140">Un indice primario è condizionale (il membro<strong>grbit</strong> del <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha JET_bitIndexPrimary set e il membro <strong>cConditionalColumn</strong> di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è maggiore di zero).</span><span class="sxs-lookup"><span data-stu-id="ef50c-140">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="ef50c-141">Windows Server 2003 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef50c-141">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="ef50c-142">Tentativo di creare un indice di tupla con limiti di tupla, ma senza passare informazioni nel membro <strong>ptuplelimits</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> , ovvero <em>grbit</em> ha impostato JET_bitIndexTupleLimits, ma il puntatore <strong>ptuplelimits</strong> è null.</span><span class="sxs-lookup"><span data-stu-id="ef50c-142">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="ef50c-143">Passaggio di una definizione di chiave non valida nel membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="ef50c-143">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="ef50c-144">Per una descrizione delle definizioni valide, vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="ef50c-144">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="ef50c-145">L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> su un valore maggiore di JET_cbPrimaryKeyMost (per un indice primario) o maggiore di JET_cbSecondaryKeyMost (per un indice secondario).</span><span class="sxs-lookup"><span data-stu-id="ef50c-145">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="ef50c-146">Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit JET_bitIndexUnicode impostato nel membro <strong>grbit</strong> di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="ef50c-146">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="ef50c-147">Alcune cause comuni possono essere che il campo pidxunicode della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è null o che l'identificatore LCID specificato nella struttura pidxunicode non è valido.</span><span class="sxs-lookup"><span data-stu-id="ef50c-147">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="ef50c-148">Specifica di una colonna multivalore per un indice primario.</span><span class="sxs-lookup"><span data-stu-id="ef50c-148">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="ef50c-149">Tentativo di indicizzare un numero eccessivo di colonne condizionali.</span><span class="sxs-lookup"><span data-stu-id="ef50c-149">Trying to index too many conditional columns.</span></span> <span data-ttu-id="ef50c-150">Il membro <strong>cConditionalColumn</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve essere maggiore di JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="ef50c-150">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-151">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="ef50c-151">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="ef50c-152">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef50c-152">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ef50c-153">È stata specificata una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> e i relativi limiti non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="ef50c-153">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="ef50c-154">Vedere la sezione Osservazioni della struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="ef50c-154">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-155">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="ef50c-155">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="ef50c-156">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef50c-156">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ef50c-157">Un indice di tupla non può essere univoco (<em>grbit</em> non deve avere sia JET_bitIndexTuples che JET_bitIndexUnique impostato).</span><span class="sxs-lookup"><span data-stu-id="ef50c-157">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-158">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="ef50c-158">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="ef50c-159">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef50c-159">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ef50c-160">Un indice di tupla può trovarsi solo su una singola colonna, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> dispone di JET_bitIndexTuples set e il membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> specifica più di una colonna.</span><span class="sxs-lookup"><span data-stu-id="ef50c-160">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-161">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="ef50c-161">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="ef50c-162">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef50c-162">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ef50c-163">Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexTuples impostato).</span><span class="sxs-lookup"><span data-stu-id="ef50c-163">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-164">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="ef50c-164">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="ef50c-165">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef50c-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ef50c-166">Un indice tupla può trovarsi solo in una colonna di tipo text o Unicode.</span><span class="sxs-lookup"><span data-stu-id="ef50c-166">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="ef50c-167">Il tentativo di indicizzare altre colonne, ad esempio colonne binarie, comporterà la JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="ef50c-167">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-168">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="ef50c-168">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="ef50c-169">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="ef50c-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ef50c-170">Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="ef50c-170">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-171">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="ef50c-171">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="ef50c-172">È stato effettuato un tentativo di creare un indice senza informazioni sulla versione in una transazione.</span><span class="sxs-lookup"><span data-stu-id="ef50c-172">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-173">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="ef50c-173">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="ef50c-174">La definizione dell'indice non è valida perché il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene valori incoerenti.</span><span class="sxs-lookup"><span data-stu-id="ef50c-174">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="ef50c-175">Di seguito sono riportati alcuni dei possibili motivi:</span><span class="sxs-lookup"><span data-stu-id="ef50c-175">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef50c-176">Per un indice primario è stato specificato un bit ignoto (JET_bitIndexPrimary è stato passato con una delle JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="ef50c-176">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="ef50c-177">Un indice vuoto non ignora alcun campo NULL, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha JET_bitIndexEmpty set, ma non ha JET_bitIndexIgnoreAnyNull set.</span><span class="sxs-lookup"><span data-stu-id="ef50c-177">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="ef50c-178">Passaggio di una struttura di <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit</strong> non valido.</span><span class="sxs-lookup"><span data-stu-id="ef50c-178">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="ef50c-179">Vedere <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="ef50c-179">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="ef50c-180">Quando si creano più indici contemporaneamente (ovvero se il parametro <em>cIndexCreate</em> è maggiore di uno), nessuno degli indici può contenere uno dei bit seguenti:</span><span class="sxs-lookup"><span data-stu-id="ef50c-180">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef50c-181">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="ef50c-181">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="ef50c-182">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="ef50c-182">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="ef50c-183">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="ef50c-183">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-184">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="ef50c-184">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="ef50c-185">È stato passato un ID delle impostazioni locali (LCID) non valido (tramite il membro <strong>LCID</strong> della struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , che il membro <strong>pidxunicode</strong> nella struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene un puntatore a oppure tramite il membro <strong>LCID</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="ef50c-185">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-186">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="ef50c-186">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="ef50c-187">È stato specificato un nome di indice non valido.</span><span class="sxs-lookup"><span data-stu-id="ef50c-187">An invalid index name was specified.</span></span> <span data-ttu-id="ef50c-188">Per ulteriori informazioni, vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="ef50c-188">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-189">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ef50c-189">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ef50c-190">Un parametro non valido è stato passato nell'API.</span><span class="sxs-lookup"><span data-stu-id="ef50c-190">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="ef50c-191">Di seguito sono riportati alcuni dei motivi per cui può essere restituito questo errore:</span><span class="sxs-lookup"><span data-stu-id="ef50c-191">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="ef50c-192">Il campo <strong>cbKey</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="ef50c-192">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="ef50c-193">Il membro <strong>cbStruct</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è impostato su sizeof ( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="ef50c-193">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-194">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="ef50c-194">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="ef50c-195">Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode.</span><span class="sxs-lookup"><span data-stu-id="ef50c-195">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="ef50c-196">Questo problema può essere causato dall'esaurimento delle risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="ef50c-196">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-197">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="ef50c-197">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="ef50c-198">Un elemento della struttura degli hint di spazio JET non è corretto o non è attivabile.</span><span class="sxs-lookup"><span data-stu-id="ef50c-198">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ef50c-199">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef50c-199">Remarks</span></span>

<span data-ttu-id="ef50c-200">Il valore restituito viene JET_errSuccess al completamento di tutti gli indici specificati.</span><span class="sxs-lookup"><span data-stu-id="ef50c-200">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="ef50c-201">**JetCreateIndex3** scorre gli indici specificati in **pindexcreate** e talvolta viene interrotto al primo errore.</span><span class="sxs-lookup"><span data-stu-id="ef50c-201">**JetCreateIndex3** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="ef50c-202">Eventuali indici dopo il primo indice con un errore potrebbero non essere stati tentati, anche se il membro **Err** della struttura [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contiene JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="ef50c-202">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ef50c-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef50c-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-204"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ef50c-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ef50c-205">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ef50c-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ef50c-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ef50c-207">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ef50c-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-208"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ef50c-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ef50c-209">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ef50c-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-210"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="ef50c-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ef50c-211">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ef50c-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ef50c-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ef50c-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ef50c-213">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ef50c-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef50c-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ef50c-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ef50c-215">Implementato come <strong>JetCreateIndex3W</strong> (Unicode) e <strong>JetCreateIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ef50c-215">Implemented as <strong>JetCreateIndex3W</strong> (Unicode) and <strong>JetCreateIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ef50c-216">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ef50c-216">See Also</span></span>

[<span data-ttu-id="ef50c-217">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="ef50c-217">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="ef50c-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ef50c-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ef50c-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ef50c-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ef50c-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ef50c-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ef50c-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ef50c-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ef50c-222">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="ef50c-222">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="ef50c-223">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="ef50c-223">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="ef50c-224">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="ef50c-224">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="ef50c-225">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="ef50c-225">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="ef50c-226">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="ef50c-226">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
