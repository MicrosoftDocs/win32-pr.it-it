---
title: Funzioni di gestione
description: Di seguito sono riportate le funzioni di gestione di Windows Filtering Platform (WFP) per il motore di filtro.
ms.assetid: 983eb1bb-af6b-42cf-8148-ed3a0e3102a9
keywords:
- Funzioni di gestione API della piattaforma filtro Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab42fc22d6e51e85a1e03f4835ee510917ff534
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299806"
---
# <a name="management-functions"></a><span data-ttu-id="59b54-104">Funzioni di gestione</span><span class="sxs-lookup"><span data-stu-id="59b54-104">Management Functions</span></span>

<span data-ttu-id="59b54-105">Di seguito sono riportate le funzioni di gestione di Windows Filtering Platform (WFP) per il motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="59b54-105">The Windows Filtering Platform (WFP) management functions for the filter engine are as follows.</span></span>

<span data-ttu-id="59b54-106">Gestione dei callout</span><span class="sxs-lookup"><span data-stu-id="59b54-106">Callout Management</span></span>

-   [<span data-ttu-id="59b54-107">**\_Modifica CALLOUT \_ FWPM \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="59b54-107">**FWPM\_CALLOUT\_CHANGE\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_callout_change_callback0)
-   [<span data-ttu-id="59b54-108">**FwpmCalloutAdd0**</span><span class="sxs-lookup"><span data-stu-id="59b54-108">**FwpmCalloutAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutadd0)
-   [<span data-ttu-id="59b54-109">**FwpmCalloutCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-109">**FwpmCalloutCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0)
-   [<span data-ttu-id="59b54-110">**FwpmCalloutDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="59b54-110">**FwpmCalloutDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutdeletebyid0)
-   [<span data-ttu-id="59b54-111">**FwpmCalloutDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-111">**FwpmCalloutDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutdeletebykey0)
-   [<span data-ttu-id="59b54-112">**FwpmCalloutDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-112">**FwpmCalloutDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutdestroyenumhandle0)
-   [<span data-ttu-id="59b54-113">**FwpmCalloutEnum0**</span><span class="sxs-lookup"><span data-stu-id="59b54-113">**FwpmCalloutEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutenum0)
-   [<span data-ttu-id="59b54-114">**FwpmCalloutGetById0**</span><span class="sxs-lookup"><span data-stu-id="59b54-114">**FwpmCalloutGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0)
-   [<span data-ttu-id="59b54-115">**FwpmCalloutGetByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-115">**FwpmCalloutGetByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0)
-   [<span data-ttu-id="59b54-116">**FwpmCalloutGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-116">**FwpmCalloutGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-117">**FwpmCalloutSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-117">**FwpmCalloutSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-118">**FwpmCalloutSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="59b54-118">**FwpmCalloutSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)
-   [<span data-ttu-id="59b54-119">**FwpmCalloutSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="59b54-119">**FwpmCalloutSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)
-   [<span data-ttu-id="59b54-120">**FwpmCalloutUnsubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="59b54-120">**FwpmCalloutUnsubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)

<span data-ttu-id="59b54-121">Gestione degli oggetti di connessione</span><span class="sxs-lookup"><span data-stu-id="59b54-121">Connection Object Management</span></span>

-   [<span data-ttu-id="59b54-122">**\_Connessione FWPM \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="59b54-122">**FWPM\_CONNECTION\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_connection_callback0)
-   [<span data-ttu-id="59b54-123">**FwpmConnectionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-123">**FwpmConnectionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [<span data-ttu-id="59b54-124">**FwpmConnectionDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-124">**FwpmConnectionDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [<span data-ttu-id="59b54-125">**FwpmConnectionEnum0**</span><span class="sxs-lookup"><span data-stu-id="59b54-125">**FwpmConnectionEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [<span data-ttu-id="59b54-126">**FwpmConnectionGetById0**</span><span class="sxs-lookup"><span data-stu-id="59b54-126">**FwpmConnectionGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [<span data-ttu-id="59b54-127">**FwpmConnectionGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="59b54-127">**FwpmConnectionGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [<span data-ttu-id="59b54-128">**FwpmConnectionSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="59b54-128">**FwpmConnectionSetSecurityInfo0**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [<span data-ttu-id="59b54-129">**FwpmConnectionSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="59b54-129">**FwpmConnectionSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [<span data-ttu-id="59b54-130">**FwpmConnectionSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="59b54-130">**FwpmConnectionSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [<span data-ttu-id="59b54-131">**FwpmConnectionUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="59b54-131">**FwpmConnectionUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)

<span data-ttu-id="59b54-132">Gestione degli eventi</span><span class="sxs-lookup"><span data-stu-id="59b54-132">Event Management</span></span>

-   <span data-ttu-id="59b54-133">\_ \_ callback evento NET FWPM \_ :</span><span class="sxs-lookup"><span data-stu-id="59b54-133">FWPM\_NET\_EVENT\_CALLBACK:</span></span>
    -   <span data-ttu-id="59b54-134">[**FWPM \_ \_ \_ CALLBACK0 evento NET**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_net_event_callback0) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="59b54-134">[**FWPM\_NET\_EVENT\_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_net_event_callback0) (Windows 7)</span></span>
    -   <span data-ttu-id="59b54-135">[**FWPM \_ NET \_ Event \_ CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="59b54-135">[**FWPM\_NET\_EVENT\_CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1) (Windows 8)</span></span>
-   [<span data-ttu-id="59b54-136">**FwpmNetEventCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-136">**FwpmNetEventCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)
-   [<span data-ttu-id="59b54-137">**FwpmNetEventDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-137">**FwpmNetEventDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventdestroyenumhandle0)
-   <span data-ttu-id="59b54-138">FwpmNetEventEnum:</span><span class="sxs-lookup"><span data-stu-id="59b54-138">FwpmNetEventEnum:</span></span>
    -   <span data-ttu-id="59b54-139">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="59b54-139">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="59b54-140">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="59b54-140">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) (Windows 7)</span></span>
    -   <span data-ttu-id="59b54-141">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="59b54-141">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) (Windows 8)</span></span>
-   [<span data-ttu-id="59b54-142">**FwpmNetEventsGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="59b54-142">**FwpmNetEventsGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventsgetsecurityinfo0)
-   [<span data-ttu-id="59b54-143">**FwpmNetEventsSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="59b54-143">**FwpmNetEventsSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventssetsecurityinfo0)
-   <span data-ttu-id="59b54-144">FwpmNetEventsSubscribe:</span><span class="sxs-lookup"><span data-stu-id="59b54-144">FwpmNetEventsSubscribe:</span></span>
    -   <span data-ttu-id="59b54-145">[**FwpmNetEventSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventsubscribe0) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="59b54-145">[**FwpmNetEventSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventsubscribe0) (Windows 7)</span></span>
    -   <span data-ttu-id="59b54-146">[**FwpmNetEventSubscribe1**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="59b54-146">[**FwpmNetEventSubscribe1**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1) (Windows 8)</span></span>
-   [<span data-ttu-id="59b54-147">**FwpmNetEventSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="59b54-147">**FwpmNetEventSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventsubscriptionsget0)
-   [<span data-ttu-id="59b54-148">**FwpmNetEventUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="59b54-148">**FwpmNetEventUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventunsubscribe0)

<span data-ttu-id="59b54-149">Gestione dei filtri</span><span class="sxs-lookup"><span data-stu-id="59b54-149">Filter Management</span></span>

-   [<span data-ttu-id="59b54-150">**\_Modifica filtro \_ FWPM \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="59b54-150">**FWPM\_FILTER\_CHANGE\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_filter_change_callback0)
-   [<span data-ttu-id="59b54-151">**FwpmFilterAdd0**</span><span class="sxs-lookup"><span data-stu-id="59b54-151">**FwpmFilterAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)
-   [<span data-ttu-id="59b54-152">**FwpmFilterCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-152">**FwpmFilterCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)
-   [<span data-ttu-id="59b54-153">**FwpmFilterDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="59b54-153">**FwpmFilterDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)
-   [<span data-ttu-id="59b54-154">**FwpmFilterDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-154">**FwpmFilterDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)
-   [<span data-ttu-id="59b54-155">**FwpmFilterDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-155">**FwpmFilterDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdestroyenumhandle0)
-   [<span data-ttu-id="59b54-156">**FwpmFilterEnum0**</span><span class="sxs-lookup"><span data-stu-id="59b54-156">**FwpmFilterEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterenum0)
-   [<span data-ttu-id="59b54-157">**FwpmFilterGetById0**</span><span class="sxs-lookup"><span data-stu-id="59b54-157">**FwpmFilterGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)
-   [<span data-ttu-id="59b54-158">**FwpmFilterGetByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-158">**FwpmFilterGetByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)
-   [<span data-ttu-id="59b54-159">**FwpmFilterGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-159">**FwpmFilterGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-160">**FwpmFilterSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-160">**FwpmFilterSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-161">**FwpmFilterSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="59b54-161">**FwpmFilterSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)
-   [<span data-ttu-id="59b54-162">**FwpmFilterSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="59b54-162">**FwpmFilterSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)
-   [<span data-ttu-id="59b54-163">**FwpmFilterUnsubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="59b54-163">**FwpmFilterUnsubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterunsubscribechanges0)
-   [<span data-ttu-id="59b54-164">**FwpmGetAppIdFromFileName0**</span><span class="sxs-lookup"><span data-stu-id="59b54-164">**FwpmGetAppIdFromFileName0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0)

<span data-ttu-id="59b54-165">Gestione dei livelli</span><span class="sxs-lookup"><span data-stu-id="59b54-165">Layer Management</span></span>

-   [<span data-ttu-id="59b54-166">**FwpmLayerCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-166">**FwpmLayerCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmlayercreateenumhandle0)
-   [<span data-ttu-id="59b54-167">**FwpmLayerDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-167">**FwpmLayerDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmlayerdestroyenumhandle0)
-   [<span data-ttu-id="59b54-168">**FwpmLayerEnum0**</span><span class="sxs-lookup"><span data-stu-id="59b54-168">**FwpmLayerEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmlayerenum0)
-   [<span data-ttu-id="59b54-169">**FwpmLayerGetById0**</span><span class="sxs-lookup"><span data-stu-id="59b54-169">**FwpmLayerGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmlayergetbyid0)
-   [<span data-ttu-id="59b54-170">**FwpmLayerGetByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-170">**FwpmLayerGetByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmlayergetbykey0)
-   [<span data-ttu-id="59b54-171">**FwpmLayerGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-171">**FwpmLayerGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmlayergetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-172">**FwpmLayerSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-172">**FwpmLayerSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmlayersetsecurityinfobykey0)

<span data-ttu-id="59b54-173">Gestione del contesto del provider</span><span class="sxs-lookup"><span data-stu-id="59b54-173">Provider Context Management</span></span>

-   [<span data-ttu-id="59b54-174">**\_Modifica del contesto del provider FWPM \_ \_ \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="59b54-174">**FWPM\_PROVIDER\_CONTEXT\_CHANGE\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_provider_context_change_callback0)
-   <span data-ttu-id="59b54-175">FwpmProviderContextAdd:</span><span class="sxs-lookup"><span data-stu-id="59b54-175">FwpmProviderContextAdd:</span></span>
    -   <span data-ttu-id="59b54-176">[**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="59b54-176">[**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0) (Windows Vista)</span></span>
    -   <span data-ttu-id="59b54-177">[**FwpmProviderContextAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="59b54-177">[**FwpmProviderContextAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd1) (Windows 7)</span></span>
    -   <span data-ttu-id="59b54-178">[**FwpmProviderContextAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="59b54-178">[**FwpmProviderContextAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2) (Windows 8)</span></span>
-   [<span data-ttu-id="59b54-179">**FwpmProviderContextCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-179">**FwpmProviderContextCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0)
-   [<span data-ttu-id="59b54-180">**FwpmProviderContextDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="59b54-180">**FwpmProviderContextDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebyid0)
-   [<span data-ttu-id="59b54-181">**FwpmProviderContextDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-181">**FwpmProviderContextDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebykey0)
-   [<span data-ttu-id="59b54-182">**FwpmProviderContextDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-182">**FwpmProviderContextDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdestroyenumhandle0)
-   <span data-ttu-id="59b54-183">FwpmProviderContextEnum:</span><span class="sxs-lookup"><span data-stu-id="59b54-183">FwpmProviderContextEnum:</span></span>
    -   <span data-ttu-id="59b54-184">[**FwpmProviderContextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="59b54-184">[**FwpmProviderContextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="59b54-185">[**FwpmProviderContextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="59b54-185">[**FwpmProviderContextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum1) (Windows 7)</span></span>
    -   <span data-ttu-id="59b54-186">[**FwpmProviderContextEnum2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="59b54-186">[**FwpmProviderContextEnum2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2) (Windows 8)</span></span>
-   <span data-ttu-id="59b54-187">FwpmProviderContextGetById:</span><span class="sxs-lookup"><span data-stu-id="59b54-187">FwpmProviderContextGetById:</span></span>
    -   <span data-ttu-id="59b54-188">[**FwpmProviderContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="59b54-188">[**FwpmProviderContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="59b54-189">[**FwpmProviderContextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="59b54-189">[**FwpmProviderContextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid1) (Windows 7)</span></span>
    -   <span data-ttu-id="59b54-190">[**FwpmProviderContextGetById2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="59b54-190">[**FwpmProviderContextGetById2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2) (Windows 8)</span></span>
-   <span data-ttu-id="59b54-191">FwpmProviderContextGetByKey:</span><span class="sxs-lookup"><span data-stu-id="59b54-191">FwpmProviderContextGetByKey:</span></span>
    -   <span data-ttu-id="59b54-192">[**FwpmProviderContextGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="59b54-192">[**FwpmProviderContextGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey0) (Windows Vista)</span></span>
    -   <span data-ttu-id="59b54-193">[**FwpmProviderContextGetByKey1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="59b54-193">[**FwpmProviderContextGetByKey1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey1) (Windows 7)</span></span>
    -   <span data-ttu-id="59b54-194">[**FwpmProviderContextGetByKey2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="59b54-194">[**FwpmProviderContextGetByKey2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2) (Windows 8)</span></span>
-   [<span data-ttu-id="59b54-195">**FwpmProviderContextGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-195">**FwpmProviderContextGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-196">**FwpmProviderContextSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-196">**FwpmProviderContextSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-197">**FwpmProviderContextSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="59b54-197">**FwpmProviderContextSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0)
-   [<span data-ttu-id="59b54-198">**FwpmProviderContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="59b54-198">**FwpmProviderContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscriptionsget0)
-   [<span data-ttu-id="59b54-199">**FwpmProviderContextUnsubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="59b54-199">**FwpmProviderContextUnsubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextunsubscribechanges0)

<span data-ttu-id="59b54-200">Gestione provider</span><span class="sxs-lookup"><span data-stu-id="59b54-200">Provider Management</span></span>

-   [<span data-ttu-id="59b54-201">**\_Modifica del provider FWPM \_ \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="59b54-201">**FWPM\_PROVIDER\_CHANGE\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_provider_change_callback0)
-   [<span data-ttu-id="59b54-202">**FwpmProviderAdd0**</span><span class="sxs-lookup"><span data-stu-id="59b54-202">**FwpmProviderAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovideradd0)
-   [<span data-ttu-id="59b54-203">**FwpmProviderCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-203">**FwpmProviderCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercreateenumhandle0)
-   [<span data-ttu-id="59b54-204">**FwpmProviderDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-204">**FwpmProviderDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmproviderdeletebykey0)
-   [<span data-ttu-id="59b54-205">**FwpmProviderDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-205">**FwpmProviderDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmproviderdestroyenumhandle0)
-   [<span data-ttu-id="59b54-206">**FwpmProviderEnum0**</span><span class="sxs-lookup"><span data-stu-id="59b54-206">**FwpmProviderEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmproviderenum0)
-   [<span data-ttu-id="59b54-207">**FwpmProviderGetByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-207">**FwpmProviderGetByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidergetbykey0)
-   [<span data-ttu-id="59b54-208">**FwpmProviderGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-208">**FwpmProviderGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidergetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-209">**FwpmProviderSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-209">**FwpmProviderSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-210">**FwpmProviderSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="59b54-210">**FwpmProviderSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0)
-   [<span data-ttu-id="59b54-211">**FwpmProviderSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="59b54-211">**FwpmProviderSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscriptionsget0)
-   [<span data-ttu-id="59b54-212">**FwpmProviderUnsubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="59b54-212">**FwpmProviderUnsubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmproviderunsubscribechanges0)

<span data-ttu-id="59b54-213">Gestione delle sessioni</span><span class="sxs-lookup"><span data-stu-id="59b54-213">Session Management</span></span>

-   [<span data-ttu-id="59b54-214">**FwpmEngineClose0**</span><span class="sxs-lookup"><span data-stu-id="59b54-214">**FwpmEngineClose0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0)
-   [<span data-ttu-id="59b54-215">**FwpmEngineGetOption0**</span><span class="sxs-lookup"><span data-stu-id="59b54-215">**FwpmEngineGetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)
-   [<span data-ttu-id="59b54-216">**FwpmEngineGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="59b54-216">**FwpmEngineGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetsecurityinfo0)
-   [<span data-ttu-id="59b54-217">**FwpmEngineOpen0**</span><span class="sxs-lookup"><span data-stu-id="59b54-217">**FwpmEngineOpen0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)
-   [<span data-ttu-id="59b54-218">**FwpmEngineSetOption0**</span><span class="sxs-lookup"><span data-stu-id="59b54-218">**FwpmEngineSetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)
-   [<span data-ttu-id="59b54-219">**FwpmEngineSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="59b54-219">**FwpmEngineSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetsecurityinfo0)
-   [<span data-ttu-id="59b54-220">**FwpmSessionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-220">**FwpmSessionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)
-   [<span data-ttu-id="59b54-221">**FwpmSessionDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-221">**FwpmSessionDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessiondestroyenumhandle0)
-   [<span data-ttu-id="59b54-222">**FwpmSessionEnum0**</span><span class="sxs-lookup"><span data-stu-id="59b54-222">**FwpmSessionEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessionenum0)

<span data-ttu-id="59b54-223">Gestione del sottolivello</span><span class="sxs-lookup"><span data-stu-id="59b54-223">Sublayer Management</span></span>

-   [<span data-ttu-id="59b54-224">**\_Modifica del SOTTOLIVELLO FWPM \_ \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="59b54-224">**FWPM\_SUBLAYER\_CHANGE\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_sublayer_change_callback0)
-   [<span data-ttu-id="59b54-225">**FwpmSubLayerAdd0**</span><span class="sxs-lookup"><span data-stu-id="59b54-225">**FwpmSubLayerAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0)
-   [<span data-ttu-id="59b54-226">**FwpmSubLayerCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-226">**FwpmSubLayerCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayercreateenumhandle0)
-   [<span data-ttu-id="59b54-227">**FwpmSubLayerDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-227">**FwpmSubLayerDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayerdeletebykey0)
-   [<span data-ttu-id="59b54-228">**FwpmSubLayerDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="59b54-228">**FwpmSubLayerDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayerdestroyenumhandle0)
-   [<span data-ttu-id="59b54-229">**FwpmSubLayerEnum0**</span><span class="sxs-lookup"><span data-stu-id="59b54-229">**FwpmSubLayerEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayerenum0)
-   [<span data-ttu-id="59b54-230">**FwpmSubLayerGetByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-230">**FwpmSubLayerGetByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayergetbykey0)
-   [<span data-ttu-id="59b54-231">**FwpmSubLayerGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-231">**FwpmSubLayerGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayergetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-232">**FwpmSubLayerSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="59b54-232">**FwpmSubLayerSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayersetsecurityinfobykey0)
-   [<span data-ttu-id="59b54-233">**FwpmSubLayerSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="59b54-233">**FwpmSubLayerSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayersubscribechanges0)
-   [<span data-ttu-id="59b54-234">**FwpmSubLayerSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="59b54-234">**FwpmSubLayerSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayersubscriptionsget0)
-   [<span data-ttu-id="59b54-235">**FwpmSubLayerUnsubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="59b54-235">**FwpmSubLayerUnsubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayerunsubscribechanges0)

<span data-ttu-id="59b54-236">Gestione delle porte di sistema</span><span class="sxs-lookup"><span data-stu-id="59b54-236">System Ports Management</span></span>

-   [<span data-ttu-id="59b54-237">**\_Porte di sistema FWPM \_ \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="59b54-237">**FWPM\_SYSTEM\_PORTS\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_system_ports_callback0)
-   [<span data-ttu-id="59b54-238">**FwpmSystemPortsGet0**</span><span class="sxs-lookup"><span data-stu-id="59b54-238">**FwpmSystemPortsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsystemportsget0)
-   [<span data-ttu-id="59b54-239">**FwpmSystemPortsSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="59b54-239">**FwpmSystemPortsSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsystemportssubscribe0)
-   [<span data-ttu-id="59b54-240">**FwpmSystemPortsUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="59b54-240">**FwpmSystemPortsUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsystemportsunsubscribe0)

<span data-ttu-id="59b54-241">Gestione transazioni</span><span class="sxs-lookup"><span data-stu-id="59b54-241">Transaction Management</span></span>

-   [<span data-ttu-id="59b54-242">**FwpmTransactionAbort0**</span><span class="sxs-lookup"><span data-stu-id="59b54-242">**FwpmTransactionAbort0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0)
-   [<span data-ttu-id="59b54-243">**FwpmTransactionBegin0**</span><span class="sxs-lookup"><span data-stu-id="59b54-243">**FwpmTransactionBegin0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)
-   [<span data-ttu-id="59b54-244">**FwpmTransactionCommit0**</span><span class="sxs-lookup"><span data-stu-id="59b54-244">**FwpmTransactionCommit0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)

<span data-ttu-id="59b54-245">Gestione vSwitch</span><span class="sxs-lookup"><span data-stu-id="59b54-245">vSwitch Management</span></span>

-   [<span data-ttu-id="59b54-246">**FWPM \_ vswitch \_ evento \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="59b54-246">**FWPM\_VSWITCH\_EVENT\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_vswitch_event_callback0)
-   [<span data-ttu-id="59b54-247">**FwpmvSwitchEventsGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="59b54-247">**FwpmvSwitchEventsGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [<span data-ttu-id="59b54-248">**FwpmvSwitchEventsSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="59b54-248">**FwpmvSwitchEventsSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [<span data-ttu-id="59b54-249">**FwpmvSwitchEventSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="59b54-249">**FwpmvSwitchEventSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [<span data-ttu-id="59b54-250">**FwpmvSwitchEventUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="59b54-250">**FwpmvSwitchEventUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)

 

 