---
title: Metodo INapSystemHealthAgentCallback GetSoHRequest (NapSystemHealthAgent. h)
description: Viene chiamato da NapAgent per eseguire una query sulla richiesta di rapporto di integrità dell'agente integrità sistema.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- NAP metodo GetSoHRequest
- Metodo GetSoHRequest NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400713"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a><span data-ttu-id="d4f58-106">Metodo INapSystemHealthAgentCallback:: GetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="d4f58-106">INapSystemHealthAgentCallback::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="d4f58-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="d4f58-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d4f58-108">Il metodo **INapSystemHealthAgentCallback:: GetSoHRequest** viene chiamato da napagent per eseguire una query sulla richiesta di integrità dell'agente integrità sistema.</span><span class="sxs-lookup"><span data-stu-id="d4f58-108">The **INapSystemHealthAgentCallback::GetSoHRequest** method is called by the NapAgent to query the system health agent's SoH request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f58-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4f58-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="d4f58-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4f58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f58-111">*richiesta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4f58-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f58-112">Puntatore COM a un oggetto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) che identifica l'oggetto Request.</span><span class="sxs-lookup"><span data-stu-id="d4f58-112">A COM pointer to an [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f58-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4f58-113">Return value</span></span>



| <span data-ttu-id="d4f58-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d4f58-114">Return code</span></span>                                                                                                                      | <span data-ttu-id="d4f58-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4f58-115">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4f58-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4f58-116"><dt>**S\_OK**</dt></span></span> </dl>                                             | <span data-ttu-id="d4f58-117">Indica l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d4f58-117">Indicates success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="d4f58-118"><dt>**HRESULT \_ da \_ Win32 ( \_ server RPC \_ non \_ disponibile)**</dt></span><span class="sxs-lookup"><span data-stu-id="d4f58-118"><dt>**HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**</dt></span></span> </dl> | <span data-ttu-id="d4f58-119">Se questo codice viene restituito dall'implementazione, NapAgent rimuove l'SHA dall'elenco Bound-SHA e Scarica la voce della cache.</span><span class="sxs-lookup"><span data-stu-id="d4f58-119">If this code is returned by your implementation, the NapAgent then removes the SHA from the bound-SHA list and flushes its cache entry.</span></span><br/> |



 

<span data-ttu-id="d4f58-120">Quando un valore restituito (ad eccezione di **HRESULT \_ da \_ Win32 (server RPC non \_ \_ \_ disponibile)**) viene restituito dall'implementazione, il sistema di protezione accesso alla rete crea e restituisce un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) all'oggetto convalida integrità corrispondente con i tipi e i valori di attributo seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4f58-120">When any return value (except **HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**) is returned by your implementation, the NAP system constructs and returns a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="d4f58-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="d4f58-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="d4f58-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="d4f58-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="d4f58-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = errore <-codice></span><span class="sxs-lookup"><span data-stu-id="d4f58-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <error-code></span></span>

## <a name="remarks"></a><span data-ttu-id="d4f58-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4f58-124">Remarks</span></span>

<span data-ttu-id="d4f58-125">Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.</span><span class="sxs-lookup"><span data-stu-id="d4f58-125">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="d4f58-126">Questo metodo deve elaborare la richiesta e restituire immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="d4f58-126">This method must process the request and return immediately.</span></span> <span data-ttu-id="d4f58-127">Ritardare la restituzione di questo metodo influisce negativamente sulle prestazioni e la velocità di risposta del sistema e può causare il timeout di altre parti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d4f58-127">Delaying the return of this method negatively impacts system performance and responsiveness, and may cause other parts of the operating system to time out.</span></span>

<span data-ttu-id="d4f58-128">Il monitoraggio dello stato di integrità non deve essere eseguito come parte di questa chiamata, soprattutto se si tratta di un utilizzo intensivo del calcolo e richiede molto tempo.</span><span class="sxs-lookup"><span data-stu-id="d4f58-128">Health state monitoring should not be done as part of this call, especially if it is computation intensive and takes a long time.</span></span> <span data-ttu-id="d4f58-129">Il monitoraggio dello stato di integrità e il calcolo del rapporto di integrità devono essere eseguiti in un thread o un servizio separato.</span><span class="sxs-lookup"><span data-stu-id="d4f58-129">Health state monitoring and SoH computation should be performed in a separate thread or service.</span></span> <span data-ttu-id="d4f58-130">L'unica funzione di questo metodo deve essere quella di impostare il rapporto di integrità SHA e restituire.</span><span class="sxs-lookup"><span data-stu-id="d4f58-130">The sole function of this method should be to set the SHA's SoH and return.</span></span>

<span data-ttu-id="d4f58-131">Se la generazione di un rapporto di integrità da parte di SHA richiede molto tempo, il rapporto di integrità memorizzato nella cache deve essere restituito a NapAgent.</span><span class="sxs-lookup"><span data-stu-id="d4f58-131">If it will take a long time for the SHA to generate a SoH, then the cached SoH should be returned to the NapAgent.</span></span> <span data-ttu-id="d4f58-132">Se non viene restituito alcun rapporto di integrità memorizzato nella cache, l'SHA dovrebbe restituire immediatamente un rapporto di integrità con i tipi e i valori di attributo seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4f58-132">If there is no cached SoH to return, then the SHA should immediately return a SoH with the following attribute types and values:</span></span>

-   <span data-ttu-id="d4f58-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="d4f58-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="d4f58-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="d4f58-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="d4f58-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ nessun rapporto di \_ \_ integrità memorizzato nella cache**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="d4f58-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NO\_CACHED\_SOH**](nap-error-constants.md)</span></span>

<span data-ttu-id="d4f58-136">Quando è stato generato il rapporto di integrità, SHA deve chiamare [**INapSystemHealthAgentBinding:: NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) per notificare al napagent la modifica dell'integrità del sistema.</span><span class="sxs-lookup"><span data-stu-id="d4f58-136">When the SoH has been generated, the SHA must call [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to notify the NapAgent of the system health change.</span></span>

<span data-ttu-id="d4f58-137">NapAgent chiama questo metodo per eseguire una query sul SoHRequest dell'agente integrità sistema.</span><span class="sxs-lookup"><span data-stu-id="d4f58-137">The NapAgent calls this method to query the system health agent's SoHRequest.</span></span> <span data-ttu-id="d4f58-138">SHA può eseguire una query sull'oggetto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) passato per i parametri necessari per calcolare il SoHRequest.</span><span class="sxs-lookup"><span data-stu-id="d4f58-138">The SHA can query the passed [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object for parameters that it needs to compute the SoHRequest.</span></span> <span data-ttu-id="d4f58-139">SHA deve impostare il SoHRequest calcolato nell'oggetto Request.</span><span class="sxs-lookup"><span data-stu-id="d4f58-139">The SHA must set the computed SoHRequest on the request object.</span></span> <span data-ttu-id="d4f58-140">Al termine della chiamata, il SHA non deve conservare riferimenti all'oggetto Request.</span><span class="sxs-lookup"><span data-stu-id="d4f58-140">The SHA must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="d4f58-141">Quando questo metodo viene chiamato, se è presente un rapporto di integrità nella cache di NapAgent, viene impostato sull'oggetto Request.</span><span class="sxs-lookup"><span data-stu-id="d4f58-141">When this method is called, if there is a SoH in the NapAgent's cache, then it is set on the request object.</span></span> <span data-ttu-id="d4f58-142">SHA può eseguire una query per l'oggetto usando **GetSoHRequest**.</span><span class="sxs-lookup"><span data-stu-id="d4f58-142">The SHA can query for it using **GetSoHRequest**.</span></span> <span data-ttu-id="d4f58-143">Se SHA non imposta un nuovo rapporto di integrità, viene usato il valore memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="d4f58-143">If the SHA does not set a new SoH, then the cached one is used.</span></span>

<span data-ttu-id="d4f58-144">Per i SHAs non associati registrati con il sistema, il sistema di protezione accesso alla rete crea e invia un SoHRequest al servizio di convalida dell'integrità di sistema corrispondente con i tipi e i valori di attributo seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4f58-144">For unbound SHAs which are registered with the system, the NAP system constructs and sends a SoHRequest to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="d4f58-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="d4f58-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="d4f58-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="d4f58-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="d4f58-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ non \_ inizializzato**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="d4f58-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NOT\_INITIALIZED**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f58-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4f58-148">Requirements</span></span>



| <span data-ttu-id="d4f58-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4f58-149">Requirement</span></span> | <span data-ttu-id="d4f58-150">Valore</span><span class="sxs-lookup"><span data-stu-id="d4f58-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f58-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4f58-151">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f58-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4f58-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d4f58-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4f58-153">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f58-154">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d4f58-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d4f58-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4f58-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4f58-156"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4f58-156"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4f58-157">IDL</span><span class="sxs-lookup"><span data-stu-id="d4f58-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4f58-158"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4f58-158"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4f58-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4f58-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f58-160">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="d4f58-160">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





