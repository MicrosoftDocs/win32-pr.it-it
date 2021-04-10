---
description: Questa sezione contiene un elenco alfabetico delle funzioni del dispositivo line disponibili nella telefonia SPI.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: Funzioni della periferica di linea TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea2ca54096ac89b76a4658129362e87d4281fcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882330"
---
# <a name="tspi-line-device-functions"></a><span data-ttu-id="36cb2-103">Funzioni della periferica di linea TSPI</span><span class="sxs-lookup"><span data-stu-id="36cb2-103">TSPI Line Device Functions</span></span>

<span data-ttu-id="36cb2-104">Questa sezione contiene un elenco alfabetico delle funzioni del dispositivo line disponibili nella telefonia SPI.</span><span class="sxs-lookup"><span data-stu-id="36cb2-104">This section contains an alphabetic list of the available line device functions in the Telephony SPI.</span></span> <span data-ttu-id="36cb2-105">Le informazioni per ogni funzione includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="36cb2-105">The information for each function includes the following:</span></span>

-   <span data-ttu-id="36cb2-106">Istruzione dello scopo della funzione.</span><span class="sxs-lookup"><span data-stu-id="36cb2-106">A statement of the function's purpose.</span></span>
-   <span data-ttu-id="36cb2-107">Sintassi corretta per la funzione.</span><span class="sxs-lookup"><span data-stu-id="36cb2-107">The correct syntax for the function.</span></span>
-   <span data-ttu-id="36cb2-108">Descrizione dei parametri della funzione, inclusi gli Stati di chiamata validi.</span><span class="sxs-lookup"><span data-stu-id="36cb2-108">A description of the function's parameters, including valid call states.</span></span>
-   <span data-ttu-id="36cb2-109">Descrizione del valore restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="36cb2-109">A description of the function's return value.</span></span>
-   <span data-ttu-id="36cb2-110">Una sezione note che può includere uno o tutti gli elementi seguenti: un elenco degli Stati di chiamata validi all'immissione della funzione e le transizioni tipiche dello stato di chiamata al completamento della richiesta. Descrizione dei membri delle strutture di dati di grandi dimensioni che devono essere compilati dal provider di servizi e di quali membri devono essere conservati intatti. e confronto con una funzione corrispondente all'interno di TAPI.</span><span class="sxs-lookup"><span data-stu-id="36cb2-110">A Remarks section that can include any or all of the following: a list of the valid call states on entry of the function and typical call state transitions when the request completes; a description of which members of large data structures must be filled in by the service provider and which members must have their values preserved intact; and comparison with a corresponding function within TAPI.</span></span>
-   <span data-ttu-id="36cb2-111">Riferimenti ad altre funzioni, messaggi o strutture di dati.</span><span class="sxs-lookup"><span data-stu-id="36cb2-111">References to other functions, messages, or data structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="36cb2-112">Gli Stati effettivi in cui è possibile eseguire una funzione possono essere limitati dalle funzionalità del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="36cb2-112">The actual states in which a function can be performed may be limited by the capabilities of the service provider.</span></span> <span data-ttu-id="36cb2-113">I provider di servizi devono impostare il membro **dwCallFeatures** nella struttura [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus) , il membro **dwAddressFeatures** nella struttura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) e il membro **dwLineFeatures** nella struttura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) per indicare alle applicazioni se una funzione è consentita o meno in quel momento.</span><span class="sxs-lookup"><span data-stu-id="36cb2-113">Service providers must set the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure to indicate to applications whether or not a function is permitted at that point in time.</span></span>

     

<span data-ttu-id="36cb2-114">Questa sezione contiene le funzioni del dispositivo line TSPI seguenti:</span><span class="sxs-lookup"><span data-stu-id="36cb2-114">This section contains the following TSPI line device functions:</span></span>

-   [<span data-ttu-id="36cb2-115">**\_LINEACCEPT TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-115">**TSPI\_lineAccept**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [<span data-ttu-id="36cb2-116">**\_LINEADDTOCONFERENCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-116">**TSPI\_lineAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [<span data-ttu-id="36cb2-117">**\_LINEANSWER TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-117">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [<span data-ttu-id="36cb2-118">**\_LINEBLINDTRANSFER TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-118">**TSPI\_lineBlindTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [<span data-ttu-id="36cb2-119">**\_LINECLOSE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-119">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [<span data-ttu-id="36cb2-120">**\_LINECLOSECALL TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-120">**TSPI\_lineCloseCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [<span data-ttu-id="36cb2-121">**\_LINECLOSEMSPINSTANCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-121">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="36cb2-122">**\_LINECOMPLETECALL TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-122">**TSPI\_lineCompleteCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [<span data-ttu-id="36cb2-123">**\_LINECOMPLETETRANSFER TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-123">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="36cb2-124">**\_LINECONDITIONALMEDIADETECTION TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-124">**TSPI\_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [<span data-ttu-id="36cb2-125">**\_LINECONFIGDIALOG TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-125">**TSPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [<span data-ttu-id="36cb2-126">**\_LINECONFIGDIALOGEDIT TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-126">**TSPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [<span data-ttu-id="36cb2-127">**\_LINECREATEMSPINSTANCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-127">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="36cb2-128">**\_LINEDEVSPECIFIC TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-128">**TSPI\_lineDevSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [<span data-ttu-id="36cb2-129">**\_LINEDEVSPECIFICFEATURE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-129">**TSPI\_lineDevSpecificFeature**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [<span data-ttu-id="36cb2-130">**\_LINEDIAL TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-130">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [<span data-ttu-id="36cb2-131">**\_LINEDROP TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-131">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [<span data-ttu-id="36cb2-132">\_LINEDROPNOOWNER TSPI</span><span class="sxs-lookup"><span data-stu-id="36cb2-132">TSPI\_lineDropNoOwner</span></span>](tspi-linedropnoowner.md)
-   [<span data-ttu-id="36cb2-133">\_LINEDROPONCLOSE TSPI</span><span class="sxs-lookup"><span data-stu-id="36cb2-133">TSPI\_lineDropOnClose</span></span>](tspi-linedroponclose.md)
-   [<span data-ttu-id="36cb2-134">**\_LINEFORWARD TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-134">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="36cb2-135">**\_LINEGATHERDIGITS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-135">**TSPI\_lineGatherDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [<span data-ttu-id="36cb2-136">**\_LINEGENERATEDIGITS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-136">**TSPI\_lineGenerateDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [<span data-ttu-id="36cb2-137">**\_LINEGENERATETONE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-137">**TSPI\_lineGenerateTone**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [<span data-ttu-id="36cb2-138">**\_LINEGETADDRESSCAPS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-138">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [<span data-ttu-id="36cb2-139">**\_LINEGETADDRESSID TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-139">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [<span data-ttu-id="36cb2-140">**\_LINEGETADDRESSSTATUS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-140">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [<span data-ttu-id="36cb2-141">**\_LINEGETCALLADDRESSID TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-141">**TSPI\_lineGetCallAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [<span data-ttu-id="36cb2-142">**\_LINEGETCALLHUBTRACKING TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-142">**TSPI\_lineGetCallHubTracking**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [<span data-ttu-id="36cb2-143">**\_LINEGETCALLIDS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-143">**TSPI\_lineGetCallIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [<span data-ttu-id="36cb2-144">**\_LINEGETCALLINFO TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-144">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [<span data-ttu-id="36cb2-145">**\_LINEGETCALLSTATUS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-145">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [<span data-ttu-id="36cb2-146">**\_LINEGETDEVCAPS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [<span data-ttu-id="36cb2-147">**\_LINEGETDEVCONFIG TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-147">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [<span data-ttu-id="36cb2-148">**\_LINEGETEXTENSIONID TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-148">**TSPI\_lineGetExtensionID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [<span data-ttu-id="36cb2-149">**\_LINEGETICON TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-149">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [<span data-ttu-id="36cb2-150">**\_LINEGETID TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-150">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="36cb2-151">**\_LINEGETLINEDEVSTATUS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-151">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [<span data-ttu-id="36cb2-152">**\_LINEGETNUMADDRESSIDS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-152">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [<span data-ttu-id="36cb2-153">**\_LINEHOLD TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-153">**TSPI\_lineHold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [<span data-ttu-id="36cb2-154">**\_LINEMAKECALL TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-154">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="36cb2-155">**\_LINEMONITORDIGITS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-155">**TSPI\_lineMonitorDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [<span data-ttu-id="36cb2-156">**\_LINEMONITORMEDIA TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-156">**TSPI\_lineMonitorMedia**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [<span data-ttu-id="36cb2-157">**\_LINEMONITORTONES TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-157">**TSPI\_lineMonitorTones**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [<span data-ttu-id="36cb2-158">**\_LINEMSPIDENTIFY TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-158">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="36cb2-159">**\_LINENEGOTIATEEXTVERSION TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-159">**TSPI\_lineNegotiateExtVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [<span data-ttu-id="36cb2-160">**\_LINENEGOTIATETSPIVERSION TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-160">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [<span data-ttu-id="36cb2-161">**\_LINEOPEN TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-161">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [<span data-ttu-id="36cb2-162">**\_LINEPARK TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-162">**TSPI\_linePark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [<span data-ttu-id="36cb2-163">**\_LINEPICKUP TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-163">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="36cb2-164">**\_LINEPREPAREADDTOCONFERENCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-164">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="36cb2-165">**\_LINERECEIVEMSPDATA TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-165">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="36cb2-166">**\_LINEREDIRECT TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-166">**TSPI\_lineRedirect**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [<span data-ttu-id="36cb2-167">**\_LINERELEASEUSERUSERINFO TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-167">**TSPI\_lineReleaseUserUserInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [<span data-ttu-id="36cb2-168">**\_LINEREMOVEFROMCONFERENCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-168">**TSPI\_lineRemoveFromConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [<span data-ttu-id="36cb2-169">**\_LINESECURECALL TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-169">**TSPI\_lineSecureCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [<span data-ttu-id="36cb2-170">**\_LINESELECTEXTVERSION TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-170">**TSPI\_lineSelectExtVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [<span data-ttu-id="36cb2-171">**\_LINESENDUSERUSERINFO TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-171">**TSPI\_lineSendUserUserInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [<span data-ttu-id="36cb2-172">**\_LINESETAPPSPECIFIC TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-172">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [<span data-ttu-id="36cb2-173">**\_LINESETCALLDATA TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-173">**TSPI\_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="36cb2-174">**\_LINESETCALLHUBTRACKING TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-174">**TSPI\_lineSetCallHubTracking**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [<span data-ttu-id="36cb2-175">**\_LINESETCALLPARAMS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-175">**TSPI\_lineSetCallParams**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [<span data-ttu-id="36cb2-176">**\_LINESETCALLQUALITYOFSERVICE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-176">**TSPI\_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="36cb2-177">**\_LINESETCALLTREATMENT TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-177">**TSPI\_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="36cb2-178">\_LINESETCURRENTLOCATION TSPI</span><span class="sxs-lookup"><span data-stu-id="36cb2-178">TSPI\_lineSetCurrentLocation</span></span>](tspi-linesetcurrentlocation.md)
-   [<span data-ttu-id="36cb2-179">**\_LINESETDEFAULTMEDIADETECTION TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-179">**TSPI\_lineSetDefaultMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [<span data-ttu-id="36cb2-180">**\_LINESETDEVCONFIG TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-180">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [<span data-ttu-id="36cb2-181">**\_LINESETLINEDEVSTATUS TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-181">**TSPI\_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="36cb2-182">**\_LINESETMEDIACONTROL TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-182">**TSPI\_lineSetMediaControl**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [<span data-ttu-id="36cb2-183">**\_LINESETMEDIAMODE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-183">**TSPI\_lineSetMediaMode**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [<span data-ttu-id="36cb2-184">**\_LINESETSTATUSMESSAGES TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-184">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [<span data-ttu-id="36cb2-185">**\_LINESETTERMINAL TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-185">**TSPI\_lineSetTerminal**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [<span data-ttu-id="36cb2-186">**\_LINESETUPCONFERENCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-186">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="36cb2-187">**\_LINESETUPTRANSFER TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-187">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="36cb2-188">**\_LINESWAPHOLD TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-188">**TSPI\_lineSwapHold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [<span data-ttu-id="36cb2-189">**\_LINEUNCOMPLETECALL TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-189">**TSPI\_lineUncompleteCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [<span data-ttu-id="36cb2-190">**\_LINEUNHOLD TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-190">**TSPI\_lineUnhold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [<span data-ttu-id="36cb2-191">**\_LINEUNPARK TSPI**</span><span class="sxs-lookup"><span data-stu-id="36cb2-191">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
