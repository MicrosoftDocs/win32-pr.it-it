---
title: Panoramica dello sviluppo dell'interfaccia utente
description: In questa sezione vengono descritte le tre fasi della progettazione dell'interfaccia utente e vengono introdotte le attività generalmente associate a ogni fase.
ms.assetid: ab544cb9-eed3-4575-a8dd-2f5d7b5c575f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b531fb07a1805c14441c81777bbdddad0739e7cb
ms.sourcegitcommit: e5c43274e96cb8fd1b60fc187ef16723e9258367
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/17/2020
ms.locfileid: "104046223"
---
# <a name="overview-of-the-user-interface-development-process"></a><span data-ttu-id="bd4e3-103">Panoramica del processo di sviluppo dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="bd4e3-103">Overview of the User Interface Development Process</span></span>

<span data-ttu-id="bd4e3-104">In questa sezione vengono descritte le tre fasi della progettazione dell'interfaccia utente e vengono introdotte le attività generalmente associate a ogni fase.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-104">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span>

## <a name="the-application-user-interface-and-the-user-experience"></a><span data-ttu-id="bd4e3-105">Interfaccia utente dell'applicazione e esperienza utente</span><span class="sxs-lookup"><span data-stu-id="bd4e3-105">The Application User Interface and the User Experience</span></span>

<span data-ttu-id="bd4e3-106">Per iniziare, è necessario chiarire i termini "interfaccia utente" e "esperienza utente".</span><span class="sxs-lookup"><span data-stu-id="bd4e3-106">To begin, the terms "user interface" and "user experience" must be clarified.</span></span>

<span data-ttu-id="bd4e3-107">L'interfaccia utente di un'applicazione include in genere gli oggetti che un utente Visualizza e interagisce direttamente sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-107">The user interface of an application typically involves those objects that a user sees and interacts with directly on their screen.</span></span> <span data-ttu-id="bd4e3-108">Ad esempio, gli oggetti di questo tipo includono lo spazio del documento, i menu, le finestre di dialogo, le icone, le immagini e le animazioni.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-108">For example, such objects include the document space, menus, dialog boxes, icons, images, and animations.</span></span>

<span data-ttu-id="bd4e3-109">Tuttavia, l'interfaccia utente di un'applicazione è solo un aspetto dell'esperienza utente complessiva.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-109">However, the user interface of an application is only one aspect of the overall user experience.</span></span> <span data-ttu-id="bd4e3-110">Altri aspetti dell'esperienza utente che non sono visibili all'utente, ma sono parte integrante di un'applicazione e critici per la relativa usabilità, includono tempo di avvio, latenza, gestione degli errori e attività automatizzate completate senza interazione diretta dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-110">Other aspects of the user experience that are not visible to the user, but are integral to an application and critical to its usability, include start up time, latency, error handling, and automated tasks that are completed without direct user interaction.</span></span>

<span data-ttu-id="bd4e3-111">In generale, un'interfaccia utente richiede un'azione da un utente per completare un'attività, ma è possibile ottenere un'esperienza utente eccezionale senza alcuna interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-111">In general, a user interface requires action by a user to accomplish a task, while a great user experience can be achieved with no user interface at all.</span></span>

## <a name="user-interface-development"></a><span data-ttu-id="bd4e3-112">Sviluppo dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="bd4e3-112">User Interface Development</span></span>

<span data-ttu-id="bd4e3-113">Per garantire un'esperienza utente corretta, è necessario un approccio bilanciato durante tutto il ciclo di vita dello sviluppo.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-113">Providing a successful user experience requires a balanced approach throughout the development life cycle.</span></span> <span data-ttu-id="bd4e3-114">Per garantire questo bilanciamento, è necessario non solo concentrarsi sull'implementazione della funzionalità necessaria per completare un'attività, ma anche sulla modalità di esposizione dell'attività tramite l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-114">To ensure this balance, you must not only focus on implementing the functionality required to complete a task but also on how the task is exposed through the user interface.</span></span> <span data-ttu-id="bd4e3-115">Tenere presente che l'interfaccia utente non solo funziona, ma deve essere anche utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-115">Remember, the user interface must not only be functional, it must also be usable.</span></span>

<span data-ttu-id="bd4e3-116">Di seguito vengono descritte le fasi tipiche del processo dvelopment dell'interfaccia utente:</span><span class="sxs-lookup"><span data-stu-id="bd4e3-116">The following outlines the typical phases of the user interface dvelopment process:</span></span>

### <a name="designing"></a><span data-ttu-id="bd4e3-117">Progettazione</span><span class="sxs-lookup"><span data-stu-id="bd4e3-117">Designing</span></span>

-   <span data-ttu-id="bd4e3-118">Requisiti funzionali: determinare i requisiti e gli obiettivi iniziali per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-118">Functional requirements – Determine the initial requirements and goals for the application.</span></span>
-   <span data-ttu-id="bd4e3-119">Analisi utente: identificare gli scenari utente e comprendere le esigenze e le aspettative degli utenti per ogni scenario.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-119">User analysis – Identify the user scenarios and understand the needs and expectations of users for each scenario.</span></span>
-   <span data-ttu-id="bd4e3-120">Progettazione concettuale: modellare l'attività sottostante che l'applicazione deve supportare.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-120">Conceptual design – Model the underlying business that the application must support.</span></span>
-   <span data-ttu-id="bd4e3-121">Progettazione logica: progettare il processo e il flusso di informazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-121">Logical design – Design the process and information flow of the application.</span></span>
-   <span data-ttu-id="bd4e3-122">Progettazione fisica: decidere come verrà implementata la progettazione logica su piattaforme fisiche specifiche.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-122">Physical design – Decide how the logical design will be implemented on specific physical platforms.</span></span>

### <a name="implementing"></a><span data-ttu-id="bd4e3-123">Attuazione</span><span class="sxs-lookup"><span data-stu-id="bd4e3-123">Implementing</span></span>

-   <span data-ttu-id="bd4e3-124">Prototipo: sviluppare modelli di carta o di schermate interattive che si concentrano sull'interfaccia e non includono la distrazione degli elementi di progettazione visivi.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-124">Prototype – Develop paper or interactive screen mockups that focus on the interface and don't include distracting visual design elements.</span></span>
-   <span data-ttu-id="bd4e3-125">Costrutto: compila l'applicazione e prepara le richieste di modifica della progettazione.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-125">Construct – Build the application and prepare for design change requests.</span></span>

### <a name="testing"></a><span data-ttu-id="bd4e3-126">Test</span><span class="sxs-lookup"><span data-stu-id="bd4e3-126">Testing</span></span>

-   <span data-ttu-id="bd4e3-127">Test di usabilità: testare l'applicazione con diversi utenti e scenari.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-127">Usability testing – Test the application with various users and scenarios.</span></span>
-   <span data-ttu-id="bd4e3-128">Test di accessibilità: testare l'applicazione con tecnologie accessibili e strumenti di test automatizzati.</span><span class="sxs-lookup"><span data-stu-id="bd4e3-128">Accessibility testing – Test the application with accessible technologies and automated test tools.</span></span>

 

 




