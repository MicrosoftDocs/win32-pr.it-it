---
title: Interfaccia INapSystemHealthAgentCallback (NapSystemHealthAgent. h)
description: Sono dichiarati dal sistema e implementati dal writer SHA in modo che NapAgent possa comunicare con l'SHA.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- NAP interfaccia INapSystemHealthAgentCallback
- Interfaccia NAP di INapSystemHealthAgentCallback, descrizione
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302256"
---
# <a name="inapsystemhealthagentcallback-interface"></a><span data-ttu-id="896d7-105">Interfaccia INapSystemHealthAgentCallback</span><span class="sxs-lookup"><span data-stu-id="896d7-105">INapSystemHealthAgentCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="896d7-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="896d7-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="896d7-107">L'interfaccia **INapSystemHealthAgentCallback** fornisce metodi di callback dichiarati dal sistema e implementati dal writer Sha in modo che napagent possa comunicare con l'SHA.</span><span class="sxs-lookup"><span data-stu-id="896d7-107">The **INapSystemHealthAgentCallback** interface provides callback methods that are declared by the system and implemented by the SHA writer so the NapAgent can communicate with the SHA.</span></span>

## <a name="members"></a><span data-ttu-id="896d7-108">Membri</span><span class="sxs-lookup"><span data-stu-id="896d7-108">Members</span></span>

<span data-ttu-id="896d7-109">L'interfaccia **INapSystemHealthAgentCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="896d7-109">The **INapSystemHealthAgentCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="896d7-110">**INapSystemHealthAgentCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="896d7-110">**INapSystemHealthAgentCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="896d7-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="896d7-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="896d7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="896d7-112">Methods</span></span>

<span data-ttu-id="896d7-113">L'interfaccia **INapSystemHealthAgentCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="896d7-113">The **INapSystemHealthAgentCallback** interface has these methods.</span></span>



| <span data-ttu-id="896d7-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="896d7-114">Method</span></span>                                                                                                                                           | <span data-ttu-id="896d7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="896d7-115">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="896d7-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span><span class="sxs-lookup"><span data-stu-id="896d7-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span></span>](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | <span data-ttu-id="896d7-117">Usato dall'SHA per confrontare invieranno.</span><span class="sxs-lookup"><span data-stu-id="896d7-117">Used by the SHA to compare the SoHs.</span></span><br/>                                                                      |
| [<span data-ttu-id="896d7-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="896d7-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span></span>](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | <span data-ttu-id="896d7-119">Chiamato da NapAgent per determinare lo stato dell'SHA.</span><span class="sxs-lookup"><span data-stu-id="896d7-119">Called by the NapAgent to determine the state of the SHA.</span></span><br/>                                                 |
| [<span data-ttu-id="896d7-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="896d7-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span></span>](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | <span data-ttu-id="896d7-121">Chiamato da NapAgent per eseguire una query sulla richiesta di rapporto di integrità SHA.</span><span class="sxs-lookup"><span data-stu-id="896d7-121">Called by the NapAgent to query the SHA's SoH request.</span></span><br/>                                                    |
| [<span data-ttu-id="896d7-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="896d7-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span></span>](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | <span data-ttu-id="896d7-123">Chiamato se è stata eseguita una query sul rapporto di integrità dall'SHA, ma la risposta non è mai stata restituita.</span><span class="sxs-lookup"><span data-stu-id="896d7-123">Called if an SoH request was queried from the SHA, but the response never came back.</span></span><br/>                      |
| [<span data-ttu-id="896d7-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span><span class="sxs-lookup"><span data-stu-id="896d7-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span></span>](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | <span data-ttu-id="896d7-125">Chiamato da NapAgent per indicare che è stato modificato lo stato di isolamento del sistema o l'ora di fine della prova.</span><span class="sxs-lookup"><span data-stu-id="896d7-125">Called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span><br/> |
| [<span data-ttu-id="896d7-126">**INapSystemHealthAgentCallback::P rocessSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="896d7-126">**INapSystemHealthAgentCallback::ProcessSoHResponse**</span></span>](inapsystemhealthagentcallback-processsohresponse-method.md)                             | <span data-ttu-id="896d7-127">Chiamato quando NapAgent riceve una risposta a rapporto di integrità destinata a questo agente integrità.</span><span class="sxs-lookup"><span data-stu-id="896d7-127">Called when the NapAgent receives an SoH response destined for this health agent.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="896d7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="896d7-128">Requirements</span></span>



| <span data-ttu-id="896d7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="896d7-129">Requirement</span></span> | <span data-ttu-id="896d7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="896d7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="896d7-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="896d7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="896d7-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="896d7-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="896d7-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="896d7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="896d7-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="896d7-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="896d7-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="896d7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="896d7-136"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="896d7-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="896d7-137">IDL</span><span class="sxs-lookup"><span data-stu-id="896d7-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="896d7-138"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="896d7-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="896d7-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="896d7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="896d7-140">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="896d7-140">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="896d7-141">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="896d7-141">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

