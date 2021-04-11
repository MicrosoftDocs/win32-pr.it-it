---
description: 'Altre informazioni su: funzione JetGetDatabaseInfo'
title: Funzione JetGetDatabaseInfo
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231800"
---
# <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="84083-103">Funzione JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="84083-103">JetGetDatabaseInfo Function</span></span>


<span data-ttu-id="84083-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="84083-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="84083-105">Funzione JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="84083-105">JetGetDatabaseInfo Function</span></span>

<span data-ttu-id="84083-106">La funzione **JetGetDatabaseInfo** recupera vari tipi di informazioni sul database.</span><span class="sxs-lookup"><span data-stu-id="84083-106">The **JetGetDatabaseInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="84083-107">Questa API può essere chiamata quando un database è collegato o in linea (con **JetGetDatabaseInfo**) o mentre il database o il motore di database è offline (con [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="84083-107">This API can be called while a database is attached or online (with **JetGetDatabaseInfo**) or while the database or database engine is offline (with [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="84083-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="84083-108">Parameters</span></span>

<span data-ttu-id="84083-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="84083-109">*sesid*</span></span>

<span data-ttu-id="84083-110">Sessione da utilizzare per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="84083-110">The session to use for this call.</span></span>

<span data-ttu-id="84083-111">*dbid*</span><span class="sxs-lookup"><span data-stu-id="84083-111">*dbid*</span></span>

<span data-ttu-id="84083-112">[JET_DBID](./jet-dbid.md) per il database da cui recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="84083-112">The [JET_DBID](./jet-dbid.md) for the database to retrieve the information from.</span></span>

<span data-ttu-id="84083-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="84083-113">*pvResult*</span></span>

<span data-ttu-id="84083-114">Puntatore a un buffer che riceverà le informazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="84083-114">Pointer to a buffer which will receive the specified information.</span></span> <span data-ttu-id="84083-115">La dimensione del buffer, in byte, viene passata in *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="84083-115">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="84083-116">In caso di errore, il contenuto di *pvResult* non è definito.</span><span class="sxs-lookup"><span data-stu-id="84083-116">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="84083-117">Le informazioni archiviate in *pvResult* dipendono da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="84083-117">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="84083-118">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="84083-118">*cbMax*</span></span>

<span data-ttu-id="84083-119">Dimensione, in byte, del buffer passato in *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="84083-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="84083-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="84083-120">*InfoLevel*</span></span>

<span data-ttu-id="84083-121">*InfoLevel* specifica il tipo di informazioni da recuperare sul database specificato.</span><span class="sxs-lookup"><span data-stu-id="84083-121">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="84083-122">Influiscono sul modo in cui *pvResult* viene interpretato.</span><span class="sxs-lookup"><span data-stu-id="84083-122">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="84083-123">Alcuni *InfoLevel* sono disponibili solo nella versione offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) o in linea (**JetGetDatabaseInfo**) dell'API.</span><span class="sxs-lookup"><span data-stu-id="84083-123">Some *InfoLevel* are available only in the offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) or online (**JetGetDatabaseInfo**) version of the API.</span></span>

<span data-ttu-id="84083-124">Se il buffer *pvResult* fornito è troppo piccolo, viene restituito JET_errInvalidBufferSize o JET_errBufferTooSmall a seconda del valore di *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="84083-124">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84083-125">Valore</span><span class="sxs-lookup"><span data-stu-id="84083-125">Value</span></span></p></th>
<th><p><span data-ttu-id="84083-126">Significato</span><span class="sxs-lookup"><span data-stu-id="84083-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84083-127">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="84083-127">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="84083-128">Non ancora supportato e restituisce i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="84083-128">Not yet supported and return default values.</span></span> <span data-ttu-id="84083-129">Non usare.</span><span class="sxs-lookup"><span data-stu-id="84083-129">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-130">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="84083-130">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="84083-131">Questi <em>InfoLevels</em> sono deprecati e non sono attualmente supportati.</span><span class="sxs-lookup"><span data-stu-id="84083-131">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="84083-132">Non usare.</span><span class="sxs-lookup"><span data-stu-id="84083-132">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-133">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="84083-133">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="84083-134">Non ancora supportato e restituisce i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="84083-134">Not yet supported and return default values.</span></span> <span data-ttu-id="84083-135">Non usare.</span><span class="sxs-lookup"><span data-stu-id="84083-135">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-136">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="84083-136">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="84083-137">Non ancora supportato e restituisce i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="84083-137">Not yet supported and return default values.</span></span> <span data-ttu-id="84083-138">Non usare.</span><span class="sxs-lookup"><span data-stu-id="84083-138">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-139">JET_DbInfoFilename</span><span class="sxs-lookup"><span data-stu-id="84083-139">JET_DbInfoFilename</span></span></p></td>
<td><p><span data-ttu-id="84083-140"><em>pvResult</em> verrà interpretato come un buffer di stringa (Char \*).</span><span class="sxs-lookup"><span data-stu-id="84083-140"><em>pvResult</em> will be interpreted as a string buffer (char \*).</span></span> <span data-ttu-id="84083-141">È stato suggerito un buffer di MAX_PATH, tuttavia non è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="84083-141">A MAX_PATH buffer is suggested, however not required.</span></span> <span data-ttu-id="84083-142">Se la lunghezza del buffer non è sufficiente, verrà restituito JET_errBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="84083-142">If the buffer is not long enough, JET_errBufferTooSmall will be returned.</span></span> <span data-ttu-id="84083-143">La stringa verrà popolata con il percorso del database per questo DBID.</span><span class="sxs-lookup"><span data-stu-id="84083-143">The string will be populated with the path of the database for this DBID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-144">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="84083-144">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="84083-145"><em>pvResult</em> verrà interpretato come un valore DWORD (4 byte).</span><span class="sxs-lookup"><span data-stu-id="84083-145"><em>pvResult</em> will be interpreted as a DWORD (4 bytes).</span></span> <span data-ttu-id="84083-146">Restituisce le dimensioni del database in pagine.</span><span class="sxs-lookup"><span data-stu-id="84083-146">Returns the size of the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-147">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="84083-147">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="84083-148">Questi <em>InfoLevels</em> sono deprecati e non sono attualmente supportati.</span><span class="sxs-lookup"><span data-stu-id="84083-148">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="84083-149">Non usare.</span><span class="sxs-lookup"><span data-stu-id="84083-149">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-150">JET_DbInfoLCID</span><span class="sxs-lookup"><span data-stu-id="84083-150">JET_DbInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="84083-151">(Windows XP e versioni successive) Questo <em>InfoLevel</em> è stato originariamente specificato come: JET_DbInfoLangid (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="84083-151">(Windows XP and later) This <em>InfoLevel</em> was originally specified as: JET_DbInfoLangid (Windows 2000)</span></span></p>
<p><span data-ttu-id="84083-152"><em>pvResult</em> verrà interpretato come Long.</span><span class="sxs-lookup"><span data-stu-id="84083-152"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="84083-153">Viene restituito l'identificatore delle impostazioni locali (LCID) associato al database.</span><span class="sxs-lookup"><span data-stu-id="84083-153">This returns the Locale identifier (LCID) associate with this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-154">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="84083-154">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="84083-155"><em>pvResult</em> verrà interpretato come <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span><span class="sxs-lookup"><span data-stu-id="84083-155"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="84083-156">La struttura di <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> verrà popolata con le informazioni relative al database specificato.</span><span class="sxs-lookup"><span data-stu-id="84083-156">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the database specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-157">JET_DbInfoOptions</span><span class="sxs-lookup"><span data-stu-id="84083-157">JET_DbInfoOptions</span></span></p></td>
<td><p><span data-ttu-id="84083-158"><em>pvResult</em> verrà interpretato come un <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span><span class="sxs-lookup"><span data-stu-id="84083-158"><em>pvResult</em> will be interpreted as a <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span></span> <span data-ttu-id="84083-159">Viene restituito un valore che indica se il database è aperto in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="84083-159">This returns whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="84083-160">Se il database è in modalità esclusiva JET_bitDbExclusive verrà impostato nell' <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> fornito; in caso contrario, viene impostato zero.</span><span class="sxs-lookup"><span data-stu-id="84083-160">If the database is in exclusive mode JET_bitDbExclusive will be set in the <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> provided, otherwise zero is set.</span></span> <span data-ttu-id="84083-161">Si noti che non vengono restituite altre opzioni di <em>grbit</em> del database per <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> e <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> .</span><span class="sxs-lookup"><span data-stu-id="84083-161">Note other database <em>grbit</em> options for <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> and <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> are not returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-162">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="84083-162">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="84083-163">Disponibile solo in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="84083-163">Available only on Windows XP and later.</span></span> <span data-ttu-id="84083-164"><em>pvResult</em> verrà interpretato come unsigned long.</span><span class="sxs-lookup"><span data-stu-id="84083-164"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="84083-165">Questa operazione restituirà le dimensioni di pagina del database in byte.</span><span class="sxs-lookup"><span data-stu-id="84083-165">This will return the page size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-166">JET_DbInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="84083-166">JET_DbInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="84083-167"><em>pvResult</em> verrà interpretato come un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="84083-167"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="84083-168">Viene restituito lo spazio disponibile per il database in pagine.</span><span class="sxs-lookup"><span data-stu-id="84083-168">This returns the available space for the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-169">JET_DbInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="84083-169">JET_DbInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="84083-170"><em>pvResult</em> verrà interpretato come un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="84083-170"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="84083-171">Viene restituito lo spazio di proprietà del database in pagine.</span><span class="sxs-lookup"><span data-stu-id="84083-171">This returns the owned space for the database in pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-172">JET_DbInfoTransactions</span><span class="sxs-lookup"><span data-stu-id="84083-172">JET_DbInfoTransactions</span></span></p></td>
<td><p><span data-ttu-id="84083-173"><em>pvResult</em> verrà interpretato come Long.</span><span class="sxs-lookup"><span data-stu-id="84083-173"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="84083-174">Verrà restituito un valore maggiore del livello massimo a cui è possibile annidare le transazioni.</span><span class="sxs-lookup"><span data-stu-id="84083-174">This will return one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="84083-175">Se viene chiamato <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> (in modo annidato, ovvero nella stessa sessione senza commit o rollback) il numero di volte di questo valore, nell'ultima chiamata JET_errTransTooDeep verrà restituito da <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span><span class="sxs-lookup"><span data-stu-id="84083-175">If <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call JET_errTransTooDeep will be returned from <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span></span> <span data-ttu-id="84083-176">Si noti che il valore in Windows 2000, Windows XP e Windows Server 2003 è 7.</span><span class="sxs-lookup"><span data-stu-id="84083-176">Note the value in Windows 2000, Windows XP, and Windows Server 2003 is 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-177">JET_DbInfoVersion</span><span class="sxs-lookup"><span data-stu-id="84083-177">JET_DbInfoVersion</span></span></p></td>
<td><p><span data-ttu-id="84083-178"><em>pvResult</em> verrà interpretato come Long.</span><span class="sxs-lookup"><span data-stu-id="84083-178"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="84083-179">Viene restituita la versione principale nativa del motore di database.</span><span class="sxs-lookup"><span data-stu-id="84083-179">This returns the database engine's native major version.</span></span> <span data-ttu-id="84083-180">Questo valore è 0x620 per Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="84083-180">This value is 0x620 for Windows 2000, Windows XP, and Windows Server 2003.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="84083-181">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84083-181">Return Value</span></span>

<span data-ttu-id="84083-182">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="84083-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="84083-183">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="84083-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84083-184">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="84083-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="84083-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84083-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84083-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="84083-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="84083-187">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="84083-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-188">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="84083-188">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="84083-189">La dimensione del buffer specificata in <em>cbMax</em> è troppo piccola (o non corretta) per conservare le informazioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="84083-189">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-190">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="84083-190">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="84083-191">Il <em>InfoLevel</em> richiesto è stato JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="84083-191">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="84083-192">Questo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="84083-192">This is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-193">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="84083-193">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="84083-194">La dimensione del buffer specificata in <em>cbMax</em> è troppo piccola (o non corretta) per conservare le informazioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="84083-194">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-195">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="84083-195">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="84083-196">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="84083-196">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="84083-197">Questo errore viene restituito da <strong>JetGetDatabaseInfo</strong> quando il <a href="gg269248(v=exchg.10).md">JET_DBID</a> specificato non è un database valido (collegato).</span><span class="sxs-lookup"><span data-stu-id="84083-197">This error will be returned by <strong>JetGetDatabaseInfo</strong> when the <a href="gg269248(v=exchg.10).md">JET_DBID</a> provided is not a valid (attached) database.</span></span> <span data-ttu-id="84083-198">Questo errore viene restituito da <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> e <strong>JetGetDatabaseInfo</strong> quando un <em>InfoLevel</em> richiesto non è supportato da tale versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="84083-198">This error will be returned by <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> and <strong>JetGetDatabaseInfo</strong> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84083-199">In seguito all'esito positivo, i dati richiesti verranno restituiti nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="84083-199">On success, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="84083-200">In caso di errore, il buffer di output sarà in uno stato non definito.</span><span class="sxs-lookup"><span data-stu-id="84083-200">On failure, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="84083-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84083-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84083-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="84083-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="84083-203">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="84083-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="84083-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="84083-205">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="84083-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-206"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="84083-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="84083-207">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="84083-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-208"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="84083-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="84083-209">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="84083-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84083-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="84083-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="84083-211">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="84083-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84083-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="84083-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="84083-213">Implementato come <strong>JetGetDatabaseInfoW</strong> (Unicode) e <strong>JetGetDatabaseInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="84083-213">Implemented as <strong>JetGetDatabaseInfoW</strong> (Unicode) and <strong>JetGetDatabaseInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="84083-214">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="84083-214">See Also</span></span>

[<span data-ttu-id="84083-215">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="84083-215">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="84083-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="84083-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="84083-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="84083-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="84083-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="84083-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="84083-219">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="84083-219">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="84083-220">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="84083-220">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="84083-221">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="84083-221">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
