---
title: Identità endpoint
description: I tipi definiti in questa sezione vengono utilizzati per definire l'identità di sicurezza di un indirizzo endpoint.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Endpoint Identity Web Services per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395370"
---
# <a name="endpoint-identity"></a><span data-ttu-id="01e6a-106">Identità endpoint</span><span class="sxs-lookup"><span data-stu-id="01e6a-106">Endpoint Identity</span></span>

<span data-ttu-id="01e6a-107">I tipi definiti in questa sezione vengono utilizzati per definire l'identità di sicurezza di un indirizzo endpoint.</span><span class="sxs-lookup"><span data-stu-id="01e6a-107">The types defined in this section are used to define the security identity of an endpoint address.</span></span>

<span data-ttu-id="01e6a-108">Gli elementi API seguenti fanno parte del rientro dell'endpoint:</span><span class="sxs-lookup"><span data-stu-id="01e6a-108">The following API elements are part of endpoint indentity:</span></span>



| <span data-ttu-id="01e6a-109">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="01e6a-109">Enumeration</span></span>                                                       | <span data-ttu-id="01e6a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01e6a-110">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01e6a-111">**\_ \_ tipo identità endpoint \_ WS**</span><span class="sxs-lookup"><span data-stu-id="01e6a-111">**WS\_ENDPOINT\_IDENTITY\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | <span data-ttu-id="01e6a-112">Tipo di identità dell'endpoint, utilizzato come selettore per sottotipi di [**identità WS \_ endpoint \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span><span class="sxs-lookup"><span data-stu-id="01e6a-112">The type of the endpoint identity, used as a selector for subtypes of [**WS\_ENDPOINT\_IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span></span> |



 



| <span data-ttu-id="01e6a-113">Struttura</span><span class="sxs-lookup"><span data-stu-id="01e6a-113">Structure</span></span>                                                               | <span data-ttu-id="01e6a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01e6a-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01e6a-115">**\_ \_ identità endpoint WS \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="01e6a-115">**WS\_CERT\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | <span data-ttu-id="01e6a-116">Tipo per l'identità dell'endpoint del certificato.</span><span class="sxs-lookup"><span data-stu-id="01e6a-116">The type for certificate endpoint identity .</span></span>                                                 |
| [<span data-ttu-id="01e6a-117">**\_ \_ identità endpoint DNS \_ WS**</span><span class="sxs-lookup"><span data-stu-id="01e6a-117">**WS\_DNS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | <span data-ttu-id="01e6a-118">Tipo per specificare un'identità dell'endpoint rappresentata da un nome DNS.</span><span class="sxs-lookup"><span data-stu-id="01e6a-118">The type for specifying an endpoint identity represented by a DNS name.</span></span>                      |
| [<span data-ttu-id="01e6a-119">**\_identità endpoint \_ WS**</span><span class="sxs-lookup"><span data-stu-id="01e6a-119">**WS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | <span data-ttu-id="01e6a-120">Tipo di base per tutte le identità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="01e6a-120">The base type for all endpoint identities.</span></span>                                                   |
| [<span data-ttu-id="01e6a-121">**\_ \_ identità endpoint WS \_ RSA**</span><span class="sxs-lookup"><span data-stu-id="01e6a-121">**WS\_RSA\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | <span data-ttu-id="01e6a-122">Digitare per l'identità dell'endpoint RSA.</span><span class="sxs-lookup"><span data-stu-id="01e6a-122">Type for RSA endpoint identity.</span></span>                                                              |
| [<span data-ttu-id="01e6a-123">**\_identità dell' \_ endpoint WS SPN \_**</span><span class="sxs-lookup"><span data-stu-id="01e6a-123">**WS\_SPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | <span data-ttu-id="01e6a-124">Tipo per specificare un'identità dell'endpoint rappresentata da un SPN (nome dell'entità servizio).</span><span class="sxs-lookup"><span data-stu-id="01e6a-124">The type for specifying an endpoint identity represented by an SPN (service principal name).</span></span> |
| [<span data-ttu-id="01e6a-125">**\_ \_ identità endpoint sconosciuta \_ WS**</span><span class="sxs-lookup"><span data-stu-id="01e6a-125">**WS\_UNKNOWN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | <span data-ttu-id="01e6a-126">Tipo per un'identità dell'endpoint sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="01e6a-126">The type for an unknown endpoint identity.</span></span>                                                   |
| [<span data-ttu-id="01e6a-127">**identità dell'endpoint di WS \_ UPN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="01e6a-127">**WS\_UPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | <span data-ttu-id="01e6a-128">Tipo per specificare un'identità dell'endpoint rappresentata da un UPN (nome dell'entità utente).</span><span class="sxs-lookup"><span data-stu-id="01e6a-128">The type for specifying an endpoint identity represented by a UPN (user principal name).</span></span>     |



 

 

 




