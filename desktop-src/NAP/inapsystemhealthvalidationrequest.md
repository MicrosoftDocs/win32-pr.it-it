---
title: Interfaccia INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: Vengono utilizzati per supportare i validator di integrità del sistema definiti dallo sviluppatore di applicazioni.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- NAP interfaccia INapSystemHealthValidationRequest
- Interfaccia NAP di INapSystemHealthValidationRequest, descrizione
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf09f93e00401251a3d0e2296323edeb84ad6007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743535"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a><span data-ttu-id="66386-105">Interfaccia INapSystemHealthValidationRequest</span><span class="sxs-lookup"><span data-stu-id="66386-105">INapSystemHealthValidationRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="66386-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="66386-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="66386-107">L'interfaccia **INapSystemHealthValidationRequest** fornisce i metodi utilizzati per supportare i validator dell'integrità di sistema definiti dallo sviluppatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="66386-107">The **INapSystemHealthValidationRequest** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="66386-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) eredita tutti i metodi di questa interfaccia e deve essere usato in alternativa.</span><span class="sxs-lookup"><span data-stu-id="66386-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="66386-109">Membri</span><span class="sxs-lookup"><span data-stu-id="66386-109">Members</span></span>

<span data-ttu-id="66386-110">L'interfaccia **INapSystemHealthValidationRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="66386-110">The **INapSystemHealthValidationRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="66386-111">**INapSystemHealthValidationRequest** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="66386-111">**INapSystemHealthValidationRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="66386-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="66386-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="66386-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="66386-113">Methods</span></span>

<span data-ttu-id="66386-114">L'interfaccia **INapSystemHealthValidationRequest** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="66386-114">The **INapSystemHealthValidationRequest** interface has these methods.</span></span>



| <span data-ttu-id="66386-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="66386-115">Method</span></span>                                                                                                                               | <span data-ttu-id="66386-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66386-116">Description</span></span>                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66386-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="66386-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | <span data-ttu-id="66386-118">Utilizzato dai validator per recuperare l'ID di correlazione.</span><span class="sxs-lookup"><span data-stu-id="66386-118">Used by validators to retrieve the correlation ID.</span></span> <span data-ttu-id="66386-119">Il validator deve quindi registrare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="66386-119">The validator must then log this information.</span></span><br/>           |
| [<span data-ttu-id="66386-120">**INapSystemHealthValidationRequest:: GetMachineName**</span><span class="sxs-lookup"><span data-stu-id="66386-120">**INapSystemHealthValidationRequest::GetMachineName**</span></span>](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | <span data-ttu-id="66386-121">Utilizzato dai validator per recuperare il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="66386-121">Used by validators to retrieve the machine name.</span></span> <span data-ttu-id="66386-122">Il validator deve quindi registrare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="66386-122">The validator must then log this information.</span></span><br/>             |
| [<span data-ttu-id="66386-123">**INapSystemHealthValidationRequest::GetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="66386-123">**INapSystemHealthValidationRequest::GetPrivateData**</span></span>](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | <span data-ttu-id="66386-124">Consente al NapServer di recuperare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="66386-124">Allows the NapServer to retrieve state information.</span></span><br/>                                                        |
| [<span data-ttu-id="66386-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="66386-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span></span>](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | <span data-ttu-id="66386-126">Consente ai validator di recuperare e convalidare le informazioni SoHRequest.</span><span class="sxs-lookup"><span data-stu-id="66386-126">Allows Validators to retrieve and validate the SoHRequest information.</span></span><br/>                                     |
| [<span data-ttu-id="66386-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="66386-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | <span data-ttu-id="66386-128">Ottiene l'oggetto SoHResponse.</span><span class="sxs-lookup"><span data-stu-id="66386-128">Gets the SoHResponse object.</span></span><br/>                                                                               |
| [<span data-ttu-id="66386-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="66386-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | <span data-ttu-id="66386-130">Utilizzato dai validator per recuperare un identificatore univoco di Exchange.</span><span class="sxs-lookup"><span data-stu-id="66386-130">Used by validators to retrieve a unique exchange identifier.</span></span> <span data-ttu-id="66386-131">Il validator deve quindi registrare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="66386-131">The validator must then log this information.</span></span><br/> |
| [<span data-ttu-id="66386-132">**INapSystemHealthValidationRequest::SetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="66386-132">**INapSystemHealthValidationRequest::SetPrivateData**</span></span>](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | <span data-ttu-id="66386-133">Consente all'NapServer di archiviare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="66386-133">Allows the NapServer to store state information.</span></span><br/>                                                           |
| [<span data-ttu-id="66386-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="66386-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | <span data-ttu-id="66386-135">Consente ai validator di impostare SoHResponse.</span><span class="sxs-lookup"><span data-stu-id="66386-135">Allows validators to set the SoHResponse.</span></span><br/>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="66386-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66386-136">Requirements</span></span>



| <span data-ttu-id="66386-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="66386-137">Requirement</span></span> | <span data-ttu-id="66386-138">Valore</span><span class="sxs-lookup"><span data-stu-id="66386-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66386-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66386-139">Minimum supported client</span></span><br/> | <span data-ttu-id="66386-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="66386-140">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="66386-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66386-141">Minimum supported server</span></span><br/> | <span data-ttu-id="66386-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66386-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66386-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66386-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="66386-144"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="66386-144"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="66386-145">IDL</span><span class="sxs-lookup"><span data-stu-id="66386-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66386-146"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66386-146"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="66386-147">DLL</span><span class="sxs-lookup"><span data-stu-id="66386-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66386-148"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66386-148"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="66386-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66386-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66386-150">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="66386-150">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="66386-151">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="66386-151">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

