---
title: Gestori COM
description: Lo scopo dei gestori COM è fornire alcuni \ 0034; Smart \ 0034; codice nello spazio degli indirizzi del client che può ottimizzare le chiamate tra un client e un server. I gestori possono eseguire l'override di alcune interfacce e delegare gli altri direttamente al server (tramite il proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297751"
---
# <a name="com-handlers"></a><span data-ttu-id="1e893-104">Gestori COM</span><span class="sxs-lookup"><span data-stu-id="1e893-104">COM Handlers</span></span>

<span data-ttu-id="1e893-105">Lo scopo dei gestori COM è fornire codice "intelligente" nello spazio degli indirizzi del client in grado di ottimizzare le chiamate tra un client e un server.</span><span class="sxs-lookup"><span data-stu-id="1e893-105">The purpose of COM handlers is to provide some "smart" code in the client address space that can optimize calls between a client and server.</span></span> <span data-ttu-id="1e893-106">I gestori possono eseguire l'override di alcune interfacce e delegare gli altri direttamente al server (tramite il proxy).</span><span class="sxs-lookup"><span data-stu-id="1e893-106">Handlers can override some interfaces while delegating others directly to the server (through the proxy).</span></span>

<span data-ttu-id="1e893-107">Esistono due tipi di gestori COM:</span><span class="sxs-lookup"><span data-stu-id="1e893-107">There are two types of COM handlers:</span></span>

-   <span data-ttu-id="1e893-108">[Il gestore OLE](the-ole-handler.md) è una DLL dei pesi massimi che fornisce importanti servizi per il collegamento e l'incorporamento.</span><span class="sxs-lookup"><span data-stu-id="1e893-108">[The OLE handler](the-ole-handler.md) is a heavyweight DLL that provides important services for linking and embedding.</span></span> <span data-ttu-id="1e893-109">Viene in genere creato prima dell'avvio del server e viene inizializzato in modo che il server venga attivato quando l'oggetto incorporato entra nello stato in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1e893-109">It is usually created before the server is launched and is initialized so that the server is activated when the embedded object enters the running state.</span></span>
-   <span data-ttu-id="1e893-110">[Il gestore leggero lato client](the-lightweight-client-side-handler.md) può essere creato per qualsiasi scopo, può essere molto piccolo e non può essere creato prima del server.</span><span class="sxs-lookup"><span data-stu-id="1e893-110">[The lightweight client-side handler](the-lightweight-client-side-handler.md) can be created for any purpose, can be very small, and cannot be created before the server.</span></span>

 

 




