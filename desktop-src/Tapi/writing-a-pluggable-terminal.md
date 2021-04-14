---
description: In genere, un provider di servizi multimediali implementa la creazione del terminale.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Scrittura di un terminale collegabile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526809"
---
# <a name="writing-a-pluggable-terminal"></a><span data-ttu-id="2696e-103">Scrittura di un terminale collegabile</span><span class="sxs-lookup"><span data-stu-id="2696e-103">Writing a Pluggable Terminal</span></span>

<span data-ttu-id="2696e-104">In genere, un provider di servizi multimediali implementa la creazione del terminale.</span><span class="sxs-lookup"><span data-stu-id="2696e-104">Normally, a media service provider (MSP) implements terminal creation.</span></span> <span data-ttu-id="2696e-105">A partire da Windows 2000 SP1, TAPI 3 include terminali innestabili che consentono a un'applicazione di implementare la creazione del terminale.</span><span class="sxs-lookup"><span data-stu-id="2696e-105">Starting with Windows 2000 SP1, TAPI 3 includes pluggable terminals to allow an application to implement terminal creation.</span></span> <span data-ttu-id="2696e-106">Per altre informazioni sull'uso di questi terminali, vedere Panoramica sull' [implementazione di terminali collegabili](implementing-pluggable-terminals.md) .</span><span class="sxs-lookup"><span data-stu-id="2696e-106">Please see the overview on [implementing pluggable terminals](implementing-pluggable-terminals.md) for additional information on using these terminals.</span></span>

<span data-ttu-id="2696e-107">Non usare i terminali collegabili regolarmente perché le funzionalità complete di un terminale saranno disponibili solo quando un MSP ne è pienamente a conoscenza.</span><span class="sxs-lookup"><span data-stu-id="2696e-107">You should not use pluggable terminals routinely because the full capabilities of a terminal will only be available when an MSP is fully aware of it.</span></span> <span data-ttu-id="2696e-108">Inoltre, è consigliabile non tentare di implementare terminali innestabili, a meno che non si abbia già familiarità con la scrittura di provider di servizi multimediali.</span><span class="sxs-lookup"><span data-stu-id="2696e-108">Further, you should not attempt to implement pluggable terminals unless you are already familiar with writing media service providers.</span></span> <span data-ttu-id="2696e-109">Le tecniche e i potenziali problemi interessati sono molto simili.</span><span class="sxs-lookup"><span data-stu-id="2696e-109">The techniques and potential problems involved are quite similar.</span></span>

<span data-ttu-id="2696e-110">Il provisioning di un caso speciale di terminale collegabile è attualmente disponibile per la situazione di un server di conferenza che deve aggiungere client non Windows 2000 SP1 o non multicast H. 323 a conferenze multicast SDP/IP a più parti di TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="2696e-110">Provision for a special case of pluggable terminal currently exists for the situation of a conferencing server that needs to add non-Windows 2000 SP1 or nonmulticast H.323 clients to TAPI 3 multiparty SDP/IP multicast conferences.</span></span>

 

 



