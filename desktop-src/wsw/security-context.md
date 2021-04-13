---
title: Contesto di sicurezza
description: I contesti di sicurezza consentono di stabilire un contesto di sicurezza del messaggio in base a WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Contesto di sicurezza nativo-servizi Web
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339675"
---
# <a name="security-context"></a><span data-ttu-id="adc19-106">Contesto di sicurezza</span><span class="sxs-lookup"><span data-stu-id="adc19-106">Security Context</span></span>

<span data-ttu-id="adc19-107">I contesti di sicurezza consentono di stabilire un contesto di sicurezza del messaggio in base a WS-SecureConversation.</span><span class="sxs-lookup"><span data-stu-id="adc19-107">Security contexts enable the establishment of a message security context according to WS-SecureConversation.</span></span> <span data-ttu-id="adc19-108">Tale contesto può quindi essere utilizzato per proteggere i messaggi come alternativa alla sicurezza di un singolo punto in cui le credenziali vengono trasmesse per ogni richiesta.</span><span class="sxs-lookup"><span data-stu-id="adc19-108">That context can then be used to secure messages as an alternative to one-shot security where the credentials are transmitted for every request.</span></span> <span data-ttu-id="adc19-109">Il contesto di sicurezza stabilito è un metodo più efficiente per proteggere i messaggi quando vengono scambiati più messaggi.</span><span class="sxs-lookup"><span data-stu-id="adc19-109">The established security context is a more efficient method of securing messages when multiple messages are exchanged.</span></span>


<span data-ttu-id="adc19-110">I contesti di sicurezza richiedono la presenza di credenziali di sicurezza bootstrap utilizzate per proteggere i messaggi inviati nel contesto.</span><span class="sxs-lookup"><span data-stu-id="adc19-110">Security contexts require the presence of bootstrap security credentials that are used to secure the messages sent in the context.</span></span> <span data-ttu-id="adc19-111">Per questo scopo è possibile usare l'associazione di [**\_ sicurezza del messaggio WS Kerberos \_ \_ \_ \_ APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), l'associazione di sicurezza dei messaggi del [**\_ \_ token WS \_ \_ \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)e le strutture di [**\_ \_ \_ \_ associazione di sicurezza dei messaggi WS nomeutente**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) .</span><span class="sxs-lookup"><span data-stu-id="adc19-111">The [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding), and [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) structures may be used for this purpose.</span></span>

<span data-ttu-id="adc19-112">I contesti di sicurezza sono una funzionalità di sicurezza dei messaggi e vengono configurati tramite associazioni di sicurezza dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="adc19-112">Security contexts are a message security feature and are configured by way of message security bindings.</span></span>

## <a name="client"></a><span data-ttu-id="adc19-113">Client</span><span class="sxs-lookup"><span data-stu-id="adc19-113">Client</span></span>

<span data-ttu-id="adc19-114">Sul lato client, il contesto di sicurezza è associato a un canale specifico.</span><span class="sxs-lookup"><span data-stu-id="adc19-114">On the client side, the security context is tied to a particular channel.</span></span> <span data-ttu-id="adc19-115">Viene configurato utilizzando l' [**associazione di \_ \_ sicurezza del \_ messaggio \_ \_ del contesto di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span><span class="sxs-lookup"><span data-stu-id="adc19-115">It is configured using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span></span> <span data-ttu-id="adc19-116">Il comportamento e la durata del contesto sono determinati dal canale.</span><span class="sxs-lookup"><span data-stu-id="adc19-116">Behavior and lifetime of the context are determined by the channel.</span></span> <span data-ttu-id="adc19-117">Quando il primo messaggio viene inviato sul canale, viene stabilito il contesto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="adc19-117">When the first message is sent on the channel, the security context is established.</span></span> <span data-ttu-id="adc19-118">Successivamente, il contesto viene rinnovato in modo proattivo a un intervallo configurabile.</span><span class="sxs-lookup"><span data-stu-id="adc19-118">After that, the context is proactively renewed at a configurable interval.</span></span> <span data-ttu-id="adc19-119">Se il server restituisce un errore che indica che il contesto richiede il rinnovo, il contesto viene rinnovato quando viene inviato il messaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="adc19-119">If the server returns a fault indicating that the context requires renewal, the context is renewed when the next message is sent.</span></span> <span data-ttu-id="adc19-120">Se il canale si trova nello stato aperto, il contesto viene annullato da un messaggio di annullamento quando il canale viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="adc19-120">If the channel is in the open state, the context is canceled by a cancel message when the channel is closed.</span></span>

## <a name="server"></a><span data-ttu-id="adc19-121">Server</span><span class="sxs-lookup"><span data-stu-id="adc19-121">Server</span></span>

<span data-ttu-id="adc19-122">Sul server, un contesto di sicurezza viene configurato in modo analogo a quello del client.</span><span class="sxs-lookup"><span data-stu-id="adc19-122">On the server, a security context is configured the same way as on the client.</span></span> <span data-ttu-id="adc19-123">Tuttavia, non è associato a un canale particolare.</span><span class="sxs-lookup"><span data-stu-id="adc19-123">However, it is not tied to any particular channel.</span></span> <span data-ttu-id="adc19-124">Al contrario, tutti i canali creati per il listener con il set di [**associazioni di sicurezza del messaggio del \_ contesto di sicurezza \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sono in grado di ricevere messaggi con uno dei contesti di sicurezza stabiliti nei canali del listener.</span><span class="sxs-lookup"><span data-stu-id="adc19-124">Instead, all channels created for the listener that has the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) set are capable of receiving messages with any of the security contexts that were established on channels of that listener.</span></span>

<span data-ttu-id="adc19-125">Quando un messaggio arriva su un canale che supporta i contesti di sicurezza, il contesto utilizzato da tale messaggio può essere ottenuto chiamando la funzione [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) con [**il \_ \_ contesto di \_ sicurezza \_ della proprietà del messaggio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span><span class="sxs-lookup"><span data-stu-id="adc19-125">When a message arrives on a channel that supports security contexts, the context used by that message can by obtained by calling the [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) function with the [**WS\_MESSAGE\_PROPERTY\_SECURITY\_CONTEXT**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="adc19-126">Il valore recuperato può essere usato con [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) e [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span><span class="sxs-lookup"><span data-stu-id="adc19-126">The retrieved value can be used with [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) and [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span></span>

## <a name="metadata"></a><span data-ttu-id="adc19-127">Metadati</span><span class="sxs-lookup"><span data-stu-id="adc19-127">Metadata</span></span>

<span data-ttu-id="adc19-128">La struttura del vincolo di sicurezza del messaggio del contesto di sicurezza WS viene utilizzata per estrarre i criteri del contesto di sicurezza dai metadati. [**\_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)</span><span class="sxs-lookup"><span data-stu-id="adc19-128">The [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) structure is used to extract the security context policy from metadata.</span></span> <span data-ttu-id="adc19-129">Per altre informazioni, vedere [importazione di metadati](metadata-import.md).</span><span class="sxs-lookup"><span data-stu-id="adc19-129">For more information, see [Metadata Import](metadata-import.md).</span></span>

<span data-ttu-id="adc19-130">I seguenti elementi API vengono utilizzati con i contesti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="adc19-130">The following API elements are used with security contexts.</span></span>

| <span data-ttu-id="adc19-131">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="adc19-131">Enumeration</span></span>                                                                    | <span data-ttu-id="adc19-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adc19-132">Description</span></span>                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="adc19-133">**\_ID della \_ proprietà del contesto di sicurezza WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="adc19-133">**WS\_SECURITY\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | <span data-ttu-id="adc19-134">Identifica una proprietà di un oggetto contesto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="adc19-134">Identifies a property of a security context object.</span></span> |



 



| <span data-ttu-id="adc19-135">Funzione</span><span class="sxs-lookup"><span data-stu-id="adc19-135">Function</span></span>                                                             | <span data-ttu-id="adc19-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adc19-136">Description</span></span>                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="adc19-137">**WsGetSecurityContextProperty**</span><span class="sxs-lookup"><span data-stu-id="adc19-137">**WsGetSecurityContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | <span data-ttu-id="adc19-138">Ottiene una proprietà del contesto di sicurezza specificato.</span><span class="sxs-lookup"><span data-stu-id="adc19-138">Gets a property of the specified security context.</span></span> |
| [<span data-ttu-id="adc19-139">**WsRevokeSecurityContext**</span><span class="sxs-lookup"><span data-stu-id="adc19-139">**WsRevokeSecurityContext**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | <span data-ttu-id="adc19-140">Revoca un contesto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="adc19-140">Revokes a security context.</span></span>                        |



 



| <span data-ttu-id="adc19-141">Handle</span><span class="sxs-lookup"><span data-stu-id="adc19-141">Handle</span></span>                                           | <span data-ttu-id="adc19-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adc19-142">Description</span></span>                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="adc19-143">\_contesto di sicurezza WS \_</span><span class="sxs-lookup"><span data-stu-id="adc19-143">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md) | <span data-ttu-id="adc19-144">Tipo opaco utilizzato per fare riferimento a un oggetto contesto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="adc19-144">An opaque type used to reference a security context object.</span></span> |



 



| <span data-ttu-id="adc19-145">Struttura</span><span class="sxs-lookup"><span data-stu-id="adc19-145">Structure</span></span>                                                               | <span data-ttu-id="adc19-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adc19-146">Description</span></span>                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="adc19-147">**\_proprietà del \_ contesto di sicurezza WS \_**</span><span class="sxs-lookup"><span data-stu-id="adc19-147">**WS\_SECURITY\_CONTEXT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | <span data-ttu-id="adc19-148">Definisce una proprietà di un [ \_ \_ contesto di sicurezza WS](ws-security-context.md).</span><span class="sxs-lookup"><span data-stu-id="adc19-148">Defines a property of a [WS\_SECURITY\_CONTEXT](ws-security-context.md).</span></span> |



 

 

 




