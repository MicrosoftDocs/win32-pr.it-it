---
description: Un'applicazione COM+ è l'unità primaria di amministrazione e protezione per i servizi componenti ed è costituita da un gruppo di componenti COM che in genere eseguono funzioni correlate.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Panoramica dell'applicazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "106320227"
---
# <a name="com-application-overview"></a><span data-ttu-id="9a29b-103">Panoramica dell'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="9a29b-103">COM+ Application Overview</span></span>

<span data-ttu-id="9a29b-104">Un'applicazione COM+ è l'unità primaria di amministrazione e protezione per i servizi componenti ed è costituita da un gruppo di componenti COM che in genere eseguono funzioni correlate.</span><span class="sxs-lookup"><span data-stu-id="9a29b-104">A COM+ application is the primary unit of administration and security for Component Services and consists of a group of COM components that generally perform related functions.</span></span> <span data-ttu-id="9a29b-105">Questi componenti sono ulteriormente costituiti da interfacce e metodi, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="9a29b-105">These components further consist of interfaces and methods, as shown in the following illustration.</span></span>

![Diagramma che mostra le interfacce e i metodi all'interno di caselle, in ordine di metodo all'interno di un componente all'interno dell'applicazione COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

<span data-ttu-id="9a29b-107">È possibile utilizzare lo strumento di amministrazione Servizi componenti per creare nuove applicazioni COM+, aggiungere componenti alle applicazioni e impostare gli attributi per un'applicazione e i relativi componenti.</span><span class="sxs-lookup"><span data-stu-id="9a29b-107">You can use the Component Services administrative tool to create new COM+ applications, add components to applications, and set the attributes for an application and its components.</span></span>

<span data-ttu-id="9a29b-108">Grazie alla creazione di gruppi logici di componenti COM come applicazioni COM+, è possibile sfruttare i vantaggi di COM+ seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a29b-108">By creating logical groups of COM components as COM+ applications, you can take advantage of the following benefits of COM+:</span></span>

-   <span data-ttu-id="9a29b-109">Un ambito di distribuzione per i componenti COM.</span><span class="sxs-lookup"><span data-stu-id="9a29b-109">A deployment scope for COM components.</span></span>
-   <span data-ttu-id="9a29b-110">Un ambito di configurazione comune per i componenti COM, inclusi i limiti di sicurezza e l'accodamento.</span><span class="sxs-lookup"><span data-stu-id="9a29b-110">A common configuration scope for COM components, including security boundaries and queuing.</span></span>
-   <span data-ttu-id="9a29b-111">Archiviazione di attributi componente non fornita dallo sviluppatore del componente, ad esempio transazioni e sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a29b-111">Storage of component attributes not provided by the component developer (for example, transactions and synchronization).</span></span>
-   <span data-ttu-id="9a29b-112">Librerie a collegamento dinamico (dll) del componente caricate in processi (DLLHost.exe) su richiesta.</span><span class="sxs-lookup"><span data-stu-id="9a29b-112">Component dynamic-link libraries (DLLs) loaded into processes (DLLHost.exe) on demand.</span></span>
-   <span data-ttu-id="9a29b-113">Processi del server gestito per ospitare i componenti.</span><span class="sxs-lookup"><span data-stu-id="9a29b-113">Managed server processes to host components.</span></span>
-   <span data-ttu-id="9a29b-114">Creazione e gestione dei thread utilizzati dai componenti di.</span><span class="sxs-lookup"><span data-stu-id="9a29b-114">Creation and management of threads used by components.</span></span>
-   <span data-ttu-id="9a29b-115">Accesso all'oggetto di contesto per i dispenser di risorse, che consente di associare automaticamente le risorse acquisite al contesto.</span><span class="sxs-lookup"><span data-stu-id="9a29b-115">Access to the context object for resource dispensers, allowing acquired resources to be automatically associated with the context.</span></span> <span data-ttu-id="9a29b-116">Per ulteriori informazioni sui componenti COM e i contesti, vedere [contesti com+](com--contexts.md).</span><span class="sxs-lookup"><span data-stu-id="9a29b-116">(For more information on COM components and contexts, see [COM+ Contexts](com--contexts.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a29b-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a29b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a29b-118">Sviluppo di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="9a29b-118">Developing COM+ Applications</span></span>](developing-com--applications.md)
</dt> <dt>

[<span data-ttu-id="9a29b-119">Parti di un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="9a29b-119">Parts of a COM+ Application</span></span>](parts-of-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="9a29b-120">Tipi di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="9a29b-120">Types of COM+ Applications</span></span>](types-of-com--applications.md)
</dt> </dl>

 

 



