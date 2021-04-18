---
description: 'Altre informazioni su: funzione JetGetColumnInfo'
title: Funzione JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d96d5860f4b10f9294ab210e4e41d78cede202f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315072"
---
# <a name="jetgetcolumninfo-function"></a><span data-ttu-id="34a4f-103">Funzione JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="34a4f-103">JetGetColumnInfo Function</span></span>


<span data-ttu-id="34a4f-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="34a4f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcolumninfo-function"></a><span data-ttu-id="34a4f-105">Funzione JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="34a4f-105">JetGetColumnInfo Function</span></span>

<span data-ttu-id="34a4f-106">La funzione **JetGetColumnInfo** recupera le informazioni su una colonna.</span><span class="sxs-lookup"><span data-stu-id="34a4f-106">The **JetGetColumnInfo** function retrieves information about a column.</span></span>

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="34a4f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="34a4f-107">Parameters</span></span>

<span data-ttu-id="34a4f-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="34a4f-108">*sesid*</span></span>

<span data-ttu-id="34a4f-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="34a4f-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="34a4f-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="34a4f-110">*dbid*</span></span>

<span data-ttu-id="34a4f-111">Identifica, insieme a *szTableName*, la tabella contenente la colonna da cui vengono recuperate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="34a4f-111">Identifies, along with *szTableName*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="34a4f-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="34a4f-112">*szTableName*</span></span>

<span data-ttu-id="34a4f-113">Identifica, insieme a *dbid*, la tabella contenente la colonna da cui vengono recuperate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="34a4f-113">Identifies, along with *dbid*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="34a4f-114">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="34a4f-114">*szColumnName*</span></span>

<span data-ttu-id="34a4f-115">Nome della colonna per cui vengono recuperate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="34a4f-115">The name of the column that information is fetched for.</span></span>

<span data-ttu-id="34a4f-116">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="34a4f-116">*pvResult*</span></span>

<span data-ttu-id="34a4f-117">Puntatore a un buffer che riceverà le informazioni.</span><span class="sxs-lookup"><span data-stu-id="34a4f-117">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="34a4f-118">Il tipo di buffer dipende da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="34a4f-118">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="34a4f-119">Il chiamante deve essere configurato per allineare il buffer in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="34a4f-119">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="34a4f-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="34a4f-120">*cbMax*</span></span>

<span data-ttu-id="34a4f-121">Dimensione, in byte, del buffer passato in *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="34a4f-121">The size, in bytes, of the buffer that is passed in *pvResult*.</span></span>

<span data-ttu-id="34a4f-122">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="34a4f-122">*InfoLevel*</span></span>

<span data-ttu-id="34a4f-123">Tipo di informazioni da recuperare per la colonna specificata da *szColumnName*.</span><span class="sxs-lookup"><span data-stu-id="34a4f-123">The type of information to retrieve for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="34a4f-124">Il formato dei dati archiviati in *pvResult* dipende da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="34a4f-124">The format of the data stored in *pvResult* is dependent on this parameter.</span></span> <span data-ttu-id="34a4f-125">Per lo schema della tabella temporanea, vedere [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="34a4f-125">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="34a4f-126">Questi *InfoLevels* sono differenziati per:</span><span class="sxs-lookup"><span data-stu-id="34a4f-126">These *InfoLevels* are differentiated by:</span></span>

  - <span data-ttu-id="34a4f-127">JET_ColInfoListSortColumnid Ordina la tabella temporanea *ColumnID*.</span><span class="sxs-lookup"><span data-stu-id="34a4f-127">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="34a4f-128">JET_ColInfoListCompact comprimerà l'output.</span><span class="sxs-lookup"><span data-stu-id="34a4f-128">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="34a4f-129">Per ulteriori informazioni sull'output di Compact, vedere [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="34a4f-129">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="34a4f-130">Con questo parametro è possibile usare le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="34a4f-130">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34a4f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="34a4f-131">Value</span></span></p></th>
<th><p><span data-ttu-id="34a4f-132">Significato</span><span class="sxs-lookup"><span data-stu-id="34a4f-132">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-133">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="34a4f-133">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="34a4f-134">JET_ColInfo e JET_ColInfoByColid recuperano le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="34a4f-134">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span> <span data-ttu-id="34a4f-135"><em>pvResult</em> viene interpretato come <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>e i campi della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> sono compilati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="34a4f-135"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a4f-136">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="34a4f-136">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="34a4f-137"><em>pvResult</em> viene interpretato come una struttura <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> .</span><span class="sxs-lookup"><span data-stu-id="34a4f-137"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="34a4f-138">Questa operazione è simile a una struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> .</span><span class="sxs-lookup"><span data-stu-id="34a4f-138">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="34a4f-139">Se questa funzione ha esito positivo, la struttura viene popolata con i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="34a4f-139">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="34a4f-140">Se questa funzione ha esito negativo, la struttura contiene dati non definiti.</span><span class="sxs-lookup"><span data-stu-id="34a4f-140">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-141">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="34a4f-141">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="34a4f-142">Come JET_ColInfo, <em>pvResult</em> viene interpretato come <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, ad eccezione del fatto che questo <em>InfoLevel</em> indica che la colonna richiesta (<em>szColumName</em>) non è il nome della colonna stringa, ma un puntatore a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="34a4f-142">Like JET_ColInfo, <em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a4f-143">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="34a4f-143">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="34a4f-144"><em>pvResult</em> viene interpretato come una struttura <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="34a4f-144"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="34a4f-145">Se questa funzione ha esito positivo, la struttura viene popolata con i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="34a4f-145">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="34a4f-146">Viene aperta una tabella temporanea che viene identificata dal membro <strong>TableID</strong> della struttura <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="34a4f-146">A temporary table is opened and is identified by the <strong>tableid</strong> member of the <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="34a4f-147">La tabella deve essere chiusa con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="34a4f-147">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="34a4f-148">Se questa funzione ha esito negativo, la struttura contiene dati non definiti.</span><span class="sxs-lookup"><span data-stu-id="34a4f-148">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-149">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="34a4f-149">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="34a4f-150">Uguale a JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="34a4f-150">Same as JET_ColInfoList.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a4f-151">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="34a4f-151">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="34a4f-152">Uguale a JET_ColInfoList; Tuttavia, la tabella risultante viene ordinata in base a ColumnID, anziché al nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="34a4f-152">Same as JET_ColInfoList; however the resulting table is sorted by columnid, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-153">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="34a4f-153">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="34a4f-154">JET_ColInfoSysTabCursor è deprecato e l'uso di esso restituirà JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="34a4f-154">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a4f-155">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="34a4f-155">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="34a4f-156">Come JET_ColInfoBase, <em>pvResult</em> viene interpretato come <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, ad eccezione del fatto che questo <em>InfoLevel</em> indica che la colonna richiesta (<em>szColumName</em>) non è il nome della colonna stringa, ma un puntatore a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="34a4f-156">Like JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="34a4f-157"><strong>Windows Vista:  </strong> Questo valore è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34a4f-157"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="34a4f-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="34a4f-159">Restituire solo colonne non derivate (se la tabella è derivata da un modello).</span><span class="sxs-lookup"><span data-stu-id="34a4f-159">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="34a4f-160">Questo valore può essere logicamente o in <em>InfoLevel</em>quando il <em>InfoLevel</em> di base è JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="34a4f-160">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="34a4f-161"><strong>Windows Vista:  </strong> Questo valore è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34a4f-161"><strong>Windows Vista:  </strong>This value is introduced Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a4f-162">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="34a4f-162">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="34a4f-163">Restituisce solo il nome della colonna e il ColumnID di ogni colonna.</span><span class="sxs-lookup"><span data-stu-id="34a4f-163">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="34a4f-164">Questo valore può essere logicamente o in <em>InfoLevel</em>quando il <em>InfoLevel</em> di base è JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="34a4f-164">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="34a4f-165"><strong>Windows Vista:  </strong> Questo valore è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34a4f-165"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-166">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="34a4f-166">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="34a4f-167">Ordina elenco colonne restituite in base a ColumnID (l'impostazione predefinita consiste nell'ordinare l'elenco in base al nome della colonna).</span><span class="sxs-lookup"><span data-stu-id="34a4f-167">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="34a4f-168">Questo valore può essere logicamente o in <em>InfoLevel</em>quando il <em>InfoLevel</em> di base è JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="34a4f-168">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="34a4f-169"><strong>Windows Vista:  </strong> Questo valore è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34a4f-169"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="34a4f-170">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34a4f-170">Return Value</span></span>

<span data-ttu-id="34a4f-171">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="34a4f-171">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="34a4f-172">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="34a4f-172">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34a4f-173">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="34a4f-173">Return code</span></span></p></th>
<th><p><span data-ttu-id="34a4f-174">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34a4f-174">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-175">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="34a4f-175">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="34a4f-176">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="34a4f-176">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a4f-177">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="34a4f-177">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="34a4f-178">La colonna denominata <em>szColumnName</em> non è stata trovata nella tabella.</span><span class="sxs-lookup"><span data-stu-id="34a4f-178">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-179">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="34a4f-179">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="34a4f-180">È stato specificato un <em>InfoLevel</em> non valido.</span><span class="sxs-lookup"><span data-stu-id="34a4f-180">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a4f-181">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="34a4f-181">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="34a4f-182">Questo errore può essere restituito se:</span><span class="sxs-lookup"><span data-stu-id="34a4f-182">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="34a4f-183">È stato specificato un nome non valido per <em>szTableName</em> .</span><span class="sxs-lookup"><span data-stu-id="34a4f-183">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="34a4f-184">È stato specificato un nome non valido per <em>szColumnName</em> .</span><span class="sxs-lookup"><span data-stu-id="34a4f-184">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-185">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="34a4f-185">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="34a4f-186">Questo errore può essere restituito se:</span><span class="sxs-lookup"><span data-stu-id="34a4f-186">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="34a4f-187">È stato specificato un <em>InfoLevel</em> non valido.</span><span class="sxs-lookup"><span data-stu-id="34a4f-187">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="34a4f-188">È stato passato un <em>SZTABLENAME</em> null.</span><span class="sxs-lookup"><span data-stu-id="34a4f-188">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="34a4f-189">Il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="34a4f-189">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="34a4f-190">Commenti</span><span class="sxs-lookup"><span data-stu-id="34a4f-190">Remarks</span></span>

<span data-ttu-id="34a4f-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) e **JetGetColumnInfo** recuperano entrambe le informazioni relative a una colonna.</span><span class="sxs-lookup"><span data-stu-id="34a4f-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) and **JetGetColumnInfo** both retrieve information about a column.</span></span> <span data-ttu-id="34a4f-192">La differenza tra di esse è la modalità di identificazione della tabella:</span><span class="sxs-lookup"><span data-stu-id="34a4f-192">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="34a4f-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifica una tabella in base a *TableID*.</span><span class="sxs-lookup"><span data-stu-id="34a4f-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="34a4f-194">**JetGetColumnInfo** identifica una tabella in base alla combinazione *dbid* e *szTableName* .</span><span class="sxs-lookup"><span data-stu-id="34a4f-194">**JetGetColumnInfo** identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="34a4f-195">Quando si recuperano dati con JET_ColInfoList, JET_ColInfoListSortColumnid o JET_ColInfoListCompact, viene aperta una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="34a4f-195">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="34a4f-196">La tabella temporanea contiene dati e la struttura [JET_COLUMNLIST](./jet-columnlist-structure.md) contiene informazioni sufficienti per attraversare la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="34a4f-196">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="34a4f-197">La tabella temporanea deve essere chiusa con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="34a4f-197">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="34a4f-198">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34a4f-198">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-199"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="34a4f-199"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="34a4f-200">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="34a4f-200">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a4f-201"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="34a4f-201"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="34a4f-202">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="34a4f-202">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-203"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="34a4f-203"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="34a4f-204">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="34a4f-204">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a4f-205"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="34a4f-205"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="34a4f-206">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="34a4f-206">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34a4f-207"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="34a4f-207"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="34a4f-208">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="34a4f-208">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a4f-209"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="34a4f-209"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="34a4f-210">Implementato come <strong>JetGetColumnInfoW</strong> (Unicode) e <strong>JetGetColumnInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="34a4f-210">Implemented as <strong>JetGetColumnInfoW</strong> (Unicode) and <strong>JetGetColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="34a4f-211">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="34a4f-211">See Also</span></span>

[<span data-ttu-id="34a4f-212">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="34a4f-212">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="34a4f-213">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="34a4f-213">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="34a4f-214">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="34a4f-214">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="34a4f-215">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="34a4f-215">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="34a4f-216">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="34a4f-216">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="34a4f-217">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="34a4f-217">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="34a4f-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="34a4f-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="34a4f-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="34a4f-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="34a4f-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="34a4f-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="34a4f-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="34a4f-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="34a4f-222">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="34a4f-222">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="34a4f-223">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="34a4f-223">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
