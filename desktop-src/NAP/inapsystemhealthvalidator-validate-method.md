---
title: Metodo Validate INapSystemHealthValidator (NapSystemHealthValidator. h)
description: Sistema di protezione accesso alla rete per convalidare il SoHRequest ricevuto da un client.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Convalida NAP metodo
- Metodo Validate NAP, interfaccia INapSystemHealthValidator
- Interfaccia INapSystemHealthValidator NAP, metodo Validate
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301364"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a><span data-ttu-id="a0590-106">Metodo INapSystemHealthValidator:: Validate</span><span class="sxs-lookup"><span data-stu-id="a0590-106">INapSystemHealthValidator::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="a0590-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="a0590-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a0590-108">Il metodo **INapSystemHealthValidator:: Validate** viene definito dallo sviluppatore del servizio di convalida dell'integrità di sistema e chiamato dal sistema NAP per convalidare il [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ricevuto da un client.</span><span class="sxs-lookup"><span data-stu-id="a0590-108">The **INapSystemHealthValidator::Validate** method is defined by the SHV developer and called by the NAP system to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0590-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0590-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a><span data-ttu-id="a0590-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0590-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0590-111">*richiesta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0590-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0590-112">Puntatore COM a un oggetto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) che identifica l'oggetto della richiesta di convalida.</span><span class="sxs-lookup"><span data-stu-id="a0590-112">A COM pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that identifies the validation request object.</span></span>

</dd> <dt>

<span data-ttu-id="a0590-113">*hintTimeOutInMsec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0590-113">*hintTimeOutInMsec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0590-114">Durata, in millisecondi, del periodo di timeout della comunicazione.</span><span class="sxs-lookup"><span data-stu-id="a0590-114">The duration, in milliseconds, of the communication timeout period.</span></span> <span data-ttu-id="a0590-115">Il servizio di convalida dell'integrità di sistema deve rispondere entro questo periodo di tempo; in caso contrario, la risposta viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="a0590-115">The System Health Validator (SHV) should respond within this amount of time; otherwise the response is dropped.</span></span>

> [!Note]  
> <span data-ttu-id="a0590-116">Il timeout predefinito per tutti SHV è pari a 2000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a0590-116">The default timeout for all SHVs is 2000 milliseconds.</span></span> <span data-ttu-id="a0590-117">Se si usa un valore diverso da quello predefinito, il timeout per tutti i SHV registrati viene modificato.</span><span class="sxs-lookup"><span data-stu-id="a0590-117">Using a value other than the default will change the timeout for all registered SHVs.</span></span>

 

</dd> <dt>

<span data-ttu-id="a0590-118">*callback* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a0590-118">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0590-119">Puntatore all'oggetto callback [**INapServerCallback**](inapservercallback.md).</span><span class="sxs-lookup"><span data-stu-id="a0590-119">A pointer to the callback object [**INapServerCallback**](inapservercallback.md).</span></span> <span data-ttu-id="a0590-120">Questo puntatore di callback viene usato da SHV quando restituisce **E \_ in sospeso** dalla chiamata a **INapSystemHealthValidator:: Validate**.</span><span class="sxs-lookup"><span data-stu-id="a0590-120">This callback pointer is used by the SHVs when they return **E\_PENDING** from the call to **INapSystemHealthValidator::Validate**.</span></span> <span data-ttu-id="a0590-121">Viene utilizzato per la convalida asincrona.</span><span class="sxs-lookup"><span data-stu-id="a0590-121">This is used for asynchronous validation.</span></span> <span data-ttu-id="a0590-122">È previsto che il SHV risponda entro il tempo di *hintTimeOutInMsec* . in caso contrario, la risposta verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="a0590-122">The SHVs are expected to respond within the *hintTimeOutInMsec* time or else the response will be dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0590-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0590-123">Return value</span></span>

<span data-ttu-id="a0590-124">Se viene restituito un altro codice di errore, il sistema presuppone che si sia verificato un errore serverComponent ed è stato eseguito il mapping appropriato per il superamento o l'esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a0590-124">If any other error code is returned, then the system assumes serverComponent failure has occurred, and the appropriate mapping is done to pass/fail.</span></span>



| <span data-ttu-id="a0590-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a0590-125">Return code</span></span>                                                                                                | <span data-ttu-id="a0590-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0590-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a0590-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a0590-127"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="a0590-128">Indica che il validator ha impostato un SoHResponse sull'oggetto ' request '.</span><span class="sxs-lookup"><span data-stu-id="a0590-128">Indicates that the validator has set an SoHResponse on the 'request' object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="a0590-129"><dt>**E \_ in sospeso**</dt></span><span class="sxs-lookup"><span data-stu-id="a0590-129"><dt>**E\_PENDING**</dt></span></span> </dl>                  | <span data-ttu-id="a0590-130">Indica che OnComplete () verrà chiamato su un thread separato.</span><span class="sxs-lookup"><span data-stu-id="a0590-130">Indicates that OnComplete() will be called on a separate thread.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="a0590-131"><dt>**\_server RPC \_ non \_ disponibile**</dt></span><span class="sxs-lookup"><span data-stu-id="a0590-131"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="a0590-132">Indica che il processo di convalida dell'integrità di sistema (convalida integrità sistema) è stato terminato senza NapServer effettivamente il rilascio di un riferimento.</span><span class="sxs-lookup"><span data-stu-id="a0590-132">Indicates that the System Health Validator (SHV) process terminated without the NapServer actually releasing a reference to it.</span></span> <span data-ttu-id="a0590-133">NapServer tenterà di ricreare un nuovo riferimento al servizio di convalida dell'integrità di sistema e eseguirà nuovamente la chiamata di convalida una volta.</span><span class="sxs-lookup"><span data-stu-id="a0590-133">The NapServer will try to re-create a new reference to the SHV and will reexecute the Validate call once.</span></span> <span data-ttu-id="a0590-134">Se la creazione dell'oggetto o della convalida rieseguita non riesce, il servizio di convalida dell'integrità di sistema viene rimosso dall'elenco dei SHV caricati.</span><span class="sxs-lookup"><span data-stu-id="a0590-134">If the creation of the object or the re-executed Validate fails, the SHV is removed from the list of loaded SHVs.</span></span> <span data-ttu-id="a0590-135">L'unico modo in cui è possibile ricaricare il servizio di convalida dell'integrità di sistema è quello di annullare la registrazione e registrare di nuovo il servizio di convalida dell'integrità oppure al riavvio del NapServer.</span><span class="sxs-lookup"><span data-stu-id="a0590-135">The only way this SHV can now be reloaded is to unregister and reregister the SHV again, or when the NapServer restarts</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a0590-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0590-136">Remarks</span></span>

<span data-ttu-id="a0590-137">Per supportare il rilevamento delle intrusioni, a SHV verrà richiesto di convalidare il computer client indipendentemente dal fatto che il client abbia inviato un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) per il servizio di convalida dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="a0590-137">In order to support intrusion detection, SHVs will be asked to validate the client machine regardless of whether the client sent an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) intended for the SHV.</span></span>

<span data-ttu-id="a0590-138">Il servizio di convalida dell'integrità deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0590-138">The SHV must do the following:</span></span>

-   <span data-ttu-id="a0590-139">Recuperare il [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) da *Request* chiamando [**Request. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="a0590-139">Retrieve the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) from *request* by calling [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span></span>
-   <span data-ttu-id="a0590-140">Se il pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è null:</span><span class="sxs-lookup"><span data-stu-id="a0590-140">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is null:</span></span>
    -   <span data-ttu-id="a0590-141">Se il servizio di convalida dell'integrità di sistema è un sistema di rilevamento delle intrusioni, popolare un pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con il [**codice di errore NAP**](nap-error-constants.md) appropriato per il motivo per cui il computer client è dannoso</span><span class="sxs-lookup"><span data-stu-id="a0590-141">If the SHV is an intrusion detection system, populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the appropriate [**NAP error code**](nap-error-constants.md) as to why the client machine is malicious.</span></span>
    -   <span data-ttu-id="a0590-142">Tutti gli altri SHV devono popolare un pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con un codice di errore [**NAP \_ E \_ Missing \_ SOH**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a0590-142">All other SHVs should populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with an error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>
-   <span data-ttu-id="a0590-143">Se *napSystemGenerated* è **true** dalla chiamata a [**Request. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), il servizio di convalida dell'integrità deve prevedere un pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) con i seguenti 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span><span class="sxs-lookup"><span data-stu-id="a0590-143">If *napSystemGenerated* is **TRUE** from the call to [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), the SHV should expect an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the following 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span></span> <span data-ttu-id="a0590-144">Questo **SoHRequest** viene generato da napagent per conto dell'agente integrità sistema (SHA) perché si è verificato un errore durante il recupero di un pacchetto di richiesta dall'SHA.</span><span class="sxs-lookup"><span data-stu-id="a0590-144">This **SoHRequest** is generated by the NapAgent on behalf of the System Health Agent (SHA) since there was an error in retrieving a request packet from the SHA.</span></span>
-   <span data-ttu-id="a0590-145">Convalidare il pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="a0590-145">Validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>
    -   <span data-ttu-id="a0590-146">Se il [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) non è valido, costruire un pacchetto **SoHResponse** con il [**\_ pacchetto NAP E il \_ \_ pacchetto non valido**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a0590-146">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) is malformed, then construct a **SoHResponse** packet with error code [**NAP\_E\_INVALID\_PACKET**](nap-error-constants.md).</span></span>
    -   <span data-ttu-id="a0590-147">Se il servizio di convalida dell'integrità di sistema usa solo le informazioni memorizzate nella cache per convalidare il pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (ovvero non viene eseguita alcuna operazione di i/O), può costruire il **SoHResponse**, impostarlo sull'oggetto nella *richiesta* e restituire **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a0590-147">If the SHV is only using cached information to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet (i.e. no I/O is performed), then it can construct the **SoHResponse**, set it on the object in *request* and return **S\_OK**.</span></span>
    -   <span data-ttu-id="a0590-148">Se il servizio di convalida dell'integrità di sistema esegue operazioni di I/O per comunicare con i server back-end per convalidare l'integrità del client, deve accodare l'i/O e restituire questa funzione con **e \_ in sospeso**.</span><span class="sxs-lookup"><span data-stu-id="a0590-148">If the SHV is performing I/O in order to talk to its back-end servers to validate the client's health, then it must queue up the I/O and return this function with **E\_PENDING**.</span></span> <span data-ttu-id="a0590-149">In questo caso, il servizio di convalida dell'integrità di sistema deve chiamare [**callback. OnComplete ()**](inapservercallback-oncomplete-method.md) in un thread separato entro il periodo di timeout, *hintTimeOutInMsec*.</span><span class="sxs-lookup"><span data-stu-id="a0590-149">In this case, the SHV must call [**callback.OnComplete()**](inapservercallback-oncomplete-method.md) on a separate thread within the timeout period, *hintTimeOutInMsec*.</span></span> <span data-ttu-id="a0590-150">In caso contrario, la risposta di convalida integrità sistema verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="a0590-150">Otherwise, the SHV's response will be dropped.</span></span>
-   <span data-ttu-id="a0590-151">Non restituire altri errori diversi da quelli elencati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="a0590-151">Do not return any other error other than those listed above.</span></span> <span data-ttu-id="a0590-152">Se il servizio di convalida dell'integrità di sistema restituisce un altro codice di errore (ad esempio,</span><span class="sxs-lookup"><span data-stu-id="a0590-152">If any other error code is returned by the SHV (eg.</span></span> <span data-ttu-id="a0590-153">un errore di sistema), il pacchetto verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="a0590-153">some system error), the packet will be discarded.</span></span>

<span data-ttu-id="a0590-154">Un servizio di convalida dell'integrità di sistema deve restituire un **sohAttributeTypeComplianceResultCodes** o **sohAttributeTypeFailureCategory** TLV nel relativo [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="a0590-154">An SHV must return either an **sohAttributeTypeComplianceResultCodes** or **sohAttributeTypeFailureCategory** TLV in its [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

-   <span data-ttu-id="a0590-155">[**SOHATTRIBUTETYPECOMPLIANCERESULTCODES TLV**](sohattributetype-enum.md): se il servizio di convalida dell'integrità di sistema può convalidare l'integrità del client (ad esempio integro o non integro), viene restituito questo TLV.</span><span class="sxs-lookup"><span data-stu-id="a0590-155">[**sohAttributeTypeComplianceResultCodes TLV**](sohattributetype-enum.md): If the SHV could validate the health of the client (i.e. healthy or unhealthy), this TLV is returned.</span></span>
-   <span data-ttu-id="a0590-156">[**SOHATTRIBUTETYPEFAILURECATEGORY TLV**](sohattributetype-enum.md): se si è verificato un errore di comunicazione o componente nel client o nel server, questo deve essere indicato da questo TLV.</span><span class="sxs-lookup"><span data-stu-id="a0590-156">[**sohAttributeTypeFailureCategory TLV**](sohattributetype-enum.md): If there was any component or communication failure on the client or server, it must be indicated by this TLV.</span></span> <span data-ttu-id="a0590-157">Questo TLV verrà ulteriormente mappato a integro o non integro a seconda della configurazione del servizio di convalida dell'integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="a0590-157">This TLV will further be mapped to healthy or unhealthy depending upon the SHV's configuration.</span></span> <span data-ttu-id="a0590-158">Per altri dettagli, vedere l'interfaccia [**INapServerManagement**](inapservermanagement.md) e la struttura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .</span><span class="sxs-lookup"><span data-stu-id="a0590-158">For more details, see the [**INapServerManagement**](inapservermanagement.md) interface and the [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>

<span data-ttu-id="a0590-159">Il servizio di convalida dell'integrità di sistema non deve conservare riferimenti alla *richiesta* o al *callback* al completamento della chiamata asincrono.</span><span class="sxs-lookup"><span data-stu-id="a0590-159">The SHV must not hold references to *request* or *callback* once the asyncronous call completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0590-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0590-160">Requirements</span></span>



| <span data-ttu-id="a0590-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0590-161">Requirement</span></span> | <span data-ttu-id="a0590-162">Valore</span><span class="sxs-lookup"><span data-stu-id="a0590-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0590-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0590-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a0590-164">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a0590-164">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="a0590-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0590-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a0590-166">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0590-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0590-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0590-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0590-168"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0590-168"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0590-169">IDL</span><span class="sxs-lookup"><span data-stu-id="a0590-169">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0590-170"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0590-170"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0590-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0590-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0590-172">**INapSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="a0590-172">**INapSystemHealthValidator**</span></span>](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





