---
description: 'Altre informazioni su: funzione JetOpenTemporaryTable'
title: JetOpenTemporaryTable (funzione)
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315620"
---
# <a name="jetopentemporarytable-function"></a><span data-ttu-id="18df8-103">JetOpenTemporaryTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="18df8-103">JetOpenTemporaryTable Function</span></span>


<span data-ttu-id="18df8-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="18df8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemporarytable-function"></a><span data-ttu-id="18df8-105">JetOpenTemporaryTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="18df8-105">JetOpenTemporaryTable Function</span></span>

<span data-ttu-id="18df8-106">La funzione **JetOpenTemporaryTable** crea una tabella volatile con un solo indice che può essere usato per archiviare e recuperare record, proprio come una tabella ordinaria creata tramite [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="18df8-106">The **JetOpenTemporaryTable** function creates a volatile table with a single index that can be used to store and retrieve records, just like an ordinary table that is created via [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span>

<span data-ttu-id="18df8-107">**Windows Vista:**  **JetOpenTemporaryTable** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="18df8-107">**Windows Vista:**  **JetOpenTemporaryTable** is introduced in Windows Vista.</span></span>

<span data-ttu-id="18df8-108">Le tabelle temporanee sono più veloci delle tabelle ordinarie a causa della loro natura volatile.</span><span class="sxs-lookup"><span data-stu-id="18df8-108">Temporary tables are faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="18df8-109">Possono ordinare ed eseguire rapidamente la rimozione dei duplicati nei set di record quando sono accessibili in modo puramente sequenziale.</span><span class="sxs-lookup"><span data-stu-id="18df8-109">They can quickly sort and perform duplicate removal on record sets when they are accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a><span data-ttu-id="18df8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="18df8-110">Parameters</span></span>

<span data-ttu-id="18df8-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="18df8-111">*sesid*</span></span>

<span data-ttu-id="18df8-112">Sessione che verrà utilizzata per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="18df8-112">The session that will be used for this call.</span></span>

<span data-ttu-id="18df8-113">*popentemporarytable*</span><span class="sxs-lookup"><span data-stu-id="18df8-113">*popentemporarytable*</span></span>

<span data-ttu-id="18df8-114">Puntatore a una struttura [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) contenente la descrizione della tabella temporanea da creare in input.</span><span class="sxs-lookup"><span data-stu-id="18df8-114">A pointer to a [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) structure that contains the description of the temporary table to create on input.</span></span> <span data-ttu-id="18df8-115">Dopo una chiamata con esito positivo, la struttura contiene l'handle per gli identificatori di tabella e colonna temporanei.</span><span class="sxs-lookup"><span data-stu-id="18df8-115">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span>

### <a name="return-value"></a><span data-ttu-id="18df8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18df8-116">Return Value</span></span>

<span data-ttu-id="18df8-117">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="18df8-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="18df8-118">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="18df8-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18df8-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="18df8-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="18df8-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18df8-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18df8-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="18df8-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="18df8-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="18df8-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-123">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="18df8-123">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="18df8-124">L'operazione non è riuscita perché non è stato possibile allocare memoria sufficiente per il completamento.</span><span class="sxs-lookup"><span data-stu-id="18df8-124">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="18df8-125"><strong>JetOpenTemporaryTable</strong> può restituire JET_errOutOfMemory se lo spazio degli indirizzi del processo host diventa troppo frammentato.</span><span class="sxs-lookup"><span data-stu-id="18df8-125"><strong>JetOpenTemporaryTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="18df8-126">Il gestore tabelle temporanee allocherà un blocco di spazio degli indirizzi di 1 MB per ogni tabella temporanea creata indipendentemente dalla quantità di dati archiviati.</span><span class="sxs-lookup"><span data-stu-id="18df8-126">The temporary table manager will allocates a 1 MB chunk of address space for every temporary table created regardless of the amount of data is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="18df8-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="18df8-128">Uno dei parametri specificati contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</span><span class="sxs-lookup"><span data-stu-id="18df8-128">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="18df8-129">Questo errore viene restituito da <strong>JetOpenTemporaryTable</strong> nelle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="18df8-129">This error is returned by <strong>JetOpenTemporaryTable</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="18df8-130">Il membro <strong>cbStruct</strong> della struttura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> non corrisponde a una versione di questa struttura supportata da tale versione del motore di database</span><span class="sxs-lookup"><span data-stu-id="18df8-130">The <strong>cbStruct</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure does not correspond to a version of this structure that is supported by that version of the database engine</span></span></p></li>
<li><p><span data-ttu-id="18df8-131">Il membro <strong>cbKeyMost</strong> della struttura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> è minore di JET_cbKeyMostMin.</span><span class="sxs-lookup"><span data-stu-id="18df8-131">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is less than JET_cbKeyMostMin.</span></span></p></li>
<li><p><span data-ttu-id="18df8-132">Il membro <strong>cbKeyMost</strong> della struttura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> è più grande del valore supportato più grande per le dimensioni della pagina del database per l'istanza (JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="18df8-132">The <strong>cbKeyMost</strong> member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than the largest supported value for the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="18df8-133">Per ulteriori informazioni, vedere il parametro JET_paramKeyMost nell'elenco dei <a href="gg269241(v=exchg.10).md">parametri informativi</a> .</span><span class="sxs-lookup"><span data-stu-id="18df8-133">See the JET_paramKeyMost parameter in the list of <a href="gg269241(v=exchg.10).md">Informational Parameters</a> for more information.</span></span></p></li>
<li><p><span data-ttu-id="18df8-134">Il membro cbVarSegMac della struttura <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> è più grande del membro <strong>cbKeyMost</strong> .</span><span class="sxs-lookup"><span data-stu-id="18df8-134">The cbVarSegMac member of the <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> structure is larger than The <strong>cbKeyMost</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="18df8-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="18df8-136">Non è possibile completare l'operazione perché l'istanza di associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="18df8-136">The operation cannot complete because the instance that was associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="18df8-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="18df8-138">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="18df8-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="18df8-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="18df8-140">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="18df8-140">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="18df8-141"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="18df8-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="18df8-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="18df8-143">Non è possibile completare l'operazione perché è in corso l'arresto dell'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="18df8-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="18df8-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="18df8-145">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino nell'istanza di associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="18df8-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="18df8-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="18df8-147">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="18df8-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="18df8-148"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="18df8-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-149">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="18df8-149">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="18df8-150">L'handle di sessione non è valido o fa riferimento a una sessione chiusa.</span><span class="sxs-lookup"><span data-stu-id="18df8-150">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="18df8-151"><strong>Nota</strong>  Questo errore non viene restituito in tutte le circostanze.</span><span class="sxs-lookup"><span data-stu-id="18df8-151"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="18df8-152">Gli handle vengono convalidati solo in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="18df8-152">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-153">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="18df8-153">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="18df8-154">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per aprire un nuovo cursore.</span><span class="sxs-lookup"><span data-stu-id="18df8-154">The operation failed because the engine cannot allocate the resources that are required to open a new cursor.</span></span> <span data-ttu-id="18df8-155">Le risorse del cursore vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="18df8-155">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-156">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="18df8-156">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="18df8-157">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per creare una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="18df8-157">The operation failed because the engine cannot allocate the resources that are required to create a temporary table.</span></span> <span data-ttu-id="18df8-158">Le risorse della tabella temporanea vengono configurate utilizzando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span><span class="sxs-lookup"><span data-stu-id="18df8-158">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-159">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="18df8-159">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="18df8-160"><strong>JetOpenTemporaryTable</strong> non riuscito perché è stato specificato JET_bitTTForwardOnly e non è stato possibile creare la tabella temporanea specificata con l'ottimizzazione di sola trasmissione.</span><span class="sxs-lookup"><span data-stu-id="18df8-160"><strong>JetOpenTemporaryTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table that was specified could not be created using the forward-only optimization.</span></span></p>
<p><span data-ttu-id="18df8-161"><strong>Windows Server 2003:</strong>  Questo errore verrà restituito solo da Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="18df8-161"><strong>Windows Server 2003:</strong>  This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-162">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="18df8-162">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="18df8-163">È stato effettuato un tentativo di aggiungere un numero eccessivo di colonne alla tabella.</span><span class="sxs-lookup"><span data-stu-id="18df8-163">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="18df8-164">Una tabella non può contenere più di JET_ccolFixedMost colonne fisse, non più di JET_ccolVarMost colonne a lunghezza variabile e non più di JET_ccolTaggedMost colonne con tag.</span><span class="sxs-lookup"><span data-stu-id="18df8-164">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-165">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="18df8-165">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="18df8-166">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache lo schema della tabella.</span><span class="sxs-lookup"><span data-stu-id="18df8-166">The operation failed because the engine cannot allocate the resources that are required to cache the schema of the table.</span></span> <span data-ttu-id="18df8-167">Per configurare il numero di tabelle che contengono schemi che possono essere memorizzati nella cache, utilizzare <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="18df8-167">To configure the number of tables that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-168">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="18df8-168">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="18df8-169">Il membro <strong>CP</strong> della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su una tabella codici valida.</span><span class="sxs-lookup"><span data-stu-id="18df8-169">The <strong>cp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="18df8-170">Gli unici valori validi per le colonne di testo sono English (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="18df8-170">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="18df8-171">Il valore 0 indica che verrà utilizzata l'impostazione predefinita (inglese, 1252).</span><span class="sxs-lookup"><span data-stu-id="18df8-171">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-172">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="18df8-172">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="18df8-173">Il membro <strong>coltyp</strong> del <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> non è stato impostato su un tipo di colonna valido.</span><span class="sxs-lookup"><span data-stu-id="18df8-173">The <strong>coltyp</strong> member of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-174">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="18df8-174">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="18df8-175">Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un ID delle impostazioni locali non valido.</span><span class="sxs-lookup"><span data-stu-id="18df8-175">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="18df8-176">È possibile che l'ID delle impostazioni locali sia completamente non valido o che il Language Pack associato non sia installato.</span><span class="sxs-lookup"><span data-stu-id="18df8-176">The locale ID might be either completely invalid or the associated language pack might not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-177">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="18df8-177">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="18df8-178">Impossibile creare l'indice perché è stato effettuato un tentativo di utilizzare un set di flag di normalizzazione non valido.</span><span class="sxs-lookup"><span data-stu-id="18df8-178">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span></p>
<p><span data-ttu-id="18df8-179"><strong>Windows XP:</strong>  Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="18df8-179"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p>
<p><span data-ttu-id="18df8-180"><strong>Windows 2000:</strong>  In Windows 2000, i flag di normalizzazione non validi determineranno JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="18df8-180"><strong>Windows 2000:</strong>  On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-181">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="18df8-181">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="18df8-182">Impossibile creare l'indice perché è stata specificata una definizione di indice non valida.</span><span class="sxs-lookup"><span data-stu-id="18df8-182">The index could not be created because an invalid index definition was specified.</span></span> <span data-ttu-id="18df8-183"><strong>JetOpenTemporaryTable</strong> restituirà questo errore nelle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="18df8-183"><strong>JetOpenTemporaryTable</strong> will return this error under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="18df8-184">Le impostazioni locali indipendenti dalla lingua sono specificate.</span><span class="sxs-lookup"><span data-stu-id="18df8-184">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="18df8-185">È stato specificato un set di flag di normalizzazione non valido.</span><span class="sxs-lookup"><span data-stu-id="18df8-185">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="18df8-186"><strong>Windows 2000:</strong>  Questo errore verrà restituito solo da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="18df8-186"><strong>Windows 2000:</strong>  This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-187">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="18df8-187">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="18df8-188">L'operazione non è riuscita perché il motore non è in grado di allocare le risorse necessarie per memorizzare nella cache gli indici della tabella.</span><span class="sxs-lookup"><span data-stu-id="18df8-188">The operation failed because the engine cannot allocate the resources that are required to cache the indexes of the table.</span></span> <span data-ttu-id="18df8-189">Per configurare il numero di indici con schemi che possono essere memorizzati nella cache, utilizzare <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span><span class="sxs-lookup"><span data-stu-id="18df8-189">To configure the number of indexes that have schemas that can be cached, use <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18df8-190">In seguito all'esito positivo, verrà restituito un cursore aperto nella tabella temporanea appena creata.</span><span class="sxs-lookup"><span data-stu-id="18df8-190">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="18df8-191">Lo stato del database temporaneo sarà pronto per contenere la nuova tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="18df8-191">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="18df8-192">Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="18df8-192">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="18df8-193">In caso di errore, la tabella temporanea non verrà creata e non verrà restituito un cursore.</span><span class="sxs-lookup"><span data-stu-id="18df8-193">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="18df8-194">Lo stato del database temporaneo può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="18df8-194">The state of the temporary database can be changed.</span></span> <span data-ttu-id="18df8-195">Lo stato di qualsiasi database normale utilizzato dal motore di database rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="18df8-195">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="18df8-196">Commenti</span><span class="sxs-lookup"><span data-stu-id="18df8-196">Remarks</span></span>

<span data-ttu-id="18df8-197">Le tabelle temporanee non supportano il complemento completo delle opzioni di definizione di colonna normalmente supportate dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="18df8-197">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="18df8-198">In realtà, sono supportati solo JET_bitColumnFixed e JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="18df8-198">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="18df8-199">Ciò significa che non è possibile creare un incremento automatico, una versione o una colonna multivalore in una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="18df8-199">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="18df8-200">Infine, le colonne di aggiornamento del deposito a garanzia non sono supportate perché possono essere utilizzate solo da una sessione alla volta.</span><span class="sxs-lookup"><span data-stu-id="18df8-200">Finally, escrow update columns are not supported because they can only be used by one session at a time.</span></span> <span data-ttu-id="18df8-201">Se viene richiesta una qualsiasi di queste opzioni, queste verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="18df8-201">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="18df8-202">Le tabelle temporanee non supportano i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="18df8-202">Temporary tables do not support default values.</span></span> <span data-ttu-id="18df8-203">Se viene fornita una definizione di colonna contenente una specifica del valore predefinito, tale specifica verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="18df8-203">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="18df8-204">Le tabelle temporanee vengono restituite al chiamante in seguito a numerose funzioni ESE diverse.</span><span class="sxs-lookup"><span data-stu-id="18df8-204">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="18df8-205">Ad esempio, [JetGetIndexInfo](./jetgetindexinfo-function.md) con il set di opzioni JET_IdxInfo restituirà una tabella temporanea contenente un elenco di tutte le colonne chiave di un indice specificato.</span><span class="sxs-lookup"><span data-stu-id="18df8-205">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="18df8-206">Le tabelle temporanee seguono le stesse regole del ciclo di vita delle tabelle temporanee comuni, come descritto qui.</span><span class="sxs-lookup"><span data-stu-id="18df8-206">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="18df8-207">Le tabelle temporanee vengono inoltre utilizzate internamente dal motore di database per molte attività.</span><span class="sxs-lookup"><span data-stu-id="18df8-207">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="18df8-208">La più importante di queste attività è la creazione di un indice su una tabella esistente.</span><span class="sxs-lookup"><span data-stu-id="18df8-208">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="18df8-209">Una tabella temporanea verrà utilizzata per ordinare le chiavi di indice utilizzate per costruire tale indice.</span><span class="sxs-lookup"><span data-stu-id="18df8-209">A temporary table will be used to sort the index keys that are used to construct that index.</span></span>

<span data-ttu-id="18df8-210">Tutte le tabelle temporanee vengono archiviate nel database temporaneo.</span><span class="sxs-lookup"><span data-stu-id="18df8-210">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="18df8-211">Il database temporaneo è un file di database speciale mantenuto durante la durata di un'istanza ESE e viene eliminato quando l'istanza viene arrestata o riavviata.</span><span class="sxs-lookup"><span data-stu-id="18df8-211">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="18df8-212">Il percorso del database temporaneo può essere configurato tramite [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="18df8-212">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="18df8-213">La posizione del database temporaneo su disco rispetto ai file di log delle transazioni e dei file di database può essere importante se l'applicazione usa in modo intensivo le tabelle temporanee o crea gli indici di frequente.</span><span class="sxs-lookup"><span data-stu-id="18df8-213">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="18df8-214">Il ciclo di vita di una tabella temporanea è associato ai cursori che vi fanno riferimento.</span><span class="sxs-lookup"><span data-stu-id="18df8-214">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="18df8-215">Se tutti i cursori che fanno riferimento a una tabella temporanea sono chiusi, in modo implicito o esplicito, la tabella temporanea verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="18df8-215">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="18df8-216">Se una tabella temporanea viene creata all'interno di una transazione e successivamente viene eseguito il rollback della transazione, la tabella temporanea verrà eliminata perché i cursori che vi fanno riferimento in questo momento verranno chiusi in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="18df8-216">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="18df8-217">I nuovi cursori possono fare riferimento a una tabella temporanea solo tramite l'uso di [JetDupCursor](./jetdupcursor-function.md).</span><span class="sxs-lookup"><span data-stu-id="18df8-217">New cursors can reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="18df8-218">In questo caso, i nuovi cursori verranno posizionati sulla prima voce di indice della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="18df8-218">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="18df8-219">[JetDupCursor](./jetdupcursor-function.md) funzionerà solo durante determinate fasi di utilizzo della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="18df8-219">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="18df8-220">Per ulteriori informazioni, vedere le osservazioni relative alle funzionalità del cursore della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="18df8-220">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="18df8-221">Non è possibile fare riferimento a una tabella temporanea da più di una sessione alla volta.</span><span class="sxs-lookup"><span data-stu-id="18df8-221">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="18df8-222">**Attenzione**  Si è verificato un problema importante in [JetDupCursor](./jetdupcursor-function.md) che influiscono sulle tabelle temporanee.</span><span class="sxs-lookup"><span data-stu-id="18df8-222">**Caution**  There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="18df8-223">Se viene effettuato un tentativo di duplicare una tabella temporanea in modalità di sola trasmissione, il cursore risultante non verrà creato correttamente e non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="18df8-223">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="18df8-224">È comunque possibile duplicare un cursore su una tabella temporanea materializzata.</span><span class="sxs-lookup"><span data-stu-id="18df8-224">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="18df8-225">Il gestore tabelle temporaneo può implementare una tabella temporanea in tre modi.</span><span class="sxs-lookup"><span data-stu-id="18df8-225">The temporary table manager can implement a temporary table in three ways.</span></span> <span data-ttu-id="18df8-226">Il primo metodo consiste nel mantenere una tabella in memoria.</span><span class="sxs-lookup"><span data-stu-id="18df8-226">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="18df8-227">Questa strategia è la più veloce, ma può essere usata solo per le tabelle temporanee di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="18df8-227">This strategy is the fastest but can only be used for small, simple, temporary tables.</span></span> <span data-ttu-id="18df8-228">Il secondo metodo consiste nel creare un ordinamento basato su disco che può essere guidato utilizzando un iteratore di tipo "solo".</span><span class="sxs-lookup"><span data-stu-id="18df8-228">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="18df8-229">Questa strategia può essere utilizzata solo in determinate circostanze ed è il modo più rapido per ordinare e rimuovere i duplicati da un set di dati di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="18df8-229">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="18df8-230">Il terzo metodo consiste nel creare un albero B + nel database temporaneo che contenga la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="18df8-230">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="18df8-231">Questa strategia è la più lenta, ma la più versatile, ed è definita tabella temporanea materializzata.</span><span class="sxs-lookup"><span data-stu-id="18df8-231">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="18df8-232">Queste strategie possono essere usate in combinazione per ottenere in definitiva la funzionalità richiesta della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="18df8-232">These strategies can be used in combination to ultimately achieve the functionality that is requested of the temporary table.</span></span>

<span data-ttu-id="18df8-233">Quando la tabella temporanea non viene materializzata, viene utilizzata principalmente in due fasi principali.</span><span class="sxs-lookup"><span data-stu-id="18df8-233">When the temporary table is not materialized then it is used primarily in two major phases.</span></span> <span data-ttu-id="18df8-234">La prima fase è la fase di inserimento in cui la tabella viene popolata con il set di dati iniziale.</span><span class="sxs-lookup"><span data-stu-id="18df8-234">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="18df8-235">Durante questa fase, è consentito solo l'inserimento di dati.</span><span class="sxs-lookup"><span data-stu-id="18df8-235">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="18df8-236">Questa fase termina quando viene effettuato un tentativo di spostare il cursore utilizzando [JetMove](./jetmove-function.md) o [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="18df8-236">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="18df8-237">La seconda fase è la fase di estrazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="18df8-237">The second phase is the data extraction phase.</span></span> <span data-ttu-id="18df8-238">Durante questa fase, i dati archiviati nella tabella temporanea possono essere estratti in base alle funzionalità richieste durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="18df8-238">During this phase, the data that is stored in the temporary table can be extracted according to the capabilities that were requested when the temporary table was created.</span></span>

<span data-ttu-id="18df8-239">**Funzionalità del cursore tabella temporanea**</span><span class="sxs-lookup"><span data-stu-id="18df8-239">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="18df8-240">Quando la tabella temporanea viene materializzata, il cursore presenta le funzionalità seguenti, ma potrebbe essere ulteriormente limitato dalle opzioni richieste:</span><span class="sxs-lookup"><span data-stu-id="18df8-240">When the temporary table is materialized, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="18df8-241">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="18df8-241">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="18df8-242">JetDelete</span><span class="sxs-lookup"><span data-stu-id="18df8-242">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="18df8-243">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="18df8-243">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="18df8-244">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="18df8-244">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="18df8-245">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="18df8-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="18df8-246">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="18df8-246">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="18df8-247">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="18df8-247">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="18df8-248">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="18df8-248">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="18df8-249">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="18df8-249">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="18df8-250">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="18df8-250">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="18df8-251">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="18df8-251">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="18df8-252">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="18df8-252">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="18df8-253">JetMove</span><span class="sxs-lookup"><span data-stu-id="18df8-253">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="18df8-254">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="18df8-254">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="18df8-255">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="18df8-255">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="18df8-256">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="18df8-256">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="18df8-257">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="18df8-257">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="18df8-258">JetSeek</span><span class="sxs-lookup"><span data-stu-id="18df8-258">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="18df8-259">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="18df8-259">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="18df8-260">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="18df8-260">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="18df8-261">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="18df8-261">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="18df8-262">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="18df8-262">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="18df8-263">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="18df8-263">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="18df8-264">Quando la tabella temporanea non viene materializzata e si trova nella fase di inserimento, il cursore presenta le funzionalità seguenti, ma potrebbe essere ulteriormente limitato dalle opzioni richieste:</span><span class="sxs-lookup"><span data-stu-id="18df8-264">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but might be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="18df8-265">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="18df8-265">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="18df8-266">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="18df8-266">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="18df8-267">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="18df8-267">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="18df8-268">JetMove</span><span class="sxs-lookup"><span data-stu-id="18df8-268">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="18df8-269">**Nota**  Causa la transizione alla fase di estrazione.</span><span class="sxs-lookup"><span data-stu-id="18df8-269">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="18df8-270">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="18df8-270">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="18df8-271">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="18df8-271">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="18df8-272">JetSeek</span><span class="sxs-lookup"><span data-stu-id="18df8-272">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="18df8-273">**Nota**  Causa la transizione alla fase di estrazione.</span><span class="sxs-lookup"><span data-stu-id="18df8-273">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="18df8-274">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="18df8-274">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="18df8-275">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="18df8-275">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="18df8-276">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="18df8-276">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="18df8-277">Quando la tabella temporanea non viene materializzata e si trova nella fase di estrazione, il cursore presenta le funzionalità seguenti, ma può essere ulteriormente limitato dalle opzioni richieste:</span><span class="sxs-lookup"><span data-stu-id="18df8-277">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options that are requested:</span></span>

  - [<span data-ttu-id="18df8-278">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="18df8-278">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="18df8-279">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="18df8-279">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="18df8-280">**Nota**  Se viene effettuato un tentativo di duplicare una tabella temporanea in modalità di sola trasmissione, il cursore risultante non verrà creato correttamente e non funzionerà correttamente.</span><span class="sxs-lookup"><span data-stu-id="18df8-280">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="18df8-281">È comunque possibile duplicare un cursore su una tabella temporanea materializzata.</span><span class="sxs-lookup"><span data-stu-id="18df8-281">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="18df8-282">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="18df8-282">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="18df8-283">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="18df8-283">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="18df8-284">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="18df8-284">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="18df8-285">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="18df8-285">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="18df8-286">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="18df8-286">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="18df8-287">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="18df8-287">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="18df8-288">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="18df8-288">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="18df8-289">JetMove</span><span class="sxs-lookup"><span data-stu-id="18df8-289">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="18df8-290">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="18df8-290">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="18df8-291">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="18df8-291">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="18df8-292">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="18df8-292">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="18df8-293">JetSeek</span><span class="sxs-lookup"><span data-stu-id="18df8-293">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="18df8-294">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="18df8-294">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="18df8-295">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="18df8-295">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="18df8-296">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18df8-296">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18df8-297"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="18df8-297"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="18df8-298">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="18df8-298">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-299"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="18df8-299"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="18df8-300">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="18df8-300">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-301"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="18df8-301"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="18df8-302">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="18df8-302">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18df8-303"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="18df8-303"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="18df8-304">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="18df8-304">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18df8-305"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="18df8-305"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="18df8-306">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="18df8-306">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="18df8-307">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="18df8-307">See Also</span></span>

[<span data-ttu-id="18df8-308">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="18df8-308">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="18df8-309">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="18df8-309">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="18df8-310">JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="18df8-310">JET_OPENTEMPORARYTABLE</span></span>](./jet-opentemporarytable-structure.md)  
[<span data-ttu-id="18df8-311">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="18df8-311">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="18df8-312">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="18df8-312">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="18df8-313">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="18df8-313">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="18df8-314">JetMove</span><span class="sxs-lookup"><span data-stu-id="18df8-314">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="18df8-315">JetRollback</span><span class="sxs-lookup"><span data-stu-id="18df8-315">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="18df8-316">JetSeek</span><span class="sxs-lookup"><span data-stu-id="18df8-316">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="18df8-317">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="18df8-317">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="18df8-318">Parametri informativi</span><span class="sxs-lookup"><span data-stu-id="18df8-318">Informational Parameters</span></span>](./informational-parameters.md)  
[<span data-ttu-id="18df8-319">Parametri di database temporanei</span><span class="sxs-lookup"><span data-stu-id="18df8-319">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
