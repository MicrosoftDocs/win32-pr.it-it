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
# <a name="listener"></a>Listener

Un listener viene utilizzato dal client per accettare un [canale](channel.md) in ingresso da un servizio.

Per creare un listener, è necessario specificare il tipo di canale come valore di enumerazione del [**\_ \_ tipo di canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , le informazioni di [Binding](binding.md) e l' [URL](url.md) su cui restare in ascolto.


Per iniziare l'ascolto sull'URL, chiamare la funzione [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) .

Per accettare le comunicazioni in ingresso, chiamare [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).

Per annullare l'i/o in sospeso per un listener, chiamare [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).

Per informazioni sulle transizioni di stato per un listener, vedere l' [**enumerazione \_ \_ dello stato del listener WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .

I callback seguenti fanno parte del listener:

-   [**\_callback del \_ listener WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**\_ \_ callback canale WS \_ Accept**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**\_callback del \_ listener WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ Crea \_ canale \_ per \_ \_ callback listener**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**\_callback WS crea \_ listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**CALLBACK di WS \_ Free \_ listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**\_callback della \_ proprietà del listener WS Get \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**CALLBACK di WS \_ Open \_ listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**CALLBACK di WS \_ Reset \_ listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**\_callback della \_ proprietà del listener set \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

Le enumerazioni seguenti fanno parte del listener:

-   [**versione di WS \_ IP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**\_ID della \_ proprietà del listener WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**\_stato del listener WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

Le funzioni seguenti fanno parte del listener:

-   [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [**WsCloseListener**](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [**WsFreeListener**](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [**WsGetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [**WsResetListener**](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [**WsSetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

Il seguente handle fa parte del listener:

-   [\_listener WS](ws-listener.md)

Le strutture seguenti fanno parte del listener:

-   [**\_callback di \_ listener \_ personalizzati WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**\_ \_ \_ sottostringhe agente utente non consentito WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**\_nomi host \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**\_proprietà del listener WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**\_Proprietà listener \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




