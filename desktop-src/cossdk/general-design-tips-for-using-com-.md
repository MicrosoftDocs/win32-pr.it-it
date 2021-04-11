---
description: La chiave per una progettazione efficace è la pianificazione. Se non si ha familiarità con la progettazione di un'applicazione a tre livelli, vedere la sezione intitolata progettazione dell'applicazione COM+ con UML.
ms.assetid: 463f4154-92f6-46c3-95ff-8513963dcadd
title: Suggerimenti di progettazione generali per l'utilizzo di COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5765259f170b1a98f1abb2d097dfdaec2e09d47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126585"
---
# <a name="general-design-tips-for-using-com"></a><span data-ttu-id="25e58-104">Suggerimenti di progettazione generali per l'utilizzo di COM+</span><span class="sxs-lookup"><span data-stu-id="25e58-104">General Design Tips for Using COM+</span></span>

<span data-ttu-id="25e58-105">La chiave per una progettazione efficace è la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="25e58-105">The key to good design is planning.</span></span> <span data-ttu-id="25e58-106">Se non si ha familiarità con la progettazione di un'applicazione a tre livelli, vedere la sezione intitolata [progettazione dell'applicazione com+ con UML](designing-the-com--application-using-uml.md).</span><span class="sxs-lookup"><span data-stu-id="25e58-106">If you are unfamiliar with designing a three-tier application, see the section entitled [Designing the COM+ Application Using UML](designing-the-com--application-using-uml.md).</span></span>

<span data-ttu-id="25e58-107">Il modo in cui si costruiscono i componenti COM che costituiscono il livello intermedio dell'applicazione COM+ può influenzare notevolmente le prestazioni, la scalabilità e la facilità di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="25e58-107">How you construct the COM components that make up the middle tier of your COM+ application can dramatically affect performance, scalability, and ease of deployment.</span></span> <span data-ttu-id="25e58-108">Negli argomenti seguenti vengono fornite considerazioni di progettazione e suggerimenti di implementazione che è necessario conoscere quando si progettano componenti COM.</span><span class="sxs-lookup"><span data-stu-id="25e58-108">The following topics provide design considerations and implementation tips you should know about when designing COM components.</span></span>



| <span data-ttu-id="25e58-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="25e58-109">Topic</span></span>                                                                   | <span data-ttu-id="25e58-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25e58-110">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25e58-111">Progettazione per la scalabilità</span><span class="sxs-lookup"><span data-stu-id="25e58-111">Designing for Scalability</span></span>](designing-for-scalability.md)<br/>   | <span data-ttu-id="25e58-112">Suggerisce modi per aumentare la scalabilità dell'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="25e58-112">Suggests ways to increase the scalability of your COM+ application.</span></span><br/>                                             |
| [<span data-ttu-id="25e58-113">Progettazione per la disponibilità</span><span class="sxs-lookup"><span data-stu-id="25e58-113">Designing for Availability</span></span>](designing-for-availability.md)<br/> | <span data-ttu-id="25e58-114">Vengono illustrati i servizi che è possibile utilizzare per migliorare la disponibilità delle funzionalità di livello intermedio nelle applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="25e58-114">Discusses services you can use to improve the availability your middle-tier functionality in COM+ applications.</span></span><br/> |
| [<span data-ttu-id="25e58-115">Progettazione per la sicurezza</span><span class="sxs-lookup"><span data-stu-id="25e58-115">Designing for Security</span></span>](designing-for-security.md)<br/>         | <span data-ttu-id="25e58-116">Vengono illustrati i modi per configurare la sicurezza per un'applicazione COM+ in modo più efficiente.</span><span class="sxs-lookup"><span data-stu-id="25e58-116">Discusses ways to most efficiently set up security for a COM+ application.</span></span><br/>                                      |
| [<span data-ttu-id="25e58-117">Progettazione per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="25e58-117">Designing for Deployment</span></span>](designing-for-deployment.md)<br/>     | <span data-ttu-id="25e58-118">Vengono illustrati i modi per ridurre al minimo i problemi di distribuzione durante la progettazione di un'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="25e58-118">Discusses ways to minimize deployment headaches when designing a distributed application.</span></span><br/>                       |



 

<span data-ttu-id="25e58-119">Assicurarsi inoltre di [migliorare le prestazioni con il pool di oggetti](improving-performance-with-object-pooling.md) in modo da utilizzare in modo più efficace il pool di oggetti.</span><span class="sxs-lookup"><span data-stu-id="25e58-119">Also, be sure to see [Improving Performance with Object Pooling](improving-performance-with-object-pooling.md) for ways to most effectively use object pooling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25e58-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25e58-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25e58-121">Presupposti e principi di progettazione COM+</span><span class="sxs-lookup"><span data-stu-id="25e58-121">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="25e58-122">Progettazione dell'applicazione COM+ tramite UML</span><span class="sxs-lookup"><span data-stu-id="25e58-122">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="25e58-123">Ottimizzazione delle interazioni con il livello di logica di business COM+</span><span class="sxs-lookup"><span data-stu-id="25e58-123">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="25e58-124">Altri strumenti Microsoft per la creazione di applicazioni distribuite</span><span class="sxs-lookup"><span data-stu-id="25e58-124">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 




