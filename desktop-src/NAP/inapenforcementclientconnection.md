---
title: Interfaccia INapEnforcementClientConnection (NapEnforcementClient. h)
description: Consente la gestione della connessione client. | Interfaccia INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- NAP interfaccia INapEnforcementClientConnection
- Interfaccia NAP di INapEnforcementClientConnection, descrizione
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234688"
---
# <a name="inapenforcementclientconnection-interface"></a><span data-ttu-id="3eae4-106">Interfaccia INapEnforcementClientConnection</span><span class="sxs-lookup"><span data-stu-id="3eae4-106">INapEnforcementClientConnection interface</span></span>

> [!Note]  
> <span data-ttu-id="3eae4-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="3eae4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3eae4-108">**INapEnforcementClientConnection** fornisce metodi che consentono la gestione della connessione client.</span><span class="sxs-lookup"><span data-stu-id="3eae4-108">The **INapEnforcementClientConnection** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="3eae4-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) eredita tutti i metodi di questa interfaccia e deve essere usato in alternativa.</span><span class="sxs-lookup"><span data-stu-id="3eae4-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="3eae4-110">Membri</span><span class="sxs-lookup"><span data-stu-id="3eae4-110">Members</span></span>

<span data-ttu-id="3eae4-111">L'interfaccia **INapEnforcementClientConnection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3eae4-111">The **INapEnforcementClientConnection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3eae4-112">**INapEnforcementClientConnection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3eae4-112">**INapEnforcementClientConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="3eae4-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="3eae4-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3eae4-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="3eae4-114">Methods</span></span>

<span data-ttu-id="3eae4-115">L'interfaccia **INapEnforcementClientConnection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3eae4-115">The **INapEnforcementClientConnection** interface has these methods.</span></span>



| <span data-ttu-id="3eae4-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="3eae4-116">Method</span></span>                                                                                                                           | <span data-ttu-id="3eae4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3eae4-117">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3eae4-118">**INapEnforcementClientConnection:: GetConnectionId**</span><span class="sxs-lookup"><span data-stu-id="3eae4-118">**INapEnforcementClientConnection::GetConnectionId**</span></span>](inapenforcementclientconnection-getconnectionid-method.md)               | <span data-ttu-id="3eae4-119">Ottiene l'ID connessione del client.</span><span class="sxs-lookup"><span data-stu-id="3eae4-119">Gets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="3eae4-120">**INapEnforcementClientConnection::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="3eae4-120">**INapEnforcementClientConnection::GetCorrelationId**</span></span>](inapenforcementclientconnection-getcorrelationid-method.md)             | <span data-ttu-id="3eae4-121">Ottiene l'ID usato per correlare le richieste di rapporto di integrità e le risposte a rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="3eae4-121">Gets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="3eae4-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span><span class="sxs-lookup"><span data-stu-id="3eae4-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-getenforcerprivatedata-method.md) | <span data-ttu-id="3eae4-123">Utilizzato dall'applicazione per ottenere i dati privati.</span><span class="sxs-lookup"><span data-stu-id="3eae4-123">Used by the enforcer to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="3eae4-124">**INapEnforcementClientConnection:: GetFlags**</span><span class="sxs-lookup"><span data-stu-id="3eae4-124">**INapEnforcementClientConnection::GetFlags**</span></span>](inapenforcementclientconnection-getflags-method.md)                             | <span data-ttu-id="3eae4-125">Ottiene il valore del flag che distingue le risposte per la prima volta dalle risposte dovute a SoHRequests memorizzate nella cache dalle forze di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3eae4-125">Gets the value of the flag that differentiates first-time responses from responses due to SoHRequests cached by the enforcers.</span></span><br/> |
| [<span data-ttu-id="3eae4-126">**INapEnforcementClientConnection::GetIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="3eae4-126">**INapEnforcementClientConnection::GetIsolationInfo**</span></span>](inapenforcementclientconnection-getisolationinfo-method.md)             | <span data-ttu-id="3eae4-127">Usato per ottenere le informazioni di isolamento del client.</span><span class="sxs-lookup"><span data-stu-id="3eae4-127">Used get the isolation information of the client.</span></span><br/>                                                                              |
| [<span data-ttu-id="3eae4-128">**INapEnforcementClientConnection::GetMaxSize**</span><span class="sxs-lookup"><span data-stu-id="3eae4-128">**INapEnforcementClientConnection::GetMaxSize**</span></span>](inapenforcementclientconnection-getmaxsize-method.md)                         | <span data-ttu-id="3eae4-129">Ottiene la dimensione massima del pacchetto di rapporto di integrità per il client.</span><span class="sxs-lookup"><span data-stu-id="3eae4-129">Gets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="3eae4-130">**INapEnforcementClientConnection::GetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="3eae4-130">**INapEnforcementClientConnection::GetPrivateData**</span></span>](inapenforcementclientconnection-getprivatedata-method.md)                 | <span data-ttu-id="3eae4-131">Usato da NapAgent per ottenere i dati privati.</span><span class="sxs-lookup"><span data-stu-id="3eae4-131">Used by the NapAgent to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="3eae4-132">**INapEnforcementClientConnection::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="3eae4-132">**INapEnforcementClientConnection::GetSoHRequest**</span></span>](inapenforcementclientconnection-getsohrequest-method.md)                   | <span data-ttu-id="3eae4-133">Ottiene la richiesta di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="3eae4-133">Gets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="3eae4-134">**INapEnforcementClientConnection::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="3eae4-134">**INapEnforcementClientConnection::GetSoHResponse**</span></span>](inapenforcementclientconnection-getsohresponse-method.md)                 | <span data-ttu-id="3eae4-135">Ottiene la SoH-Response ricevuta dal client di imposizione.</span><span class="sxs-lookup"><span data-stu-id="3eae4-135">Gets the SoH-Response received by the enforcement client.</span></span><br/>                                                                      |
| [<span data-ttu-id="3eae4-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="3eae4-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span></span>](inapenforcementclientconnection-getstringcorrelationid-method.md) | <span data-ttu-id="3eae4-137">Ottiene la versione in formato stringa dell'oggetto CorrelationId.</span><span class="sxs-lookup"><span data-stu-id="3eae4-137">Gets the string version of the CorrelationId.</span></span> <span data-ttu-id="3eae4-138">Utilizzato principalmente per scopi di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3eae4-138">Used primarily for logging purposes.</span></span><br/>                                             |
| [<span data-ttu-id="3eae4-139">**INapEnforcementClientConnection:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="3eae4-139">**INapEnforcementClientConnection::Initialize**</span></span>](inapenforcementclientconnection-initialize-method.md)                         | <span data-ttu-id="3eae4-140">Inizializza la raccolta.</span><span class="sxs-lookup"><span data-stu-id="3eae4-140">Initializes the connection.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="3eae4-141">**INapEnforcementClientConnection::SetConnectionId**</span><span class="sxs-lookup"><span data-stu-id="3eae4-141">**INapEnforcementClientConnection::SetConnectionId**</span></span>](inapenforcementclientconnection-setconnectionid-method.md)               | <span data-ttu-id="3eae4-142">Imposta l'ID connessione del client.</span><span class="sxs-lookup"><span data-stu-id="3eae4-142">Sets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="3eae4-143">**INapEnforcementClientConnection::SetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="3eae4-143">**INapEnforcementClientConnection::SetCorrelationId**</span></span>](inapenforcementclientconnection-setcorrelationid-method.md)             | <span data-ttu-id="3eae4-144">Imposta l'ID usato per correlare le richieste di rapporto di integrità e le risposte a rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="3eae4-144">Sets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="3eae4-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span><span class="sxs-lookup"><span data-stu-id="3eae4-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-setenforcerprivatedata-method.md) | <span data-ttu-id="3eae4-146">Utilizzato dall'applicazione per impostare i dati privati.</span><span class="sxs-lookup"><span data-stu-id="3eae4-146">Used by the enforcer to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="3eae4-147">**INapEnforcementClientConnection:: Flags**</span><span class="sxs-lookup"><span data-stu-id="3eae4-147">**INapEnforcementClientConnection::SetFlags**</span></span>](inapenforcementclientconnection-setflags-method.md)                             | <span data-ttu-id="3eae4-148">Imposta il flag che distingue le risposte per la prima volta dalle risposte dovute a SoHRequests memorizzate nella cache da Enforcer.</span><span class="sxs-lookup"><span data-stu-id="3eae4-148">Sets the flag that differentiates first-time responses from responses due to SoHRequests cached by enforcers.</span></span><br/>                  |
| [<span data-ttu-id="3eae4-149">**INapEnforcementClientConnection::SetIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="3eae4-149">**INapEnforcementClientConnection::SetIsolationInfo**</span></span>](inapenforcementclientconnection-setisolationinfo-method.md)             | <span data-ttu-id="3eae4-150">Utilizzato da NapAgent per impostare le informazioni di isolamento del client.</span><span class="sxs-lookup"><span data-stu-id="3eae4-150">Used by the NapAgent to set the isolation information of the client.</span></span><br/>                                                           |
| [<span data-ttu-id="3eae4-151">**INapEnforcementClientConnection::SetMaxSize**</span><span class="sxs-lookup"><span data-stu-id="3eae4-151">**INapEnforcementClientConnection::SetMaxSize**</span></span>](inapenforcementclientconnection-setmaxsize-method.md)                         | <span data-ttu-id="3eae4-152">Imposta la dimensione massima del pacchetto di rapporto di integrità per il client.</span><span class="sxs-lookup"><span data-stu-id="3eae4-152">Sets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="3eae4-153">**INapEnforcementClientConnection::SetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="3eae4-153">**INapEnforcementClientConnection::SetPrivateData**</span></span>](inapenforcementclientconnection-setprivatedata-method.md)                 | <span data-ttu-id="3eae4-154">Usato da NapAgent per impostare i dati privati.</span><span class="sxs-lookup"><span data-stu-id="3eae4-154">Used by the NapAgent to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="3eae4-155">**INapEnforcementClientConnection::SetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="3eae4-155">**INapEnforcementClientConnection::SetSoHRequest**</span></span>](inapenforcementclientconnection-setsohrequest-method.md)                   | <span data-ttu-id="3eae4-156">Imposta la richiesta di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="3eae4-156">Sets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="3eae4-157">**INapEnforcementClientConnection::SetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="3eae4-157">**INapEnforcementClientConnection::SetSoHResponse**</span></span>](inapenforcementclientconnection-setsohresponse-method.md)                 | <span data-ttu-id="3eae4-158">Imposta il SoH-Response e viene utilizzato dal client di imposizione per la ricezione di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3eae4-158">Sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span><br/>                                             |



 

## <a name="requirements"></a><span data-ttu-id="3eae4-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3eae4-159">Requirements</span></span>



| <span data-ttu-id="3eae4-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eae4-160">Requirement</span></span> | <span data-ttu-id="3eae4-161">Valore</span><span class="sxs-lookup"><span data-stu-id="3eae4-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eae4-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eae4-162">Minimum supported client</span></span><br/> | <span data-ttu-id="3eae4-163">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3eae4-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3eae4-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eae4-164">Minimum supported server</span></span><br/> | <span data-ttu-id="3eae4-165">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3eae4-165">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3eae4-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3eae4-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="3eae4-167"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eae4-167"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3eae4-168">IDL</span><span class="sxs-lookup"><span data-stu-id="3eae4-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3eae4-169"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3eae4-169"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="3eae4-170">DLL</span><span class="sxs-lookup"><span data-stu-id="3eae4-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3eae4-171"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eae4-171"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3eae4-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3eae4-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eae4-173">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="3eae4-173">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3eae4-174">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="3eae4-174">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

