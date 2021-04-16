---
description: La disponibilità è la capacità di un'applicazione di tollerare gli errori nelle risorse del server.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Progettazione per la disponibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523546"
---
# <a name="designing-for-availability"></a><span data-ttu-id="bf879-103">Progettazione per la disponibilità</span><span class="sxs-lookup"><span data-stu-id="bf879-103">Designing for Availability</span></span>

<span data-ttu-id="bf879-104">La disponibilità è la capacità di un'applicazione di tollerare gli errori nelle risorse del server.</span><span class="sxs-lookup"><span data-stu-id="bf879-104">Availability is the ability of an application to tolerate failures in server resources.</span></span> <span data-ttu-id="bf879-105">Ciò significa che il client continua a essere gestito attraverso l'errore e che, idealmente, l'errore è trasparente per il client.</span><span class="sxs-lookup"><span data-stu-id="bf879-105">This means that the client continues to be served through the failure and that, ideally, the failure is transparent to the client.</span></span> <span data-ttu-id="bf879-106">Ovviamente, l'errore può provenire da origini hardware o software, quindi è necessario svilupparle per entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="bf879-106">Obviously, the failure can come from either hardware or software sources, so you must develop for both cases.</span></span>

<span data-ttu-id="bf879-107">La disponibilità può essere influenzata dai fattori seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf879-107">Availability can be affected by the following factors:</span></span>

-   <span data-ttu-id="bf879-108">Modello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="bf879-108">Application model.</span></span> <span data-ttu-id="bf879-109">Per la massima disponibilità, assicurarsi che la logica dell'applicazione critica venga eseguita utilizzando il servizio [transazioni com+](com--transactions.md) .</span><span class="sxs-lookup"><span data-stu-id="bf879-109">For highest availability, ensure that the critical application logic is conducted using the [COM+ transactions](com--transactions.md) service.</span></span> <span data-ttu-id="bf879-110">Inoltre, l'utilizzo di un meccanismo di compensazione può essere efficace per garantire che le risorse rimangano in uno stato integro dopo gli errori.</span><span class="sxs-lookup"><span data-stu-id="bf879-110">In addition, using a compensation mechanism can be effective in ensuring that resources remain in a healthy state after failures.</span></span>
-   <span data-ttu-id="bf879-111">Modello client.</span><span class="sxs-lookup"><span data-stu-id="bf879-111">Client model.</span></span> <span data-ttu-id="bf879-112">Integrare la logica di "tentativi in caso di errore" nell'applicazione client e cercare una riduzione del livello di prestazioni dell'applicazione se le risorse o i servizi non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="bf879-112">Integrate "retry on failure" logic into the client application, and strive for a graceful degradation in the application if resources or services are unavailable.</span></span> <span data-ttu-id="bf879-113">Comprendere il comportamento previsto dal client dall'applicazione e creare una progettazione che consenta alternative quando si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="bf879-113">Understand what the client is expecting from the application, and create a design that allows for alternatives when a failure occurs.</span></span>
-   <span data-ttu-id="bf879-114">Disponibilità dei dati/stato.</span><span class="sxs-lookup"><span data-stu-id="bf879-114">Data/state availability.</span></span> <span data-ttu-id="bf879-115">Per un accesso coerente ai dati persistenti, usare il clustering di Windows per fornire il supporto del failover.</span><span class="sxs-lookup"><span data-stu-id="bf879-115">For consistent access to persistent data, use Windows Clustering to provide failover support.</span></span>
-   <span data-ttu-id="bf879-116">Disponibilità del servizio.</span><span class="sxs-lookup"><span data-stu-id="bf879-116">Service availability.</span></span> <span data-ttu-id="bf879-117">È possibile usare bilanciamento carico di rete per bilanciare il carico delle richieste IP in ingresso in un cluster di server.</span><span class="sxs-lookup"><span data-stu-id="bf879-117">You can use Network Load Balancing to load balance incoming IP requests across a cluster of servers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf879-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf879-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf879-119">Progettazione per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="bf879-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="bf879-120">Progettazione per la scalabilità</span><span class="sxs-lookup"><span data-stu-id="bf879-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="bf879-121">Progettazione per la sicurezza</span><span class="sxs-lookup"><span data-stu-id="bf879-121">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



