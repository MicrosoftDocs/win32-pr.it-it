---
description: 'Altre informazioni su: funzione JetGetTableInfo'
title: Funzione JetGetTableInfo
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968432"
---
# <a name="jetgettableinfo-function"></a><span data-ttu-id="022de-103">Funzione JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="022de-103">JetGetTableInfo Function</span></span>


<span data-ttu-id="022de-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="022de-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableinfo-function"></a><span data-ttu-id="022de-105">Funzione JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="022de-105">JetGetTableInfo Function</span></span>

<span data-ttu-id="022de-106">La funzione **JetGetTableInfo** Recupera varie informazioni su una tabella in un database.</span><span class="sxs-lookup"><span data-stu-id="022de-106">The **JetGetTableInfo** function retrieves various pieces of information about a table in a database.</span></span>

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="022de-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="022de-107">Parameters</span></span>

<span data-ttu-id="022de-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="022de-108">*sesid*</span></span>

<span data-ttu-id="022de-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="022de-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="022de-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="022de-110">*tableid*</span></span>

<span data-ttu-id="022de-111">Tabella a cui si applicano le informazioni.</span><span class="sxs-lookup"><span data-stu-id="022de-111">The table that the information applies to.</span></span>

<span data-ttu-id="022de-112">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="022de-112">*pvResult*</span></span>

<span data-ttu-id="022de-113">Puntatore a un buffer che riceverà le informazioni.</span><span class="sxs-lookup"><span data-stu-id="022de-113">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="022de-114">Il tipo di buffer dipende da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="022de-114">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="022de-115">È responsabilità del chiamante allineare il buffer in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="022de-115">It is the responsibility of the caller to align the buffer appropriately.</span></span>

<span data-ttu-id="022de-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="022de-116">*cbMax*</span></span>

<span data-ttu-id="022de-117">Dimensione, in byte, del buffer passato in *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="022de-117">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="022de-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="022de-118">*InfoLevel*</span></span>

<span data-ttu-id="022de-119">Tipo di informazioni che verranno recuperate per la tabella specificata da *TableID*.</span><span class="sxs-lookup"><span data-stu-id="022de-119">The type of information that will be retrieved for the table that is specified by *tableid*.</span></span> <span data-ttu-id="022de-120">Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="022de-120">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="022de-121">Per questo parametro è possibile impostare le opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="022de-121">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="022de-122">Valore</span><span class="sxs-lookup"><span data-stu-id="022de-122">Value</span></span></p></th>
<th><p><span data-ttu-id="022de-123">Significato</span><span class="sxs-lookup"><span data-stu-id="022de-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="022de-124">JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="022de-124">JET_TblInfo</span></span></p></td>
<td><p><span data-ttu-id="022de-125"><em>pvResult</em> viene interpretato come una struttura <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="022de-125"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span> <span data-ttu-id="022de-126">Se il metodo ha esito positivo, la struttura <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> viene compilata con i dati appropriati.</span><span class="sxs-lookup"><span data-stu-id="022de-126">If the method succeeds, the <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is filled in with the appropriate data.</span></span> <span data-ttu-id="022de-127">Se ha esito negativo, il contenuto non è definito.</span><span class="sxs-lookup"><span data-stu-id="022de-127">If it fails, the contents are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-128">JET_TblInfoDbid</span><span class="sxs-lookup"><span data-stu-id="022de-128">JET_TblInfoDbid</span></span></p></td>
<td><p><span data-ttu-id="022de-129"><em>pvResult</em> viene considerato come una matrice di due oggetti <a href="gg269248(v=exchg.10).md">JET_DBID</a> .</span><span class="sxs-lookup"><span data-stu-id="022de-129"><em>pvResult</em> is treated as an array of two <a href="gg269248(v=exchg.10).md">JET_DBID</a> objects.</span></span> <span data-ttu-id="022de-130">L'identificatore del database proprietario della tabella viene archiviato due volte in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="022de-130">The database identifier of the database that owns the table is stored in this array twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-131">JET_TblInfoDumpTable</span><span class="sxs-lookup"><span data-stu-id="022de-131">JET_TblInfoDumpTable</span></span></p></td>
<td><p><span data-ttu-id="022de-132">JET_TblInfoDumpTable è deprecato.</span><span class="sxs-lookup"><span data-stu-id="022de-132">JET_TblInfoDumpTable is deprecated.</span></span> <span data-ttu-id="022de-133">L'API restituirà JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="022de-133">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-134">JET_TblInfoName</span><span class="sxs-lookup"><span data-stu-id="022de-134">JET_TblInfoName</span></span></p></td>
<td><p><span data-ttu-id="022de-135">JET_TblInfoName Recupera il nome della tabella e lo archivia in <em>pvResult</em>.</span><span class="sxs-lookup"><span data-stu-id="022de-135">JET_TblInfoName retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="022de-136">Se il buffer è troppo piccolo, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="022de-136">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-137">JET_TblInfoMostMany</span><span class="sxs-lookup"><span data-stu-id="022de-137">JET_TblInfoMostMany</span></span></p></td>
<td><p><span data-ttu-id="022de-138">JET_TblInfoMostMany Recupera il nome della tabella e lo archivia in <em>pvResult</em>.</span><span class="sxs-lookup"><span data-stu-id="022de-138">JET_TblInfoMostMany retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="022de-139">Se il buffer è troppo piccolo, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="022de-139">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-140">JET_TblInfoOLC</span><span class="sxs-lookup"><span data-stu-id="022de-140">JET_TblInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="022de-141">JET_TblInfoOLC è deprecato.</span><span class="sxs-lookup"><span data-stu-id="022de-141">JET_TblInfoOLC is deprecated.</span></span> <span data-ttu-id="022de-142">L'API restituirà JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="022de-142">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-143">JET_TblInfoRvt</span><span class="sxs-lookup"><span data-stu-id="022de-143">JET_TblInfoRvt</span></span></p></td>
<td><p><span data-ttu-id="022de-144">JET_TblInfoRvt è deprecato.</span><span class="sxs-lookup"><span data-stu-id="022de-144">JET_TblInfoRvt is deprecated.</span></span> <span data-ttu-id="022de-145">L'API restituirà JET_errQueryNotSupported.</span><span class="sxs-lookup"><span data-stu-id="022de-145">The API will return JET_errQueryNotSupported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-146">JET_TblInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="022de-146">JET_TblInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="022de-147">JET_TblInfoResetOLC è deprecato.</span><span class="sxs-lookup"><span data-stu-id="022de-147">JET_TblInfoResetOLC is deprecated.</span></span> <span data-ttu-id="022de-148">L'API restituirà JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="022de-148">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-149">JET_TblInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="022de-149">JET_TblInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="022de-150"><em>pvResult</em> viene interpretato come una matrice di due ULONG:</span><span class="sxs-lookup"><span data-stu-id="022de-150"><em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="022de-151">Il primo <strong>ULONG</strong> è il numero di pagine nella tabella.</span><span class="sxs-lookup"><span data-stu-id="022de-151">The first <strong>ULONG</strong> is the number of pages in the table.</span></span></p></li>
<li><p><span data-ttu-id="022de-152">Il secondo <strong>ULONG</strong> è la densità di destinazione delle pagine per la tabella.</span><span class="sxs-lookup"><span data-stu-id="022de-152">The second <strong>ULONG</strong> is the target density of pages for the table.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-153">JET_TblInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="022de-153">JET_TblInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="022de-154"><em>pvResult</em> viene interpretato come <strong>ULONG</strong>.</span><span class="sxs-lookup"><span data-stu-id="022de-154"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="022de-155"><strong>ULONG</strong> è la somma del numero di pagine disponibili nella tabella, dei relativi indici e dell'albero del valore Long.</span><span class="sxs-lookup"><span data-stu-id="022de-155">The <strong>ULONG</strong> is the sum of the number of pages that are available in the table, its indexes, and the long value tree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-156">JET_TblInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="022de-156">JET_TblInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="022de-157"><em>pvResult</em> viene interpretato come <strong>ULONG</strong>.</span><span class="sxs-lookup"><span data-stu-id="022de-157"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="022de-158"><strong>ULONG</strong> è la somma del numero di pagine di proprietà della tabella, inclusi gli indici e l'albero del valore Long e tutte le pagine disponibili.</span><span class="sxs-lookup"><span data-stu-id="022de-158">The <strong>ULONG</strong> is the sum of the number of pages that are owned by the table (including its indexes, and the long value tree and any available pages therein).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-159">JET_TblInfoSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="022de-159">JET_TblInfoSpaceUsage</span></span></p></td>
<td><p><span data-ttu-id="022de-160">Il comportamento dell'API dipende dalla dimensione del buffer passato all'API.</span><span class="sxs-lookup"><span data-stu-id="022de-160">The behavior of the API depends on how large the buffer that is passed to the API is.</span></span> <span data-ttu-id="022de-161">I due valori di <em>cbMax</em> devono essere almeno (2 \* sizeof (ulong)).</span><span class="sxs-lookup"><span data-stu-id="022de-161">Two <em>cbMax</em> values must be at least ( 2 \* sizeof( ULONG ) ).</span></span></p>
<ul>
<li><p><span data-ttu-id="022de-162">Se <em>cbMax</em> è (2 \* sizeof (ulong)), <em>pvResult</em> viene interpretato come una matrice di due ULONG:</span><span class="sxs-lookup"><span data-stu-id="022de-162">If <em>cbMax</em> is ( 2 \* sizeof( ULONG ) ), <em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="022de-163">Il primo <strong>ULONG</strong> è il numero di extent di proprietà della tabella.</span><span class="sxs-lookup"><span data-stu-id="022de-163">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="022de-164">Il secondo <strong>ULONG</strong> è il numero di extent disponibili della tabella.</span><span class="sxs-lookup"><span data-stu-id="022de-164">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="022de-165"><em>pvResult</em> viene interpretato come una matrice di:</span><span class="sxs-lookup"><span data-stu-id="022de-165"><em>pvResult</em> is interpreted as an array of:</span></span></p>
<ul>
<li><p><span data-ttu-id="022de-166">Il primo <strong>ULONG</strong> è il numero di extent di proprietà della tabella.</span><span class="sxs-lookup"><span data-stu-id="022de-166">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="022de-167">Il secondo <strong>ULONG</strong> è il numero di extent disponibili della tabella.</span><span class="sxs-lookup"><span data-stu-id="022de-167">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-168">JET_TblInfoTemplateTableName</span><span class="sxs-lookup"><span data-stu-id="022de-168">JET_TblInfoTemplateTableName</span></span></p></td>
<td><p><span data-ttu-id="022de-169"><em>pvResult</em> viene interpretato come un buffer di stringa.</span><span class="sxs-lookup"><span data-stu-id="022de-169"><em>pvResult</em> is interpreted as a string buffer.</span></span> <span data-ttu-id="022de-170">Il buffer deve essere almeno JET_cbNameMost + 1, inclusa la terminazione <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="022de-170">The buffer must be at least JET_cbNameMost + 1, including the terminating <strong>NULL</strong>.</span></span> <span data-ttu-id="022de-171">Se la tabella è una tabella derivata, il buffer verrà compilato con il nome della tabella da cui la tabella derivata eredita la DDL.</span><span class="sxs-lookup"><span data-stu-id="022de-171">If the table is a derived table, the buffer will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="022de-172">Se la tabella non è una tabella derivata, il buffer sarà una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="022de-172">If the table is not a derived table, the buffer will an empty string.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="022de-173">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="022de-173">Return Value</span></span>

<span data-ttu-id="022de-174">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="022de-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="022de-175">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="022de-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="022de-176">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="022de-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="022de-177">Descrizione</span><span class="sxs-lookup"><span data-stu-id="022de-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="022de-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="022de-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="022de-179">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="022de-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-180">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="022de-180">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="022de-181">Il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="022de-181">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-182">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="022de-182">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="022de-183">È stato specificato un <em>InfoLevel</em> deprecato.</span><span class="sxs-lookup"><span data-stu-id="022de-183">A deprecated <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-184">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="022de-184">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="022de-185">Dimensioni del buffer non corrette.</span><span class="sxs-lookup"><span data-stu-id="022de-185">The buffer was not the right size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-186">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="022de-186">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="022de-187">La tabella passata è una tabella temporanea e non è possibile recuperare il <em>InfoLevel</em> richiesto per una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="022de-187">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-188">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="022de-188">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="022de-189">La tabella passata è una tabella temporanea e non è possibile recuperare il <em>InfoLevel</em> richiesto per una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="022de-189">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-190">JET_errQueryNotSupported</span><span class="sxs-lookup"><span data-stu-id="022de-190">JET_errQueryNotSupported</span></span></p></td>
<td><p><span data-ttu-id="022de-191"><em>InfoLevel</em> non è supportato.</span><span class="sxs-lookup"><span data-stu-id="022de-191">The <em>InfoLevel</em> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-192">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="022de-192">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="022de-193">La tabella è utilizzata da un'altra operazione di database.</span><span class="sxs-lookup"><span data-stu-id="022de-193">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-194">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="022de-194">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="022de-195">La tabella è bloccata da un'altra operazione di database.</span><span class="sxs-lookup"><span data-stu-id="022de-195">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-196">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="022de-196">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="022de-197">La tabella viene utilizzata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="022de-197">The table is being used by the system.</span></span> <span data-ttu-id="022de-198">Questo avviso non è irreversibile.</span><span class="sxs-lookup"><span data-stu-id="022de-198">This warning is nonfatal.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="022de-199">Commenti</span><span class="sxs-lookup"><span data-stu-id="022de-199">Remarks</span></span>

<span data-ttu-id="022de-200">Alcune informazioni non sono valide per le tabelle temporanee (vedere [JetOpenTempTable](./jetopentemptable-function.md)).</span><span class="sxs-lookup"><span data-stu-id="022de-200">Some pieces of information are not valid for temporary tables (See [JetOpenTempTable](./jetopentemptable-function.md)).</span></span>

<span data-ttu-id="022de-201">Le statistiche della tabella includono il numero di record e il numero di pagine nell'indice cluster, ovvero l'indice contenente i dati del record.</span><span class="sxs-lookup"><span data-stu-id="022de-201">The table statistics include the number of records and the number of pages in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="022de-202">È possibile accedere alle statistiche dell'indice separatamente in base al nome, utilizzando [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="022de-202">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="022de-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="022de-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="022de-204"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="022de-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="022de-205">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="022de-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="022de-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="022de-207">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="022de-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-208"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="022de-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="022de-209">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="022de-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-210"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="022de-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="022de-211">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="022de-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="022de-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="022de-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="022de-213">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="022de-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="022de-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="022de-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="022de-215">Implementato come <strong>JetGetTableInfoW</strong> (Unicode) e <strong>JetGetTableInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="022de-215">Implemented as <strong>JetGetTableInfoW</strong> (Unicode) and <strong>JetGetTableInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="022de-216">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="022de-216">See Also</span></span>

[<span data-ttu-id="022de-217">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="022de-217">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="022de-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="022de-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="022de-219">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="022de-219">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="022de-220">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="022de-220">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="022de-221">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="022de-221">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="022de-222">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="022de-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="022de-223">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="022de-223">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="022de-224">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="022de-224">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="022de-225">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="022de-225">JetOpenTempTable</span></span>](./jetopentemptable-function.md)
