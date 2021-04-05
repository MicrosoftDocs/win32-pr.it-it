---
title: Implementazione di un dispositivo ospitato
description: L'host del dispositivo con la tecnologia UPnP implementa i protocolli UPnP di base per l'individuazione, la descrizione, il controllo e la gestione degli eventi.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713576"
---
# <a name="implementing-a-hosted-device"></a><span data-ttu-id="2bd90-103">Implementazione di un dispositivo ospitato</span><span class="sxs-lookup"><span data-stu-id="2bd90-103">Implementing a Hosted Device</span></span>

<span data-ttu-id="2bd90-104">L'host dispositivo con tecnologia UPnP implementa i protocolli UPnP principali: individuazione, descrizione, controllo ed eventi.</span><span class="sxs-lookup"><span data-stu-id="2bd90-104">The device host with UPnP technology implements the core UPnP protocols: discovery, description, control, and eventing.</span></span> <span data-ttu-id="2bd90-105">Lo sviluppatore che implementa un dispositivo ospitato deve solo fornire:</span><span class="sxs-lookup"><span data-stu-id="2bd90-105">The developer who implements a hosted device only needs to provide:</span></span>

-   <span data-ttu-id="2bd90-106">Una descrizione del dispositivo e dei relativi servizi.</span><span class="sxs-lookup"><span data-stu-id="2bd90-106">A description of the device and its services.</span></span>
-   <span data-ttu-id="2bd90-107">Implementazione della funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd90-107">An implementation of the device's functionality.</span></span>

<span data-ttu-id="2bd90-108">Ad esempio, lo sviluppatore di un dispositivo clock deve fornire descrizioni di dispositivi e servizi basati su UPnP e un'implementazione delle funzioni di clock, ad esempio la conservazione del tempo, l'impostazione dell'ora e la risposta alle query per l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="2bd90-108">For example, the developer of a clock device must provide UPnP-based device and service descriptions for it, and an implementation of the clock functions (such as keeping time, setting time, and responding to queries for the current time).</span></span> <span data-ttu-id="2bd90-109">Host del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="2bd90-109">The device host:</span></span>

-   <span data-ttu-id="2bd90-110">Annuncia il dispositivo in base al protocollo di individuazione UPnP.</span><span class="sxs-lookup"><span data-stu-id="2bd90-110">Announces the device according to the UPnP discovery protocol.</span></span>
-   <span data-ttu-id="2bd90-111">Risponde alle query per la descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2bd90-111">Responds to queries for the device's description.</span></span>
-   <span data-ttu-id="2bd90-112">Instrada le richieste di controllo alla parte del codice del dispositivo che implementa le funzioni Clock.</span><span class="sxs-lookup"><span data-stu-id="2bd90-112">Routes control requests to the part of the device's code that implements the clock functions.</span></span>
-   <span data-ttu-id="2bd90-113">Mantiene le sottoscrizioni di eventi ai servizi.</span><span class="sxs-lookup"><span data-stu-id="2bd90-113">Maintains event subscriptions to services.</span></span>
-   <span data-ttu-id="2bd90-114">Invia notifiche degli eventi ai sottoscrittori quando lo stato del servizio viene modificato.</span><span class="sxs-lookup"><span data-stu-id="2bd90-114">Sends event notifications to subscribers when the service's state changes.</span></span>

 

 




