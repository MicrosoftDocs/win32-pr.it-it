---
description: Quando si sviluppano applicazioni COM+, le attività principali includono la progettazione di componenti COM per incapsulare la logica dell'applicazione e l'integrazione di questi componenti in un'applicazione COM+, la creazione dell'applicazione COM+ e l'amministrazione dell'applicazione tramite la distribuzione e la manutenzione.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Sviluppo di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523242"
---
# <a name="developing-com-applications"></a><span data-ttu-id="5f61d-103">Sviluppo di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="5f61d-103">Developing COM+ Applications</span></span>

<span data-ttu-id="5f61d-104">Quando si sviluppano applicazioni COM+, le attività principali includono la progettazione di componenti COM per incapsulare la logica dell'applicazione e l'integrazione di questi componenti in un'applicazione COM+, la creazione dell'applicazione COM+ e l'amministrazione dell'applicazione tramite la distribuzione e la manutenzione.</span><span class="sxs-lookup"><span data-stu-id="5f61d-104">When developing COM+ applications, the principal tasks include designing COM components to encapsulate application logic and integrating these components into a COM+ application, creating the COM+ application, and administering the application through deployment and maintenance.</span></span>

## <a name="designing-com-components"></a><span data-ttu-id="5f61d-105">Progettazione di componenti COM</span><span class="sxs-lookup"><span data-stu-id="5f61d-105">Designing COM Components</span></span>

<span data-ttu-id="5f61d-106">Nei passaggi seguenti viene descritta una procedura generale per la progettazione di un componente efficace:</span><span class="sxs-lookup"><span data-stu-id="5f61d-106">The following steps describe a general procedure for good component design:</span></span>

1.  <span data-ttu-id="5f61d-107">Definire le classi COM e le classi di implementazione.</span><span class="sxs-lookup"><span data-stu-id="5f61d-107">Define the COM classes and implementation classes.</span></span>
2.  <span data-ttu-id="5f61d-108">Raggruppare le classi in componenti.</span><span class="sxs-lookup"><span data-stu-id="5f61d-108">Group the classes into components.</span></span>
3.  <span data-ttu-id="5f61d-109">Selezionare il set di servizi COM+ per il componente, anche se non vengono specificati tutti quando si sviluppa il componente.</span><span class="sxs-lookup"><span data-stu-id="5f61d-109">Select the set of COM+ services for your component, even if you do not specify all of them when developing the component.</span></span> <span data-ttu-id="5f61d-110">Questi servizi possono essere specificati in un secondo momento utilizzando lo strumento di amministrazione Servizi componenti o il modello a oggetti di amministrazione COM+. per ulteriori informazioni sul modello a oggetti di amministrazione com+, vedere [automazione dell'amministrazione com+](automating-com--administration.md) .</span><span class="sxs-lookup"><span data-stu-id="5f61d-110">These services can later be specified using the Component Services administrative tool or the COM+ administration object model (See [Automating COM+ Administration](automating-com--administration.md) for more information about the COM+ administration object model.)</span></span>

## <a name="creating-the-com-application"></a><span data-ttu-id="5f61d-111">Creazione dell'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="5f61d-111">Creating the COM+ Application</span></span>

<span data-ttu-id="5f61d-112">Dopo aver progettato i componenti COM, lo sviluppatore integra i componenti in un'applicazione COM+ e configura l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f61d-112">After designing the COM components, the developer integrates the components into a COM+ application and configures the application.</span></span> <span data-ttu-id="5f61d-113">I passaggi seguenti descrivono il processo:</span><span class="sxs-lookup"><span data-stu-id="5f61d-113">The following steps describe the process:</span></span>

1.  <span data-ttu-id="5f61d-114">Integrare i componenti in un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="5f61d-114">Integrate the components into a COM+ application.</span></span> <span data-ttu-id="5f61d-115">È possibile integrare i componenti in un'applicazione COM+ esistente o creare una nuova applicazione (vuota) per i componenti.</span><span class="sxs-lookup"><span data-stu-id="5f61d-115">You can integrate the components into an existing COM+ application or create a new (empty) application for the components.</span></span> <span data-ttu-id="5f61d-116">Vedere [creazione di applicazioni com+](creating-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="5f61d-116">(See [Creating COM+ Applications](creating-com--applications.md).)</span></span>
2.  <span data-ttu-id="5f61d-117">Specificare il set di attributi corretto per ogni classe (se presente) e se non è specificato nello strumento di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="5f61d-117">Specify the correct set of attributes for each of the classes (if any, and if not specified in the development tool).</span></span> <span data-ttu-id="5f61d-118">Questi attributi esprimono le dipendenze dei componenti da qualsiasi servizio COM+ su cui può basarsi l'implementazione (ad esempio, transazioni, componenti in coda, sicurezza, pool di oggetti e attivazione JIT).</span><span class="sxs-lookup"><span data-stu-id="5f61d-118">These attributes express the components dependencies on any COM+ services its implementation might rely on (for example, transactions, Queued Components, Security, Object Pooling, and Just-in-Time Activation).</span></span>
3.  <span data-ttu-id="5f61d-119">Configurare il Framework di sicurezza (ruoli e assegnazione di ruoli a classi, interfacce e metodi).</span><span class="sxs-lookup"><span data-stu-id="5f61d-119">Set up the security framework (roles and assignment of roles to classes, interfaces, and methods).</span></span>
4.  <span data-ttu-id="5f61d-120">Configurare gli attributi specifici dell'ambiente sulle classi e sulle applicazioni, ad esempio le dimensioni predefinite del pool di oggetti.</span><span class="sxs-lookup"><span data-stu-id="5f61d-120">Configure environment-specific attributes on classes and applications (the default object pool size, for example).</span></span> <span data-ttu-id="5f61d-121">Questi attributi specifici dell'ambiente possono essere impostati o modificati in un secondo momento dall'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="5f61d-121">These environment-specific attributes can later be set (or modified) by the system administrator.</span></span>
5.  <span data-ttu-id="5f61d-122">Esportare l'applicazione per la ridistribuzione e la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5f61d-122">Export the application for redistribution and deployment.</span></span>

<span data-ttu-id="5f61d-123">Per informazioni più dettagliate sui passaggi per la progettazione di applicazioni distribuite, vedere [progettazione di applicazioni com+](designing-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="5f61d-123">For more detailed information on the steps in designing distributed applications, see [Designing COM+ Applications](designing-com--applications.md).</span></span>

## <a name="administering-com-applications"></a><span data-ttu-id="5f61d-124">Amministrazione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="5f61d-124">Administering COM+ Applications</span></span>

<span data-ttu-id="5f61d-125">In genere, uno sviluppatore Invia un'applicazione COM+ parzialmente configurata all'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="5f61d-125">Typically, a developer delivers a partially configured COM+ application to the system administrator.</span></span> <span data-ttu-id="5f61d-126">L'amministratore può quindi personalizzare l'applicazione per uno o più ambienti specifici, ad esempio aggiungendo account utente in ruoli e nomi di server in un cluster di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5f61d-126">The administrator can then customize the application for one or more specific environments (for example, by adding user accounts in roles and server names in an application cluster).</span></span> <span data-ttu-id="5f61d-127">Le attività dell'amministratore includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="5f61d-127">The administrator's tasks include the following:</span></span>

-   <span data-ttu-id="5f61d-128">Installazione dell'applicazione COM+ parzialmente configurata in un computer amministrativo.</span><span class="sxs-lookup"><span data-stu-id="5f61d-128">Installing the partially configured COM+ application on an administrative computer.</span></span>
-   <span data-ttu-id="5f61d-129">Fornire attributi specifici dell'ambiente, ad esempio i membri del ruolo e le dimensioni del pool di oggetti.</span><span class="sxs-lookup"><span data-stu-id="5f61d-129">Providing environment-specific attributes, such as role members and object pool size.</span></span>
-   <span data-ttu-id="5f61d-130">Riesportazione dell'applicazione COM+ completamente configurata.</span><span class="sxs-lookup"><span data-stu-id="5f61d-130">Re-exporting the fully configured COM+ application.</span></span>
-   <span data-ttu-id="5f61d-131">Creazione di un proxy di applicazione (se l'applicazione deve essere accessibile in modalità remota).</span><span class="sxs-lookup"><span data-stu-id="5f61d-131">Creating an application proxy (if the application is to be accessed remotely).</span></span>

<span data-ttu-id="5f61d-132">Dopo che un'applicazione è stata completamente configurata per un ambiente specifico, l'amministratore può quindi distribuirla nei computer di test o di produzione.</span><span class="sxs-lookup"><span data-stu-id="5f61d-132">After an application is fully configured for a specific environment, the administrator can then deploy it on test or production machines.</span></span> <span data-ttu-id="5f61d-133">Questa operazione comporta l'installazione dell'applicazione COM+ completamente configurata in uno o più computer.</span><span class="sxs-lookup"><span data-stu-id="5f61d-133">This involves installing the fully configured COM+ application on one or more computers.</span></span>

<span data-ttu-id="5f61d-134">Per informazioni dettagliate sulle procedure di amministrazione COM+, vedere lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="5f61d-134">For detailed information on COM+ administration procedures, see the Component Services administrative tool.</span></span>

 

 



