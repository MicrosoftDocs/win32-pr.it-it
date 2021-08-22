---
title: Configurazione del gruppo di URL
description: Configurazione del gruppo di URL
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d335af063eb8cadc557db3f01da850b468099866e292bcd5ea2a3af314de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014909"
---
# <a name="configuring-the-url-group"></a>Configurazione del gruppo di URL

L'ID gruppo DI URL viene creato con la [**funzione HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) e usato nella chiamata a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). Il *parametro pPropertyInformation* punta alla struttura di configurazione per il tipo di proprietà impostato. Il **parametro PropertyInformationLength** specifica le dimensioni, in byte, della struttura di configurazione. Ad esempio, quando si imposta **HttpServerTimeoutsProperty,** il *parametro pPropertyInformation* deve puntare a un buffer che non può essere inferiore alla struttura [**HTTP TIMEOUT LIMIT \_ \_ \_ INFO.**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) Le configurazioni del gruppo di URL vengono interrogate chiamando [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty).

Dopo aver creato il gruppo di URL, gli URL vengono aggiunti al gruppo con [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup). Il gruppo di URL deve essere associato a una coda di richieste versione 2.0 per ricevere le richieste. Per associare il gruppo di URL a una coda di richieste, l'applicazione chiama [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) e specifica **HttpServerBindingProperty** nel *parametro Property.* Se questa proprietà non è impostata, le richieste corrispondenti per il gruppo di URL non vengono recapitate a una coda di richieste e l'API server HTTP genera una risposta 503. L'applicazione può aggiungere gli URL che sono stati precedentemente riservati con il servizio a un gruppo di URL solo quando vengono eseguiti con privilegi minimi. Per altre informazioni, vedere l'argomento [Prenotazioni, registrazioni e routing dello](namespace-reservations-registrations-and-routing.md) spazio dei nomi.

 

 




