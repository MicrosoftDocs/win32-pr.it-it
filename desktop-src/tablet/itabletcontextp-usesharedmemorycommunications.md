---
description: Consente di accedere alla memoria condivisa tra i thread del tablet.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'Metodo ITabletContextP:: UseSharedMemoryCommunications'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319167"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a><span data-ttu-id="90999-103">Metodo ITabletContextP:: UseSharedMemoryCommunications</span><span class="sxs-lookup"><span data-stu-id="90999-103">ITabletContextP::UseSharedMemoryCommunications method</span></span>

<span data-ttu-id="90999-104">Consente di accedere alla memoria condivisa tra i thread del tablet.</span><span class="sxs-lookup"><span data-stu-id="90999-104">Provides access to memory shared between tablet threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="90999-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90999-105">Syntax</span></span>


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a><span data-ttu-id="90999-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="90999-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90999-107">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90999-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90999-108">ID del processo.</span><span class="sxs-lookup"><span data-stu-id="90999-108">Process id.</span></span>

</dd> <dt>

<span data-ttu-id="90999-109">*phEventMoreData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="90999-109">*phEventMoreData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90999-110">Handle di evento che segnala quando i nuovi dati sono disponibili per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="90999-110">Event handle that signals when new data is available to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="90999-111">*phEventClientReady* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="90999-111">*phEventClientReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90999-112">Handle di evento restituito utilizzato per segnalare che il client è pronto per la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="90999-112">Returned event handle used to signal that the client is ready to receive data.</span></span> <span data-ttu-id="90999-113">Segnalato dopo l'elaborazione di nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="90999-113">Signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="90999-114">*phMutexAccess* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="90999-114">*phMutexAccess* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90999-115">Mutex che concede l'accesso alla memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="90999-115">The mutex granting access to shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="90999-116">*phFileMapping* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="90999-116">*phFileMapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90999-117">Puntatore al blocco di memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="90999-117">Pointer to the shared memory block.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90999-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90999-118">Return value</span></span>

<span data-ttu-id="90999-119">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="90999-119">This method can return one of these values.</span></span>



| <span data-ttu-id="90999-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="90999-120">Return code</span></span>                                                                            | <span data-ttu-id="90999-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90999-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="90999-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="90999-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="90999-123">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="90999-123">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="90999-124"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="90999-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="90999-125">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="90999-125">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90999-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="90999-126">Remarks</span></span>

<span data-ttu-id="90999-127">Il metodo **UseSharedMemoryCommunications** viene utilizzato come parte del protocollo di memoria condivisa di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="90999-127">The **UseSharedMemoryCommunications** method is used as part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="90999-128">Poiché il servizio wisptis ha un livello di integrità elevato, può archiviare e accedere ai dati archiviati nella memoria condivisa senza dover elevare i propri privilegi.</span><span class="sxs-lookup"><span data-stu-id="90999-128">Since the Wisptis service has a high integrity level (IL), it can store and access data stored in shared memory without needing to elevate its privileges.</span></span>

<span data-ttu-id="90999-129">Viene eseguito il cast della struttura dell' [**\_ intestazione SHAREDMEMORY**](sharedmemory-header.md) dai dati a cui fa riferimento il mapping del file e i dati dei pacchetti non elaborati seguono l' **\_ intestazione SHAREDMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="90999-129">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping and the raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="90999-130">I dati dei pacchetti non elaborati possono essere letti dalla memoria condivisa quando viene generato l'evento a cui fa riferimento *pdwEventClientReady* .</span><span class="sxs-lookup"><span data-stu-id="90999-130">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReady* is raised.</span></span>

<span data-ttu-id="90999-131">Nell'elenco seguente viene descritta la sequenza di eventi per l'accesso e l'utilizzo della memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="90999-131">The following list describes the sequence of events for accessing and using shared memory.</span></span>

-   <span data-ttu-id="90999-132">Il client imposta l'evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="90999-132">The client sets the clientReady event.</span></span>
-   <span data-ttu-id="90999-133">Il client attende l'evento moreData.</span><span class="sxs-lookup"><span data-stu-id="90999-133">The client waits for the moreData event.</span></span>
-   <span data-ttu-id="90999-134">Il client acquisisce il mutex.</span><span class="sxs-lookup"><span data-stu-id="90999-134">The client acquires the mutex.</span></span>
-   <span data-ttu-id="90999-135">Il client legge i dati dei pacchetti dalla sezione della memoria condivisa dopo l'intestazione e i numeri di serie dopo i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="90999-135">The client reads packet data from the section of shared memory after the header and serial numbers after the packets.</span></span>
-   <span data-ttu-id="90999-136">Il client gestisce i dati in base al valore di **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="90999-136">The client handles data depending on the value of **dwEvent**.</span></span>
-   <span data-ttu-id="90999-137">Il client scrive-1 (0xFFFFFFFF) in **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="90999-137">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
-   <span data-ttu-id="90999-138">Il client rilascia il mutex.</span><span class="sxs-lookup"><span data-stu-id="90999-138">The client releases the mutex.</span></span>
-   <span data-ttu-id="90999-139">Il client imposta l'evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="90999-139">The client sets the clientReady event.</span></span>

## <a name="requirements"></a><span data-ttu-id="90999-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90999-140">Requirements</span></span>



| <span data-ttu-id="90999-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="90999-141">Requirement</span></span> | <span data-ttu-id="90999-142">Valore</span><span class="sxs-lookup"><span data-stu-id="90999-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90999-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90999-143">Minimum supported client</span></span><br/> | <span data-ttu-id="90999-144">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="90999-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="90999-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90999-145">Minimum supported server</span></span><br/> | <span data-ttu-id="90999-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="90999-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="90999-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="90999-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="90999-148"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90999-148"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90999-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90999-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90999-150">**Interfaccia ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="90999-150">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="90999-151">**UseNamedSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="90999-151">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




