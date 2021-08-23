---
title: Listener
description: Un listener viene usato dal client per accettare un canale in ingresso da un servizio.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Servizi Web listener per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26a2f9951dedefd5fb686de7935a76ce3b6ef24dcea140d5414b713e89ad1f1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026379"
---
# <a name="listener"></a>Listener

Un listener viene usato dal client per accettare un canale [in ingresso](channel.md) da un servizio.

Per creare un listner, specificare il tipo di canale come [](binding.md) valore di enumerazione [**WS \_ CHANNEL \_ TYPE,**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) le informazioni di associazione e [l'URL](url.md) su cui restare in ascolto.


Per avviare l'ascolto sull'URL, chiamare la [**funzione WsOpenListener.**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)

Per accettare le comunicazioni in ingresso, [**chiamare WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).

Per annullare le operazioni di I/O in sospeso per un listener, [**chiamare WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).

Per informazioni sulle transizioni di stato per un listener, vedere [**l'enumerazione WS \_ LISTENER \_ STATE.**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

I callback seguenti fanno parte del listener:

-   [**CALLBACK DEL \_ LISTENER DI \_ INTERRUZIONE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**CALLBACK DEL CANALE WS \_ \_ ACCEPT \_**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**CALLBACK \_ DEL LISTENER DI CHIUSURA WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ FOR \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**CALLBACK \_ DEL \_ \_ LISTENER WS CREATE**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**CALLBACK \_ DEL LISTENER GRATUITO WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**CALLBACK DELLE \_ PROPRIETÀ \_ DEL \_ \_ LISTENER WS GET**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**CALLBACK \_ DEL \_ \_ LISTENER WS OPEN**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**CALLBACK \_ DEL LISTENER DI \_ REIMPOSTAZIONE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**CALLBACK DELLE \_ PROPRIETÀ \_ DEL \_ \_ LISTENER WS SET**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

Le enumerazioni seguenti fanno parte del listener:

-   [**VERSIONE \_ IP WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**ID PROPRIETÀ LISTENER WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**STATO DEL LISTENER WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

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

L'handle seguente fa parte del listener:

-   [WS \_ LISTENER](ws-listener.md)

Le strutture seguenti fanno parte del listener:

-   [**CALLBACK DEL \_ LISTENER PERSONALIZZATO \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**\_SOTTOSTRINGHE DELL'AGENTE UTENTE NON \_ \_ \_ CONSENTITE DI WS**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**NOMI HOST WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**PROPRIETÀ DEL LISTENER WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**PROPRIETÀ LISTENER WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




