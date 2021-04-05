---
title: Gestori di oggetti
description: Gestori di oggetti
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7294ddd48d2acaa010ad15c0e2497fd33c7f071
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855645"
---
# <a name="object-handlers"></a><span data-ttu-id="b2e50-103">Gestori di oggetti</span><span class="sxs-lookup"><span data-stu-id="b2e50-103">Object Handlers</span></span>

<span data-ttu-id="b2e50-104">Se un'applicazione server OLE è un server locale, vale a dire che viene eseguita nel proprio spazio di elaborazione, la comunicazione tra il contenitore e il server deve essere eseguita tra i limiti del processo.</span><span class="sxs-lookup"><span data-stu-id="b2e50-104">If an OLE server application is a local server, meaning that it runs in its own process space, communication between container and server must occur across process boundaries.</span></span> <span data-ttu-id="b2e50-105">Poiché questo processo è dispendioso, OLE si basa su un oggetto surrogato caricato nello spazio di processo del contenitore per agire per conto di un'applicazione server locale.</span><span class="sxs-lookup"><span data-stu-id="b2e50-105">Because this process is expensive, OLE relies on a surrogate object loaded into the container's process space to act on behalf of a local server application.</span></span> <span data-ttu-id="b2e50-106">Questo oggetto surrogato, noto come *gestore di oggetti*, richiede il contenitore dei servizi che non richiedono l'attenzione dell'applicazione server, ad esempio le richieste di disegno.</span><span class="sxs-lookup"><span data-stu-id="b2e50-106">This surrogate object, known as an *object handler*, services container requests that do not require the attention of the server application, such as requests for drawing.</span></span> <span data-ttu-id="b2e50-107">Quando un contenitore richiede un elemento che non può essere fornito dal gestore di oggetti, il gestore comunica con l'applicazione server utilizzando il meccanismo di comunicazione out-of-process di COM.</span><span class="sxs-lookup"><span data-stu-id="b2e50-107">When a container requests something that the object handler cannot provide, the handler communicates with the server application using COM's out-of-process communication mechanism.</span></span>

<span data-ttu-id="b2e50-108">Un gestore di oggetti è univoco per una classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="b2e50-108">An object handler is unique to an object class.</span></span> <span data-ttu-id="b2e50-109">Quando si crea un'istanza di un gestore per una classe, non è possibile utilizzarla per un'altra classe.</span><span class="sxs-lookup"><span data-stu-id="b2e50-109">When you create an instance of a handler for one class, you cannot use it for another.</span></span> <span data-ttu-id="b2e50-110">Quando viene usato per un documento composto, il gestore dell'oggetto implementa le strutture dei dati sul lato contenitore quando si accede in remoto agli oggetti di una determinata classe.</span><span class="sxs-lookup"><span data-stu-id="b2e50-110">When used for a compound document, the object handler implements the container-side data structures when objects of a particular class are accessed remotely.</span></span>

<span data-ttu-id="b2e50-111">OLE fornisce un gestore di oggetti predefinito che può essere utilizzato dalle applicazioni server locali.</span><span class="sxs-lookup"><span data-stu-id="b2e50-111">OLE provides a default object handler that local server applications can use.</span></span> <span data-ttu-id="b2e50-112">Per le applicazioni che richiedono comportamenti speciali, gli sviluppatori possono implementare un gestore personalizzato che sostituisce il gestore predefinito o lo usa per fornire determinati comportamenti predefiniti.</span><span class="sxs-lookup"><span data-stu-id="b2e50-112">For applications that require special behaviors, developers can implement a custom handler that either replaces the default handler or uses it to provide certain default behaviors.</span></span>

<span data-ttu-id="b2e50-113">Un gestore di oggetti è una DLL che contiene diversi componenti di interazione.</span><span class="sxs-lookup"><span data-stu-id="b2e50-113">An object handler is a DLL containing several interacting components.</span></span> <span data-ttu-id="b2e50-114">Questi componenti includono parti remote per gestire la comunicazione tra il gestore e la relativa applicazione server, una cache per archiviare i dati di un oggetto, oltre a informazioni sulla modalità di formattazione e visualizzazione dei dati e un oggetto di controllo che coordina le attività degli altri componenti della DLL.</span><span class="sxs-lookup"><span data-stu-id="b2e50-114">These components include remoting pieces to manage communication between the handler and its server application, a cache for storing an object's data, along with information on how that data should be formatted and displayed, and a controlling object that coordinates the activities of the DLL's other components.</span></span> <span data-ttu-id="b2e50-115">Inoltre, se un oggetto è un collegamento, la DLL include anche un componente di collegamento, o un *oggetto collegato*, che tiene traccia del nome e della posizione dell'origine del collegamento.</span><span class="sxs-lookup"><span data-stu-id="b2e50-115">In addition, if an object is a link, the DLL also includes a linking component, or *linked object*, which keeps track of the name and location of the link source.</span></span>

<span data-ttu-id="b2e50-116">La *cache* contiene dati e informazioni di presentazione sufficienti affinché il gestore visualizzi un oggetto caricato, ma non in esecuzione, nel relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="b2e50-116">The *cache* contains data and presentation information sufficient for the handler to display a loaded, but not running, object in its container.</span></span> <span data-ttu-id="b2e50-117">OLE fornisce un'implementazione della cache utilizzata dal gestore dell'oggetto predefinito OLE e dall'oggetto collegamento.</span><span class="sxs-lookup"><span data-stu-id="b2e50-117">OLE provides an implementation of the cache used by OLE's default object handler and the link object.</span></span> <span data-ttu-id="b2e50-118">La cache archivia i dati in formati necessari al gestore dell'oggetto per soddisfare le richieste di estrazione del contenitore.</span><span class="sxs-lookup"><span data-stu-id="b2e50-118">The cache stores data in formats needed by the object handler to satisfy container draw requests.</span></span> <span data-ttu-id="b2e50-119">Quando si modificano i dati di un oggetto, l'oggetto invia una notifica alla cache in modo da consentire l'esecuzione di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b2e50-119">When an object's data changes, the object sends a notification to the cache so that an update can occur.</span></span> <span data-ttu-id="b2e50-120">Per ulteriori informazioni sulla cache, vedere [View Caching](view-caching.md).</span><span class="sxs-lookup"><span data-stu-id="b2e50-120">For more information on the cache, see [View Caching](view-caching.md).</span></span>

<span data-ttu-id="b2e50-121">Per altre informazioni, vedere l'argomento seguente:</span><span class="sxs-lookup"><span data-stu-id="b2e50-121">For more information, see the following topic:</span></span>

-   [<span data-ttu-id="b2e50-122">Gestore predefinito e gestori personalizzati</span><span class="sxs-lookup"><span data-stu-id="b2e50-122">The Default Handler and Custom Handlers</span></span>](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="b2e50-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b2e50-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e50-124">Documenti composti</span><span class="sxs-lookup"><span data-stu-id="b2e50-124">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




