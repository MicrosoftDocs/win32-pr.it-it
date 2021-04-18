---
description: Il messaggio della linea TAPI \_ AGENTSPECIFIC viene inviato quando lo stato di un agente ACD viene modificato su una linea attualmente aperta dall'applicazione. L'applicazione può richiamare lineGetAgentStatus per determinare lo stato corrente dell'agente.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: Messaggio di LINE_AGENTSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331041"
---
# <a name="line_agentspecific-message"></a><span data-ttu-id="f987c-104">\_Messaggio linea AGENTSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="f987c-104">LINE\_AGENTSPECIFIC message</span></span>

<span data-ttu-id="f987c-105">Il messaggio della **linea TAPI \_ AGENTSPECIFIC** viene inviato quando lo stato di un agente ACD viene modificato su una linea attualmente aperta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f987c-105">The TAPI **LINE\_AGENTSPECIFIC** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="f987c-106">L'applicazione può richiamare [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) per determinare lo stato corrente dell'agente.</span><span class="sxs-lookup"><span data-stu-id="f987c-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f987c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f987c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f987c-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="f987c-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f987c-109">Handle dell'applicazione per il dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="f987c-109">The application's handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="f987c-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f987c-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f987c-111">Istanza di callback fornita all'apertura della riga della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f987c-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="f987c-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f987c-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f987c-113">Indice nella matrice di identificatori di estensione del gestore nella struttura [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) dell'estensione del gestore a cui è associato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="f987c-113">The index into the array of handler extension identifiers in the [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) structure of the handler extension with which the message is associated.</span></span>

</dd> <dt>

<span data-ttu-id="f987c-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f987c-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f987c-115">Specifico dell'estensione del gestore.</span><span class="sxs-lookup"><span data-stu-id="f987c-115">Specific to the handler extension.</span></span> <span data-ttu-id="f987c-116">In genere, questo valore viene usato per fare in modo che l'applicazione richiami una funzione [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) per recuperare ulteriori dettagli sul messaggio.</span><span class="sxs-lookup"><span data-stu-id="f987c-116">Generally, this value is used to cause the application to invoke a [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) function to fetch further details about the message.</span></span>

</dd> <dt>

<span data-ttu-id="f987c-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f987c-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f987c-118">Specifico dell'estensione del gestore.</span><span class="sxs-lookup"><span data-stu-id="f987c-118">Specific to the handler extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f987c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f987c-119">Return value</span></span>

<span data-ttu-id="f987c-120">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f987c-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f987c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f987c-121">Remarks</span></span>

<span data-ttu-id="f987c-122">Il messaggio di **riga \_ AGENTSPECIFIC** non viene inviato ad applicazioni che supportano le versioni precedenti di TAPI.</span><span class="sxs-lookup"><span data-stu-id="f987c-122">The **LINE\_AGENTSPECIFIC** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="f987c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f987c-123">Requirements</span></span>



| <span data-ttu-id="f987c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f987c-124">Requirement</span></span> | <span data-ttu-id="f987c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f987c-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f987c-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f987c-126">TAPI version</span></span><br/> | <span data-ttu-id="f987c-127">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f987c-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f987c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f987c-128">Header</span></span><br/>       | <dl> <span data-ttu-id="f987c-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f987c-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f987c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f987c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f987c-131">**LINEAGENTCAPS**</span><span class="sxs-lookup"><span data-stu-id="f987c-131">**LINEAGENTCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[<span data-ttu-id="f987c-132">**lineAgentSpecific**</span><span class="sxs-lookup"><span data-stu-id="f987c-132">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[<span data-ttu-id="f987c-133">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="f987c-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




