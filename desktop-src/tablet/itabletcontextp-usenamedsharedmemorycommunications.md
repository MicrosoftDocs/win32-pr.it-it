---
description: Imposta la comunicazione della memoria condivisa per il contesto della tavoletta.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: 'Metodo ITabletContextP:: UseNamedSharedMemoryCommunications'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313917"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a><span data-ttu-id="a0ef8-103">Metodo ITabletContextP:: UseNamedSharedMemoryCommunications</span><span class="sxs-lookup"><span data-stu-id="a0ef8-103">ITabletContextP::UseNamedSharedMemoryCommunications method</span></span>

<span data-ttu-id="a0ef8-104">Imposta la comunicazione della memoria condivisa per il contesto della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-104">Sets up shared memory communication for the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ef8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0ef8-105">Syntax</span></span>


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a><span data-ttu-id="a0ef8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0ef8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0ef8-107">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0ef8-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ef8-108">ID processo del client che accede alla memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-108">The process ID of the client that accesses shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="a0ef8-109">*pszCallerSid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0ef8-109">*pszCallerSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ef8-110">Identificatore di sicurezza del chiamante della funzione.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-110">The security identifier of the function caller.</span></span>

</dd> <dt>

<span data-ttu-id="a0ef8-111">*pszCallerIntegritySid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0ef8-111">*pszCallerIntegritySid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ef8-112">Identificatore di sicurezza in grado di verificare l'integrità della funzione chiamante.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-112">The security identifier that can verify the integrity of the calling function.</span></span>

</dd> <dt>

<span data-ttu-id="a0ef8-113">*pdwEventMoreDataId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a0ef8-113">*pdwEventMoreDataId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ef8-114">Integer utilizzato per costruire il nome di un evento.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-114">An integer used to construct the name of an event.</span></span> <span data-ttu-id="a0ef8-115">L'evento indica se sono presenti più dati.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-115">The event indicates whether there is more data.</span></span>

</dd> <dt>

<span data-ttu-id="a0ef8-116">*pdwEventClientReadyId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a0ef8-116">*pdwEventClientReadyId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ef8-117">Integer utilizzato per costruire il nome di un evento.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-117">An integer used to construct the name of an event.</span></span> <span data-ttu-id="a0ef8-118">L'evento segnala che il client è pronto per la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-118">The event signals that the client is ready to receive data.</span></span> <span data-ttu-id="a0ef8-119">L'evento viene segnalato dopo l'elaborazione di nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-119">The event is signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="a0ef8-120">*pdwMutexAccessId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a0ef8-120">*pdwMutexAccessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ef8-121">Puntatore all'identificatore di accesso della memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-121">A pointer to the access identifier of the shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="a0ef8-122">*pdwFileMappingId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a0ef8-122">*pdwFileMappingId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ef8-123">Intero che identifica la memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-123">An integer that identifies the shared memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0ef8-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0ef8-124">Return value</span></span>

<span data-ttu-id="a0ef8-125">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a0ef8-126">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a0ef8-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0ef8-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0ef8-127">Remarks</span></span>

<span data-ttu-id="a0ef8-128">Il metodo **UseNamedSharedMemoryCommunications** fa parte del protocollo di memoria condivisa di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-128">The **UseNamedSharedMemoryCommunications** method is part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="a0ef8-129">Un client senza privilegi elevati passa a un ID di sicurezza (SID) e a un identificatore di sicurezza del livello di integrità (IL-SID), in modo che il servizio Tablet possa usare gli elenchi di controllo di accesso (ACL) per accedere agli oggetti Shared Memory.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-129">A client without elevated privileges passes in a security identifier (SID) and an integrity level security identifier (IL-SID) so that the Tablet service can use access control lists (ACL) to access the shared memory objects.</span></span> <span data-ttu-id="a0ef8-130">Se il client dispone di privilegi elevati, deve usare UseSharedMemoryCommunications, ovvero l'API che viene chiamata se il servizio dispone già di un privilegio con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-130">If the client has elevated privileges, it should use UseSharedMemoryCommunications, which is the API that is called if the service already has an elevated privilege.</span></span>

<span data-ttu-id="a0ef8-131">La struttura dell' [**\_ intestazione SHAREDMEMORY**](sharedmemory-header.md) archivia l'intestazione Shared Memory.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-131">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure stores the shared memory header.</span></span>

<span data-ttu-id="a0ef8-132">Viene eseguito il cast della struttura dell' [**\_ intestazione SHAREDMEMORY**](sharedmemory-header.md) dai dati a cui fa riferimento il mapping del file.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-132">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping.</span></span> <span data-ttu-id="a0ef8-133">I dati dei pacchetti non elaborati seguono l' **\_ intestazione SHAREDMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-133">The raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="a0ef8-134">I dati dei pacchetti non elaborati possono essere letti dalla memoria condivisa quando viene generato l'evento a cui fa riferimento *pdwEventClientReadyId* .</span><span class="sxs-lookup"><span data-stu-id="a0ef8-134">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReadyId* is raised.</span></span>

<span data-ttu-id="a0ef8-135">Nell'elenco seguente viene descritta la sequenza di eventi per l'accesso e l'utilizzo della memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-135">The following list describes the sequence of events for accessing and using shared memory.</span></span>

1.  <span data-ttu-id="a0ef8-136">Il client genera l'evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-136">The client raises the clientReady event.</span></span>
2.  <span data-ttu-id="a0ef8-137">Il client attende l'evento moreData.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-137">The client waits for the moreData event.</span></span>
3.  <span data-ttu-id="a0ef8-138">Il client acquisisce il mutex.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-138">The client acquires the mutex.</span></span>
4.  <span data-ttu-id="a0ef8-139">Il client legge i dati dei pacchetti dalla sezione della memoria condivisa che segue l'intestazione.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-139">The client reads packet data from the section of shared memory that follows the header.</span></span> <span data-ttu-id="a0ef8-140">I numeri di serie vengono visualizzati nella memoria condivisa dopo i dati del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-140">Serial numbers appear in the shared memory after the packet data.</span></span>
5.  <span data-ttu-id="a0ef8-141">Il client gestisce i dati in base al valore di **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-141">The client handles data depending on the value of **dwEvent**.</span></span>
6.  <span data-ttu-id="a0ef8-142">Il client scrive-1 (0xFFFFFFFF) in **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-142">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
7.  <span data-ttu-id="a0ef8-143">Il client rilascia il mutex.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-143">The client releases the mutex.</span></span>
8.  <span data-ttu-id="a0ef8-144">Il client genera l'evento clientReady.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-144">The client raises the clientReady event.</span></span>

<span data-ttu-id="a0ef8-145">I nomi degli eventi vengono creati formattando l'output di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-145">The event names are created by formatting the output of this method.</span></span> <span data-ttu-id="a0ef8-146">Le definizioni seguenti possono essere utilizzate insieme a sprintf o all'equivalente per creare i nomi degli eventi.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-146">The following definitions can be used in conjunction with sprintf or its equivalent to create the event names.</span></span>


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



<span data-ttu-id="a0ef8-147">In ogni definizione la sezione% d viene sostituita con l'ID del processo e la sezione% u viene sostituita con il valore integer restituito in *pdwEventMoreDataId* o *pdwEventClientReadyId*.</span><span class="sxs-lookup"><span data-stu-id="a0ef8-147">In each definition, the %d section is replaced with the process ID, and the %u section is replaced with the integer returned in *pdwEventMoreDataId* or *pdwEventClientReadyId*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0ef8-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0ef8-148">Requirements</span></span>



| <span data-ttu-id="a0ef8-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0ef8-149">Requirement</span></span> | <span data-ttu-id="a0ef8-150">Valore</span><span class="sxs-lookup"><span data-stu-id="a0ef8-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ef8-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0ef8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ef8-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0ef8-152">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a0ef8-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0ef8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ef8-154">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a0ef8-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a0ef8-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0ef8-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0ef8-156"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0ef8-156"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0ef8-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0ef8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ef8-158">**UseSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="a0ef8-158">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[<span data-ttu-id="a0ef8-159">**ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="a0ef8-159">**ITabletContextP**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




