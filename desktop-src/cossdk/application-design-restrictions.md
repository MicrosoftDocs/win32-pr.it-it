---
description: Alcune applicazioni sono progettate in modo da impedire l'installazione di più istanze dell'applicazione in un computer.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Limitazioni relative alla progettazione di applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304739"
---
# <a name="application-design-restrictions"></a><span data-ttu-id="2256b-103">Limitazioni relative alla progettazione di applicazioni</span><span class="sxs-lookup"><span data-stu-id="2256b-103">Application Design Restrictions</span></span>

<span data-ttu-id="2256b-104">Alcune applicazioni sono progettate in modo da impedire l'installazione di più istanze dell'applicazione in un computer.</span><span class="sxs-lookup"><span data-stu-id="2256b-104">Some applications are designed in a way that prevents multiple instances of the application from being installed on a computer.</span></span> <span data-ttu-id="2256b-105">Con tale limitazione, un'applicazione non può utilizzare la funzionalità partizioni.</span><span class="sxs-lookup"><span data-stu-id="2256b-105">With such a limitation, an application cannot make use of the partitions feature.</span></span> <span data-ttu-id="2256b-106">Potrebbe essere necessario modificare le seguenti funzionalità di progettazione dell'applicazione prima di poter utilizzare le partizioni per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2256b-106">The following application design features might need to be modified before partitions can be used for that application.</span></span>

## <a name="tables-and-arrays"></a><span data-ttu-id="2256b-107">Tabelle e matrici</span><span class="sxs-lookup"><span data-stu-id="2256b-107">Tables and Arrays</span></span>

<span data-ttu-id="2256b-108">Alcune applicazioni creano tabelle di database, tabelle in memoria o matrici che utilizzano un CLSID come chiave univoca del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2256b-108">Some applications create database tables, in-memory tables, or arrays that use a CLSID as a unique registry key.</span></span> <span data-ttu-id="2256b-109">In un computer senza partizioni, questa chiave del registro di sistema è in genere computer/CLSID (un CLSID per computer).</span><span class="sxs-lookup"><span data-stu-id="2256b-109">On a computer without partitions, this registry key is typically computer/CLSID (one CLSID per computer).</span></span>

<span data-ttu-id="2256b-110">Viceversa, in un computer con partizioni, questa chiave del registro di sistema è ID computer/partizione/ID applicazione/CLSID (più istanze di un CLSID per computer).</span><span class="sxs-lookup"><span data-stu-id="2256b-110">Conversely, on a computer with partitions, this registry key is computer/partition ID/application ID/CLSID (multiple instances of a CLSID per computer).</span></span> <span data-ttu-id="2256b-111">Poiché la funzionalità partizioni consente l'esistenza di più istanze di un CLSID in un computer, le applicazioni che contengono elementi di progettazione che richiedono un CLSID univoco per computer potrebbero essere compromesse.</span><span class="sxs-lookup"><span data-stu-id="2256b-111">Because the partitions feature allows multiple instances of a CLSID to exist on a computer, applications that contain design elements that require a unique CLSID per computer might be adversely affected.</span></span>

## <a name="global-resources"></a><span data-ttu-id="2256b-112">Risorse globali</span><span class="sxs-lookup"><span data-stu-id="2256b-112">Global Resources</span></span>

<span data-ttu-id="2256b-113">Alcune applicazioni utilizzano risorse globali quali la memoria condivisa, i file di dati e le voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2256b-113">Some applications use global resources such as shared memory, data files, and registry entries.</span></span> <span data-ttu-id="2256b-114">Questo può causare problemi se più istanze di tale applicazione sono in esecuzione simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="2256b-114">This could cause problems if multiple instances of such an application are executing simultaneously.</span></span>

<span data-ttu-id="2256b-115">Se, ad esempio, un componente utilizza memoria condivisa per interagire con altri componenti, sarà necessario modificare il componente in modo che ogni istanza del componente allochi la propria memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="2256b-115">For example, if a component uses shared memory for interacting with other components, the component will need to be modified so that each instance of the component allocates its own shared memory.</span></span>

## <a name="type-libraries"></a><span data-ttu-id="2256b-116">Librerie dei tipi</span><span class="sxs-lookup"><span data-stu-id="2256b-116">Type Libraries</span></span>

<span data-ttu-id="2256b-117">Le librerie dei tipi forniscono informazioni sulle interfacce e i metodi di un componente.</span><span class="sxs-lookup"><span data-stu-id="2256b-117">Type libraries provide information about a component's interfaces and methods.</span></span> <span data-ttu-id="2256b-118">Queste informazioni vengono utilizzate per diversi scopi, incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="2256b-118">This information is used for several purposes, including the following:</span></span>

-   <span data-ttu-id="2256b-119">Marshalling dei dati tra i componenti quando vengono effettuate chiamate di funzione</span><span class="sxs-lookup"><span data-stu-id="2256b-119">Marshaling data between components when function calls are made</span></span>
-   <span data-ttu-id="2256b-120">Supporto dei componenti in coda COM+ e dei servizi eventi COM+</span><span class="sxs-lookup"><span data-stu-id="2256b-120">Helping the COM+ Queued Components and COM+ Events services</span></span>
-   <span data-ttu-id="2256b-121">Fornire le informazioni corrette in un editor di Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2256b-121">Providing the correct information within a Microsoft Visual Basic editor</span></span>

<span data-ttu-id="2256b-122">I riferimenti a una libreria dei tipi vengono installati nel registro di sistema di un computer.</span><span class="sxs-lookup"><span data-stu-id="2256b-122">References to a type library are installed in the registry of a computer.</span></span> <span data-ttu-id="2256b-123">Quando si sviluppano applicazioni che verranno richiamate dall'interno di partizioni, è importante che nel registro di sistema sia installata la versione più recente di una libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="2256b-123">When developing applications that will be invoked from within partitions, it is important that the latest version of a type library is installed in the registry.</span></span> <span data-ttu-id="2256b-124">In questo modo si garantisce che l'editor Visual Basic in uso ottenga informazioni accurate sui metodi disponibili per tale componente.</span><span class="sxs-lookup"><span data-stu-id="2256b-124">This ensures that the Visual Basic editor being used will get accurate information about the methods available for that component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2256b-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2256b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2256b-126">Componenti e partizioni in coda COM+</span><span class="sxs-lookup"><span data-stu-id="2256b-126">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="2256b-127">Implementazione della partizione</span><span class="sxs-lookup"><span data-stu-id="2256b-127">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="2256b-128">Registrazione e attivazione di componenti nelle partizioni</span><span class="sxs-lookup"><span data-stu-id="2256b-128">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="2256b-129">Che cosa sono le partizioni COM+?</span><span class="sxs-lookup"><span data-stu-id="2256b-129">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



