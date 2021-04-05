---
title: Configurazione del gruppo di URL
description: .
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d9be6969b2b197d0bdcb404ad6b8965c278235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955660"
---
# <a name="configuring-the-url-group"></a>Configurazione del gruppo di URL

L'ID del gruppo URL viene creato con la funzione [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) e usato nella chiamata a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). Il parametro *pPropertyInformation* punta alla struttura di configurazione per il tipo di proprietà impostato. Il parametro **PropertyInformationLength** specifica la dimensione, in byte, della struttura di configurazione. Ad esempio, quando si imposta **HttpServerTimeoutsProperty** , il parametro *pPropertyInformation* deve puntare a un buffer che non può essere inferiore alla struttura di [**informazioni sul \_ \_ limite \_ di timeout http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) . Viene eseguita una query sulle configurazioni del gruppo di URL chiamando [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty).

Dopo la creazione del gruppo di URL, gli URL vengono aggiunti al gruppo con [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup). Il gruppo di URL deve essere associato a una coda di richieste della versione 2,0 per ricevere le richieste. Per associare il gruppo di URL a una coda di richieste, l'applicazione chiama [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) e specifica **HttpServerBindingProperty** nel parametro *Property* . Se questa proprietà non è impostata, le richieste corrispondenti per il gruppo di URL non vengono recapitate a una coda di richieste e l'API del server HTTP genera una risposta 503. L'applicazione può aggiungere solo URL che in precedenza sono stati riservati con il servizio a un gruppo di URL durante l'esecuzione con privilegi limitati. Per ulteriori informazioni, vedere l'argomento [prenotazioni, registrazioni e routing dello spazio dei nomi](namespace-reservations-registrations-and-routing.md) .

 

 




