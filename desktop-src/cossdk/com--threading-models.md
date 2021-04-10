---
description: I modelli di threading COM+ sono progettati intorno a una raccolta di oggetti denominata Apartment. Un Apartment è una raccolta di contesti contenuti in un processo.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modelli di threading COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "103761116"
---
# <a name="com-threading-models"></a><span data-ttu-id="4f4bd-104">Modelli di threading COM+</span><span class="sxs-lookup"><span data-stu-id="4f4bd-104">COM+ Threading Models</span></span>

<span data-ttu-id="4f4bd-105">I modelli di threading COM+ sono progettati intorno a una raccolta di oggetti denominata Apartment.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-105">COM+ threading models are designed around an object collection called an apartment.</span></span> <span data-ttu-id="4f4bd-106">Un Apartment è una raccolta di contesti contenuti in un processo, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-106">An apartment is a collection of contexts contained in a process, as shown in the following illustration.</span></span>

![Diagramma che mostra una raccolta di contesti in un'attività, all'interno di un Apartment, all'interno di un processo.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

<span data-ttu-id="4f4bd-108">Le chiamate all'interno di un Apartment sono dirette, mentre le chiamate tra gli appartamenti (out-of-process) sono indirette e richiedono codice del proxy e dello stub.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-108">Calls within an apartment are direct, while calls across apartments (out-of-process) are indirect and require proxy and stub code.</span></span> <span data-ttu-id="4f4bd-109">Gli Apartment consentono oggetti con diverse proprietà di sincronizzazione e rientranza e hanno due categorie: a thread singolo e multithreading.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-109">Apartments allow for objects with different synchronization and reentrancy properties and have two categories: single-threaded and multithreaded.</span></span> <span data-ttu-id="4f4bd-110">Gli oggetti in un Apartment a thread singolo (STA) vengono eseguiti sul thread specifico in cui sono stati creati.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-110">Objects in a single-threaded apartment (STA) execute on the particular thread in which they were created.</span></span> <span data-ttu-id="4f4bd-111">STAs consente l'esecuzione di un solo metodo alla volta.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-111">STAs allow only one method to execute at a time.</span></span> <span data-ttu-id="4f4bd-112">Sono progettate per le interfacce utente e si basano sulla coda di messaggi di Microsoft Windows per elaborare le chiamate in ingresso.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-112">They are designed for user interfaces and rely on the Microsoft Windows message queue to process incoming calls.</span></span>

<span data-ttu-id="4f4bd-113">Gli oggetti in un Apartment a thread multipli (MTA) vengono eseguiti su qualsiasi thread e consentono l'esecuzione simultanea di un numero qualsiasi di metodi.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-113">Objects in a multithreaded apartment (MTA) execute on any thread and allow any number of methods to occur simultaneously.</span></span> <span data-ttu-id="4f4bd-114">Gli MTA supportano il reingresso in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-114">MTAs support reentrance implicitly.</span></span>

<span data-ttu-id="4f4bd-115">Le classi COM+ sono contrassegnate con una proprietà **ThreadingModel** che consente a com+ di creare l'oggetto nell'Apartment appropriato.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-115">COM+ classes are marked with a **ThreadingModel** property that allows COM+ to create the object in the proper apartment.</span></span> <span data-ttu-id="4f4bd-116">Per determinare in quale Apartment viene creato un oggetto, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utilizza la proprietà **ThreadingModel** .</span><span class="sxs-lookup"><span data-stu-id="4f4bd-116">To determine which apartment an object is created in, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) uses the **ThreadingModel** property.</span></span>

<span data-ttu-id="4f4bd-117">I thread devono chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) prima di poter usare com+.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-117">Threads must call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) before they can use COM+.</span></span> <span data-ttu-id="4f4bd-118">In questo modo vengono creati all'interno dell'Apartment e del contesto corretti.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-118">This creates them inside the correct apartment and context.</span></span> <span data-ttu-id="4f4bd-119">L'Apartment del thread principale è determinato come il primo STA chiamato da **CoInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-119">The main thread apartment is determined to be the first STA called by **CoInitializeEx**.</span></span> <span data-ttu-id="4f4bd-120">Questa operazione è in genere associata al thread principale di un processo.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-120">This is usually associated with the main thread of a process.</span></span> <span data-ttu-id="4f4bd-121">**CoInitializeEx** indica il tipo di Apartment richiesto dal thread impostando i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f4bd-121">**CoInitializeEx** indicates the type of apartment required by the thread by setting the following flags:</span></span>

-   <span data-ttu-id="4f4bd-122">**COinit \_ Multithreading**: individua il thread nel singolo Apartment a thread multipli.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-122">**COINIT\_MULTITHREADED**—Locates the thread in the single multithreaded apartment.</span></span>
-   <span data-ttu-id="4f4bd-123">**COinit \_ APARTMENTTHREADED**: inserisce il thread in un nuovo sta.</span><span class="sxs-lookup"><span data-stu-id="4f4bd-123">**COINIT\_APARTMENTTHREADED**—Places the thread into a new STA.</span></span>

<span data-ttu-id="4f4bd-124">Negli argomenti seguenti di questa sezione vengono fornite ulteriori informazioni sull'utilizzo di modelli di threading e di Apartment in COM+:</span><span class="sxs-lookup"><span data-stu-id="4f4bd-124">The following topics in this section provide more information about using threading models and apartments in COM+:</span></span>

-   [<span data-ttu-id="4f4bd-125">Attributo del modello di threading</span><span class="sxs-lookup"><span data-stu-id="4f4bd-125">Threading Model Attribute</span></span>](threading-model-attribute.md)
-   [<span data-ttu-id="4f4bd-126">Appartamenti neutri</span><span class="sxs-lookup"><span data-stu-id="4f4bd-126">Neutral Apartments</span></span>](neutral-apartments.md)

## <a name="related-topics"></a><span data-ttu-id="4f4bd-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f4bd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f4bd-128">Processi, thread e Apartment</span><span class="sxs-lookup"><span data-stu-id="4f4bd-128">Processes, Threads, and Apartments</span></span>](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[<span data-ttu-id="4f4bd-129">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="4f4bd-129">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
