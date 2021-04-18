---
description: 'Altre informazioni su: funzione JetGetIndexInfo'
title: Funzione JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315069"
---
# <a name="jetgetindexinfo-function"></a><span data-ttu-id="f9e5e-103">Funzione JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="f9e5e-103">JetGetIndexInfo Function</span></span>


<span data-ttu-id="f9e5e-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f9e5e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetindexinfo-function"></a><span data-ttu-id="f9e5e-105">Funzione JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="f9e5e-105">JetGetIndexInfo Function</span></span>

<span data-ttu-id="f9e5e-106">La funzione **JetGetIndexInfo** recupera le informazioni su un indice.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-106">The **JetGetIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="f9e5e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9e5e-107">Parameters</span></span>

<span data-ttu-id="f9e5e-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f9e5e-108">*sesid*</span></span>

<span data-ttu-id="f9e5e-109">Contesto della sessione di database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="f9e5e-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="f9e5e-110">*dbid*</span></span>

<span data-ttu-id="f9e5e-111">Identificatore del database da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="f9e5e-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="f9e5e-112">*szTableName*</span></span>

<span data-ttu-id="f9e5e-113">Nome della tabella contenente l'indice con le informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-113">The name of the table containing the index with the information to retrieve.</span></span>

<span data-ttu-id="f9e5e-114">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="f9e5e-114">*szIndexName*</span></span>

<span data-ttu-id="f9e5e-115">Nome dell'indice con le informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-115">The name of the index with the information to retrieve.</span></span>

<span data-ttu-id="f9e5e-116">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="f9e5e-116">*pvResult*</span></span>

<span data-ttu-id="f9e5e-117">Puntatore a un buffer che riceverà le informazioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-117">Pointer to a buffer that will receive the desired information.</span></span> <span data-ttu-id="f9e5e-118">Il buffer deve essere allineato per contenere il tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-118">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="f9e5e-119">Il tipo del buffer dipende dal parametro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="f9e5e-119">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="f9e5e-120">*cbResult*</span><span class="sxs-lookup"><span data-stu-id="f9e5e-120">*cbResult*</span></span>

<span data-ttu-id="f9e5e-121">Dimensione, in byte, del buffer passato come *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-121">The size, in bytes, of the buffer passed as *pvResult*.</span></span>

<span data-ttu-id="f9e5e-122">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="f9e5e-122">*InfoLevel*</span></span>

<span data-ttu-id="f9e5e-123">Informazioni che verranno archiviate in *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-123">The information that will be stored in *pvResult*.</span></span> <span data-ttu-id="f9e5e-124">Per questo parametro è possibile usare le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-124">The following options can be used for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9e5e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f9e5e-125">Value</span></span></p></th>
<th><p><span data-ttu-id="f9e5e-126">Significato</span><span class="sxs-lookup"><span data-stu-id="f9e5e-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-127">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="f9e5e-127">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-128"><em>pvResult</em> viene interpretato come una struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="f9e5e-128"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="f9e5e-129">In seguito all'esito positivo, la struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> riceve informazioni sull'indice.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-129">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="f9e5e-130">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-130">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-131">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="f9e5e-131">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-132"><em>pvResult</em> viene interpretato come ulong.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-132"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="f9e5e-133">In seguito all'esito positivo, ULONG include il conteggio degli indici nella tabella specificata.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-133">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="f9e5e-134"><em>szIndexName</em> viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-134"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="f9e5e-135">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-135">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-136">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="f9e5e-136">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-137"><em>pvResult</em> viene interpretato come <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-137"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="f9e5e-138">In seguito all'esito positivo, la struttura <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> riceve informazioni sull'indice.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-138">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="f9e5e-139">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-139">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-140">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="f9e5e-140">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-141">JET_IdxInfoLangid è deprecato.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-141">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="f9e5e-142">Usare invece JET_IdxInfoLCID e la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</span><span class="sxs-lookup"><span data-stu-id="f9e5e-142">Use JET_IdxInfoLCID and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-143">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="f9e5e-143">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-144"><em>pvResult</em> viene interpretato come un identificatore LCID.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-144"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="f9e5e-145">In seguito all'esito positivo, l'LCID include l'identificatore delle impostazioni locali dell'indice.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-145">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="f9e5e-146">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-146">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="f9e5e-147"><strong>Windows XP:  </strong> JET_IdxInfoLCID è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-147"><strong>Windows XP:  </strong>JET_IdxInfoLCID is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-148">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="f9e5e-148">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-149"><em>pvResult</em> viene interpretato come una struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="f9e5e-149"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="f9e5e-150">In seguito all'esito positivo, la struttura <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> riceve informazioni sull'indice.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-150">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="f9e5e-151">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-151">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-152">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="f9e5e-152">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-153">JET_IdxInfoOLC è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-153">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-154">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="f9e5e-154">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-155">JET_IdxInfoResetOLC è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-155">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-156">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="f9e5e-156">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-157"><em>pvResult</em> viene interpretato come ulong.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-157"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="f9e5e-158">In seguito all'esito positivo, ULONG determinerà l'utilizzo dello spazio dell'indice.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-158">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="f9e5e-159">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-160">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="f9e5e-160">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-161">JET_IdxInfoSysTabCursor è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-161">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-162">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="f9e5e-162">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-163"><em>pvResult</em> viene interpretato come UShort.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-163"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="f9e5e-164">In caso di esito positivo, il USHORT include il valore di <em>cbVarSegMac</em> usato durante la creazione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-164">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="f9e5e-165">Per una descrizione di <em>cbVarSegMac</em>, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f9e5e-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="f9e5e-166">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-166">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-167">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="f9e5e-167">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-168"><em>pvResult</em> viene interpretato come UShort.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-168"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="f9e5e-169">In caso di esito positivo, il USHORT include il valore di <em>cbKeyMost</em> usato durante la creazione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-169">On success, the USHORT holds the value of <em>cbKeyMost</em> used when the index was created.</span></span> <span data-ttu-id="f9e5e-170">Per una descrizione di <em>cbKeyMost</em>, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f9e5e-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbKeyMost</em>.</span></span> <span data-ttu-id="f9e5e-171">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="f9e5e-172"><strong>Windows Vista:  </strong> JET_IdxInfoKeyMost è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-172"><strong>Windows Vista:  </strong>JET_IdxInfoKeyMost is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-173">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="f9e5e-173">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-174"><em>pvResult</em> viene interpretato come una struttura <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f9e5e-174"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="f9e5e-175">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="f9e5e-176"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-177">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="f9e5e-177">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-178"><em>pvResult</em> viene interpretato come una struttura <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="f9e5e-178"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="f9e5e-179">In caso di errore, il contenuto di <em>pvBuffer</em> non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-179">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="f9e5e-180"><strong>Windows 7:  </strong> JET_IdxInfoCreateIndex2 è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-180"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f9e5e-181">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9e5e-181">Return Value</span></span>

<span data-ttu-id="f9e5e-182">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f9e5e-183">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="f9e5e-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9e5e-184">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f9e5e-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="f9e5e-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9e5e-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f9e5e-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-187">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-188">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="f9e5e-188">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-189">Impossibile trovare l'indice specificato nella tabella specificata.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-189">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-190">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="f9e5e-190">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="f9e5e-191">Il buffer passato come <em>pvResult</em> è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-191">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="f9e5e-192">Il contenuto del buffer non è definito.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-192">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="f9e5e-193">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9e5e-193">Remarks</span></span>

<span data-ttu-id="f9e5e-194">**JetGetIndexInfo** e [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) recuperano informazioni identiche su un indice.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-194">**JetGetIndexInfo** and [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) retrieve identical information about an index.</span></span> <span data-ttu-id="f9e5e-195">La differenza consiste nel modo in cui viene specificata la tabella.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-195">The difference is in how the table is specified.</span></span> <span data-ttu-id="f9e5e-196">**JetGetIndexInfo** prevede un database (*dbid*) e il nome di una tabella (*szTableName*), mentre [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) prevede un identificatore di tabella (*TableID*).</span><span class="sxs-lookup"><span data-stu-id="f9e5e-196">**JetGetIndexInfo** expects a database (*dbid*) and name of a table (*szTableName*), while [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="f9e5e-197">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9e5e-197">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-198"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f9e5e-198"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f9e5e-199">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-199">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-200"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f9e5e-200"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f9e5e-201">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-201">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-202"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="f9e5e-202"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f9e5e-203">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-203">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-204"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="f9e5e-204"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f9e5e-205">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-205">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9e5e-206"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f9e5e-206"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f9e5e-207">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f9e5e-207">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e5e-208"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f9e5e-208"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f9e5e-209">Implementato come <strong>JetGetIndexInfoW</strong> (Unicode) e <strong>JetGetIndexInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f9e5e-209">Implemented as <strong>JetGetIndexInfoW</strong> (Unicode) and <strong>JetGetIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f9e5e-210">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f9e5e-210">See Also</span></span>

[<span data-ttu-id="f9e5e-211">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="f9e5e-211">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="f9e5e-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f9e5e-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f9e5e-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f9e5e-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f9e5e-214">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="f9e5e-214">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="f9e5e-215">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="f9e5e-215">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="f9e5e-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f9e5e-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f9e5e-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f9e5e-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f9e5e-218">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="f9e5e-218">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
