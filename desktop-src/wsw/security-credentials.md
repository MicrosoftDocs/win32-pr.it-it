---
title: Credenziali di protezione
description: Le credenziali di sicurezza sono una parte di evidenza che un'entità di comunicazione possiede, che può essere usata per creare o ottenere un token di sicurezza.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Servizi Web per le credenziali di sicurezza per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300703"
---
# <a name="security-credentials"></a><span data-ttu-id="22705-106">Credenziali di protezione</span><span class="sxs-lookup"><span data-stu-id="22705-106">Security Credentials</span></span>

<span data-ttu-id="22705-107">Le credenziali di sicurezza sono una parte di evidenza che un'entità di comunicazione possiede, che può essere usata per creare o ottenere un token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="22705-107">Security credentials are a piece of evidence that a communicating party possesses that can be used to create or obtain a security token.</span></span> <span data-ttu-id="22705-108">Pertanto, le credenziali sono in genere più longeve dei token di sicurezza e un token di sicurezza può essere visualizzato come la manifestazione di runtime delle credenziali di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="22705-108">Thus, credentials are typically longer-lived than security tokens, and a security token can be viewed as the runtime manifestation of the security credentials.</span></span> <span data-ttu-id="22705-109">Esempi di credenziali includono un certificato del computer (che può essere convertito in un token di sicurezza X. 509 in fase di esecuzione) o una coppia nome utente/password per un dominio (che può essere usato per ottenere un token di sicurezza Kerberos).</span><span class="sxs-lookup"><span data-stu-id="22705-109">Example of credentials include a machine certificate (which can be converted into an X.509 security token at runtime) or a username/password pair for a domain (which can be used to obtain a Kerberos security token).</span></span>


<span data-ttu-id="22705-110">Le credenziali vengono specificate come parte delle [associazioni di sicurezza](security-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="22705-110">Credentials are specified as part of the [security bindings](security-bindings.md).</span></span>

<span data-ttu-id="22705-111">Con le credenziali di sicurezza vengono usati gli elementi API seguenti.</span><span class="sxs-lookup"><span data-stu-id="22705-111">The following API elements are used with security credentials.</span></span>

| <span data-ttu-id="22705-112">Callback</span><span class="sxs-lookup"><span data-stu-id="22705-112">Callback</span></span>                                                                  | <span data-ttu-id="22705-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22705-113">Description</span></span>                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="22705-114">**CALLBACK di WS \_ get \_ CERT \_**</span><span class="sxs-lookup"><span data-stu-id="22705-114">**WS\_GET\_CERT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | <span data-ttu-id="22705-115">Fornisce un certificato al runtime di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="22705-115">Provides a certificate to the security runtime.</span></span>          |
| [<span data-ttu-id="22705-116">**\_callback WS Validate \_ password \_**</span><span class="sxs-lookup"><span data-stu-id="22705-116">**WS\_VALIDATE\_PASSWORD\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | <span data-ttu-id="22705-117">Convalida una coppia nome utente/password sul lato ricevente.</span><span class="sxs-lookup"><span data-stu-id="22705-117">Validates a username/password pair on the receiver side.</span></span> |



 



| <span data-ttu-id="22705-118">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="22705-118">Enumeration</span></span>                                                                                           | <span data-ttu-id="22705-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22705-119">Description</span></span>                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="22705-120">**\_tipo di \_ credenziale WS CERT \_**</span><span class="sxs-lookup"><span data-stu-id="22705-120">**WS\_CERT\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | <span data-ttu-id="22705-121">Tipo di credenziale del certificato.</span><span class="sxs-lookup"><span data-stu-id="22705-121">The type of the certificate credential.</span></span>                       |
| [<span data-ttu-id="22705-122">**\_tipo di \_ credenziale WS nomeutente \_**</span><span class="sxs-lookup"><span data-stu-id="22705-122">**WS\_USERNAME\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | <span data-ttu-id="22705-123">Tipo di credenziali nome utente/password.</span><span class="sxs-lookup"><span data-stu-id="22705-123">The type of the username/password credential.</span></span>                 |
| [<span data-ttu-id="22705-124">**\_tipo di \_ \_ credenziali di autenticazione integrata \_ \_ di WS Windows**</span><span class="sxs-lookup"><span data-stu-id="22705-124">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | <span data-ttu-id="22705-125">Tipo di credenziale di autenticazione integrata di Windows.</span><span class="sxs-lookup"><span data-stu-id="22705-125">The type of the Windows Integrated Authentication credential.</span></span> |



 



| <span data-ttu-id="22705-126">Struttura</span><span class="sxs-lookup"><span data-stu-id="22705-126">Structure</span></span>                                                                                                   | <span data-ttu-id="22705-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22705-127">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22705-128">**\_credenziali WS CERT \_**</span><span class="sxs-lookup"><span data-stu-id="22705-128">**WS\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | <span data-ttu-id="22705-129">Il tipo di base astratto per tutti i tipi di credenziali del certificato.</span><span class="sxs-lookup"><span data-stu-id="22705-129">The abstract base type for all certificate credential types.</span></span>                                                          |
| [<span data-ttu-id="22705-130">**\_ \_ credenziale certificato personalizzata WS \_**</span><span class="sxs-lookup"><span data-stu-id="22705-130">**WS\_CUSTOM\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | <span data-ttu-id="22705-131">Tipo per specificare le credenziali di un certificato che devono essere fornite da un callback all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="22705-131">The type for specifying a certificate credential that is to be supplied by a callback to the application.</span></span>             |
| [<span data-ttu-id="22705-132">**\_credenziali di \_ \_ autenticazione integrata \_ di Windows WS predefinite \_**</span><span class="sxs-lookup"><span data-stu-id="22705-132">**WS\_DEFAULT\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | <span data-ttu-id="22705-133">Digitare per fornire le credenziali di autenticazione integrata di Windows in base al token del thread corrente.</span><span class="sxs-lookup"><span data-stu-id="22705-133">Type for supplying a Windows Integrated Authentication credential based on the current thread token.</span></span>                  |
| [<span data-ttu-id="22705-134">**\_credenziali di \_ \_ autenticazione integrata \_ di Windows WS opaco \_**</span><span class="sxs-lookup"><span data-stu-id="22705-134">**WS\_OPAQUE\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | <span data-ttu-id="22705-135">Digitare per fornire le credenziali di autenticazione integrata di Windows.</span><span class="sxs-lookup"><span data-stu-id="22705-135">Type for supplying a Windows Integrated Authentication credential.</span></span>                                                    |
| [<span data-ttu-id="22705-136">**\_ \_ credenziali nome utente WS stringa \_**</span><span class="sxs-lookup"><span data-stu-id="22705-136">**WS\_STRING\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | <span data-ttu-id="22705-137">Tipo per la fornitura di una coppia nome utente/password come stringhe.</span><span class="sxs-lookup"><span data-stu-id="22705-137">The type for supplying a username/password pair as strings.</span></span>                                                           |
| [<span data-ttu-id="22705-138">**\_credenziali di \_ \_ autenticazione integrata \_ di Windows WS String \_**</span><span class="sxs-lookup"><span data-stu-id="22705-138">**WS\_STRING\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | <span data-ttu-id="22705-139">Digitare per specificare le credenziali di Windows come nome utente, password, stringhe di dominio.</span><span class="sxs-lookup"><span data-stu-id="22705-139">Type for supplying a Windows credential as username, password, domain strings.</span></span>                                        |
| [<span data-ttu-id="22705-140">**\_ \_ credenziali certificato del nome del soggetto ws \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22705-140">**WS\_SUBJECT\_NAME\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | <span data-ttu-id="22705-141">Tipo per specificare una credenziale del certificato usando il nome del soggetto, il percorso e il nome dell'archivio del certificato.</span><span class="sxs-lookup"><span data-stu-id="22705-141">The type for specifying a certificate credential using the certificate's subject name, store location and store name.</span></span> |
| [<span data-ttu-id="22705-142">**\_credenziali del certificato di identificazione personale ws \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22705-142">**WS\_THUMBPRINT\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | <span data-ttu-id="22705-143">Tipo per specificare una credenziale del certificato utilizzando l'identificazione personale del certificato, il percorso dell'archivio e il nome dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="22705-143">The type for specifying a certificate credential using the certificate's thumbprint, store location and store name.</span></span>   |
| [<span data-ttu-id="22705-144">**\_credenziali nome utente WS \_**</span><span class="sxs-lookup"><span data-stu-id="22705-144">**WS\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | <span data-ttu-id="22705-145">Il tipo di base astratto per tutte le credenziali nome utente/password.</span><span class="sxs-lookup"><span data-stu-id="22705-145">The abstract base type for all username/password credentials.</span></span>                                                         |
| [<span data-ttu-id="22705-146">**\_credenziali di \_ \_ autenticazione integrata \_ di WS Windows**</span><span class="sxs-lookup"><span data-stu-id="22705-146">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | <span data-ttu-id="22705-147">Il tipo di base astratto per tutti i tipi di credenziali utilizzati con l'autenticazione integrata di Windows.</span><span class="sxs-lookup"><span data-stu-id="22705-147">The abstract base type for all credential types used with Windows Integrated Authentication.</span></span>                          |



 

 

 




