---
description: Monitorare le notifiche degli eventi di sistema dai programmi eseguiti sui computer portatili per determinare la latenza e la larghezza di banda della connessione di rete. Scrivi applicazioni ottimizzate per il mobile computing e le LAN a latenza elevata.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Servizio di notifica eventi di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968199"
---
# <a name="system-event-notification-service"></a>Servizio di notifica eventi di sistema

## <a name="purpose"></a>Scopo

Le applicazioni progettate per l'uso da parte degli utenti mobili richiedono un set univoco di notifiche e funzioni di connettività. In passato queste singole applicazioni erano necessarie per implementare queste funzionalità internamente. Il servizio di notifica eventi di sistema (SENS) offre ora queste funzionalità nel sistema operativo, creando una connettività uniforme e un'interfaccia di notifica per le applicazioni. L'uso degli sviluppatori di SENS può determinare la larghezza di banda di connessione e le informazioni sulla latenza all'interno dell'applicazione e ottimizzare l'operazione dell'applicazione in base a tali condizioni.

## <a name="where-applicable"></a>Se applicabile

Le funzioni di connettività e le notifiche di SENS sono utili per le applicazioni scritte per computer portatili o computer connessi a reti locali a latenza elevata.

## <a name="developer-audience"></a>Sviluppatori

Questo documento è destinato agli sviluppatori di software che sviluppano applicazioni per il mobile computing e le reti locali a latenza elevata. Questo documento fornisce un riferimento completo di tutte le parti del servizio di notifica degli eventi di sistema, inclusi l'oggetto SENS e i metodi di supporto.

## <a name="run-time-requirements"></a>Requisiti di runtime

Richiede Microsoft Windows XP o versione successiva. Per informazioni sui sistemi operativi necessari per usare un'interfaccia o una funzione specifica, vedere la sezione requisiti della documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                              | Descrizione                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Overview](about-system-event-notification-service.md)<br/> | Informazioni generali sul servizio di notifica eventi di sistema.<br/>               |
| [Riferimento](sens-reference.md)<br/>                         | Documentazione relativa a metodi e interfacce del servizio di notifica degli eventi di sistema.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IEventSubscription**](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
