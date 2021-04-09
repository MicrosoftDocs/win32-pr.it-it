---
title: Configurazione della coda di richieste
description: Configurazione della coda di richieste
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ed397ffbcb42d887d519bc4492bd167dd98c57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856129"
---
# <a name="configuring-the-request-queue"></a>Configurazione della coda di richieste

Quando la coda di richieste viene aperta o creata, l'applicazione chiamante riceve un handle che può essere utilizzato per inviare richieste o configurare la coda delle richieste. La chiamata di [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerBindingProperty** e la specifica dell'handle della coda di richiesta nella struttura di [**\_ \_ informazioni di binding http**](/windows/desktop/api/Http/ns-http-http_binding_info) , specificata nel parametro *pPropertyInformation* , associa il gruppo di URL alla coda di richieste. Le proprietà della coda di richieste vengono impostate solo dall'applicazione che crea la coda delle richieste. Per impostare la proprietà Lunghezza coda del server, ad esempio, l'applicazione Creator chiama [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) specificando **HttpServerQueueLengthProperty** nel parametro *Property* .

 

 




