---
title: Enumerazioni del registro eventi di Windows
description: Nel registro eventi di Windows sono definite le enumerazioni seguenti.
ms.assetid: 2dd0e9ef-057b-4d0a-8b21-e7f14e5ae6e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c019a090d1a12e30948e5ed1f5672853caed848c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298592"
---
# <a name="windows-event-log-enumerations"></a>Enumerazioni del registro eventi di Windows

Nel registro eventi di Windows sono definite le enumerazioni seguenti.



| Enumerazione                                                                          | Descrizione                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo di \_ clock del canale evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_clock_type)                          | Definisce i valori che specificano il tipo di timestamp da utilizzare durante la registrazione del canale degli eventi.                                         |
| [**\_ID della \_ proprietà di configurazione del canale evt \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id)         | Definisce gli identificatori che identificano le proprietà di configurazione di un canale.                                                   |
| [**\_tipo di \_ isolamento \_ canale evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_isolation_type)                  | Definisce le autorizzazioni di accesso predefinite da applicare al canale.                                                                    |
| [**\_flag di \_ riferimento del canale evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_reference_flags)                | Definisce i valori che specificano il modo in cui viene fatto riferimento a un canale.                                                                       |
| [**\_tipo di \_ SID del canale evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_sid_type)                              | Definisce i valori che determinano se l'evento include l'ID di sicurezza (SID) dell'entità che ha registrato l'evento. |
| [**\_tipo di canale evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_type)                                       | Definisce il tipo di un canale.                                                                                                     |
| [**\_ID della \_ proprietà dei metadati dell'evento \_ evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_metadata_property_id)         | Definisce gli identificatori che identificano le proprietà dei metadati di una definizione di evento.                                              |
| [**\_ID della \_ proprietà dell'evento evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_property_id)               | Definisce i valori che determinano le informazioni di query da recuperare.                                                               |
| [**\_flag EXPORTLOG \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_exportlog_flags)                                 | Definisce i valori che indicano se gli eventi provengono da un canale o da un file di log.                                                   |
| [**\_ \_ flag messaggio formato \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_format_message_flags)                      | Definisce i valori che specificano la stringa di messaggio dall'evento da formattare.                                                       |
| [**\_ID della \_ proprietà di log evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_log_property_id)                                | Definisce gli identificatori che identificano le proprietà dei metadati del file di log di un canale o di un file di log.                                   |
| [**\_classe di accesso evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_login_class)                                         | Definisce i tipi di metodi di connessione che è possibile utilizzare per connettersi al computer remoto.                                             |
| [**EVT \_ \_ flag di log aperti \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_open_log_flags)                                  | Definisce i valori che specificano se aprire un canale o un file di log esportato.                                                    |
| [**\_ID della \_ proprietà dei metadati del server di pubblicazione evt \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_publisher_metadata_property_id) | Definisce gli identificatori che identificano le proprietà dei metadati di un provider.                                                       |
| [**\_flag di query evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)                                         | Definisce i valori che specificano come restituire i risultati della query e se si esegue una query su un canale o un file di log.           |
| [**\_ID della \_ proprietà di query evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_property_id)                            | Definisce gli identificatori che identificano le informazioni di query che è possibile recuperare.                                                 |
| [**\_flag del \_ contesto di rendering evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_context_flags)                      | Definisce i valori che specificano il tipo di informazioni a cui accedere dall'evento.                                                  |
| [**\_flag di rendering evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_flags)                                       | Definisce i valori che specificano gli elementi di cui eseguire il rendering.                                                                                    |
| [**\_flag di \_ accesso \_ RPC evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_rpc_login_flags)                                | Definisce i tipi di autenticazione che è possibile utilizzare per autenticare l'utente durante la connessione a un computer remoto.                |
| [**\_flag di ricerca evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_seek_flags)                                           | Definisce la posizione relativa nel set di risultati da cui eseguire la ricerca.                                                                |
| [**\_flag sottoscrizioni evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_flags)                                 | Definisce i valori possibili che specificano quando iniziare a sottoscrivere gli eventi.                                                      |
| [**\_azione di \_ notifica \_ sottoscrizione evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_notify_action)                | Definisce i possibili tipi di dati che il servizio di sottoscrizione può recapitare al callback.                                     |
| [**\_ID della \_ proprietà di sistema evt \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_system_property_id)                          | Definisce gli identificatori che identificano le proprietà definite dal sistema di un evento.                                                   |
| [**\_tipo Variant \_ evt**](/windows/desktop/api/WinEvt/ne-winevt-evt_variant_type)                                       | Definisce i tipi di dati possibili di un elemento di dati Variant.                                                                            |



 

 

 




