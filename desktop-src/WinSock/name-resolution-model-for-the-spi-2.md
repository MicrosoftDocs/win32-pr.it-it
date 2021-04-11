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
# <a name="name-resolution-model-for-the-spi"></a><span data-ttu-id="3297d-103">Modello di risoluzione dei nomi per SPI</span><span class="sxs-lookup"><span data-stu-id="3297d-103">Name Resolution Model for the SPI</span></span>

<span data-ttu-id="3297d-104">Per lo sviluppo di un'applicazione client/server indipendente dal protocollo, esistono due requisiti di base per quanto riguarda la risoluzione dei nomi e la registrazione:</span><span class="sxs-lookup"><span data-stu-id="3297d-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="3297d-105">La capacità della metà del server dell'applicazione (in seguito definita come servizio) di registrarne l'esistenza entro (o diventare accessibile) uno o più spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3297d-105">The ability of the server half of the application (hereafter referred to as a service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="3297d-106">La capacità dell'applicazione client di trovare il servizio in uno spazio dei nomi e di ottenere il protocollo di trasporto e le informazioni di indirizzamento richiesti.</span><span class="sxs-lookup"><span data-stu-id="3297d-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="3297d-107">Per chi è abituato allo sviluppo di applicazioni basate su TCP/IP, questo può comportare un minor numero di informazioni rispetto alla ricerca di un indirizzo host e quindi all'utilizzo di un numero di porta concordato.</span><span class="sxs-lookup"><span data-stu-id="3297d-107">For those accustomed to developing TCP/IP-based applications, this may involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="3297d-108">Altri schemi di rete, tuttavia, consentono di individuare il percorso del servizio, il protocollo utilizzato per il servizio e altri attributi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3297d-108">Other networking schemes, however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run-time.</span></span> <span data-ttu-id="3297d-109">Per soddisfare la gamma di funzionalità disponibili nei servizi dei nomi esistenti, l'interfaccia Windows Sockets 2 adotta il modello descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="3297d-109">To accommodate the range of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described below.</span></span>

<span data-ttu-id="3297d-110">Uno *spazio dei nomi* si riferisce a una funzionalità che consente di associare (come minimo) il protocollo e gli attributi di indirizzamento di un servizio di rete con uno o più nomi descrittivi.</span><span class="sxs-lookup"><span data-stu-id="3297d-110">A *namespace* refers to some capability to associate (as a minimum) the protocol and addressing attributes of a network service with one or more human-friendly names.</span></span> <span data-ttu-id="3297d-111">Molti spazi dei nomi sono attualmente in uso ampio, tra cui Internet Domain Name System (DNS), servizi directory NetWare (NDS), X. 500 e così via. Questi spazi dei nomi variano notevolmente nel modo in cui sono organizzati e implementati.</span><span class="sxs-lookup"><span data-stu-id="3297d-111">Many namespaces are currently in wide use including the Internet's Domain Name System (DNS), NetWare Directory Services (NDS), X.500, etc. These namespaces vary widely in how they are organized and implemented.</span></span> <span data-ttu-id="3297d-112">Alcune proprietà sono particolarmente importanti da comprendere dal punto di vista della risoluzione dei nomi di Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="3297d-112">Some of their properties are particularly important to understand from the perspective of Windows Sockets name resolution.</span></span>

 

 



