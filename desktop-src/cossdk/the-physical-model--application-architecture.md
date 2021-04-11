---
description: Una volta completati i modelli concettuali e logici, è possibile prendere decisioni sull'implementazione fisica dell'applicazione.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: "Modello fisico: architettura dell'applicazione"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127542"
---
# <a name="the-physical-model-application-architecture"></a><span data-ttu-id="fb34f-103">Modello fisico: architettura dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="fb34f-103">The Physical Model: Application Architecture</span></span>

<span data-ttu-id="fb34f-104">Una volta completati i modelli concettuali e logici, è possibile prendere decisioni sull'implementazione fisica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb34f-104">After the conceptual and logical models are complete, you can make decisions on the physical implementation of the application.</span></span> <span data-ttu-id="fb34f-105">Per creare il modello fisico, è necessario conoscere la posizione dei vari servizi dell'applicazione e il modo in cui devono essere implementati.</span><span class="sxs-lookup"><span data-stu-id="fb34f-105">To create the physical model, you must understand where the various services of the application should be located and how they should be implemented.</span></span> <span data-ttu-id="fb34f-106">Determinare la posizione in cui risiedono i servizi deve precedere il modo in cui verranno implementati i servizi.</span><span class="sxs-lookup"><span data-stu-id="fb34f-106">Determining where various services reside should come before how the services will be implemented.</span></span>

<span data-ttu-id="fb34f-107">Una regola di base per determinare la posizione in cui risiedono i diversi servizi è la seguente: inserire il componente in cui viene usato.</span><span class="sxs-lookup"><span data-stu-id="fb34f-107">One basic rule for determining where various services reside is this: Put the component where it is being used.</span></span> <span data-ttu-id="fb34f-108">Se, ad esempio, un componente Visualizza informazioni per il client di base, deve essere installato nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fb34f-108">If, for example, a component displays information for the base client, it should go on the user's computer.</span></span> <span data-ttu-id="fb34f-109">Se un componente convalida le informazioni dal client di base, deve risiedere anche nel computer del client di base.</span><span class="sxs-lookup"><span data-stu-id="fb34f-109">If a component validates information from the base client, it should also reside on the base client's computer.</span></span> <span data-ttu-id="fb34f-110">Se un componente Aggiorna le informazioni in un database, dovrebbe risiedere nel server di database.</span><span class="sxs-lookup"><span data-stu-id="fb34f-110">If a component updates information in a database, it should reside on the database server.</span></span>

<span data-ttu-id="fb34f-111">Esistono, naturalmente, considerazioni aggiuntive che fanno eccezioni a questa regola.</span><span class="sxs-lookup"><span data-stu-id="fb34f-111">There are, of course, additional considerations that make exceptions to this rule.</span></span> <span data-ttu-id="fb34f-112">I problemi di prestazioni e sicurezza possono anche determinare la posizione di un componente.</span><span class="sxs-lookup"><span data-stu-id="fb34f-112">Performance and security issues can also dictate where a component is located.</span></span> <span data-ttu-id="fb34f-113">Considerare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="fb34f-113">Consider the following:</span></span>

-   <span data-ttu-id="fb34f-114">Un componente verrà modificato di frequente, rendendo difficile la distribuzione degli aggiornamenti?</span><span class="sxs-lookup"><span data-stu-id="fb34f-114">Is a component going to change frequently, making distributing updates difficult?</span></span>
-   <span data-ttu-id="fb34f-115">Il componente verrà usato da altre applicazioni, ad esempio un componente comune di verifica della sicurezza?</span><span class="sxs-lookup"><span data-stu-id="fb34f-115">Will the component be used by other applications, such as a common security verification component?</span></span>
-   <span data-ttu-id="fb34f-116">Il componente esegue calcoli lunghi o esegue funzioni, ad esempio la stampa, di cui è possibile eseguire il offload in un server?</span><span class="sxs-lookup"><span data-stu-id="fb34f-116">Does the component make lengthy calculations or performs functions, such as printing, that can be offloaded to a server?</span></span>
-   <span data-ttu-id="fb34f-117">È possibile migliorare la sicurezza di un componente inserendolo in un server?</span><span class="sxs-lookup"><span data-stu-id="fb34f-117">Can the security of a component be enhanced by placing it on a server?</span></span>

<span data-ttu-id="fb34f-118">Individuare correttamente i componenti di un'applicazione può anche isolare il team di sviluppo dalla ricodifica costosa se il sistema o la posizione dei dati cambia.</span><span class="sxs-lookup"><span data-stu-id="fb34f-118">Properly locating components of an application can also insulate the development team from costly recoding if the system or the location of the data changes.</span></span> <span data-ttu-id="fb34f-119">Se ad esempio si inseriscono le regole di accesso ai dati in un livello dati piuttosto che nelle stored procedure, l'applicazione è più facilmente isolata dalla dipendenza da un DBMS specifico.</span><span class="sxs-lookup"><span data-stu-id="fb34f-119">For example, by putting the data access rules in a data layer rather than in stored procedures, the application is more easily insulated from dependence on a specific DBMS.</span></span> <span data-ttu-id="fb34f-120">Non solo le modifiche sono conformi e il test di compartimentato, ma le origini dati possono essere modificate e i dati possono essere distribuiti senza modificare radicalmente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb34f-120">Not only are changes confined and testing compartmentalized, but data sources can be changed and data can be distributed without fundamentally changing the application.</span></span>

<span data-ttu-id="fb34f-121">Infine, l'individuazione dei componenti dovrebbe sfruttare le efficienze del sistema.</span><span class="sxs-lookup"><span data-stu-id="fb34f-121">Finally, locating components should take advantage of system efficiencies.</span></span> <span data-ttu-id="fb34f-122">Il posizionamento di oggetti business in posizioni centralizzate sulla rete è una soluzione conveniente.</span><span class="sxs-lookup"><span data-stu-id="fb34f-122">It is time and cost-effective to place business objects in centralized locations on the network.</span></span> <span data-ttu-id="fb34f-123">Gli oggetti possono essere condivisi tra le applicazioni e il testing unità può essere eseguito prima della distribuzione di qualsiasi componente.</span><span class="sxs-lookup"><span data-stu-id="fb34f-123">Objects can be shared among applications, and unit testing can be done before any components are deployed.</span></span> <span data-ttu-id="fb34f-124">È anche possibile ridurre i costi di manutenzione perché le modifiche alle regole si verificano solo in un singolo punto.</span><span class="sxs-lookup"><span data-stu-id="fb34f-124">Maintenance costs can also be decreased because rule changes occur only at a single point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb34f-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb34f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb34f-126">Modello concettuale: requisiti delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="fb34f-126">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
</dt> <dt>

[<span data-ttu-id="fb34f-127">Modello logico: definizione dell'applicazione e pianificazione</span><span class="sxs-lookup"><span data-stu-id="fb34f-127">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



