---
description: Le \_ costanti LINECALLFEATURE2 elencano le funzionalità aggiuntive disponibili per la conferenza, il trasferimento e le chiamate di parcheggio.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: Costanti LINECALLFEATURE2_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327883"
---
# <a name="linecallfeature2_-constants"></a><span data-ttu-id="73e10-103">\_Costanti LINECALLFEATURE2</span><span class="sxs-lookup"><span data-stu-id="73e10-103">LINECALLFEATURE2\_ Constants</span></span>

<span data-ttu-id="73e10-104">Le **costanti \_ LINECALLFEATURE2** elencano le funzionalità aggiuntive disponibili per la conferenza, il trasferimento e le chiamate di parcheggio.</span><span class="sxs-lookup"><span data-stu-id="73e10-104">The **LINECALLFEATURE2\_** constants list the supplemental features available for conferencing, transferring, and parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="73e10-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**\_COMPLCALLBACK LINECALLFEATURE2**</span><span class="sxs-lookup"><span data-stu-id="73e10-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2\_COMPLCALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73e10-106">Se questo bit è on, la funzionalità "callback" può essere richiamata usando l' \_ opzione di callback LINECOMPLMODE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="73e10-106">If this bit is on, the "callback" feature can be invoked by using the LINECOMPLMODE\_CALLBACK option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="73e10-107">Il \_ bit COMPLETECALL LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="73e10-107">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73e10-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**\_COMPLCAMPON LINECALLFEATURE2**</span><span class="sxs-lookup"><span data-stu-id="73e10-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2\_COMPLCAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73e10-109">Se questo bit è attivato, la funzionalità "Camp on" può essere richiamata usando l'opzione LINECOMPLMODE di \_ campo con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="73e10-109">If this bit is on, the "camp on" feature can be invoked by using the LINECOMPLMODE\_CAMPON option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="73e10-110">Il \_ bit COMPLETECALL LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="73e10-110">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73e10-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**\_COMPLINTRUDE LINECALLFEATURE2**</span><span class="sxs-lookup"><span data-stu-id="73e10-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2\_COMPLINTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73e10-112">Se questo bit è attivato, la funzionalità "intrusione" può essere richiamata usando l' \_ opzione LINECOMPLMODE Intruder con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="73e10-112">If this bit is on, the "intrude" feature can be invoked by using the LINECOMPLMODE\_INTRUDE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="73e10-113">Il \_ bit COMPLETECALL LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="73e10-113">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73e10-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**\_COMPLMESSAGE LINECALLFEATURE2**</span><span class="sxs-lookup"><span data-stu-id="73e10-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2\_COMPLMESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73e10-115">Se questo bit è attivato, la funzionalità "lascia messaggio" può essere richiamata usando l' \_ opzione del messaggio LINECOMPLMODE con [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="73e10-115">If this bit is on, the "leave message" feature can be invoked by using the LINECOMPLMODE\_MESSAGE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="73e10-116">Il \_ bit COMPLETECALL LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="73e10-116">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73e10-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**\_NOHOLDCONFERENCE LINECALLFEATURE2**</span><span class="sxs-lookup"><span data-stu-id="73e10-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73e10-118">Se questo bit è acceso, non è possibile creare una "conferenza di attesa" utilizzando l' \_ opzione LINECALLPARAMFLAGS NOHOLDCONFERENCE con [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference).</span><span class="sxs-lookup"><span data-stu-id="73e10-118">If this bit is on, a "no hold conference" can be created by using the LINECALLPARAMFLAGS\_NOHOLDCONFERENCE option with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference).</span></span> <span data-ttu-id="73e10-119">Il \_ bit SETUPCONF LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="73e10-119">The LINECALLFEATURE\_SETUPCONF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73e10-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**\_ONESTEPTRANSFER LINECALLFEATURE2**</span><span class="sxs-lookup"><span data-stu-id="73e10-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73e10-121">Se questo bit è on, è possibile creare il "trasferimento di un passaggio" utilizzando l' \_ opzione LINECALLPARAMFLAGS ONESTEPTRANSFER con [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span><span class="sxs-lookup"><span data-stu-id="73e10-121">If this bit is on, "one step transfer" can be created by using the LINECALLPARAMFLAGS\_ONESTEPTRANSFER option with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="73e10-122">Il \_ bit SETUPTRANSFER LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="73e10-122">The LINECALLFEATURE\_SETUPTRANSFER bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="73e10-123">Se nessuno dei bit "COMPl" viene specificato nel membro **dwCallFeatures2** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ma \_ viene specificato LINECALLFEATURE COMPLETECALL, è possibile che uno di essi funzionerà, ma il provider di servizi non ha specificato quale.</span><span class="sxs-lookup"><span data-stu-id="73e10-123">If none of the "COMPL" bits is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETECALL is specified, then it is possible that any of them will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="73e10-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**\_TRANSFERCONF LINECALLFEATURE2**</span><span class="sxs-lookup"><span data-stu-id="73e10-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2\_TRANSFERCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73e10-125">Se questo bit è on, la funzione [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) può essere usata per risolvere il trasferimento come conferenza a tre vie.</span><span class="sxs-lookup"><span data-stu-id="73e10-125">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a three-way conference.</span></span> <span data-ttu-id="73e10-126">Il \_ bit COMPLETETRANSF LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="73e10-126">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73e10-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**\_TRANSFERNORM LINECALLFEATURE2**</span><span class="sxs-lookup"><span data-stu-id="73e10-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2\_TRANSFERNORM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73e10-128">Se questo bit è on, la funzione [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) può essere usata per risolvere il trasferimento come trasferimento normale.</span><span class="sxs-lookup"><span data-stu-id="73e10-128">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a normal transfer.</span></span> <span data-ttu-id="73e10-129">Il \_ bit COMPLETETRANSF LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="73e10-129">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="73e10-130">Se non si specifica né TRANSFERNORM né TRANSFERCONF nel membro **dwCallFeatures2** di [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ma \_ viene specificato LINECALLFEATURE COMPLETETRANSF, è possibile che sia funzionante, ma che il provider di servizi non abbia specificato quale.</span><span class="sxs-lookup"><span data-stu-id="73e10-130">If neither TRANSFERNORM nor TRANSFERCONF is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETETRANSF is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="73e10-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**\_PARKDIRECT LINECALLFEATURE2**</span><span class="sxs-lookup"><span data-stu-id="73e10-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2\_PARKDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73e10-132">Se questo bit è attivato, è possibile richiamare la funzionalità "directed Park" utilizzando l' \_ opzione LINEPARKMODE directed con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span><span class="sxs-lookup"><span data-stu-id="73e10-132">If this bit is on, the "directed park" feature can be invoked by using the LINEPARKMODE\_DIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="73e10-133">Il \_ bit del parco LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="73e10-133">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="73e10-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**\_PARKNONDIRECT LINECALLFEATURE2**</span><span class="sxs-lookup"><span data-stu-id="73e10-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2\_PARKNONDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="73e10-135">Se questo bit è attivato, la funzionalità "parco non diretto" può essere richiamata usando l'opzione LINEPARKMODE non \_ indirizzata con [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span><span class="sxs-lookup"><span data-stu-id="73e10-135">If this bit is on, the "non-directed park" feature can be invoked by using the LINEPARKMODE\_NONDIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="73e10-136">Il \_ bit del parco LINECALLFEATURE sarà anche on nel membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="73e10-136">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="73e10-137">Se non viene specificato né PARKDIRECT né PARKNONDIRECT nel membro **dwCallFeatures2** di [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ma \_ è stato specificato LINECALLFEATURE Park, è possibile che sia funzionante, ma che il provider di servizi non abbia specificato quale.</span><span class="sxs-lookup"><span data-stu-id="73e10-137">If neither PARKDIRECT nor PARKNONDIRECT is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_PARK is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73e10-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73e10-138">Requirements</span></span>



| <span data-ttu-id="73e10-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="73e10-139">Requirement</span></span> | <span data-ttu-id="73e10-140">Valore</span><span class="sxs-lookup"><span data-stu-id="73e10-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="73e10-141">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="73e10-141">TAPI version</span></span><br/> | <span data-ttu-id="73e10-142">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="73e10-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="73e10-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73e10-143">Header</span></span><br/>       | <dl> <span data-ttu-id="73e10-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="73e10-144"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e10-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73e10-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e10-146">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="73e10-146">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="73e10-147">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="73e10-147">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="73e10-148">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="73e10-148">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="73e10-149">**linePark**</span><span class="sxs-lookup"><span data-stu-id="73e10-149">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[<span data-ttu-id="73e10-150">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="73e10-150">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="73e10-151">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="73e10-151">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




