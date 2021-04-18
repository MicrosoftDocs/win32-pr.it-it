---
description: 'Altre informazioni su: funzione JetCreateTableColumnIndex4W'
title: JetCreateTableColumnIndex4W (funzione)
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319181"
---
# <a name="jetcreatetablecolumnindex4w-function"></a><span data-ttu-id="88686-103">JetCreateTableColumnIndex4W (funzione)</span><span class="sxs-lookup"><span data-stu-id="88686-103">JetCreateTableColumnIndex4W Function</span></span>


<span data-ttu-id="88686-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="88686-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="88686-105">La funzione **JetCreateTableColumnIndex4W** crea una tabella in un motore di archiviazione estensibile (ESE, database con un set iniziale di indici e un set iniziale di colonne da una matrice di strutture di [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="88686-105">The **JetCreateTableColumnIndex4W** function creates a table in an Extensible Storage Engine (ESE( database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="88686-106">La struttura di [JET_TABLECREATE3](./jet-tablecreate3-structure.md) consente di specificare una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="88686-106">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="88686-107">La funzione **JetCreateTableColumnIndex4W** è stata introdotta nel sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="88686-107">The **JetCreateTableColumnIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a><span data-ttu-id="88686-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="88686-108">Parameters</span></span>

<span data-ttu-id="88686-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="88686-109">*sesid*</span></span>

<span data-ttu-id="88686-110">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="88686-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="88686-111">*dbid*</span><span class="sxs-lookup"><span data-stu-id="88686-111">*dbid*</span></span>

<span data-ttu-id="88686-112">Identificatore del database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="88686-112">The database identifier to use for the API call.</span></span>

<span data-ttu-id="88686-113">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="88686-113">*ptablecreate*</span></span>

<span data-ttu-id="88686-114">Puntatore a una struttura [JET_TABLECREATE3](./jet-tablecreate3-structure.md) che definisce la tabella da creare.</span><span class="sxs-lookup"><span data-stu-id="88686-114">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="88686-115">Per ulteriori informazioni, vedere [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="88686-115">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="88686-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88686-116">Return value</span></span>

<span data-ttu-id="88686-117">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="88686-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="88686-118">Per ulteriori informazioni sui possibili errori di Extensible Storage enginge (ESE), vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="88686-118">For more information about the possible Extensible Storage Enginge (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88686-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="88686-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="88686-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88686-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88686-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="88686-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="88686-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="88686-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-123">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="88686-123">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="88686-124">Non è stato possibile risolvere la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="88686-124">The callback function could not be resolved.</span></span> <span data-ttu-id="88686-125">È possibile che la DLL non sia stata trovata o che la funzione nella DLL non sia stata trovata.</span><span class="sxs-lookup"><span data-stu-id="88686-125">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="88686-126">Con la registrazione sufficiente abilitata, nel registro eventi vengono forniti ulteriori dettagli.</span><span class="sxs-lookup"><span data-stu-id="88686-126">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-127">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="88686-127">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="88686-128">È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna di aggiornamento del deposito o di una colonna SLV. si noti che le colonne SLV sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="88686-128">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-129">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="88686-129">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="88686-130">Restituito se il parametro <em>ptablecreate- &gt; grbit</em> specifica il valore JET_bitTableCreateTemplateTable, ma il parametro <em>ptablecreate- &gt; szTemplateTableName</em> è impostato su null.</span><span class="sxs-lookup"><span data-stu-id="88686-130">Returned if the <em>ptablecreate-&gt;grbit</em> parameter specifies the JET_bitTableCreateTemplateTable value, but the <em>ptablecreate-&gt;szTemplateTableName</em> parameter is set to null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-131">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="88686-131">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="88686-132">Una colonna esiste già.</span><span class="sxs-lookup"><span data-stu-id="88686-132">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="88686-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="88686-134">È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna inesistente.</span><span class="sxs-lookup"><span data-stu-id="88686-134">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="88686-135">Un tentativo di eseguire l'indicizzazione condizionale su una colonna inesistente può anche generare questo errore.</span><span class="sxs-lookup"><span data-stu-id="88686-135">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-136">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="88686-136">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="88686-137">È stato effettuato un tentativo di aggiungere una colonna ridondante.</span><span class="sxs-lookup"><span data-stu-id="88686-137">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="88686-138">Non deve esistere più di una colonna AutoIncrement e non deve esistere più di una colonna di versione per ogni tabella.</span><span class="sxs-lookup"><span data-stu-id="88686-138">No more than one autoincrement column should exist, and no more than one version column should exist per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-139">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="88686-139">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="88686-140">Questo errore viene restituito se il membro <strong>ulDensity</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su un numero minore di 20 o maggiore di 100.</span><span class="sxs-lookup"><span data-stu-id="88686-140">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-141">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="88686-141">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="88686-142">Indica che la tabella denominata nel membro <strong>szTemplateTableName</strong> della struttura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> non è stata contrassegnata come tabella modello (ovvero, per la tabella non è stato impostato il valore del parametro JET_bitTableCreateTemplateTable).</span><span class="sxs-lookup"><span data-stu-id="88686-142">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have the JET_bitTableCreateTemplateTable parameter value set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-143">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="88686-143">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="88686-144">È stato eseguito un tentativo di definire due indici identici.</span><span class="sxs-lookup"><span data-stu-id="88686-144">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-145">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="88686-145">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="88686-146">È stato effettuato un tentativo di specificare più di un indice primario per una tabella.</span><span class="sxs-lookup"><span data-stu-id="88686-146">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="88686-147">Una tabella deve avere esattamente un indice primario.</span><span class="sxs-lookup"><span data-stu-id="88686-147">A table must have exactly one primary index.</span></span> <span data-ttu-id="88686-148">Se non viene specificato alcun indice primario, il motore di database ne creerà uno in modo trasparente.</span><span class="sxs-lookup"><span data-stu-id="88686-148">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-149">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="88686-149">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="88686-150">È stata specificata una definizione di indice non valida.</span><span class="sxs-lookup"><span data-stu-id="88686-150">An invalid index definition was specified.</span></span> <span data-ttu-id="88686-151">Di seguito sono riportate alcune delle possibili cause di questo errore:</span><span class="sxs-lookup"><span data-stu-id="88686-151">The following are some of the possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="88686-152">Un indice primario è condizionale (ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> dispone del valore JET_bitIndexPrimary impostato e il membro <strong>cConditionalColumn</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è maggiore di zero).</span><span class="sxs-lookup"><span data-stu-id="88686-152">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexPrimary value set, and the <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="88686-153">Si applica alle versioni del sistema operativo Windows Server a partire da Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="88686-153">Applies to versions of the Windows Server operating system starting with Windows Server 2003.</span></span> <span data-ttu-id="88686-154">Tentativo di creare un indice di tupla con limiti di tupla, ma senza passare il membro <strong>ptuplelimits</strong> nella struttura di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (ovvero il membro <strong>grbit</strong> della struttura <strong>JET_INDEXCREATE2</strong> ha JET_bitIndexTupleLimits set di valori, ma il puntatore <strong>ptuplelimits</strong> è null).</span><span class="sxs-lookup"><span data-stu-id="88686-154">An attempt to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the <strong>JET_INDEXCREATE2</strong> structure has JET_bitIndexTupleLimits value set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="88686-155">Passaggio di una definizione di chiave non valida nel membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="88686-155">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="88686-156">Per informazioni sulle definizioni valide, vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="88686-156">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="88686-157">L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> in modo che sia maggiore del valore di JET_cbPrimaryKeyMost (per un indice primario) o maggiore del valore JET_cbSecondaryKeyMost (per un indice secondario).</span><span class="sxs-lookup"><span data-stu-id="88686-157">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than the JET_cbPrimaryKeyMost value (for a primary index) or greater than the JET_cbSecondaryKeyMost value (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="88686-158">Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit del valore JET_bitIndexUnicode impostato nel membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="88686-158">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode value bit set in the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span> <span data-ttu-id="88686-159">Alcune cause comuni includono il membro <strong>pidxunicode</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è null o l'LCID specificato nella struttura <strong>pidxunicode</strong> non è valido.</span><span class="sxs-lookup"><span data-stu-id="88686-159">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="88686-160">Specifica di una colonna multivalore per un indice primario.</span><span class="sxs-lookup"><span data-stu-id="88686-160">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="88686-161">Tentativo di indicizzare un numero eccessivo di colonne condizionali.</span><span class="sxs-lookup"><span data-stu-id="88686-161">Trying to index too many conditional columns.</span></span> <span data-ttu-id="88686-162">Il membro <strong>cConditionalColumn</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve essere maggiore di <strong>JET_ccolKeyMost</strong>.</span><span class="sxs-lookup"><span data-stu-id="88686-162">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-163">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="88686-163">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="88686-164">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88686-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="88686-165">È stata specificata una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> e i relativi limiti non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="88686-165">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="88686-166">Per ulteriori informazioni, vedere la sezione Osservazioni della struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="88686-166">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-167">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="88686-167">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="88686-168">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88686-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="88686-169">Un indice di tupla non può essere univoco, ovvero il membro <em>grbit</em> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere set di valori JET_bitIndexPrimary e JET_bitIndexUnique).</span><span class="sxs-lookup"><span data-stu-id="88686-169">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique values set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-170">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="88686-170">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="88686-171">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88686-171">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="88686-172">Un indice di tupla può trovarsi solo su una singola colonna, ovvero se il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> dispone di JET_bitIndexTuples valore impostato e il membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> specifica più di una colonna.</span><span class="sxs-lookup"><span data-stu-id="88686-172">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples value set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-173">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="88686-173">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="88686-174">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88686-174">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="88686-175">Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexTuples impostato).</span><span class="sxs-lookup"><span data-stu-id="88686-175">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-176">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="88686-176">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="88686-177">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88686-177">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="88686-178">Un indice tupla può trovarsi solo in una colonna di tipo text o Unicode.</span><span class="sxs-lookup"><span data-stu-id="88686-178">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="88686-179">Un tentativo di indicizzare altre colonne, ad esempio colonne binarie, comporterà un JET_errIndexTuplesTextColumnsOnly codice di risposta.</span><span class="sxs-lookup"><span data-stu-id="88686-179">An attempt to index other columns (such as binary columns) will result in a JET_errIndexTuplesTextColumnsOnly response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-180">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="88686-180">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="88686-181">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88686-181">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="88686-182">Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="88686-182">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-183">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="88686-183">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="88686-184">È stato effettuato un tentativo di creare un indice senza informazioni sulla versione in una transazione.</span><span class="sxs-lookup"><span data-stu-id="88686-184">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-185">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="88686-185">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="88686-186">Il membro <strong>CP</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> non è stato impostato su una tabella codici valida.</span><span class="sxs-lookup"><span data-stu-id="88686-186">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="88686-187">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="88686-187">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="88686-188">Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="88686-188">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-189">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="88686-189">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="88686-190">Il membro <strong>coltyp</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> non è stato impostato su un tipo di colonna valido.</span><span class="sxs-lookup"><span data-stu-id="88686-190">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-191">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="88686-191">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="88686-192">Di seguito sono riportati alcuni dei motivi per cui è possibile che si verifichi questo errore:</span><span class="sxs-lookup"><span data-stu-id="88686-192">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="88686-193">Il membro <strong>rgindexcreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su null.</span><span class="sxs-lookup"><span data-stu-id="88686-193">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="88686-194">Il membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su null.</span><span class="sxs-lookup"><span data-stu-id="88686-194">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="88686-195">Il membro <strong>cbStruct</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è stato impostato su un valore valido.</span><span class="sxs-lookup"><span data-stu-id="88686-195">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-196">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="88686-196">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="88686-197">Nella struttura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> è stata specificata una combinazione non valida di membri <strong>grbit</strong> .</span><span class="sxs-lookup"><span data-stu-id="88686-197">An invalid combination of <strong>grbit</strong> members was specified in the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure.</span></span></p>
<p><span data-ttu-id="88686-198">La definizione dell'indice non è valida perché il membro <strong>grbit</strong> contiene valori incoerenti.</span><span class="sxs-lookup"><span data-stu-id="88686-198">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="88686-199">Di seguito sono riportati alcuni dei possibili motivi:</span><span class="sxs-lookup"><span data-stu-id="88686-199">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="88686-200">Per un indice primario è stato specificato un bit ignore, ovvero JET_bitIndexPrimary valore è stato passato con i valori JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull.</span><span class="sxs-lookup"><span data-stu-id="88686-200">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary value was passed with the JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull values).</span></span></p></li>
<li><p><span data-ttu-id="88686-201">Un indice vuoto non ignora i membri null, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> dispone del valore JET_bitIndexEmpty impostato, ma non ha JET_bitIndexIgnoreAnyNull set di valori.</span><span class="sxs-lookup"><span data-stu-id="88686-201">An empty index does not ignore any null members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexEmpty value set, but does not have JET_bitIndexIgnoreAnyNull value set).</span></span></p></li>
<li><p><span data-ttu-id="88686-202">Passaggio di una struttura di <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit</strong> non valido.</span><span class="sxs-lookup"><span data-stu-id="88686-202">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="88686-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="88686-204">È stato passato un ID delle impostazioni locali (LCID) non valido (tramite il membro <strong>LCID</strong> della struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a cui punta il membro <strong>pidxunicode</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> o tramite il campo <strong>LCID</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="88686-204">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure that the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure points to, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-205">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="88686-205">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="88686-206">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="88686-206">An invalid parameter was given.</span></span> <span data-ttu-id="88686-207">Di seguito sono riportati alcuni dei possibili motivi:</span><span class="sxs-lookup"><span data-stu-id="88686-207">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="88686-208">Il membro <strong>rgcolumncreate</strong> della struttura <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> è null.</span><span class="sxs-lookup"><span data-stu-id="88686-208">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is null.</span></span></p></li>
<li><p><span data-ttu-id="88686-209">Il membro <strong>cbStruct</strong> di una delle strutture <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> fornite nel membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> non è stato impostato su sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="88686-209">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="88686-210">Il membro <strong>cbKey</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="88686-210">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="88686-211">Il membro <strong>cbStruct</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è impostato su sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="88686-211">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-212">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="88686-212">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="88686-213">Il record è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="88686-213">The record is too big.</span></span> <span data-ttu-id="88686-214">La somma del membro <strong>cbMax</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> per tutte le colonne fisse non deve superare un determinato valore.</span><span class="sxs-lookup"><span data-stu-id="88686-214">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-215">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="88686-215">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="88686-216">La tabella esiste già.</span><span class="sxs-lookup"><span data-stu-id="88686-216">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-217">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="88686-217">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="88686-218">È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella.</span><span class="sxs-lookup"><span data-stu-id="88686-218">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="88686-219">Una tabella non può contenere più di <strong>JET_ccolFixedMost</strong> colonne fisse, non più di <strong>JET_ccolVarMost</strong> colonne a lunghezza variabile e non più di <strong>JET_ccolTaggedMost</strong> colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="88686-219">A table can have no more than <strong>JET_ccolFixedMost</strong> fixed columns, no more than <strong>JET_ccolVarMost</strong> variable-length columns, and no more than <strong>JET_ccolTaggedMost</strong> tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-220">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="88686-220">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="88686-221">Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode.</span><span class="sxs-lookup"><span data-stu-id="88686-221">An error occurred when an attempt was made to normalize a Unicode column.</span></span> <span data-ttu-id="88686-222">Questo problema può essere causato dall'esaurimento delle risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="88686-222">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-223">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="88686-223">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="88686-224">Un elemento della struttura degli hint di spazio JET non è corretto o non è attivabile.</span><span class="sxs-lookup"><span data-stu-id="88686-224">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="88686-225">Commenti</span><span class="sxs-lookup"><span data-stu-id="88686-225">Remarks</span></span>

<span data-ttu-id="88686-226">La funzione **JetCreateTableColumnIndex4W** crea una tabella con un set iniziale di colonne e indici.</span><span class="sxs-lookup"><span data-stu-id="88686-226">The **JetCreateTableColumnIndex4W** function creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="88686-227">È possibile aggiungere e rimuovere in modo dinamico colonne e indici aggiuntivi mediante le funzioni [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)e [JetDeleteIndex](./jetdeleteindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="88686-227">Additional columns and indexes can be added and removed dynamically by means of the [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md) functions.</span></span>

<span data-ttu-id="88686-228">Come per la funzione [JetOpenTable](./jetopentable-function.md) , quando l'applicazione viene eseguita utilizzando il *TableID* restituito, la funzione [JetCloseTable](./jetclosetable-function.md) deve chiudere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="88686-228">As with the [JetOpenTable](./jetopentable-function.md) function, when the application is done using the returned *tableid*, the [JetCloseTable](./jetclosetable-function.md) function should close the application.</span></span>

#### <a name="requirements"></a><span data-ttu-id="88686-229">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88686-229">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88686-230"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="88686-230"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="88686-231">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="88686-231">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-232"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="88686-232"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="88686-233">Richiede Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="88686-233">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-234"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="88686-234"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="88686-235">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="88686-235">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88686-236"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="88686-236"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="88686-237">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="88686-237">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88686-238"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="88686-238"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="88686-239">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="88686-239">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="88686-240">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88686-240">See also</span></span>

[<span data-ttu-id="88686-241">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="88686-241">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="88686-242">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="88686-242">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="88686-243">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="88686-243">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="88686-244">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="88686-244">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="88686-245">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="88686-245">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="88686-246">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="88686-246">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="88686-247">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="88686-247">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="88686-248">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="88686-248">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="88686-249">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="88686-249">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="88686-250">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="88686-250">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="88686-251">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="88686-251">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="88686-252">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="88686-252">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="88686-253">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="88686-253">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="88686-254">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="88686-254">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="88686-255">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="88686-255">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="88686-256">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="88686-256">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="88686-257">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="88686-257">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="88686-258">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="88686-258">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="88686-259">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="88686-259">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
