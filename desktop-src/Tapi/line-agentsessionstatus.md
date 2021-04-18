---
description: Il messaggio di riga \_ AGENTSESSIONSTATUS viene inviato quando lo stato di una sessione dell'agente ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta. Questo messaggio viene generato tramite la funzione lineProxyMessage.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: Messaggio di LINE_AGENTSESSIONSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331043"
---
# <a name="line_agentsessionstatus-message"></a><span data-ttu-id="69f71-104">\_Messaggio linea AGENTSESSIONSTATUS</span><span class="sxs-lookup"><span data-stu-id="69f71-104">LINE\_AGENTSESSIONSTATUS message</span></span>

<span data-ttu-id="69f71-105">Il messaggio di **riga \_ AGENTSESSIONSTATUS** viene inviato quando lo stato di una sessione dell'agente ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta.</span><span class="sxs-lookup"><span data-stu-id="69f71-105">The **LINE\_AGENTSESSIONSTATUS** message is sent when the status of an ACD agent session changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="69f71-106">Questo messaggio viene generato tramite la funzione [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="69f71-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="69f71-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="69f71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69f71-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="69f71-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="69f71-109">Handle dell'applicazione per il dispositivo della linea in cui è stato modificato lo stato della sessione dell'agente.</span><span class="sxs-lookup"><span data-stu-id="69f71-109">The application's handle to the line device on which the agent session status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="69f71-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="69f71-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="69f71-111">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="69f71-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="69f71-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="69f71-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="69f71-113">Handle della sessione di Agent il cui stato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="69f71-113">A handle of the agent session whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="69f71-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="69f71-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="69f71-115">Specifica lo stato della sessione dell'agente che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="69f71-115">Specifies the agent session status that has changed.</span></span> <span data-ttu-id="69f71-116">Può essere una o più **righe \_ AGENTSESSIONSTATUS**.</span><span class="sxs-lookup"><span data-stu-id="69f71-116">Can be one or more of the **LINE\_AGENTSESSIONSTATUS**.</span></span>

</dd> <dt>

<span data-ttu-id="69f71-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="69f71-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="69f71-118">Se *dwParam2* include il \_ bit di stato LINEAGENTSTATUSEX, *dwParam3* indica il nuovo valore dello stato dell'agente, che corrisponde a una [**delle \_ costanti LINEAGENTSTATEEX**](lineagentstateex--constants.md).</span><span class="sxs-lookup"><span data-stu-id="69f71-118">If *dwParam2* includes the LINEAGENTSTATUSEX\_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="69f71-119">In caso contrario, *dwParam3* è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="69f71-119">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69f71-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69f71-120">Requirements</span></span>



| <span data-ttu-id="69f71-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="69f71-121">Requirement</span></span> | <span data-ttu-id="69f71-122">Valore</span><span class="sxs-lookup"><span data-stu-id="69f71-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="69f71-123">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="69f71-123">TAPI version</span></span><br/> | <span data-ttu-id="69f71-124">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="69f71-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="69f71-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69f71-125">Header</span></span><br/>       | <dl> <span data-ttu-id="69f71-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="69f71-126"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69f71-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69f71-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f71-128">**lineGetAgentSessionInfo**</span><span class="sxs-lookup"><span data-stu-id="69f71-128">**lineGetAgentSessionInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[<span data-ttu-id="69f71-129">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="69f71-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




