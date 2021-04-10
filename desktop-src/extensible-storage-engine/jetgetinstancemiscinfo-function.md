---
description: 'Altre informazioni su: funzione JetGetInstanceMiscInfo'
title: JetGetInstanceMiscInfo (funzione)
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057924"
---
# <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="25d36-103">JetGetInstanceMiscInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="25d36-103">JetGetInstanceMiscInfo Function</span></span>


<span data-ttu-id="25d36-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="25d36-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="25d36-105">JetGetInstanceMiscInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="25d36-105">JetGetInstanceMiscInfo Function</span></span>

<span data-ttu-id="25d36-106">La funzione **JetGetInstanceMiscInfo** recupera informazioni sull'istanza di, mentre l'istanza è online.</span><span class="sxs-lookup"><span data-stu-id="25d36-106">The **JetGetInstanceMiscInfo** function retrieves information about the instance, while the instance is online.</span></span>

<span data-ttu-id="25d36-107">**Windows Vista: JetGetInstanceMiscInfo** è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="25d36-107">**Windows Vista:  JetGetInstanceMiscInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="25d36-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="25d36-108">Parameters</span></span>

<span data-ttu-id="25d36-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="25d36-109">*instance*</span></span>

<span data-ttu-id="25d36-110">Identifica l'istanza del database che verrà usata per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="25d36-110">Identifies the database instance that will be used for the API call.</span></span>

<span data-ttu-id="25d36-111">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="25d36-111">*pvResult*</span></span>

<span data-ttu-id="25d36-112">Puntatore a un buffer che riceverà le informazioni.</span><span class="sxs-lookup"><span data-stu-id="25d36-112">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="25d36-113">Il tipo di buffer dipende da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="25d36-113">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="25d36-114">Il chiamante è responsabile dell'allineamento appropriato del buffer.</span><span class="sxs-lookup"><span data-stu-id="25d36-114">The caller is responsible for aligning the buffer appropriately.</span></span>

<span data-ttu-id="25d36-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="25d36-115">*cbMax*</span></span>

<span data-ttu-id="25d36-116">Dimensione, in byte, del buffer passato in *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="25d36-116">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="25d36-117">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="25d36-117">*InfoLevel*</span></span>

<span data-ttu-id="25d36-118">Determina il tipo di informazioni che verranno recuperate per l'istanza di specificata dall' *istanza*.</span><span class="sxs-lookup"><span data-stu-id="25d36-118">Determines what type of information will be retrieved for the instance specified by *instance*.</span></span> <span data-ttu-id="25d36-119">Il formato dei dati archiviati in *pvResult* dipende da *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="25d36-119">The format of the data stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="25d36-120">Con questo parametro è possibile usare le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="25d36-120">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25d36-121">Valore</span><span class="sxs-lookup"><span data-stu-id="25d36-121">Value</span></span></p></th>
<th><p><span data-ttu-id="25d36-122">Significato</span><span class="sxs-lookup"><span data-stu-id="25d36-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25d36-123">JET_InstanceMiscInfoLogSignature</span><span class="sxs-lookup"><span data-stu-id="25d36-123">JET_InstanceMiscInfoLogSignature</span></span></p></td>
<td><p><span data-ttu-id="25d36-124"><em>pvResult</em> viene interpretato come una struttura <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> della sequenza del log delle transazioni associata a questa istanza.</span><span class="sxs-lookup"><span data-stu-id="25d36-124"><em>pvResult</em> is interpreted as a <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> structure of the transaction log sequence associated with this instance.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="25d36-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25d36-125">Return Value</span></span>

<span data-ttu-id="25d36-126">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="25d36-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="25d36-127">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="25d36-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25d36-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="25d36-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="25d36-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25d36-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25d36-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="25d36-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="25d36-131">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="25d36-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d36-132">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="25d36-132">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="25d36-133">Il buffer è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="25d36-133">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d36-134">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="25d36-134">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="25d36-135">È stato specificato un <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> non valido o un <em>InfoLevel</em> non valido.</span><span class="sxs-lookup"><span data-stu-id="25d36-135">Either an invalid <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> or an invalid <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="25d36-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25d36-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25d36-137"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="25d36-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="25d36-138">Richiede Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="25d36-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d36-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="25d36-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="25d36-140">Richiede Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="25d36-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d36-141"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="25d36-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="25d36-142">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="25d36-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25d36-143"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="25d36-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="25d36-144">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="25d36-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25d36-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="25d36-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="25d36-146">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="25d36-146">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="25d36-147">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="25d36-147">See Also</span></span>

[<span data-ttu-id="25d36-148">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="25d36-148">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="25d36-149">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="25d36-149">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="25d36-150">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="25d36-150">JET_SIGNATURE</span></span>](./jet-signature-structure.md)
