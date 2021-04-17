---
title: Novità della piattaforma filtro Windows
description: Windows 8 e Windows Server 2012 introducono nuovi elementi di programmazione della piattaforma filtro Windows.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104339873"
---
# <a name="whats-new-in-windows-filtering-platform"></a><span data-ttu-id="50f95-103">Novità della piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="50f95-103">What's New in Windows Filtering Platform</span></span>

<span data-ttu-id="50f95-104">Windows 8 e Windows Server 2012 introducono nuovi elementi di programmazione della piattaforma filtro Windows.</span><span class="sxs-lookup"><span data-stu-id="50f95-104">Windows 8 and Windows Server 2012 introduce new Windows Filtering Platform programming elements.</span></span> <span data-ttu-id="50f95-105">Le nuove funzionalità includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="50f95-105">New functionality includes the following:</span></span>

-   <span data-ttu-id="50f95-106">*Filtro di livello 2*: fornisce l'accesso al livello L2 (Mac), consentendo il filtraggio del traffico a tale livello.</span><span class="sxs-lookup"><span data-stu-id="50f95-106">*Layer 2 filtering*: Provides access to the L2 (MAC) layer, allowing filtering of traffic at that layer.</span></span>
-   <span data-ttu-id="50f95-107">*filtro vswitch*: consente di controllare e/o modificare i pacchetti che attraversano un vswitch.</span><span class="sxs-lookup"><span data-stu-id="50f95-107">*vSwitch filtering*: Allows packets traversing a vSwitch to be inspected and/or modified.</span></span> <span data-ttu-id="50f95-108">I filtri o i callout di WFP possono essere usati in ingresso e in uscita vSwitch.</span><span class="sxs-lookup"><span data-stu-id="50f95-108">WFP filters or callouts can be used at the vSwitch ingress and egress.</span></span>
-   <span data-ttu-id="50f95-109">*Gestione dei contenitori di app*: consente l'accesso alle informazioni sui contenitori di app e sui problemi di connettività di isolamento rete.</span><span class="sxs-lookup"><span data-stu-id="50f95-109">*App container management*: Allows access to information about app containers and network isolation connectivity issues.</span></span>
-   <span data-ttu-id="50f95-110">*Aggiornamenti IPSec*: funzionalità IPSec estese, tra cui il monitoraggio dello stato della connessione, la selezione del certificato e la gestione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="50f95-110">*IPsec updates*: Extended IPsec functionality including connection state monitoring, certificate selection, and key management.</span></span>

<span data-ttu-id="50f95-111">Il kit driver di Windows include anche informazioni sulle [modifiche del WFP per Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).</span><span class="sxs-lookup"><span data-stu-id="50f95-111">The Windows Driver Kit also includes information on [WFP Changes for Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).</span></span>

## <a name="windows-8-api-updates"></a><span data-ttu-id="50f95-112">Aggiornamenti dell'API di Windows 8</span><span class="sxs-lookup"><span data-stu-id="50f95-112">Windows 8 API updates</span></span>

<span data-ttu-id="50f95-113">Sono state aggiunte molte nuove API per Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="50f95-113">Many new APIs have been added for Windows 8 and Windows Server 2012.</span></span>

## <a name="new-functions"></a><span data-ttu-id="50f95-114">Nuove funzioni</span><span class="sxs-lookup"><span data-stu-id="50f95-114">New functions</span></span>

-   [<span data-ttu-id="50f95-115">**\_Evento FWPM \_ net \_ CALLBACK1**</span><span class="sxs-lookup"><span data-stu-id="50f95-115">**FWPM\_NET\_EVENT\_CALLBACK1**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [<span data-ttu-id="50f95-116">**FwpmConnectionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="50f95-116">**FwpmConnectionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [<span data-ttu-id="50f95-117">**FwpmConnectionDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="50f95-117">**FwpmConnectionDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [<span data-ttu-id="50f95-118">**FwpmConnectionEnum0**</span><span class="sxs-lookup"><span data-stu-id="50f95-118">**FwpmConnectionEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [<span data-ttu-id="50f95-119">**FwpmConnectionGetById0**</span><span class="sxs-lookup"><span data-stu-id="50f95-119">**FwpmConnectionGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [<span data-ttu-id="50f95-120">**FwpmConnectionGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="50f95-120">**FwpmConnectionGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [<span data-ttu-id="50f95-121">**FwpmConnectionSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="50f95-121">**FwpmConnectionSetSecurityInfo0**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [<span data-ttu-id="50f95-122">**FwpmConnectionSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="50f95-122">**FwpmConnectionSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [<span data-ttu-id="50f95-123">**FwpmConnectionSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="50f95-123">**FwpmConnectionSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [<span data-ttu-id="50f95-124">**FwpmConnectionUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="50f95-124">**FwpmConnectionUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [<span data-ttu-id="50f95-125">**FwpmIPsecTunnelAdd2**</span><span class="sxs-lookup"><span data-stu-id="50f95-125">**FwpmIPsecTunnelAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [<span data-ttu-id="50f95-126">**FwpmNetEventEnum2**</span><span class="sxs-lookup"><span data-stu-id="50f95-126">**FwpmNetEventEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [<span data-ttu-id="50f95-127">**FwpmNetEventSubscribe1**</span><span class="sxs-lookup"><span data-stu-id="50f95-127">**FwpmNetEventSubscribe1**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [<span data-ttu-id="50f95-128">**FwpmProviderContextAdd2**</span><span class="sxs-lookup"><span data-stu-id="50f95-128">**FwpmProviderContextAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [<span data-ttu-id="50f95-129">**FwpmProviderContextEnum2**</span><span class="sxs-lookup"><span data-stu-id="50f95-129">**FwpmProviderContextEnum2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [<span data-ttu-id="50f95-130">**FwpmProviderContextGetById2**</span><span class="sxs-lookup"><span data-stu-id="50f95-130">**FwpmProviderContextGetById2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [<span data-ttu-id="50f95-131">**FwpmProviderContextGetByKey2**</span><span class="sxs-lookup"><span data-stu-id="50f95-131">**FwpmProviderContextGetByKey2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [<span data-ttu-id="50f95-132">**FwpmvSwitchEventsGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="50f95-132">**FwpmvSwitchEventsGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [<span data-ttu-id="50f95-133">**FwpmvSwitchEventsSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="50f95-133">**FwpmvSwitchEventsSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [<span data-ttu-id="50f95-134">**FwpmvSwitchEventSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="50f95-134">**FwpmvSwitchEventSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [<span data-ttu-id="50f95-135">**FwpmvSwitchEventUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="50f95-135">**FwpmvSwitchEventUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [<span data-ttu-id="50f95-136">**IkeextSaEnum2**</span><span class="sxs-lookup"><span data-stu-id="50f95-136">**IkeextSaEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [<span data-ttu-id="50f95-137">**IkeextSaGetById2**</span><span class="sxs-lookup"><span data-stu-id="50f95-137">**IkeextSaGetById2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [<span data-ttu-id="50f95-138">**CHECK0 chiave di \_ Gestione chiavi IPSec \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="50f95-138">**IPSEC\_KEY\_MANAGER\_KEY\_DICTATION\_CHECK0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [<span data-ttu-id="50f95-139">**Il \_ gestore delle chiavi IPSec \_ \_ impone \_ Key0**</span><span class="sxs-lookup"><span data-stu-id="50f95-139">**IPSEC\_KEY\_MANAGER\_DICTATE\_KEY0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [<span data-ttu-id="50f95-140">**\_ \_ \_ Notifica Key0 di gestione chiavi IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="50f95-140">**IPSEC\_KEY\_MANAGER\_NOTIFY\_KEY0**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [<span data-ttu-id="50f95-141">**\_ \_ CALLBACK0 contesto SA \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="50f95-141">**IPSEC\_SA\_CONTEXT\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [<span data-ttu-id="50f95-142">**IPsecKeyManagerAddAndRegister0**</span><span class="sxs-lookup"><span data-stu-id="50f95-142">**IPsecKeyManagerAddAndRegister0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [<span data-ttu-id="50f95-143">**IPsecKeyManagerGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="50f95-143">**IPsecKeyManagerGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [<span data-ttu-id="50f95-144">**IPsecKeyManagerSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="50f95-144">**IPsecKeyManagerSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [<span data-ttu-id="50f95-145">**IPsecKeyManagersGet0**</span><span class="sxs-lookup"><span data-stu-id="50f95-145">**IPsecKeyManagersGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [<span data-ttu-id="50f95-146">**IPsecKeyManagerUnregisterAndDelete0**</span><span class="sxs-lookup"><span data-stu-id="50f95-146">**IPsecKeyManagerUnregisterAndDelete0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [<span data-ttu-id="50f95-147">**IPsecSaContextSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="50f95-147">**IPsecSaContextSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [<span data-ttu-id="50f95-148">**IPsecSaContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="50f95-148">**IPsecSaContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [<span data-ttu-id="50f95-149">**IPsecSaContextUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="50f95-149">**IPsecSaContextUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [<span data-ttu-id="50f95-150">**NetworkIsolationDiagnoseConnectFailureAndGetInfo**</span><span class="sxs-lookup"><span data-stu-id="50f95-150">**NetworkIsolationDiagnoseConnectFailureAndGetInfo**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [<span data-ttu-id="50f95-151">**NetworkIsolationEnumAppContainers**</span><span class="sxs-lookup"><span data-stu-id="50f95-151">**NetworkIsolationEnumAppContainers**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [<span data-ttu-id="50f95-152">**NetworkIsolationEnumerateAppContainerRules**</span><span class="sxs-lookup"><span data-stu-id="50f95-152">**NetworkIsolationEnumerateAppContainerRules**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [<span data-ttu-id="50f95-153">**NetworkIsolationFreeAppContainers**</span><span class="sxs-lookup"><span data-stu-id="50f95-153">**NetworkIsolationFreeAppContainers**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [<span data-ttu-id="50f95-154">**NetworkIsolationGetAppContainerConfig**</span><span class="sxs-lookup"><span data-stu-id="50f95-154">**NetworkIsolationGetAppContainerConfig**</span></span>](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [<span data-ttu-id="50f95-155">**NetworkIsolationRegisterForAppContainerChanges**</span><span class="sxs-lookup"><span data-stu-id="50f95-155">**NetworkIsolationRegisterForAppContainerChanges**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [<span data-ttu-id="50f95-156">**NetworkIsolationSetAppContainerConfig**</span><span class="sxs-lookup"><span data-stu-id="50f95-156">**NetworkIsolationSetAppContainerConfig**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [<span data-ttu-id="50f95-157">**NetworkIsolationSetupAppContainerBinaries**</span><span class="sxs-lookup"><span data-stu-id="50f95-157">**NetworkIsolationSetupAppContainerBinaries**</span></span>](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [<span data-ttu-id="50f95-158">**PAC \_ modifiche \_ richiamate \_ FN**</span><span class="sxs-lookup"><span data-stu-id="50f95-158">**PAC\_CHANGES\_CALLBACK\_FN**</span></span>](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a><span data-ttu-id="50f95-159">Nuove strutture</span><span class="sxs-lookup"><span data-stu-id="50f95-159">New structures</span></span>

-   [<span data-ttu-id="50f95-160">**\_METHOD2 IKEEXT Authentication \_**</span><span class="sxs-lookup"><span data-stu-id="50f95-160">**IKEEXT\_AUTHENTICATION\_METHOD2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [<span data-ttu-id="50f95-161">**\_Certificato IKEEXT \_ EKUS0**</span><span class="sxs-lookup"><span data-stu-id="50f95-161">**IKEEXT\_CERT\_EKUS0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [<span data-ttu-id="50f95-162">**\_Certificato IKEEXT \_ NAME0**</span><span class="sxs-lookup"><span data-stu-id="50f95-162">**IKEEXT\_CERT\_NAME0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [<span data-ttu-id="50f95-163">**\_Accodare certificato \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="50f95-163">**IKEEXT\_CERTIFICATE\_AUTHENTICATION2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [<span data-ttu-id="50f95-164">**\_CRITERIA0 certificato \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="50f95-164">**IKEEXT\_CERTIFICATE\_CRITERIA0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [<span data-ttu-id="50f95-165">**IKEEXT \_ em \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="50f95-165">**IKEEXT\_EM\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [<span data-ttu-id="50f95-166">**\_AUTHENTICATION1 Kerberos \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="50f95-166">**IKEEXT\_KERBEROS\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [<span data-ttu-id="50f95-167">**\_POLICY2 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="50f95-167">**IKEEXT\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [<span data-ttu-id="50f95-168">**\_Chiave IPsec \_ MANAGER0**</span><span class="sxs-lookup"><span data-stu-id="50f95-168">**IPSEC\_KEY\_MANAGER0**</span></span>](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [<span data-ttu-id="50f95-169">**\_CALLBACKS0 di \_ gestione \_ chiavi IPSec**</span><span class="sxs-lookup"><span data-stu-id="50f95-169">**IPSEC\_KEY\_MANAGER\_CALLBACKS0**</span></span>](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [<span data-ttu-id="50f95-170">**\_POLICY1 di chiavi IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="50f95-170">**IPSEC\_KEYING\_POLICY1**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [<span data-ttu-id="50f95-171">**\_ \_ CHANGE0 contesto SA \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="50f95-171">**IPSEC\_SA\_CONTEXT\_CHANGE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [<span data-ttu-id="50f95-172">**\_ \_ SUBSCRIPTION0 contesto SA \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="50f95-172">**IPSEC\_SA\_CONTEXT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [<span data-ttu-id="50f95-173">**\_POLICY2 trasporto \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="50f95-173">**IPSEC\_TRANSPORT\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [<span data-ttu-id="50f95-174">**\_ENDPOINT0 tunnel \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="50f95-174">**IPSEC\_TUNNEL\_ENDPOINT0**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [<span data-ttu-id="50f95-175">**\_ENDPOINTS2 tunnel \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="50f95-175">**IPSEC\_TUNNEL\_ENDPOINTS2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [<span data-ttu-id="50f95-176">**\_POLICY2 tunnel \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="50f95-176">**IPSEC\_TUNNEL\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [<span data-ttu-id="50f95-177">**\_CONNECTION0 FWPM**</span><span class="sxs-lookup"><span data-stu-id="50f95-177">**FWPM\_CONNECTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [<span data-ttu-id="50f95-178">**\_ \_ TEMPLATE0 enum di connessione FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="50f95-178">**FWPM\_CONNECTION\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [<span data-ttu-id="50f95-179">**\_Connessione FWPM \_ SUBSCRIPTION0**</span><span class="sxs-lookup"><span data-stu-id="50f95-179">**FWPM\_CONNECTION\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [<span data-ttu-id="50f95-180">**FWPM \_ net \_ event2**</span><span class="sxs-lookup"><span data-stu-id="50f95-180">**FWPM\_NET\_EVENT2**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [<span data-ttu-id="50f95-181">**\_ \_ Funzionalità evento NET \_ FWPM \_ ALLOW0**</span><span class="sxs-lookup"><span data-stu-id="50f95-181">**FWPM\_NET\_EVENT\_CAPABILITY\_ALLOW0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [<span data-ttu-id="50f95-182">**\_ \_ Funzionalità evento NET \_ FWPM \_ DROP0**</span><span class="sxs-lookup"><span data-stu-id="50f95-182">**FWPM\_NET\_EVENT\_CAPABILITY\_DROP0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [<span data-ttu-id="50f95-183">**\_ \_ Classificazione evento FWPM \_ net \_ ALLOW0**</span><span class="sxs-lookup"><span data-stu-id="50f95-183">**FWPM\_NET\_EVENT\_CLASSIFY\_ALLOW0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [<span data-ttu-id="50f95-184">**\_ \_ Classificazione evento FWPM \_ net \_ DROP2**</span><span class="sxs-lookup"><span data-stu-id="50f95-184">**FWPM\_NET\_EVENT\_CLASSIFY\_DROP2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [<span data-ttu-id="50f95-185">**FWPM \_ net \_ Event \_ Classification \_ Drop \_ MAC0**</span><span class="sxs-lookup"><span data-stu-id="50f95-185">**FWPM\_NET\_EVENT\_CLASSIFY\_DROP\_MAC0**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [<span data-ttu-id="50f95-186">**\_Evento FWPM \_ net \_ HEADER2**</span><span class="sxs-lookup"><span data-stu-id="50f95-186">**FWPM\_NET\_EVENT\_HEADER2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [<span data-ttu-id="50f95-187">**\_Provider FWPM \_ CONTEXT2**</span><span class="sxs-lookup"><span data-stu-id="50f95-187">**FWPM\_PROVIDER\_CONTEXT2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [<span data-ttu-id="50f95-188">**FWPM \_ vswitch \_ EVENT0**</span><span class="sxs-lookup"><span data-stu-id="50f95-188">**FWPM\_VSWITCH\_EVENT0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [<span data-ttu-id="50f95-189">**FWPM \_ vswitch \_ evento \_ SUBSCRIPTION0**</span><span class="sxs-lookup"><span data-stu-id="50f95-189">**FWPM\_VSWITCH\_EVENT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a><span data-ttu-id="50f95-190">Nuovi tipi enumerati</span><span class="sxs-lookup"><span data-stu-id="50f95-190">New enumerated types</span></span>

-   [<span data-ttu-id="50f95-191">**\_tipo di \_ rete \_ vswitch FWP**</span><span class="sxs-lookup"><span data-stu-id="50f95-191">**FWP\_VSWITCH\_NETWORK\_TYPE**</span></span>](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [<span data-ttu-id="50f95-192">**\_tipo di \_ funzionalità di rete APPC \_ FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="50f95-192">**FWPM\_APPC\_NETWORK\_CAPABILITY\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [<span data-ttu-id="50f95-193">**\_tipo di \_ evento di connessione FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="50f95-193">**FWPM\_CONNECTION\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [<span data-ttu-id="50f95-194">**\_tipo di \_ evento \_ vswitch di FWPM**</span><span class="sxs-lookup"><span data-stu-id="50f95-194">**FWPM\_VSWITCH\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [<span data-ttu-id="50f95-195">**\_tipo di \_ \_ nome criteri CERT IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="50f95-195">**IKEEXT\_CERT\_CRITERIA\_NAME\_TYPE**</span></span>](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [<span data-ttu-id="50f95-196">**\_Evento del \_ contesto SA IPSec \_ \_ TYPE0**</span><span class="sxs-lookup"><span data-stu-id="50f95-196">**IPSEC\_SA\_CONTEXT\_EVENT\_TYPE0**</span></span>](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a><span data-ttu-id="50f95-197">Nuovi identificatori del livello di filtro</span><span class="sxs-lookup"><span data-stu-id="50f95-197">New filtering layer identifiers</span></span>

[<span data-ttu-id="50f95-198">**Filtraggio degli identificatori di livello:**</span><span class="sxs-lookup"><span data-stu-id="50f95-198">**Filtering Layer Identifiers:**</span></span>](management-filtering-layer-identifiers-.md)

-   <span data-ttu-id="50f95-199">FWPM \_ Layer in \_ ingresso \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="50f95-199">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="50f95-200">FWPM \_ Layer in \_ uscita \_ Mac \_ frame \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="50f95-200">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="50f95-201">\_ \_ \_ \_ frame Mac \_ nativo in ingresso livello FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-201">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="50f95-202">\_ \_ frame Mac in uscita livello FWPM \_ \_ \_ nativo</span><span class="sxs-lookup"><span data-stu-id="50f95-202">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="50f95-203">FWPM \_ Layer in \_ ingresso \_ vswitch \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="50f95-203">FWPM\_LAYER\_INGRESS\_VSWITCH\_ETHERNET</span></span>
-   <span data-ttu-id="50f95-204">FWPM \_ Layer in \_ uscita \_ vswitch \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="50f95-204">FWPM\_LAYER\_EGRESS\_VSWITCH\_ETHERNET</span></span>
-   <span data-ttu-id="50f95-205">FWPM \_ Layer in \_ ingresso \_ vswitch \_ trasporto \_ V4/FWPM \_ livello \_ ingresso \_ vswitch \_ trasporto \_ V6</span><span class="sxs-lookup"><span data-stu-id="50f95-205">FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V6</span></span>
-   <span data-ttu-id="50f95-206">Livello FWPM in \_ \_ uscita vswitch trasporto di \_ \_ \_ livello V4/FWPM in \_ \_ uscita \_ vswitch \_ trasporto \_ V6</span><span class="sxs-lookup"><span data-stu-id="50f95-206">FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V6</span></span>

## <a name="new-filtering-condition-identifiers"></a><span data-ttu-id="50f95-207">Nuovi identificatori di condizione di filtro</span><span class="sxs-lookup"><span data-stu-id="50f95-207">New filtering condition identifiers</span></span>

[<span data-ttu-id="50f95-208">**Filtraggio degli identificatori di condizione:**</span><span class="sxs-lookup"><span data-stu-id="50f95-208">**Filtering Condition Identifiers:**</span></span>](filtering-condition-identifiers-.md)

-   <span data-ttu-id="50f95-209">\_ \_ indirizzo MAC dell'interfaccia della condizione FWPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="50f95-209">FWPM\_CONDITION\_INTERFACE\_MAC\_ADDRESS</span></span>
-   <span data-ttu-id="50f95-210">\_ \_ \_ indirizzo locale Mac della condizione FWPM \_</span><span class="sxs-lookup"><span data-stu-id="50f95-210">FWPM\_CONDITION\_MAC\_LOCAL\_ADDRESS</span></span>
-   <span data-ttu-id="50f95-211">\_ \_ \_ indirizzo remoto Mac condizione \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-211">FWPM\_CONDITION\_MAC\_REMOTE\_ADDRESS</span></span>
-   <span data-ttu-id="50f95-212">\_ \_ tipo etere della condizione FWPM \_</span><span class="sxs-lookup"><span data-stu-id="50f95-212">FWPM\_CONDITION\_ETHER\_TYPE</span></span>
-   <span data-ttu-id="50f95-213">\_ \_ ID VLAN della condizione FWPM \_</span><span class="sxs-lookup"><span data-stu-id="50f95-213">FWPM\_CONDITION\_VLAN\_ID</span></span>
-   <span data-ttu-id="50f95-214">\_ \_ porta NDIS (FWPM Condition) \_</span><span class="sxs-lookup"><span data-stu-id="50f95-214">FWPM\_CONDITION\_NDIS\_PORT</span></span>
-   <span data-ttu-id="50f95-215">\_tipo di \_ \_ supporto NDIS Condition FWPM \_</span><span class="sxs-lookup"><span data-stu-id="50f95-215">FWPM\_CONDITION\_NDIS\_MEDIA\_TYPE</span></span>
-   <span data-ttu-id="50f95-216">\_tipo di \_ \_ supporto fisico \_ NDIS \_ condizione FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-216">FWPM\_CONDITION\_NDIS\_PHYSICAL\_MEDIA\_TYPE</span></span>
-   <span data-ttu-id="50f95-217">\_ \_ Flag L2 della condizione FWPM \_</span><span class="sxs-lookup"><span data-stu-id="50f95-217">FWPM\_CONDITION\_L2\_FLAGS</span></span>
-   <span data-ttu-id="50f95-218">\_tipo di \_ \_ indirizzo locale \_ Mac \_ della condizione FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-218">FWPM\_CONDITION\_MAC\_LOCAL\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="50f95-219">\_tipo di \_ \_ indirizzo remoto \_ Mac \_ della condizione FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-219">FWPM\_CONDITION\_MAC\_REMOTE\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="50f95-220">\_ \_ \_ ID pacchetto ale condizione \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-220">FWPM\_CONDITION\_ALE\_PACKAGE\_ID</span></span>
-   <span data-ttu-id="50f95-221">\_indirizzo di \_ \_ origine Mac della condizione \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-221">FWPM\_CONDITION\_MAC\_SOURCE\_ADDRESS</span></span>
-   <span data-ttu-id="50f95-222">\_indirizzo di \_ \_ destinazione Mac della condizione \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-222">FWPM\_CONDITION\_MAC\_DESTINATION\_ADDRESS</span></span>
-   <span data-ttu-id="50f95-223">\_tipo di \_ \_ indirizzo di origine Mac della condizione \_ FWPM \_</span><span class="sxs-lookup"><span data-stu-id="50f95-223">FWPM\_CONDITION\_MAC\_SOURCE\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="50f95-224">\_tipo di \_ \_ indirizzo di destinazione Mac della condizione \_ FWPM \_</span><span class="sxs-lookup"><span data-stu-id="50f95-224">FWPM\_CONDITION\_MAC\_DESTINATION\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="50f95-225">\_porta di \_ \_ origine IP della condizione \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-225">FWPM\_CONDITION\_IP\_SOURCE\_PORT</span></span>
-   <span data-ttu-id="50f95-226">\_porta di \_ \_ destinazione IP della condizione \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-226">FWPM\_CONDITION\_IP\_DESTINATION\_PORT</span></span>
-   <span data-ttu-id="50f95-227">\_ \_ ID vswitch condizione \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="50f95-227">FWPM\_CONDITION\_VSWITCH\_ID</span></span>
-   <span data-ttu-id="50f95-228">\_tipo di \_ \_ rete vswitch condizione FWPM \_</span><span class="sxs-lookup"><span data-stu-id="50f95-228">FWPM\_CONDITION\_VSWITCH\_NETWORK\_TYPE</span></span>
-   <span data-ttu-id="50f95-229">FWPM \_ Condition \_ vswitch \_ \_ ID interfaccia di origine \_</span><span class="sxs-lookup"><span data-stu-id="50f95-229">FWPM\_CONDITION\_VSWITCH\_SOURCE\_INTERFACE\_ID</span></span>
-   <span data-ttu-id="50f95-230">FWPM \_ Condition \_ vswitch \_ \_ ID interfaccia di destinazione \_</span><span class="sxs-lookup"><span data-stu-id="50f95-230">FWPM\_CONDITION\_VSWITCH\_DESTINATION\_INTERFACE\_ID</span></span>
-   <span data-ttu-id="50f95-231">FWPM \_ Condition \_ vswitch \_ \_ ID macchina virtuale di origine \_</span><span class="sxs-lookup"><span data-stu-id="50f95-231">FWPM\_CONDITION\_VSWITCH\_SOURCE\_VM\_ID</span></span>
-   <span data-ttu-id="50f95-232">FWPM \_ Condition \_ vswitch \_ \_ ID macchina virtuale di destinazione \_</span><span class="sxs-lookup"><span data-stu-id="50f95-232">FWPM\_CONDITION\_VSWITCH\_DESTINATION\_VM\_ID</span></span>
-   <span data-ttu-id="50f95-233">FWPM \_ Condition \_ vswitch \_ \_ tipo di interfaccia di origine \_</span><span class="sxs-lookup"><span data-stu-id="50f95-233">FWPM\_CONDITION\_VSWITCH\_SOURCE\_INTERFACE\_TYPE</span></span>
-   <span data-ttu-id="50f95-234">FWPM \_ Condition \_ vswitch \_ \_ ID rete \_ tenant</span><span class="sxs-lookup"><span data-stu-id="50f95-234">FWPM\_CONDITION\_VSWITCH\_TENANT\_NETWORK\_ID</span></span>

## <a name="new-filtering-condition-flags"></a><span data-ttu-id="50f95-235">Nuovi flag di condizione di filtro</span><span class="sxs-lookup"><span data-stu-id="50f95-235">New filtering condition flags</span></span>

[<span data-ttu-id="50f95-236">**Flag di condizione di filtro:**</span><span class="sxs-lookup"><span data-stu-id="50f95-236">**Filtering Condition Flags:**</span></span>](filtering-condition-flags-.md)

-   <span data-ttu-id="50f95-237">il \_ flag di condizione FWP \_ è una \_ \_ \_ connessione proxy</span><span class="sxs-lookup"><span data-stu-id="50f95-237">FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION</span></span>
-   <span data-ttu-id="50f95-238">il \_ flag di condizione FWP \_ è un \_ \_ \_ loopback appcontainer</span><span class="sxs-lookup"><span data-stu-id="50f95-238">FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK</span></span>
-   <span data-ttu-id="50f95-239">il \_ flag di condizione FWP \_ è un \_ \_ \_ loopback non appcontainer \_</span><span class="sxs-lookup"><span data-stu-id="50f95-239">FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK</span></span>
-   <span data-ttu-id="50f95-240">il \_ flag di condizione FWP \_ \_ sta \_ rispettando l' \_ \_ autorizzazione per i criteri</span><span class="sxs-lookup"><span data-stu-id="50f95-240">FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE</span></span>
-   <span data-ttu-id="50f95-241">\_La condizione \_ FWP \_ L2 \_ è \_ Ethernet nativa</span><span class="sxs-lookup"><span data-stu-id="50f95-241">FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET</span></span>
-   <span data-ttu-id="50f95-242">\_La condizione FWP \_ L2 \_ è \_ Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="50f95-242">FWP\_CONDITION\_L2\_IS\_WIFI</span></span>
-   <span data-ttu-id="50f95-243">\_La condizione FWP \_ L2 \_ è \_ mobile \_ Broadband</span><span class="sxs-lookup"><span data-stu-id="50f95-243">FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND</span></span>
-   <span data-ttu-id="50f95-244">\_La condizione \_ FWP \_ L2 \_ è \_ dati diretti Wi-Fi \_</span><span class="sxs-lookup"><span data-stu-id="50f95-244">FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA</span></span>
-   <span data-ttu-id="50f95-245">\_La condizione FWP \_ L2 \_ è \_ VM2VM</span><span class="sxs-lookup"><span data-stu-id="50f95-245">FWP\_CONDITION\_L2\_IS\_VM2VM</span></span>
-   <span data-ttu-id="50f95-246">\_La condizione FWP \_ L2 è un \_ \_ pacchetto in formato non valido \_</span><span class="sxs-lookup"><span data-stu-id="50f95-246">FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET</span></span>
-   <span data-ttu-id="50f95-247">\_La condizione FWP \_ L2 è un gruppo di \_ \_ \_ frammenti IP \_</span><span class="sxs-lookup"><span data-stu-id="50f95-247">FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP</span></span>
-   <span data-ttu-id="50f95-248">\_Condizione FWP \_ L2 \_ se \_ connettore \_ presente</span><span class="sxs-lookup"><span data-stu-id="50f95-248">FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT</span></span>

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a><span data-ttu-id="50f95-249">Aggiornamenti di Windows 7 alla piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="50f95-249">Windows 7 updates to the Windows Filtering Platform</span></span>

<span data-ttu-id="50f95-250">Il documento [novità di Windows Filtering Platform descrive in]() dettaglio molti degli aggiornamenti effettuati per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="50f95-250">The document [What's New in Windows Filtering Platform]() details many of the updates made for Windows 7.</span></span> <span data-ttu-id="50f95-251">Le informazioni sono inoltre disponibili nel kit driver Windows sulle [modifiche al WFP per Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).</span><span class="sxs-lookup"><span data-stu-id="50f95-251">Information is also available in the Windows Driver Kit on [WFP Changes for Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).</span></span>

 

 