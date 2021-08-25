---
title: Configurazione dei timer a livello di API del server HTTP
description: Configurazione dei timer a livello di API del server HTTP
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0eb5fc40bedd51884830893673b3bae2341a21110fa2c3b33878dba7a4aef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047351"
---
# <a name="configuring-the-http-server-api-wide-timers"></a>Configurazione dei timer a livello di API del server HTTP

I timer **HeaderWait** e **IdleConnection** a livello di API del server HTTP vengono configurati chiamando la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) versione 1.0. Il *parametro ConfigId* è impostato su **HttpServiceConfigTimeout** e il parametro *pConfigInformation* specifica la struttura [**HTTP SERVICE CONFIG TIMEOUT \_ \_ \_ \_ SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) che contiene il timer impostato e il valore per il timer.

La configurazione dei timeout a livello di API del server HTTP richiede privilegi amministrativi, ma non l'esecuzione di query su di essi. Queste configurazioni vengono impostate per tutte le applicazioni nel computer e vengono mantenute quando il servizio HTTP viene riavviato o il computer viene riavviato. Per eseguire query sui timeout esistenti a livello di API del server HTTP, l'applicazione chiama [**HttpQueryServiceConfiguration.**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)

 

 




