---
description: 'Altre informazioni su: funzione JetCreateTableColumnIndex3'
title: JetCreateTableColumnIndex3 (funzione)
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1d6aed3178f5593826097f8c5d6b01bd8c72d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319182"
---
# <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="29980-103">JetCreateTableColumnIndex3 (funzione)</span><span class="sxs-lookup"><span data-stu-id="29980-103">JetCreateTableColumnIndex3 Function</span></span>


<span data-ttu-id="29980-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="29980-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="29980-105">JetCreateTableColumnIndex3 (funzione)</span><span class="sxs-lookup"><span data-stu-id="29980-105">JetCreateTableColumnIndex3 Function</span></span>

<span data-ttu-id="29980-106">La funzione **JetCreateTableColumnIndex3** crea una tabella in un database ESE con un set iniziale di indici e un set iniziale di colonne da una matrice di strutture di [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="29980-106">The **JetCreateTableColumnIndex3** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="29980-107">La struttura di [JET_TABLECREATE3](./jet-tablecreate3-structure.md) consente di specificare una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="29980-107">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="29980-108">**Windows 7:** **JetCreateTableColumnIndex3** è stato introdotto nel sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="29980-108">**Windows 7:** **JetCreateTableColumnIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE3* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="29980-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="29980-109">Parameters</span></span>

<span data-ttu-id="29980-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="29980-110">*sesid*</span></span>

<span data-ttu-id="29980-111">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="29980-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="29980-112">*dbid*</span><span class="sxs-lookup"><span data-stu-id="29980-112">*dbid*</span></span>

<span data-ttu-id="29980-113">Identificatore del database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="29980-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="29980-114">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="29980-114">*ptablecreate*</span></span>

<span data-ttu-id="29980-115">Puntatore a una struttura [JET_TABLECREATE3](./jet-tablecreate3-structure.md) che definisce la tabella da creare.</span><span class="sxs-lookup"><span data-stu-id="29980-115">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="29980-116">Per ulteriori informazioni, vedere [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="29980-116">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="29980-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29980-117">Return Value</span></span>

<span data-ttu-id="29980-118">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="29980-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="29980-119">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="29980-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29980-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="29980-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="29980-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29980-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29980-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="29980-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="29980-123">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="29980-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="29980-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="29980-125">Non è stato possibile risolvere la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="29980-125">The callback function could not be resolved.</span></span> <span data-ttu-id="29980-126">È possibile che la DLL non sia stata trovata o che la funzione nella DLL non sia stata trovata.</span><span class="sxs-lookup"><span data-stu-id="29980-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="29980-127">Con la registrazione sufficiente abilitata, nel registro eventi vengono forniti ulteriori dettagli.</span><span class="sxs-lookup"><span data-stu-id="29980-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="29980-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="29980-129">È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna di aggiornamento del deposito o di una colonna SLV. si noti che le colonne SLV sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="29980-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="29980-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="29980-131">Se ptablecreate- &gt; grbit specifica JET_bitTableCreateTemplateTable, ma ptablecreate- &gt; szTemplateTableName è impostato su null.</span><span class="sxs-lookup"><span data-stu-id="29980-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="29980-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="29980-133">Una colonna esiste già.</span><span class="sxs-lookup"><span data-stu-id="29980-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="29980-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="29980-135">È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna non esistente.</span><span class="sxs-lookup"><span data-stu-id="29980-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="29980-136">Il tentativo di eseguire l'indicizzazione condizionale su una colonna inesistente può anche generare questo errore.</span><span class="sxs-lookup"><span data-stu-id="29980-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="29980-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="29980-138">È stato effettuato un tentativo di aggiungere una colonna ridondante.</span><span class="sxs-lookup"><span data-stu-id="29980-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="29980-139">Non deve essere presente più di una colonna AutoIncrement e non più di una colonna versione per tabella.</span><span class="sxs-lookup"><span data-stu-id="29980-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="29980-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="29980-141">Questo errore viene restituito se il membro <strong>ulDensity</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su un numero minore di 20 o maggiore di 100.</span><span class="sxs-lookup"><span data-stu-id="29980-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="29980-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="29980-143">Indica che la tabella denominata nel membro <strong>szTemplateTableName</strong> della struttura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> non è stata contrassegnata come tabella modello (ovvero la tabella non dispone di JET_bitTableCreateTemplateTable impostato).</span><span class="sxs-lookup"><span data-stu-id="29980-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="29980-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="29980-145">È stato eseguito un tentativo di definire due indici identici.</span><span class="sxs-lookup"><span data-stu-id="29980-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="29980-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="29980-147">È stato effettuato un tentativo di specificare più di un indice primario per una tabella.</span><span class="sxs-lookup"><span data-stu-id="29980-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="29980-148">Una tabella deve avere esattamente un indice primario.</span><span class="sxs-lookup"><span data-stu-id="29980-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="29980-149">Se non viene specificato alcun indice primario, il motore di database ne creerà uno in modo trasparente.</span><span class="sxs-lookup"><span data-stu-id="29980-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="29980-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="29980-151">È stata specificata una definizione di indice non valida.</span><span class="sxs-lookup"><span data-stu-id="29980-151">An invalid index definition was specified.</span></span> <span data-ttu-id="29980-152">Di seguito sono riportati alcuni dei possibili motivi per la ricezione di questo errore:</span><span class="sxs-lookup"><span data-stu-id="29980-152">The following are some of the possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="29980-153">Un indice primario è condizionale (ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha JET_bitIndexPrimary set e il membro <strong>cConditionalColumn</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è maggiore di zero).</span><span class="sxs-lookup"><span data-stu-id="29980-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="29980-154">Windows Server 2003 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="29980-154">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="29980-155">Il tentativo di creare un indice di tupla con limiti di tupla, ma senza passare il membro <strong>ptuplelimits</strong> nella struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ovvero il membro <strong>grbit</strong> della struttura JET_INDEXCREATE2 ha JET_bitIndexTupleLimits set, ma il puntatore <strong>ptuplelimits</strong> è null).</span><span class="sxs-lookup"><span data-stu-id="29980-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the JET_INDEXCREATE2 structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="29980-156">Passaggio di una definizione di chiave non valida nel membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="29980-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="29980-157">Per una descrizione delle definizioni valide, vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="29980-157">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="29980-158">L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> su un valore maggiore di JET_cbPrimaryKeyMost (per un indice primario) o maggiore di JET_cbSecondaryKeyMost (per un indice secondario).</span><span class="sxs-lookup"><span data-stu-id="29980-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="29980-159">Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit JET_bitIndexUnicode impostato nel membro <strong>grbit</strong> di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="29980-159">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="29980-160">Alcune cause comuni includono il membro <strong>pidxunicode</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è null o l'LCID specificato nella struttura <strong>pidxunicode</strong> non è valido.</span><span class="sxs-lookup"><span data-stu-id="29980-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="29980-161">Specifica di una colonna multivalore per un indice primario.</span><span class="sxs-lookup"><span data-stu-id="29980-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="29980-162">Tentativo di indicizzare un numero eccessivo di colonne condizionali.</span><span class="sxs-lookup"><span data-stu-id="29980-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="29980-163">Il membro <strong>cConditionalColumn</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve essere maggiore di JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="29980-163">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="29980-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="29980-165">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="29980-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="29980-166">È stata specificata una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> e i relativi limiti non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="29980-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="29980-167">Vedere la sezione Osservazioni della struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="29980-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="29980-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="29980-169">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="29980-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="29980-170">Un indice di tupla non può essere univoco, ovvero il membro <em>grbit</em> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexUnique impostato).</span><span class="sxs-lookup"><span data-stu-id="29980-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="29980-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="29980-172">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="29980-172">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="29980-173">Un indice della tupla può trovarsi solo su una singola colonna, ovvero se il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> dispone di JET_bitIndexTuples set e il membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> specifica più di una colonna.</span><span class="sxs-lookup"><span data-stu-id="29980-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="29980-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="29980-175">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="29980-175">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="29980-176">Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexTuples impostato).</span><span class="sxs-lookup"><span data-stu-id="29980-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="29980-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="29980-178">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="29980-178">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="29980-179">Un indice tupla può trovarsi solo in una colonna di tipo text o Unicode.</span><span class="sxs-lookup"><span data-stu-id="29980-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="29980-180">Il tentativo di indicizzare altre colonne, ad esempio colonne binarie, comporterà la JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="29980-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="29980-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="29980-182">Windows XP e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="29980-182">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="29980-183">Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="29980-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="29980-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="29980-185">È stato effettuato un tentativo di creare un indice senza informazioni sulla versione in una transazione.</span><span class="sxs-lookup"><span data-stu-id="29980-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="29980-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="29980-187">Il membro <strong>CP</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> non è stato impostato su una tabella codici valida.</span><span class="sxs-lookup"><span data-stu-id="29980-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="29980-188">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="29980-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="29980-189">Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="29980-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="29980-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="29980-191">Il membro <strong>coltyp</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> non è stato impostato su un tipo di colonna valido.</span><span class="sxs-lookup"><span data-stu-id="29980-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="29980-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="29980-193">Di seguito sono riportati alcuni dei motivi per cui è possibile che si verifichi questo errore:</span><span class="sxs-lookup"><span data-stu-id="29980-193">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="29980-194">Il membro <strong>rgindexcreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su null.</span><span class="sxs-lookup"><span data-stu-id="29980-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="29980-195">Il membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su null.</span><span class="sxs-lookup"><span data-stu-id="29980-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="29980-196">Il membro <strong>cbStruct</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è stato impostato su un valore valido.</span><span class="sxs-lookup"><span data-stu-id="29980-196">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="29980-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="29980-198">In <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>è stata specificata una combinazione non valida di membri <strong>grbit</strong> .</span><span class="sxs-lookup"><span data-stu-id="29980-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</span></span></p>
<p><span data-ttu-id="29980-199">La definizione dell'indice non è valida perché il membro <strong>grbit</strong> contiene valori incoerenti.</span><span class="sxs-lookup"><span data-stu-id="29980-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="29980-200">Di seguito sono riportati alcuni dei possibili motivi:</span><span class="sxs-lookup"><span data-stu-id="29980-200">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="29980-201">Per un indice primario è stato specificato un bit Ignore (ovvero, JET_bitIndexPrimary è stato passato con JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="29980-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="29980-202">Un indice vuoto non ignora i membri NULL, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha JET_bitIndexEmpty impostato, ma non ha JET_bitIndexIgnoreAnyNull set.</span><span class="sxs-lookup"><span data-stu-id="29980-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="29980-203">Passaggio di una struttura di <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit</strong> non valido.</span><span class="sxs-lookup"><span data-stu-id="29980-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="29980-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="29980-205">È stato passato un ID delle impostazioni locali (LCID) non valido (tramite il membro <strong>LCID</strong> della struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a cui fa riferimento il membro <strong>pidxunicode</strong> nella struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> o tramite il campo <strong>LCID</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="29980-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="29980-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="29980-207">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="29980-207">An invalid parameter was given.</span></span> <span data-ttu-id="29980-208">Di seguito sono riportati alcuni dei possibili motivi:</span><span class="sxs-lookup"><span data-stu-id="29980-208">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="29980-209">Il membro <strong>rgcolumncreate</strong> della struttura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> è null.</span><span class="sxs-lookup"><span data-stu-id="29980-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="29980-210">Il membro <strong>cbStruct</strong> di una delle strutture <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> fornite nel membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> non è stato impostato su sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="29980-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="29980-211">Il membro <strong>cbKey</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="29980-211">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="29980-212">Il membro <strong>cbStruct</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è impostato su sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="29980-212">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="29980-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="29980-214">Il record è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="29980-214">The record is too big.</span></span> <span data-ttu-id="29980-215">La somma del membro <strong>cbMax</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> per tutte le colonne fisse non deve superare un determinato valore.</span><span class="sxs-lookup"><span data-stu-id="29980-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="29980-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="29980-217">La tabella esiste già.</span><span class="sxs-lookup"><span data-stu-id="29980-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="29980-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="29980-219">È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella.</span><span class="sxs-lookup"><span data-stu-id="29980-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="29980-220">Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="29980-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="29980-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="29980-222">Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode.</span><span class="sxs-lookup"><span data-stu-id="29980-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="29980-223">Questo problema può essere causato dall'esaurimento delle risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="29980-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-224">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="29980-224">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="29980-225">Un elemento della struttura degli hint di spazio JET non è corretto o non è attivabile.</span><span class="sxs-lookup"><span data-stu-id="29980-225">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="29980-226">Commenti</span><span class="sxs-lookup"><span data-stu-id="29980-226">Remarks</span></span>

<span data-ttu-id="29980-227">Il nome **JetCreateTableColumnIndex3** deriva dall'ordine di creazione degli oggetti: prima crea una tabella, le colonne e infine gli indici.</span><span class="sxs-lookup"><span data-stu-id="29980-227">The name **JetCreateTableColumnIndex3** comes from the order of creation of the objects: It first creates a table, columns, and then finally indexes.</span></span> <span data-ttu-id="29980-228">**JetCreateTableColumnIndex3** crea una tabella con un set iniziale di colonne e indici.</span><span class="sxs-lookup"><span data-stu-id="29980-228">**JetCreateTableColumnIndex3** creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="29980-229">Altre colonne e indici possono essere aggiunti e rimossi dinamicamente con [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md)e [JetDeleteIndex](./jetdeleteindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="29980-229">Additional columns and indexes can be added and removed dynamically with [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md).</span></span>

<span data-ttu-id="29980-230">Come [JetOpenTable](./jetopentable-function.md), quando l'applicazione viene eseguita utilizzando il *TableID* restituito, in genere deve essere chiuso con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="29980-230">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="29980-231">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29980-231">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29980-232"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="29980-232"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="29980-233">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29980-233">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-234"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="29980-234"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="29980-235">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="29980-235">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-236"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="29980-236"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="29980-237">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="29980-237">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-238"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="29980-238"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="29980-239">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="29980-239">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29980-240"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="29980-240"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="29980-241">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="29980-241">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29980-242"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="29980-242"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="29980-243">Implementato come <strong>JetCreateTableColumnIndex3W</strong> (Unicode) e <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="29980-243">Implemented as <strong>JetCreateTableColumnIndex3W</strong> (Unicode) and <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="29980-244">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="29980-244">See Also</span></span>

[<span data-ttu-id="29980-245">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="29980-245">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="29980-246">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="29980-246">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="29980-247">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="29980-247">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="29980-248">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="29980-248">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="29980-249">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="29980-249">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="29980-250">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="29980-250">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="29980-251">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="29980-251">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="29980-252">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="29980-252">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="29980-253">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="29980-253">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="29980-254">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="29980-254">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="29980-255">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="29980-255">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="29980-256">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="29980-256">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="29980-257">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="29980-257">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="29980-258">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="29980-258">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="29980-259">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="29980-259">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="29980-260">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="29980-260">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="29980-261">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="29980-261">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="29980-262">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="29980-262">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="29980-263">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="29980-263">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
