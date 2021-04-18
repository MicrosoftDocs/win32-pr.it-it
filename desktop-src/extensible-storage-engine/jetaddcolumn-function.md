---
description: 'Altre informazioni su: funzione JetAddColumn'
title: Funzione JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316457"
---
# <a name="jetaddcolumn-function"></a><span data-ttu-id="3ec49-103">Funzione JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="3ec49-103">JetAddColumn Function</span></span>


<span data-ttu-id="3ec49-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3ec49-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetaddcolumn-function"></a><span data-ttu-id="3ec49-105">Funzione JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="3ec49-105">JetAddColumn Function</span></span>

<span data-ttu-id="3ec49-106">La funzione **JetAddColumn** aggiunge una nuova colonna a una tabella esistente in un database ESE.</span><span class="sxs-lookup"><span data-stu-id="3ec49-106">The **JetAddColumn** function adds a new column to an existing table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="3ec49-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ec49-107">Parameters</span></span>

<span data-ttu-id="3ec49-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3ec49-108">*sesid*</span></span>

<span data-ttu-id="3ec49-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="3ec49-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="3ec49-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="3ec49-110">*tableid*</span></span>

<span data-ttu-id="3ec49-111">Tabella alla quale aggiungere la colonna.</span><span class="sxs-lookup"><span data-stu-id="3ec49-111">The table to which to add the column.</span></span>

<span data-ttu-id="3ec49-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="3ec49-112">*szColumnName*</span></span>

<span data-ttu-id="3ec49-113">Nome della colonna da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="3ec49-113">The name of the column to add.</span></span> <span data-ttu-id="3ec49-114">Il nome deve soddisfare i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ec49-114">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="3ec49-115">Deve avere una lunghezza inferiore a JET_cbNameMost caratteri, escluso il carattere **null** di terminazione.</span><span class="sxs-lookup"><span data-stu-id="3ec49-115">It must be fewer than JET_cbNameMost characters in length, not including the terminating **NULL**.</span></span>

  - <span data-ttu-id="3ec49-116">Deve contenere solo caratteri dei set seguenti: da 0 a 9, da A A Z, da a a z e da tutti gli altri segni di punteggiatura, ad eccezione di punto esclamativo ( \! ), virgola (,), parentesi quadra aperta ( \[ ) e parentesi quadra chiusa ( \] ), ovvero caratteri ASCII 0x20, 0x22 tramite 0x2D, 0x2F tramite 0x5A, 0x5c e 0x5D tramite 0x7F.</span><span class="sxs-lookup"><span data-stu-id="3ec49-116">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="3ec49-117">Non può iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="3ec49-117">It cannot begin with a space.</span></span>

  - <span data-ttu-id="3ec49-118">Deve contenere almeno un carattere diverso dallo spazio.</span><span class="sxs-lookup"><span data-stu-id="3ec49-118">It must contain at least one non-space character.</span></span>

<span data-ttu-id="3ec49-119">*pcolumndef*</span><span class="sxs-lookup"><span data-stu-id="3ec49-119">*pcolumndef*</span></span>

<span data-ttu-id="3ec49-120">Puntatore a una struttura [JET_COLUMNDEF](./jet-columndef-structure.md) , che definisce i dati che possono essere archiviati in una colonna.</span><span class="sxs-lookup"><span data-stu-id="3ec49-120">A pointer to a [JET_COLUMNDEF](./jet-columndef-structure.md) structure, which defines the data that can be stored in a column.</span></span>

<span data-ttu-id="3ec49-121">*pvDefault*</span><span class="sxs-lookup"><span data-stu-id="3ec49-121">*pvDefault*</span></span>

<span data-ttu-id="3ec49-122">Puntatore a un buffer che contiene il valore predefinito per la colonna.</span><span class="sxs-lookup"><span data-stu-id="3ec49-122">A pointer to a buffer that contains the default value for the column.</span></span> <span data-ttu-id="3ec49-123">La lunghezza del buffer è **cbDefault**.</span><span class="sxs-lookup"><span data-stu-id="3ec49-123">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="3ec49-124">Se non è disponibile alcun valore predefinito, impostare **pvDefault** su **null** e **cbDefault** su zero.</span><span class="sxs-lookup"><span data-stu-id="3ec49-124">If there is no default, set **pvDefault** to **NULL** and **cbDefault** to zero.</span></span> <span data-ttu-id="3ec49-125">I valori predefiniti non possono essere maggiori di JET_cbColumnMost byte per le colonne fisse o JET_cbLVDefaultValueMost byte per i valori Long.</span><span class="sxs-lookup"><span data-stu-id="3ec49-125">Default values cannot be larger than JET_cbColumnMost bytes for fixed columns or JET_cbLVDefaultValueMost bytes for long values.</span></span> <span data-ttu-id="3ec49-126">Se un valore predefinito è maggiore, verrà troncato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3ec49-126">If a default value is larger than that, it will be silently truncated.</span></span>

<span data-ttu-id="3ec49-127">Se *grbit* ha JET_bitColumnUserDefinedDefault set, **pvDefault** verrà interpretato come un puntatore a una struttura di [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec49-127">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure.</span></span>

<span data-ttu-id="3ec49-128">*cbDefault*</span><span class="sxs-lookup"><span data-stu-id="3ec49-128">*cbDefault*</span></span>

<span data-ttu-id="3ec49-129">Dimensione, in byte, del buffer specificato in **pvDefault**.</span><span class="sxs-lookup"><span data-stu-id="3ec49-129">The size, in bytes, of the buffer that is specified in **pvDefault**.</span></span>

<span data-ttu-id="3ec49-130">*pColumnID*</span><span class="sxs-lookup"><span data-stu-id="3ec49-130">*pcolumnid*</span></span>

<span data-ttu-id="3ec49-131">Puntatore a una struttura [JET_COLUMNID](./jet-columnid.md) , che, in esito positivo, riceverà l'identificatore della colonna appena creata.</span><span class="sxs-lookup"><span data-stu-id="3ec49-131">A pointer to a [JET_COLUMNID](./jet-columnid.md) structure, which, on success, will receive the identifier of the newly created column.</span></span> <span data-ttu-id="3ec49-132">In caso di errore, il valore non è definito.</span><span class="sxs-lookup"><span data-stu-id="3ec49-132">On failure, the value is undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="3ec49-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ec49-133">Return Value</span></span>

<span data-ttu-id="3ec49-134">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="3ec49-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3ec49-135">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec49-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ec49-136">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3ec49-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="3ec49-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ec49-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3ec49-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3ec49-139">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3ec49-139">The operation was successful.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-140">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="3ec49-140">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="3ec49-141">È stato effettuato un tentativo di modificare la definizione dei dati di una tabella DDL fissa.</span><span class="sxs-lookup"><span data-stu-id="3ec49-141">An attempt was made to modify the data definition of a fixed DDL table.</span></span> <span data-ttu-id="3ec49-142">Un esempio di tabella con DDL fisso è una tabella modello.</span><span class="sxs-lookup"><span data-stu-id="3ec49-142">An example of a table with fixed DDL is a Template Table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3ec49-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3ec49-144">Un parametro non valido è stato passato nell'API.</span><span class="sxs-lookup"><span data-stu-id="3ec49-144">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="3ec49-145">Alcuni esempi di parametri non validi sono:</span><span class="sxs-lookup"><span data-stu-id="3ec49-145">Some examples of invalid parameters are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3ec49-146">Il passaggio della dimensione non corretta della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> nel membro <em>cbStruct</em> .</span><span class="sxs-lookup"><span data-stu-id="3ec49-146">Passing in the wrong size of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure in its <em>cbStruct</em> member.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-147">Passando JET_bitColumnUserDefinedDefault, ma non impostando <strong>cbDefault</strong> su sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="3ec49-147">Passing in JET_bitColumnUserDefinedDefault, but not setting <strong>cbDefault</strong> to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-148">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="3ec49-148">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="3ec49-149">È stato effettuato un tentativo di aggiungere una colonna con il bit JET_bitColumnUnversioned set, ma la sessione è attualmente in una transazione.</span><span class="sxs-lookup"><span data-stu-id="3ec49-149">An attempt was made to add a column with the JET_bitColumnUnversioned bit set, but the session is currently in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-150">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="3ec49-150">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="3ec49-151">Una colonna esiste già.</span><span class="sxs-lookup"><span data-stu-id="3ec49-151">A column already exists.</span></span> <span data-ttu-id="3ec49-152">È stato effettuato un tentativo di aggiungere una colonna senza informazioni sulla versione e tale colonna esiste già.</span><span class="sxs-lookup"><span data-stu-id="3ec49-152">An attempt was made to add a column without version information, and that column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-153">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="3ec49-153">JET_errTableNotEmpty</span></span></p></td>
<td><p><span data-ttu-id="3ec49-154">La tabella contiene dati.</span><span class="sxs-lookup"><span data-stu-id="3ec49-154">The table contains data.</span></span> <span data-ttu-id="3ec49-155">Una colonna di aggiornamento del deposito può essere aggiunta solo a una tabella vuota.</span><span class="sxs-lookup"><span data-stu-id="3ec49-155">An Escrow Update column can only be added to an empty table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-156">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="3ec49-156">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="3ec49-157">Il record è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="3ec49-157">The record is too big.</span></span> <span data-ttu-id="3ec49-158">La somma del parametro <strong>cbMax</strong> per le colonne fisse non deve superare un determinato valore.</span><span class="sxs-lookup"><span data-stu-id="3ec49-158">The sum of the <strong>cbMax</strong> parameter for the fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-159">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="3ec49-159">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="3ec49-160">È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella.</span><span class="sxs-lookup"><span data-stu-id="3ec49-160">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="3ec49-161">Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="3ec49-161">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-162">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="3ec49-162">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="3ec49-163">È stato effettuato un tentativo di aggiungere una colonna ridondante.</span><span class="sxs-lookup"><span data-stu-id="3ec49-163">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="3ec49-164">Non deve essere presente più di una colonna AutoIncrement e non più di una colonna versione per tabella.</span><span class="sxs-lookup"><span data-stu-id="3ec49-164">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-165">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="3ec49-165">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="3ec49-166">Non è stato possibile risolvere la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="3ec49-166">The callback function could not be resolved.</span></span> <span data-ttu-id="3ec49-167">È possibile che la DLL non sia stata trovata o che la funzione nella DLL non sia stata trovata.</span><span class="sxs-lookup"><span data-stu-id="3ec49-167">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="3ec49-168">Se è abilitata la registrazione sufficiente, nel registro eventi vengono forniti ulteriori dettagli.</span><span class="sxs-lookup"><span data-stu-id="3ec49-168">The event log will provide more details if sufficient logging is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="3ec49-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="3ec49-170">Avviso che indica che la lunghezza massima (<strong>cbMax</strong>) di una colonna fissa o variabile è maggiore della JET_cbColumnMost.</span><span class="sxs-lookup"><span data-stu-id="3ec49-170">A warning indicating that the maximum length (<strong>cbMax</strong>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="3ec49-171">Questo limite non si applica ai valori Long (ovvero <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> e <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="3ec49-171">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-172">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="3ec49-172">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="3ec49-173">Un nome non valido è stato passato come <strong>szColumnName</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec49-173">An invalid name was passed as <strong>szColumnName</strong>.</span></span> <span data-ttu-id="3ec49-174">Per ulteriori informazioni sulle restrizioni, vedere i criteri per <strong>szColumnName</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec49-174">For more information about the restrictions, see the criteria for <strong>szColumnName</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-175">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="3ec49-175">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="3ec49-176">Il campo <strong>coltyp</strong> non è stato impostato su un tipo di colonna valido.</span><span class="sxs-lookup"><span data-stu-id="3ec49-176">The <strong>coltyp</strong> field was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-177">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="3ec49-177">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="3ec49-178">Il parametro <strong>CP</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida.</span><span class="sxs-lookup"><span data-stu-id="3ec49-178">The <strong>cp</strong> parameter of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="3ec49-179">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="3ec49-179">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="3ec49-180">Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="3ec49-180">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-181">JET_errTaggedNotNULL</span><span class="sxs-lookup"><span data-stu-id="3ec49-181">JET_errTaggedNotNULL</span></span></p></td>
<td><p><span data-ttu-id="3ec49-182">Non è possibile usare JET_bitColumnNotNULL con colonne con tag, Long Value o SLV.</span><span class="sxs-lookup"><span data-stu-id="3ec49-182">JET_bitColumnNotNULL cannot be used with tagged, Long Value, or SLV columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-183">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="3ec49-183">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="3ec49-184">È stata specificata una combinazione non valida di <em>grbits</em> .</span><span class="sxs-lookup"><span data-stu-id="3ec49-184">An invalid combination of <em>grbits</em> was specified.</span></span> <span data-ttu-id="3ec49-185">Di seguito sono riportati alcuni dei motivi di questo errore:</span><span class="sxs-lookup"><span data-stu-id="3ec49-185">Some of the reasons for this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3ec49-186">JET_bitColumnFixed è stato utilizzato in una colonna con tag, Long Value o SLV.</span><span class="sxs-lookup"><span data-stu-id="3ec49-186">JET_bitColumnFixed was used on a tagged, Long Value, or SLV column.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-187">JET_bitColumnEscrowUpdate è stato utilizzato in una colonna non di tipo <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec49-187">JET_bitColumnEscrowUpdate was used on a column that was not of type <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-188">JET_bitColumnEscrowUpdate è stato utilizzato in una colonna versione (JET_bitColumnVersion).</span><span class="sxs-lookup"><span data-stu-id="3ec49-188">JET_bitColumnEscrowUpdate was used on a Version column (JET_bitColumnVersion).</span></span></p></li>
<li><p><span data-ttu-id="3ec49-189">JET_bitColumnEscrowUpdate è stato usato in una colonna AutoIncrememnt (JET_bitColumnAutoincrement).</span><span class="sxs-lookup"><span data-stu-id="3ec49-189">JET_bitColumnEscrowUpdate was used on an AutoIncrememnt column (JET_bitColumnAutoincrement).</span></span></p></li>
<li><p><span data-ttu-id="3ec49-190">JET_bitColumnEscrowUpdate è stato utilizzato in una colonna che non disponeva di un valore predefinito (<strong>cbDefault</strong> era uguale a zero).</span><span class="sxs-lookup"><span data-stu-id="3ec49-190">JET_bitColumnEscrowUpdate was used on a column that did not have a default value (<strong>cbDefault</strong> was equal to zero).</span></span></p></li>
<li><p><span data-ttu-id="3ec49-191">JET_bitColumnFinalize è stato utilizzato in una colonna che non è una colonna di aggiornamento del deposito (JET_bitColumnEscrowUpdate non è stato impostato).</span><span class="sxs-lookup"><span data-stu-id="3ec49-191">JET_bitColumnFinalize was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="3ec49-192">JET_bitColumnDeleteOnZero è stato utilizzato in una colonna che non è una colonna di aggiornamento del deposito (JET_bitColumnEscrowUpdate non è stato impostato).</span><span class="sxs-lookup"><span data-stu-id="3ec49-192">JET_bitColumnDeleteOnZero was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="3ec49-193">JET_bitColumnAutoincrement è stato utilizzato in una colonna che non è stata <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec49-193">JET_bitColumnAutoincrement was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p>
<p><span data-ttu-id="3ec49-194"><strong>Windows 2000:  </strong> Questo motivo del codice di errore viene usato solo in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3ec49-194"><strong>Windows 2000:  </strong>This reason for the error code is used only in Windows 2000.</span></span></p>
<p><span data-ttu-id="3ec49-195">JET_bitColumnAutoincrement è stato utilizzato in una colonna non <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> né <a href="gg269213(v=exchg.10).md">JET_coltypCurrencyta</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec49-195">JET_bitColumnAutoincrement was used on a column that was neither <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> nor <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span></span></p>
<p><span data-ttu-id="3ec49-196"><strong>Windows XP:  </strong> Questo motivo del codice di errore viene utilizzato in Windows XP e nei sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="3ec49-196"><strong>Windows XP:  </strong>This reason for the error code is used in Windows XP and later operating systems.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-197">JET_bitColumnVersion è stato utilizzato in una colonna che non è stata <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="3ec49-197">JET_bitColumnVersion was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-198">JET_bitColumnVersion è stato utilizzato in una colonna AutoIncrement.</span><span class="sxs-lookup"><span data-stu-id="3ec49-198">JET_bitColumnVersion was used on an autoincrement column.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-199">JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="3ec49-199">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFixed.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-200">JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnNotNULL.</span><span class="sxs-lookup"><span data-stu-id="3ec49-200">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnNotNULL.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-201">JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnVersion.</span><span class="sxs-lookup"><span data-stu-id="3ec49-201">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnVersion.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-202">JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="3ec49-202">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnAutoincrement.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-203">JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnUpdatable.</span><span class="sxs-lookup"><span data-stu-id="3ec49-203">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnUpdatable.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-204">JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="3ec49-204">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnEscrowUpdate.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-205">JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="3ec49-205">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFinalize.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-206">JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="3ec49-206">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnDeleteOnZero.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-207">JET_bitColumnUserDefinedDefault utilizzata insieme a JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="3ec49-207">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnMaybeNull.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-208">JET_bitColumnUserDefinedDefault è stato utilizzato in una colonna non contrassegnata (che è fissa o variabile).</span><span class="sxs-lookup"><span data-stu-id="3ec49-208">JET_bitColumnUserDefinedDefault was used on a non-tagged column (that is fixed or variable).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-209">JET_errMultiValuedColumnMustBeTagged</span><span class="sxs-lookup"><span data-stu-id="3ec49-209">JET_errMultiValuedColumnMustBeTagged</span></span></p></td>
<td><p><span data-ttu-id="3ec49-210">Una colonna multivalore (JET_bitColumnMultiValued) può essere utilizzata solo in una colonna con tag o valori Long (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="3ec49-210">A multi-valued column (JET_bitColumnMultiValued) can only be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-211">JET_errCannotBeTagged</span><span class="sxs-lookup"><span data-stu-id="3ec49-211">JET_errCannotBeTagged</span></span></p></td>
<td><p><span data-ttu-id="3ec49-212">Si è tentato di usare una colonna con tag quando è possibile che la colonna non sia contrassegnata con tag.</span><span class="sxs-lookup"><span data-stu-id="3ec49-212">An attempt was made to use a tagged column when the column might not be tagged.</span></span> <span data-ttu-id="3ec49-213">Alcuni dei vincoli per la disabilitazione delle colonne con tag sono:</span><span class="sxs-lookup"><span data-stu-id="3ec49-213">Some of the constraints for disallowing tagged columns are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3ec49-214">Una colonna di aggiornamento del deposito (JET_bitColumnEscrowUpdate) non può essere usata in una colonna con tag o valori Long (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="3ec49-214">An Escrow Update column (JET_bitColumnEscrowUpdate) cannot be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-215">Una colonna AutoIncrement potrebbe non essere contrassegnata con tag.</span><span class="sxs-lookup"><span data-stu-id="3ec49-215">An autoincrement column might not be tagged.</span></span></p></li>
<li><p><span data-ttu-id="3ec49-216">Una colonna versione potrebbe non essere contrassegnata con tag.</span><span class="sxs-lookup"><span data-stu-id="3ec49-216">A Version column might not be tagged.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-217">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="3ec49-217">JET_errExclusiveTableLockRequired</span></span></p></td>
<td><p><span data-ttu-id="3ec49-218">Per questa operazione è necessario un blocco esclusivo sulla tabella.</span><span class="sxs-lookup"><span data-stu-id="3ec49-218">An exclusive lock on the table was required for this operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-219">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="3ec49-219">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="3ec49-220">Avviso che indica che la lunghezza massima (<em>cbMax</em>) di una colonna fissa o variabile è maggiore della JET_cbColumnMost.</span><span class="sxs-lookup"><span data-stu-id="3ec49-220">A warning indicating that the maximum length (<em>cbMax</em>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="3ec49-221">Questo limite non si applica ai valori Long (ovvero <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> e <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="3ec49-221">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="3ec49-222">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ec49-222">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-223"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3ec49-223"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3ec49-224">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3ec49-224">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-225"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3ec49-225"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3ec49-226">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3ec49-226">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-227"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="3ec49-227"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3ec49-228">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="3ec49-228">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-229"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="3ec49-229"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3ec49-230">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3ec49-230">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec49-231"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3ec49-231"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3ec49-232">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3ec49-232">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec49-233"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="3ec49-233"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="3ec49-234">Implementato come <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="3ec49-234">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3ec49-235">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3ec49-235">See Also</span></span>

[<span data-ttu-id="3ec49-236">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="3ec49-236">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="3ec49-237">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="3ec49-237">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="3ec49-238">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="3ec49-238">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="3ec49-239">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="3ec49-239">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="3ec49-240">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3ec49-240">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3ec49-241">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3ec49-241">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3ec49-242">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3ec49-242">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3ec49-243">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3ec49-243">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3ec49-244">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="3ec49-244">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="3ec49-245">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="3ec49-245">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
