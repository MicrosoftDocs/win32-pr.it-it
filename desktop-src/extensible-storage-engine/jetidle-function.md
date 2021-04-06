---
description: 'Altre informazioni su: funzione JetIdle'
title: JetIdle (funzione)
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883465"
---
# <a name="jetidle-function"></a><span data-ttu-id="2cc68-103">JetIdle (funzione)</span><span class="sxs-lookup"><span data-stu-id="2cc68-103">JetIdle Function</span></span>


<span data-ttu-id="2cc68-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2cc68-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetidle-function"></a><span data-ttu-id="2cc68-105">JetIdle (funzione)</span><span class="sxs-lookup"><span data-stu-id="2cc68-105">JetIdle Function</span></span>

<span data-ttu-id="2cc68-106">La funzione **JetIdle** è inattiva e deve essere usata solo a scopo di test.</span><span class="sxs-lookup"><span data-stu-id="2cc68-106">The **JetIdle** function is defunct, and should only be used for testing purposes.</span></span> <span data-ttu-id="2cc68-107">**JetIdle** può essere utilizzato per eseguire attività di pulizia inattive o controllare lo stato dell'archivio versioni in ESE.</span><span class="sxs-lookup"><span data-stu-id="2cc68-107">**JetIdle** can be used to perform idle cleanup tasks or check the version store status in ESE.</span></span>

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="2cc68-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cc68-108">Parameters</span></span>

<span data-ttu-id="2cc68-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2cc68-109">*sesid*</span></span>

<span data-ttu-id="2cc68-110">Sessione che verrà utilizzata per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="2cc68-110">The session that will be used for this call.</span></span>

<span data-ttu-id="2cc68-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="2cc68-111">*grbit*</span></span>

<span data-ttu-id="2cc68-112">Gruppo di bit che contiene le opzioni da utilizzare per la chiamata, che includono zero o più dei bit seguenti:</span><span class="sxs-lookup"><span data-stu-id="2cc68-112">A group of bits that contain the options to be used for this call, which include zero or more of the following bits:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2cc68-113">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc68-113">Value</span></span></p></th>
<th><p><span data-ttu-id="2cc68-114">Significato</span><span class="sxs-lookup"><span data-stu-id="2cc68-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cc68-115">JET_bitIdleCompact</span><span class="sxs-lookup"><span data-stu-id="2cc68-115">JET_bitIdleCompact</span></span></p></td>
<td><p><span data-ttu-id="2cc68-116">Attiva la pulizia dell'archivio delle versioni.</span><span class="sxs-lookup"><span data-stu-id="2cc68-116">Triggers cleanup of the version store.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cc68-117">JET_bitIdleFlushBuffers</span><span class="sxs-lookup"><span data-stu-id="2cc68-117">JET_bitIdleFlushBuffers</span></span></p></td>
<td><p><span data-ttu-id="2cc68-118">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="2cc68-118">Reserved for future use.</span></span> <span data-ttu-id="2cc68-119">Se questo flag è specificato, l'API restituirà JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="2cc68-119">If this flag is specified, the API will return JET_errInvalidgrbit.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cc68-120">JET_bitIdleStatus</span><span class="sxs-lookup"><span data-stu-id="2cc68-120">JET_bitIdleStatus</span></span></p></td>
<td><p><span data-ttu-id="2cc68-121">Restituisce JET_wrnIdleFull se l'archivio delle versioni supera la metà.</span><span class="sxs-lookup"><span data-stu-id="2cc68-121">Returns JET_wrnIdleFull if version store is more than half full.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2cc68-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2cc68-122">Return Value</span></span>

<span data-ttu-id="2cc68-123">Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="2cc68-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2cc68-124">Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="2cc68-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2cc68-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2cc68-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="2cc68-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cc68-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cc68-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2cc68-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2cc68-128">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="2cc68-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cc68-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2cc68-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2cc68-130">Un parametro <em>grbit</em> fornito all'API non è valido.</span><span class="sxs-lookup"><span data-stu-id="2cc68-130">A <em>grbit</em> parameter that was provided to the API was not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2cc68-131">Se questa funzione ha esito positivo, verrà attivata l'operazione appropriata oppure un codice di errore che indica il modo in cui l'archivio versione è pieno a seconda del *grbit* fornito.</span><span class="sxs-lookup"><span data-stu-id="2cc68-131">If this function succeeds, the appropriate operation will be triggered, or an error code indicating how full the version store is depending on the *grbit* provided.</span></span>

<span data-ttu-id="2cc68-132">Se questa funzione ha esito negativo, l'operazione richiesta non viene completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="2cc68-132">If this function fails, the requested operation will not have completed successfully.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2cc68-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cc68-133">Remarks</span></span>

<span data-ttu-id="2cc68-134">L'archivio versioni mantiene il meccanismo di isolamento dello snapshot di ESE.</span><span class="sxs-lookup"><span data-stu-id="2cc68-134">The version store maintains ESE's snapshot isolation mechanism.</span></span> <span data-ttu-id="2cc68-135">Se l'archivio delle versioni supera la metà, il programma potrebbe chiudere transazioni con esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="2cc68-135">If the version store is more than half full, the program might close long-running transactions.</span></span> <span data-ttu-id="2cc68-136">Se una transazione con esecuzione prolungata esaurisce l'archivio versioni, ESE smetterà di consentire operazioni di scrittura nel database.</span><span class="sxs-lookup"><span data-stu-id="2cc68-136">If a long-running transaction exhausts the version store, ESE will stop allowing write operations to the database.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2cc68-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cc68-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cc68-138"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2cc68-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2cc68-139">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2cc68-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cc68-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2cc68-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2cc68-141">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2cc68-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cc68-142"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="2cc68-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2cc68-143">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="2cc68-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cc68-144"><strong>Libreria</strong></span><span class="sxs-lookup"><span data-stu-id="2cc68-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2cc68-145">Usare ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2cc68-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cc68-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2cc68-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2cc68-147">Richiede ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2cc68-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2cc68-148">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2cc68-148">See Also</span></span>

[<span data-ttu-id="2cc68-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2cc68-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2cc68-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2cc68-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2cc68-151">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2cc68-151">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2cc68-152">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="2cc68-152">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
