---
description: In COM+ lo stato temporaneo condiviso per gli oggetti viene gestito tramite Gestione proprietà condivise (SPM). SPM è un dispenser di risorse che è possibile usare per condividere lo stato tra più oggetti all'interno di un processo server.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Concetti di Gestione proprietà condivisi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305146"
---
# <a name="com-shared-property-manager-concepts"></a><span data-ttu-id="d1a9e-104">Concetti di Gestione proprietà condivisi COM+</span><span class="sxs-lookup"><span data-stu-id="d1a9e-104">COM+ Shared Property Manager Concepts</span></span>

<span data-ttu-id="d1a9e-105">In COM+ lo stato temporaneo condiviso per gli oggetti viene gestito tramite Gestione proprietà condivise (SPM).</span><span class="sxs-lookup"><span data-stu-id="d1a9e-105">In COM+, shared transient state for objects is managed by using the shared property manager (SPM).</span></span> <span data-ttu-id="d1a9e-106">SPM è un dispenser di risorse che è possibile usare per condividere lo stato tra più oggetti all'interno di un processo server.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-106">The SPM is a resource dispenser that you can use to share state among multiple objects within a server process.</span></span>

<span data-ttu-id="d1a9e-107">Non è possibile usare le variabili globali in un ambiente distribuito a causa di problemi di concorrenza e conflitti di nomi.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-107">You cannot use global variables in a distributed environment because of concurrency and name collision issues.</span></span> <span data-ttu-id="d1a9e-108">Il gestore delle proprietà condivise Elimina i conflitti di nomi fornendo gruppi di proprietà condivisi, che definiscono spazi dei nomi univoci per le proprietà condivise che contengono.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-108">The shared property manager eliminates name collisions by providing shared property groups, which establish unique namespaces for the shared properties they contain.</span></span> <span data-ttu-id="d1a9e-109">Il SPM implementa anche i blocchi e i semafori per proteggere le proprietà condivise dall'accesso simultaneo, che può comportare la perdita di aggiornamenti e lasciare le proprietà in uno stato imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-109">The SPM also implements locks and semaphores to help protect shared properties from simultaneous access, which could result in lost updates and leave properties in an unpredictable state.</span></span>

> [!Note]  
> <span data-ttu-id="d1a9e-110">Lo stato temporaneo condiviso è quello di informazioni sullo stato mantenute in memoria che non sopravvivono a errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-110">Shared transient state is state information kept in memory that does not survive system failures.</span></span> <span data-ttu-id="d1a9e-111">Le informazioni sono progettate per essere condivise da più oggetti oltre i limiti delle transazioni, ma non tra più processi.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-111">The information is designed to be shared by multiple objects across transaction (but not across process) boundaries.</span></span>

 

<span data-ttu-id="d1a9e-112">Le proprietà condivise archiviate in SPM sono disponibili solo per gli oggetti in esecuzione nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-112">Shared properties stored in the SPM are available only to objects running in the same process.</span></span> <span data-ttu-id="d1a9e-113">Ciò significa che gli oggetti che utilizzeranno la funzione SPM per archiviare i valori e che dovranno avere accesso a questi valori devono essere installati come parte della stessa applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-113">This means that the objects that will use the SPM for storing values and that will need to have access to these values must be installed as part of the same COM+ application.</span></span> <span data-ttu-id="d1a9e-114">È possibile che gli amministratori di sistema sposti le classi COM+ da un pacchetto a un altro dopo che l'applicazione COM+ è stata distribuita.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-114">It is possible for system administrators to move COM+ classes from one package to another after your COM+ application has been deployed.</span></span> <span data-ttu-id="d1a9e-115">Se si fa affidamento su diversi oggetti che condividono le proprietà tramite il SPM, è necessario documentare chiaramente che devono essere installati nella stessa applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-115">If you rely on several objects sharing properties through the SPM, you should clearly document that they must be installed in the same COM+ application.</span></span>

<span data-ttu-id="d1a9e-116">È anche importante per i componenti che condividono le proprietà con lo stesso attributo di attivazione.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-116">It's also important for components sharing properties to have the same activation attribute.</span></span> <span data-ttu-id="d1a9e-117">Se due componenti nello stesso pacchetto hanno attributi di attivazione diversi, in genere non saranno in grado di condividere le proprietà.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-117">If two components in the same package have different activation attributes, they generally won't be able to share properties.</span></span> <span data-ttu-id="d1a9e-118">Se, ad esempio, un componente è configurato per l'esecuzione in un processo client e l'altro è configurato per essere eseguito in un processo server, i relativi oggetti vengono in genere eseguiti in processi diversi anche se si trovano nello stesso pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-118">For example, if one component is configured to run in a client process and the other is configured to run in a server process, their objects will usually run in different processes even though they're in the same package.</span></span>

<span data-ttu-id="d1a9e-119">È sempre necessario creare istanze degli oggetti [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)e [**SharedProperty**](sharedproperty.md) dai componenti com+ anziché da un client di base.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-119">You should always instantiate the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md), and [**SharedProperty**](sharedproperty.md) objects from COM+ components rather than from a base client.</span></span> <span data-ttu-id="d1a9e-120">Se un client di base crea proprietà e gruppi di proprietà condivisi, le proprietà condivise si trovano all'interno del processo client di base, non in un processo server.</span><span class="sxs-lookup"><span data-stu-id="d1a9e-120">If a base client creates shared property groups and properties, the shared properties are inside the base-client process, not in a server process.</span></span> <span data-ttu-id="d1a9e-121">Ciò significa che gli oggetti COM+ non possono condividere le proprietà, a meno che gli oggetti non siano in esecuzione anche nel processo client (che in genere non è un'idea consigliata).</span><span class="sxs-lookup"><span data-stu-id="d1a9e-121">This means the COM+ objects cannot share the properties unless the objects are also running in the client process (which is generally not a good idea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1a9e-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1a9e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1a9e-123">Gestione proprietà condivise COM+</span><span class="sxs-lookup"><span data-stu-id="d1a9e-123">COM+ Shared Property Manager</span></span>](com--shared-property-manager.md)
</dt> <dt>

[<span data-ttu-id="d1a9e-124">Gruppi di proprietà condivise</span><span class="sxs-lookup"><span data-stu-id="d1a9e-124">Shared Property Groups</span></span>](shared-property-groups.md)
</dt> </dl>

 

 



