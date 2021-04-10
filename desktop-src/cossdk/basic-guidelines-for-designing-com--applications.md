---
description: Linee guida di base per la progettazione di applicazioni COM+
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Linee guida di base per la progettazione di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127162"
---
# <a name="basic-guidelines-for-designing-com-applications"></a><span data-ttu-id="b2a62-103">Linee guida di base per la progettazione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="b2a62-103">Basic Guidelines for Designing COM+ Applications</span></span>

<span data-ttu-id="b2a62-104">Per sfruttare tutti i vantaggi di COM+, è possibile utilizzare alcune linee guida di base per la creazione di un'applicazione:</span><span class="sxs-lookup"><span data-stu-id="b2a62-104">To take full advantage of COM+, there are a few basic guidelines you can use when creating an application:</span></span>

-   <span data-ttu-id="b2a62-105">**Modellare lo stato durevole come schema di database, utilizzando lo strumento di database preferito.**</span><span class="sxs-lookup"><span data-stu-id="b2a62-105">**Model your durable state as a database schema, using your database tool of choice.**</span></span> <span data-ttu-id="b2a62-106">Quasi tutte le applicazioni devono mantenere lo stato durevole.</span><span class="sxs-lookup"><span data-stu-id="b2a62-106">Almost every application needs to maintain durable state.</span></span> <span data-ttu-id="b2a62-107">I database forniscono i servizi necessari per creare un archivio durevole e scalabile dello stato.</span><span class="sxs-lookup"><span data-stu-id="b2a62-107">Databases provide the services needed to create durable and scalable storage of state.</span></span> <span data-ttu-id="b2a62-108">Pertanto, il primo passaggio nella creazione di un'applicazione COM+ consiste nel modellare lo stato durevole dell'applicazione come una sorta di schema di database.</span><span class="sxs-lookup"><span data-stu-id="b2a62-108">Therefore, the first step in creating a COM+ application is to model the durable state of your application as some sort of database schema.</span></span> <span data-ttu-id="b2a62-109">Il database utilizzato non è rilevante. la maggior parte dei database commerciali è compatibile con COM+.</span><span class="sxs-lookup"><span data-stu-id="b2a62-109">It doesn't really matter what database you use; most commercial databases are compatible with COM+.</span></span> <span data-ttu-id="b2a62-110">Microsoft SQL Server è un valido esempio di una soluzione che è possibile usare.</span><span class="sxs-lookup"><span data-stu-id="b2a62-110">Microsoft SQL Server is a good example of one solution you could use.</span></span>

-   <span data-ttu-id="b2a62-111">**Modellare la logica dell'applicazione COM+ come un set di interfacce COM.**</span><span class="sxs-lookup"><span data-stu-id="b2a62-111">**Model the logic of your COM+ application as a set of COM interfaces.**</span></span> <span data-ttu-id="b2a62-112">Quando si dispone di uno schema che rappresenta le informazioni sullo stato dell'applicazione, modellare gli interscambi che si verificano nell'applicazione come interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="b2a62-112">Once you have a schema that represents the state information of the application, model the interchanges that happen in the application as COM interfaces.</span></span> <span data-ttu-id="b2a62-113">Queste interfacce modellano il comportamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2a62-113">These interfaces will model the behavior of the application.</span></span> <span data-ttu-id="b2a62-114">Si tratta anche della fase di sviluppo in cui è necessario determinare quali servizi COM+ funzionano meglio per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2a62-114">This is also the development stage when you should determine which COM+ services work best for your application.</span></span>

-   <span data-ttu-id="b2a62-115">**Compilare DLL del componente contenenti componenti che utilizzano lo schema di dati fisico ed esporre una visualizzazione logica dei dati ad altri componenti (il primo elemento dell'elenco), nonché i componenti implementati in termini di modello di dati logico (il secondo elemento in questo elenco).**</span><span class="sxs-lookup"><span data-stu-id="b2a62-115">**Build component DLLs that contain components that use the physical data schema and expose a logical view of the data to other components (the first item in this list), as well as components that are implemented in terms of the logical data model (the second item in this list).**</span></span> <span data-ttu-id="b2a62-116">Una volta che si dispone della struttura della logica e delle informazioni sullo stato, è possibile iniziare a scrivere il codice ed è ora possibile scrivere componenti COM basati su DLL che implementano le interfacce in termini di schema definito.</span><span class="sxs-lookup"><span data-stu-id="b2a62-116">Once you have the structure of the logic and the state information, you can begin to write code and can now write DLL-based COM components that implement the interfaces in terms of the defined schema.</span></span> <span data-ttu-id="b2a62-117">I componenti fungono semplicemente da manipolatori per lavorare con le informazioni del database e le DLL dei componenti consentono di compilare un'applicazione COM+ che funziona e che viene ridimensionata correttamente.</span><span class="sxs-lookup"><span data-stu-id="b2a62-117">Your components simply act as manipulators for working with your database information, and your component DLLs enable you build a COM+ application that works and that scales successfully.</span></span>

-   <span data-ttu-id="b2a62-118">**Distribuire i componenti nell'ambiente COM+ utilizzando i servizi COM+ selezionati.**</span><span class="sxs-lookup"><span data-stu-id="b2a62-118">**Deploy the components in the COM+ environment using the COM+ services you've selected.**</span></span> <span data-ttu-id="b2a62-119">Dopo aver compilato l'applicazione, è possibile distribuire l'applicazione in un cluster di rete o di server.</span><span class="sxs-lookup"><span data-stu-id="b2a62-119">Once you have built the application, you can then deploy the application across a network or server cluster.</span></span> <span data-ttu-id="b2a62-120">È ora possibile prendere decisioni in base alle risorse disponibili ed è possibile personalizzare ogni componente per ottenere le prestazioni massime.</span><span class="sxs-lookup"><span data-stu-id="b2a62-120">You can now make decisions based on resources available, and you can tailor each component for maximum performance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2a62-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b2a62-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2a62-122">Presupposti e principi di progettazione COM+</span><span class="sxs-lookup"><span data-stu-id="b2a62-122">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="b2a62-123">Progettazione dell'applicazione COM+ tramite UML</span><span class="sxs-lookup"><span data-stu-id="b2a62-123">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="b2a62-124">Suggerimenti di progettazione generali per l'utilizzo di COM+</span><span class="sxs-lookup"><span data-stu-id="b2a62-124">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="b2a62-125">Ottimizzazione delle interazioni con il livello di logica di business COM+</span><span class="sxs-lookup"><span data-stu-id="b2a62-125">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="b2a62-126">Altri strumenti Microsoft per la creazione di applicazioni distribuite</span><span class="sxs-lookup"><span data-stu-id="b2a62-126">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



