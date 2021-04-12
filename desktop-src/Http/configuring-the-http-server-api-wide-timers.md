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
# <a name="configuring-the-http-server-api-wide-timers"></a><span data-ttu-id="ee7d6-103">Configurazione dei timer wide dell'API del server HTTP</span><span class="sxs-lookup"><span data-stu-id="ee7d6-103">Configuring the HTTP Server API Wide Timers</span></span>

<span data-ttu-id="ee7d6-104">I timer **HeaderWait** e **IdleConnection** a livello di API del server HTTP sono configurati chiamando la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) della versione 1,0.</span><span class="sxs-lookup"><span data-stu-id="ee7d6-104">The HTTP Server API-wide **HeaderWait** and **IdleConnection** timers are configured by calling the version 1.0 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function.</span></span> <span data-ttu-id="ee7d6-105">Il parametro *ConfigId* è impostato su **HttpServiceConfigTimeout** e il parametro *pConfigInformation* specifica la struttura del set di [**\_ timeout della configurazione del servizio \_ \_ \_ http**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) che contiene il timer impostato e il valore per il timer.</span><span class="sxs-lookup"><span data-stu-id="ee7d6-105">The *ConfigId* parameter is set to **HttpServiceConfigTimeout** and the *pConfigInformation* parameter specifies the [**HTTP\_SERVICE\_CONFIG\_TIMEOUT\_SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) structure that contains the timer that is set and the value for the timer.</span></span>

<span data-ttu-id="ee7d6-106">La configurazione dei timeout a livello di API del server HTTP richiede privilegi amministrativi, tuttavia non viene eseguita una query su di essi.</span><span class="sxs-lookup"><span data-stu-id="ee7d6-106">Configuring the HTTP Server API-wide timeouts requires administrative privileges, however querying them does not.</span></span> <span data-ttu-id="ee7d6-107">Queste configurazioni sono impostate per tutte le applicazioni nel computer e vengono mantenute quando il servizio HTTP viene riavviato o il computer viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="ee7d6-107">These configurations are set for all applications on the computer and they persist when the HTTP service is restarted or the computer is restarted.</span></span> <span data-ttu-id="ee7d6-108">Per eseguire query sui timeout a livello di API del server HTTP esistente, l'applicazione chiama [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).</span><span class="sxs-lookup"><span data-stu-id="ee7d6-108">To query existing HTTP Server API-wide timeouts, the application calls [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).</span></span>

 

 




