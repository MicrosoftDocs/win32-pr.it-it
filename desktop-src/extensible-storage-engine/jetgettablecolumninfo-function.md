---
description: 'Altre informazioni su: funzione JetGetTableColumnInfo'
title: JetGetTableColumnInfo (funzione)
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104235243"
---
# <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="5598c-103">JetGetTableColumnInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="5598c-103">JetGetTableColumnInfo Function</span></span>


<span data-ttu-id="5598c-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5598c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="5598c-105">JetGetTableColumnInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="5598c-105">JetGetTableColumnInfo Function</span></span>

<span data-ttu-id="5598c-106">La funzione **JetGetTableColumnInfo** recupera le informazioni su una colonna della tabella.</span><span class="sxs-lookup"><span data-stu-id="5598c-106">The **JetGetTableColumnInfo** function retrieves information about a table column.</span></span>

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a><span data-ttu-id="5598c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5598c-107">Parameters</span></span>

<span data-ttu-id="5598c-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5598c-108">*sesid*</span></span>

<span data-ttu-id="5598c-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="5598c-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="5598c-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="5598c-110">*tableid*</span></span>

<span data-ttu-id="5598c-111">Tabella contenente la colonna per la quale recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="5598c-111">The table that contains the column to fetch information for.</span></span>

<span data-ttu-id="5598c-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="5598c-112">*szColumnName*</span></span>

<span data-ttu-id="5598c-113">Nome della colonna per cui recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="5598c-113">The name of the column to fetch information for.</span></span>

<span data-ttu-id="5598c-114">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="5598c-114">*pvResult*</span></span>

<span data-ttu-id="5598c-115">Puntatore a un buffer che riceverà le informazioni.</span><span class="sxs-lookup"><span data-stu-id="5598c-115">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="5598c-116">Il tipo di buffer dipende da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="5598c-116">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="5598c-117">Il chiamante deve essere configurato per allineare il buffer in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="5598c-117">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="5598c-118">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="5598c-118">*cbMax*</span></span>

<span data-ttu-id="5598c-119">Dimensione, in byte, del buffer passato in *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="5598c-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="5598c-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="5598c-120">*InfoLevel*</span></span>

<span data-ttu-id="5598c-121">Tipo di informazioni che verranno recuperate per la colonna specificata da *szColumnName*.</span><span class="sxs-lookup"><span data-stu-id="5598c-121">The type of information that will be retrieved for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="5598c-122">Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="5598c-122">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span> <span data-ttu-id="5598c-123">Per lo schema della tabella temporanea, vedere [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="5598c-123">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

  - <span data-ttu-id="5598c-124">JET_ColInfoListSortColumnid Ordina la tabella temporanea *ColumnID*.</span><span class="sxs-lookup"><span data-stu-id="5598c-124">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="5598c-125">JET_ColInfoListCompact comprimerà l'output.</span><span class="sxs-lookup"><span data-stu-id="5598c-125">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="5598c-126">Per ulteriori informazioni sull'output di Compact, vedere [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="5598c-126">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="5598c-127">Per questo parametro è possibile impostare le opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5598c-127">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5598c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5598c-128">Value</span></span></p></th>
<th><p><span data-ttu-id="5598c-129">Significato</span><span class="sxs-lookup"><span data-stu-id="5598c-129">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5598c-130">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="5598c-130">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="5598c-131"><em>pvResult</em> viene interpretato come <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>e i campi della struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> sono compilati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="5598c-131"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span> <span data-ttu-id="5598c-132">JET_ColInfo e JET_ColInfoByColid recuperano le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="5598c-132">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5598c-133">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="5598c-133">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="5598c-134"><em>pvResult</em> viene interpretato come una struttura <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> .</span><span class="sxs-lookup"><span data-stu-id="5598c-134"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="5598c-135">Questa operazione è simile a una struttura <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> .</span><span class="sxs-lookup"><span data-stu-id="5598c-135">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="5598c-136">Se questa funzione ha esito positivo, la struttura viene popolata con i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="5598c-136">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="5598c-137">Se questa funzione ha esito negativo, la struttura contiene dati non definiti.</span><span class="sxs-lookup"><span data-stu-id="5598c-137">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5598c-138">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="5598c-138">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="5598c-139"><em>pvResult</em> viene interpretato come <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, ad eccezione del fatto che questo <em>InfoLevel</em> indica che la colonna richiesta (<em>szColumName</em>) non è il nome della colonna stringa, ma un puntatore a una <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="5598c-139"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span> <span data-ttu-id="5598c-140">JET_ColInfo e JET_ColInfoByColid recuperano le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="5598c-140">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5598c-141">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="5598c-141">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="5598c-142"><em>pvResult</em> viene interpretato come una struttura <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="5598c-142"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="5598c-143">Se questa funzione ha esito positivo, la struttura viene popolata con i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="5598c-143">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="5598c-144">Viene aperta una tabella temporanea che viene identificata dal membro <em>TableID</em> del <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="5598c-144">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="5598c-145">La tabella deve essere chiusa con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="5598c-145">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="5598c-146">Se questa funzione ha esito negativo, la struttura contiene dati non definiti.</span><span class="sxs-lookup"><span data-stu-id="5598c-146">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5598c-147">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="5598c-147">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="5598c-148"><em>pvResult</em> viene interpretato come una struttura <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="5598c-148"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="5598c-149">Se questa funzione ha esito positivo, la struttura viene popolata con i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="5598c-149">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="5598c-150">Viene aperta una tabella temporanea che viene identificata dal membro <em>TableID</em> del <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="5598c-150">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="5598c-151">La tabella deve essere chiusa con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="5598c-151">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="5598c-152">Se questa funzione ha esito negativo, la struttura contiene dati non definiti.</span><span class="sxs-lookup"><span data-stu-id="5598c-152">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5598c-153">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="5598c-153">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="5598c-154">Come JET_ColInfoList, tuttavia, la tabella risultante viene ordinata in base a <em>ColumnID</em>, anziché al nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="5598c-154">Same as JET_ColInfoList, however the resulting table is sorted by <em>columnid</em>, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5598c-155">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="5598c-155">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="5598c-156">JET_ColInfoSysTabCursor è deprecato e l'uso di esso restituirà JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="5598c-156">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5598c-157">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="5598c-157">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="5598c-158">Come JET_ColInfoBase, <em>pvResult</em> viene interpretato come <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, ad eccezione del fatto che questo <em>InfoLevel</em> indica che la colonna richiesta (<em>szColumName</em>) non è il nome della colonna stringa, ma un puntatore a un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="5598c-158">Same as JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="5598c-159"><strong>Windows Vista:  </strong> Questa operazione è disponibile in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5598c-159"><strong>Windows Vista:  </strong>This is available in Windows Vista and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5598c-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="5598c-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="5598c-161">Restituire solo colonne non derivate (se la tabella è derivata da un modello).</span><span class="sxs-lookup"><span data-stu-id="5598c-161">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="5598c-162">Questo valore può essere logicamente o in <em>InfoLevel</em>quando il <em>InfoLevel</em> di base è JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="5598c-162">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="5598c-163"><strong>Windows Vista:  </strong> Questo valore è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5598c-163"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5598c-164">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="5598c-164">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="5598c-165">Restituisce solo il nome della colonna e il ColumnID di ogni colonna.</span><span class="sxs-lookup"><span data-stu-id="5598c-165">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="5598c-166">Questo valore può essere logicamente o in <em>InfoLevel</em>quando il <em>InfoLevel</em> di base è JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="5598c-166">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="5598c-167"><strong>Windows Vista:  </strong> Questo valore è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5598c-167"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5598c-168">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="5598c-168">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="5598c-169">Ordina elenco colonne restituite in base a ColumnID (l'impostazione predefinita consiste nell'ordinare l'elenco in base al nome della colonna).</span><span class="sxs-lookup"><span data-stu-id="5598c-169">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="5598c-170">Questo valore può essere logicamente o in <em>InfoLevel</em>quando il <em>InfoLevel</em> di base è JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="5598c-170">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="5598c-171"><strong>Windows Vista:  </strong> Questo valore è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5598c-171"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5598c-172">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5598c-172">Return Value</span></span>

<span data-ttu-id="5598c-173">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="5598c-173">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5598c-174">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="5598c-174">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5598c-175">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5598c-175">Return code</span></span></p></th>
<th><p><span data-ttu-id="5598c-176">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5598c-176">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5598c-177">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5598c-177">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5598c-178">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="5598c-178">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5598c-179">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="5598c-179">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="5598c-180">La colonna denominata <em>szColumnName</em> non è stata trovata nella tabella.</span><span class="sxs-lookup"><span data-stu-id="5598c-180">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5598c-181">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="5598c-181">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="5598c-182">È stato specificato un <em>InfoLevel</em> non valido.</span><span class="sxs-lookup"><span data-stu-id="5598c-182">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5598c-183">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="5598c-183">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="5598c-184">Questo errore può essere restituito se:</span><span class="sxs-lookup"><span data-stu-id="5598c-184">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="5598c-185">È stato specificato un nome non valido per <em>szTableName</em> .</span><span class="sxs-lookup"><span data-stu-id="5598c-185">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="5598c-186">È stato specificato un nome non valido per <em>szColumnName</em> .</span><span class="sxs-lookup"><span data-stu-id="5598c-186">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5598c-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5598c-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5598c-188">Questo errore può essere restituito se:</span><span class="sxs-lookup"><span data-stu-id="5598c-188">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="5598c-189">È stato specificato un <em>InfoLevel</em> non valido.</span><span class="sxs-lookup"><span data-stu-id="5598c-189">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="5598c-190">È stato passato un <em>SZTABLENAME</em> null.</span><span class="sxs-lookup"><span data-stu-id="5598c-190">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="5598c-191">Il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="5598c-191">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="5598c-192">Commenti</span><span class="sxs-lookup"><span data-stu-id="5598c-192">Remarks</span></span>

<span data-ttu-id="5598c-193">**JetGetTableColumnInfo** e [JetGetColumnInfo](./jetgetcolumninfo-function.md) recuperano entrambe le informazioni relative a una colonna.</span><span class="sxs-lookup"><span data-stu-id="5598c-193">**JetGetTableColumnInfo** and [JetGetColumnInfo](./jetgetcolumninfo-function.md) both retrieve information about a column.</span></span> <span data-ttu-id="5598c-194">La differenza tra di esse è la modalità di identificazione della tabella:</span><span class="sxs-lookup"><span data-stu-id="5598c-194">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="5598c-195">**JetGetTableColumnInfo** identifica una tabella in base a *TableID*.</span><span class="sxs-lookup"><span data-stu-id="5598c-195">**JetGetTableColumnInfo** identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="5598c-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifica una tabella in base alla combinazione *dbid* e *szTableName* .</span><span class="sxs-lookup"><span data-stu-id="5598c-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="5598c-197">Quando si recuperano dati con JET_ColInfoList, JET_ColInfoListSortColumnid o JET_ColInfoListCompact, viene aperta una tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="5598c-197">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="5598c-198">La tabella temporanea contiene dati e la struttura [JET_COLUMNLIST](./jet-columnlist-structure.md) contiene informazioni sufficienti per attraversare la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="5598c-198">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="5598c-199">La tabella temporanea deve essere chiusa con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="5598c-199">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5598c-200">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5598c-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5598c-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5598c-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5598c-202">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5598c-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5598c-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5598c-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5598c-204">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5598c-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5598c-205"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="5598c-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5598c-206">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="5598c-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5598c-207"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="5598c-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5598c-208">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5598c-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5598c-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5598c-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5598c-210">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5598c-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5598c-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5598c-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5598c-212">Implementato come <strong>JetGetTableColumnInfoW</strong> (Unicode) e <strong>JetGetTableColumnInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5598c-212">Implemented as <strong>JetGetTableColumnInfoW</strong> (Unicode) and <strong>JetGetTableColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5598c-213">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5598c-213">See Also</span></span>

[<span data-ttu-id="5598c-214">Errori del motore di archiviazione estendibile</span><span class="sxs-lookup"><span data-stu-id="5598c-214">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="5598c-215">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="5598c-215">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="5598c-216">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="5598c-216">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="5598c-217">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="5598c-217">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="5598c-218">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="5598c-218">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="5598c-219">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="5598c-219">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="5598c-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5598c-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5598c-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5598c-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5598c-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5598c-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5598c-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5598c-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5598c-224">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="5598c-224">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="5598c-225">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="5598c-225">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="5598c-226">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="5598c-226">JetGetTableColumnInfo</span></span>]()
