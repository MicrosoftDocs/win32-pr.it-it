---
description: Modello di registrazione e risoluzione dei nomi per Windows Sockets (Winsock) SPI.
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Modello di risoluzione dei nomi per SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e79593f56cd11671b3c16ef9098d455bf548505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129150"
---
# <a name="name-resolution-model-for-the-spi"></a>Modello di risoluzione dei nomi per SPI

Per lo sviluppo di un'applicazione client/server indipendente dal protocollo, esistono due requisiti di base per quanto riguarda la risoluzione dei nomi e la registrazione:

-   La capacità della metà del server dell'applicazione (in seguito definita come servizio) di registrarne l'esistenza entro (o diventare accessibile) uno o più spazi dei nomi.
-   La capacità dell'applicazione client di trovare il servizio in uno spazio dei nomi e di ottenere il protocollo di trasporto e le informazioni di indirizzamento richiesti.

Per chi è abituato allo sviluppo di applicazioni basate su TCP/IP, questo può comportare un minor numero di informazioni rispetto alla ricerca di un indirizzo host e quindi all'utilizzo di un numero di porta concordato. Altri schemi di rete, tuttavia, consentono di individuare il percorso del servizio, il protocollo utilizzato per il servizio e altri attributi in fase di esecuzione. Per soddisfare la gamma di funzionalità disponibili nei servizi dei nomi esistenti, l'interfaccia Windows Sockets 2 adotta il modello descritto di seguito.

Uno *spazio dei nomi* si riferisce a una funzionalità che consente di associare (come minimo) il protocollo e gli attributi di indirizzamento di un servizio di rete con uno o più nomi descrittivi. Molti spazi dei nomi sono attualmente in uso ampio, tra cui Internet Domain Name System (DNS), servizi directory NetWare (NDS), X. 500 e così via. Questi spazi dei nomi variano notevolmente nel modo in cui sono organizzati e implementati. Alcune proprietà sono particolarmente importanti da comprendere dal punto di vista della risoluzione dei nomi di Windows Sockets.

 

 



