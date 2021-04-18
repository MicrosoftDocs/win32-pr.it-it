---
description: Queste costanti vengono utilizzate in due contesti.
ms.assetid: 5c05a567-cc65-411e-b049-919a442c5c57
title: Costanti LINEPROXYREQUEST_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba34a3a7f7b1f41f0c32783c4132afcfafef1aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331252"
---
# <a name="lineproxyrequest_-constants"></a><span data-ttu-id="ef9ff-103">\_Costanti LINEPROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="ef9ff-103">LINEPROXYREQUEST\_ Constants</span></span>

<span data-ttu-id="ef9ff-104">Queste costanti vengono utilizzate in due contesti.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-104">These constants are used in two contexts.</span></span> <span data-ttu-id="ef9ff-105">In primo luogo, possono essere usati in una matrice di valori **DWORD** nella struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passata con [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) quando \_ viene specificata l'opzione proxy LINEOPENOPTION per indicare le funzioni che l'applicazione è disposti a gestire.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-105">First, they can be used in an array of **DWORD** values in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) when the LINEOPENOPTION\_PROXY option is specified, to indicate which functions the application is willing to handle.</span></span> <span data-ttu-id="ef9ff-106">In secondo luogo, vengono usati nella [**riga \_ PROXYREQUEST**](line-proxyrequest.md) passata all'applicazione Handler da un messaggio di **riga \_ PROXYREQUEST** per indicare il tipo di richiesta da elaborare e il formato dei dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-106">Second, they are used in the [**LINE\_PROXYREQUEST**](line-proxyrequest.md) passed to the handler application by a **LINE\_PROXYREQUEST** message to indicate the type of request that is to be processed and the format of the data in the buffer.</span></span>

<dl> <dt>

<span data-ttu-id="ef9ff-107"><span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**\_AGENTSPECIFIC LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-107"><span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**LINEPROXYREQUEST\_AGENTSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-108">Associato a [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-108">Associated with [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-109"><span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**\_CREATEAGENT LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-109"><span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**LINEPROXYREQUEST\_CREATEAGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-110">Associato a [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-110">Associated with [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-111"><span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**\_CREATEAGENTSESSION LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-111"><span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**LINEPROXYREQUEST\_CREATEAGENTSESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-112">Associato a [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-112">Associated with [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-113"><span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**\_GETAGENTACTIVITYLIST LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-113"><span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**LINEPROXYREQUEST\_GETAGENTACTIVITYLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-114">Associato a [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-114">Associated with [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-115"><span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**\_GETAGENTCAPS LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-115"><span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**LINEPROXYREQUEST\_GETAGENTCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-116">Associato a [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-116">Associated with [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-117"><span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**\_GETAGENTGROUPLIST LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-117"><span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**LINEPROXYREQUEST\_GETAGENTGROUPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-118">Associato a [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-118">Associated with [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-119"><span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**\_GETAGENTINFO LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-119"><span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**LINEPROXYREQUEST\_GETAGENTINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-120">Associato a [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-120">Associated with [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-121"><span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**\_GETAGENTSESSIONINFO LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-121"><span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**LINEPROXYREQUEST\_GETAGENTSESSIONINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-122">Associato a [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-122">Associated with [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-123"><span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**\_GETAGENTSESSIONLIST LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-123"><span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**LINEPROXYREQUEST\_GETAGENTSESSIONLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-124">Associato a [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-124">Associated with [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-125"><span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**\_GETAGENTSTATUS LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-125"><span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**LINEPROXYREQUEST\_GETAGENTSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-126">Associato a [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-126">Associated with [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-127"><span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST \_ GETgrouping**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-127"><span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST\_GETGROUPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-128">Associato a [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-128">Associated with [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-129"><span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**\_GETQUEUEINFO LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-129"><span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**LINEPROXYREQUEST\_GETQUEUEINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-130">Associato a [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-130">Associated with [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-131"><span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST \_ GETqueuein**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-131"><span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST\_GETQUEUELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-132">Associato a [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-132">Associated with [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-133"><span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**\_SETAGENTACTIVITY LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-133"><span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**LINEPROXYREQUEST\_SETAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-134">Associato a [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-134">Associated with [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-135"><span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**\_SETAGENTGROUP LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-135"><span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**LINEPROXYREQUEST\_SETAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-136">Associato a [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-136">Associated with [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-137"><span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**\_SETAGENTMEASUREMENTPERIOD LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-137"><span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-138">Associato a [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-138">Associated with [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-139"><span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**\_SETAGENTSESSIONSTATE LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-139"><span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**LINEPROXYREQUEST\_SETAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-140">Associato a [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-140">Associated with [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-141"><span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**\_SETAGENTSTATE LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-141"><span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**LINEPROXYREQUEST\_SETAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-142">Associato a [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-142">Associated with [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-143"><span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**\_SETAGENTSTATEEX LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-143"><span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**LINEPROXYREQUEST\_SETAGENTSTATEEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-144">Associato a [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-144">Associated with [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ef9ff-145"><span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**\_SETQUEUEMEASUREMENTPERIOD LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-145"><span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ef9ff-146">Associato a [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-146">Associated with [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef9ff-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef9ff-147">Requirements</span></span>



| <span data-ttu-id="ef9ff-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef9ff-148">Requirement</span></span> | <span data-ttu-id="ef9ff-149">Valore</span><span class="sxs-lookup"><span data-stu-id="ef9ff-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ef9ff-150">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="ef9ff-150">TAPI version</span></span><br/> | <span data-ttu-id="ef9ff-151">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ef9ff-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ef9ff-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef9ff-152">Header</span></span><br/>       | <dl> <span data-ttu-id="ef9ff-153"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef9ff-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef9ff-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef9ff-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef9ff-155">Costanti Call Center</span><span class="sxs-lookup"><span data-stu-id="ef9ff-155">Call Center Constants</span></span>](call-center-constants.md)
</dt> <dt>

[<span data-ttu-id="ef9ff-156">Funzioni Call Center</span><span class="sxs-lookup"><span data-stu-id="ef9ff-156">Call Center Functions</span></span>](call-center-functions.md)
</dt> </dl>

 

 




