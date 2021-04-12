---
title: Sequenza di chiamate API del metodo tunnel
description: Informazioni sulla sequenza di chiamate API per i metodi di tunneling. Vedere una panoramica e visualizzare altre risorse disponibili.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339302"
---
# <a name="tunnel-method-api-call-sequence"></a><span data-ttu-id="ead57-104">Sequenza di chiamate API del metodo tunnel</span><span class="sxs-lookup"><span data-stu-id="ead57-104">Tunnel Method API Call Sequence</span></span>

<span data-ttu-id="ead57-105">In questo argomento viene illustrata la sequenza di chiamate API per i metodi tunnel</span><span class="sxs-lookup"><span data-stu-id="ead57-105">This topic covers the API call sequence for Tunnel Methods</span></span>

## <a name="tunnel-method-call-sequence-overview"></a><span data-ttu-id="ead57-106">Panoramica della sequenza di chiamate al metodo tunnel</span><span class="sxs-lookup"><span data-stu-id="ead57-106">Tunnel Method Call Sequence Overview</span></span>

<span data-ttu-id="ead57-107">Quando richiedente viene richiesta l'identità dell'utente e i dati utente, viene in genere generato il flusso di chiamate API seguente.</span><span class="sxs-lookup"><span data-stu-id="ead57-107">When Supplicant gets request for user identity and user data the following API call flow typically occurs.</span></span>

-   <span data-ttu-id="ead57-108">Il supplicant chiama EapHostPeerProcessReceivedPacket su EapHost per elaborare il pacchetto ricevuto dall'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="ead57-108">The Supplicant calls EapHostPeerProcessReceivedPacket on EapHost, to process the packet received from the authenticator.</span></span>
-   <span data-ttu-id="ead57-109">Quando si elabora questo pacchetto, EAPHost lo determina come pacchetto IdentityRequest e chiama [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) sul metodo tunnel per ottenere l'identità utente da usare per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ead57-109">Upon processing this packet, EAPHost determines it as IdentityRequest packet and calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on tunnel method to obtain the user identity to use for authentication.</span></span>
-   <span data-ttu-id="ead57-110">Se il metodo tunnel deve ottenere l'identità dell'utente dal metodo interno, chiama [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) su EAPHost interno, che a sua volta chiama [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) sul metodo interno.</span><span class="sxs-lookup"><span data-stu-id="ead57-110">If tunnel method needs to obtain user identity from the inner method, it calls [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) on inner EAPHost, which in turn calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on the inner method.</span></span>

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a><span data-ttu-id="ead57-111">Interazione dell'utente con il flusso di chiamate API dei metodi tunnel</span><span class="sxs-lookup"><span data-stu-id="ead57-111">User Interaction with the Tunnel Methods API Call Flow</span></span>

<span data-ttu-id="ead57-112">In alcuni casi, quando l'identità non è disponibile o quando l'utente deve fornire informazioni aggiuntive, il metodo EAP genera una finestra di dialogo dell'interfaccia utente nel supplicant.</span><span class="sxs-lookup"><span data-stu-id="ead57-112">In certain cases, when the identity is not available, or when the user must provide additional information, Eap Method raises an user interface dialog box on the supplicant.</span></span>

<span data-ttu-id="ead57-113">In questi casi, la sequenza di chiamate viene in genere svolta per ottenere informazioni direttamente dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ead57-113">In such cases following call sequence typically takes place to get information directly from the user.</span></span>

-   <span data-ttu-id="ead57-114">Il metodo EAP del tunnel restituisce il codice dell'azione per richiamare l'interfaccia utente in EapHost.</span><span class="sxs-lookup"><span data-stu-id="ead57-114">Tunnel Eap Method returns action code to invoke UI to EapHost.</span></span> <span data-ttu-id="ead57-115">Supplicant chiama [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)per ottenere le informazioni sul contesto dell'interfaccia utente corrente per la finestra di dialogo dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ead57-115">Supplicant calls [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)to obtain the current user interface context information for the user interface dialog box.</span></span>
-   <span data-ttu-id="ead57-116">Supplicant chiama quindi [ **EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span><span class="sxs-lookup"><span data-stu-id="ead57-116">Supplicant then calls [**EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span></span> <span data-ttu-id="ead57-117">Questa funzione utilizza le informazioni sul contesto dell'interfaccia utente per generare un'interfaccia utente interattiva utilizzata per ottenere informazioni sulle credenziali dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ead57-117">This function uses the UI context information to raise an interactive user interface which is used to get credential information from the user.</span></span> <span data-ttu-id="ead57-118">Il processo dell'interfaccia utente carica Eappcfg.dll e ottiene i puntatori a EapPeerInvokeInteractiveUI e EapPeerFreeMemory.</span><span class="sxs-lookup"><span data-stu-id="ead57-118">The UI process loads Eappcfg.dll and obtains the pointers to EapPeerInvokeInteractiveUI and EapPeerFreeMemory.</span></span>
    > [!Note]  
    > <span data-ttu-id="ead57-119">Il processo dell'interfaccia utente in genere raccoglie l'interfaccia utente o gestisce l'interfaccia utente interattiva ed è separato dal processo di supplicant.</span><span class="sxs-lookup"><span data-stu-id="ead57-119">UI process typically collects UI or handles interactive UI and is separate from the supplicant process.</span></span> <span data-ttu-id="ead57-120">La separazione dei due processi non è un requisito di EAPHost, ma questa operazione ha il vantaggio di consentire al processo dell'interfaccia utente di interagire con il desktop.</span><span class="sxs-lookup"><span data-stu-id="ead57-120">Separating the two processes is not a requirement of EAPHost, but doing so has the advantage of allowing the UI process to interact with the desktop.</span></span>

     

-   <span data-ttu-id="ead57-121">EapHost chiama [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) sul metodo tunnel per ottenere informazioni sull'identità dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ead57-121">EapHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on tunnel method to obtain user identity information.</span></span>
-   <span data-ttu-id="ead57-122">Per ottenere l'identità dell'utente dal metodo interno, il metodo tunnel chiama [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) sull'EAPHost interno.</span><span class="sxs-lookup"><span data-stu-id="ead57-122">In order to obtain user identity from inner method, tunnel method calls [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) on inner EAPHost.</span></span>
-   <span data-ttu-id="ead57-123">EAPHost interno chiama [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) sul metodo interno per richiamare l'interfaccia utente dell'identità utente.</span><span class="sxs-lookup"><span data-stu-id="ead57-123">Inner EAPHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on inner method to invoke user identity UI.</span></span>
-   <span data-ttu-id="ead57-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) fornisce informazioni sul contesto dell'interfaccia utente nuove o aggiornate al metodo peer EAP caricato in EAPHost dopo la generazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="ead57-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) provides a new or updated UI context information to the EAP peer method loaded on EAPHost after the UI has been raised.</span></span>

<span data-ttu-id="ead57-125">Il diagramma seguente illustra la sequenza di chiamate API per i metodi tunnel</span><span class="sxs-lookup"><span data-stu-id="ead57-125">Following diagram explains the API Call Sequence for Tunnel Methods</span></span>

![sequenza di chiamate API di metodi tunnel](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a><span data-ttu-id="ead57-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ead57-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ead57-128">Sequenza di chiamate EAPHost</span><span class="sxs-lookup"><span data-stu-id="ead57-128">EAPHost Call Sequence</span></span>](about-eaphost-call-sequences.md)
</dt> <dt>

[<span data-ttu-id="ead57-129">Sequenza di chiamate API supplicant</span><span class="sxs-lookup"><span data-stu-id="ead57-129">Supplicant API Call Sequence</span></span>](supplicant-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="ead57-130">Informazioni di riferimento sull'API del richiedente EAPHost</span><span class="sxs-lookup"><span data-stu-id="ead57-130">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




