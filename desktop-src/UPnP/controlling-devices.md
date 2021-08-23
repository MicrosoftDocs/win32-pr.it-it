---
title: Controllo dei dispositivi
description: I dispositivi basati su UPnP sono controllati dai servizi esposti.
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410818552f1f6563b28fcb963fcfca5c9b3067973e325adfd66ede5bffaedb75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999631"
---
# <a name="controlling-devices"></a>Controllo dei dispositivi

I dispositivi basati su UPnP sono controllati dai servizi esposti. Un servizio UPnP è l'entità controllabile più piccola nell'architettura UPnP. I dispositivi espongono un servizio per ogni funzione primaria che eseguono. I dispositivi complessi sono in genere costituiti da diversi servizi semplici e altri dispositivi.

Un servizio è costituito da un set di variabili di stato e da un set di azioni che un'applicazione può richiamare che operano su tali variabili di stato. Nell'API del punto di controllo con tecnologia UPnP, i servizi sono rappresentati da oggetti **servizio** che espongono [**l'interfaccia IUPnPService.**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)

Un tipo di servizio definisce le variabili di stato e le azioni supportate da un particolare servizio. Ad esempio, il tipo di servizio per un servizio orologio definisce le **azioni GetTime** e **SetTime,** insieme a una **variabile di stato Time.**

Un ID servizio distingue più tipi di servizi comuni all'interno di un singolo dispositivo. Ad esempio, possono essere presenti due servizi di orologio in una sveglia, uno per l'orologio normale e l'altro per l'allarme. Deve essere possibile distinguere tra i due servizi, che hanno tipi di servizio identici. L'ID servizio fornisce un modo univoco per identificare un'istanza di un tipo di servizio. Questo ID servizio viene quindi usato per accedere al servizio corretto dalla raccolta [**IUPnPServices,**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) perché il tipo di servizio non è un identificatore univoco. [**L'interfaccia IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) consente anche alle applicazioni di registrare una funzione di callback con l'oggetto servizio. Quando il valore della variabile di stato di un servizio cambia, l'oggetto servizio richiama il callback registrato per notificare all'applicazione la modifica. Il framework UPnP richiama anche questo callback per notificare alle applicazioni quando un'istanza del servizio non è più disponibile. Il servizio può diventare non disponibile per diversi motivi, tra cui un errore di rete temporaneo.

Per altre informazioni, vedere i seguenti argomenti:

-   [Recupero di oggetti servizio](obtaining-service-objects.md)
-   [Registrazione di un callback](registering-a-callback.md)
-   [Esecuzione di query su variabili di stato](querying-state-variables.md)
-   [Chiamata di azioni](invoking-actions.md)

 

 




