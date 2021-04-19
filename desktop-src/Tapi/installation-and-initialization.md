---
description: L'installazione di un nuovo provider di servizi è molto specifica per i dispositivi e il sistema operativo, quindi i dettagli non rientrano nell'ambito di questo SDK.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Installazione e inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317652"
---
# <a name="installation-and-initialization"></a><span data-ttu-id="a0cd2-103">Installazione e inizializzazione</span><span class="sxs-lookup"><span data-stu-id="a0cd2-103">Installation and Initialization</span></span>

<span data-ttu-id="a0cd2-104">L'installazione di un nuovo provider di servizi è molto specifica per i dispositivi e il sistema operativo, quindi i dettagli non rientrano nell'ambito di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="a0cd2-104">Installation of a new service provider is highly device- and operating-system-specific, so the details are outside the scope of this SDK.</span></span> <span data-ttu-id="a0cd2-105">In generale, l'obiettivo dell'installazione è la configurazione del provider di servizi per l'ambiente di comunicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="a0cd2-105">Generally speaking, the goal of installation is configuration of the service provider for the current communications environment.</span></span> <span data-ttu-id="a0cd2-106">Questo in genere riguarda le voci del registro di sistema e l'impostazione delle dipendenze del servizio.</span><span class="sxs-lookup"><span data-stu-id="a0cd2-106">This usually involves registry entries and the setting of service dependencies.</span></span>

<span data-ttu-id="a0cd2-107">L'inizializzazione di un provider di servizi di telefonia inizia con la negoziazione della versione.</span><span class="sxs-lookup"><span data-stu-id="a0cd2-107">Initialization of a telephony service provider starts with version negotiation.</span></span> <span data-ttu-id="a0cd2-108">Per una descrizione della negoziazione della versione e della versione corrente, vedere [controllo delle versioni di TSPI](tspi-versioning.md) .</span><span class="sxs-lookup"><span data-stu-id="a0cd2-108">See [TSPI Versioning](tspi-versioning.md) for a discussion of version negotiation and current version.</span></span>

<span data-ttu-id="a0cd2-109">TAPI chiama quindi [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), che passa al provider un puntatore a una funzione di callback utilizzata per segnalare lo stato di avanzamento delle funzioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="a0cd2-109">TAPI then calls [**TSPI\_providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), which passes the provider a pointer to a callback function used to report on asynchronous functions progress.</span></span> <span data-ttu-id="a0cd2-110">Il TSP restituisce un conteggio dei dispositivi line e Phone associati all'identificatore del dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="a0cd2-110">The TSP returns a count of line and phone devices associated with the current device identifier.</span></span>

<span data-ttu-id="a0cd2-111">In genere, il passaggio successivo sarà l'inventario delle risorse, condotto da TAPI che richiama [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) e [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span><span class="sxs-lookup"><span data-stu-id="a0cd2-111">Typically, the next step will be resource inventory, conducted by TAPI invoking [**TSPI\_lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) and [**TSPI\_lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span></span> <span data-ttu-id="a0cd2-112">Si prevede che il provider di servizi compilerà gli elementi delle strutture di dati che riguardano le funzionalità del dispositivo e della sessione supportate.</span><span class="sxs-lookup"><span data-stu-id="a0cd2-112">The service provider is expected to fill in those elements of the data structures involved that pertain to device and session capabilities it supports.</span></span>

<span data-ttu-id="a0cd2-113">TAPI raccoglie informazioni dalle diverse applicazioni relative ai requisiti di notifica degli eventi e indica al TSP usando [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) di indicare quali tipi di supporti rilevare per una riga e [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) per indicare quali eventi di riga e di indirizzo devono essere segnalati.</span><span class="sxs-lookup"><span data-stu-id="a0cd2-113">TAPI collects information from the various applications concerning event notification requirements, and instructs the TSP using [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) to indicate which media types to detect for a line and [**TSPI\_lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) to indicate which line and address events should be reported.</span></span>

 

 
