---
title: Configurazione di Run-Time
description: L'API HTTP consente alle applicazioni di eseguire la configurazione dinamica in fase di esecuzione.
ms.assetid: 5118b48b-b44c-4cf5-9754-ce23c5a0b87e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1b0a310f9fe86b2e6972aa2dff3d3b7fc05965
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298509"
---
# <a name="run-time-configuration"></a>Configurazione di Run-Time

L'API HTTP consente alle applicazioni di eseguire la configurazione dinamica in fase di esecuzione. La configurazione della fase di esecuzione non è persistente, richiede solo privilegi di basso livello e interessa solo l'applicazione. La configurazione in fase di esecuzione può includere le attività seguenti:

-   Inizializzazione del servizio HTTP e creazione di una sessione del server. Un'applicazione Inizializza il servizio HTTP chiamando la funzione [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) . Il server deve essere inizializzato prima di poter chiamare altre funzioni server. L'applicazione crea quindi una sessione del server chiamando la funzione [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) . La sessione del server è un contenitore per le proprietà che si applicano a tutti i gruppi di URL appartenenti a tale sessione del server. Ogni allication ha in genere una sola sessione del server. Per informazioni sull'impostazione delle proprietà della sessione del server e sul relativo ambito, vedere [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).
-   Registrazione per gli URL. Una volta creata la sessione del server, un'applicazione può registrarsi per gli URL creando uno o più gruppi di URL. Un gruppo di URL è un gruppo di URL a cui verranno applicate le stesse proprietà. Un'applicazione crea un gruppo di URL chiamando la funzione [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) e quindi aggiunge gli URL desiderati chiamando la funzione [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) . Dopo che un'applicazione è stata registrata per gli URL creando un gruppo di URL e ha associato il gruppo di URL a una coda di richieste (vedere [creazione e associazione a una coda di richieste](creating-and-binding-to-a-request-queue.md)), tutte le richieste provenienti da questi URL vengono indirizzate alla coda di richieste associata a tale applicazione. Per ulteriori informazioni sulle proprietà dei gruppi di URL impostando, vedere [ **HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
-   Abilitare le funzionalità impostando le proprietà del server HTTP, ad esempio [l'autenticazione](authentication-in-http-version-2-0.md), la [registrazione](server-side-logging-in-http-version-2-0.md), le impostazioni QoS, i timeout, lo stato abilitato e le informazioni di binding. Per informazioni sull'impostazione delle proprietà, vedere [**http \_ server \_ Property**](/windows/desktop/api/Http/ne-http-http_server_property).

 

 




