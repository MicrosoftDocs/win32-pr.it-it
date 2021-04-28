---
title: Configurazione del gruppo di URL
description: Configurazione del gruppo di URL
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407ca18fc5d2797c99e86661bf462eaf0a3fdc5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109699"
---
# <a name="configuring-the-url-group"></a>Configurazione del gruppo di URL

L'ID del gruppo di URL viene creato con [**la funzione HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) e usato nella chiamata a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). Il *parametro pPropertyInformation* punta alla struttura di configurazione per il tipo di proprietà impostato. Il **parametro PropertyInformationLength** specifica le dimensioni, in byte, della struttura di configurazione. Ad esempio, quando si imposta **HttpServerTimeoutsProperty,** il parametro *pPropertyInformation* deve puntare a un buffer che non può essere inferiore alla struttura [**HTTP TIMEOUT LIMIT \_ \_ \_ INFO.**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) Le configurazioni del gruppo di URL vengono sottoposti a query chiamando [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty).

Dopo aver creato il gruppo di URL, gli URL vengono aggiunti al gruppo con [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup). Il gruppo di URL deve essere associato a una coda di richieste versione 2.0 per ricevere le richieste. Per associare il gruppo di URL a una coda di richieste, l'applicazione chiama [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) e specifica **HttpServerBindingProperty** nel *parametro Property.* Se questa proprietà non è impostata, le richieste corrispondenti per il gruppo di URL non vengono recapitate a una coda di richieste e l'API del server HTTP genera una risposta 503. L'applicazione può aggiungere url che sono stati precedentemente riservati con il servizio a un gruppo di URL solo in caso di esecuzione con privilegi bassi. Per altre informazioni, vedere l'argomento [Prenotazioni, registrazioni e routing](namespace-reservations-registrations-and-routing.md) dello spazio dei nomi.

 

 




