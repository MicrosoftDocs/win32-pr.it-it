---
description: Per lo sviluppo di un'applicazione COM+ corretta è necessario progettare l'architettura dell'applicazione di primo piano.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Progettazione dell'applicazione COM+ tramite UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401423"
---
# <a name="designing-the-com-application-using-uml"></a><span data-ttu-id="ad4ae-103">Progettazione dell'applicazione COM+ tramite UML</span><span class="sxs-lookup"><span data-stu-id="ad4ae-103">Designing the COM+ Application Using UML</span></span>

<span data-ttu-id="ad4ae-104">Per lo sviluppo di un'applicazione COM+ corretta è necessario progettare l'architettura dell'applicazione di primo piano.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-104">Developing a successful COM+ application requires up-front application architectural design.</span></span> <span data-ttu-id="ad4ae-105">Il Unified Modeling Language (UML) è fondamentale per questo sviluppo di progettazione.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-105">The Unified Modeling Language (UML) is key to this design development.</span></span> <span data-ttu-id="ad4ae-106">UML è una notazione di modellazione per i dati e i processi delle applicazioni che combina le procedure consigliate del settore software.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-106">The UML is a modeling notation for application data and processes that combines the best practices of the software industry.</span></span> <span data-ttu-id="ad4ae-107">Poiché UML suddivide l'applicazione in tre visualizzazioni che riflettono l'applicazione, nonché la creazione di pacchetti e l'implementazione, la notazione di modellazione si estende per supportare la modellazione aziendale.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-107">Because the UML breaks the application into three views that reflect the application as well as its packaging and implementation, the modeling notation extends well to support enterprise modeling.</span></span>

<span data-ttu-id="ad4ae-108">UML indirizza tre visualizzazioni dell'applicazione, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ad4ae-108">The UML addresses three views of the application, as follows:</span></span>

-   <span data-ttu-id="ad4ae-109">Visualizzazione statica, modellata da informazioni ricavate da scenari utente e diagrammi classi.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-109">The static view, which is modeled by information taken from user scenarios and class diagrams.</span></span>
-   <span data-ttu-id="ad4ae-110">Visualizzazione dinamica, modellata usando diagrammi di sequenza, collaborazione e transizione di stato.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-110">The dynamic view, which is modeled using sequence, collaboration, and state transition diagrams.</span></span>
-   <span data-ttu-id="ad4ae-111">Visualizzazione funzionale, ovvero la descrizione descrittiva più tradizionale con pseudocodice e specifiche.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-111">The functional view, which is the more traditional descriptive narrative using pseudocode and specifications.</span></span>

<span data-ttu-id="ad4ae-112">Le informazioni per queste visualizzazioni possono essere raccolte seguendo tre passaggi di progettazione che funzionano bene con UML.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-112">The information for these views can be gathered by following three design steps that work well with the UML.</span></span> <span data-ttu-id="ad4ae-113">Prima di scrivere una singola riga di codice, è necessario creare i modelli seguenti:</span><span class="sxs-lookup"><span data-stu-id="ad4ae-113">Before writing a single line of code, you need to create the following models:</span></span>

<dl> <dt>

<span data-ttu-id="ad4ae-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Modello concettuale</span><span class="sxs-lookup"><span data-stu-id="ad4ae-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Conceptual model</span></span>
</dt> <dd>

<span data-ttu-id="ad4ae-115">Decidere quali componenti e servizi sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-115">Decide what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="ad4ae-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Modello logico</span><span class="sxs-lookup"><span data-stu-id="ad4ae-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Logical model</span></span>
</dt> <dd>

<span data-ttu-id="ad4ae-117">Determinare il livello di progettazione logico a cui appartengono.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-117">Determine which logical design tier they belong in.</span></span>

</dd> <dt>

<span data-ttu-id="ad4ae-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Modello fisico</span><span class="sxs-lookup"><span data-stu-id="ad4ae-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Physical model</span></span>
</dt> <dd>

<span data-ttu-id="ad4ae-119">Determinare dove risiedono fisicamente i componenti e il modo in cui devono essere codificati.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-119">Determine where the components reside physically and how they are to be coded.</span></span>

</dd> </dl>

<span data-ttu-id="ad4ae-120">Questi modelli possono essere quindi usati con gli strumenti per i casi basati su UML.</span><span class="sxs-lookup"><span data-stu-id="ad4ae-120">These models can then be used with UML-based CASE tools.</span></span> <span data-ttu-id="ad4ae-121">Per ulteriori informazioni su questi tre modelli di progettazione, vedere gli argomenti seguenti in questa sezione:</span><span class="sxs-lookup"><span data-stu-id="ad4ae-121">For more information on these three design models, see the following topics in this section:</span></span>

-   [<span data-ttu-id="ad4ae-122">Modello concettuale: requisiti delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="ad4ae-122">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
-   [<span data-ttu-id="ad4ae-123">Modello logico: definizione dell'applicazione e pianificazione</span><span class="sxs-lookup"><span data-stu-id="ad4ae-123">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
-   [<span data-ttu-id="ad4ae-124">Modello fisico: architettura dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="ad4ae-124">The Physical Model: Application Architecture</span></span>](the-physical-model--application-architecture.md)

## <a name="related-topics"></a><span data-ttu-id="ad4ae-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad4ae-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad4ae-126">Presupposti e principi di progettazione COM+</span><span class="sxs-lookup"><span data-stu-id="ad4ae-126">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="ad4ae-127">Suggerimenti di progettazione generali per l'utilizzo di COM+</span><span class="sxs-lookup"><span data-stu-id="ad4ae-127">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="ad4ae-128">Ottimizzazione delle interazioni con il livello di logica di business COM+</span><span class="sxs-lookup"><span data-stu-id="ad4ae-128">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="ad4ae-129">Altri strumenti Microsoft per la creazione di applicazioni distribuite</span><span class="sxs-lookup"><span data-stu-id="ad4ae-129">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



