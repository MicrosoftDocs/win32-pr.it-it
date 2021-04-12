---
title: Interfaccia INapSystemHealthAgentRequest (NapSystemHealthAgent. h)
description: SHAs utilizzare per comunicare e coordinare l'elaborazione con il sistema NAP.
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- NAP interfaccia INapSystemHealthAgentRequest
- Interfaccia NAP di INapSystemHealthAgentRequest, descrizione
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517704"
---
# <a name="inapsystemhealthagentrequest-interface"></a><span data-ttu-id="3df17-105">Interfaccia INapSystemHealthAgentRequest</span><span class="sxs-lookup"><span data-stu-id="3df17-105">INapSystemHealthAgentRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="3df17-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="3df17-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3df17-107">L'interfaccia **INapSystemHealthAgentRequest** fornisce i metodi usati da Shas per comunicare e coordinare l'elaborazione con il sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="3df17-107">The **INapSystemHealthAgentRequest** interface provides methods that SHAs use to communicate and coordinate processing with the NAP system.</span></span>

## <a name="members"></a><span data-ttu-id="3df17-108">Membri</span><span class="sxs-lookup"><span data-stu-id="3df17-108">Members</span></span>

<span data-ttu-id="3df17-109">L'interfaccia **INapSystemHealthAgentRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3df17-109">The **INapSystemHealthAgentRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3df17-110">**INapSystemHealthAgentRequest** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3df17-110">**INapSystemHealthAgentRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="3df17-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="3df17-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3df17-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="3df17-112">Methods</span></span>

<span data-ttu-id="3df17-113">L'interfaccia **INapSystemHealthAgentRequest** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3df17-113">The **INapSystemHealthAgentRequest** interface has these methods.</span></span>



| <span data-ttu-id="3df17-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="3df17-114">Method</span></span>                                                                                                                     | <span data-ttu-id="3df17-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3df17-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3df17-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span><span class="sxs-lookup"><span data-stu-id="3df17-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span></span>](inapsystemhealthagentrequest-getcachesohflag-method.md)               | <span data-ttu-id="3df17-117">Utilizzato solo da NapAgent.</span><span class="sxs-lookup"><span data-stu-id="3df17-117">Used only by the NapAgent.</span></span><br/>                                                            |
| [<span data-ttu-id="3df17-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="3df17-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span></span>](inapsystemhealthagentrequest-getcorrelationid-method.md)             | <span data-ttu-id="3df17-119">Utilizzato dagli agenti di integrità del sistema per la correlazione di invieranno e [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="3df17-119">Used by system health agents to correlate SoHs and [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/> |
| [<span data-ttu-id="3df17-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="3df17-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span></span>](inapsystemhealthagentrequest-getsohrequest-method.md)                   | <span data-ttu-id="3df17-121">Usato da SHAs per ottenere invieranno precedentemente memorizzati nella cache da NapAgent.</span><span class="sxs-lookup"><span data-stu-id="3df17-121">Used by SHAs to get SoHs previously cached by the NapAgent.</span></span><br/>                           |
| [<span data-ttu-id="3df17-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="3df17-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span></span>](inapsystemhealthagentrequest-getsohresponse-method.md)                 | <span data-ttu-id="3df17-123">Utilizzato dall'agente per l'integrità per recuperare il [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="3df17-123">Used by the health agent to retrieve their [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/>         |
| [<span data-ttu-id="3df17-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="3df17-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span></span>](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | <span data-ttu-id="3df17-125">Utilizzato dagli agenti di integrità del sistema per registrare l'ID di correlazione.</span><span class="sxs-lookup"><span data-stu-id="3df17-125">Used by system health agents to log the correlation ID.</span></span><br/>                               |
| [<span data-ttu-id="3df17-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="3df17-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span></span>](inapsystemhealthagentrequest-setsohrequest-method.md)                   | <span data-ttu-id="3df17-127">Utilizzato dagli agenti di integrità per scrivere la richiesta di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="3df17-127">Used by health agents to write their SoH request.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="3df17-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3df17-128">Requirements</span></span>



| <span data-ttu-id="3df17-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3df17-129">Requirement</span></span> | <span data-ttu-id="3df17-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3df17-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df17-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3df17-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3df17-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3df17-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3df17-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3df17-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3df17-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3df17-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3df17-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3df17-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3df17-136"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="3df17-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="3df17-137">IDL</span><span class="sxs-lookup"><span data-stu-id="3df17-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3df17-138"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3df17-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="3df17-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3df17-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3df17-140"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df17-140"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="3df17-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3df17-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df17-142">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="3df17-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3df17-143">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="3df17-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

