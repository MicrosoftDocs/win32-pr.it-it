---
title: Associazioni di sicurezza
description: Un'associazione di sicurezza è la specifica di un token di sicurezza e indica al runtime come ottenere e usare un token di sicurezza per la sicurezza del canale.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Associazioni di sicurezza servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104118670"
---
# <a name="security-bindings"></a><span data-ttu-id="e962d-106">Associazioni di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e962d-106">Security Bindings</span></span>

<span data-ttu-id="e962d-107">Un'associazione di sicurezza è la specifica di un token di sicurezza e indica al runtime come ottenere e usare un token di sicurezza per la sicurezza del canale.</span><span class="sxs-lookup"><span data-stu-id="e962d-107">A security binding is the specification of a security token, and tells the runtime how to obtain and use a security token for channel security.</span></span> <span data-ttu-id="e962d-108">Il token di sicurezza contiene informazioni che giustificano il diritto di accesso alle risorse.</span><span class="sxs-lookup"><span data-stu-id="e962d-108">The security token contains information that vouches for the right to access resources.</span></span> <span data-ttu-id="e962d-109">Potrebbe inoltre disporre di una chiave crittografica associata per eseguire le firme e la crittografia.</span><span class="sxs-lookup"><span data-stu-id="e962d-109">It may also have an associated cryptographic key for performing signatures and encryption.</span></span>


<span data-ttu-id="e962d-110">Ogni associazione di sicurezza contiene una raccolta specifica di [impostazioni di associazione di sicurezza](security-binding-settings.md) facoltative che hanno come ambito il token di sicurezza definito.</span><span class="sxs-lookup"><span data-stu-id="e962d-110">Each security binding contains its own collection of optional [security binding settings](security-binding-settings.md) that are scoped to the security token it defines.</span></span> <span data-ttu-id="e962d-111">Contiene anche le [credenziali di sicurezza](security-credentials.md), che rappresentano l'evidenza di sicurezza, ad esempio nome utente e password o certificati, necessari per creare i token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e962d-111">It also contains [security credentials](security-credentials.md), representing the security evidence (such as username and passwords, or certificates) needed to create security tokens.</span></span>

<span data-ttu-id="e962d-112">I callback seguenti fanno parte dell'associazione di sicurezza:</span><span class="sxs-lookup"><span data-stu-id="e962d-112">The following callbacks are part of the security binding:</span></span>

-   [<span data-ttu-id="e962d-113">**\_ \_ callback SAML WS \_ Validate**</span><span class="sxs-lookup"><span data-stu-id="e962d-113">**WS\_VALIDATE\_SAML\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

<span data-ttu-id="e962d-114">Le enumerazioni seguenti fanno parte dell'associazione di sicurezza:</span><span class="sxs-lookup"><span data-stu-id="e962d-114">The following enumerations are part of the security binding:</span></span>

-   [<span data-ttu-id="e962d-115">**\_utilizzo della \_ sicurezza del messaggio WS \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-115">**WS\_MESSAGE\_SECURITY\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [<span data-ttu-id="e962d-116">**\_tipo di \_ autenticatore WS SAML \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-116">**WS\_SAML\_AUTHENTICATOR\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [<span data-ttu-id="e962d-117">**\_tipo di \_ associazione di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-117">**WS\_SECURITY\_BINDING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [<span data-ttu-id="e962d-118">**\_tipo di \_ handle della chiave di sicurezza WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-118">**WS\_SECURITY\_KEY\_HANDLE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

<span data-ttu-id="e962d-119">Le funzioni seguenti fanno parte dell'associazione di sicurezza:</span><span class="sxs-lookup"><span data-stu-id="e962d-119">The following functions are part of the security binding:</span></span>

-   [<span data-ttu-id="e962d-120">**WsCreateXmlSecurityToken**</span><span class="sxs-lookup"><span data-stu-id="e962d-120">**WsCreateXmlSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [<span data-ttu-id="e962d-121">**WsFreeSecurityToken**</span><span class="sxs-lookup"><span data-stu-id="e962d-121">**WsFreeSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

<span data-ttu-id="e962d-122">Le strutture seguenti fanno parte dell'associazione di sicurezza:</span><span class="sxs-lookup"><span data-stu-id="e962d-122">The following structures are part of the security binding:</span></span>

-   [<span data-ttu-id="e962d-123">**\_handle della \_ \_ chiave di sicurezza asimmetrica \_ \_ di WS capi**</span><span class="sxs-lookup"><span data-stu-id="e962d-123">**WS\_CAPI\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [<span data-ttu-id="e962d-124">**\_ \_ \_ autenticatore SAML firmato da WS CERT \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-124">**WS\_CERT\_SIGNED\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [<span data-ttu-id="e962d-125">**\_binding di \_ sicurezza di autenticazione dell'intestazione WS http \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-125">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [<span data-ttu-id="e962d-126">**\_binding di \_ \_ sicurezza del messaggio WS Kerberos APREQ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-126">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [<span data-ttu-id="e962d-127">**BINDING di sicurezza del trasporto di WS \_ NAMEDPIPE \_ SSPI \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-127">**WS\_NAMEDPIPE\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="e962d-128">**\_handle della \_ \_ chiave di sicurezza asimmetrica WS NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-128">**WS\_NCRYPT\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [<span data-ttu-id="e962d-129">**\_handle di \_ \_ chiave di sicurezza simmetrica WS RAW \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-129">**WS\_RAW\_SYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [<span data-ttu-id="e962d-130">**\_ \_ autenticatore WS SAML**</span><span class="sxs-lookup"><span data-stu-id="e962d-130">**WS\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [<span data-ttu-id="e962d-131">**\_binding di \_ sicurezza del messaggio WS SAML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-131">**WS\_SAML\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [<span data-ttu-id="e962d-132">**\_binding di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-132">**WS\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [<span data-ttu-id="e962d-133">**\_associazione di \_ sicurezza del messaggio del contesto di sicurezza WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-133">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [<span data-ttu-id="e962d-134">**\_handle della \_ chiave di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-134">**WS\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [<span data-ttu-id="e962d-135">**\_binding di \_ sicurezza del trasporto \_ \_ di WS SSL**</span><span class="sxs-lookup"><span data-stu-id="e962d-135">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [<span data-ttu-id="e962d-136">**\_binding di \_ \_ sicurezza del trasporto SSPI \_ \_ di WS TCP**</span><span class="sxs-lookup"><span data-stu-id="e962d-136">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [<span data-ttu-id="e962d-137">**\_binding di \_ \_ sicurezza messaggio WS nomeutente \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-137">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [<span data-ttu-id="e962d-138">**\_associazione di \_ sicurezza del messaggio del token WS XML \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e962d-138">**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




