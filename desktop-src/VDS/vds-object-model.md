---
description: Modello a oggetti VDS
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: Modello a oggetti VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234406"
---
# <a name="vds-object-model"></a><span data-ttu-id="976cf-103">Modello a oggetti VDS</span><span class="sxs-lookup"><span data-stu-id="976cf-103">VDS Object Model</span></span>

<span data-ttu-id="976cf-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="976cf-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="976cf-105">VDS consente l'accesso indiretto ai dispositivi di archiviazione basati su host, ad esempio i dischi e i dispositivi CD-ROM, e agli array di dischi gestiti da controller RAID hardware.</span><span class="sxs-lookup"><span data-stu-id="976cf-105">VDS provides indirect access to host-based storage devices, such as disks and CD-ROM devices, and to disk arrays that are managed by hardware RAID controllers.</span></span> <span data-ttu-id="976cf-106">Mentre alcune entità di archiviazione modellano i dispositivi fisici, altri costrutti virtuali del modello: volumi, partizioni e così via.</span><span class="sxs-lookup"><span data-stu-id="976cf-106">While some storage entities model physical devices, others model virtual constructs: volumes, partitions, and so on.</span></span> <span data-ttu-id="976cf-107">Gli oggetti descritti in questo argomento rappresentano le entità fisiche e virtuali di VDS.</span><span class="sxs-lookup"><span data-stu-id="976cf-107">The objects that are described in this topic represent both the physical and virtual entities of VDS.</span></span>

<span data-ttu-id="976cf-108">Le applicazioni chiamano i metodi esposti da tali oggetti e VDS chiama il provider appropriato per eseguire le operazioni di archiviazione richieste.</span><span class="sxs-lookup"><span data-stu-id="976cf-108">Applications call the methods that are exposed by these objects and VDS calls the appropriate provider to perform the requested storage operations.</span></span> <span data-ttu-id="976cf-109">Un'applicazione non chiama mai direttamente un programma provider.</span><span class="sxs-lookup"><span data-stu-id="976cf-109">An application never calls a provider program directly.</span></span>

### <a name="classification-of-objects"></a><span data-ttu-id="976cf-110">Classificazione degli oggetti</span><span class="sxs-lookup"><span data-stu-id="976cf-110">Classification of Objects</span></span>

<span data-ttu-id="976cf-111">Come illustrato nella figura seguente, i programmi del provider software implementano gli oggetti che modellano le entità basate su host. i programmi del provider hardware implementano oggetti che modellano dispositivi RAID hardware interni ed esterni; gli oggetti comuni rimanenti sono indipendenti dal provider o sono implementati da VDS.</span><span class="sxs-lookup"><span data-stu-id="976cf-111">As the following illustration shows, software provider programs implement objects that model host-based entities; hardware provider programs implement objects that model internal and external hardware RAID devices; the remaining common objects are either provider-independent, or are implemented by VDS.</span></span> <span data-ttu-id="976cf-112">Un mandrino, che non è un oggetto VDS, è un termine per supporti di archiviazione generici che comprende gli extent del disco o dell'unità.</span><span class="sxs-lookup"><span data-stu-id="976cf-112">A spindle, which is not a VDS object, is a term for generic storage media that comprises of disk or drive extents.</span></span>

![Diagramma che mostra una classificazione di oggetti, definiti come "oggetti comuni", "oggetti provider software" e "oggetti provider hardware".](images/vdsobjectmodel.png)

<span data-ttu-id="976cf-114">Per ulteriori informazioni sul comportamento di ogni oggetto, selezionare uno degli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="976cf-114">To learn more about the behavior of each object, select from the following topics:</span></span>

-   <span data-ttu-id="976cf-115">Service Loader e oggetti servizio, vedere [Startup and Service Objects](startup-and-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="976cf-115">Service loader and service objects, see [Startup and Service Objects](startup-and-service-objects.md).</span></span>
-   <span data-ttu-id="976cf-116">Enumerazione e oggetti asincroni, vedere [oggetti helper](helper-objects.md).</span><span class="sxs-lookup"><span data-stu-id="976cf-116">Enumeration and async objects, see [Helper Objects](helper-objects.md).</span></span>
-   <span data-ttu-id="976cf-117">Oggetto provider, vedere [oggetto provider](provider-object.md).</span><span class="sxs-lookup"><span data-stu-id="976cf-117">Provider object, see [Provider Object](provider-object.md).</span></span>
-   <span data-ttu-id="976cf-118">Oggetti Pack, disco, volume e volume Plex, vedere [oggetti provider di software](software-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="976cf-118">Pack, disk, volume, and volume plex objects, see [Software Provider Objects](software-provider-objects.md).</span></span>
-   <span data-ttu-id="976cf-119">Oggetti Plex del sottosistema, controller, unità, LUN e LUN, vedere [oggetti provider hardware](hardware-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="976cf-119">Subsystem, controller, drive, LUN, and LUN plex objects, see [Hardware Provider Objects](hardware-provider-objects.md).</span></span>

### <a name="object-creation"></a><span data-ttu-id="976cf-120">Creazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="976cf-120">Object Creation</span></span>

<span data-ttu-id="976cf-121">Il completamento delle operazioni di configurazione e query associate alla creazione di oggetti può richiedere molto tempo. di conseguenza, VDS richiama tutti i metodi in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="976cf-121">The configuration and query operations that are associated with object creation can take considerable time to complete; as such, VDS invokes all methods asynchronously.</span></span> <span data-ttu-id="976cf-122">Il provider di individuazione restituisce tutti gli eventi di completamento, di errore o di modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="976cf-122">The discovering provider returns all completion, error, or state change events.</span></span> <span data-ttu-id="976cf-123">I provider di software registrano inoltre tutti gli errori e le modifiche significative di stato.</span><span class="sxs-lookup"><span data-stu-id="976cf-123">Software providers also log all the errors and significant state changes.</span></span>

### <a name="object-deletion"></a><span data-ttu-id="976cf-124">Eliminazione oggetti</span><span class="sxs-lookup"><span data-stu-id="976cf-124">Object Deletion</span></span>

<span data-ttu-id="976cf-125">Diversi metodi VDS eliminano o trasformano oggetti VDS.</span><span class="sxs-lookup"><span data-stu-id="976cf-125">Several VDS methods delete or transform VDS objects.</span></span> <span data-ttu-id="976cf-126">Un chiamante può mantenere un riferimento, tramite un puntatore a interfaccia, a un oggetto eliminato dopo la restituzione del metodo.</span><span class="sxs-lookup"><span data-stu-id="976cf-126">A caller can hold a reference, by way of an interface pointer, to a deleted object after the method returns.</span></span> <span data-ttu-id="976cf-127">Quando il chiamante rilascia l'interfaccia, VDS Elimina l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="976cf-127">When the caller releases the interface, VDS deletes the object.</span></span>

<span data-ttu-id="976cf-128">Per quanto riguarda l'eliminazione di oggetti, i chiamanti devono evitare di richiamare qualsiasi elemento tranne il metodo [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) su queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="976cf-128">With regard to object deletion, callers should refrain from invoking anything except the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on these interfaces.</span></span> <span data-ttu-id="976cf-129">Il provider deve essere sufficientemente solido per gestire i chiamanti errati; Se un chiamante richiama un metodo su un oggetto eliminato, il provider deve restituire l' **\_ oggetto VDS \_ E \_ eliminato**.</span><span class="sxs-lookup"><span data-stu-id="976cf-129">The provider must be robust enough to deal with errant callers; if a caller invokes a method on a deleted object, the provider should return **VDS\_E\_OBJECT\_DELETED**.</span></span>

### <a name="service-initialization"></a><span data-ttu-id="976cf-130">Inizializzazione del servizio</span><span class="sxs-lookup"><span data-stu-id="976cf-130">Service Initialization</span></span>

<span data-ttu-id="976cf-131">VDS fornisce un identificatore di classe (CLSID) per il caricatore del servizio e gli oggetti servizio, ma solo il CLSID del caricatore di servizi è pubblico.</span><span class="sxs-lookup"><span data-stu-id="976cf-131">VDS supplies a class identifier (Clsid) for the service loader and the service objects, but only the service loader Clsid is public.</span></span> <span data-ttu-id="976cf-132">L'inizializzazione del servizio si verifica quando i provider, un'applicazione chiamante e il servizio eseguono le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="976cf-132">Service initialization occurs when the providers, a calling application, and the service perform the following tasks:</span></span>

-   <span data-ttu-id="976cf-133">Ogni nuovo provider richiama il metodo [**IVdsAdmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) durante l'installazione per la registrazione con VDS.</span><span class="sxs-lookup"><span data-stu-id="976cf-133">Each new provider invokes the [**IVdsAdmin::RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) method during installation to register with VDS.</span></span> <span data-ttu-id="976cf-134">La chiamata crea una chiave del registro di sistema nell'hive di sistema, identificata dal GUID oggetto del provider.</span><span class="sxs-lookup"><span data-stu-id="976cf-134">The call creates a registry key under the SYSTEM hive, identified by the object GUID of the provider.</span></span> <span data-ttu-id="976cf-135">Contenuto in questa chiave è il CLSID dell'oggetto provider, il nome, la versione e il GUID della versione del provider.</span><span class="sxs-lookup"><span data-stu-id="976cf-135">Contained under this key is the Clsid of the provider object, the name, version, and the version GUID of the provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="976cf-136">I GUID oggetto provider sono permanenti; i GUID degli oggetti software e hardware non lo sono.</span><span class="sxs-lookup"><span data-stu-id="976cf-136">Provider object GUIDs are persistent; software and hardware object GUIDs are not.</span></span>

     

-   <span data-ttu-id="976cf-137">Un'applicazione chiama la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , passando il CLSID del caricatore del servizio come argomento.</span><span class="sxs-lookup"><span data-stu-id="976cf-137">An application calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, passing the service loader Clsid as an argument.</span></span> <span data-ttu-id="976cf-138">Con un puntatore all'oggetto del caricatore del servizio, l'applicazione può avviare VDS localmente o in remoto passando il nome del computer desiderato come parametro al metodo [**IVdsServiceLoader:: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) .</span><span class="sxs-lookup"><span data-stu-id="976cf-138">With a pointer to the service loader object, the application can start VDS either locally or remotely by passing the desired computer name as a parameter to the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method.</span></span>
-   <span data-ttu-id="976cf-139">Quando l'applicazione iniziale si connette al servizio, VDS chiama prima [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) su ogni CLSID trovato sotto la chiave del registro di sistema e quindi chiama il metodo [**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) su ogni provider per inizializzare i programmi.</span><span class="sxs-lookup"><span data-stu-id="976cf-139">When the initial application attaches to the service, VDS first calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on each Clsid found under the registry key, and then calls the [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) method on each provider to initialize the programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="976cf-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="976cf-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="976cf-141">Informazioni su VDS</span><span class="sxs-lookup"><span data-stu-id="976cf-141">About VDS</span></span>](about-vds.md)
</dt> <dt>

[<span data-ttu-id="976cf-142">**IVdsAdmin:: RegisterProvider**</span><span class="sxs-lookup"><span data-stu-id="976cf-142">**IVdsAdmin::RegisterProvider**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[<span data-ttu-id="976cf-143">**IVdsServiceLoader::LoadService**</span><span class="sxs-lookup"><span data-stu-id="976cf-143">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="976cf-144">**IVdsProviderPrivate:: OnLoad**</span><span class="sxs-lookup"><span data-stu-id="976cf-144">**IVdsProviderPrivate::OnLoad**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
