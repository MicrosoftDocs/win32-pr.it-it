---
title: Riutilizzo di oggetti
description: Riutilizzo di oggetti
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2020
ms.locfileid: "104516696"
---
# <a name="reusing-objects"></a><span data-ttu-id="311d8-103">Riutilizzo di oggetti</span><span class="sxs-lookup"><span data-stu-id="311d8-103">Reusing Objects</span></span>

<span data-ttu-id="311d8-104">Un obiettivo importante di qualsiasi modello a oggetti è quello di consentire agli autori di oggetti di riutilizzare ed estendere gli oggetti forniti da altri come parti delle proprie implementazioni.</span><span class="sxs-lookup"><span data-stu-id="311d8-104">An important goal of any object model is to enable object authors to reuse and extend objects provided by others as pieces of their own implementations.</span></span> <span data-ttu-id="311d8-105">Un modo per eseguire questa operazione in Microsoft Visual C++ e in altri linguaggi consiste nell'usare l' *ereditarietà dell'implementazione*, che consente a un oggetto di ereditare ("sottoclasse") alcune delle funzioni di un altro oggetto durante l'override di altre funzioni.</span><span class="sxs-lookup"><span data-stu-id="311d8-105">One way to do this in Microsoft Visual C++ and other languages is by using *implementation inheritance*, which allows an object to inherit ("subclass") some of its functions from another object while overriding other functions.</span></span>

<span data-ttu-id="311d8-106">Il problema per l'interazione dell'oggetto a livello con l'ereditarietà dell'implementazione tradizionale è che il contratto (l'interfaccia) tra gli oggetti in una gerarchia di implementazione non è chiaramente definito.</span><span class="sxs-lookup"><span data-stu-id="311d8-106">The problem for systemwide object interaction using traditional implementation inheritance is that the contract (the interface) between objects in an implementation hierarchy is not clearly defined.</span></span> <span data-ttu-id="311d8-107">In realtà, è implicito e ambiguo.</span><span class="sxs-lookup"><span data-stu-id="311d8-107">In fact, it is implicit and ambiguous.</span></span> <span data-ttu-id="311d8-108">Quando l'implementazione dell'oggetto padre o figlio viene modificata, il comportamento dei componenti correlati potrebbe diventare non definito o implementato in modo non stabile.</span><span class="sxs-lookup"><span data-stu-id="311d8-108">When the parent or child object changes its implementation, the behavior of related components might become undefined or unstably implemented.</span></span> <span data-ttu-id="311d8-109">In ogni singola applicazione, in cui l'implementazione può essere gestita da un singolo team di progettazione che Aggiorna contemporaneamente tutti i componenti, questo non è sempre un problema importante.</span><span class="sxs-lookup"><span data-stu-id="311d8-109">In any single application, where the implementation can be managed by a single engineering team that updates all of the components at the same time, this is not always a major concern.</span></span> <span data-ttu-id="311d8-110">In un ambiente in cui i componenti di un team vengono compilati tramite il riutilizzo della scatola nera di altri componenti creati da altri team, questo tipo di instabilità compromette il riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="311d8-110">In an environment where the components of one team are built through black-box reuse of other components built by other teams, this type of instability jeopardizes reuse.</span></span> <span data-ttu-id="311d8-111">Inoltre, l'ereditarietà dell'implementazione di in genere funziona solo all'interno dei limiti del processo.</span><span class="sxs-lookup"><span data-stu-id="311d8-111">Additionally, implementation inheritance usually works only within process boundaries.</span></span> <span data-ttu-id="311d8-112">In questo modo l'ereditarietà tradizionale dell'implementazione non è praticabile per sistemi di grandi dimensioni e in continua evoluzione costituiti da componenti software creati da molti team di progettazione</span><span class="sxs-lookup"><span data-stu-id="311d8-112">This makes traditional implementation inheritance impractical for large, evolving systems composed of software components built by many engineering teams.</span></span>

<span data-ttu-id="311d8-113">La chiave per la creazione di componenti riutilizzabili consiste nell'essere in grado di trattare l'oggetto come una casella opaca.</span><span class="sxs-lookup"><span data-stu-id="311d8-113">The key to building reusable components is to be able to treat the object as an opaque box.</span></span> <span data-ttu-id="311d8-114">Ciò significa che il frammento di codice che tenta di riutilizzare un altro oggetto non conosce nulla e non deve necessariamente conoscere la struttura interna o l'implementazione del componente utilizzato.</span><span class="sxs-lookup"><span data-stu-id="311d8-114">This means that the piece of code attempting to reuse another object knows nothing, and needs to know nothing, about the internal structure or implementation of the component being used.</span></span> <span data-ttu-id="311d8-115">In altre parole, il codice che tenta di riutilizzare un componente dipende dal comportamento dell'oggetto e non dall'implementazione esatta.</span><span class="sxs-lookup"><span data-stu-id="311d8-115">In other words, the code attempting to reuse a component depends on the behavior of the object and not its exact implementation.</span></span>

<span data-ttu-id="311d8-116">Per ottenere la riusabilità nera, COM adotta altri meccanismi di riusabilità stabiliti, ad esempio *contenimento/delega* e *aggregazione*.</span><span class="sxs-lookup"><span data-stu-id="311d8-116">To achieve black-box reusability, COM adopts other established reusability mechanisms such as *containment/delegation* and *aggregation*.</span></span>

> [!NOTE]  
> <span data-ttu-id="311d8-117">Per praticità, l'oggetto da riutilizzare viene chiamato *oggetto interno* e l'oggetto che utilizza tale oggetto interno è l' *oggetto esterno*.</span><span class="sxs-lookup"><span data-stu-id="311d8-117">For convenience, the object being reused is called the *inner object* and the object making use of that inner object is the *outer object*.</span></span>

 

<span data-ttu-id="311d8-118">È importante ricordare in entrambi i meccanismi il modo in cui l'oggetto esterno appare ai client.</span><span class="sxs-lookup"><span data-stu-id="311d8-118">It is important to remember in both these mechanisms how the outer object appears to its clients.</span></span> <span data-ttu-id="311d8-119">Per quanto riguarda i client, entrambi gli oggetti implementano qualsiasi interfaccia a cui il client può ottenere un puntatore.</span><span class="sxs-lookup"><span data-stu-id="311d8-119">As far as the clients are concerned, both objects implement any interfaces to which the client can get a pointer.</span></span> <span data-ttu-id="311d8-120">Il client considera l'oggetto esterno come una casella opaca e pertanto non è rilevante, né deve preoccuparsi, sulla struttura interna del objectâ esterno, il client si occupa solo del comportamento.</span><span class="sxs-lookup"><span data-stu-id="311d8-120">The client treats the outer object as an opaque box and therefore does not care, nor does it need to care, about the internal structure of the outer objectâ€”the client cares only about behavior.</span></span>

<span data-ttu-id="311d8-121">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="311d8-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="311d8-122">Contenimento/delega</span><span class="sxs-lookup"><span data-stu-id="311d8-122">Containment/Delegation</span></span>](containment-delegation.md)
-   [<span data-ttu-id="311d8-123">Aggregazione</span><span class="sxs-lookup"><span data-stu-id="311d8-123">Aggregation</span></span>](aggregation.md)

 

 




