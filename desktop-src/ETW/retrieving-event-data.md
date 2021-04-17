---
description: Per utilizzare dati specifici dell'evento, il consumer deve essere in grado di individuare il formato dei dati dell'evento.
ms.assetid: d783ff64-73c5-4ace-a866-38a42db7c8b6
title: Recupero dei dati dell'evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427d39f9c187d1dd0279d5946e546e415badd13f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977602"
---
# <a name="retrieving-event-data"></a><span data-ttu-id="3bdf6-103">Recupero dei dati dell'evento</span><span class="sxs-lookup"><span data-stu-id="3bdf6-103">Retrieving Event Data</span></span>

<span data-ttu-id="3bdf6-104">Per utilizzare dati specifici dell'evento, il consumer deve essere in grado di individuare il formato dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3bdf6-104">To consume event specific data, the consumer must know the format of the event data.</span></span> <span data-ttu-id="3bdf6-105">Questo non è un problema se si utilizzano eventi del provider personalizzato perché si conosce il formato dei dati.</span><span class="sxs-lookup"><span data-stu-id="3bdf6-105">This is not an issue if you are consuming events from your own provider because you know the format of the data.</span></span> <span data-ttu-id="3bdf6-106">Tuttavia, per utilizzare un evento da qualsiasi provider, il provider deve pubblicare il layout dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3bdf6-106">However, to consume an event from any provider, the provider must publish the layout of the event data.</span></span> <span data-ttu-id="3bdf6-107">Per una panoramica del funzionamento dei metadati degli eventi e per la pubblicazione dei metadati degli eventi in modo che altri utenti possano usarlo, vedere [Cenni preliminari sui metadati degli eventi](event-metadata-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3bdf6-107">For an overview of how event metadata operates as well as how to publish your event metadata so others can use it, see [Event Metadata Overview](event-metadata-overview.md).</span></span>

<span data-ttu-id="3bdf6-108">Per utilizzare gli eventi in Windows Vista pubblicati utilizzando un file manifesto, MOF o MDF, nonché gli eventi TraceLogging, vedere [recupero di dati di evento mediante TDH](retrieving-event-data-using-tdh.md).</span><span class="sxs-lookup"><span data-stu-id="3bdf6-108">To consume events on Windows Vista that were published using a manifest, MOF, or TMF files, as well as TraceLogging events, see [Retrieving Event Data Using TDH](retrieving-event-data-using-tdh.md).</span></span>

<span data-ttu-id="3bdf6-109">Per utilizzare gli eventi precedenti a Windows Vista pubblicati utilizzando MOF, vedere [recupero di dati di evento tramite MOF](retrieving-event-data-using-mof.md).</span><span class="sxs-lookup"><span data-stu-id="3bdf6-109">To consume events prior to Windows Vista that were published using MOF, see [Retrieving Event Data Using MOF](retrieving-event-data-using-mof.md).</span></span>

 

 



