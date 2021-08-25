---
title: Configurazione dell'installazione
description: La configurazione dell'installazione richiede privilegi di amministratore ed è persistente tra i riavvii.
ms.assetid: 96e9c069-829b-4615-b94b-3761bc541440
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d59065ff34e7998d9df0503f6ae7503d9d402def6053f8176ba5af5b6a9efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996118"
---
# <a name="setup-configuration"></a>Configurazione dell'installazione

La configurazione dell'installazione richiede privilegi di amministratore ed è persistente tra i riavvii. In genere, un'applicazione di installazione in esecuzione con privilegi di amministratore esegue tale configurazione permanente durante l'installazione in modo che le applicazioni possano quindi essere eseguite con privilegi inferiori, anche se la configurazione permanente può essere eseguita in qualsiasi momento. La configurazione dell'installazione può includere una delle quattro attività seguenti:

-   Creazione di una prenotazione URL. L'API HTTP consente all'applicazione di installazione di riservare prefissi URL per le code di richieste associate ad applicazioni specifiche. Per riservare un URL, l'applicazione di installazione chiama la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con il parametro *ConfigId* impostato su **HttpServiceConfigUrlAclInfo** e passa un puntatore nel *parametro pConfigInformation* a una struttura [**HTTP SERVICE CONFIG \_ \_ \_ URLACL \_ SET**](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set) contenente le informazioni di registrazione. Per altre informazioni, vedere [Prenotazioni,](namespace-reservations-registrations-and-routing.md)registrazioni e routing dello spazio dei nomi .
-   Configurazione di SSL. Per configurare SSL, l'amministratore chiama la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con il parametro *ConfigId* impostato su **HttpServiceConfigSSLCertInfo** e passa un puntatore nel *parametro pConfigInformation* a una struttura [**HTTP SERVICE CONFIG SSL \_ \_ \_ \_ SET**](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set) contenente le informazioni sul certificato SSL.
-   Impostazione di altre configurazioni persistenti a livello di server HTTP, ad esempio gli indirizzi IP su cui il server HTTP sarà in ascolto e il valore di timeout a livello di server. Vedere [Elenco di ascolto IP e](ip-listen-list.md) TIMEOUT CONFIGURAZIONE SERVIZIO HTTP [**\_ \_ \_ \_ SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set).

 

 




