---
title: Configurazione della coda delle richieste
description: Configurazione della coda delle richieste
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08a8f931d8875fda43b485bada93d2bf5291d0d2b90e85c8b31bd631e8c7fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014929"
---
# <a name="configuring-the-request-queue"></a>Configurazione della coda delle richieste

Quando la coda di richieste viene aperta o creata, l'applicazione chiamante riceve un handle che può essere usato per inviare richieste o configurare la coda delle richieste. Chiamando [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerBindingProperty** e fornendo l'handle della coda di richieste nella struttura [**HTTP BINDING \_ \_ INFO,**](/windows/desktop/api/Http/ns-http-http_binding_info) specificata nel *parametro pPropertyInformation,* il gruppo di URL viene associato alla coda delle richieste. Le proprietà della coda di richiesta vengono impostate solo dall'applicazione che crea la coda di richieste. Ad esempio, per impostare la proprietà della lunghezza della coda del server, l'applicazione creator chiama [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) specificando **HttpServerQueueLengthProperty** nel *parametro Property.*

 

 




