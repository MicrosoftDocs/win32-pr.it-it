---
description: 'Altre informazioni su: funzione JetSetCurrentIndex2'
title: Funzione JetSetCurrentIndex2
TOCTitle: JetSetCurrentIndex2 Function
ms:assetid: da94465e-bd35-45c2-9ccc-1d2e8c34aa9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294110(v=EXCHG.10)
ms:contentKeyID: 32765725
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex2W
- JetSetCurrentIndex2A
- JetSetCurrentIndex2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c95e665b549fff82e0beaaca9682329217ebb0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305727"
---
# <a name="jetsetcurrentindex2-function"></a><span data-ttu-id="2f2c1-103">Funzione JetSetCurrentIndex2</span><span class="sxs-lookup"><span data-stu-id="2f2c1-103">JetSetCurrentIndex2 Function</span></span>


<span data-ttu-id="2f2c1-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2f2c1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex2-function"></a><span data-ttu-id="2f2c1-105">Funzione JetSetCurrentIndex2</span><span class="sxs-lookup"><span data-stu-id="2f2c1-105">JetSetCurrentIndex2 Function</span></span>

<span data-ttu-id="2f2c1-106">La funzione **JetSetCurrentIndex2** imposta l'indice corrente di un cursore che definisce quali record di una tabella sono visibili a tale cursore e l'ordine in cui vengono visualizzati selezionando il set di voci di indice da utilizzare per esporre tali record.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-106">The **JetSetCurrentIndex2** function sets the current index of a cursor that defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="2f2c1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f2c1-107">Parameters</span></span>

<span data-ttu-id="2f2c1-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2f2c1-108">*sesid*</span></span>

<span data-ttu-id="2f2c1-109">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-109">The session to use for this call.</span></span>

<span data-ttu-id="2f2c1-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="2f2c1-110">*tableid*</span></span>

<span data-ttu-id="2f2c1-111">Cursore da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-111">The cursor to use for this call.</span></span>

<span data-ttu-id="2f2c1-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="2f2c1-112">*szIndexName*</span></span>

<span data-ttu-id="2f2c1-113">Nome dell'indice da selezionare per il cursore.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-113">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="2f2c1-114">Se questo parametro è NULL o una stringa vuota, verrà selezionato l'indice cluster.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-114">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="2f2c1-115">Se viene definito un indice primario per la tabella, l'indice verrà selezionato perché corrisponde all'indice cluster.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-115">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="2f2c1-116">Se per la tabella non è definito alcun indice primario, verrà selezionato l'indice sequenziale.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-116">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="2f2c1-117">La definizione dell'indice sequenziale non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-117">The sequential index has no index definition.</span></span> <span data-ttu-id="2f2c1-118">Per ulteriori informazioni, vedere [JetCreateIndex](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="2f2c1-118">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="2f2c1-119">Se *pIndexID* non è null, il nome dell'indice verrà ignorato e l'indice verrà selezionato in base al relativo ID di indice.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-119">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="2f2c1-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="2f2c1-120">*grbit*</span></span>

<span data-ttu-id="2f2c1-121">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-121">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f2c1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2f2c1-122">Value</span></span></p></th>
<th><p><span data-ttu-id="2f2c1-123">Significato</span><span class="sxs-lookup"><span data-stu-id="2f2c1-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-124">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="2f2c1-124">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-125">Questa opzione indica che il cursore deve essere posizionato sulla prima voce dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-125">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="2f2c1-126">Se viene selezionato l'indice cluster (indice primario o sequenziale) e l'indice corrente è un indice secondario, viene utilizzato JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-126">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="2f2c1-127">Se viene selezionato l'indice corrente, questa opzione viene ignorata e non viene apportata alcuna modifica alla posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-127">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2c1-128">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="2f2c1-128">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-129">Questa opzione indica che il cursore deve essere posizionato sulla voce di indice del nuovo indice che corrisponde al record associato alla voce di indice in corrispondenza della posizione corrente del cursore sull'indice precedente.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-129">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="2f2c1-130">Se la definizione del nuovo indice contiene almeno una colonna chiave multivalore, la voce dell'indice di destinazione è ambigua.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-130">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="2f2c1-131">In questo caso, l'oggetto <em>itagSequence</em> specificato viene utilizzato per selezionare il multivalore della colonna chiave multivalore più significativa utilizzata per posizionare il cursore.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-131">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="2f2c1-132">È necessario passare un solo <em>itagSequence</em> , anche nel caso di più colonne chiave multivalore perché il motore espande solo tutti i valori per la colonna chiave multivalore più significativa.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-132">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="2f2c1-133">Per ulteriori informazioni, vedere <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> .</span><span class="sxs-lookup"><span data-stu-id="2f2c1-133">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="2f2c1-134">Se viene specificato JET_bitMoveFirst, questa opzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-134">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="2f2c1-135">Se viene selezionato l'indice corrente, questa opzione viene ignorata e non viene apportata alcuna modifica alla posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-135">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="2f2c1-136">Se questo parametro non è presente, il relativo valore si presume che sia JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-136">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2f2c1-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f2c1-137">Return Value</span></span>

<span data-ttu-id="2f2c1-138">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2f2c1-139">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="2f2c1-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f2c1-140">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2f2c1-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="2f2c1-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f2c1-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2f2c1-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-143">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2c1-144">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="2f2c1-144">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-145">È stato selezionato un indice secondario con l'opzione JET_bitNoMove e non è presente alcun valore per la prima colonna chiave multivalore nella nuova definizione per l'indice che corrisponde al numero di sequenza specificato.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-145">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new definition for the index that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2f2c1-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-147">Non è possibile completare l'operazione perché tutte le attività nell'istanza associata alla sessione sono state interrotte in seguito a una chiamata a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2c1-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2f2c1-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-149">Non è possibile completare l'operazione perché l'istanza associata alla sessione ha rilevato un errore irreversibile che richiede che l'accesso a tutti i dati venga revocato per proteggere l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="2f2c1-150">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-151">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="2f2c1-151">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-152">Il contenuto dell'ID di indice non è valido o è scaduto e deve essere aggiornato.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-152">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="2f2c1-153">Questo problema può verificarsi per <strong>JetSetCurrentIndex2</strong> quando:</span><span class="sxs-lookup"><span data-stu-id="2f2c1-153">This can happen for <strong>JetSetCurrentIndex2</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="2f2c1-154">pIndexID- &gt; cbStruct non è della dimensione prevista (Windows Server 2003 e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="2f2c1-154">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="2f2c1-155">Il motore è stato arrestato perché è stato recuperato l'ID dell'indice.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-155">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="2f2c1-156">Tutti i cursori che fanno riferimento alla tabella contenente l'indice corrispondente all'ID dell'indice sono stati chiusi e il motore ha eliminato la definizione per l'indice dalla cache dello schema.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-156">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted the definition for the index from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="2f2c1-157">L'ID di indice viene utilizzato con un cursore aperto nella tabella errata.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-157">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="2f2c1-158">L'indice è stato eliminato o non è ancora visibile alla sessione.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-158">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2c1-159">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="2f2c1-159">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-160">Uno dei nomi di oggetto specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-160">One of the specified object names was invalid.</span></span> <span data-ttu-id="2f2c1-161">Tutti i nomi di oggetto devono essere conformi allo stesso set di regole.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-161">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="2f2c1-162">Le regole sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f2c1-162">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="2f2c1-163">I nomi degli oggetti devono essere composti da caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-163">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="2f2c1-164">I nomi degli oggetti devono avere una lunghezza di almeno un carattere.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-164">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="2f2c1-165">I nomi degli oggetti non possono superare la lunghezza di JET_cbNameMost (64) caratteri.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-165">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="2f2c1-166">I nomi degli oggetti non possono iniziare con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-166">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="2f2c1-167">I nomi degli oggetti non possono contenere caratteri di controllo ASCII (da 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="2f2c1-167">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="2f2c1-168">I nomi degli oggetti non possono contenere punti esclamativi (!), punti (.), parentesi quadra aperta ([) o parentesi quadra chiusa (]).</span><span class="sxs-lookup"><span data-stu-id="2f2c1-168">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="2f2c1-169">Una volta convalidata, solo la parte della stringa fino al primo spazio (se presente) verrà utilizzata per il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-169">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="2f2c1-170">Ciò significa che i nomi degli oggetti non possono contenere uno spazio.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-170">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-171">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2f2c1-171">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-172">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-172">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="2f2c1-173">Questo problema può verificarsi per <strong>JetSetCurrentIndex2</strong> quando <em>PINDEXID</em> non è null e pIndexID- &gt; cbStruct non è della dimensione prevista (Windows XP e versioni precedenti).</span><span class="sxs-lookup"><span data-stu-id="2f2c1-173">This can happen for <strong>JetSetCurrentIndex2</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2c1-174">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="2f2c1-174">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-175">Un indice secondario viene selezionato con l'opzione JET_bitNoMove e non è presente alcuna voce di indice nel nuovo indice che corrisponde al record associato alla voce di indice nella posizione corrente del cursore sull'indice precedente.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-175">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-176">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2f2c1-176">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-177">Non è possibile completare l'operazione perché l'istanza associata alla sessione non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-177">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2c1-178">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="2f2c1-178">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-179">Il motore ha esaurito il pool di risorse utilizzate per aprire i cursori.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-179">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="2f2c1-180">Il numero massimo di cursori che è possibile aprire in qualsiasi momento viene controllato utilizzando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-180">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="2f2c1-181">Per ulteriori informazioni, vedere <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> .</span><span class="sxs-lookup"><span data-stu-id="2f2c1-181">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="2f2c1-182">Questo problema può verificarsi per <strong>JetSetCurrentIndex2</strong> quando è stato selezionato un indice secondario e il motore non è in grado di aprire un cursore interno per utilizzare tale indice.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-182">This can happen for <strong>JetSetCurrentIndex2</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-183">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2f2c1-183">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-184">Non è possibile completare l'operazione perché è in corso un'operazione di ripristino sull'istanza associata alla sessione.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-184">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2c1-185">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="2f2c1-185">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-186">Non è possibile usare la stessa sessione per più di un thread nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-186">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="2f2c1-187">Questo errore verrà restituito solo da Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-187">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-188">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2f2c1-188">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2f2c1-189">Non è possibile completare l'operazione perché l'istanza associata alla sessione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-189">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f2c1-190">In seguito all'esito positivo, l'indice corrente del cursore viene impostato sull'indice richiesto.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-190">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="2f2c1-191">È ora possibile cercare le voci di indice usando [JetSeek](./jetseek-function.md) in base alla definizione dell'indice dell'indice richiesto.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-191">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="2f2c1-192">È inoltre possibile enumerare le voci di indice utilizzando [JetMove](./jetmove-function.md) nell'ordine specificato dalla definizione di tale indice.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-192">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="2f2c1-193">La posizione corrente del cursore viene impostata sulla prima voce di indice nell'indice (JET_bitMoveFirst) o su una voce di indice specifica correlata alla posizione corrente del cursore sull'indice precedente (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="2f2c1-193">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="2f2c1-194">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-194">No change to the database state will occur.</span></span>

<span data-ttu-id="2f2c1-195">In caso di errore, l'indice corrente e la posizione corrente del cursore sono in uno stato non definito.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-195">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="2f2c1-196">Non si verificherà alcuna modifica allo stato del database.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-196">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2f2c1-197">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f2c1-197">Remarks</span></span>

<span data-ttu-id="2f2c1-198">Se l'hint ID dell'indice non è aggiornato, l'API ha semplicemente esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-198">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="2f2c1-199">In questo caso, non esiste alcun fallback al nome di testo dell'indice, come si può prevedere.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-199">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="2f2c1-200">Questo fallback deve essere eseguito manualmente dal chiamante dell'API.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-200">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2f2c1-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f2c1-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2f2c1-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2c1-203">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2c1-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2f2c1-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2c1-205">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-206"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="2f2c1-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2c1-207">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2c1-208"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="2f2c1-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2c1-209">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f2c1-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2f2c1-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2c1-211">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f2c1-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2f2c1-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2f2c1-213">Implementato come <strong>JetSetCurrentIndex2W</strong> (Unicode) e <strong>JetSetCurrentIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2f2c1-213">Implemented as <strong>JetSetCurrentIndex2W</strong> (Unicode) and <strong>JetSetCurrentIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2f2c1-214">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2f2c1-214">See Also</span></span>

[<span data-ttu-id="2f2c1-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2f2c1-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2f2c1-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2f2c1-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2f2c1-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2f2c1-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2f2c1-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2f2c1-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2f2c1-219">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="2f2c1-219">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="2f2c1-220">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="2f2c1-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="2f2c1-221">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="2f2c1-221">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="2f2c1-222">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="2f2c1-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="2f2c1-223">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="2f2c1-223">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="2f2c1-224">JetMove</span><span class="sxs-lookup"><span data-stu-id="2f2c1-224">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="2f2c1-225">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="2f2c1-225">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="2f2c1-226">JetSeek</span><span class="sxs-lookup"><span data-stu-id="2f2c1-226">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="2f2c1-227">JetStopService</span><span class="sxs-lookup"><span data-stu-id="2f2c1-227">JetStopService</span></span>](./jetstopservice-function.md)
