---
description: 'Altre informazioni su: JET_CALLBACK funzione di callback'
title: Funzione di callback JET_CALLBACK
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308517"
---
# <a name="jet_callback-callback-function"></a><span data-ttu-id="dc5b4-103">Funzione di callback JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="dc5b4-103">JET_CALLBACK Callback Function</span></span>


<span data-ttu-id="dc5b4-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dc5b4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_callback-callback-function"></a><span data-ttu-id="dc5b4-105">Funzione di callback JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="dc5b4-105">JET_CALLBACK Callback Function</span></span>

<span data-ttu-id="dc5b4-106">La funzione **JET_CALLBACK** è una funzione di callback multifunzione utilizzata dal motore di database per informare l'applicazione di un evento che interessa la deframmentazione in linea e le notifiche dello stato del cursore.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-106">The **JET_CALLBACK** function is a multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="dc5b4-107">Vedere [JET_CBTYP](./jet-cbtyp.md) per impostazioni specifiche da usare per i parametri di questa funzione, in quanto queste impostazioni variano in base all'opzione di **JET_CBTYP** selezionata per l'uso nel parametro *CBTYP* .</span><span class="sxs-lookup"><span data-stu-id="dc5b4-107">See [JET_CBTYP](./jet-cbtyp.md) for specific settings to use for the parameters of this function, as these settings will differ depending upon the **JET_CBTYP** option that is selected for use in the *cbtyp* parameter.</span></span>

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a><span data-ttu-id="dc5b4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc5b4-108">Parameters</span></span>

<span data-ttu-id="dc5b4-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="dc5b4-109">*sesid*</span></span>

<span data-ttu-id="dc5b4-110">Sessione per cui viene eseguito il callback.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-110">The session for which the callback is being made.</span></span>

<span data-ttu-id="dc5b4-111">*dbid*</span><span class="sxs-lookup"><span data-stu-id="dc5b4-111">*dbid*</span></span>

<span data-ttu-id="dc5b4-112">Database per il quale viene eseguito il callback.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-112">The database for which the callback is being made.</span></span>

<span data-ttu-id="dc5b4-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="dc5b4-113">*tableid*</span></span>

<span data-ttu-id="dc5b4-114">Cursore per il quale viene eseguito il callback.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-114">The cursor for which the callback is being made.</span></span>

<span data-ttu-id="dc5b4-115">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="dc5b4-115">*cbtyp*</span></span>

<span data-ttu-id="dc5b4-116">Punto nell'operazione in cui viene eseguito il callback.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-116">The point in the operation at which the callback is being made.</span></span> <span data-ttu-id="dc5b4-117">Vedere [JET_CBTYP](./jet-cbtyp.md) per un elenco di valori e il significato dei parametri seguenti in ogni caso.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-117">See [JET_CBTYP](./jet-cbtyp.md) for a list of values and the meaning of the following parameters in each case.</span></span>

<span data-ttu-id="dc5b4-118">*pvArg1*</span><span class="sxs-lookup"><span data-stu-id="dc5b4-118">*pvArg1*</span></span>

<span data-ttu-id="dc5b4-119">Parametro utilizzato per comunicare con l'applicazione utilizzando il callback.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-119">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="dc5b4-120">Per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database, vedere [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5b4-120">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="dc5b4-121">*pvArg2*</span><span class="sxs-lookup"><span data-stu-id="dc5b4-121">*pvArg2*</span></span>

<span data-ttu-id="dc5b4-122">Parametro utilizzato per comunicare con l'applicazione utilizzando il callback.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-122">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="dc5b4-123">Per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database, vedere [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5b4-123">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="dc5b4-124">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="dc5b4-124">*pvContext*</span></span>

<span data-ttu-id="dc5b4-125">Parametro utilizzato per comunicare con l'applicazione utilizzando il callback.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-125">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="dc5b4-126">Per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database, vedere [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5b4-126">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="dc5b4-127">*ulUnused*</span><span class="sxs-lookup"><span data-stu-id="dc5b4-127">*ulUnused*</span></span>

<span data-ttu-id="dc5b4-128">Parametro utilizzato per comunicare con l'applicazione utilizzando il callback.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-128">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="dc5b4-129">Per informazioni sull'uso di questo parametro per ogni callback supportato dal motore di database, vedere [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5b4-129">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

#### <a name="return-value"></a><span data-ttu-id="dc5b4-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc5b4-130">Return Value</span></span>

<span data-ttu-id="dc5b4-131">La funzione restituisce uno dei [codici di errore del motore di archiviazione estendibile](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dc5b4-131">The function returns one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="dc5b4-132">Per informazioni su come restituire questi codici come HRESULT, vedere [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="dc5b4-132">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="dc5b4-133">In seguito all'esito positivo, l'operazione che ha emesso il callback può procedere normalmente.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-133">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="dc5b4-134">In alcuni casi, il callback può restituire un avviso che influenza l'operazione.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-134">In some cases, the callback may return a warning that influences that operation.</span></span> <span data-ttu-id="dc5b4-135">Per informazioni sull'uso di questi avvisi da parte dell'operazione, vedere [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5b4-135">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of these warnings by the operation.</span></span>

<span data-ttu-id="dc5b4-136">In caso di errore, l'operazione che ha emesso il callback può procedere normalmente o potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-136">On failure, the operation that issued the callback may proceed normally or may fail.</span></span> <span data-ttu-id="dc5b4-137">Per informazioni sull'uso del codice di errore da parte dell'operazione, vedere [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5b4-137">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of the error code by the operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="dc5b4-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc5b4-138">Remarks</span></span>

<span data-ttu-id="dc5b4-139">Se il callback passa un cursore all'applicazione, è importante tenere presente che questo cursore è intenzionalmente limitato a un set di funzionalità più piccolo per evitare la ricorsione e altre Brute.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-139">If the callback passes a cursor to the application then it is important to know that this cursor is intentionally limited to a smaller set of functionality to avoid recursion and other ugliness.</span></span> <span data-ttu-id="dc5b4-140">Sono consentite le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc5b4-140">The following operations are allowed:</span></span>

  - [<span data-ttu-id="dc5b4-141">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="dc5b4-141">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="dc5b4-142">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="dc5b4-142">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="dc5b4-143">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="dc5b4-143">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="dc5b4-144">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="dc5b4-144">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)

  - [<span data-ttu-id="dc5b4-145">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="dc5b4-145">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="dc5b4-146">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="dc5b4-146">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="dc5b4-147">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="dc5b4-147">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)

  - [<span data-ttu-id="dc5b4-148">JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="dc5b4-148">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)

  - [<span data-ttu-id="dc5b4-149">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="dc5b4-149">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)

  - [<span data-ttu-id="dc5b4-150">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="dc5b4-150">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)

  - [<span data-ttu-id="dc5b4-151">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="dc5b4-151">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="dc5b4-152">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="dc5b4-152">JetRegisterCallback</span></span>](./jetregistercallback-function.md)

  - [<span data-ttu-id="dc5b4-153">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="dc5b4-153">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="dc5b4-154">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="dc5b4-154">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="dc5b4-155">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="dc5b4-155">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="dc5b4-156">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="dc5b4-156">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="dc5b4-157">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="dc5b4-157">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="dc5b4-158">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="dc5b4-158">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="dc5b4-159">JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="dc5b4-159">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)

<span data-ttu-id="dc5b4-160">Quando si progetta il callback, tenere presente che anche con queste restrizioni, è comunque possibile che il callback abbia esito negativo.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-160">When you design your callback, take into account that even with these restrictions, it is still possible for the callback to fail.</span></span>

#### <a name="requirements"></a><span data-ttu-id="dc5b4-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc5b4-161">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc5b4-162"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="dc5b4-162"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dc5b4-163">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-163">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc5b4-164"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dc5b4-164"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dc5b4-165">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-165">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc5b4-166"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="dc5b4-166"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dc5b4-167">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-167">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="dc5b4-168">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dc5b4-168">See Also</span></span>

[<span data-ttu-id="dc5b4-169">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="dc5b4-169">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="dc5b4-170">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="dc5b4-170">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="dc5b4-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="dc5b4-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="dc5b4-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="dc5b4-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="dc5b4-173">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="dc5b4-173">JET_CBTYP</span></span>](./jet-cbtyp.md)
