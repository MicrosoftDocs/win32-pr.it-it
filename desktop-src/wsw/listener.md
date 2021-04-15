---
title: Listener
description: Un listener viene utilizzato dal client per accettare un canale in ingresso da un servizio.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Servizi Web listener per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399955"
---
# <a name="listener"></a><span data-ttu-id="c30aa-106">Listener</span><span class="sxs-lookup"><span data-stu-id="c30aa-106">Listener</span></span>

<span data-ttu-id="c30aa-107">Un listener viene utilizzato dal client per accettare un [canale](channel.md) in ingresso da un servizio.</span><span class="sxs-lookup"><span data-stu-id="c30aa-107">A listener is used by the client to accept an incoming [channel](channel.md) from a service.</span></span>

<span data-ttu-id="c30aa-108">Per creare un listener, è necessario specificare il tipo di canale come valore di enumerazione del [**\_ \_ tipo di canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , le informazioni di [Binding](binding.md) e l' [URL](url.md) su cui restare in ascolto.</span><span class="sxs-lookup"><span data-stu-id="c30aa-108">To create a listner, you specify the channel type as a [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) enumeration value, the [binding](binding.md) information, and the [URL](url.md) to listen on.</span></span>


<span data-ttu-id="c30aa-109">Per iniziare l'ascolto sull'URL, chiamare la funzione [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) .</span><span class="sxs-lookup"><span data-stu-id="c30aa-109">To start listening on the URL, call the [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) function.</span></span>

<span data-ttu-id="c30aa-110">Per accettare le comunicazioni in ingresso, chiamare [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span><span class="sxs-lookup"><span data-stu-id="c30aa-110">To accept incoming communications, call [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span></span>

<span data-ttu-id="c30aa-111">Per annullare l'i/o in sospeso per un listener, chiamare [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span><span class="sxs-lookup"><span data-stu-id="c30aa-111">To cancel pending IO for a listener, call [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span></span>

<span data-ttu-id="c30aa-112">Per informazioni sulle transizioni di stato per un listener, vedere l' [**enumerazione \_ \_ dello stato del listener WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .</span><span class="sxs-lookup"><span data-stu-id="c30aa-112">For information on the state transitions for a listener, see the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) enumeration.</span></span>

<span data-ttu-id="c30aa-113">I callback seguenti fanno parte del listener:</span><span class="sxs-lookup"><span data-stu-id="c30aa-113">The following callbacks are part of the listener:</span></span>

-   [<span data-ttu-id="c30aa-114">**\_callback del \_ listener WS Abort \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-114">**WS\_ABORT\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [<span data-ttu-id="c30aa-115">**\_ \_ callback canale WS \_ Accept**</span><span class="sxs-lookup"><span data-stu-id="c30aa-115">**WS\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [<span data-ttu-id="c30aa-116">**\_callback del \_ listener WS Close \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-116">**WS\_CLOSE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [<span data-ttu-id="c30aa-117">**WS \_ Crea \_ canale \_ per \_ \_ callback listener**</span><span class="sxs-lookup"><span data-stu-id="c30aa-117">**WS\_CREATE\_CHANNEL\_FOR\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [<span data-ttu-id="c30aa-118">**\_callback WS crea \_ listener \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-118">**WS\_CREATE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [<span data-ttu-id="c30aa-119">**CALLBACK di WS \_ Free \_ listener \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-119">**WS\_FREE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [<span data-ttu-id="c30aa-120">**\_callback della \_ proprietà del listener WS Get \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-120">**WS\_GET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [<span data-ttu-id="c30aa-121">**CALLBACK di WS \_ Open \_ listener \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-121">**WS\_OPEN\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [<span data-ttu-id="c30aa-122">**CALLBACK di WS \_ Reset \_ listener \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-122">**WS\_RESET\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [<span data-ttu-id="c30aa-123">**\_callback della \_ proprietà del listener set \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-123">**WS\_SET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

<span data-ttu-id="c30aa-124">Le enumerazioni seguenti fanno parte del listener:</span><span class="sxs-lookup"><span data-stu-id="c30aa-124">The following enumerations are part of the listener:</span></span>

-   [<span data-ttu-id="c30aa-125">**versione di WS \_ IP \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-125">**WS\_IP\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [<span data-ttu-id="c30aa-126">**\_ID della \_ proprietà del listener WS \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-126">**WS\_LISTENER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [<span data-ttu-id="c30aa-127">**\_stato del listener WS \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-127">**WS\_LISTENER\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

<span data-ttu-id="c30aa-128">Le funzioni seguenti fanno parte del listener:</span><span class="sxs-lookup"><span data-stu-id="c30aa-128">The following functions are part of the listener:</span></span>

-   [<span data-ttu-id="c30aa-129">**WsAbortListener**</span><span class="sxs-lookup"><span data-stu-id="c30aa-129">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [<span data-ttu-id="c30aa-130">**WsAcceptChannel**</span><span class="sxs-lookup"><span data-stu-id="c30aa-130">**WsAcceptChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [<span data-ttu-id="c30aa-131">**WsCloseListener**</span><span class="sxs-lookup"><span data-stu-id="c30aa-131">**WsCloseListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [<span data-ttu-id="c30aa-132">**WsCreateListener**</span><span class="sxs-lookup"><span data-stu-id="c30aa-132">**WsCreateListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [<span data-ttu-id="c30aa-133">**WsFreeListener**</span><span class="sxs-lookup"><span data-stu-id="c30aa-133">**WsFreeListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [<span data-ttu-id="c30aa-134">**WsGetListenerProperty**</span><span class="sxs-lookup"><span data-stu-id="c30aa-134">**WsGetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [<span data-ttu-id="c30aa-135">**WsOpenListener**</span><span class="sxs-lookup"><span data-stu-id="c30aa-135">**WsOpenListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [<span data-ttu-id="c30aa-136">**WsResetListener**</span><span class="sxs-lookup"><span data-stu-id="c30aa-136">**WsResetListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [<span data-ttu-id="c30aa-137">**WsSetListenerProperty**</span><span class="sxs-lookup"><span data-stu-id="c30aa-137">**WsSetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

<span data-ttu-id="c30aa-138">Il seguente handle fa parte del listener:</span><span class="sxs-lookup"><span data-stu-id="c30aa-138">The following handle is part of the listener:</span></span>

-   [<span data-ttu-id="c30aa-139">\_listener WS</span><span class="sxs-lookup"><span data-stu-id="c30aa-139">WS\_LISTENER</span></span>](ws-listener.md)

<span data-ttu-id="c30aa-140">Le strutture seguenti fanno parte del listener:</span><span class="sxs-lookup"><span data-stu-id="c30aa-140">The following structures are part of the listener:</span></span>

-   [<span data-ttu-id="c30aa-141">**\_callback di \_ listener \_ personalizzati WS**</span><span class="sxs-lookup"><span data-stu-id="c30aa-141">**WS\_CUSTOM\_LISTENER\_CALLBACKS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [<span data-ttu-id="c30aa-142">**\_ \_ \_ sottostringhe agente utente non consentito WS \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-142">**WS\_DISALLOWED\_USER\_AGENT\_SUBSTRINGS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [<span data-ttu-id="c30aa-143">**\_nomi host \_ WS**</span><span class="sxs-lookup"><span data-stu-id="c30aa-143">**WS\_HOST\_NAMES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [<span data-ttu-id="c30aa-144">**\_proprietà del listener WS \_**</span><span class="sxs-lookup"><span data-stu-id="c30aa-144">**WS\_LISTENER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [<span data-ttu-id="c30aa-145">**\_Proprietà listener \_ WS**</span><span class="sxs-lookup"><span data-stu-id="c30aa-145">**WS\_LISTENER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




