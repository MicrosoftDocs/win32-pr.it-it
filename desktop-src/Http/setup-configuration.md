---
title: Configurazione del programma di installazione
description: Per la configurazione dell'installazione sono necessari privilegi di amministratore ed è persistente tra i riavvii.
ms.assetid: 96e9c069-829b-4615-b94b-3761bc541440
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43b543bfc81f963341d7b5f690f4b40312ee420
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515484"
---
# <a name="setup-configuration"></a>Configurazione del programma di installazione

Per la configurazione dell'installazione sono necessari privilegi di amministratore ed è persistente tra i riavvii. In genere, un'applicazione di installazione eseguita con privilegi di amministratore esegue tale configurazione persistente durante l'installazione, in modo che le applicazioni possano quindi essere eseguite con privilegi inferiori, sebbene la configurazione permanente possa essere eseguita in qualsiasi momento. La configurazione del programma di installazione può includere le quattro attività seguenti:

-   Creazione di una prenotazione URL. L'API HTTP consente all'applicazione di installazione di riservare i prefissi URL per le code di richiesta associate a applicazioni specifiche. Per riservare un URL, l'applicazione di installazione chiama la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con il parametro *ConfigId* impostato su **HttpServiceConfigUrlAclInfo** e passa un puntatore nel parametro *pConfigInformation* a una struttura del [**\_ \_ \_ \_ set di URLACL del servizio http**](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set) che contiene le informazioni di registrazione. Per altre informazioni, vedere [prenotazioni per spazi dei nomi, registrazioni e routing](namespace-reservations-registrations-and-routing.md).
-   Configurazione di SSL. Per configurare SSL, l'amministratore chiama la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con il parametro *ConfigId* impostato su **HttpServiceConfigSSLCertInfo** e passa un puntatore nel parametro *pConfigInformation* a una struttura del [**\_ \_ \_ \_ set SSL del servizio http di configurazione**](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set) che contiene le informazioni sul certificato SSL.
-   Impostazione di altre configurazioni persistenti a livello di server HTTP, ad esempio gli indirizzi IP su cui il server HTTP resterà in ascolto e il valore di timeout a livello di server. Vedere l' [elenco di ascolto IP](ip-listen-list.md) e il [**timeout della configurazione del servizio http \_ \_ \_ \_ impostati**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set).

 

 




