---
description: 'Altre informazioni su: funzione JetGetTableIndexInfo'
title: Funzione JetGetTableIndexInfo
TOCTitle: JetGetTableIndexInfo Function
ms:assetid: d250d254-2b10-4fe7-bbb1-72bb967f22dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294102(v=EXCHG.10)
ms:contentKeyID: 32765717
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableIndexInfoW
- JetGetTableIndexInfoA
- JetGetTableIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 904391218fbd073cd273655ce74fdec116b6a22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234092"
---
# <a name="jetgettableindexinfo-function"></a><span data-ttu-id="22a46-103">Funzione JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="22a46-103">JetGetTableIndexInfo Function</span></span>


<span data-ttu-id="22a46-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="22a46-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableindexinfo-function"></a><span data-ttu-id="22a46-105">Funzione JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="22a46-105">JetGetTableIndexInfo Function</span></span>

<span data-ttu-id="22a46-106">La funzione **JetGetTableIndexInfo** recupera le informazioni su un indice.</span><span class="sxs-lookup"><span data-stu-id="22a46-106">The **JetGetTableIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetTableIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="22a46-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="22a46-107">Parameters</span></span>

<span data-ttu-id="22a46-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="22a46-108">*sesid*</span></span>

<span data-ttu-id="22a46-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="22a46-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="22a46-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="22a46-110">*tableid*</span></span>

<span data-ttu-id="22a46-111">Tabella di database che contiene l'indice che contiene le informazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="22a46-111">The database table that contains the index that holds the needed information.</span></span>

<span data-ttu-id="22a46-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="22a46-112">*szIndexName*</span></span>

<span data-ttu-id="22a46-113">Nome dell'indice contenente le informazioni che verranno recuperate.</span><span class="sxs-lookup"><span data-stu-id="22a46-113">The name of the index that contains information that will be retrieved.</span></span>

<span data-ttu-id="22a46-114">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="22a46-114">*pvResult*</span></span>

<span data-ttu-id="22a46-115">Puntatore a un buffer che riceverà le informazioni.</span><span class="sxs-lookup"><span data-stu-id="22a46-115">Pointer to a buffer which will receive the information.</span></span> <span data-ttu-id="22a46-116">Il buffer deve essere allineato per contenere il tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="22a46-116">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="22a46-117">Il tipo del buffer dipende dal parametro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="22a46-117">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="22a46-118">*cbResult*</span><span class="sxs-lookup"><span data-stu-id="22a46-118">*cbResult*</span></span>

<span data-ttu-id="22a46-119">Dimensione, in byte, del buffer passato nel parametro *pvResult* .</span><span class="sxs-lookup"><span data-stu-id="22a46-119">The size, in bytes, of the buffer passed in the *pvResult* parameter.</span></span>

<span data-ttu-id="22a46-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="22a46-120">*InfoLevel*</span></span>

<span data-ttu-id="22a46-121">Specifica le informazioni che verranno archiviate in *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="22a46-121">Specifies which information will be stored in *pvResult*.</span></span> <span data-ttu-id="22a46-122">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="22a46-122">The valid values are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22a46-123">Valore</span><span class="sxs-lookup"><span data-stu-id="22a46-123">Value</span></span></p></th>
<th><p><span data-ttu-id="22a46-124">Significato</span><span class="sxs-lookup"><span data-stu-id="22a46-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22a46-125">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="22a46-125">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="22a46-126"><em>pvResult</em> viene interpretato come una struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="22a46-126"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="22a46-127">In seguito all'esito positivo, la struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> riceve informazioni sull'indice.</span><span class="sxs-lookup"><span data-stu-id="22a46-127">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="22a46-128">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-128">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-129">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="22a46-129">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="22a46-130"><em>pvResult</em> viene interpretato come un identificatore LCID.</span><span class="sxs-lookup"><span data-stu-id="22a46-130"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="22a46-131">In seguito all'esito positivo, l'LCID include l'identificatore delle impostazioni locali dell'indice.</span><span class="sxs-lookup"><span data-stu-id="22a46-131">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="22a46-132">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-132">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a46-133">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="22a46-133">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="22a46-134"><em>pvResult</em> viene interpretato come una struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="22a46-134"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="22a46-135">In seguito all'esito positivo, la struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> riceve informazioni sull'indice.</span><span class="sxs-lookup"><span data-stu-id="22a46-135">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="22a46-136">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-136">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-137">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="22a46-137">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="22a46-138">JET_IdxInfoOLC è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="22a46-138">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a46-139">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="22a46-139">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="22a46-140">JET_IdxInfoResetOLC è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="22a46-140">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-141">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="22a46-141">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="22a46-142"><em>pvResult</em> viene interpretato come ulong.</span><span class="sxs-lookup"><span data-stu-id="22a46-142"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="22a46-143">In seguito all'esito positivo, ULONG determinerà l'utilizzo dello spazio dell'indice.</span><span class="sxs-lookup"><span data-stu-id="22a46-143">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="22a46-144">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-144">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a46-145">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="22a46-145">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="22a46-146">JET_IdxInfoSysTabCursor è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="22a46-146">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-147">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="22a46-147">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="22a46-148">JET_IdxInfoLangid è deprecato.</span><span class="sxs-lookup"><span data-stu-id="22a46-148">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="22a46-149">In alternativa, usare JET_IdxInfoLCID e la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</span><span class="sxs-lookup"><span data-stu-id="22a46-149">Use JET_IdxInfoLCID instead, and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a46-150">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="22a46-150">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="22a46-151"><em>pvResult</em> viene interpretato come ulong.</span><span class="sxs-lookup"><span data-stu-id="22a46-151"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="22a46-152">In seguito all'esito positivo, ULONG include il conteggio degli indici nella tabella specificata.</span><span class="sxs-lookup"><span data-stu-id="22a46-152">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="22a46-153"><em>szIndexName</em> viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="22a46-153"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="22a46-154">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-154">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-155">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="22a46-155">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="22a46-156"><em>pvResult</em> viene interpretato come UShort.</span><span class="sxs-lookup"><span data-stu-id="22a46-156"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="22a46-157">In caso di esito positivo, il USHORT include il valore di <em>cbVarSegMac</em> usato durante la creazione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="22a46-157">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="22a46-158">Per una descrizione di <em>cbVarSegMac</em>, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="22a46-158">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="22a46-159">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a46-160">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="22a46-160">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="22a46-161"><em>pvResult</em> viene interpretato come <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span><span class="sxs-lookup"><span data-stu-id="22a46-161"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="22a46-162">In seguito all'esito positivo, la struttura <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> riceve informazioni sull'indice.</span><span class="sxs-lookup"><span data-stu-id="22a46-162">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="22a46-163">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-163">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-164">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="22a46-164">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="22a46-165"><em>pvResult</em> viene interpretato come UShort.</span><span class="sxs-lookup"><span data-stu-id="22a46-165"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="22a46-166">In caso di esito positivo, il USHORT include il valore di cbKeyMost usato durante la creazione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="22a46-166">On success, the USHORT holds the value of cbKeyMost used when the index was created.</span></span> <span data-ttu-id="22a46-167">Per una descrizione di cbKeyMost, vedere la struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="22a46-167">See the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure for a description of cbKeyMost.</span></span> <span data-ttu-id="22a46-168">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-168">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a46-169">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="22a46-169">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="22a46-170"><em>pvResult</em> viene interpretato come una struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="22a46-170"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="22a46-171">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="22a46-172"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="22a46-172"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-173">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="22a46-173">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="22a46-174"><em>pvResult</em> viene interpretato come una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="22a46-174"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="22a46-175">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="22a46-176"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="22a46-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="22a46-177">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22a46-177">Return Value</span></span>

<span data-ttu-id="22a46-178">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="22a46-178">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="22a46-179">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="22a46-179">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22a46-180">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="22a46-180">Return code</span></span></p></th>
<th><p><span data-ttu-id="22a46-181">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22a46-181">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22a46-182">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="22a46-182">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="22a46-183">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="22a46-183">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-184">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="22a46-184">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="22a46-185">Impossibile trovare l'indice specificato nella tabella specificata.</span><span class="sxs-lookup"><span data-stu-id="22a46-185">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a46-186">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="22a46-186">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="22a46-187">Il buffer passato come <em>pvResult</em> è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="22a46-187">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="22a46-188">Il contenuto del buffer non è definito.</span><span class="sxs-lookup"><span data-stu-id="22a46-188">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="22a46-189">Commenti</span><span class="sxs-lookup"><span data-stu-id="22a46-189">Remarks</span></span>

<span data-ttu-id="22a46-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) e **JetGetTableIndexInfo** recuperano informazioni identiche su un indice.</span><span class="sxs-lookup"><span data-stu-id="22a46-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) and **JetGetTableIndexInfo** retrieve identical information about an index.</span></span> <span data-ttu-id="22a46-191">La differenza consiste nel modo in cui viene specificata la tabella.</span><span class="sxs-lookup"><span data-stu-id="22a46-191">The difference is in how the table is specified.</span></span> <span data-ttu-id="22a46-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) prevede un database (*dbid*) e il nome di una tabella (*szTableName*), mentre **JetGetTableIndexInfo** prevede un identificatore di tabella (*TableID*).</span><span class="sxs-lookup"><span data-stu-id="22a46-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) expects a database (*dbid*) and name of a table (*szTableName*), while **JetGetTableIndexInfo** expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="22a46-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22a46-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22a46-194"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="22a46-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="22a46-195">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="22a46-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="22a46-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="22a46-197">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="22a46-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a46-198"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="22a46-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="22a46-199">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="22a46-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-200"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="22a46-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="22a46-201">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="22a46-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a46-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="22a46-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="22a46-203">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="22a46-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a46-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="22a46-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="22a46-205">Implementato come <strong>JetGetTableIndexInfoW</strong> (Unicode) e <strong>JetGetTableIndexInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="22a46-205">Implemented as <strong>JetGetTableIndexInfoW</strong> (Unicode) and <strong>JetGetTableIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="22a46-206">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="22a46-206">See Also</span></span>

[<span data-ttu-id="22a46-207">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="22a46-207">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="22a46-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="22a46-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="22a46-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="22a46-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="22a46-210">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="22a46-210">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="22a46-211">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="22a46-211">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="22a46-212">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="22a46-212">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="22a46-213">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="22a46-213">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="22a46-214">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="22a46-214">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)
