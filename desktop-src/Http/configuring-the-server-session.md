---
title: Configurazione della sessione del server
description: .
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf069b22992fa178798c7f28545e30217d0dada
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297761"
---
# <a name="configuring-the-server-session"></a>Configurazione della sessione del server

L'ID di sessione del server viene creato con la funzione [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) e usato nella chiamata a [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty). Il parametro *pPropertyInformation* punta alla struttura di configurazione per il tipo di proprietà impostato. Il parametro *PropertyInformationLength* specifica la dimensione, in byte, della struttura di configurazione. Ad esempio, quando si imposta **HttpServerTimeoutsProperty** , il parametro **pPropertyInformation** deve puntare a un buffer che corrisponde almeno alla dimensione della struttura [**di \_ \_ \_ informazioni sul limite di timeout http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) .

In genere, un'applicazione HTTP crea una singola sessione del server e può impostare le proprietà a livello di applicazione, ad esempio il limite globale di limitazione della larghezza di banda o abilitare la registrazione centralizzata in questa sessione del server. [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) esegue l'override delle configurazioni dell'API del server http per l'applicazione chiamante. non influisce sulle proprietà a livello di API del server HTTP. Viene eseguita una query sulle configurazioni di sessione del server chiamando [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).

 

 




