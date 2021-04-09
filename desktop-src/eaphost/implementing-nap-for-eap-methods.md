---
title: Implementazione del supporto NAP per i metodi EAP
description: Informazioni su come implementare il supporto di protezione accesso alla rete per un supplicant EAPHost. Vedere gli argomenti relativi a protezione accesso alla rete correlati a EAPHost e visualizzare altre risorse disponibili.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5f0bc8900ee3d9cb01edb79b64b8ef5a68df4c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104047633"
---
# <a name="implementing-nap-support-for-eap-methods"></a><span data-ttu-id="3b7b3-104">Implementazione del supporto NAP per i metodi EAP</span><span class="sxs-lookup"><span data-stu-id="3b7b3-104">Implementing NAP Support for EAP Methods</span></span>

<span data-ttu-id="3b7b3-105">In questo argomento viene illustrato come implementare NAP per un supplicant EAPHost.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-105">This topic explains how to implement NAP for an EAPHost supplicant.</span></span> <span data-ttu-id="3b7b3-106">In Windows Vista e Windows Server 2008 è disponibile un client di imposizione di protezione accesso alla rete (NAP EC) per le connessioni autenticate [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="3b7b3-106">In Windows Vista and Windows Server 2008 a NAP Enforcement Client (NAP EC) is available for [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authenticated connections.</span></span>

## <a name="implementing-network-access-protection-nap"></a><span data-ttu-id="3b7b3-107">Implementazione di protezione accesso alla rete (NAP)</span><span class="sxs-lookup"><span data-stu-id="3b7b3-107">Implementing Network Access Protection (NAP)</span></span>

<span data-ttu-id="3b7b3-108">Per supportare NAP, un supplicant EAPHost implementa una funzione di callback che corrisponde al prototipo di callback [**NotificationHandler**](/previous-versions/windows/desktop/api) e deve fornire un puntatore a questa funzione di callback durante la chiamata di [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="3b7b3-108">To support NAP, an EAPHost supplicant implements a callback function matching the [**NotificationHandler**](/previous-versions/windows/desktop/api) callback prototype and must provide a pointer to this callback function when calling [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>

<span data-ttu-id="3b7b3-109">La funzione di callback accetta due parametri.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-109">The callback function takes two parameters.</span></span>

-   <span data-ttu-id="3b7b3-110">GUID che identifica in modo univoco l'interfaccia associata all'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-110">A GUID that uniquely identifies the interface associated with the authentication.</span></span>
-   <span data-ttu-id="3b7b3-111">Puntatore VOID a una struttura di dati opaca fornita dal supplicar.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-111">A VOID pointer to an opaque data structure that is supplied by the supplicant.</span></span>

<span data-ttu-id="3b7b3-112">EAPHost chiamerà la funzione di callback fornita dal richiedente con il GUID dell'interfaccia univoco e il puntatore VOID quando lo stato di quarantena del computer viene modificato.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-112">EAPHost will call the supplicant-provided callback function with the unique interface GUID and the VOID pointer when the quarantine state of the machine changes.</span></span> <span data-ttu-id="3b7b3-113">Quando EAPHost chiama la funzione di callback fornita dal richiedente, il supplicant risponde chiudendo la connessione di rete logica identificata dal puntatore GUID/VOID dell'interfaccia e inizia di nuovo l'autenticazione con **EapHostPeerBeginSession**.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-113">When EAPHost calls the supplicant-provided callback function, the supplicant responds by tearing down the logical network connection identified by the interface GUID/VOID pointer and begins authentication again using **EapHostPeerBeginSession**.</span></span>

<span data-ttu-id="3b7b3-114">EAPHost può chiamare la funzione di callback fornita da supplicant in qualsiasi momento: prima, durante un'autenticazione attiva o dopo il completamento dell'autenticazione (dopo la chiamata di [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) ma non prima della chiamata a [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ).</span><span class="sxs-lookup"><span data-stu-id="3b7b3-114">EAPHost may call the supplicant-supplied callback function at any time: before, during an active authentication, or after the authentication has been completed (after [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) has been called but not before [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) has been called).</span></span> <span data-ttu-id="3b7b3-115">Il richiedente risponde sempre chiudendo la connessione di rete logica ed eseguendo di nuovo l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-115">The supplicant should always respond by tearing down the logical network connection and re-authenticating.</span></span>

<span data-ttu-id="3b7b3-116">Se il richiedente si sta arrestando o scegliendo di non ricevere più notifiche relative alle modifiche dello stato di isolamento, il supplicant deve chiamare [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) e specificare il GUID dell'interfaccia appropriato.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-116">If the supplicant is shutting down or choosing to no longer receive notification of isolation state changes, the supplicant should call [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) and specify the appropriate interface GUID.</span></span> <span data-ttu-id="3b7b3-117">Se il richiedente desidera determinare l'isolamento della connessione di rete logica, il supplicant può ottenere tali informazioni da **EapHostPeerMethodResult. isolationState** quando [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) viene ottenuto da [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span><span class="sxs-lookup"><span data-stu-id="3b7b3-117">If the supplicant wishes to determine the isolation of the logical network connection, the supplicant can obtain that information from **EapHostPeerMethodResult.isolationState** when the [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) is obtained from [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span></span>

## <a name="eaphost-related-nap-information"></a><span data-ttu-id="3b7b3-118">Informazioni su protezione accesso alla rete correlate a EAPHost</span><span class="sxs-lookup"><span data-stu-id="3b7b3-118">EAPHost Related NAP Information</span></span>

<span data-ttu-id="3b7b3-119">Per informazioni su NAP correlate all'API EAPHost, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-119">For EAPHost API related NAP information refer to the following topics.</span></span>

-   [<span data-ttu-id="3b7b3-120">**\_tipo di attributo EAP \_**</span><span class="sxs-lookup"><span data-stu-id="3b7b3-120">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [<span data-ttu-id="3b7b3-121">**\_errore EAP**</span><span class="sxs-lookup"><span data-stu-id="3b7b3-121">**EAP\_ERROR**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [<span data-ttu-id="3b7b3-122">Domande frequenti sul richiedente EAPHost</span><span class="sxs-lookup"><span data-stu-id="3b7b3-122">EAPHost Supplicant Frequently Asked Questions</span></span>](eaphost-supplicant-frequently-asked-questions.md)
-   [<span data-ttu-id="3b7b3-123">**Proprietà del metodo EAP**</span><span class="sxs-lookup"><span data-stu-id="3b7b3-123">**EAP Method Properties**</span></span>](eap-method-properties.md)
-   [<span data-ttu-id="3b7b3-124">**EapHostPeerBeginSession**</span><span class="sxs-lookup"><span data-stu-id="3b7b3-124">**EapHostPeerBeginSession**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [<span data-ttu-id="3b7b3-125">**Costanti di errore e informazioni correlate a EAP**</span><span class="sxs-lookup"><span data-stu-id="3b7b3-125">**EAP Related Error and Information Constants**</span></span>](eap-related-error-and-information-constants.md)
-   [<span data-ttu-id="3b7b3-126">**stato di isolamento \_**</span><span class="sxs-lookup"><span data-stu-id="3b7b3-126">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [<span data-ttu-id="3b7b3-127">**NotificationHandler**</span><span class="sxs-lookup"><span data-stu-id="3b7b3-127">**NotificationHandler**</span></span>](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a><span data-ttu-id="3b7b3-128">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="3b7b3-128">Additional Resources</span></span>


-   <span data-ttu-id="3b7b3-129">Per un elenco delle risorse NAP, vedere [Protezione accesso alla rete](https://go.microsoft.com/fwlink/p/?linkid=84107).</span><span class="sxs-lookup"><span data-stu-id="3b7b3-129">For a list of NAP resources, see [Network Access Protection](https://go.microsoft.com/fwlink/p/?linkid=84107).</span></span>
-   <span data-ttu-id="3b7b3-130">Per informazioni sullo stato di integrità, vedere la pagina relativa [al rapporto di integrità (NAP, Network Access Protection) dei messaggi di](https://go.microsoft.com/fwlink/p/?linkid=83918)integrità.</span><span class="sxs-lookup"><span data-stu-id="3b7b3-130">For Statement of Health information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>
-   <span data-ttu-id="3b7b3-131">Per la pagina Web del gruppo di rete aziendale e il Blog, vedere [Protezione accesso alla rete (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span><span class="sxs-lookup"><span data-stu-id="3b7b3-131">For the Enterprise Networking Group webpage and blog, see [Network Access Protection (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span></span>
-   <span data-ttu-id="3b7b3-132">Per informazioni sull'API NAP, vedere [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page).</span><span class="sxs-lookup"><span data-stu-id="3b7b3-132">For NAP API information, see [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page).</span></span>


## <a name="related-topics"></a><span data-ttu-id="3b7b3-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b7b3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b7b3-134">Configurazione dell'interfaccia utente del metodo EAP</span><span class="sxs-lookup"><span data-stu-id="3b7b3-134">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="3b7b3-135">Abilitazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="3b7b3-135">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="3b7b3-136">Implementazione del supporto di In-Band NAP per i metodi EAP</span><span class="sxs-lookup"><span data-stu-id="3b7b3-136">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="3b7b3-137">Trasferimento di dati tra i metodi supplicant e EAP</span><span class="sxs-lookup"><span data-stu-id="3b7b3-137">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="3b7b3-138">Supplicant EAPHost</span><span class="sxs-lookup"><span data-stu-id="3b7b3-138">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 