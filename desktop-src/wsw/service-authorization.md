---
title: Autorizzazione servizio
description: Un'applicazione può implementare un'autorizzazione personalizzata per i messaggi in arrivo in un host del servizio.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Servizi Web di autorizzazione servizio per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c296dc6b4900bd20df7d1e70631e758599a0028d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104118666"
---
# <a name="service-authorization"></a><span data-ttu-id="36773-106">Autorizzazione servizio</span><span class="sxs-lookup"><span data-stu-id="36773-106">Service Authorization</span></span>

<span data-ttu-id="36773-107">Un'applicazione può implementare un'autorizzazione personalizzata per i messaggi in arrivo in un host del servizio.</span><span class="sxs-lookup"><span data-stu-id="36773-107">An application can implement custom authorization for incoming messages on a service host .</span></span>


<span data-ttu-id="36773-108">Un host del servizio riceve un [**\_ \_ \_ callback di sicurezza WS Service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) callback di sicurezza come parte dell' [**\_ \_ endpoint del servizio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) che viene passato alla funzione [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) .</span><span class="sxs-lookup"><span data-stu-id="36773-108">A service host receives a security callback [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) as part of the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) which is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function.</span></span> <span data-ttu-id="36773-109">Questo callback viene richiamato quando viene ricevuto il [ \_ messaggio WS](ws-message.md) .</span><span class="sxs-lookup"><span data-stu-id="36773-109">This callback is invoked when the [WS\_MESSAGE](ws-message.md) is received.</span></span>

<span data-ttu-id="36773-110">L'applicazione può basarsi su questo callback per implementare l'autorizzazione personalizzata per i messaggi in arrivo nell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="36773-110">The application can rely on this callback to implement custom authorization for incoming messages on the service host.</span></span> <span data-ttu-id="36773-111">Se l'autorizzazione ha esito negativo, la funzione di callback di sicurezza restituisce un'ora di errore e l'host del servizio interrompe il canale.</span><span class="sxs-lookup"><span data-stu-id="36773-111">If the authorization fails the security callback function returns a failure HR, and the service host aborts the channel.</span></span>

<span data-ttu-id="36773-112">Per un'implementazione di esempio, vedere l'esempio relativo al nome utente su SSL, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="36773-112">See the user name over SSL example, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), for an example implementation.</span></span>

 

 




