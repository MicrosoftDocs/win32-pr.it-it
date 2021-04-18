---
description: 'Altre informazioni su: funzione JetCreateTable'
title: Funzione JetCreateTable
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f385cfd668af934bfde2669277db7ed048a1fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319184"
---
# <a name="jetcreatetable-function"></a><span data-ttu-id="f60b4-103">Funzione JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="f60b4-103">JetCreateTable Function</span></span>


<span data-ttu-id="f60b4-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f60b4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetable-function"></a><span data-ttu-id="f60b4-105">Funzione JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="f60b4-105">JetCreateTable Function</span></span>

<span data-ttu-id="f60b4-106">La funzione **JetCreateTable** crea una tabella vuota in un database ESE.</span><span class="sxs-lookup"><span data-stu-id="f60b4-106">The **JetCreateTable** function creates an empty table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="f60b4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f60b4-107">Parameters</span></span>

<span data-ttu-id="f60b4-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f60b4-108">*sesid*</span></span>

<span data-ttu-id="f60b4-109">Contesto della sessione di database da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f60b4-109">The database session context to use.</span></span>

<span data-ttu-id="f60b4-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="f60b4-110">*dbid*</span></span>

<span data-ttu-id="f60b4-111">Identificatore del database da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f60b4-111">The database identifier to use.</span></span>

<span data-ttu-id="f60b4-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="f60b4-112">*szTableName*</span></span>

<span data-ttu-id="f60b4-113">Nome dell'indice da creare.</span><span class="sxs-lookup"><span data-stu-id="f60b4-113">The name of the index to create.</span></span>

<span data-ttu-id="f60b4-114">Il nome deve essere formattato in base alle regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="f60b4-114">The name must be formatted according to the following rules:</span></span>

  - <span data-ttu-id="f60b4-115">Essere minore di JET_cbNameMost, escluso il valore NULL di terminazione.</span><span class="sxs-lookup"><span data-stu-id="f60b4-115">Be less than JET_cbNameMost, not including the terminating NULL.</span></span>

  - <span data-ttu-id="f60b4-116">Essere costituito dal set di caratteri seguente: da 0 a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di " \! "</span><span class="sxs-lookup"><span data-stu-id="f60b4-116">Be made of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="f60b4-117">(punto esclamativo), "," (virgola), " \[ " (parentesi di apertura) e " \] " (parentesi di chiusura), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c, 0x5D tramite 0x7F.</span><span class="sxs-lookup"><span data-stu-id="f60b4-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="f60b4-118">Non iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="f60b4-118">Not begin with a space.</span></span>

  - <span data-ttu-id="f60b4-119">Essere costituito da almeno un carattere diverso dallo spazio.</span><span class="sxs-lookup"><span data-stu-id="f60b4-119">Be made of at least one non-space character.</span></span>

<span data-ttu-id="f60b4-120">*lPages*</span><span class="sxs-lookup"><span data-stu-id="f60b4-120">*lPages*</span></span>

<span data-ttu-id="f60b4-121">Numero iniziale di pagine del database da allocare per la tabella.</span><span class="sxs-lookup"><span data-stu-id="f60b4-121">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="f60b4-122">La specifica di un numero maggiore di uno può ridurre la frammentazione se nella tabella vengono inserite molte righe.</span><span class="sxs-lookup"><span data-stu-id="f60b4-122">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="f60b4-123">*lDensity*</span><span class="sxs-lookup"><span data-stu-id="f60b4-123">*lDensity*</span></span>

<span data-ttu-id="f60b4-124">Densità della tabella, in punti percentuali.</span><span class="sxs-lookup"><span data-stu-id="f60b4-124">The table density, in percentage points.</span></span> <span data-ttu-id="f60b4-125">Il numero deve essere 0 o compreso tra 20 e 100.</span><span class="sxs-lookup"><span data-stu-id="f60b4-125">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="f60b4-126">Il valore 0 indica che deve essere utilizzato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f60b4-126">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="f60b4-127">Il valore predefinito è 80.</span><span class="sxs-lookup"><span data-stu-id="f60b4-127">The default is 80.</span></span>

<span data-ttu-id="f60b4-128">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="f60b4-128">*ptableid*</span></span>

<span data-ttu-id="f60b4-129">In seguito all'esito positivo, l'identificatore di tabella viene restituito in questo campo.</span><span class="sxs-lookup"><span data-stu-id="f60b4-129">On success, the table identifier is returned in this field.</span></span> <span data-ttu-id="f60b4-130">Il valore non è definito se l'API non restituisce JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="f60b4-130">The value is undefined if the API does not return JET_errSuccess.</span></span>

### <a name="return-value"></a><span data-ttu-id="f60b4-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f60b4-131">Return Value</span></span>

<span data-ttu-id="f60b4-132">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="f60b4-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f60b4-133">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="f60b4-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f60b4-134">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f60b4-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="f60b4-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f60b4-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f60b4-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f60b4-137">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="f60b4-137">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-138">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="f60b4-138">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="f60b4-139">Non è stato possibile risolvere la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="f60b4-139">The callback function could not be resolved.</span></span> <span data-ttu-id="f60b4-140">È possibile che la DLL non sia stata trovata o che la funzione nella DLL non sia stata trovata.</span><span class="sxs-lookup"><span data-stu-id="f60b4-140">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="f60b4-141">Con la registrazione sufficiente abilitata, nel registro eventi vengono forniti ulteriori dettagli.</span><span class="sxs-lookup"><span data-stu-id="f60b4-141">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-142">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="f60b4-142">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="f60b4-143">È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna di aggiornamento del deposito o di una colonna SLV. si noti che le colonne SLV sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="f60b4-143">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-144">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="f60b4-144">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="f60b4-145">Se ptablecreate- &gt; grbit specifica JET_bitTableCreateTemplateTable, ma ptablecreate- &gt; szTemplateTableName è impostato su null.</span><span class="sxs-lookup"><span data-stu-id="f60b4-145">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-146">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="f60b4-146">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="f60b4-147">Una colonna esiste già.</span><span class="sxs-lookup"><span data-stu-id="f60b4-147">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-148">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="f60b4-148">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="f60b4-149">È stato effettuato un tentativo di eseguire l'indicizzazione su una colonna non esistente.</span><span class="sxs-lookup"><span data-stu-id="f60b4-149">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="f60b4-150">Il tentativo di eseguire l'indicizzazione condizionale su una colonna inesistente può anche generare questo errore.</span><span class="sxs-lookup"><span data-stu-id="f60b4-150">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-151">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="f60b4-151">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="f60b4-152">È stato effettuato un tentativo di aggiungere una colonna ridondante.</span><span class="sxs-lookup"><span data-stu-id="f60b4-152">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="f60b4-153">Non deve essere presente più di una colonna AutoIncrement e non più di una colonna versione per tabella.</span><span class="sxs-lookup"><span data-stu-id="f60b4-153">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-154">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="f60b4-154">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="f60b4-155">È stata passata una densità non valida nel membro <em>ulDensity</em> della struttura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="f60b4-155">An invalid density was passed in the <em>ulDensity</em> member in the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-156">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="f60b4-156">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="f60b4-157">Indica che la tabella denominata nel membro <strong>szTemplateTableName</strong> della struttura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> non è stata contrassegnata come tabella modello (ovvero la tabella non dispone di JET_bitTableCreateTemplateTable impostato).</span><span class="sxs-lookup"><span data-stu-id="f60b4-157">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not a marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-158">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="f60b4-158">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="f60b4-159">È stato effettuato un tentativo di definire due indici identici.</span><span class="sxs-lookup"><span data-stu-id="f60b4-159">An attempt was made to define two identical indexes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-160">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="f60b4-160">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="f60b4-161">È stato effettuato un tentativo di specificare più di un indice primario per una tabella.</span><span class="sxs-lookup"><span data-stu-id="f60b4-161">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="f60b4-162">Una tabella deve avere esattamente un indice primario.</span><span class="sxs-lookup"><span data-stu-id="f60b4-162">A table must have exactly one primary index.</span></span> <span data-ttu-id="f60b4-163">Se non viene specificato alcun indice primario, il motore di database ne creerà uno in modo trasparente.</span><span class="sxs-lookup"><span data-stu-id="f60b4-163">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-164">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="f60b4-164">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="f60b4-165">È stata specificata una definizione di indice non valida.</span><span class="sxs-lookup"><span data-stu-id="f60b4-165">An invalid index definition was specified.</span></span> <span data-ttu-id="f60b4-166">Di seguito sono riportati alcuni dei possibili motivi per la ricezione di questo errore:</span><span class="sxs-lookup"><span data-stu-id="f60b4-166">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="f60b4-167">Un indice primario è condizionale (ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_bitIndexPrimary set e il membro <strong>cConditionalColumn</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è maggiore di zero).</span><span class="sxs-lookup"><span data-stu-id="f60b4-167">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="f60b4-168">Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f60b4-168">Windows Server 2003 and later.</span></span> <span data-ttu-id="f60b4-169">Il tentativo di creare un indice di tupla con limiti di tupla, ma senza passare il membro <strong>ptuplelimits</strong> nella struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_BITINDEXTUPLELIMITS set, ma il puntatore <strong>ptuplelimits</strong> è null).</span><span class="sxs-lookup"><span data-stu-id="f60b4-169">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="f60b4-170">Passaggio di una definizione di chiave non valida nel membro <strong>szKey</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f60b4-170">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="f60b4-171">Per una descrizione delle definizioni valide, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f60b4-171">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="f60b4-172">L'impostazione del membro <strong>cbVarSegMac</strong> in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> su un valore maggiore di JET_cbPrimaryKeyMost (per un indice primario) o maggiore di JET_cbSecondaryKeyMost (per un indice secondario).</span><span class="sxs-lookup"><span data-stu-id="f60b4-172">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="f60b4-173">Passaggio di una combinazione non valida per un indice Unicode definito dall'utente (uno con il bit JET_bitIndexUnicode impostato nel membro <strong>grbit</strong> di <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span><span class="sxs-lookup"><span data-stu-id="f60b4-173">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="f60b4-174">Alcune cause comuni includono il membro <strong>pidxunicode</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è null o l'LCID specificato nella struttura <strong>pidxunicode</strong> non è valido.</span><span class="sxs-lookup"><span data-stu-id="f60b4-174">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="f60b4-175">Specifica di una colonna multivalore per un indice primario.</span><span class="sxs-lookup"><span data-stu-id="f60b4-175">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="f60b4-176">Tentativo di indicizzare un numero eccessivo di colonne condizionali.</span><span class="sxs-lookup"><span data-stu-id="f60b4-176">Trying to index too many conditional columns.</span></span> <span data-ttu-id="f60b4-177">Il membro <strong>cConditionalColumn</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non deve essere maggiore di JET_ccolKeyMost.</span><span class="sxs-lookup"><span data-stu-id="f60b4-177">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-178">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="f60b4-178">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="f60b4-179">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f60b4-179">Windows XP and later.</span></span> <span data-ttu-id="f60b4-180">È stata specificata una struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> e i relativi limiti non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="f60b4-180">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="f60b4-181">Vedere la sezione Osservazioni della struttura <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</span><span class="sxs-lookup"><span data-stu-id="f60b4-181">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-182">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="f60b4-182">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="f60b4-183">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f60b4-183">Windows XP and later.</span></span> <span data-ttu-id="f60b4-184">Un indice di tupla non può essere univoco, ovvero il membro <em>grbit</em> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexUnique impostato).</span><span class="sxs-lookup"><span data-stu-id="f60b4-184">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-185">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="f60b4-185">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="f60b4-186">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f60b4-186">Windows XP and later.</span></span> <span data-ttu-id="f60b4-187">Un indice della tupla può trovarsi solo su una singola colonna, ovvero se il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> dispone di JET_bitIndexTuples set e il membro <strong>szKey</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> specifica più di una colonna.</span><span class="sxs-lookup"><span data-stu-id="f60b4-187">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-188">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="f60b4-188">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="f60b4-189">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f60b4-189">Windows XP and later.</span></span> <span data-ttu-id="f60b4-190">Un indice di tupla non può essere un indice primario, ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non deve avere sia JET_bitIndexPrimary che JET_bitIndexTuples impostato).</span><span class="sxs-lookup"><span data-stu-id="f60b4-190">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-191">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="f60b4-191">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="f60b4-192">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f60b4-192">Windows XP and later.</span></span> <span data-ttu-id="f60b4-193">Un indice di tupla non consente l'impostazione del membro <strong>cbVarSegMac</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f60b4-193">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-194">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="f60b4-194">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="f60b4-195">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f60b4-195">Windows XP and later.</span></span> <span data-ttu-id="f60b4-196">Un indice tupla può trovarsi solo in una colonna di tipo text o Unicode.</span><span class="sxs-lookup"><span data-stu-id="f60b4-196">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="f60b4-197">Il tentativo di indicizzare altre colonne, ad esempio colonne binarie, comporterà la JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="f60b4-197">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-198">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="f60b4-198">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="f60b4-199">È stato effettuato un tentativo di creare un indice senza informazioni sulla versione in una transazione.</span><span class="sxs-lookup"><span data-stu-id="f60b4-199">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-200">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="f60b4-200">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="f60b4-201">Il membro <strong>CP</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> non è stato impostato su una tabella codici valida.</span><span class="sxs-lookup"><span data-stu-id="f60b4-201">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="f60b4-202">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="f60b4-202">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="f60b4-203">Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="f60b4-203">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-204">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="f60b4-204">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="f60b4-205">Il membro <strong>coltyp</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> non è stato impostato su un tipo di colonna valido.</span><span class="sxs-lookup"><span data-stu-id="f60b4-205">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-206">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="f60b4-206">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="f60b4-207">Di seguito sono riportati alcuni dei motivi per cui questo errore può verificarsi:</span><span class="sxs-lookup"><span data-stu-id="f60b4-207">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="f60b4-208">Il membro <strong>rgindexcreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su null.</span><span class="sxs-lookup"><span data-stu-id="f60b4-208">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="f60b4-209">Il membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è stato impostato su null.</span><span class="sxs-lookup"><span data-stu-id="f60b4-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="f60b4-210">Il membro <strong>cbStruct</strong> di una struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non è stato impostato su un valore valido.</span><span class="sxs-lookup"><span data-stu-id="f60b4-210">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-211">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="f60b4-211">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="f60b4-212">In <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>è stata specificata una combinazione non valida di membri <strong>grbit</strong> .</span><span class="sxs-lookup"><span data-stu-id="f60b4-212">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="f60b4-213">La definizione dell'indice non è valida perché il membro <strong>grbit</strong> contiene valori incoerenti.</span><span class="sxs-lookup"><span data-stu-id="f60b4-213">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="f60b4-214">Di seguito sono riportate alcune possibili cause:</span><span class="sxs-lookup"><span data-stu-id="f60b4-214">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="f60b4-215">Per un indice primario è stato specificato un bit Ignore (ovvero, JET_bitIndexPrimary è stato passato con JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull o JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="f60b4-215">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="f60b4-216">Un indice vuoto non ignora i membri NULL, ovvero il membro <strong>grbit</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ha JET_bitIndexEmpty impostato, ma non ha JET_bitIndexIgnoreAnyNull set.</span><span class="sxs-lookup"><span data-stu-id="f60b4-216">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="f60b4-217">Passaggio di una struttura di <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> con un membro <strong>grbit</strong> non valido.</span><span class="sxs-lookup"><span data-stu-id="f60b4-217">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-218">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="f60b4-218">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="f60b4-219">È stato passato un ID delle impostazioni locali (LCID) non valido (tramite il membro <strong>LCID</strong> della struttura <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> a cui fa riferimento il membro <strong>pidxunicode</strong> nella struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> o tramite il campo <strong>LCID</strong> della struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span><span class="sxs-lookup"><span data-stu-id="f60b4-219">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-220">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f60b4-220">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f60b4-221">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="f60b4-221">An invalid parameter was given.</span></span> <span data-ttu-id="f60b4-222">Di seguito sono riportate alcune possibili cause:</span><span class="sxs-lookup"><span data-stu-id="f60b4-222">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="f60b4-223">Il membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> è null.</span><span class="sxs-lookup"><span data-stu-id="f60b4-223">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="f60b4-224">Il membro <strong>cbStruct</strong> di una delle strutture <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> fornite nel membro <strong>rgcolumncreate</strong> della struttura <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> non è stato impostato su sizeof (JET_COLUMNCREATE).</span><span class="sxs-lookup"><span data-stu-id="f60b4-224">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="f60b4-225">Il membro <strong>cbKey</strong> di una struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="f60b4-225">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="f60b4-226">Il membro <strong>cbStruct</strong> di una struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> non è impostato su sizeof (JET_INDEXCREATE).</span><span class="sxs-lookup"><span data-stu-id="f60b4-226">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-227">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="f60b4-227">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="f60b4-228">Il record è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="f60b4-228">The record is too big.</span></span> <span data-ttu-id="f60b4-229">La somma del membro <strong>cbMax</strong> della struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> per tutte le colonne fisse non deve superare un determinato valore.</span><span class="sxs-lookup"><span data-stu-id="f60b4-229">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-230">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="f60b4-230">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="f60b4-231">La tabella esiste già.</span><span class="sxs-lookup"><span data-stu-id="f60b4-231">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-232">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="f60b4-232">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="f60b4-233">È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella.</span><span class="sxs-lookup"><span data-stu-id="f60b4-233">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="f60b4-234">Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="f60b4-234">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-235">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="f60b4-235">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="f60b4-236">Si è verificato un errore durante il tentativo di normalizzare una colonna Unicode.</span><span class="sxs-lookup"><span data-stu-id="f60b4-236">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="f60b4-237">Questo problema può essere causato dall'esaurimento delle risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="f60b4-237">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="f60b4-238">Commenti</span><span class="sxs-lookup"><span data-stu-id="f60b4-238">Remarks</span></span>

<span data-ttu-id="f60b4-239">**JetCreateTable** crea una tabella che non contiene colonne.</span><span class="sxs-lookup"><span data-stu-id="f60b4-239">**JetCreateTable** creates a table which does not contain any columns.</span></span> <span data-ttu-id="f60b4-240">Per aggiungere colonne, vedere [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="f60b4-240">To add columns, see [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="f60b4-241">Internamente, **JetCreateTable** chiama [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), compilando una struttura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) con:</span><span class="sxs-lookup"><span data-stu-id="f60b4-241">Internally, **JetCreateTable** calls [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), filling in a [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure with:</span></span>

  - <span data-ttu-id="f60b4-242">JET_TABLECREATE2. cbStruct = sizeof (JET_TABLECREATE2)</span><span class="sxs-lookup"><span data-stu-id="f60b4-242">JET_TABLECREATE2.cbStruct = sizeof( JET_TABLECREATE2 )</span></span>

  - <span data-ttu-id="f60b4-243">JET_TABLECREATE2. szTableName = szTableName</span><span class="sxs-lookup"><span data-stu-id="f60b4-243">JET_TABLECREATE2.szTableName = szTableName</span></span>

  - <span data-ttu-id="f60b4-244">JET_TABLECREATE2. ulPages = lPage</span><span class="sxs-lookup"><span data-stu-id="f60b4-244">JET_TABLECREATE2.ulPages = lPage</span></span>

  - <span data-ttu-id="f60b4-245">JET_TABLECREATE2. ulDensity = lDensity</span><span class="sxs-lookup"><span data-stu-id="f60b4-245">JET_TABLECREATE2.ulDensity = lDensity</span></span>

  - <span data-ttu-id="f60b4-246">JET_TABLECREATE2. TableID = JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="f60b4-246">JET_TABLECREATE2.tableid = JET_tableidNil</span></span>

<span data-ttu-id="f60b4-247">Tutti gli altri campi della struttura [JET_TABLECREATE2](./jet-tablecreate2-structure.md) interna sono impostati su zero o null.</span><span class="sxs-lookup"><span data-stu-id="f60b4-247">All the other fields of the internal [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure are set to zero or NULL.</span></span> <span data-ttu-id="f60b4-248">Nell'output *pTableID* verrà impostato su JET_TABLECREATE2. TableID.</span><span class="sxs-lookup"><span data-stu-id="f60b4-248">On output, *ptableid* will be set to JET_TABLECREATE2.tableid.</span></span>

<span data-ttu-id="f60b4-249">Per ulteriori informazioni, vedere [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="f60b4-249">See [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) for more details.</span></span>

<span data-ttu-id="f60b4-250">Analogamente a [JetOpenTable](./jetopentable-function.md), quando l'applicazione viene eseguita utilizzando il membro **TableID** restituito dalla struttura di [JET_TABLECREATE2](./jet-tablecreate2-structure.md) , è in genere necessario chiuderla con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="f60b4-250">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned **tableid** member from the [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="f60b4-251">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f60b4-251">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-252"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f60b4-252"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f60b4-253">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f60b4-253">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-254"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f60b4-254"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f60b4-255">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f60b4-255">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-256"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="f60b4-256"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f60b4-257">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="f60b4-257">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-258"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="f60b4-258"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f60b4-259">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f60b4-259">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f60b4-260"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f60b4-260"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f60b4-261">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f60b4-261">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f60b4-262"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f60b4-262"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f60b4-263">Implementato come <strong>JetCreateTableW</strong> (Unicode) e <strong>JetCreateTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f60b4-263">Implemented as <strong>JetCreateTableW</strong> (Unicode) and <strong>JetCreateTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f60b4-264">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f60b4-264">See Also</span></span>

[<span data-ttu-id="f60b4-265">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="f60b4-265">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="f60b4-266">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f60b4-266">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f60b4-267">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f60b4-267">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f60b4-268">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f60b4-268">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f60b4-269">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="f60b4-269">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="f60b4-270">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="f60b4-270">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="f60b4-271">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="f60b4-271">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="f60b4-272">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="f60b4-272">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
