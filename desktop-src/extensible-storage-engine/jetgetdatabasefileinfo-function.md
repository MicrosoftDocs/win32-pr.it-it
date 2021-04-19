---
description: 'Altre informazioni su: funzione JetGetDatabaseFileInfo'
title: JetGetDatabaseFileInfo (funzione)
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319632"
---
# <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="c7363-103">JetGetDatabaseFileInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="c7363-103">JetGetDatabaseFileInfo Function</span></span>


<span data-ttu-id="c7363-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c7363-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="c7363-105">JetGetDatabaseFileInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="c7363-105">JetGetDatabaseFileInfo Function</span></span>

<span data-ttu-id="c7363-106">La funzione **JetGetDatabaseFileInfo** recupera vari tipi di informazioni sul database.</span><span class="sxs-lookup"><span data-stu-id="c7363-106">The **JetGetDatabaseFileInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="c7363-107">Questa API può essere chiamata quando un database è collegato o in linea (con [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) o mentre il database o il motore di database è offline (con **JetGetDatabaseFileInfo**).</span><span class="sxs-lookup"><span data-stu-id="c7363-107">This API can be called while a database is attached or online (with [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) or while the database or database engine is offline (with **JetGetDatabaseFileInfo**).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="c7363-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7363-108">Parameters</span></span>

<span data-ttu-id="c7363-109">*szDatabaseName*</span><span class="sxs-lookup"><span data-stu-id="c7363-109">*szDatabaseName*</span></span>

<span data-ttu-id="c7363-110">Percorso del database da cui recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="c7363-110">The path of the database from which to retrieve the information.</span></span>

<span data-ttu-id="c7363-111">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="c7363-111">*pvResult*</span></span>

<span data-ttu-id="c7363-112">Puntatore a un buffer che riceverà le informazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="c7363-112">Pointer to a buffer that will receive the specified information.</span></span> <span data-ttu-id="c7363-113">La dimensione del buffer, in byte, viene passata in *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="c7363-113">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="c7363-114">Se questa funzione ha esito negativo, il contenuto di *pvResult* non è definito.</span><span class="sxs-lookup"><span data-stu-id="c7363-114">If this function fails, the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="c7363-115">Le informazioni archiviate in *pvResult* dipendono da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="c7363-115">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="c7363-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="c7363-116">*cbMax*</span></span>

<span data-ttu-id="c7363-117">Dimensione, in byte, del buffer passato in *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="c7363-117">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="c7363-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="c7363-118">*InfoLevel*</span></span>

<span data-ttu-id="c7363-119">*InfoLevel* specifica il tipo di informazioni da recuperare sul database specificato.</span><span class="sxs-lookup"><span data-stu-id="c7363-119">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="c7363-120">Influiscono sul modo in cui *pvResult* viene interpretato.</span><span class="sxs-lookup"><span data-stu-id="c7363-120">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="c7363-121">Alcuni oggetti *InfoLevel* sono disponibili solo nella versione offline (**JetGetDatabaseFileInfo**) o in linea ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) dell'API.</span><span class="sxs-lookup"><span data-stu-id="c7363-121">Some *InfoLevel* objects are available only in the offline (**JetGetDatabaseFileInfo**) or online ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) version of the API.</span></span>

<span data-ttu-id="c7363-122">Se il buffer di *pvResult* fornito è troppo piccolo, viene restituito JET_errInvalidBufferSize o JET_errBufferTooSmall, a seconda del valore di *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="c7363-122">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned, depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7363-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c7363-123">Value</span></span></p></th>
<th><p><span data-ttu-id="c7363-124">Significato</span><span class="sxs-lookup"><span data-stu-id="c7363-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7363-125">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="c7363-125">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="c7363-126"><em>pvResult</em> verrà interpretato come QWORD (8 byte).</span><span class="sxs-lookup"><span data-stu-id="c7363-126"><em>pvResult</em> will be interpreted as a QWORD (8 bytes).</span></span> <span data-ttu-id="c7363-127">Restituisce le dimensioni in byte del database.</span><span class="sxs-lookup"><span data-stu-id="c7363-127">Returns the size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-128">JET_DbInfoUpgrade</span><span class="sxs-lookup"><span data-stu-id="c7363-128">JET_DbInfoUpgrade</span></span></p></td>
<td><p><span data-ttu-id="c7363-129"><em>pvResult</em> verrà interpretato come <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span><span class="sxs-lookup"><span data-stu-id="c7363-129"><em>pvResult</em> will be interpreted as a <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span></span> <span data-ttu-id="c7363-130">La struttura di <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> verrà popolata con le informazioni relative al database specificato.</span><span class="sxs-lookup"><span data-stu-id="c7363-130">The <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-131">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="c7363-131">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="c7363-132"><em>pvResult</em> verrà interpretato come <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span><span class="sxs-lookup"><span data-stu-id="c7363-132"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="c7363-133">La struttura di <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> verrà popolata con le informazioni relative al database specificato.</span><span class="sxs-lookup"><span data-stu-id="c7363-133">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-134">JET_DbInfoDBInUse</span><span class="sxs-lookup"><span data-stu-id="c7363-134">JET_DbInfoDBInUse</span></span></p></td>
<td><p><span data-ttu-id="c7363-135"><em>pvResult</em> verrà interpretato come bool (4 byte).</span><span class="sxs-lookup"><span data-stu-id="c7363-135"><em>pvResult</em> will be interpreted as a BOOL (4 bytes).</span></span> <span data-ttu-id="c7363-136">Verrà restituito un valore che indica se il motore di database dispone attualmente di database aperti o collegati.</span><span class="sxs-lookup"><span data-stu-id="c7363-136">This will return whether the database engine currently has any open or attached databases.</span></span></p>
<p><span data-ttu-id="c7363-137"><strong>Windows XP:  </strong> Questo valore è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c7363-137"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-138">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="c7363-138">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="c7363-139"><em>pvResult</em> verrà interpretato come unsigned long.</span><span class="sxs-lookup"><span data-stu-id="c7363-139"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="c7363-140">Questa operazione restituirà le dimensioni di pagina del database in byte.</span><span class="sxs-lookup"><span data-stu-id="c7363-140">This will return the page size of the database in bytes.</span></span></p>
<p><span data-ttu-id="c7363-141"><strong>Windows XP:  </strong> Questo valore è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c7363-141"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-142">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="c7363-142">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="c7363-143">Questi <em>InfoLevels</em> non sono ancora supportati e restituiscono valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c7363-143">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="c7363-144">Non usare questi <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="c7363-144">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-145">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="c7363-145">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="c7363-146">Questi <em>InfoLevels</em> non sono ancora supportati e restituiscono valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c7363-146">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="c7363-147">Non usare questi <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="c7363-147">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-148">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="c7363-148">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="c7363-149">Uguale a JET_DbInfoCp.</span><span class="sxs-lookup"><span data-stu-id="c7363-149">Same as JET_DbInfoCp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-150">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="c7363-150">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="c7363-151">Questi <em>InfoLevels</em> sono deprecati e non sono attualmente supportati.</span><span class="sxs-lookup"><span data-stu-id="c7363-151">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="c7363-152">Non usare questi <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="c7363-152">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-153">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="c7363-153">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="c7363-154">Uguale a JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="c7363-154">Same as JET_DbInfoIsam.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-155">JET_DbInfoFileType</span><span class="sxs-lookup"><span data-stu-id="c7363-155">JET_DbInfoFileType</span></span></p></td>
<td><p><span data-ttu-id="c7363-156"><strong>Windows Vista:  </strong> Questo valore <em>InfoLevel</em> è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c7363-156"><strong>Windows Vista:  </strong>This <em>InfoLevel</em> value is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="c7363-157"><em>pvResult</em> verrà considerato un puntatore a un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="c7363-157"><em>pvResult</em> will be treated as a pointer to a DWORD.</span></span> <span data-ttu-id="c7363-158">Restituisce un valore di enumerazione che indica il tipo di file considerato dal motore.</span><span class="sxs-lookup"><span data-stu-id="c7363-158">Returns an enumeration value, indicating what kind of file the engine considers this to be.</span></span> <span data-ttu-id="c7363-159">I tipi di file sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c7363-159">File types are listed in the following table.</span></span> <span data-ttu-id="c7363-160">Per altre informazioni su questi tipi di file e sul relativo utilizzo al motore, vedere <a href="gg294069(v=exchg.10).md">file del motore di archiviazione estensibile</a>.</span><span class="sxs-lookup"><span data-stu-id="c7363-160">For more information about these types of files and their usage to the engine, see <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7363-161">Valore</span><span class="sxs-lookup"><span data-stu-id="c7363-161">Value</span></span></p></th>
<th><p><span data-ttu-id="c7363-162">Significato</span><span class="sxs-lookup"><span data-stu-id="c7363-162">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7363-163">JET_filetypeUnknown</span><span class="sxs-lookup"><span data-stu-id="c7363-163">JET_filetypeUnknown</span></span></p></td>
<td><p><span data-ttu-id="c7363-164">Il tipo di file è sconosciuto o non è un tipo di file ESE.</span><span class="sxs-lookup"><span data-stu-id="c7363-164">The type of file is unknown, or not an ESE file type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-165">JET_filetypeDatabase</span><span class="sxs-lookup"><span data-stu-id="c7363-165">JET_filetypeDatabase</span></span></p></td>
<td><p><span data-ttu-id="c7363-166">Il file è un file di database.</span><span class="sxs-lookup"><span data-stu-id="c7363-166">The file is a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-167">JET_filetypeLog</span><span class="sxs-lookup"><span data-stu-id="c7363-167">JET_filetypeLog</span></span></p></td>
<td><p><span data-ttu-id="c7363-168">Il file è un file di log delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="c7363-168">The file is a transaction log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-169">JET_filetypeCheckpoint</span><span class="sxs-lookup"><span data-stu-id="c7363-169">JET_filetypeCheckpoint</span></span></p></td>
<td><p><span data-ttu-id="c7363-170">Il file è un file del checkpoint.</span><span class="sxs-lookup"><span data-stu-id="c7363-170">The file is a checkpoint file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-171">JET_filetypeTempDatabase</span><span class="sxs-lookup"><span data-stu-id="c7363-171">JET_filetypeTempDatabase</span></span></p></td>
<td><p><span data-ttu-id="c7363-172">Il file è un file di database temporaneo.</span><span class="sxs-lookup"><span data-stu-id="c7363-172">The file is a temporary database file.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c7363-173">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7363-173">Return Value</span></span>

<span data-ttu-id="c7363-174">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="c7363-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c7363-175">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="c7363-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7363-176">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c7363-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="c7363-177">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7363-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7363-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c7363-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c7363-179">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c7363-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-180">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="c7363-180">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="c7363-181">Il <em>InfoLevel</em> richiesto è stato JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="c7363-181">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="c7363-182">Questo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c7363-182">This is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-183">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="c7363-183">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="c7363-184">Il buffer fornito in <em>cbMax</em> è troppo piccolo per le informazioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="c7363-184">The buffer that is given in <em>cbMax</em> is too small for the desired information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-185">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="c7363-185">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="c7363-186">Il buffer fornito in <em>cbMax</em> non è la dimensione corretta per le informazioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="c7363-186">The buffer that is given in <em>cbMax</em> is not the correct size for the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c7363-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c7363-188">Uno dei parametri forniti contiene un valore imprevisto o la combinazione di diversi valori di parametro ha restituito un risultato imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c7363-188">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="c7363-189">Questo errore viene restituito da <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> quando DBID specificato non è un database valido (collegato).</span><span class="sxs-lookup"><span data-stu-id="c7363-189">This error will be returned by <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when the DBID provided is not a valid (attached) database.</span></span> <span data-ttu-id="c7363-190">Questo errore viene restituito da <strong>JetGetDatabaseFileInfo</strong> e <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> quando un <em>InfoLevel</em> richiesto non è supportato da tale versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="c7363-190">This error will be returned by <strong>JetGetDatabaseFileInfo</strong> and <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c7363-191">Se questa funzione ha esito positivo, i dati richiesti verranno restituiti nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="c7363-191">If this function succeeds, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="c7363-192">Se questa funzione ha esito negativo, il buffer di output sarà in uno stato non definito.</span><span class="sxs-lookup"><span data-stu-id="c7363-192">If this function fails, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c7363-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7363-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7363-194"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c7363-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c7363-195">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c7363-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c7363-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c7363-197">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c7363-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-198"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c7363-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c7363-199">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c7363-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-200"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="c7363-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c7363-201">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c7363-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7363-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c7363-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c7363-203">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c7363-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7363-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c7363-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c7363-205">Implementato come <strong>JetGetDatabaseFileInfoW</strong> (Unicode) e <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c7363-205">Implemented as <strong>JetGetDatabaseFileInfoW</strong> (Unicode) and <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c7363-206">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c7363-206">See Also</span></span>

[<span data-ttu-id="c7363-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c7363-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c7363-208">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="c7363-208">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="c7363-209">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="c7363-209">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="c7363-210">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="c7363-210">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)
