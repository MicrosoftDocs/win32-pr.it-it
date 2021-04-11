---
description: 'Altre informazioni su: funzione JetGetErrorInfoW'
title: JetGetErrorInfoW (funzione)
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104132435"
---
# <a name="jetgeterrorinfow-function"></a><span data-ttu-id="2e788-103">JetGetErrorInfoW (funzione)</span><span class="sxs-lookup"><span data-stu-id="2e788-103">JetGetErrorInfoW Function</span></span>


<span data-ttu-id="2e788-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2e788-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgeterrorinfow-function"></a><span data-ttu-id="2e788-105">JetGetErrorInfoW (funzione)</span><span class="sxs-lookup"><span data-stu-id="2e788-105">JetGetErrorInfoW Function</span></span>

<span data-ttu-id="2e788-106">Funzione **JetGetErrorInfoW** BAS_ del motore di database.</span><span class="sxs-lookup"><span data-stu-id="2e788-106">The **JetGetErrorInfoW** function BAS_ of the database engine.</span></span>

<span data-ttu-id="2e788-107">Nota: questa documentazione si basa su una versione preliminare del motore di archiviazione estendibile.</span><span class="sxs-lookup"><span data-stu-id="2e788-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="2e788-108">Queste informazioni sono soggette a modifiche.</span><span class="sxs-lookup"><span data-stu-id="2e788-108">This information is subject to change.</span></span>

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a><span data-ttu-id="2e788-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e788-109">Parameters</span></span>

<span data-ttu-id="2e788-110">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="2e788-110">*pvContext*</span></span>

<span data-ttu-id="2e788-111">Il contesto o il valore di errore per il quale sono necessarie le informazioni estese sull'errore.</span><span class="sxs-lookup"><span data-stu-id="2e788-111">The context or error value for which the extended error information is needed.</span></span> <span data-ttu-id="2e788-112">Il valore passato dipende dal valore del parametro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="2e788-112">The value passed in depends on the *InfoLevel* parameter value.</span></span>

<span data-ttu-id="2e788-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="2e788-113">*pvResult*</span></span>

<span data-ttu-id="2e788-114">Puntatore a un buffer che riceverà le informazioni.</span><span class="sxs-lookup"><span data-stu-id="2e788-114">A pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="2e788-115">Il tipo di buffer dipende dal valore del parametro *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="2e788-115">The type of the buffer depends on the *InfoLevel* parameter value.</span></span> <span data-ttu-id="2e788-116">Il chiamante deve essere configurato per allineare il buffer in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="2e788-116">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="2e788-117">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="2e788-117">*cbMax*</span></span>

<span data-ttu-id="2e788-118">Dimensione massima della struttura *pvResult* passata.</span><span class="sxs-lookup"><span data-stu-id="2e788-118">The maximum size of the *pvResult* structure that is passed in.</span></span>

<span data-ttu-id="2e788-119">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="2e788-119">*InfoLevel*</span></span>

<span data-ttu-id="2e788-120">Il tipo di informazioni che verranno recuperate per il contesto o le informazioni sull'errore viene specificato dal parametro *pvContext* .</span><span class="sxs-lookup"><span data-stu-id="2e788-120">The type of information that will be retrieved for the error info/context is specified by the *pvContext* parameter.</span></span> <span data-ttu-id="2e788-121">Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="2e788-121">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="2e788-122">Nella tabella seguente sono elencati i valori possibili per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2e788-122">The following table lists the possible values for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e788-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2e788-123">Value</span></span></p></th>
<th><p><span data-ttu-id="2e788-124">Significato</span><span class="sxs-lookup"><span data-stu-id="2e788-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e788-125">JET_ErrorInfoSpecificErr</span><span class="sxs-lookup"><span data-stu-id="2e788-125">JET_ErrorInfoSpecificErr</span></span></p></td>
<td><p><span data-ttu-id="2e788-126"><em>pvContext</em> viene interpretato come un codice di/Error <a href="gg269297(v=exchg.10).md">JET_ERR</a>, <em>pvResult</em> viene interpretato come <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>e i campi della struttura <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> vengono compilati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="2e788-126"><em>pvContext</em> is interpreted as a <a href="gg269297(v=exchg.10).md">JET_ERR</a>/error code, <em>pvResult</em> is interpreted as a <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>, and the fields of the <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> structure are filled in appropriately.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2e788-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="2e788-127">*grbit*</span></span>

<span data-ttu-id="2e788-128">Riservato.</span><span class="sxs-lookup"><span data-stu-id="2e788-128">Reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="2e788-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e788-129">Return Value</span></span>

<span data-ttu-id="2e788-130">Questa funzione restituisce il tipo di dati [JET_ERR](./extensible-storage-engine-error-codes.md) con uno dei codici restituiti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2e788-130">This function returns the [JET_ERR](./extensible-storage-engine-error-codes.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="2e788-131">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="2e788-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e788-132">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2e788-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="2e788-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e788-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e788-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2e788-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2e788-135">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="2e788-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e788-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2e788-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2e788-137">Uno dei parametri forniti contiene un valore imprevisto o contiene un valore che non ha senso se combinato con il valore di un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="2e788-137">One of the parameters provided contains an unexpected value or contains a value that does not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="2e788-138">Questa situazione può verificarsi per <strong>JetGetErrorInfo</strong> quando si verifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="2e788-138">This can happen for <strong>JetGetErrorInfo</strong> when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="2e788-139">Il valore del parametro <em>InfoLevel</em> specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="2e788-139">The specified <em>InfoLevel</em> parameter value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="2e788-140">Il valore <em>grbit</em> specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="2e788-140">The specified <em>grbit</em> value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="2e788-141">Il valore <em>cbMax</em> del buffer del parametro <em>pvResult</em> specificato è inferiore alla dimensione richiesta per l'output del parametro <em>InfoLevel</em> .</span><span class="sxs-lookup"><span data-stu-id="2e788-141">The specified <em>pvResult</em> parameter buffer’s <em>cbMax</em> value is less than the required size for output of this <em>InfoLevel</em> parameter.</span></span></p></li>
<li><p><span data-ttu-id="2e788-142">Per <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, il valore <a href="gg294092(v=exchg.10).md">JET_ERR</a> passato è sconosciuto al motore.</span><span class="sxs-lookup"><span data-stu-id="2e788-142">For <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, the <a href="gg294092(v=exchg.10).md">JET_ERR</a> value passed in is unknown to the engine.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e788-143">JET_errDisabledFunctionality</span><span class="sxs-lookup"><span data-stu-id="2e788-143">JET_errDisabledFunctionality</span></span></p></td>
<td><p><span data-ttu-id="2e788-144">Se questo SKU di Windows non supporta questa funzione, viene restituito questo errore.</span><span class="sxs-lookup"><span data-stu-id="2e788-144">If this SKU of windows doesn’t support this function, this error will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2e788-145">In caso di esito positivo, il buffer di output appropriato per il valore o il contesto di errore richiesto verrà impostato sulle informazioni di errore estese richieste.</span><span class="sxs-lookup"><span data-stu-id="2e788-145">On success, the output buffer that is appropriate for the requested error context/value will be set to the extended error info requested.</span></span>

<span data-ttu-id="2e788-146">In caso di errore, lo stato dei buffer di output sarà indefinito.</span><span class="sxs-lookup"><span data-stu-id="2e788-146">On failure, the state of the output buffers will be undefined.</span></span>

### <a name="remarks"></a><span data-ttu-id="2e788-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e788-147">Remarks</span></span>

<span data-ttu-id="2e788-148">La funzione [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) e [JET_ERRCAT](./jet-errcat.md) gruppo di costanti contengono la documentazione sulle informazioni estese sugli errori restituite per *InfoLevel* = JET_ErrorInfoSpecificErr.</span><span class="sxs-lookup"><span data-stu-id="2e788-148">The [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) function and [JET_ERRCAT](./jet-errcat.md) group of constants contain documentation about the extended error information that is returned for *InfoLevel* = JET_ErrorInfoSpecificErr.</span></span>

### <a name="requirements"></a><span data-ttu-id="2e788-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e788-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e788-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2e788-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2e788-151">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2e788-151">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e788-152"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2e788-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2e788-153">Richiede Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="2e788-153">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e788-154"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="2e788-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2e788-155">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="2e788-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e788-156"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="2e788-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2e788-157">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2e788-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e788-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2e788-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2e788-159">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2e788-159">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e788-160"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2e788-160"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2e788-161">Nota: viene implementato solo <strong>JetGetErrorInfoW</strong> (Unicode).</span><span class="sxs-lookup"><span data-stu-id="2e788-161">Note: Only the <strong>JetGetErrorInfoW</strong> (Unicode) is implemented.</span></span> <span data-ttu-id="2e788-162">Questa API non ha una versione (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2e788-162">This API does not have an A (ANSI) version.</span></span></p></td>
</tr>
</tbody>
</table>
