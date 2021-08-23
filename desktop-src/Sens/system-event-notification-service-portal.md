---
description: Monitorare le notifiche degli eventi di sistema dai programmi eseguiti nei computer mobili per determinare la larghezza di banda e la latenza della connessione di rete. Scrivere applicazioni ottimizzate per il mobile computing e reti LAN a latenza elevata.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Servizio di notifica eventi di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e76ee51ea0e7a341f0205528e9083cb1f6c0420f941025ec71c32c9154850b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003929"
---
# <a name="system-event-notification-service"></a>Servizio di notifica eventi di sistema

## <a name="purpose"></a>Scopo

Le applicazioni progettate per l'uso da parte degli utenti mobili richiedono un set univoco di funzioni e notifiche di connettività. In passato queste singole applicazioni erano necessarie per implementare queste funzionalità internamente. System Event Notification Service (SENS) offre ora queste funzionalità nel sistema operativo, creando un'interfaccia di connettività e notifica uniforme per le applicazioni. Gli sviluppatori SENS possono determinare la larghezza di banda della connessione e le informazioni sulla latenza dall'interno dell'applicazione e ottimizzare il funzionamento dell'applicazione in base a tali condizioni.

## <a name="where-applicable"></a>Se applicabile

Le funzioni di connettività e le notifiche di SENS sono utili per le applicazioni scritte per computer mobili o computer connessi a reti locali a latenza elevata.

## <a name="developer-audience"></a>Sviluppatori

Questo documento è destinato agli sviluppatori di software che sviluppano applicazioni per il mobile computing e reti locali a latenza elevata. Questo documento fornisce un riferimento completo di tutte le parti del servizio di notifica degli eventi di sistema, inclusi l'oggetto SENS e i metodi di supporto.

## <a name="run-time-requirements"></a>Requisiti di runtime

Richiede Microsoft Windows XP o versione successiva. Per informazioni sui sistemi operativi necessari per usare una determinata interfaccia o funzione, vedere la sezione Requisiti della documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                              | Descrizione                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Overview](about-system-event-notification-service.md)<br/> | Informazioni generali sul Servizio notifica eventi di sistema.<br/>               |
| [Riferimento](sens-reference.md)<br/>                         | Documentazione dei metodi e delle interfacce del servizio di notifica eventi di sistema.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IEventSubscription**](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
