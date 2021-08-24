---
description: Modello di risoluzione dei nomi e registrazione per Windows Sockets (Winsock) SPI.
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Modello di risoluzione dei nomi per SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f012a5c14a6dae9045b303ecb7c4e39f1d93d264285138d98c0e93274ef921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132114"
---
# <a name="name-resolution-model-for-the-spi"></a>Modello di risoluzione dei nomi per SPI

Nello sviluppo di un'applicazione client/server indipendente dal protocollo esistono due requisiti di base relativi alla risoluzione dei nomi e alla registrazione:

-   La capacità della metà server dell'applicazione (da qui in poi definita servizio) di registrarne l'esistenza all'interno (o diventare accessibile a) uno o più spazi dei nomi.
-   Possibilità dell'applicazione client di trovare il servizio all'interno di uno spazio dei nomi e di ottenere il protocollo di trasporto e le informazioni di indirizzamento richiesti.

Per gli utenti abituati a sviluppare applicazioni basate su TCP/IP, ciò può comportare poco più della ricerca di un indirizzo host e quindi dell'uso di un numero di porta concordato. Altri schemi di rete, tuttavia, consentono di individuare la posizione del servizio, il protocollo usato per il servizio e altri attributi in fase di esecuzione. Per supportare la gamma di funzionalità disponibili nei servizi dei nomi esistenti, l'interfaccia Windows Sockets 2 adotta il modello descritto di seguito.

Uno *spazio* dei nomi fa riferimento ad alcune funzionalità per associare (come minimo) il protocollo e gli attributi di indirizzamento di un servizio di rete a uno o più nomi descrittivi. Molti spazi dei nomi sono attualmente in uso su vasta gamma, tra cui DNS (Internet's Domain Name System), NetWare Directory Services (NDS), X.500 e così via. Questi spazi dei nomi variano notevolmente nel modo in cui vengono organizzati e implementati. Alcune delle relative proprietà sono particolarmente importanti da comprendere dal punto di vista della risoluzione dei Windows Sockets.

 

 



