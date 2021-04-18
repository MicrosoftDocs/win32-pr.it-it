---
description: Il \_ messaggio di riga AGENTSTATUSEX viene inviato quando lo stato di un agente ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta. Questo messaggio viene generato tramite la funzione lineProxyMessage.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: Messaggio di LINE_AGENTSTATUSEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331034"
---
# <a name="line_agentstatusex-message"></a><span data-ttu-id="cd658-104">\_Messaggio linea AGENTSTATUSEX</span><span class="sxs-lookup"><span data-stu-id="cd658-104">LINE\_AGENTSTATUSEX message</span></span>

<span data-ttu-id="cd658-105">Il messaggio di **riga \_ AGENTSTATUSEX** viene inviato quando lo stato di un agente ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta.</span><span class="sxs-lookup"><span data-stu-id="cd658-105">The **LINE\_AGENTSTATUSEX** message is sent when the status of an ACD agent changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="cd658-106">Questo messaggio viene generato tramite la funzione [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="cd658-106">This message is generated using [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="cd658-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd658-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd658-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="cd658-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="cd658-109">Handle dell'applicazione per il dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="cd658-109">The application's handle to the line device.</span></span> <span data-ttu-id="cd658-110">Questo si riferisce al gestore agenti.</span><span class="sxs-lookup"><span data-stu-id="cd658-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="cd658-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="cd658-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="cd658-112">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="cd658-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="cd658-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="cd658-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="cd658-114">Handle dell'agente il cui stato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="cd658-114">The handle of the agent whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="cd658-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="cd658-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="cd658-116">Specifica lo stato della coda che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="cd658-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="cd658-117">Può essere una o più delle [**\_ costanti LINEQUEUESTATUS**](linequeuestatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="cd658-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd658-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="cd658-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="cd658-119">Se *dwParam2* include il \_ bit di stato LINEAGENTSTATUSEX, *dwParam3* indica il nuovo valore dello stato dell'agente, che corrisponde a una [**delle \_ costanti LINEAGENTSTATEEX**](lineagentstateex--constants.md).</span><span class="sxs-lookup"><span data-stu-id="cd658-119">If *dwParam2* includes the LINEAGENTSTATUSEX \_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="cd658-120">In caso contrario, *dwParam3* è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="cd658-120">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd658-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd658-121">Requirements</span></span>



| <span data-ttu-id="cd658-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd658-122">Requirement</span></span> | <span data-ttu-id="cd658-123">Valore</span><span class="sxs-lookup"><span data-stu-id="cd658-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cd658-124">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="cd658-124">TAPI version</span></span><br/> | <span data-ttu-id="cd658-125">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="cd658-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="cd658-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd658-126">Header</span></span><br/>       | <dl> <span data-ttu-id="cd658-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd658-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd658-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd658-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd658-129">**lineGetAgentInfo**</span><span class="sxs-lookup"><span data-stu-id="cd658-129">**lineGetAgentInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[<span data-ttu-id="cd658-130">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="cd658-130">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




