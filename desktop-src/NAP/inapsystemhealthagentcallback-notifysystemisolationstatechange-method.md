---
title: Metodo INapSystemHealthAgentCallback NotifySystemIsolationStateChange (NapSystemHealthAgent. h)
description: Viene chiamato da NapAgent per indicare che lo stato di isolamento del sistema o l'ora di fine della prova è stato modificato.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- NAP metodo NotifySystemIsolationStateChange
- Metodo NotifySystemIsolationStateChange NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo NotifySystemIsolationStateChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741954"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a><span data-ttu-id="71f8d-106">Metodo INapSystemHealthAgentCallback:: NotifySystemIsolationStateChange</span><span class="sxs-lookup"><span data-stu-id="71f8d-106">INapSystemHealthAgentCallback::NotifySystemIsolationStateChange method</span></span>

> [!Note]  
> <span data-ttu-id="71f8d-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="71f8d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="71f8d-108">Il metodo **INapSystemHealthAgentCallback:: NotifySystemIsolationStateChange** viene chiamato da napagent per indicare che è stato modificato lo stato di isolamento del sistema o l'ora di fine della prova.</span><span class="sxs-lookup"><span data-stu-id="71f8d-108">The **INapSystemHealthAgentCallback::NotifySystemIsolationStateChange** method is called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f8d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71f8d-109">Syntax</span></span>


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a><span data-ttu-id="71f8d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="71f8d-110">Parameters</span></span>

<span data-ttu-id="71f8d-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="71f8d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71f8d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71f8d-112">Return value</span></span>

<span data-ttu-id="71f8d-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="71f8d-113">This method can return one of these values.</span></span>



| <span data-ttu-id="71f8d-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="71f8d-114">Return code</span></span>                                                                          | <span data-ttu-id="71f8d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71f8d-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="71f8d-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71f8d-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="71f8d-117">Indica l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="71f8d-117">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="71f8d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="71f8d-118">Remarks</span></span>

<span data-ttu-id="71f8d-119">Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.</span><span class="sxs-lookup"><span data-stu-id="71f8d-119">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="71f8d-120">L'agente di integrità può eseguire una query sullo stato di protezione accesso alla rete del sistema utilizzando [**INapSystemHealthAgentBinding:: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="71f8d-120">The health agent can query the system NAP state using the [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71f8d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71f8d-121">Requirements</span></span>



| <span data-ttu-id="71f8d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="71f8d-122">Requirement</span></span> | <span data-ttu-id="71f8d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="71f8d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f8d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71f8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="71f8d-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71f8d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="71f8d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71f8d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="71f8d-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71f8d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="71f8d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71f8d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="71f8d-129"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="71f8d-129"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="71f8d-130">IDL</span><span class="sxs-lookup"><span data-stu-id="71f8d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71f8d-131"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71f8d-131"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71f8d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71f8d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f8d-133">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="71f8d-133">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





