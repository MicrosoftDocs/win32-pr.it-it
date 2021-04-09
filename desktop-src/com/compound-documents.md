---
title: Documenti composti
description: I documenti composti OLE consentono agli utenti di lavorare all'interno di una singola applicazione di modificare i dati scritti in vari formati e derivati da più origini.
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118558"
---
# <a name="compound-documents"></a><span data-ttu-id="3be6d-103">Documenti composti</span><span class="sxs-lookup"><span data-stu-id="3be6d-103">Compound Documents</span></span>

<span data-ttu-id="3be6d-104">I documenti composti OLE consentono agli utenti di lavorare all'interno di una singola applicazione di modificare i dati scritti in vari formati e derivati da più origini.</span><span class="sxs-lookup"><span data-stu-id="3be6d-104">OLE compound documents enable users working within a single application to manipulate data written in various formats and derived from multiple sources.</span></span> <span data-ttu-id="3be6d-105">Ad esempio, un utente può inserire in un documento di elaborazione di Word un grafo creato in una seconda applicazione e un oggetto audio creato in una terza applicazione.</span><span class="sxs-lookup"><span data-stu-id="3be6d-105">For example, a user might insert into a word processing document a graph created in a second application and a sound object created in a third application.</span></span> <span data-ttu-id="3be6d-106">Se si attiva il grafo, la seconda applicazione caricherà la propria interfaccia utente o almeno quella parte contenente gli strumenti necessari per modificare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3be6d-106">Activating the graph causes the second application to load its user interface, or at least that part containing tools necessary to edit the object.</span></span> <span data-ttu-id="3be6d-107">L'attivazione dell'oggetto audio comporta la riproduzione della terza applicazione.</span><span class="sxs-lookup"><span data-stu-id="3be6d-107">Activating the sound object causes the third application to play it.</span></span> <span data-ttu-id="3be6d-108">In entrambi i casi, un utente è in grado di modificare i dati da origini esterne dall'interno del contesto di un singolo documento.</span><span class="sxs-lookup"><span data-stu-id="3be6d-108">In both cases, a user is able to manipulate data from external sources from within the context of a single document.</span></span>

<span data-ttu-id="3be6d-109">La tecnologia per documenti compositi OLE si basa su una base composta da COM, archiviazione strutturata e trasferimento dati uniforme.</span><span class="sxs-lookup"><span data-stu-id="3be6d-109">OLE compound document technology rests on a foundation consisting of COM, structured storage, and uniform data transfer.</span></span> <span data-ttu-id="3be6d-110">Come riepilogato di seguito, ognuna di queste tecnologie di base svolge un ruolo fondamentale nei documenti compositi OLE:</span><span class="sxs-lookup"><span data-stu-id="3be6d-110">As summarized below, each of these core technologies plays a critical role in OLE compound documents:</span></span>

<dl> <dt>

<span data-ttu-id="3be6d-111"><span id="COM"></span><span id="com"></span>COM</span><span class="sxs-lookup"><span data-stu-id="3be6d-111"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="3be6d-112">Un oggetto documento composto è essenzialmente un oggetto COM che può essere incorporato o collegato a un documento esistente.</span><span class="sxs-lookup"><span data-stu-id="3be6d-112">A compound document object is essentially a COM object that can be embedded in, or linked to, an existing document.</span></span> <span data-ttu-id="3be6d-113">Come oggetto COM, un oggetto documento composto espone l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , tramite la quale i client possono ottenere i puntatori alle altre interfacce, inclusi diversi, ad esempio [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)e [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), che forniscono funzionalità speciali univoche per gli oggetti documento composti.</span><span class="sxs-lookup"><span data-stu-id="3be6d-113">As a COM object, a compound document object exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces, including several, such as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink), and [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), that provide special features unique to compound document objects.</span></span>

</dd> <dt>

<span data-ttu-id="3be6d-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Archiviazione strutturata</span><span class="sxs-lookup"><span data-stu-id="3be6d-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Structured Storage</span></span>
</dt> <dd>

<span data-ttu-id="3be6d-115">Un oggetto documento composto deve implementare [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) o, facoltativamente, le interfacce [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) per gestire la propria archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3be6d-115">A compound document object must implement the [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) or, optionally, [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) interfaces to manage its own storage.</span></span> <span data-ttu-id="3be6d-116">Un contenitore utilizzato per creare documenti composti deve fornire l'interfaccia [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , tramite la quale gli oggetti archiviano e recuperano i dati.</span><span class="sxs-lookup"><span data-stu-id="3be6d-116">A container used to create compound documents must supply the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface, through which objects store and retrieve data.</span></span> <span data-ttu-id="3be6d-117">I contenitori forniscono quasi sempre istanze di **IStorage** ottenute dall'implementazione dei file composti di OLE.</span><span class="sxs-lookup"><span data-stu-id="3be6d-117">Containers almost always provide instances of **IStorage** obtained from OLE's Compound Files implementation.</span></span> <span data-ttu-id="3be6d-118">I contenitori devono usare anche le interfacce **IPersistStorage** e/o **IPersistStream** di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="3be6d-118">Containers must also use an object's **IPersistStorage** and/or **IPersistStream** interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="3be6d-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer</span><span class="sxs-lookup"><span data-stu-id="3be6d-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer</span></span>
</dt> <dd>

<span data-ttu-id="3be6d-120">Le applicazioni che supportano i documenti composti devono implementare [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) perché gli oggetti incorporati e gli oggetti collegati iniziano come dati trasferiti con formati degli Appunti OLE speciali, anziché con formati degli Appunti standard di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3be6d-120">Applications that support compound documents must implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) because embedded objects and linked objects begin as data that has been transferred using special OLE clipboard formats, rather than standard Microsoft Windows clipboard formats.</span></span> <span data-ttu-id="3be6d-121">In altre parole, la formattazione dei dati come oggetto incorporato o collegato è semplicemente un'altra opzione fornita dal modello di trasferimento dei dati uniforme di OLE.</span><span class="sxs-lookup"><span data-stu-id="3be6d-121">In other words, formatting data as an embedded or linked object is simply one more option provided by OLE's uniform data transfer model.</span></span>

</dd> </dl>

<span data-ttu-id="3be6d-122">La tecnologia dei documenti compositi di OLE offre agli sviluppatori e agli utenti del software lo stesso vantaggio.</span><span class="sxs-lookup"><span data-stu-id="3be6d-122">OLE's compound document technology benefits both software developers and users alike.</span></span> <span data-ttu-id="3be6d-123">Anziché essere obbligati a stipare ogni funzionalità concepibile in un'unica applicazione, gli sviluppatori di software sono ora gratuiti, se desiderano, per sviluppare applicazioni più piccole e più mirate che si basano su altre applicazioni per fornire funzionalità aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="3be6d-123">Instead of feeling obligated to cram every conceivable feature into a single application, software developers are now free, if they like, to develop smaller, more focused applications that rely on other applications to supply additional features.</span></span> <span data-ttu-id="3be6d-124">Nei casi in cui uno sviluppatore di software decide di fornire un'applicazione con funzionalità oltre alle funzionalità di base, lo sviluppatore può implementare questi servizi aggiuntivi come DLL separate, che vengono caricati in memoria solo quando sono necessari i relativi servizi.</span><span class="sxs-lookup"><span data-stu-id="3be6d-124">In cases where a software developer decides to provide an application with capabilities beyond its core features, the developer can implement these additional services as separate DLLs, which are loaded into memory only when their services are required.</span></span> <span data-ttu-id="3be6d-125">Gli utenti traggono vantaggio da software più piccolo, più veloce e più idoneo che possono combinare in base alle esigenze, manipolando tutti i componenti necessari da un singolo documento master.</span><span class="sxs-lookup"><span data-stu-id="3be6d-125">Users benefit from smaller, faster, more capable software that they can mix and match as needed, manipulating all required components from within a single master document.</span></span>

<span data-ttu-id="3be6d-126">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="3be6d-126">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3be6d-127">Contenitori e server</span><span class="sxs-lookup"><span data-stu-id="3be6d-127">Containers and Servers</span></span>](containers-and-servers.md)
-   [<span data-ttu-id="3be6d-128">Collegamento e incorporamento</span><span class="sxs-lookup"><span data-stu-id="3be6d-128">Linking and Embedding</span></span>](linking-and-embedding.md)
-   [<span data-ttu-id="3be6d-129">Gestori di oggetti</span><span class="sxs-lookup"><span data-stu-id="3be6d-129">Object Handlers</span></span>](object-handlers.md)
-   [<span data-ttu-id="3be6d-130">Server in-process</span><span class="sxs-lookup"><span data-stu-id="3be6d-130">In-Process Servers</span></span>](in-process-servers.md)
-   [<span data-ttu-id="3be6d-131">Oggetti collegati e moniker</span><span class="sxs-lookup"><span data-stu-id="3be6d-131">Linked Objects and Monikers</span></span>](linked-objects-and-monikers.md)
-   [<span data-ttu-id="3be6d-132">Notifications</span><span class="sxs-lookup"><span data-stu-id="3be6d-132">Notifications</span></span>](notifications.md)
-   [<span data-ttu-id="3be6d-133">Interfacce di documenti composti</span><span class="sxs-lookup"><span data-stu-id="3be6d-133">Compound Document Interfaces</span></span>](compound-document-interfaces.md)
-   [<span data-ttu-id="3be6d-134">Stati degli oggetti</span><span class="sxs-lookup"><span data-stu-id="3be6d-134">Object States</span></span>](object-states.md)
-   [<span data-ttu-id="3be6d-135">Implementazione di In-Place attivazione</span><span class="sxs-lookup"><span data-stu-id="3be6d-135">Implementing In-Place Activation</span></span>](implementing-in-place-activation.md)
-   [<span data-ttu-id="3be6d-136">Creazione di oggetti collegati e incorporati da dati esistenti</span><span class="sxs-lookup"><span data-stu-id="3be6d-136">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
-   [<span data-ttu-id="3be6d-137">Visualizza Caching</span><span class="sxs-lookup"><span data-stu-id="3be6d-137">View Caching</span></span>](view-caching.md)

## <a name="related-topics"></a><span data-ttu-id="3be6d-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3be6d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3be6d-139">Trasferimento dati</span><span class="sxs-lookup"><span data-stu-id="3be6d-139">Data Transfer</span></span>](data-transfer.md)
</dt> <dt>

[<span data-ttu-id="3be6d-140">Archiviazione strutturata</span><span class="sxs-lookup"><span data-stu-id="3be6d-140">Structured Storage</span></span>](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 