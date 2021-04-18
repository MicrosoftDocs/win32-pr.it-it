---
description: 'Altre informazioni su: funzione JetCreateIndex4W'
title: Funzione JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315631"
---
# <a name="jetcreateindex4w-function"></a><span data-ttu-id="23802-103">Funzione JetCreateIndex4W</span><span class="sxs-lookup"><span data-stu-id="23802-103">JetCreateIndex4W Function</span></span>


<span data-ttu-id="23802-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="23802-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="23802-105">La funzione **JetCreateIndex4W** crea indici sui dati in un database Extensible Storage Engine (ESE), che può essere usato per individuare rapidamente dati specifici.</span><span class="sxs-lookup"><span data-stu-id="23802-105">The **JetCreateIndex4W** function creates indexes over data in an Extensible Storage Engine (ESE) database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="23802-106">La funzione **JetCreateIndex4W** è stata introdotta nel sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="23802-106">The **JetCreateIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a><span data-ttu-id="23802-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="23802-107">Parameters</span></span>

<span data-ttu-id="23802-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="23802-108">*sesid*</span></span>

<span data-ttu-id="23802-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="23802-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="23802-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="23802-110">*tableid*</span></span>

<span data-ttu-id="23802-111">Tabella in cui verrà creato l'indice.</span><span class="sxs-lookup"><span data-stu-id="23802-111">The table on which the index will be created.</span></span>

<span data-ttu-id="23802-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="23802-112">*pindexcreate*</span></span>

<span data-ttu-id="23802-113">Matrice di strutture di [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , ognuna delle quali definisce un indice da creare.</span><span class="sxs-lookup"><span data-stu-id="23802-113">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="23802-114">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="23802-114">*cIndexCreate*</span></span>

<span data-ttu-id="23802-115">Numero di elementi nella matrice *pindexcreate* .</span><span class="sxs-lookup"><span data-stu-id="23802-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="23802-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23802-116">Return value</span></span>

<span data-ttu-id="23802-117">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei codici restituiti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="23802-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="23802-118">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="23802-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23802-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="23802-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="23802-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23802-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23802-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="23802-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="23802-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="23802-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="23802-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="23802-124">È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna di aggiornamento del deposito o di una colonna SLV. si noti che le colonne SLV sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="23802-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="23802-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="23802-126">È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna inesistente.</span><span class="sxs-lookup"><span data-stu-id="23802-126">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="23802-127">Un tentativo di eseguire l'indicizzazione condizionale su una colonna inesistente può anche generare questo errore.</span><span class="sxs-lookup"><span data-stu-id="23802-127">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="23802-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="23802-129">Questo errore viene restituito se il membro <strong>ulDensity</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su un numero minore di 20 o maggiore di 100.</span><span class="sxs-lookup"><span data-stu-id="23802-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="23802-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="23802-131">È stato eseguito un tentativo di definire due indici identici.</span><span class="sxs-lookup"><span data-stu-id="23802-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="23802-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="23802-133">È stato effettuato un tentativo di specificare più di un indice primario per una tabella.</span><span class="sxs-lookup"><span data-stu-id="23802-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="23802-134">Una tabella deve avere esattamente un indice primario.</span><span class="sxs-lookup"><span data-stu-id="23802-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="23802-135">Se non viene specificato alcun indice primario, il motore di database ne creerà uno in modo trasparente.</span><span class="sxs-lookup"><span data-stu-id="23802-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="23802-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="23802-137">È stata specificata una definizione di indice non valida.</span><span class="sxs-lookup"><span data-stu-id="23802-137">An invalid index definition was specified.</span></span> <span data-ttu-id="23802-138">Di seguito sono riportate alcune possibili cause di questo errore:</span><span class="sxs-lookup"><span data-stu-id="23802-138">The following are some possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="23802-139">Un indice primario è condizionale (il membro<strong>grbit</strong> del <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha <strong>JET_bitIndexPrimary</strong> set e il membro <strong>cConditionalColumn</strong> di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è maggiore di zero).</span><span class="sxs-lookup"><span data-stu-id="23802-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has <strong>JET_bitIndexPrimary</strong> set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="23802-140">Si applica alle versioni di Windows a partire da Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="23802-140">Applies to versions of Windows starting with Windows Server 2003.</span></span> <span data-ttu-id="23802-141">È stato effettuato un tentativo di creare un indice di tupla con limiti di tupla, ma senza passare le informazioni nel membro <strong>ptuplelimits</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> , ovvero <em>grbit</em> ha impostato <strong>JET_bitIndexTupleLimits</strong> , ma il puntatore <strong>ptuplelimits</strong> è null.</span><span class="sxs-lookup"><span data-stu-id="23802-141">An attempt was made to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has <strong>JET_bitIndexTupleLimits</strong> set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="23802-142">Passaggio di una definizione di chiave non valida nel membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="23802-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="23802-143">Per informazioni sulle definizioni valide, vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="23802-143">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="23802-144">L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> su un valore maggiore di <strong>JET_cbPrimaryKeyMost</strong> (per un indice primario) o maggiore di <strong>JET_cbSecondaryKeyMost</strong> (per un indice secondario).</span><span class="sxs-lookup"><span data-stu-id="23802-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than <strong>JET_cbPrimaryKeyMost</strong> (for a primary index) or greater than <strong>JET_cbSecondaryKeyMost</strong> (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="23802-145">Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit <strong>JET_bitIndexUnicode</strong> impostato nel membro <strong>grbit</strong> di <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span><span class="sxs-lookup"><span data-stu-id="23802-145">Passing an invalid combination for a user-defined Unicode index (one which has the <strong>JET_bitIndexUnicode</strong> bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="23802-146">Alcune cause comuni possono essere che il campo pidxunicode della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è null o che l'identificatore LCID specificato nella struttura pidxunicode non è valido.</span><span class="sxs-lookup"><span data-stu-id="23802-146">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="23802-147">Specifica di una colonna multivalore per un indice primario.</span><span class="sxs-lookup"><span data-stu-id="23802-147">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="23802-148">Tentativo di indicizzare un numero eccessivo di colonne condizionali.</span><span class="sxs-lookup"><span data-stu-id="23802-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="23802-149">Il membro <strong>cConditionalColumn</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve essere maggiore di <strong>JET_ccolKeyMost</strong>.</span><span class="sxs-lookup"><span data-stu-id="23802-149">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="23802-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="23802-151">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="23802-151">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="23802-152">È stata specificata una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> e i relativi limiti non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="23802-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="23802-153">Per ulteriori informazioni, vedere la sezione Osservazioni della struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="23802-153">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="23802-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="23802-155">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="23802-155">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="23802-156">Un indice di tupla non può essere univoco (<em>grbit</em> non deve avere sia <strong>JET_bitIndexTuples</strong> che <strong>JET_bitIndexUnique</strong> impostato).</span><span class="sxs-lookup"><span data-stu-id="23802-156">A tuple index cannot be unique (<em>grbit</em> must not have both <strong>JET_bitIndexTuples</strong> and <strong>JET_bitIndexUnique</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="23802-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="23802-158">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="23802-158">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="23802-159">Un indice di tupla può trovarsi solo su una singola colonna, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> dispone di <strong>JET_bitIndexTuples</strong> set e il membro <strong>szKey</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> specifica più di una colonna.</span><span class="sxs-lookup"><span data-stu-id="23802-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexTuples</strong> set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="23802-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="23802-161">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="23802-161">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="23802-162">Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non deve avere sia <strong>JET_bitIndexPrimary</strong> che <strong>JET_bitIndexTuples</strong> impostato).</span><span class="sxs-lookup"><span data-stu-id="23802-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both <strong>JET_bitIndexPrimary</strong> and <strong>JET_bitIndexTuples</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="23802-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="23802-164">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="23802-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="23802-165">Un indice tupla può trovarsi solo in una colonna di tipo text o Unicode.</span><span class="sxs-lookup"><span data-stu-id="23802-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="23802-166">Il tentativo di indicizzare altre colonne, ad esempio colonne binarie, comporterà la <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span><span class="sxs-lookup"><span data-stu-id="23802-166">An attempt to index other columns (for example, binary columns) will result in <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="23802-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="23802-168">Si applica alle versioni di Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="23802-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="23802-169">Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="23802-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="23802-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="23802-171">È stato effettuato un tentativo di creare un indice senza informazioni sulla versione in una transazione.</span><span class="sxs-lookup"><span data-stu-id="23802-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="23802-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="23802-173">La definizione dell'indice non è valida perché il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene valori incoerenti.</span><span class="sxs-lookup"><span data-stu-id="23802-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="23802-174">Di seguito sono riportati alcuni dei possibili motivi:</span><span class="sxs-lookup"><span data-stu-id="23802-174">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="23802-175">Per un indice primario è stato specificato un bit ignoto (JET_bitIndexPrimary è stato passato con una delle <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>o <strong>JET_bitIndexIgnoreFirstNull</strong>).</span><span class="sxs-lookup"><span data-stu-id="23802-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>, or <strong>JET_bitIndexIgnoreFirstNull</strong>).</span></span></p></li>
<li><p><span data-ttu-id="23802-176">Un indice vuoto non ignora alcun campo null, ovvero il membro <strong>grbit</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ha <strong>JET_bitIndexEmpty</strong> set, ma non ha <strong>JET_bitIndexIgnoreAnyNull</strong> set.</span><span class="sxs-lookup"><span data-stu-id="23802-176">An empty index does not ignore any null fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexEmpty</strong> set, but does not have <strong>JET_bitIndexIgnoreAnyNull</strong> set).</span></span></p></li>
<li><p><span data-ttu-id="23802-177">Passaggio di una struttura di <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit</strong> non valido.</span><span class="sxs-lookup"><span data-stu-id="23802-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="23802-178">Vedere <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="23802-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="23802-179">Quando si creano più indici contemporaneamente (ovvero se il parametro <em>cIndexCreate</em> è maggiore di uno), nessuno degli indici può contenere uno dei bit seguenti:</span><span class="sxs-lookup"><span data-stu-id="23802-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="23802-180"><strong>JET_bitIndexPrimary</strong></span><span class="sxs-lookup"><span data-stu-id="23802-180"><strong>JET_bitIndexPrimary</strong></span></span></p></li>
<li><p><span data-ttu-id="23802-181"><strong>JET_bitIndexUnversioned</strong></span><span class="sxs-lookup"><span data-stu-id="23802-181"><strong>JET_bitIndexUnversioned</strong></span></span></p></li>
<li><p><span data-ttu-id="23802-182"><strong>JET_bitIndexEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="23802-182"><strong>JET_bitIndexEmpty</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="23802-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="23802-184">È stato passato un ID delle impostazioni locali (LCID) non valido (tramite il membro <strong>LCID</strong> della struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , che il membro <strong>pidxunicode</strong> nella struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contiene un puntatore a oppure tramite il membro <strong>LCID</strong> della struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span><span class="sxs-lookup"><span data-stu-id="23802-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="23802-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="23802-186">È stato specificato un nome di indice non valido.</span><span class="sxs-lookup"><span data-stu-id="23802-186">An invalid index name was specified.</span></span> <span data-ttu-id="23802-187">Per ulteriori informazioni, vedere <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="23802-187">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="23802-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="23802-189">Un parametro non valido è stato passato nell'API.</span><span class="sxs-lookup"><span data-stu-id="23802-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="23802-190">Di seguito sono riportati alcuni dei motivi per cui può essere restituito questo errore:</span><span class="sxs-lookup"><span data-stu-id="23802-190">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="23802-191">Il campo <strong>cbKey</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="23802-191">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="23802-192">Il membro <strong>cbStruct</strong> di una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> non è impostato su sizeof (JET_INDEXCREATE2).</span><span class="sxs-lookup"><span data-stu-id="23802-192">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof(JET_INDEXCREATE2).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="23802-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="23802-194">Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode.</span><span class="sxs-lookup"><span data-stu-id="23802-194">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="23802-195">Questo problema può essere causato dall'esaurimento delle risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="23802-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-196">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="23802-196">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="23802-197">Un elemento della struttura degli hint di spazio JET non è corretto o non è attivabile.</span><span class="sxs-lookup"><span data-stu-id="23802-197">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="23802-198">Commenti</span><span class="sxs-lookup"><span data-stu-id="23802-198">Remarks</span></span>

<span data-ttu-id="23802-199">La funzione **JetCreateIndex4W** scorre gli indici specificati nel parametro *pindexcreate* e talvolta si interrompe al primo errore.</span><span class="sxs-lookup"><span data-stu-id="23802-199">The **JetCreateIndex4W** function iterates through the indexes given in the *pindexcreate* parameter, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="23802-200">Eventuali indici dopo il primo indice con un errore potrebbero non essere stati tentati, anche se il membro **Err** della struttura [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contiene JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="23802-200">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="23802-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23802-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23802-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="23802-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="23802-203">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="23802-203">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="23802-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="23802-205">Richiede Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="23802-205">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-206"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="23802-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="23802-207">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="23802-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23802-208"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="23802-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="23802-209">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="23802-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23802-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="23802-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="23802-211">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="23802-211">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="23802-212">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23802-212">See also</span></span>

[<span data-ttu-id="23802-213">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="23802-213">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="23802-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="23802-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="23802-215">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="23802-215">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="23802-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="23802-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="23802-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="23802-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="23802-218">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="23802-218">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="23802-219">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="23802-219">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="23802-220">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="23802-220">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="23802-221">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="23802-221">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="23802-222">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="23802-222">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
