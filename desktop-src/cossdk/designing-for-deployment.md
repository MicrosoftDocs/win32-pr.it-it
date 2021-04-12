---
description: Progettazione per la distribuzione
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Progettazione per la distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483045"
---
# <a name="designing-for-deployment"></a><span data-ttu-id="a29b1-103">Progettazione per la distribuzione</span><span class="sxs-lookup"><span data-stu-id="a29b1-103">Designing for Deployment</span></span>

<span data-ttu-id="a29b1-104">La pianificazione dell'ambito delle applicazioni COM+ è un'attività di progettazione importante da considerare prima.</span><span class="sxs-lookup"><span data-stu-id="a29b1-104">Planning the scope of COM+ applications is an important design task you should consider early on.</span></span> <span data-ttu-id="a29b1-105">I sistemi distribuiti che devono essere eseguiti utilizzando COM+ devono essere progettati per la distribuzione con la quantità minima di configurazione singola e per utilizzare in modo più efficiente ogni processo.</span><span class="sxs-lookup"><span data-stu-id="a29b1-105">Distributed systems that are intended to run using COM+ should be designed for deployment with the least amount of individual configuration and to most efficiently use each process.</span></span> <span data-ttu-id="a29b1-106">Sono inoltre disponibili tecniche che consentono di ottenere prestazioni ottimali quando si distribuisce un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="a29b1-106">There are also techniques you can use that will enable you to achieve optimal performance when deploying a COM+ application.</span></span> <span data-ttu-id="a29b1-107">Per ulteriori informazioni, vedere [distribuzione per una comunicazione più rapida](deploying-for-faster-communication.md).</span><span class="sxs-lookup"><span data-stu-id="a29b1-107">(For more information, see [Deploying for Faster Communication](deploying-for-faster-communication.md).)</span></span>

<span data-ttu-id="a29b1-108">Quando viene visualizzato con lo strumento di amministrazione Servizi componenti, ogni applicazione COM+ viene visualizzata come una cartella all'interno della quale vengono raggruppati logicamente i set di componenti.</span><span class="sxs-lookup"><span data-stu-id="a29b1-108">When viewed with the Component Services administrative tool, each COM+ application appears as a folder within which sets of components are logically grouped.</span></span> <span data-ttu-id="a29b1-109">Sebbene sia possibile spostare singoli componenti tra cartelle dei **componenti** dell'applicazione com+ (in altre parole, da un'applicazione a un'altra), diversi servizi impostati a livello di applicazione com+, ad esempio la sicurezza, possono variare.</span><span class="sxs-lookup"><span data-stu-id="a29b1-109">While you can move individual components between COM+ application **Components** folders (in other words, from one application to another), several services set at the COM+ application level, such as security, may differ.</span></span> <span data-ttu-id="a29b1-110">Queste impostazioni del servizio possono influire sulla portabilità.</span><span class="sxs-lookup"><span data-stu-id="a29b1-110">These service settings can affect portability.</span></span>

## <a name="a-com-server-application-defines-a-process-boundary"></a><span data-ttu-id="a29b1-111">Un'applicazione server COM+ definisce un limite di processo</span><span class="sxs-lookup"><span data-stu-id="a29b1-111">A COM+ Server Application Defines a Process Boundary</span></span>

<span data-ttu-id="a29b1-112">Quando si crea una nuova applicazione server COM+, si definisce realmente un nuovo limite di processo.</span><span class="sxs-lookup"><span data-stu-id="a29b1-112">When you create a new COM+ server application, you are really defining a new process boundary.</span></span> <span data-ttu-id="a29b1-113">Si noti l'eccezione per le applicazioni di libreria descritte di seguito. Questo processo diventa l'istanza dell'applicazione di controllo per i componenti contenuti nell'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="a29b1-113">(Note the exception for library applications explained below.) This process becomes the controlling application instance for the components that are contained in the COM+ application.</span></span> <span data-ttu-id="a29b1-114">Tutti questi componenti vengono eseguiti in-process in una nuova istanza del programma eseguibile COM+ ogni volta che un programma chiama in un'applicazione COM+ per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="a29b1-114">These components all run in-process in a new instance of the COM+ executable program whenever a program calls into a COM+ application for the first time.</span></span> <span data-ttu-id="a29b1-115">Ciò significa che tutti i componenti all'interno di una determinata cartella dei **componenti** dell'applicazione com+ vengono eseguiti in un singolo spazio di processo che funge da server DCOM.</span><span class="sxs-lookup"><span data-stu-id="a29b1-115">This means that all of the components within a given COM+ application's **Components** folder run in a single process space that serves as the DCOM server.</span></span> <span data-ttu-id="a29b1-116">All'interno dell'applicazione COM+, COM+ gestisce la memoria, coordinando il Distributed Transaction Coordinator (DTC), l'attivazione dell'istanza del componente JIT, il rilevamento e il recupero di arresti anomali e la protezione basata sui ruoli.</span><span class="sxs-lookup"><span data-stu-id="a29b1-116">Within the COM+ application, COM+ manages memory, coordination with the Distributed Transaction Coordinator (DTC), just-in-time component instance activation, crash detection and recovery, and role-based security.</span></span>

## <a name="calling-across-com-application-boundaries"></a><span data-ttu-id="a29b1-117">Chiamata attraverso i limiti dell'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="a29b1-117">Calling Across COM+ Application Boundaries</span></span>

<span data-ttu-id="a29b1-118">Poiché ogni applicazione COM+ viene normalmente implementata come file eseguibile separato, l'effetto della suddivisione di un'applicazione distribuita in più applicazioni COM+ introduce chiamate COM out-of-process quando i componenti di un'applicazione COM+ chiamano i componenti in un'altra applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="a29b1-118">Because each COM+ application normally is implemented as a separate executable, the effect of splitting a distributed application across multiple COM+ applications introduces out-of-process COM calls when components in one COM+ application call the components in another COM+ application.</span></span> <span data-ttu-id="a29b1-119">In questo modo si introduce un calo delle prestazioni a causa del carico aggiuntivo che il marshalling dei parametri COM nei processi impone.</span><span class="sxs-lookup"><span data-stu-id="a29b1-119">This introduces performance degradation due to the extra burden that marshaling COM parameters across processes imposes.</span></span>

> [!Note]  
> <span data-ttu-id="a29b1-120">Non vi sono problemi intrinseci che incorrano a questa riduzione delle prestazioni. è sufficiente tenere presente che si verificherà.</span><span class="sxs-lookup"><span data-stu-id="a29b1-120">There is nothing inherently wrong with incurring this performance penalty; you just need to be aware that it is going to occur.</span></span> <span data-ttu-id="a29b1-121">A seconda del tempo di risposta richiesto, del numero di utenti che richiederanno simultaneamente servizi aziendali e del carico di avvio aggiunto che ogni componente aggiunge a ogni applicazione COM+, è accettabile che l'impatto sulle prestazioni sia attribuibile alle chiamate tra applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a29b1-121">Depending on the required response time, the number of users that will simultaneously request business services, and the added start-up burden that each component adds to each COM+ application, you may find that the performance hit attributable to cross-application calls is acceptable.</span></span>

 

<span data-ttu-id="a29b1-122">Una possibilità che elimina la riduzione delle prestazioni della chiamata attraverso i limiti dell'applicazione COM+ consiste nel contrassegnare un'applicazione COM+ specifica come applicazione di libreria.</span><span class="sxs-lookup"><span data-stu-id="a29b1-122">One possibility that eliminates the performance penalty of calling across COM+ application boundaries is to mark a given COM+ application as a library application.</span></span> <span data-ttu-id="a29b1-123">Un'applicazione libreria COM+ viene eseguita nel processo del client che la crea.</span><span class="sxs-lookup"><span data-stu-id="a29b1-123">A COM+ library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="a29b1-124">Naturalmente, nessun miglioramento delle prestazioni ha un costo zero.</span><span class="sxs-lookup"><span data-stu-id="a29b1-124">Of course, no performance gain has zero cost.</span></span> <span data-ttu-id="a29b1-125">In questo caso, il compromesso riguarda le limitazioni delle applicazioni di libreria COM+.</span><span class="sxs-lookup"><span data-stu-id="a29b1-125">In this case, the trade-off involves the limitations of COM+ library applications.</span></span> <span data-ttu-id="a29b1-126">Sebbene un'applicazione di libreria possa utilizzare la protezione basata sui ruoli, non è in grado di supportare i componenti in coda o l'accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="a29b1-126">While a library application can use role-based security, it cannot support queued components or remote access.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a29b1-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a29b1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a29b1-128">Distribuzione per una comunicazione più veloce</span><span class="sxs-lookup"><span data-stu-id="a29b1-128">Deploying for Faster Communication</span></span>](deploying-for-faster-communication.md)
</dt> <dt>

[<span data-ttu-id="a29b1-129">Progettazione per la disponibilità</span><span class="sxs-lookup"><span data-stu-id="a29b1-129">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="a29b1-130">Progettazione per la scalabilità</span><span class="sxs-lookup"><span data-stu-id="a29b1-130">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="a29b1-131">Progettazione per la sicurezza</span><span class="sxs-lookup"><span data-stu-id="a29b1-131">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



