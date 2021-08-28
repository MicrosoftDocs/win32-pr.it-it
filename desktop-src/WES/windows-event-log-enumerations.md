---
title: Windows Enumerazioni del log eventi
description: Windows Registro eventi definisce le enumerazioni seguenti.
ms.assetid: 2dd0e9ef-057b-4d0a-8b21-e7f14e5ae6e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4fa05f1d9115c7888b3b796a90dd6a07019ad5158764bd91c80f20d96c71e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904031"
---
# <a name="windows-event-log-enumerations"></a>Windows Enumerazioni del log eventi

Windows Registro eventi definisce le enumerazioni seguenti.



| Enumerazione                                                                          | Descrizione                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DI \_ CLOCK DEL \_ CANALE EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_clock_type)                          | Definisce i valori che specificano il tipo di timestamp da utilizzare per la registrazione del canale eventi.                                         |
| [**ID PROPRIETÀ DI \_ \_ CONFIGURAZIONE DEL \_ CANALE \_ EVT**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_config_property_id)         | Definisce gli identificatori che identificano le proprietà di configurazione di un canale.                                                   |
| [**TIPO DI ISOLAMENTO DEL CANALE EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_isolation_type)                  | Definisce le autorizzazioni di accesso predefinite da applicare al canale.                                                                    |
| [**FLAG DI RIFERIMENTO DEL CANALE EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_reference_flags)                | Definisce i valori che specificano come viene fatto riferimento a un canale.                                                                       |
| [**TIPO DI \_ \_ SID CANALE EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_sid_type)                              | Definisce i valori che determinano se l'evento include l'identificatore di sicurezza (SID) dell'entità che ha registrato l'evento. |
| [**TIPO DI \_ CANALE EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_channel_type)                                       | Definisce il tipo di un canale.                                                                                                     |
| [**ID PROPRIETÀ METADATI EVENTO EVT \_ \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_metadata_property_id)         | Definisce gli identificatori che identificano le proprietà dei metadati di una definizione di evento.                                              |
| [**ID PROPRIETÀ EVENTO EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_event_property_id)               | Definisce i valori che determinano le informazioni sulla query da recuperare.                                                               |
| [**FLAG EVT \_ EXPORTLOG \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_exportlog_flags)                                 | Definisce valori che indicano se gli eventi provengono da un canale o da un file di log.                                                   |
| [**FLAG DI MESSAGGIO IN FORMATO EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_format_message_flags)                      | Definisce i valori che specificano la stringa di messaggio dall'evento da formattare.                                                       |
| [**ID PROPRIETÀ LOG EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_log_property_id)                                | Definisce gli identificatori che identificano le proprietà dei metadati del file di log di un canale o di un file di log.                                   |
| [**CLASSE LOGIN \_ EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_login_class)                                         | Definisce i tipi di metodi di connessione che è possibile usare per connettersi al computer remoto.                                             |
| [**FLAG DI LOG APERTI EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_open_log_flags)                                  | Definisce i valori che specificano se aprire un canale o un file di log esportato.                                                    |
| [**ID PROPRIETÀ METADATI SERVER DI PUBBLICAZIONE EVT \_ \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_publisher_metadata_property_id) | Definisce gli identificatori che identificano le proprietà dei metadati di un provider.                                                       |
| [**FLAG DI QUERY EVT \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags)                                         | Definisce i valori che specificano come restituire i risultati della query e se si esegue una query su un canale o un file di log.           |
| [**ID PROPRIETÀ QUERY EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_property_id)                            | Definisce gli identificatori che identificano le informazioni di query che è possibile recuperare.                                                 |
| [**FLAG DI CONTESTO DI RENDERING EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_context_flags)                      | Definisce i valori che specificano il tipo di informazioni a cui accedere dall'evento.                                                  |
| [**FLAG DI RENDERING EVT \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_render_flags)                                       | Definisce i valori che specificano gli elementi di cui eseguire il rendering.                                                                                    |
| [**FLAG DI ACCESSO RPC EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_rpc_login_flags)                                | Definisce i tipi di autenticazione che è possibile usare per autenticare l'utente durante la connessione a un computer remoto.                |
| [**FLAG DI RICERCA EVT \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_seek_flags)                                           | Definisce la posizione relativa nel set di risultati da cui eseguire la ricerca.                                                                |
| [**FLAG DI SOTTOSCRIZIONE EVT \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_flags)                                 | Definisce i valori possibili che specificano quando avviare la sottoscrizione agli eventi.                                                      |
| [**AZIONE NOTIFICA SOTTOSCRIZIONE EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_subscribe_notify_action)                | Definisce i possibili tipi di dati che il servizio di sottoscrizione può recapitare al callback.                                     |
| [**ID PROPRIETÀ DI SISTEMA EVT \_ \_ \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_system_property_id)                          | Definisce gli identificatori che identificano le proprietà definite dal sistema di un evento.                                                   |
| [**TIPO VARIANT \_ EVT \_**](/windows/desktop/api/WinEvt/ne-winevt-evt_variant_type)                                       | Definisce i tipi di dati possibili di un elemento di dati variant.                                                                            |



 

 

 




