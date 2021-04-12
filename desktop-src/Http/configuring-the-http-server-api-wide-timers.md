---
title: Configurazione dei timer wide dell'API del server HTTP
description: Configurazione dei timer wide dell'API del server HTTP
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae91abb1c89419e99fa13273cd55b0783df3906a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221470"
---
# <a name="configuring-the-http-server-api-wide-timers"></a>Configurazione dei timer wide dell'API del server HTTP

I timer **HeaderWait** e **IdleConnection** a livello di API del server HTTP sono configurati chiamando la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) della versione 1,0. Il parametro *ConfigId* è impostato su **HttpServiceConfigTimeout** e il parametro *pConfigInformation* specifica la struttura del set di [**\_ timeout della configurazione del servizio \_ \_ \_ http**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) che contiene il timer impostato e il valore per il timer.

La configurazione dei timeout a livello di API del server HTTP richiede privilegi amministrativi, tuttavia non viene eseguita una query su di essi. Queste configurazioni sono impostate per tutte le applicazioni nel computer e vengono mantenute quando il servizio HTTP viene riavviato o il computer viene riavviato. Per eseguire query sui timeout a livello di API del server HTTP esistente, l'applicazione chiama [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).

 

 




