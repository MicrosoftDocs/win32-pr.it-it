---
title: Run-Time configurazione
description: L'API HTTP consente alle applicazioni di eseguire la configurazione dinamica in fase di esecuzione.
ms.assetid: 5118b48b-b44c-4cf5-9754-ce23c5a0b87e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b240438ada7fce186f334df3175b8ecc5b557626c5f1f085cdf82965fb32365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393753"
---
# <a name="run-time-configuration"></a>Run-Time configurazione

L'API HTTP consente alle applicazioni di eseguire la configurazione dinamica in fase di esecuzione. La configurazione in fase di esecuzione non è persistente, richiede solo privilegi di basso livello e influisce solo sull'applicazione. La configurazione in fase di esecuzione può includere una delle attività seguenti:

-   Inizializzazione del servizio HTTP e creazione di una sessione del server. Un'applicazione inizializza il servizio HTTP chiamando la [**funzione HttpInitialize.**](/windows/desktop/api/Http/nf-http-httpinitialize) Il server deve essere inizializzato prima di poter chiamare qualsiasi altra funzione del server. L'applicazione crea quindi una sessione server chiamando la [**funzione HttpCreateServerSession.**](/windows/desktop/api/Http/nf-http-httpcreateserversession) La sessione server è un contenitore per le proprietà che si applicano a tutti i gruppi di URL appartenenti a tale sessione server. In genere ogni allication ha una sola sessione del server. Per informazioni sull'impostazione delle proprietà della sessione del server e sul relativo ambito, vedere [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).
-   Registrazione per gli URL. Dopo aver creato la sessione del server, un'applicazione può registrarsi per gli URL creando uno o più gruppi di URL. Un gruppo di URL è un gruppo di URL a cui verranno applicate le stesse proprietà. Un'applicazione crea un gruppo di URL chiamando la [**funzione HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) e quindi aggiunge gli URL desiderati chiamando la [**funzione HttpAddUrlToUrlGroup.**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) Dopo che un'applicazione è stata registrata per gli URL creando un gruppo di URL e ha associato il gruppo di URL a una coda di richieste (vedere Creazione e associazione [a](creating-and-binding-to-a-request-queue.md)una coda di richieste), tutte le richieste provenienti da questi URL vengono indirizzate alla coda di richieste associata all'applicazione. Per altre informazioni sull'impostazione delle proprietà del gruppo di URL, [ **vedere HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
-   Abilitazione delle funzionalità impostando le [](authentication-in-http-version-2-0.md)proprietà del server HTTP, ad esempio l'autenticazione, [la registrazione,](server-side-logging-in-http-version-2-0.md)le impostazioni QOS, i timeout, lo stato abilitato e le informazioni di associazione. Per informazioni sull'impostazione delle proprietà, vedere [**HTTP \_ SERVER \_ PROPERTY**](/windows/desktop/api/Http/ne-http-http_server_property).

 

 




