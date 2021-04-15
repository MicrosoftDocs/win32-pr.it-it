---
title: Metodo IConnectionBrokerClient GetTargetInfo (Cbclient. h)
description: Richiede informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetTargetInfo
- Metodo GetTargetInfo Servizi Desktop remoto, interfaccia IConnectionBrokerClient
- Interfaccia IConnectionBrokerClient Servizi Desktop remoto, metodo GetTargetInfo
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517368"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a><span data-ttu-id="fb825-106">Metodo IConnectionBrokerClient:: GetTargetInfo</span><span class="sxs-lookup"><span data-stu-id="fb825-106">IConnectionBrokerClient::GetTargetInfo method</span></span>

<span data-ttu-id="fb825-107">Richiede informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione.</span><span class="sxs-lookup"><span data-stu-id="fb825-107">Requests information about the target computer where the connection should be redirected.</span></span> <span data-ttu-id="fb825-108">Questo metodo viene utilizzato dal redirector per ottenere informazioni di reindirizzamento per la richiesta di connessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="fb825-108">This method is used by the redirector to get redirection information for the incoming connection request.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb825-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb825-109">Syntax</span></span>


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a><span data-ttu-id="fb825-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb825-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb825-111">*pConnectionInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb825-111">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb825-112">Indirizzo di una struttura [**di \_ \_ informazioni di connessione CB**](cb-connection-info.md) che contiene informazioni sulla richiesta di connessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="fb825-112">The address of a [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure that contains information about the incoming connection request.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-113">*Riservato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb825-113">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb825-114">Questo parametro è riservato per utilizzi futuri e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fb825-114">This parameter is reserved for future use and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-115">*hStatusEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb825-115">*hStatusEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb825-116">Handle di un evento che verrà impostato ogni volta che viene eseguito un aggiornamento dello stato di avanzamento della richiesta.</span><span class="sxs-lookup"><span data-stu-id="fb825-116">The handle of an event that will get set whenever there is an update to the progress of the request.</span></span> <span data-ttu-id="fb825-117">L'utente è responsabile della creazione e della chiusura di questo evento.</span><span class="sxs-lookup"><span data-stu-id="fb825-117">You are responsible for creating and closing this event.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-118">*pTargetInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb825-118">*pTargetInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb825-119">Indirizzo di una struttura [**di \_ \_ informazioni di destinazione del CB**](cb-target-info.md) che riceve informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="fb825-119">The address of a [**CB\_TARGET\_INFO**](cb-target-info.md) structure that receives information about the target computer where the incoming connection should be redirected.</span></span> <span data-ttu-id="fb825-120">Poiché si tratta di un metodo asincrono, questa memoria deve rimanere disponibile fino al completamento della richiesta.</span><span class="sxs-lookup"><span data-stu-id="fb825-120">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="fb825-121">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="fb825-121">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-122">*pResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb825-122">*pResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb825-123">Indirizzo di una variabile **DWORD** che riceve un codice risultato.</span><span class="sxs-lookup"><span data-stu-id="fb825-123">The address of a **DWORD** variable that receives a result code.</span></span> <span data-ttu-id="fb825-124">Poiché si tratta di un metodo asincrono, questa memoria deve rimanere disponibile fino al completamento della richiesta.</span><span class="sxs-lookup"><span data-stu-id="fb825-124">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="fb825-125">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="fb825-125">For more information, see Remarks.</span></span>

<span data-ttu-id="fb825-126">Il codice risultante sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fb825-126">This result code will be one of the following values.</span></span>

<dt>

<span data-ttu-id="fb825-127">0</span><span class="sxs-lookup"><span data-stu-id="fb825-127">0</span></span>
</dt> <dd>

<span data-ttu-id="fb825-128">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fb825-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-129">0x0000400</span><span class="sxs-lookup"><span data-stu-id="fb825-129">0x0000400</span></span>
</dt> <dd>

<span data-ttu-id="fb825-130">Il computer di destinazione non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="fb825-130">The destination computer could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-131">0x0000401</span><span class="sxs-lookup"><span data-stu-id="fb825-131">0x0000401</span></span>
</dt> <dd>

<span data-ttu-id="fb825-132">Il computer di destinazione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="fb825-132">The destination computer is not available.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-133">0x0000402</span><span class="sxs-lookup"><span data-stu-id="fb825-133">0x0000402</span></span>
</dt> <dd>

<span data-ttu-id="fb825-134">Errore durante il caricamento del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fb825-134">Error loading destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-135">0x0000403</span><span class="sxs-lookup"><span data-stu-id="fb825-135">0x0000403</span></span>
</dt> <dd>

<span data-ttu-id="fb825-136">Errore durante la porta del computer di destinazione online.</span><span class="sxs-lookup"><span data-stu-id="fb825-136">Error bringing destination computer online.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-137">0x0000404</span><span class="sxs-lookup"><span data-stu-id="fb825-137">0x0000404</span></span>
</dt> <dd>

<span data-ttu-id="fb825-138">Errore durante il reindirizzamento al computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fb825-138">Error redirecting to destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-139">0x0000405</span><span class="sxs-lookup"><span data-stu-id="fb825-139">0x0000405</span></span>
</dt> <dd>

<span data-ttu-id="fb825-140">Errore durante il riattivazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb825-140">Error waking virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-141">0x0000406</span><span class="sxs-lookup"><span data-stu-id="fb825-141">0x0000406</span></span>
</dt> <dd>

<span data-ttu-id="fb825-142">Errore durante l'avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb825-142">Error booting virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-143">0x0000407</span><span class="sxs-lookup"><span data-stu-id="fb825-143">0x0000407</span></span>
</dt> <dd>

<span data-ttu-id="fb825-144">Errore durante la ricerca dell'indirizzo IP della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb825-144">Error finding the IP address of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-145">0x0000408</span><span class="sxs-lookup"><span data-stu-id="fb825-145">0x0000408</span></span>
</dt> <dd>

<span data-ttu-id="fb825-146">Il broker di sessione non è riuscito a trovare i computer disponibili nel pool.</span><span class="sxs-lookup"><span data-stu-id="fb825-146">The session broker could not find any available computers in the pool.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-147">0x0000409</span><span class="sxs-lookup"><span data-stu-id="fb825-147">0x0000409</span></span>
</dt> <dd>

<span data-ttu-id="fb825-148">Il broker di sessione ha annullato la connessione.</span><span class="sxs-lookup"><span data-stu-id="fb825-148">The session broker canceled the connection.</span></span>

</dd> <dt>

<span data-ttu-id="fb825-149">0x0000410</span><span class="sxs-lookup"><span data-stu-id="fb825-149">0x0000410</span></span>
</dt> <dd>

<span data-ttu-id="fb825-150">Il broker di sessione non è riuscito a convalidare le impostazioni di connessione.</span><span class="sxs-lookup"><span data-stu-id="fb825-150">The session broker could not validate the connection settings.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fb825-151">*ppCbReq* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb825-151">*ppCbReq* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb825-152">Indirizzo di un puntatore a interfaccia [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) usato per ottenere gli aggiornamenti di stato per un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="fb825-152">The address of an [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) interface pointer that you use to obtain status updates for an asynchronous operation.</span></span> <span data-ttu-id="fb825-153">Questa interfaccia viene utilizzata insieme al parametro *hStatusEvent* per attendere e ottenere i risultati di questa operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="fb825-153">This interface is used in conjunction with the *hStatusEvent* parameter to wait for and get the results of this asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb825-154">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb825-154">Return value</span></span>

<span data-ttu-id="fb825-155">Restituisce **E \_ in sospeso** se la richiesta asincrona viene creata.</span><span class="sxs-lookup"><span data-stu-id="fb825-155">Returns **E\_PENDING** if the asynchronous request is created.</span></span> <span data-ttu-id="fb825-156">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb825-156">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb825-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb825-157">Remarks</span></span>

<span data-ttu-id="fb825-158">Questo metodo è asincrono.</span><span class="sxs-lookup"><span data-stu-id="fb825-158">This method is asynchronous.</span></span> <span data-ttu-id="fb825-159">I parametri *pTargetInfo* e *pResult* devono rimanere validi finché il metodo [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) non ottiene la richiesta di **stato CB \_ \_ \_ completata**.</span><span class="sxs-lookup"><span data-stu-id="fb825-159">The *pTargetInfo* and *pResult* parameters must remain valid until the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method obtains **CB\_STATUS\_REQUEST\_COMPLETED**.</span></span>

<span data-ttu-id="fb825-160">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [come utilizzare l'API client di connessione Desktop remoto broker](use-the-remote-desktop-connection-broker-client-api.md).</span><span class="sxs-lookup"><span data-stu-id="fb825-160">For more information about how to use this method, see [How to use the Remote Desktop Connection Broker client API](use-the-remote-desktop-connection-broker-client-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb825-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb825-161">Requirements</span></span>



| <span data-ttu-id="fb825-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb825-162">Requirement</span></span> | <span data-ttu-id="fb825-163">Valore</span><span class="sxs-lookup"><span data-stu-id="fb825-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb825-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb825-164">Minimum supported client</span></span><br/> | <span data-ttu-id="fb825-165">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fb825-165">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="fb825-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb825-166">Minimum supported server</span></span><br/> | <span data-ttu-id="fb825-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb825-167">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="fb825-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb825-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb825-169"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb825-169"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb825-170">Libreria</span><span class="sxs-lookup"><span data-stu-id="fb825-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb825-171"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb825-171"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="fb825-172">DLL</span><span class="sxs-lookup"><span data-stu-id="fb825-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb825-173"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb825-173"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb825-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb825-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb825-175">**IConnectionBrokerClient**</span><span class="sxs-lookup"><span data-stu-id="fb825-175">**IConnectionBrokerClient**</span></span>](iconnectionbrokerclient.md)
</dt> </dl>

 

 





