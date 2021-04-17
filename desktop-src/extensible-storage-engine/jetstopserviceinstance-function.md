---
description: 'Altre informazioni su: funzione JetStopServiceInstance'
title: JetStopServiceInstance (funzione)
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b2e3307f13a63d00cbbaf33f491750bbfcdb9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306211"
---
# <a name="jetstopserviceinstance-function"></a><span data-ttu-id="a5f16-103">JetStopServiceInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="a5f16-103">JetStopServiceInstance Function</span></span>


<span data-ttu-id="a5f16-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a5f16-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopserviceinstance-function"></a><span data-ttu-id="a5f16-105">JetStopServiceInstance (funzione)</span><span class="sxs-lookup"><span data-stu-id="a5f16-105">JetStopServiceInstance Function</span></span>

<span data-ttu-id="a5f16-106">La funzione **JetStopServiceInstance** prepara un'istanza per la chiusura.</span><span class="sxs-lookup"><span data-stu-id="a5f16-106">The **JetStopServiceInstance** function prepares an instance for termination.</span></span>

<span data-ttu-id="a5f16-107">**Windows XP:**  **JetStopServiceInstance** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5f16-107">**Windows XP:**  **JetStopServiceInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="a5f16-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5f16-108">Parameters</span></span>

<span data-ttu-id="a5f16-109">*istanza*</span><span class="sxs-lookup"><span data-stu-id="a5f16-109">*instance*</span></span>

<span data-ttu-id="a5f16-110">Istanza in esecuzione da usare per la chiamata API.</span><span class="sxs-lookup"><span data-stu-id="a5f16-110">The running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="a5f16-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5f16-111">Return Value</span></span>

<span data-ttu-id="a5f16-112">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="a5f16-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a5f16-113">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f16-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5f16-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a5f16-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="a5f16-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5f16-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5f16-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a5f16-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a5f16-117">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a5f16-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f16-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a5f16-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a5f16-119">Il valore del parametro di istanza specificato non è valido (non è un'istanza attualmente in esecuzione).</span><span class="sxs-lookup"><span data-stu-id="a5f16-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="a5f16-120"><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5f16-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5f16-121">Se questa funzione ha esito positivo, viene preparata per una terminazione futura.</span><span class="sxs-lookup"><span data-stu-id="a5f16-121">If this function succeeds, it prepares for a future termination.</span></span> <span data-ttu-id="a5f16-122">I passaggi necessari per preparare la chiusura includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5f16-122">The steps taken to prepare for a termination include the following:</span></span>

  - <span data-ttu-id="a5f16-123">Arrestare la deframmentazione in linea se è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a5f16-123">Stop online defragmentation if it is running.</span></span>

  - <span data-ttu-id="a5f16-124">Avviare una pulizia dell'archivio versioni.</span><span class="sxs-lookup"><span data-stu-id="a5f16-124">Start a version store clean-up.</span></span>

  - <span data-ttu-id="a5f16-125">Per ridurre la profondità del checkpoint, iniziare a scaricare le pagine dirty in Gestione buffer.</span><span class="sxs-lookup"><span data-stu-id="a5f16-125">Reduce the checkpoint depth by starting to flush dirty pages in the buffer manager.</span></span>

  - <span data-ttu-id="a5f16-126">Evitare chiamate future alla maggior parte delle funzioni per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="a5f16-126">Prevent future calls to most functions for that instance.</span></span>

<span data-ttu-id="a5f16-127">Se questa funzione ha esito negativo, non verrà eseguita alcuna procedura per preparare la terminazione di un'istanza, quindi non si verificherà alcuna modifica allo stato dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a5f16-127">If this function fails, none of the steps to prepare for an instance termination will be taken, so no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a5f16-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5f16-128">Remarks</span></span>

<span data-ttu-id="a5f16-129">Questa funzione ridurrà il lavoro che l'istanza dovrà eseguire quando viene terminata, ma non verrà terminata l'istanza.</span><span class="sxs-lookup"><span data-stu-id="a5f16-129">This function will reduce the work the instance will have to do when terminated but will not terminate the instance.</span></span> <span data-ttu-id="a5f16-130">Di conseguenza, questa funzione è solo un'ottimizzazione e non è obbligatoria per l'uso di.</span><span class="sxs-lookup"><span data-stu-id="a5f16-130">As a result, this function is just an optimization and is not mandatory to use.</span></span> <span data-ttu-id="a5f16-131">Si noti che la quantità di lavoro svolto in preparazione era minore in Windows 2000 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5f16-131">Note that the amount of work done in preparation was less in Windows 2000 and Windows XP.</span></span> <span data-ttu-id="a5f16-132">Quando la funzione ha esito positivo, la chiamata di funzioni che non sono più consentite restituirà JET_errClientRequestToStopJetService.</span><span class="sxs-lookup"><span data-stu-id="a5f16-132">Once the function succeeds, calling functions that are no longer allowed will return JET_errClientRequestToStopJetService.</span></span> <span data-ttu-id="a5f16-133">Le funzioni ancora consentite dopo questa chiamata sono: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="a5f16-133">Functions that are still allowed after this call are: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="a5f16-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5f16-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5f16-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a5f16-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f16-136">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5f16-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f16-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a5f16-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f16-138">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a5f16-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f16-139"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="a5f16-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f16-140">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="a5f16-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5f16-141"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="a5f16-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f16-142">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a5f16-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5f16-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a5f16-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a5f16-144">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a5f16-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a5f16-145">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a5f16-145">See Also</span></span>

[<span data-ttu-id="a5f16-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a5f16-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a5f16-147">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a5f16-147">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a5f16-148">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="a5f16-148">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="a5f16-149">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="a5f16-149">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="a5f16-150">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="a5f16-150">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="a5f16-151">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="a5f16-151">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="a5f16-152">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="a5f16-152">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="a5f16-153">JetRollback</span><span class="sxs-lookup"><span data-stu-id="a5f16-153">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="a5f16-154">JetTerm</span><span class="sxs-lookup"><span data-stu-id="a5f16-154">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="a5f16-155">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="a5f16-155">JetTerm2</span></span>](./jetterm2-function.md)
