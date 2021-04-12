---
title: Metodo INapSystemHealthAgentCallback NotifyOrphanedSoHRequest (NapSystemHealthAgent. h)
description: Viene chiamato se un SoHRequest è stato sottoposto a query dall'SHA, ma la risposta non è mai stata restituita.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- NAP metodo NotifyOrphanedSoHRequest
- Metodo NotifyOrphanedSoHRequest NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo NotifyOrphanedSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400890"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a><span data-ttu-id="ab715-106">Metodo INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest</span><span class="sxs-lookup"><span data-stu-id="ab715-106">INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="ab715-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="ab715-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ab715-108">Il metodo **INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest** viene chiamato se un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è stato sottoposto a query dall'SHA, ma la risposta non è mai stata restituita.</span><span class="sxs-lookup"><span data-stu-id="ab715-108">The **INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest** method is called if an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was queried from the SHA, but the response never came back.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab715-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab715-109">Syntax</span></span>


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="ab715-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab715-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab715-111">ID correlazione  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab715-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab715-112">Puntatore alla struttura univoca [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) che identifica il [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)orfano.</span><span class="sxs-lookup"><span data-stu-id="ab715-112">A pointer to the unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies the orphaned [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab715-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab715-113">Return value</span></span>

<span data-ttu-id="ab715-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ab715-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ab715-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ab715-115">Return code</span></span>                                                                          | <span data-ttu-id="ab715-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab715-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="ab715-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ab715-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ab715-118">Indica l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ab715-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ab715-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab715-119">Remarks</span></span>

<span data-ttu-id="ab715-120">Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.</span><span class="sxs-lookup"><span data-stu-id="ab715-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="ab715-121">Questo metodo può essere chiamato dal sistema nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab715-121">This method can be called by the system in the following cases:</span></span>

-   <span data-ttu-id="ab715-122">Non è stato possibile inviare un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) in rete.</span><span class="sxs-lookup"><span data-stu-id="ab715-122">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) could not be sent on the wire.</span></span>
-   <span data-ttu-id="ab715-123">Un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è stato inviato in rete, ma non è stato restituito alcun **SoHResponse** , ovvero si è verificato il timeout dell'applicazione o non è presente alcun servizio di convalida dell'integrità corrispondente sul lato server.</span><span class="sxs-lookup"><span data-stu-id="ab715-123">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was sent on the wire, but no **SoHResponse** came back, i.e. the enforcer timed out or there was no corresponding SHV on the server-side.</span></span>
-   <span data-ttu-id="ab715-124">La connessione è stata interrotta o un Enforcer è andato offline.</span><span class="sxs-lookup"><span data-stu-id="ab715-124">The connection went down or an enforcer went offline.</span></span>

<span data-ttu-id="ab715-125">Si tratta solo di una notifica di massimo sforzo, quindi SHAs non deve basarsi su queste informazioni per pulire lo stato.</span><span class="sxs-lookup"><span data-stu-id="ab715-125">This is only a best effort notification, so SHAs must not rely on this information to clean up state.</span></span> <span data-ttu-id="ab715-126">Esistono diverse situazioni in cui un SHA non riceve alcuna notifica:</span><span class="sxs-lookup"><span data-stu-id="ab715-126">There are several situations in which an SHA will not be notified:</span></span>

-   <span data-ttu-id="ab715-127">Se un Enforcer si comporta in modo improprio, ovvero non invia una notifica all'SHA quando lo stato della connessione non è attivo.</span><span class="sxs-lookup"><span data-stu-id="ab715-127">If an enforcer misbehaves, i.e. it does not notify the SHA when the connection state is down.</span></span>
-   <span data-ttu-id="ab715-128">Se un'applicazione si arresta in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="ab715-128">If an enforcer crashes.</span></span>
-   <span data-ttu-id="ab715-129">In condizioni di errore, ad esempio, il NapAgent ha esaurito la memoria.</span><span class="sxs-lookup"><span data-stu-id="ab715-129">In error conditions, i.e. the NapAgent is out of memory.</span></span>

<span data-ttu-id="ab715-130">SHAs può ricevere alcune notifiche non corrette quando vengono prima associate al NapAgent, ad esempio se è in corso uno scambio di rapporto di integrità quando si verifica un binding SHA e si verifica il timeout.</span><span class="sxs-lookup"><span data-stu-id="ab715-130">SHAs may get some spurious notifications when they first bind to the NapAgent, for instance, if an SoH exchange is in progress when the SHA bound, and then it times out.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab715-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab715-131">Requirements</span></span>



| <span data-ttu-id="ab715-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab715-132">Requirement</span></span> | <span data-ttu-id="ab715-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ab715-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab715-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab715-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ab715-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab715-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ab715-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab715-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ab715-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab715-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ab715-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab715-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab715-139"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab715-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab715-140">IDL</span><span class="sxs-lookup"><span data-stu-id="ab715-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab715-141"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab715-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab715-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab715-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab715-143">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="ab715-143">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





