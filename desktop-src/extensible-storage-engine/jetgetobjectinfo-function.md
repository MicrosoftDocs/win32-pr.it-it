---
description: 'Altre informazioni su: funzione JetGetObjectInfo'
title: Funzione JetGetObjectInfo
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313101"
---
# <a name="jetgetobjectinfo-function"></a><span data-ttu-id="ae239-103">Funzione JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="ae239-103">JetGetObjectInfo Function</span></span>


<span data-ttu-id="ae239-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ae239-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetobjectinfo-function"></a><span data-ttu-id="ae239-105">Funzione JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="ae239-105">JetGetObjectInfo Function</span></span>

<span data-ttu-id="ae239-106">La funzione **JetGetObjectInfo** recupera le informazioni sugli oggetti di database.</span><span class="sxs-lookup"><span data-stu-id="ae239-106">The **JetGetObjectInfo** function retrieves information about database objects.</span></span> <span data-ttu-id="ae239-107">Attualmente sono supportate solo le tabelle.</span><span class="sxs-lookup"><span data-stu-id="ae239-107">Currently, only tables are supported.</span></span> <span data-ttu-id="ae239-108">[JetGetTableInfo](./jetgettableinfo-function.md) può essere usato per recuperare altre informazioni rispetto a **JetGetObjectInfo**.</span><span class="sxs-lookup"><span data-stu-id="ae239-108">[JetGetTableInfo](./jetgettableinfo-function.md) can be used to fetch more information than **JetGetObjectInfo**.</span></span>

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="ae239-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae239-109">Parameters</span></span>

<span data-ttu-id="ae239-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ae239-110">*sesid*</span></span>

<span data-ttu-id="ae239-111">Contesto della sessione di database da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="ae239-111">The database session context to use.</span></span>

<span data-ttu-id="ae239-112">*dbid*</span><span class="sxs-lookup"><span data-stu-id="ae239-112">*dbid*</span></span>

<span data-ttu-id="ae239-113">Database da cui vengono recuperate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="ae239-113">The database from which the information is retrieved.</span></span>

<span data-ttu-id="ae239-114">*objtyp*</span><span class="sxs-lookup"><span data-stu-id="ae239-114">*objtyp*</span></span>

<span data-ttu-id="ae239-115">Oggetti che contengono informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ae239-115">The objects that contain information to be retrieved.</span></span> <span data-ttu-id="ae239-116">Attualmente sono supportate solo JET_objtypNil e JET_objtypTable, entrambe comportano in modo identico.</span><span class="sxs-lookup"><span data-stu-id="ae239-116">Currently, only JET_objtypNil and JET_objtypTable are supported, both of which behave identically.</span></span> <span data-ttu-id="ae239-117">Verranno recuperate solo le tabelle.</span><span class="sxs-lookup"><span data-stu-id="ae239-117">Only tables will be retrieved.</span></span>

<span data-ttu-id="ae239-118">*szContainerName*</span><span class="sxs-lookup"><span data-stu-id="ae239-118">*szContainerName*</span></span>

<span data-ttu-id="ae239-119">Questo parametro è riservato per utilizzi futuri e passa **null**.</span><span class="sxs-lookup"><span data-stu-id="ae239-119">This parameter is reserved for future use and passes **NULL**.</span></span> <span data-ttu-id="ae239-120">Nome dei tipi di oggetti sui quali recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="ae239-120">The name of the types of objects about which to retrieve information.</span></span>

<span data-ttu-id="ae239-121">*szObjectName*</span><span class="sxs-lookup"><span data-stu-id="ae239-121">*szObjectName*</span></span>

<span data-ttu-id="ae239-122">Nome dell'oggetto che contiene le informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ae239-122">The name of the object that contains information to retrieve.</span></span> <span data-ttu-id="ae239-123">Quando *InfoLevel* usa le opzioni JET_ObjInfoList o JET_ObjInfoListNoStats per recuperare un elenco di tutti gli oggetti, questo valore deve essere **null** o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="ae239-123">When *InfoLevel* uses the JET_ObjInfoList or JET_ObjInfoListNoStats options to retrieve a list of all objects, this value should be **NULL** or an empty string.</span></span>

<span data-ttu-id="ae239-124">Attualmente sono supportati solo i nomi di tabella.</span><span class="sxs-lookup"><span data-stu-id="ae239-124">Only table names are currently supported.</span></span>

<span data-ttu-id="ae239-125">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="ae239-125">*pvResult*</span></span>

<span data-ttu-id="ae239-126">Puntatore a un buffer che riceve le informazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="ae239-126">Pointer to a buffer which receives the specified information.</span></span>

<span data-ttu-id="ae239-127">La dimensione del buffer, in byte, viene passata in *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="ae239-127">The size of the buffer, in bytes, is passed in *cbMax*.</span></span> <span data-ttu-id="ae239-128">In caso di errore, il contenuto di *pvResult* non è definito.</span><span class="sxs-lookup"><span data-stu-id="ae239-128">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="ae239-129">Le informazioni archiviate in *pvResult* dipendono da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="ae239-129">The information that is stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="ae239-130">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="ae239-130">*cbMax*</span></span>

<span data-ttu-id="ae239-131">Dimensione, in byte, del buffer passato in *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="ae239-131">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="ae239-132">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="ae239-132">*InfoLevel*</span></span>

<span data-ttu-id="ae239-133">Specifica il tipo di informazioni da recuperare per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="ae239-133">Specifies which type of information to retrieve for the specified object.</span></span> <span data-ttu-id="ae239-134">Influiscono sul modo in cui *pvResult* viene interpretato.</span><span class="sxs-lookup"><span data-stu-id="ae239-134">It affects how *pvResult* is interpreted.</span></span>

<span data-ttu-id="ae239-135">Le opzioni seguenti sono disponibili per l'impostazione di questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ae239-135">The following options are available to set for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae239-136">Valore</span><span class="sxs-lookup"><span data-stu-id="ae239-136">Value</span></span></p></th>
<th><p><span data-ttu-id="ae239-137">Significato</span><span class="sxs-lookup"><span data-stu-id="ae239-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae239-138">JET_ObjInfo</span><span class="sxs-lookup"><span data-stu-id="ae239-138">JET_ObjInfo</span></span></p></td>
<td><p><span data-ttu-id="ae239-139"><em>pvResult</em> viene interpretato come una struttura <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="ae239-139"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span></p>
<p><span data-ttu-id="ae239-140">La struttura <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> viene popolata con le informazioni relative all'oggetto denominato in <em>szObjectName</em>.</span><span class="sxs-lookup"><span data-stu-id="ae239-140">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="ae239-141">Se il chiamante non desidera determinare il numero di record e pagine per l'oggetto, è consigliabile utilizzare JET_ObjInfoNoStats livello di informazioni, che potrebbe essere più veloce poiché le statistiche non vengono incluse.</span><span class="sxs-lookup"><span data-stu-id="ae239-141">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoNoStats information level, which might be faster since statistics are not included.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae239-142">JET_ObjInfoList</span><span class="sxs-lookup"><span data-stu-id="ae239-142">JET_ObjInfoList</span></span></p></td>
<td><p><span data-ttu-id="ae239-143"><em>pvResult</em> viene interpretato come una struttura <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="ae239-143"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="ae239-144">Vengono recuperate informazioni su tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="ae239-144">Information about all objects is retrieved.</span></span> <span data-ttu-id="ae239-145">Verrà creata una tabella temporanea e le informazioni necessarie per attraversare la tabella temporanea sono descritte nella struttura <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="ae239-145">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="ae239-146">Per ulteriori informazioni, vedere <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="ae239-146">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="ae239-147">Se il chiamante non desidera ottenere informazioni sul numero di record e pagine per l'oggetto, provare a utilizzare JET_ObjInfoListNoStats, che potrebbe essere più veloce.</span><span class="sxs-lookup"><span data-stu-id="ae239-147">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoListNoStats, which might be faster.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae239-148">JET_ObjInfoListACM</span><span class="sxs-lookup"><span data-stu-id="ae239-148">JET_ObjInfoListACM</span></span></p></td>
<td><p><span data-ttu-id="ae239-149">Deprecato e attualmente non supportato.</span><span class="sxs-lookup"><span data-stu-id="ae239-149">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae239-150">JET_ObjInfoListNoStats</span><span class="sxs-lookup"><span data-stu-id="ae239-150">JET_ObjInfoListNoStats</span></span></p></td>
<td><p><span data-ttu-id="ae239-151"><em>pvResult</em> viene interpretato come una struttura <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="ae239-151"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="ae239-152">Vengono recuperate informazioni su tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="ae239-152">Information about all objects is retrieved.</span></span> <span data-ttu-id="ae239-153">Verrà creata una tabella temporanea e le informazioni necessarie per attraversare la tabella temporanea sono descritte nella struttura <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="ae239-153">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="ae239-154">Per ulteriori informazioni, vedere <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="ae239-154">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="ae239-155">JET_ObjInfoListNoStats è identico a JET_ObjInfoList, ad eccezione del fatto che le colonne che segnalano il numero di record (<em>columnidcRecord</em>) e le pagine (<em>columnidcPage</em>) non verranno aggiornate.</span><span class="sxs-lookup"><span data-stu-id="ae239-155">JET_ObjInfoListNoStats is identical to JET_ObjInfoList, except that the columns that report the number of records (<em>columnidcRecord</em>) and pages (<em>columnidcPage</em>) will not be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae239-156">JET_ObjInfoMax</span><span class="sxs-lookup"><span data-stu-id="ae239-156">JET_ObjInfoMax</span></span></p></td>
<td><p><span data-ttu-id="ae239-157"><em>pvResult</em> viene interpretato come <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="ae239-157"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="ae239-158">Le dimensioni massime dell'oggetto sono in pagine.</span><span class="sxs-lookup"><span data-stu-id="ae239-158">The maximum size of the object is in pages.</span></span> <span data-ttu-id="ae239-159">Attualmente verranno restituite solo le tabelle.</span><span class="sxs-lookup"><span data-stu-id="ae239-159">Currently only tables will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae239-160">JET_ObjInfoNoStats</span><span class="sxs-lookup"><span data-stu-id="ae239-160">JET_ObjInfoNoStats</span></span></p></td>
<td><p><span data-ttu-id="ae239-161"><em>pvResult</em> viene interpretato come <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="ae239-161"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="ae239-162">Verranno recuperate solo le informazioni relative all'oggetto fornito in <em>szObjectName</em> .</span><span class="sxs-lookup"><span data-stu-id="ae239-162">Information about only the object given in <em>szObjectName</em> will be retrieved.</span></span></p>
<p><span data-ttu-id="ae239-163">La struttura di <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> verrà popolata con informazioni relative all'oggetto denominato in <em>szObjectName</em>.</span><span class="sxs-lookup"><span data-stu-id="ae239-163">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure will be populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="ae239-164">JET_ObjInfoNoStats è identico a JET_ObjInfo, ad eccezione del fatto che i campi che segnalano il numero di record e le pagine sono impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="ae239-164">JET_ObjInfoNoStats is identical to JET_ObjInfo, except that the fields that report the number of records and pages are set to zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae239-165">JET_ObjInfoRulesLoaded</span><span class="sxs-lookup"><span data-stu-id="ae239-165">JET_ObjInfoRulesLoaded</span></span></p></td>
<td><p><span data-ttu-id="ae239-166">Deprecato e attualmente non supportato.</span><span class="sxs-lookup"><span data-stu-id="ae239-166">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae239-167">JET_ObjInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="ae239-167">JET_ObjInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="ae239-168">Deprecato e attualmente non supportato.</span><span class="sxs-lookup"><span data-stu-id="ae239-168">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae239-169">JET_ObjInfoSysTabReadOnly</span><span class="sxs-lookup"><span data-stu-id="ae239-169">JET_ObjInfoSysTabReadOnly</span></span></p></td>
<td><p><span data-ttu-id="ae239-170">Deprecato e attualmente non supportato.</span><span class="sxs-lookup"><span data-stu-id="ae239-170">Deprecated and not currently supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ae239-171">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae239-171">Return Value</span></span>

<span data-ttu-id="ae239-172">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="ae239-172">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ae239-173">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ae239-173">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae239-174">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ae239-174">Return code</span></span></p></th>
<th><p><span data-ttu-id="ae239-175">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae239-175">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae239-176">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ae239-176">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ae239-177">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="ae239-177">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae239-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="ae239-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="ae239-179">La dimensione del buffer specificata in <em>cbMax</em> è troppo piccola per conservare le informazioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="ae239-179">The size of the buffer given in <em>cbMax</em> was too small to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae239-180">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="ae239-180">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="ae239-181">È stato specificato un nome non valido in <em>szObjectName</em> o <em>szContainerName</em>.</span><span class="sxs-lookup"><span data-stu-id="ae239-181">An invalid name was given in <em>szObjectName</em> or <em>szContainerName</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae239-182">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ae239-182">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ae239-183">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="ae239-183">A bad parameter was given.</span></span> <span data-ttu-id="ae239-184">È possibile che sia stato passato un livello non valido a <em>InfoLevel</em>.</span><span class="sxs-lookup"><span data-stu-id="ae239-184">It is possible that a bad level was passed in to <em>InfoLevel</em>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ae239-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae239-185">Remarks</span></span>

<span data-ttu-id="ae239-186">Se **JetGetObjectInfo** crea correttamente una tabella temporanea, ad esempio JET_ObjInfoList o JET_ObjInfoNoStats, il chiamante è responsabile della chiusura della tabella temporanea con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="ae239-186">If **JetGetObjectInfo** successfully creates a temporary table (for example, JET_ObjInfoList or JET_ObjInfoNoStats), the caller is responsible for closing the temporary table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="ae239-187">**JetGetObjectInfo** supporta attualmente solo il recupero di informazioni sulle tabelle.</span><span class="sxs-lookup"><span data-stu-id="ae239-187">**JetGetObjectInfo** currently only supports retrieving information about tables.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ae239-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae239-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae239-189"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ae239-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ae239-190">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ae239-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae239-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ae239-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ae239-192">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ae239-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae239-193"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ae239-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ae239-194">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ae239-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae239-195"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="ae239-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ae239-196">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ae239-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae239-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ae239-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ae239-198">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ae239-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae239-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ae239-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ae239-200">Implementato come <strong>JetGetObjectInfoW</strong> (Unicode) e <strong>JetGetObjectInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ae239-200">Implemented as <strong>JetGetObjectInfoW</strong> (Unicode) and <strong>JetGetObjectInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ae239-201">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ae239-201">See Also</span></span>

[<span data-ttu-id="ae239-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ae239-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ae239-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ae239-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ae239-204">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="ae239-204">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="ae239-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ae239-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ae239-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ae239-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ae239-207">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="ae239-207">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="ae239-208">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="ae239-208">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="ae239-209">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="ae239-209">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="ae239-210">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="ae239-210">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
