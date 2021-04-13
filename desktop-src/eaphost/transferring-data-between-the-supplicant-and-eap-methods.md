---
title: Trasferimento di dati tra i metodi supplicant e EAP
description: Informazioni sul trasferimento di dati tra i metodi supplicant e EAP. Il trasferimento dei dati tra i metodi viene eseguito tramite gli attributi EAP.
ms.assetid: f1bcff61-286a-4f18-8a5d-93d5d1fd2b5b
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187858347e8630bfbaba0683700eaa39f116f6ce
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399734"
---
# <a name="transferring-data-between-the-supplicant-and-eap-methods"></a><span data-ttu-id="f12db-104">Trasferimento di dati tra i metodi supplicant e EAP</span><span class="sxs-lookup"><span data-stu-id="f12db-104">Transferring Data Between the Supplicant and EAP Methods</span></span>

<span data-ttu-id="f12db-105">L'uso di attributi EAP consente lo scambio di dati tra supplicant e metodi EAP.</span><span class="sxs-lookup"><span data-stu-id="f12db-105">Using EAP attributes allows data to be exchanged between supplicants and EAP methods.</span></span>

## <a name="attribute-consumption"></a><span data-ttu-id="f12db-106">Utilizzo degli attributi</span><span class="sxs-lookup"><span data-stu-id="f12db-106">Attribute Consumption</span></span>

<span data-ttu-id="f12db-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) utilizza gli attributi EAP passati direttamente al metodo EAP configurato.</span><span class="sxs-lookup"><span data-stu-id="f12db-107">[**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) consumes EAP attributes that are passed directly to the configured EAP method.</span></span> <span data-ttu-id="f12db-108">Analogamente, i metodi EAP possono restituire un codice di azione che indica al supplicant che gli attributi sono disponibili e che devono raccogliere gli attributi utilizzando [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span><span class="sxs-lookup"><span data-stu-id="f12db-108">Similarly, EAP methods are free to return an action code that indicates to the supplicant that attributes are available and that it should collect the attributes using [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes).</span></span>

<span data-ttu-id="f12db-109">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="f12db-109">For more information, see the following topics.</span></span>

-   <span data-ttu-id="f12db-110">Codici di azione del richiedente [peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span><span class="sxs-lookup"><span data-stu-id="f12db-110">[EAP Peer Supplicant Action Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="f12db-111">[Codici motivo della supplicant peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span><span class="sxs-lookup"><span data-stu-id="f12db-111">[EAP Peer Supplicant Reason Codes](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason).</span></span>
-   <span data-ttu-id="f12db-112">[Codici di azione del metodo di autenticazione EAP](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span><span class="sxs-lookup"><span data-stu-id="f12db-112">[EAP Authenticator Method Action Codes](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action).</span></span>

<span data-ttu-id="f12db-113">Si prevede che i supplicant ignorino gli attributi che non riconoscono o non possono agire.</span><span class="sxs-lookup"><span data-stu-id="f12db-113">Supplicants are expected to ignore attributes that they do not recognize or cannot act upon.</span></span> <span data-ttu-id="f12db-114">Utilizzando [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) questi attributi ignorati vengono restituiti a EAPHost e al metodo EAP.</span><span class="sxs-lookup"><span data-stu-id="f12db-114">Using [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) these ignored attributes are sent back to EAPHost and the EAP method.</span></span>

## <a name="vendor-specific-attributes"></a><span data-ttu-id="f12db-115">Attributi specifici del fornitore</span><span class="sxs-lookup"><span data-stu-id="f12db-115">Vendor Specific Attributes</span></span>

<span data-ttu-id="f12db-116">Utilizzando l'attributo EAP specifico del fornitore, i metodi e i supplicant EAP possono coinvolgere lo scambio di dati per uno scopo specifico.</span><span class="sxs-lookup"><span data-stu-id="f12db-116">By using the vendor-specific EAP attribute, EAP methods and supplicants can engage in data exchange for a specific purpose.</span></span> <span data-ttu-id="f12db-117">Gli attributi specifici del fornitore vengono ignorati dai supplicant e dai metodi che non supportano l'attributo specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="f12db-117">Vendor-specific attributes are ignored by supplicants and methods that do not support the vendor-specific attribute.</span></span>

<span data-ttu-id="f12db-118">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="f12db-118">For more information, see the following topics.</span></span>

-   <span data-ttu-id="f12db-119">[Attributi EAP](about-eap-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="f12db-119">[EAP Attributes](about-eap-attributes.md).</span></span>
-   <span data-ttu-id="f12db-120">[**EAP \_ \_tipo di attributo**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span><span class="sxs-lookup"><span data-stu-id="f12db-120">[**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f12db-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f12db-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f12db-122">Configurazione dell'interfaccia utente del metodo EAP</span><span class="sxs-lookup"><span data-stu-id="f12db-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="f12db-123">Abilitazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f12db-123">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="f12db-124">Implementazione del supporto di In-Band NAP per i metodi EAP</span><span class="sxs-lookup"><span data-stu-id="f12db-124">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="f12db-125">Implementazione del supporto NAP per i metodi EAP</span><span class="sxs-lookup"><span data-stu-id="f12db-125">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="f12db-126">Supplicant EAPHost</span><span class="sxs-lookup"><span data-stu-id="f12db-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




