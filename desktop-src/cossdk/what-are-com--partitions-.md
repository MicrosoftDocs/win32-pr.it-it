---
description: Una partizione COM+ è un contenitore logico che consente l'esecuzione delle applicazioni indipendentemente da altre configurazioni di tali applicazioni.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: Che cosa sono le partizioni COM+?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104132126"
---
# <a name="what-are-com-partitions"></a><span data-ttu-id="284e4-103">Che cosa sono le partizioni COM+?</span><span class="sxs-lookup"><span data-stu-id="284e4-103">What Are COM+ Partitions?</span></span>

<span data-ttu-id="284e4-104">Una partizione COM+ è un contenitore logico che consente l'esecuzione delle applicazioni indipendentemente da altre configurazioni di tali applicazioni.</span><span class="sxs-lookup"><span data-stu-id="284e4-104">A COM+ partition is a logical container that allows applications to run independently of other configurations of those applications.</span></span> <span data-ttu-id="284e4-105">Ogni configurazione di un'applicazione viene installata in una partizione separata e può essere gestita separatamente, in base alle esigenze specifiche degli utenti.</span><span class="sxs-lookup"><span data-stu-id="284e4-105">Each configuration of an application is installed into a separate partition and can be separately managed, according to the specific needs of its users.</span></span>

<span data-ttu-id="284e4-106">Durante l'attivazione di un componente COM+, il servizio partizioni determina la configurazione del componente da attivare, in base all'identità dell'utente che richiede l'attivazione del componente.</span><span class="sxs-lookup"><span data-stu-id="284e4-106">During activation of a COM+ component, the partitions service determines which configuration of the component to activate, based on the identity of the user requesting the component activation.</span></span> <span data-ttu-id="284e4-107">Ad esempio, una singola organizzazione che dispone di due gruppi distinti, produzione e training, potrebbe implementare partizioni COM+ come modo per consentire ai due gruppi di utilizzare configurazioni diverse di un'applicazione COM+ nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="284e4-107">For example, a single organization that has two separate groups, Production and Training, could implement COM+ partitions as a way to allow the two groups to use different configurations of a COM+ application on the same computer.</span></span>

<span data-ttu-id="284e4-108">**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="284e4-108">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="284e4-109">La partizione globale è l'unica partizione COM+ disponibile.</span><span class="sxs-lookup"><span data-stu-id="284e4-109">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="284e4-110">**Windows 2000:** Il servizio partizioni COM+ non è disponibile in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="284e4-110">**Windows 2000:** The COM+ partitions service is not available in Windows 2000.</span></span>

## <a name="benefits-of-using-com-partitions"></a><span data-ttu-id="284e4-111">Vantaggi dell'utilizzo di partizioni COM+</span><span class="sxs-lookup"><span data-stu-id="284e4-111">Benefits of Using COM+ Partitions</span></span>

<span data-ttu-id="284e4-112">L'utilizzo di partizioni COM+ offre diversi vantaggi, tra cui:</span><span class="sxs-lookup"><span data-stu-id="284e4-112">The use of COM+ partitions offers several advantages, including the following:</span></span>

-   <span data-ttu-id="284e4-113">Le organizzazioni possono ridurre il costo totale di proprietà (TCO) usando un minor numero di server di applicazioni fisiche per supportare gli utenti che necessitano di più configurazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="284e4-113">Organizations can lower their total cost of ownership (TCO) by using fewer physical application servers to support users who need multiple application configurations.</span></span>
-   <span data-ttu-id="284e4-114">Il sovraccarico amministrativo è ridotto.</span><span class="sxs-lookup"><span data-stu-id="284e4-114">Administrative overhead is reduced.</span></span> <span data-ttu-id="284e4-115">Anziché dover configurare e gestire più computer, è necessario che gli amministratori configurano e gestiscano solo più partizioni nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="284e4-115">Instead of having to configure and manage multiple computers, administrators need only configure and manage multiple partitions on the same computer.</span></span> <span data-ttu-id="284e4-116">Inoltre, le partizioni possono essere gestite a livello di codice tramite l'aggiunta di una nuova interfaccia di programmazione COM+.</span><span class="sxs-lookup"><span data-stu-id="284e4-116">Furthermore, partitions can be managed programmatically through the addition of a new COM+ programming interface.</span></span>
-   <span data-ttu-id="284e4-117">La sicurezza può essere implementata e gestita in base a una partizione per partizione per utenti locali, utenti di dominio e unità organizzative (OU).</span><span class="sxs-lookup"><span data-stu-id="284e4-117">Security can be implemented and managed on a partition-by-partition basis for local users, domain users, and organizational units (OUs).</span></span>
-   <span data-ttu-id="284e4-118">Programmatori e amministratori possono utilizzare gli strumenti di sviluppo e amministrazione di Microsoft, ad esempio Windows SDK, Active Directory utenti e computer e lo strumento di amministrazione Servizi componenti, per gestire le partizioni COM+.</span><span class="sxs-lookup"><span data-stu-id="284e4-118">Programmers and administrators can use Microsoft's development and administrative tools—such as the Windows SDK, Active Directory Users and Computers, and Component Services administrative tool—to manage COM+ partitions.</span></span> <span data-ttu-id="284e4-119">La funzionalità partizioni è completamente integrata in questi strumenti.</span><span class="sxs-lookup"><span data-stu-id="284e4-119">The partitions feature is fully integrated into these tools.</span></span>

## <a name="primary-usage-scenario"></a><span data-ttu-id="284e4-120">Scenario di utilizzo primario</span><span class="sxs-lookup"><span data-stu-id="284e4-120">Primary Usage Scenario</span></span>

<span data-ttu-id="284e4-121">Un motivo principale per cui i clienti possono distribuire la funzionalità partizioni COM+ consiste nell'ospitare applicazioni basate sul Web.</span><span class="sxs-lookup"><span data-stu-id="284e4-121">A primary reason for customers to deploy the COM+ partitions feature is to host Web-based applications.</span></span> <span data-ttu-id="284e4-122">Si supponga, ad esempio, che una piccola azienda di software sviluppa un'applicazione COM+ da utilizzare per il personale dell'ospedale.</span><span class="sxs-lookup"><span data-stu-id="284e4-122">For example, suppose a small software company develops a COM+ application for use by hospital personnel.</span></span> <span data-ttu-id="284e4-123">L'applicazione, che è un'applicazione basata sul Web distribuita, fornisce agli ospedali un modo per archiviare e recuperare le registrazioni cliniche dei pazienti usando un database SQL Server.</span><span class="sxs-lookup"><span data-stu-id="284e4-123">The application, which is a distributed Web-based application, provides a way for hospitals to store and retrieve patient medical records using a SQL Server database.</span></span>

<span data-ttu-id="284e4-124">Si supponga che la società software abbia tre clienti: Hospital A, Hospital B e Hospital C. Sebbene ogni cliente esegua il lato client dell'applicazione COM+ localmente nei propri computer desktop, il lato server dell'applicazione COM+ risiede nel server Web interno della società software ed è accessibile dai clienti tramite il Web.</span><span class="sxs-lookup"><span data-stu-id="284e4-124">Suppose the software company has three customers: Hospital A, Hospital B, and Hospital C. While each customer runs the client side of the COM+ application locally on its desktop computers, the server side of the COM+ application resides on the software company's in-house web server and is accessed by its customers via the Web.</span></span>

<span data-ttu-id="284e4-125">Poiché ogni ospedale dispone di un proprio set di requisiti di archiviazione e recupero e di un proprio set di dati personalizzati dei pazienti, l'azienda software deve fornire un modo per eseguire contemporaneamente più configurazioni della parte server dell'applicazione nel server Web.</span><span class="sxs-lookup"><span data-stu-id="284e4-125">Because each hospital has its own set of storage and retrieval requirements and its own set of customized patient data, the software company must provide a way for multiple configurations of the server part of the application to be executed simultaneously on the web server.</span></span> <span data-ttu-id="284e4-126">Le partizioni COM+ forniscono una soluzione a questo problema.</span><span class="sxs-lookup"><span data-stu-id="284e4-126">COM+ partitions provide a solution to this problem.</span></span>

<span data-ttu-id="284e4-127">Nella figura seguente viene illustrato lo scenario relativo alle partizioni per l'applicazione COM+ della società software.</span><span class="sxs-lookup"><span data-stu-id="284e4-127">The following illustration shows the partitions scenario for the software company's COM+ application.</span></span>

![Diagramma che mostra uno scenario di partizioni per un'applicazione COM+, con un'applicazione client per l'applicazione server al database di SQL Server.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a><span data-ttu-id="284e4-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="284e4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="284e4-130">Limitazioni relative alla progettazione di applicazioni</span><span class="sxs-lookup"><span data-stu-id="284e4-130">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="284e4-131">Componenti e partizioni in coda COM+</span><span class="sxs-lookup"><span data-stu-id="284e4-131">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="284e4-132">Implementazione della partizione</span><span class="sxs-lookup"><span data-stu-id="284e4-132">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="284e4-133">Registrazione e attivazione di componenti nelle partizioni</span><span class="sxs-lookup"><span data-stu-id="284e4-133">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



