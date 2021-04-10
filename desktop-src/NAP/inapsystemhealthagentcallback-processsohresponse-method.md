---
title: Metodo INapSystemHealthAgentCallback ProcessSoHResponse (NapSystemHealthAgent. h)
description: Viene chiamato quando NapAgent riceve un SoHResponse destinato a questo agente per l'integrità.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- NAP metodo ProcessSoHResponse
- Metodo ProcessSoHResponse NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964360"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a><span data-ttu-id="82f80-106">INapSystemHealthAgentCallback::P metodo rocessSoHResponse</span><span class="sxs-lookup"><span data-stu-id="82f80-106">INapSystemHealthAgentCallback::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="82f80-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="82f80-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="82f80-108">Il metodo **INapSystemHealthAgentCallback::P rocesssohresponse** viene chiamato quando napagent riceve un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinato a questo agente per l'integrità.</span><span class="sxs-lookup"><span data-stu-id="82f80-108">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method is called when the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f80-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82f80-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="82f80-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="82f80-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82f80-111">*richiesta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82f80-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f80-112">Puntatore COM a un oggetto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) che identifica l'oggetto Request.</span><span class="sxs-lookup"><span data-stu-id="82f80-112">A COM pointer to a [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82f80-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82f80-113">Return value</span></span>

<span data-ttu-id="82f80-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="82f80-114">This method can return one of these values.</span></span>



| <span data-ttu-id="82f80-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="82f80-115">Return code</span></span>                                                                                            | <span data-ttu-id="82f80-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82f80-116">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82f80-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="82f80-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="82f80-118">Indica l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="82f80-118">Indicates success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="82f80-119"><dt>**NAP \_ E \_ pacchetto non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82f80-119"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="82f80-120">Restituito da questa implementazione se la risposta non è nel formato corretto.</span><span class="sxs-lookup"><span data-stu-id="82f80-120">Returned by this implementation if the response is not in the correct format.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="82f80-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="82f80-121">Remarks</span></span>

<span data-ttu-id="82f80-122">Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.</span><span class="sxs-lookup"><span data-stu-id="82f80-122">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="82f80-123">Quando NapAgent riceve un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinato a questo agente per l'integrità, richiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="82f80-123">When the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent, it invokes this method.</span></span> <span data-ttu-id="82f80-124">L'agente di integrità deve eseguire una query su SoHResponse dall'oggetto Request.</span><span class="sxs-lookup"><span data-stu-id="82f80-124">The health agent must query the SoHResponse from the request object.</span></span> <span data-ttu-id="82f80-125">Al termine della chiamata, non devono essere presenti riferimenti all'oggetto Request.</span><span class="sxs-lookup"><span data-stu-id="82f80-125">It must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="82f80-126">Il metodo **INapSystemHealthAgentCallback::P rocesssohresponse** non deve essere bloccato.</span><span class="sxs-lookup"><span data-stu-id="82f80-126">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method must not block.</span></span> <span data-ttu-id="82f80-127">Se è necessaria un'elaborazione di correzione, qualsiasi implementazione di **ProcessSoHResponse** deve avviare un nuovo thread per eseguire l'elaborazione della correzione.</span><span class="sxs-lookup"><span data-stu-id="82f80-127">If any fix-up processing is required, any implementation of **ProcessSoHResponse** must start a new thread to perform fix-up processing.</span></span> <span data-ttu-id="82f80-128">NapAgent deve chiamare [**INapSystemHealthAgentCallBack:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) per determinare lo stato di correzione dell'SHA.</span><span class="sxs-lookup"><span data-stu-id="82f80-128">The NapAgent must call [**INapSystemHealthAgentCallBack::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) to determine the fix-up status of the SHA.</span></span>

<span data-ttu-id="82f80-129">Questo metodo deve restituire **un \_ \_ \_ pacchetto NAP E non valido** se la risposta non è nel formato corretto.</span><span class="sxs-lookup"><span data-stu-id="82f80-129">This method must return **NAP\_E\_INVALID\_PACKET** if the response is not in the correct format.</span></span>

## <a name="requirements"></a><span data-ttu-id="82f80-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82f80-130">Requirements</span></span>



| <span data-ttu-id="82f80-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="82f80-131">Requirement</span></span> | <span data-ttu-id="82f80-132">Valore</span><span class="sxs-lookup"><span data-stu-id="82f80-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82f80-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82f80-133">Minimum supported client</span></span><br/> | <span data-ttu-id="82f80-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82f80-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="82f80-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82f80-135">Minimum supported server</span></span><br/> | <span data-ttu-id="82f80-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82f80-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="82f80-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82f80-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="82f80-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="82f80-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="82f80-139">IDL</span><span class="sxs-lookup"><span data-stu-id="82f80-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82f80-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="82f80-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82f80-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82f80-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f80-142">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="82f80-142">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





