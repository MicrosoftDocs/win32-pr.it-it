---
description: .
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: Microsoft Message Queuing (MSMQ)-gestione delle code migliorata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffcc566c4c4ea461fdd9c4634b26ff69f239f03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967710"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a><span data-ttu-id="2fa1d-103">Microsoft Message Queuing (MSMQ)-gestione delle code migliorata</span><span class="sxs-lookup"><span data-stu-id="2fa1d-103">Microsoft Message Queuing (MSMQ) - Improved Queue Handling</span></span>

## <a name="platforms"></a><span data-ttu-id="2fa1d-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="2fa1d-104">Platforms</span></span>

<span data-ttu-id="2fa1d-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="2fa1d-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="2fa1d-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2fa1d-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="2fa1d-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="2fa1d-107">Feature Impact</span></span>

 <span data-ttu-id="2fa1d-108">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="2fa1d-108">**Severity** - Low</span></span>  
<span data-ttu-id="2fa1d-109">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="2fa1d-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="2fa1d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fa1d-110">Description</span></span>

<span data-ttu-id="2fa1d-111">Il servizio MSMQ non impone un limite fisso al numero di code che è possibile creare in un sistema.</span><span class="sxs-lookup"><span data-stu-id="2fa1d-111">MSMQ Service does not put a hard limit on the number of queues that can be created on a system.</span></span> <span data-ttu-id="2fa1d-112">Tuttavia, le prestazioni del sistema sono interessate quando viene creato un numero elevato di code.</span><span class="sxs-lookup"><span data-stu-id="2fa1d-112">However, the performance of the system is impacted when a large number of queues is created.</span></span> <span data-ttu-id="2fa1d-113">In particolare, quando sono presenti più di migliaia di code, il tempo di avvio del servizio MSMQ aumenta in modo esponenziale con un conseguente effetto visibile.</span><span class="sxs-lookup"><span data-stu-id="2fa1d-113">Specifically, when there are more than a few thousand queues, the start-up time of the MSMQ Service increases exponentially resulting in a visible impact.</span></span>

<span data-ttu-id="2fa1d-114">Microsoft ha ottimizzato l'avvio del servizio MSMQ in Windows 7 per ridurre l'overhead di ricerca per il caricamento delle code in memoria.</span><span class="sxs-lookup"><span data-stu-id="2fa1d-114">Microsoft has optimized the MSMQ Service start-up in Windows 7 to reduce the lookup overhead for loading the queues into memory.</span></span> <span data-ttu-id="2fa1d-115">Questa ottimizzazione ha comportato un notevole miglioramento del tempo di avvio del servizio MSMQ anche quando nel sistema vengono create diverse migliaia di code.</span><span class="sxs-lookup"><span data-stu-id="2fa1d-115">This optimization has led to a dramatic improvement of the start-up time of the MSMQ Service even when several thousand queues are created in the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="2fa1d-116">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="2fa1d-116">Manifestation of Impact</span></span>

<span data-ttu-id="2fa1d-117">Questo miglioramento delle prestazioni non influisca sulle funzionalità di un'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="2fa1d-117">This performance improvement does not impact the functionality of any existing application.</span></span>

## <a name="leveraging-the-changed-feature"></a><span data-ttu-id="2fa1d-118">Uso della funzionalità modificata</span><span class="sxs-lookup"><span data-stu-id="2fa1d-118">Leveraging the Changed Feature</span></span>

<span data-ttu-id="2fa1d-119">Gli sviluppatori di applicazioni che utilizzano MSMQ in Windows 7 possono ora progettare le proprie soluzioni senza limitare il numero di code.</span><span class="sxs-lookup"><span data-stu-id="2fa1d-119">Application developers using MSMQ on Windows 7 can now architect their solutions without limiting the number of queues.</span></span> <span data-ttu-id="2fa1d-120">Si noti che il numero di code continua a influire sulle prestazioni complessive del server MSMQ, ma l'impatto sulle prestazioni è ora in una scala lineare anziché esponenziale.</span><span class="sxs-lookup"><span data-stu-id="2fa1d-120">Note that the number of queues still affects overall performance of the MSMQ Server, but the performance impact is now on a linear rather than exponential scale.</span></span>

## <a name="compatibility-performance-reliability-and-usability-tests"></a><span data-ttu-id="2fa1d-121">Test di compatibilità, prestazioni, affidabilità e usabilità</span><span class="sxs-lookup"><span data-stu-id="2fa1d-121">Compatibility, Performance, Reliability, and Usability Tests</span></span>

<span data-ttu-id="2fa1d-122">Se si usa un numero elevato di code, simulare l'ambiente di produzione su un letto di test, monitorare le prestazioni e analizzare il tempo di avvio del servizio e la velocità effettiva dei messaggi con un numero elevato di code e messaggi presenti nel sistema di test.</span><span class="sxs-lookup"><span data-stu-id="2fa1d-122">If you use a large number of queues, simulate the production environment on a test bed, monitor performance, and analyze the service start-up time and the message throughput with a large number of queues and messages present in the test system.</span></span>

 

 



