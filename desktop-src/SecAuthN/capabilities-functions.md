---
description: L'API del provider di rete specifica una singola funzione di funzionalità.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funzioni funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049770"
---
# <a name="capabilities-functions"></a><span data-ttu-id="c9d06-103">Funzioni funzionalità</span><span class="sxs-lookup"><span data-stu-id="c9d06-103">Capabilities Functions</span></span>

<span data-ttu-id="c9d06-104">L'API del provider di rete specifica una singola funzione di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c9d06-104">The Network Provider API specifies a single capabilities function.</span></span> <span data-ttu-id="c9d06-105">Quando il sistema operativo richiede informazioni sulle funzionalità di un provider di rete, il [*router multi-provider*](/windows/desktop/SecGloss/m-gly) (MPR) chiama la funzione [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) di ogni provider di rete la cui rete è attiva.</span><span class="sxs-lookup"><span data-stu-id="c9d06-105">When the operating system requests information about a network provider's capabilities, the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function of each network provider whose network is active.</span></span>

<span data-ttu-id="c9d06-106">La funzione [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) restituisce una maschera di maschera che indica le funzioni dell'API del provider di rete supportata dal provider di rete.</span><span class="sxs-lookup"><span data-stu-id="c9d06-106">The [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function returns a bitmask indicating which functions of the Network Provider API the network provider supports.</span></span> <span data-ttu-id="c9d06-107">La funzione **NPGetCaps** è l'unica funzione che deve essere implementata da un provider di rete.</span><span class="sxs-lookup"><span data-stu-id="c9d06-107">The **NPGetCaps** function is the only function that a network provider must implement.</span></span> <span data-ttu-id="c9d06-108">Il sistema operativo chiama questa funzione per determinare quali altre funzioni dell'API del provider di rete supporta il provider.</span><span class="sxs-lookup"><span data-stu-id="c9d06-108">The operating system calls this function to determine which other functions of the Network Provider API the provider supports.</span></span>

 

 
