---
description: Risoluzione dei nomi indipendente dal protocollo e Windows Sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Risoluzione dei nomi Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343476"
---
# <a name="protocol-independent-name-resolution"></a><span data-ttu-id="532e8-103">Risoluzione dei nomi Protocol-Independent</span><span class="sxs-lookup"><span data-stu-id="532e8-103">Protocol-Independent Name Resolution</span></span>

<span data-ttu-id="532e8-104">Per lo sviluppo di un'applicazione client/server indipendente dal protocollo, esistono due requisiti di base per quanto riguarda la risoluzione dei nomi e la registrazione:</span><span class="sxs-lookup"><span data-stu-id="532e8-104">In developing a protocol-independent client/server application, there are two basic requirements that exist with respect to name resolution and registration:</span></span>

-   <span data-ttu-id="532e8-105">Capacità della metà del server dell'applicazione (servizio) di registrare la propria esistenza entro (o diventare accessibile) uno o più spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="532e8-105">The ability of the server half of the application ( service) to register its existence within (or become accessible to) one or more namespaces.</span></span>
-   <span data-ttu-id="532e8-106">La capacità dell'applicazione client di trovare il servizio in uno spazio dei nomi e di ottenere il protocollo di trasporto e le informazioni di indirizzamento richiesti.</span><span class="sxs-lookup"><span data-stu-id="532e8-106">The ability of the client application to find the service within a namespace and obtain the required transport protocol and addressing information.</span></span>

<span data-ttu-id="532e8-107">Per chi è abituato allo sviluppo di applicazioni basate su TCP/IP, questo può sembrare poco più che cercare un indirizzo host e quindi usare un numero di porta concordato.</span><span class="sxs-lookup"><span data-stu-id="532e8-107">For those accustomed to developing TCP/IP-based applications, this may seem to involve little more than looking up a host address and then using an agreed upon port number.</span></span> <span data-ttu-id="532e8-108">Tuttavia, altri schemi di rete consentono di individuare il percorso del servizio, il protocollo utilizzato per il servizio e altri attributi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="532e8-108">Other networking schemes however, allow the location of the service, the protocol used for the service, and other attributes to be discovered at run time.</span></span> <span data-ttu-id="532e8-109">Per supportare la vasta gamma di funzionalità disponibili nei servizi dei nomi esistenti, l'interfaccia Windows Sockets 2 adotta il modello descritto negli argomenti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="532e8-109">To accommodate the broad diversity of capabilities found in existing name services, the Windows Sockets 2 interface adopts the model described in the topics in this section.</span></span>

<span data-ttu-id="532e8-110">In questa sezione vengono descritte le funzionalità di risoluzione dei nomi indipendenti dal protocollo disponibili per gli sviluppatori Winsock.</span><span class="sxs-lookup"><span data-stu-id="532e8-110">This section describes protocol-independent name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="532e8-111">Nell'elenco seguente vengono descritti gli argomenti di questa sezione:</span><span class="sxs-lookup"><span data-stu-id="532e8-111">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="532e8-112">Modello di risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="532e8-112">Name Resolution Model</span></span>](name-resolution-model-2.md)
-   [<span data-ttu-id="532e8-113">Riepilogo delle funzioni di risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="532e8-113">Summary of Name Resolution Functions</span></span>](summary-of-name-resolution-functions-2.md)
-   [<span data-ttu-id="532e8-114">Strutture dei dati di risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="532e8-114">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)

## <a name="related-topics"></a><span data-ttu-id="532e8-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="532e8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="532e8-116">Registrazione e risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="532e8-116">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



