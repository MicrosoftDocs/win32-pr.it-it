---
description: Il messaggio di riga \_ PROXYSTATUS viene inviato quando i proxy disponibili cambiano in una riga attualmente aperta dall'applicazione.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: Messaggio di LINE_PROXYSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328424"
---
# <a name="line_proxystatus-message"></a><span data-ttu-id="b72e5-103">\_Messaggio linea PROXYSTATUS</span><span class="sxs-lookup"><span data-stu-id="b72e5-103">LINE\_PROXYSTATUS message</span></span>

<span data-ttu-id="b72e5-104">Il messaggio di **riga \_ PROXYSTATUS** viene inviato quando i proxy disponibili cambiano in una riga attualmente aperta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b72e5-104">The **LINE\_PROXYSTATUS** message is sent when the available proxies change on a line that the application currently has open.</span></span>

<span data-ttu-id="b72e5-105">TAPISRV genera questo messaggio durante una funzione [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) usando LINEPROXYSTATUS \_ Open e LINEPROXYSTATUS \_ ALLOPENFORACD o una funzione [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) usando LINEPROXYSTATUS \_ Close (tutte le [**\_ costanti LINEPROXYSTATUS**](lineproxystatus--constants.md)).</span><span class="sxs-lookup"><span data-stu-id="b72e5-105">TAPISRV generates this message during a [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) function using LINEPROXYSTATUS\_OPEN and LINEPROXYSTATUS\_ALLOPENFORACD or a [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) function using LINEPROXYSTATUS\_CLOSE (all [**LINEPROXYSTATUS\_ Constants**](lineproxystatus--constants.md)).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b72e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b72e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b72e5-107">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="b72e5-107">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b72e5-108">Handle dell'applicazione per il dispositivo linea.</span><span class="sxs-lookup"><span data-stu-id="b72e5-108">The application's handle to the line device.</span></span> <span data-ttu-id="b72e5-109">Questo si riferisce al gestore agenti.</span><span class="sxs-lookup"><span data-stu-id="b72e5-109">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="b72e5-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="b72e5-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b72e5-111">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="b72e5-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="b72e5-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b72e5-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b72e5-113">Specifica lo stato della coda che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="b72e5-113">Specifies the queue status that has changed.</span></span> <span data-ttu-id="b72e5-114">Può essere una o più delle [**\_ costanti LINEPROXYSTATUS**](lineproxystatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b72e5-114">Can be one or more of the [**LINEPROXYSTATUS\_ constants**](lineproxystatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b72e5-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b72e5-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b72e5-116">Se *dwParam1* è impostato su LINEPROXYSTATUS \_ Open o LINEPROXYSTATUS \_ Close, *dwParam2* indica il tipo di richiesta proxy correlato, che è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="b72e5-116">If *dwParam1* is set to LINEPROXYSTATUS\_OPEN or LINEPROXYSTATUS\_CLOSE, *dwParam2* indicates the related proxy request type, which is one of the following:</span></span>

-   <span data-ttu-id="b72e5-117">\_SETAGENTGROUP LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-117">LINEPROXYREQUEST\_SETAGENTGROUP</span></span>
-   <span data-ttu-id="b72e5-118">\_SETAGENTSTATE LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-118">LINEPROXYREQUEST\_SETAGENTSTATE</span></span>
-   <span data-ttu-id="b72e5-119">\_SETAGENTACTIVITY LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-119">LINEPROXYREQUEST\_SETAGENTACTIVITY</span></span>
-   <span data-ttu-id="b72e5-120">\_GETAGENTCAPS LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-120">LINEPROXYREQUEST\_GETAGENTCAPS</span></span>
-   <span data-ttu-id="b72e5-121">\_GETAGENTSTATUS LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-121">LINEPROXYREQUEST\_GETAGENTSTATUS</span></span>
-   <span data-ttu-id="b72e5-122">\_AGENTSPECIFIC LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-122">LINEPROXYREQUEST\_AGENTSPECIFIC</span></span>
-   <span data-ttu-id="b72e5-123">\_GETAGENTACTIVITYLIST LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-123">LINEPROXYREQUEST\_GETAGENTACTIVITYLIST</span></span>
-   <span data-ttu-id="b72e5-124">\_GETAGENTGROUPLIST LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-124">LINEPROXYREQUEST\_GETAGENTGROUPLIST</span></span>
-   <span data-ttu-id="b72e5-125">\_CREATEAGENT LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-125">LINEPROXYREQUEST\_CREATEAGENT</span></span>
-   <span data-ttu-id="b72e5-126">\_SETAGENTMEASUREMENTPERIOD LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-126">LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="b72e5-127">\_GETAGENTINFO LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-127">LINEPROXYREQUEST\_GETAGENTINFO</span></span>
-   <span data-ttu-id="b72e5-128">\_CREATEAGENTSESSION LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-128">LINEPROXYREQUEST\_CREATEAGENTSESSION</span></span>
-   <span data-ttu-id="b72e5-129">\_GETAGENTSESSIONLIST LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-129">LINEPROXYREQUEST\_GETAGENTSESSIONLIST</span></span>
-   <span data-ttu-id="b72e5-130">\_SETAGENTSESSIONSTATE LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-130">LINEPROXYREQUEST\_SETAGENTSESSIONSTATE</span></span>
-   <span data-ttu-id="b72e5-131">\_GETAGENTSESSIONINFO LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-131">LINEPROXYREQUEST\_GETAGENTSESSIONINFO</span></span>
-   <span data-ttu-id="b72e5-132">LINEPROXYREQUEST \_ GETqueuein</span><span class="sxs-lookup"><span data-stu-id="b72e5-132">LINEPROXYREQUEST\_GETQUEUELIST</span></span>
-   <span data-ttu-id="b72e5-133">\_SETQUEUEMEASUREMENTPERIOD LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-133">LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="b72e5-134">\_GETQUEUEINFO LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-134">LINEPROXYREQUEST\_GETQUEUEINFO</span></span>
-   <span data-ttu-id="b72e5-135">LINEPROXYREQUEST \_ GETgrouping</span><span class="sxs-lookup"><span data-stu-id="b72e5-135">LINEPROXYREQUEST\_GETGROUPLIST</span></span>
-   <span data-ttu-id="b72e5-136">\_SETAGENTSTATEEX LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="b72e5-136">LINEPROXYREQUEST\_SETAGENTSTATEEX</span></span>

<span data-ttu-id="b72e5-137">In caso contrario, *dwParam2* è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="b72e5-137">Otherwise, *dwParam2* is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b72e5-138">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b72e5-138">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b72e5-139">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b72e5-139">Reserved.</span></span> <span data-ttu-id="b72e5-140">Imposta su zero.</span><span class="sxs-lookup"><span data-stu-id="b72e5-140">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b72e5-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b72e5-141">Requirements</span></span>



| <span data-ttu-id="b72e5-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b72e5-142">Requirement</span></span> | <span data-ttu-id="b72e5-143">Valore</span><span class="sxs-lookup"><span data-stu-id="b72e5-143">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b72e5-144">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="b72e5-144">TAPI version</span></span><br/> | <span data-ttu-id="b72e5-145">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="b72e5-145">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="b72e5-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b72e5-146">Header</span></span><br/>       | <dl> <span data-ttu-id="b72e5-147"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b72e5-147"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b72e5-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b72e5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72e5-149">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="b72e5-149">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="b72e5-150">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="b72e5-150">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="b72e5-151">**LINEA \_ PROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="b72e5-151">**LINE\_PROXYREQUEST**</span></span>](line-proxyrequest.md)
</dt> <dt>

[<span data-ttu-id="b72e5-152">**\_Costanti LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="b72e5-152">**LINEPROXYREQUEST\_ Constants**</span></span>](lineproxyrequest--constants.md)
</dt> </dl>

 

 




