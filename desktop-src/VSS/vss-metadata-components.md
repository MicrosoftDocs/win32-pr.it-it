---
description: Fondamentale per organizzare i file di cui eseguire il backup o il ripristino del writer è il concetto di un componente.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: Componenti dei metadati VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307162"
---
# <a name="vss-metadata-components"></a><span data-ttu-id="a7ee7-103">Componenti dei metadati VSS</span><span class="sxs-lookup"><span data-stu-id="a7ee7-103">VSS Metadata Components</span></span>

<span data-ttu-id="a7ee7-104">Fondamentale per organizzare i file di cui eseguire il backup o il ripristino del writer è il concetto di un [*componente*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="a7ee7-104">Critical to organizing which files of which writer are to be backed up or restored is the concept of a [*component*](vssgloss-c.md).</span></span>

<span data-ttu-id="a7ee7-105">I componenti consentono a un writer di indicare a un motore di backup come organizzare i file, le dipendenze tra i file e il tipo di dati che tali file possono contenere.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-105">Components allow a writer to indicate to a backup engine how its files are to be organized, dependencies between files, and what type of data those files can contain.</span></span> <span data-ttu-id="a7ee7-106">Questo consente a un motore di backup di decidere come archiviare i file per ottenere la massima efficienza.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-106">This allows a backup engine to decide how to store files for maximum efficiency.</span></span>

<span data-ttu-id="a7ee7-107">Inoltre, le applicazioni basate su VSS utilizzano componenti come blocchi predefiniti per i relativi metadati e il supporto per la comunicazione writer/richiedente.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-107">In addition, VSS-based applications use components as the building blocks for their metadata and the medium for writer/requester communication.</span></span>

<span data-ttu-id="a7ee7-108">I writer e i richiedenti archiviano le informazioni sui componenti separatamente: nel documento dei metadati del writer e nel documento sui componenti di backup, rispettivamente, e le informazioni sono diverse in ogni rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-108">Writers and requesters store information about components separately—in the Writer Metadata Document and the Backup Components Document, respectively—and the information differs in each representation.</span></span>

<span data-ttu-id="a7ee7-109">Le informazioni sui componenti nei documenti di metadati del writer includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a7ee7-109">Component information in Writer Metadata Documents includes the following:</span></span>

-   <span data-ttu-id="a7ee7-110">Informazioni da un solo Writer in ogni documento</span><span class="sxs-lookup"><span data-stu-id="a7ee7-110">Information from only one writer in each document</span></span>
-   <span data-ttu-id="a7ee7-111">Tutti i componenti del writer, che possono essere inclusi in [*modo esplicito*](vssgloss-e.md) o che devono essere inclusi in modo [*implicito*](vssgloss-i.md) in un'operazione di backup o ripristino</span><span class="sxs-lookup"><span data-stu-id="a7ee7-111">All of that writer's components, whether they can be [*explicitly included*](vssgloss-e.md) or must be [*implicitly included*](vssgloss-i.md) in a backup or restore operation</span></span>
-   <span data-ttu-id="a7ee7-112">Informazioni sul [*percorso logico*](vssgloss-l.md) utilizzate per associare un componente selezionabile per il backup con particolare non selezionabile per i componenti di backup, formando così un set di componenti</span><span class="sxs-lookup"><span data-stu-id="a7ee7-112">[*Logical path*](vssgloss-l.md) information used to associate a selectable for backup component with particular nonselectable for backup components, thus forming a component set</span></span>
-   <span data-ttu-id="a7ee7-113">Informazioni sul [*set di file*](vssgloss-f.md) , ovvero percorso, specifica file e flag di ricorsione, gestite per ogni componente</span><span class="sxs-lookup"><span data-stu-id="a7ee7-113">The [*file set*](vssgloss-f.md) information—path, file specification, and recursion flag—managed for each component</span></span>

<span data-ttu-id="a7ee7-114">I documenti di metadati del writer contengono anche informazioni sui metadati a livello di writer, ad esempio metodi di ripristino e mapping dei percorsi alternativi per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-114">Writer Metadata Documents also contain writer-level metadata information, such as restore methods and alternate location mappings for restore.</span></span> <span data-ttu-id="a7ee7-115">I documenti di metadati del writer sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-115">Writer Metadata Documents are read-only.</span></span> <span data-ttu-id="a7ee7-116">L'interfaccia per l'analisi di queste informazioni è [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).</span><span class="sxs-lookup"><span data-stu-id="a7ee7-116">The interface for examining this information is [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).</span></span>

<span data-ttu-id="a7ee7-117">Le informazioni sul componente nei documenti dei componenti di backup includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a7ee7-117">Component information in Backup Components Documents includes the following:</span></span>

-   <span data-ttu-id="a7ee7-118">Solo informazioni sui componenti inclusi in modo esplicito</span><span class="sxs-lookup"><span data-stu-id="a7ee7-118">Only information on explicitly included components</span></span>
-   <span data-ttu-id="a7ee7-119">Informazioni sui metadati a livello di writer, ad esempio mapping di percorsi alternativi e ripristino</span><span class="sxs-lookup"><span data-stu-id="a7ee7-119">Writer-level metadata information, such as alternate location mappings and restore</span></span>
-   <span data-ttu-id="a7ee7-120">Informazioni sullo stato che descrivono un'operazione di backup o ripristino</span><span class="sxs-lookup"><span data-stu-id="a7ee7-120">State information describing a backup or restore operation</span></span>

<span data-ttu-id="a7ee7-121">I documenti del componente di backup non contengono informazioni sui [*set di file*](vssgloss-f.md)dei componenti.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-121">Backup Component Documents do not contain information on components' [*file sets*](vssgloss-f.md).</span></span> <span data-ttu-id="a7ee7-122">I documenti dei componenti di backup non sono di sola lettura e possono essere modificati dal writer.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-122">Backup Component Documents are not read-only and can be modified by the writer.</span></span> <span data-ttu-id="a7ee7-123">L'interfaccia per l'accesso a queste informazioni è [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).</span><span class="sxs-lookup"><span data-stu-id="a7ee7-123">The interface for accessing this information is [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).</span></span>

<span data-ttu-id="a7ee7-124">Il ciclo di vita e la relazione tra le due espressioni di un componente possono essere interpretate nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="a7ee7-124">The life cycle and relationship between the two expressions of a component can be understood as follows:</span></span>

-   <span data-ttu-id="a7ee7-125">I writer sono responsabili delle definizioni iniziali dei componenti.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-125">Writers are responsible for the initial definitions of components.</span></span>
-   <span data-ttu-id="a7ee7-126">Un richiedente esamina i metadati di tutti i writer e i relativi componenti.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-126">A requester examines the metadata of all writers and their components.</span></span>
-   <span data-ttu-id="a7ee7-127">Dalle informazioni relative a selezione e percorso logico dei componenti, un richiedente determina quali componenti devono essere inclusi in modo esplicito, che possono essere inclusi in modo esplicito, che definiscono i set di componenti e che sono membri dei set di componenti.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-127">From components' selectability and logical path information, a requester determines which components must be explicitly included, which may be explicitly included, which define component sets, and which are members of component sets.</span></span>
-   <span data-ttu-id="a7ee7-128">Un richiedente aggiunge i componenti che richiedono l'inclusione esplicita e include implicitamente sottocomponenti nei [*set di componenti*](/windows) (le cui informazioni non sono presenti nel documento componenti di backup).</span><span class="sxs-lookup"><span data-stu-id="a7ee7-128">A requester adds those components that require explicit inclusion, and implicitly includes subcomponents in [*component sets*](/windows) (whose information is not in the Backup Components Document).</span></span>
-   <span data-ttu-id="a7ee7-129">Quando si gestiscono gli eventi, i writer e i richiedenti possono modificare ed esaminare le informazioni del componente archiviate nel documento componenti di backup per coordinare l'attività.</span><span class="sxs-lookup"><span data-stu-id="a7ee7-129">When handling events, writers and requesters may modify and examine the component information stored in the Backup Components Document to coordinate their activity.</span></span>

<span data-ttu-id="a7ee7-130">Per eseguire correttamente le operazioni di backup e ripristino, sono necessarie sia le informazioni sul componente writer che le versioni del richiedente, che devono essere archiviate con tutti i dati di cui è stato eseguito il backup:</span><span class="sxs-lookup"><span data-stu-id="a7ee7-130">Both the writer and the requester versions component information are required to properly execute backup and restore operations, and both must be stored with any backed-up data:</span></span>

-   [<span data-ttu-id="a7ee7-131">Tipi di componenti</span><span class="sxs-lookup"><span data-stu-id="a7ee7-131">Component Types</span></span>](component-types.md)
-   [<span data-ttu-id="a7ee7-132">Definizione dei componenti per Writer</span><span class="sxs-lookup"><span data-stu-id="a7ee7-132">Definition of Components by Writers</span></span>](definition-of-components-by-writers.md)
-   [<span data-ttu-id="a7ee7-133">Uso dei componenti da parte del richiedente</span><span class="sxs-lookup"><span data-stu-id="a7ee7-133">Use of Components by the Requester</span></span>](use-of-components-by-the-requestor.md)

 

 
