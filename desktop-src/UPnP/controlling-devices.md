---
title: Controllo dei dispositivi
description: I dispositivi basati su UPnP sono controllati dai servizi che espongono.
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a72a4ffdf91bca358124dbb0a0d95ff9a61e30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856649"
---
# <a name="controlling-devices"></a>Controllo dei dispositivi

I dispositivi basati su UPnP sono controllati dai servizi che espongono. Un servizio UPnP è la più piccola entità controllabile nell'architettura UPnP. I dispositivi espongono un servizio per ogni funzione primaria eseguita. I dispositivi complessi sono in genere costituiti da diversi servizi semplici e altri dispositivi.

Un servizio è costituito da un set di variabili di stato e da un set di azioni che possono essere richiamate da un'applicazione che operano su tali variabili di stato. Nell'API del punto di controllo con la tecnologia UPnP i servizi sono rappresentati da oggetti **servizio** che espongono l'interfaccia [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .

Un tipo di servizio definisce le variabili di stato e le azioni supportate da un particolare servizio. Ad esempio, il tipo di servizio per un servizio clock definisce le azioni **getTime** e **setime** , insieme a una variabile di stato dell' **ora** .

Un ID servizio distingue più tipi di servizi comuni all'interno di un singolo dispositivo. Ad esempio, è possibile che siano presenti due servizi di clock in una sveglia, uno per l'orologio normale e l'altro per l'allarme. È necessario un modo per distinguere tra i due servizi, che hanno tipi di servizio identici. L'ID del servizio fornisce un modo univoco per identificare un'istanza di un tipo di servizio. Quindi, questo ID servizio viene usato per accedere al servizio corretto dalla raccolta [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) , perché il tipo di servizio non è un identificatore univoco. L'interfaccia [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) consente inoltre alle applicazioni di registrare una funzione di callback con l'oggetto servizio. Quando cambia il valore della variabile di stato di un servizio, l'oggetto servizio richiama il callback registrato per notificare all'applicazione la modifica. Il Framework UPnP richiama inoltre questo callback per notificare alle applicazioni quando un'istanza del servizio non è più disponibile. Il servizio può non essere più disponibile per diversi motivi, incluso un errore di rete temporaneo.

Per altre informazioni, vedere i seguenti argomenti:

-   [Recupero di oggetti servizio](obtaining-service-objects.md)
-   [Registrazione di un callback](registering-a-callback.md)
-   [Esecuzione di query sulle variabili di stato](querying-state-variables.md)
-   [Richiamo di azioni](invoking-actions.md)

 

 




