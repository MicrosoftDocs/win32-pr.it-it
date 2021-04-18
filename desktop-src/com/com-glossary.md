---
title: Glossario COM
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c12f3c021988f0349d9eaf6a2bdbd9505ca8a6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300517"
---
# <a name="com-glossary"></a><span data-ttu-id="55fdf-103">Glossario COM</span><span class="sxs-lookup"><span data-stu-id="55fdf-103">COM Glossary</span></span>

<dl> <dt>

<span data-ttu-id="55fdf-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**attivazione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-105">Processo di caricamento di un oggetto in memoria, che lo inserisce nello stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-105">The process of loading an object in memory, which puts it into the running state.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**stato attivo**</span><span class="sxs-lookup"><span data-stu-id="55fdf-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**active state**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-107">Oggetto COM che si trova nello stato in esecuzione e ha un'interfaccia utente visibile.</span><span class="sxs-lookup"><span data-stu-id="55fdf-107">A COM object that is in the running state and has a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**moniker assoluto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**absolute moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-109">Moniker che specifica la posizione assoluta di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-109">A moniker that specifies the absolute location of an object.</span></span> <span data-ttu-id="55fdf-110">Un moniker assoluto è analogo a un percorso completo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-110">An absolute moniker is analogous to a full path.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**titolare consultivo**</span><span class="sxs-lookup"><span data-stu-id="55fdf-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**advisory holder**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-112">Oggetto COM che memorizza nella cache, gestisce e invia notifiche delle modifiche ai sink consultivi delle applicazioni contenitore.</span><span class="sxs-lookup"><span data-stu-id="55fdf-112">A COM object that caches, manages, and sends notifications of changes to container applications' advisory sinks.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**sink consultivo**</span><span class="sxs-lookup"><span data-stu-id="55fdf-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**advisory sink**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-114">Oggetto COM che può ricevere notifiche delle modifiche in un oggetto incorporato o in un oggetto collegato perché implementa l'interfaccia [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) o [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-114">A COM object that can receive notifications of changes in an embedded object or linked object because it implements the [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) or [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) interface.</span></span> <span data-ttu-id="55fdf-115">I contenitori che devono ricevere notifiche delle modifiche negli oggetti implementano un sink consultivo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-115">Containers that need to be notified of changes in objects implement an advisory sink.</span></span> <span data-ttu-id="55fdf-116">Le notifiche provengono dal server, che usa un oggetto titolare consultivo per memorizzare nella cache e gestire le notifiche ai contenitori.</span><span class="sxs-lookup"><span data-stu-id="55fdf-116">Notifications originate in the server, which uses an advisory holder object to cache and manage notifications to containers.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**oggetto aggregate**</span><span class="sxs-lookup"><span data-stu-id="55fdf-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**aggregate object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-118">Oggetto COM costituito da uno o più oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="55fdf-118">A COM object that is made up of one or more other COM objects.</span></span> <span data-ttu-id="55fdf-119">Un oggetto nell'aggregato viene designato come oggetto di controllo, che controlla quali interfacce dell'aggregazione sono esposte e quali sono private.</span><span class="sxs-lookup"><span data-stu-id="55fdf-119">One object in the aggregate is designated the controlling object, which controls which interfaces in the aggregate are exposed and which are private.</span></span> <span data-ttu-id="55fdf-120">Questo oggetto di controllo ha un'implementazione speciale di [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) denominata **IUnknown** di controllo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-120">This controlling object has a special implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) called the controlling **IUnknown**.</span></span> <span data-ttu-id="55fdf-121">Tutti gli oggetti nell'aggregato devono passare le chiamate ai metodi **IUnknown** tramite il controllo **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="55fdf-121">All objects in the aggregate must pass calls to **IUnknown** methods through the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**aggregazione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-123">Tecnica di composizione per l'implementazione di oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="55fdf-123">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="55fdf-124">Consente di compilare un nuovo oggetto riutilizzando una o più implementazioni dell'interfaccia di oggetti esistenti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-124">It allows you to build a new object by reusing one or more existing objects' interface implementations.</span></span> <span data-ttu-id="55fdf-125">L'oggetto aggregato sceglie le interfacce da esporre ai client e le interfacce vengono esposte come se fossero implementate dall'oggetto aggregato.</span><span class="sxs-lookup"><span data-stu-id="55fdf-125">The aggregate object chooses which interfaces to expose to clients, and the interfaces are exposed as if they were implemented by the aggregate object.</span></span> <span data-ttu-id="55fdf-126">I client dell'oggetto aggregato comunicano solo con l'oggetto aggregato.</span><span class="sxs-lookup"><span data-stu-id="55fdf-126">Clients of the aggregate object communicate only with the aggregate object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**Proprietà di ambiente**</span><span class="sxs-lookup"><span data-stu-id="55fdf-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**ambient property**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-128">Proprietà della fase di esecuzione gestita ed esposta dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="55fdf-128">A run-time property that is managed and exposed by the container.</span></span> <span data-ttu-id="55fdf-129">In genere, una proprietà di ambiente rappresenta una caratteristica di un form, ad esempio il colore di sfondo, che deve essere comunicata a un controllo in modo che il controllo possa assumere l'aspetto dell'ambiente circostante.</span><span class="sxs-lookup"><span data-stu-id="55fdf-129">Typically, an ambient property represents a characteristic of a form, such as background color, that needs to be communicated to a control so that the control can assume the look and feel of its surrounding environment.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**</span><span class="sxs-lookup"><span data-stu-id="55fdf-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-131">Inverso del moniker di un file, di un elemento o di un puntatore.</span><span class="sxs-lookup"><span data-stu-id="55fdf-131">The inverse of a file, item, or pointer moniker.</span></span> <span data-ttu-id="55fdf-132">Un anti-moniker viene aggiunto alla fine di un file, di un elemento o di un moniker del puntatore per annullare l'errore.</span><span class="sxs-lookup"><span data-stu-id="55fdf-132">An anti-moniker is added to the end of a file, item, or pointer moniker to nullify it.</span></span> <span data-ttu-id="55fdf-133">Gli anti-moniker vengono usati nella costruzione di moniker relativi.</span><span class="sxs-lookup"><span data-stu-id="55fdf-133">Anti-monikers are used in the construction of relative monikers.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**conteggio dei riferimenti artificiali**</span><span class="sxs-lookup"><span data-stu-id="55fdf-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**artificial reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-135">Tecnica utilizzata per proteggere un oggetto prima di chiamare una funzione o un metodo che potrebbe eliminarlo in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-135">A technique used to help protect an object before calling a function or method that could prematurely destroy it.</span></span> <span data-ttu-id="55fdf-136">Un programma chiama **IUnknown:: AddRef** per incrementare il conteggio dei riferimenti dell'oggetto prima di effettuare la chiamata che può liberare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-136">A program calls **IUnknown::AddRef** to increment the object's reference count before making the call that could free the object.</span></span> <span data-ttu-id="55fdf-137">Dopo la restituzione della funzione, il programma chiama **IUnknown:: Release** per decrementare il numero.</span><span class="sxs-lookup"><span data-stu-id="55fdf-137">After the function returns, the program calls **IUnknown::Release** to decrement the count.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**Binding asincrono**</span><span class="sxs-lookup"><span data-stu-id="55fdf-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**asynchronous binding**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-139">Tipo di associazione in cui è necessario che il processo venga eseguito in modo asincrono per evitare un calo delle prestazioni per l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="55fdf-139">A type of binding in which it is necessary for the process to occur asynchronously to avoid performance degradation for the end user.</span></span> <span data-ttu-id="55fdf-140">In genere, l'associazione asincrona viene utilizzata negli ambienti distribuiti, ad esempio il World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="55fdf-140">Typically, asynchronous binding is used in distributed environments such as the World Wide Web.</span></span> <span data-ttu-id="55fdf-141">OLE supporta classi moniker asincrone e meccanismi di callback che consentono di eseguire il processo di individuazione e inizializzazione di un oggetto in un ambiente distribuito mentre vengono eseguite altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="55fdf-141">OLE supports asynchronous moniker classes and callback mechanisms that allow the process of locating and initializing an object in a distributed environment to occur while other operations are being carried out.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**chiamata asincrona**</span><span class="sxs-lookup"><span data-stu-id="55fdf-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**asynchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-143">Una chiamata a una funzione che viene eseguita separatamente, in modo che il chiamante possa continuare l'elaborazione delle istruzioni senza attendere la restituzione della funzione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-143">A call to a function that is executed separately so that the caller can continue processing instructions without waiting for the function to return.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**moniker asincrono**</span><span class="sxs-lookup"><span data-stu-id="55fdf-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**asynchronous moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-145">Moniker che supporta l'associazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="55fdf-145">A moniker that supports asynchronous binding.</span></span> <span data-ttu-id="55fdf-146">Ad esempio, le istanze della classe moniker dell'URL fornita dal sistema sono moniker asincroni.</span><span class="sxs-lookup"><span data-stu-id="55fdf-146">For example, instances of the system-supplied URL moniker class are asynchronous monikers.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**automazione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**automation**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-148">Un modo per modificare gli oggetti di un'applicazione dall'esterno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-148">A way to manipulate an application's objects from outside the application.</span></span> <span data-ttu-id="55fdf-149">L'automazione viene in genere usata per creare applicazioni che espongono oggetti a strumenti di programmazione e linguaggi macro, per creare e modificare oggetti di un'applicazione da un'altra applicazione o per creare strumenti per l'accesso e la modifica di oggetti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-149">Automation is typically used to create applications that expose objects to programming tools and macro languages, create and manipulate one application's objects from another applications, or to create tools for accessing and manipulating objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**contesto di associazione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**bind context**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-151">Oggetto COM che implementa l'interfaccia [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-151">A COM object that implements the [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="55fdf-152">I contesti di binding vengono utilizzati nelle operazioni del moniker per mantenere i riferimenti agli oggetti attivati quando viene associato un moniker.</span><span class="sxs-lookup"><span data-stu-id="55fdf-152">Bind contexts are used in moniker operations to hold references to the objects activated when a moniker is bound.</span></span> <span data-ttu-id="55fdf-153">Il contesto di associazione contiene i parametri che si applicano a tutte le operazioni durante l'associazione di un moniker composito generico e fornisce all'implementazione del moniker l'accesso alle informazioni relative all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-153">The bind context contains parameters that apply to all operations during the binding of a generic composite moniker and provides the moniker implementation with access to information about its environment.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**associazione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-155">Associazione di un nome al relativo referente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-155">Associating a name with its referent.</span></span> <span data-ttu-id="55fdf-156">In particolare, individuando l'oggetto denominato da un moniker, inserendolo nello stato di esecuzione, se non è già e restituendo un puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="55fdf-156">Specifically, locating the object named by a moniker, putting it into its running state if it isn't already, and returning an interface pointer to it.</span></span> <span data-ttu-id="55fdf-157">Gli oggetti possono essere associati in fase di esecuzione (chiamato anche associazione tardiva o associazione dinamica) o in fase di compilazione (detto anche binding statico).</span><span class="sxs-lookup"><span data-stu-id="55fdf-157">Objects can be bound at run time (also called late binding or dynamic binding) or at compile time (also called static binding).</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**cache**</span><span class="sxs-lookup"><span data-stu-id="55fdf-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**cache**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-159">Archivio locale di informazioni (in genere temporaneo).</span><span class="sxs-lookup"><span data-stu-id="55fdf-159">A (usually temporary) local store of information.</span></span> <span data-ttu-id="55fdf-160">In OLE, una cache contiene informazioni che definiscono la presentazione di un oggetto collegato o incorporato quando il contenitore viene aperto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-160">In OLE, a cache contains information that defines the presentation of a linked or embedded object when the container is opened.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**inizializzazione della cache**</span><span class="sxs-lookup"><span data-stu-id="55fdf-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**cache initialization**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-162">Riempimento della cache di un oggetto collegato o incorporato con i dati di presentazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-162">Filling a linked or embedded object's cache with presentation data.</span></span> <span data-ttu-id="55fdf-163">L'interfaccia [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) fornisce metodi che possono essere chiamati da un contenitore per controllare i dati che vengono memorizzati nella cache per gli oggetti collegati o incorporati.</span><span class="sxs-lookup"><span data-stu-id="55fdf-163">The [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) interface provides methods that a container can call to control the data that gets cached for linked or embedded objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**classe**</span><span class="sxs-lookup"><span data-stu-id="55fdf-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**class**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-165">Definizione di un oggetto nel codice.</span><span class="sxs-lookup"><span data-stu-id="55fdf-165">The definition of an object in code.</span></span> <span data-ttu-id="55fdf-166">In C++, la classe di un oggetto è definita come tipo di dati, ma ciò non accade in altri linguaggi.</span><span class="sxs-lookup"><span data-stu-id="55fdf-166">In C++, the class of an object is defined as a data type, but this is not the case in other languages.</span></span> <span data-ttu-id="55fdf-167">Poiché OLE può essere codificato in qualsiasi linguaggio, la classe viene utilizzata per fare riferimento alla definizione dell'oggetto generale.</span><span class="sxs-lookup"><span data-stu-id="55fdf-167">Because OLE can be coded in any language, class is used to refer to the general object definition.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**</span><span class="sxs-lookup"><span data-stu-id="55fdf-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-169">Oggetto COM che implementa l'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e che consente di creare una o più istanze di un oggetto identificato da un identificatore di classe specificato (CLSID).</span><span class="sxs-lookup"><span data-stu-id="55fdf-169">A COM object that implements the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface and that creates one or more instances of an object identified by a given class identifier(CLSID).</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**identificatore di classe (CLSID)**</span><span class="sxs-lookup"><span data-stu-id="55fdf-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**class identifier (CLSID)**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-171">Identificatore univoco globale (GUID) associato a un oggetto della classe OLE.</span><span class="sxs-lookup"><span data-stu-id="55fdf-171">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="55fdf-172">Se un oggetto classe verrà utilizzato per creare più di un'istanza di un oggetto, l'applicazione server associata deve registrare il proprio CLSID nel registro di sistema in modo che i client possano individuare e caricare il codice eseguibile associato agli oggetti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-172">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="55fdf-173">Ogni server o contenitore OLE che consente il collegamento ai relativi oggetti incorporati deve registrare un CLSID per ogni definizione di oggetto supportata.</span><span class="sxs-lookup"><span data-stu-id="55fdf-173">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**Classe (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="55fdf-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**class object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-175">Nella programmazione orientata a oggetti, un oggetto il cui stato è condiviso da tutti gli oggetti in una classe e il cui comportamento agisce sui dati dello stato classwide.</span><span class="sxs-lookup"><span data-stu-id="55fdf-175">In object-oriented programming, an object whose state is shared by all the objects in a class and whose behavior acts on that classwide state data.</span></span> <span data-ttu-id="55fdf-176">In COM, gli oggetti classe sono denominati class factory e in genere non hanno alcun comportamento ad eccezione della creazione di nuove istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="55fdf-176">In COM, class objects are called class factories, and typically have no behavior except to create new instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**client**</span><span class="sxs-lookup"><span data-stu-id="55fdf-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-178">Oggetto COM che richiede servizi da un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-178">A COM object that requests services from another object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**sito client**</span><span class="sxs-lookup"><span data-stu-id="55fdf-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**client site**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-180">Il sito di visualizzazione per un oggetto incorporato o collegato in un documento composto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-180">The display site for an embedded or linked object within a compound document.</span></span> <span data-ttu-id="55fdf-181">Il sito client è il mezzo principale mediante il quale un oggetto richiede servizi dal relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="55fdf-181">The client site is the principal means by which an object requests services from its container.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**</span><span class="sxs-lookup"><span data-stu-id="55fdf-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-183">Identificatore univoco globale (GUID) associato a un oggetto della classe OLE.</span><span class="sxs-lookup"><span data-stu-id="55fdf-183">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="55fdf-184">Se un oggetto classe verrà utilizzato per creare più di un'istanza di un oggetto, l'applicazione server associata deve registrare il proprio CLSID nel registro di sistema in modo che i client possano individuare e caricare il codice eseguibile associato agli oggetti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-184">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="55fdf-185">Ogni server o contenitore OLE che consente il collegamento ai relativi oggetti incorporati deve registrare un CLSID per ogni definizione di oggetto supportata.</span><span class="sxs-lookup"><span data-stu-id="55fdf-185">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**commit**</span><span class="sxs-lookup"><span data-stu-id="55fdf-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-187">Per salvare in modo permanente le modifiche apportate a un oggetto di archiviazione o flusso dopo l'apertura o l'ultimo salvataggio delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="55fdf-187">To persistently save any changes made to a storage or stream object since it was opened or changes were last saved.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**componente**</span><span class="sxs-lookup"><span data-stu-id="55fdf-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-189">Oggetto che incapsula sia i dati che il codice e fornisce un set ben definito di servizi disponibili pubblicamente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-189">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**</span><span class="sxs-lookup"><span data-stu-id="55fdf-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-191">Modello di programmazione orientato a oggetti OLE che definisce la modalità di interazione degli oggetti all'interno di un singolo processo o tra processi.</span><span class="sxs-lookup"><span data-stu-id="55fdf-191">The OLE object-oriented programming model that defines how objects interact within a single process or between processes.</span></span> <span data-ttu-id="55fdf-192">In COM, i client possono accedere a un oggetto tramite le interfacce implementate sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-192">In COM, clients have access to an object through interfaces implemented on the object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**barra dei menu composita**</span><span class="sxs-lookup"><span data-stu-id="55fdf-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**composite menu bar**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-194">Una barra dei menu condivisa composta da gruppi di menu sia da un'applicazione contenitore sia da un'applicazione server attivata sul posto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-194">A shared menu bar composed of menu groups from both a container application and an in-place-activated server application.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**moniker composito**</span><span class="sxs-lookup"><span data-stu-id="55fdf-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-196">Moniker costituito da due o più moniker considerati come un'unità.</span><span class="sxs-lookup"><span data-stu-id="55fdf-196">A moniker that consists of two or more monikers that are treated as a unit.</span></span> <span data-ttu-id="55fdf-197">Un moniker composito può essere non generico, vale a dire che i relativi moniker di componente hanno una conoscenza speciale, o generica, che i moniker dei componenti non conoscono l'uno dall'altro tranne che sono moniker</span><span class="sxs-lookup"><span data-stu-id="55fdf-197">A composite moniker can be non-generic, meaning that its component monikers have special knowledge of each other, or generic, meaning that its component monikers know nothing about each other except that they are monikers</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**documento composto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**compound document**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-199">Documento che include oggetti collegati o incorporati, nonché i propri dati nativi.</span><span class="sxs-lookup"><span data-stu-id="55fdf-199">A document that includes linked or embedded objects, as well as its own native data.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**file composto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**compound file**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-201">Implementazione di archiviazione strutturata fornita da OLE.</span><span class="sxs-lookup"><span data-stu-id="55fdf-201">An OLE-provided Structured Storage implementation.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**Oggetto COM**</span><span class="sxs-lookup"><span data-stu-id="55fdf-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-203">Oggetto conforme a OLE Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="55fdf-203">An object that conforms to the OLE Component Object Model (COM).</span></span> <span data-ttu-id="55fdf-204">Un oggetto COM è un'istanza di una definizione di oggetto che specifica i dati dell'oggetto e una o più implementazioni di interfacce sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-204">A COM object is an instance of an object definition, which specifies the object's data and one or more implementations of interfaces on the object.</span></span> <span data-ttu-id="55fdf-205">I client interagiscono con un oggetto COM solo tramite le relative interfacce.</span><span class="sxs-lookup"><span data-stu-id="55fdf-205">Clients interact with a COM object only through its interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**oggetto collegabile**</span><span class="sxs-lookup"><span data-stu-id="55fdf-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**connectable object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-207">Oggetto COM che implementa come minimo l'interfaccia [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) per la gestione degli oggetti del punto di connessione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-207">A COM object that implements, at a minimum, the [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) interface, for the management of connection point objects.</span></span> <span data-ttu-id="55fdf-208">Gli oggetti collegabili supportano la comunicazione dal server al client.</span><span class="sxs-lookup"><span data-stu-id="55fdf-208">Connectable objects support communication from the server to the client.</span></span> <span data-ttu-id="55fdf-209">Un oggetto collegabile crea e gestisce uno o più sottooggetti del punto di connessione che ricevono gli eventi dalle interfacce implementate su altri oggetti e li inviano al client.</span><span class="sxs-lookup"><span data-stu-id="55fdf-209">A connectable object creates and manages one or more connection point subobjects, which receive events from interfaces implemented on other objects and send them on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**oggetto punto di connessione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**connection point object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-211">Oggetto COM gestito da un oggetto collegabile che implementa l'interfaccia [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-211">A COM object that is managed by a connectable object and that implements the [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) interface.</span></span> <span data-ttu-id="55fdf-212">Uno o più oggetti punto di connessione possono essere creati e gestiti da un oggetto collegabile.</span><span class="sxs-lookup"><span data-stu-id="55fdf-212">One or more connection point objects can be created and managed by a connectable object.</span></span> <span data-ttu-id="55fdf-213">Ogni oggetto punto di connessione gestisce gli eventi in ingresso da un'interfaccia specifica su un altro oggetto e li invia al client.</span><span class="sxs-lookup"><span data-stu-id="55fdf-213">Each connection point object manages incoming events from a specific interface on another object and sends those events on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**applicazione contenitore**</span><span class="sxs-lookup"><span data-stu-id="55fdf-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**container application**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-215">Un'applicazione che supporta documenti composti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-215">An application that supports compound documents.</span></span> <span data-ttu-id="55fdf-216">L'applicazione contenitore fornisce spazio di archiviazione per un oggetto incorporato o collegato, un sito per la visualizzazione, l'accesso al sito di visualizzazione e un sink consultivo per la ricezione delle notifiche delle modifiche nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-216">The container application provides storage for an embedded or linked object, a site for its display, access to the display site, and an advisory sink for receiving notifications of changes in the object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**contenimento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**containment**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-218">Tecnica di composizione per l'implementazione di oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="55fdf-218">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="55fdf-219">Consente a un oggetto di riutilizzare alcune o tutte le implementazioni dell'interfaccia di uno o più oggetti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-219">It allows one object to reuse some or all of the interface implementations of one or more other objects.</span></span> <span data-ttu-id="55fdf-220">L'oggetto esterno funge da client per gli altri oggetti, delegando l'implementazione quando si desidera utilizzare i servizi di uno degli oggetti contenuti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-220">The outer object acts as a client to the other objects, delegating implementation when it wishes to use the services of one of the contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**contesto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-222">In COM+, set di proprietà di run-time associate a uno o più oggetti COM utilizzati per fornire servizi per tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-222">In COM+, a set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**controllo**</span><span class="sxs-lookup"><span data-stu-id="55fdf-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**control**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-224">Oggetto COM riutilizzabile e incorporabile che supporta, come minimo, l'interfaccia [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-224">An embeddable, reusable COM object that supports, at a minimum, the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) interface.</span></span> <span data-ttu-id="55fdf-225">I controlli sono in genere associati all'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-225">Controls are typically associated with the user interface.</span></span> <span data-ttu-id="55fdf-226">Supportano anche la comunicazione con un contenitore e possono essere riutilizzati da più client, a seconda dei criteri di licenza.</span><span class="sxs-lookup"><span data-stu-id="55fdf-226">They also support communication with a container and can be reused by multiple clients, depending upon licensing criteria.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**contenitore di controlli**</span><span class="sxs-lookup"><span data-stu-id="55fdf-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**control container**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-228">Un'applicazione che supporta l'incorporamento dei controlli implementando l'interfaccia [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-228">An application that supports embedding of controls by implementing the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**Proprietà del controllo**</span><span class="sxs-lookup"><span data-stu-id="55fdf-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**control property**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-230">Proprietà della fase di esecuzione esposta e gestita dal controllo stesso.</span><span class="sxs-lookup"><span data-stu-id="55fdf-230">A run-time property that is exposed and managed by the control itself.</span></span> <span data-ttu-id="55fdf-231">Ad esempio, le dimensioni del tipo di carattere e del testo utilizzate dal controllo sono proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-231">For example, the font and text size used by the control are control properties.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controllo oggetto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlling object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-233">Oggetto all'interno di un oggetto aggregato che controlla quali interfacce all'interno dell'oggetto di aggregazione sono esposte e quali sono private.</span><span class="sxs-lookup"><span data-stu-id="55fdf-233">The object within an aggregate object that controls which interfaces within the aggregate object are exposed and which are private.</span></span> <span data-ttu-id="55fdf-234">L'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) dell'oggetto di controllo viene chiamata **IUnknown** di controllo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-234">The [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the controlling object is called the controlling **IUnknown**.</span></span> <span data-ttu-id="55fdf-235">Le chiamate ai metodi **IUnknown** di altri oggetti nell'aggregazione devono essere passate all' **IUnknown** di controllo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-235">Calls to **IUnknown** methods of other objects in the aggregate must be passed to the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**sito di controllo**</span><span class="sxs-lookup"><span data-stu-id="55fdf-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**control site**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-237">Struttura implementata da un contenitore di controlli per la gestione della visualizzazione e dell'archiviazione di un controllo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-237">A structure implemented by a control container for managing the display and storage of a control.</span></span> <span data-ttu-id="55fdf-238">All'interno di un determinato contenitore, ogni controllo dispone di un sito di controllo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-238">Within a given container, each control has a corresponding control site.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**oggetto trasferimento dati**</span><span class="sxs-lookup"><span data-stu-id="55fdf-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**data transfer object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-240">Oggetto che implementa l'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e contiene i dati da trasferire da un oggetto a un altro tramite gli Appunti o le operazioni di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-240">An object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface and contains data to be transferred from one object to another through either the Clipboard or drag-and-drop operations.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**gestore oggetti predefinito**</span><span class="sxs-lookup"><span data-stu-id="55fdf-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**default object handler**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-242">DLL fornita con OLE che funge da surrogato nello spazio di elaborazione dell'applicazione contenitore per l'oggetto reale.</span><span class="sxs-lookup"><span data-stu-id="55fdf-242">A DLL provided with OLE that acts as a surrogate in the processing space of the container application for the real object.</span></span>

<span data-ttu-id="55fdf-243">Con il gestore di oggetti predefinito, è possibile esaminare i dati archiviati di un oggetto senza attivare effettivamente l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-243">With the default object handler, it is possible to look at an object's stored data without actually activating the object.</span></span> <span data-ttu-id="55fdf-244">Il gestore dell'oggetto predefinito esegue altre attività, ad esempio il rendering di un oggetto dallo stato memorizzato nella cache quando l'oggetto viene caricato in memoria.</span><span class="sxs-lookup"><span data-stu-id="55fdf-244">The default object handler performs other tasks, such as rendering an object from its cached state when the object is loaded into memory.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**oggetto dipendente**</span><span class="sxs-lookup"><span data-stu-id="55fdf-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**dependent object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-246">Oggetto COM in genere inizializzato da un altro oggetto (l'oggetto host).</span><span class="sxs-lookup"><span data-stu-id="55fdf-246">A COM object that is typically initialized by another object (the host object).</span></span> <span data-ttu-id="55fdf-247">Sebbene la durata dell'oggetto dipendente possa essere utile solo per la durata dell'oggetto host, l'oggetto host non funziona come [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) di controllo per l'oggetto dipendente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-247">Although the dependent object's lifetime may only make sense during the lifetime of the host object, the host object does not function as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent object.</span></span> <span data-ttu-id="55fdf-248">Al contrario, un oggetto è un oggetto aggregato quando la relativa durata (per mezzo del conteggio dei riferimenti) è completamente controllata dall'oggetto di gestione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-248">In contrast, an object is an aggregated object when its lifetime (by means of its reference count) is completely controlled by the managing object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**modalità di accesso diretto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**direct access mode**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-250">Una delle due modalità di accesso in cui è possibile aprire un oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-250">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="55fdf-251">In modalità diretta, viene immediatamente eseguito il commit di tutte le modifiche nell'oggetto di archiviazione radice.</span><span class="sxs-lookup"><span data-stu-id="55fdf-251">In direct mode, all changes are immediately committed to the root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**oggetto Document**</span><span class="sxs-lookup"><span data-stu-id="55fdf-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**document object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-253">Documento OLE che consente di visualizzare una o più visualizzazioni attivate sul posto dei dati all'interno di un frame nativo o esterno, ad esempio un browser, mantenendo al tempo stesso il controllo completo sulla relativa interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-253">An OLE document that can display one or more in-place activated views of its data within a native or foreign frame, such as a browser, while retaining full control over its user interface.</span></span> <span data-ttu-id="55fdf-254">Oltre a implementare il normale documento OLE e le interfacce di attivazione sul posto, un oggetto Document deve implementare [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)e ognuna delle visualizzazioni (sotto forma di oggetto visualizzazione del documento) deve implementare [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span><span class="sxs-lookup"><span data-stu-id="55fdf-254">In addition to implementing the usual OLE document and in-place activation interfaces, a document object must implement [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument), and each of its views (in the form of a document view object) must implement [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**contenitore di oggetti documento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**document object container**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-256">Applicazione contenitore in grado di visualizzare una o più visualizzazioni di uno o più oggetti documento e di gestire tutti gli oggetti documento contenuti all'interno di un file.</span><span class="sxs-lookup"><span data-stu-id="55fdf-256">A container application capable of displaying one or more views of one or more document objects and of managing all contained document objects within a file.</span></span> <span data-ttu-id="55fdf-257">Ogni oggetto Document è associato a un sito del documento e ogni sito del documento contiene uno o più siti di visualizzazione del documento corrispondenti alle visualizzazioni supportate dall'oggetto Document.</span><span class="sxs-lookup"><span data-stu-id="55fdf-257">Each document object is associated with a document site, and each document site contains one or more document view sites corresponding to the views supported by the document object.</span></span> <span data-ttu-id="55fdf-258">Un contenitore di oggetti documento include anche un frame contenitore che gestisce la negoziazione di menu e barre degli strumenti e l'enumerazione di oggetti contenuti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-258">A document object container also includes a container frame, which handles menu and toolbar negotiation and the enumeration of contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**Server oggetti documento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**document object server**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-260">Applicazione server in grado di fornire oggetti documento.</span><span class="sxs-lookup"><span data-stu-id="55fdf-260">A server application capable of providing document objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**sito del documento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**document site**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-262">Sito client implementato da un contenitore di oggetti documento per gestire la visualizzazione e l'archiviazione di un oggetto documento.</span><span class="sxs-lookup"><span data-stu-id="55fdf-262">A client site implemented by a document object container for managing the display and storage of a document object.</span></span> <span data-ttu-id="55fdf-263">Ogni oggetto Document in un contenitore dispone di un sito del documento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-263">Each document object in a container has a corresponding document site.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**oggetto del sito del documento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**document site object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-265">Oggetto COM che implementa l'interfaccia [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) , oltre alle consuete interfacce del sito client (ad esempio, [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span><span class="sxs-lookup"><span data-stu-id="55fdf-265">A COM object that implements the [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) interface, in addition to the usual client-site interfaces (such as [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**visualizzazione documento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**document view**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-267">Una presentazione particolare dei dati di un documento.</span><span class="sxs-lookup"><span data-stu-id="55fdf-267">A particular presentation of a document's data.</span></span> <span data-ttu-id="55fdf-268">Un singolo oggetto Document può avere una o più visualizzazioni, ma una sola visualizzazione documento può appartenere a un solo oggetto Document.</span><span class="sxs-lookup"><span data-stu-id="55fdf-268">A single document object can have one or more views, but a single document view can belong to one and only one document object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**oggetto visualizzazione documento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**document view object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-270">Oggetto COM che implementa l'interfaccia [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) e corrisponde a una visualizzazione del documento particolare.</span><span class="sxs-lookup"><span data-stu-id="55fdf-270">A COM object that implements the [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) interface and corresponds to a particular document view.</span></span> <span data-ttu-id="55fdf-271">Un oggetto con più visualizzazioni documento aggrega un oggetto visualizzazione documento separato per ogni visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-271">An object with multiple document views aggregates a separate document view object for each view.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**sito visualizzazione documento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**document view site**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-273">Oggetto aggregato da un oggetto sito del documento per la gestione dello spazio di visualizzazione per una visualizzazione specifica di un oggetto documento.</span><span class="sxs-lookup"><span data-stu-id="55fdf-273">An object aggregated by a document site object for managing the display space for a particular view of a document object.</span></span> <span data-ttu-id="55fdf-274">All'interno di un sito di documento specifico, ogni visualizzazione documento dispone di un sito di visualizzazione del documento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-274">Within a given document site, each document view has a corresponding document view site.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**oggetto sito visualizzazione documento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**document view site object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-276">Oggetto COM aggregato in un oggetto sito del documento e implementa l'interfaccia [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) e, facoltativamente, l'interfaccia [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-276">A COM object that is aggregated in a document site object and implements the [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) interface and, optionally, the [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**trascinamento della selezione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**drag and drop**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-278">Operazione in cui l'utente finale utilizza il mouse o un altro dispositivo di puntamento per spostare i dati in un'altra posizione nella stessa finestra o in un'altra finestra.</span><span class="sxs-lookup"><span data-stu-id="55fdf-278">An operation in which the end user uses the mouse or other pointing device to move data to another location in the same window or another window.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Incorpora**</span><span class="sxs-lookup"><span data-stu-id="55fdf-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**embed**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-280">Per inserire un oggetto in un documento composto in modo da mantenere i formati di dati nativi di tale oggetto e per consentirne la modifica dall'interno del relativo contenitore utilizzando gli strumenti esposti dal server.</span><span class="sxs-lookup"><span data-stu-id="55fdf-280">To insert an object into a compound document in such a way as to preserve the data formats native to that object, and to enable it to be edited from within its container using tools exposed by its server.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**oggetto incorporato**</span><span class="sxs-lookup"><span data-stu-id="55fdf-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**embedded object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-282">Oggetto i cui dati vengono archiviati in un documento composito, ma l'oggetto viene eseguito nello spazio di elaborazione del server.</span><span class="sxs-lookup"><span data-stu-id="55fdf-282">An object whose data is stored in a compound document, but the object runs in the process space of its server.</span></span> <span data-ttu-id="55fdf-283">Il gestore dell'oggetto predefinito fornisce un surrogato nello spazio di elaborazione dell'applicazione contenitore per l'oggetto reale.</span><span class="sxs-lookup"><span data-stu-id="55fdf-283">The default object handler provides a surrogate in the processing space of the container application for the real object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**proprietà estesa**</span><span class="sxs-lookup"><span data-stu-id="55fdf-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**extended property**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-285">Proprietà della fase di esecuzione, ad esempio la posizione e le dimensioni di un controllo, che un utente presume venga esposto dal controllo, ma viene esposto e gestito dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="55fdf-285">A run-time property, such as a control's position and size, that a user would assume to be exposed by the control but is exposed and managed by the container.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**moniker del file**</span><span class="sxs-lookup"><span data-stu-id="55fdf-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**file moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-287">Moniker basato su un percorso nel file system.</span><span class="sxs-lookup"><span data-stu-id="55fdf-287">A moniker based on a path in the file system.</span></span> <span data-ttu-id="55fdf-288">I moniker dei file possono essere utilizzati per identificare gli oggetti salvati nei propri file.</span><span class="sxs-lookup"><span data-stu-id="55fdf-288">File monikers can be used to identify objects that are saved in their own files.</span></span> <span data-ttu-id="55fdf-289">Un moniker di file è un oggetto COM che supporta l'implementazione fornita dal sistema dell'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) per la classe del moniker del file.</span><span class="sxs-lookup"><span data-stu-id="55fdf-289">A file moniker is a COM object that supports the system-provided implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface for the file moniker class.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**oggetto Font**</span><span class="sxs-lookup"><span data-stu-id="55fdf-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**font object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-291">Oggetto COM che fornisce l'accesso ai tipi di carattere Graphics Device Interface (GDI) implementando l'interfaccia [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-291">A COM object that provides access to Graphics Device Interface (GDI) fonts by implementing the [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**identificatore di formato**</span><span class="sxs-lookup"><span data-stu-id="55fdf-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**format identifier**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-293">GUID che identifica un set di proprietà permanenti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-293">A GUID that identifies a persistent property set.</span></span> <span data-ttu-id="55fdf-294">Noto anche come FMTID.</span><span class="sxs-lookup"><span data-stu-id="55fdf-294">Also referred to as FMTID.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**frame**</span><span class="sxs-lookup"><span data-stu-id="55fdf-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-296">Parte di un'applicazione contenitore responsabile della negoziazione di menu, tasti di scelta rapida, barre degli strumenti e altri elementi dell'interfaccia utente condivisi con un oggetto COM incorporato o un oggetto documento.</span><span class="sxs-lookup"><span data-stu-id="55fdf-296">The part of a container application responsible for negotiating menus, accelerator keys, toolbars, and other shared user-interface elements with an embedded COM object or a document object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**oggetto frame**</span><span class="sxs-lookup"><span data-stu-id="55fdf-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**frame object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-298">Oggetto COM che implementa l'interfaccia [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) e, facoltativamente, l'interfaccia [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-298">A COM object that implements the [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) interface and, optionally, the [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**moniker composito generico**</span><span class="sxs-lookup"><span data-stu-id="55fdf-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**generic composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-300">Raccolta sequenziata di moniker, a partire da un moniker di file per fornire il percorso a livello di documento e continuare con uno o più moniker di elemento che, considerati come intero, identifica in modo univoco un oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-300">A sequenced collection of monikers, starting with a file moniker to provide the document-level path and continuing with one or more item monikers that, taken as a whole, uniquely identifies an object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**funzione helper**</span><span class="sxs-lookup"><span data-stu-id="55fdf-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**helper function**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-302">Funzione che incapsula le chiamate ad altre funzioni e metodi di interfaccia disponibili pubblicamente in OLE SDK.</span><span class="sxs-lookup"><span data-stu-id="55fdf-302">A function that encapsulates calls to other functions and interface methods publicly available in the OLE SDK.</span></span> <span data-ttu-id="55fdf-303">Le funzioni di supporto sono un modo pratico per chiamare sequenze di funzioni e metodi usati di frequente che eseguono attività comuni.</span><span class="sxs-lookup"><span data-stu-id="55fdf-303">Helper functions are a convenient way to call frequently used sequences of function and method calls that accomplish common tasks.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**oggetto host**</span><span class="sxs-lookup"><span data-stu-id="55fdf-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**host object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-305">Oggetto COM che costituisce una relazione gerarchica con uno o più oggetti COM, noti come oggetti dipendenti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-305">A COM object that forms a hierarchical relationship with one or more other COM objects, known as the dependent objects.</span></span> <span data-ttu-id="55fdf-306">In genere, l'oggetto host crea un'istanza degli oggetti dipendenti e la loro esistenza è utile solo nell'ambito della durata dell'oggetto host.</span><span class="sxs-lookup"><span data-stu-id="55fdf-306">Typically, the host object instantiates the dependent objects, and their existence only makes sense within the lifetime of the host object.</span></span> <span data-ttu-id="55fdf-307">Tuttavia, l'oggetto host non funge da [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) di controllo per gli oggetti dipendenti, né delega direttamente alle implementazioni dell'interfaccia di tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-307">However, the host object does not act as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent objects, nor does it directly delegate to the interface implementations of those objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="55fdf-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-309">Handle di risultato opaco definito come zero per un ritorno riuscito da una funzione e diverso da zero se vengono restituite informazioni sull'errore o sullo stato.</span><span class="sxs-lookup"><span data-stu-id="55fdf-309">An opaque result handle defined to be zero for a successful return from a function and nonzero if error or status information is returned.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**Hyperlink (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="55fdf-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**hyperlink object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-311">Oggetto COM che implementa come minimo l'interfaccia [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) e funge da collegamento a un oggetto in un'altra posizione, ovvero la destinazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-311">A COM object that implements, at a minimum, the [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) interface and acts as a link to an object at another location (the target).</span></span> <span data-ttu-id="55fdf-312">Un collegamento ipertestuale è costituito da quattro parti: un moniker che identifica la posizione della destinazione. stringa per la posizione all'interno della destinazione. nome descrittivo o visualizzabile per la destinazione; e una stringa che può contenere parametri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="55fdf-312">A hyperlink is made up of four parts: a moniker that identifies the target's location; a string for the location within the target; a friendly, or displayable, name for the target; and a string that can contain additional parameters.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**contesto di esplorazione collegamento ipertestuale**</span><span class="sxs-lookup"><span data-stu-id="55fdf-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**hyperlink browse context**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-314">Oggetto COM che implementa l'interfaccia [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) e gestisce lo stack di navigazione del collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="55fdf-314">A COM object that implements the [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) interface and maintains the hyperlink navigation stack.</span></span> <span data-ttu-id="55fdf-315">L'oggetto contesto browse gestisce la finestra cornice collegamento ipertestuale e la finestra dell'oggetto di destinazione del collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="55fdf-315">The browse context object manages the hyperlink frame window and hyperlink target object's window.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**contenitore collegamento ipertestuale**</span><span class="sxs-lookup"><span data-stu-id="55fdf-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**hyperlink container**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-317">Applicazione contenitore che supporta collegamenti ipertestuali implementando l'interfaccia [**IhlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) e, se gli oggetti del contenitore possono essere destinazioni di altri collegamenti ipertestuali, l'interfaccia [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-317">A container application that supports hyperlinks by implementing the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and, if the container's objects can be targets of other hyperlinks, the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**oggetto cornice collegamento ipertestuale**</span><span class="sxs-lookup"><span data-stu-id="55fdf-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**hyperlink frame object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-319">Oggetto COM che implementa l'interfaccia [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) e controlla l'esplorazione e la visualizzazione di primo livello dei collegamenti ipertestuali per il contenitore del frame e il server della destinazione del collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="55fdf-319">A COM object that implements the [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) interface and controls the top-level navigation and display of hyperlinks for the frame's container and the hyperlink target's server.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**oggetto collegamento ipertestuale**</span><span class="sxs-lookup"><span data-stu-id="55fdf-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**hyperlink site object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-321">Oggetto COM che implementa l'interfaccia [**IhlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) e fornisce il moniker o l'identificatore di interfaccia del relativo contenitore Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="55fdf-321">A COM object that implements the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and supplies either the moniker or interface identifier of its hyperlink container.</span></span> <span data-ttu-id="55fdf-322">Un sito di collegamento ipertestuale può gestire più collegamenti ipertestuali.</span><span class="sxs-lookup"><span data-stu-id="55fdf-322">One hyperlink site can serve multiple hyperlinks.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**oggetto di destinazione collegamento ipertestuale**</span><span class="sxs-lookup"><span data-stu-id="55fdf-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**hyperlink target object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-324">Oggetto COM che implementa l'interfaccia [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) e fornisce il moniker, il nome descrittivo e altre informazioni che gli altri oggetti collegamento ipertestuale utilizzeranno per spostarsi su di esso.</span><span class="sxs-lookup"><span data-stu-id="55fdf-324">A COM object that implements the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface and supplies its moniker, friendly name, and other information that other hyperlink objects will use to navigate to it.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**parametro in**</span><span class="sxs-lookup"><span data-stu-id="55fdf-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in parameter**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-326">Parametro allocato, impostato e liberato dal chiamante di una funzione o di un metodo di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="55fdf-326">A parameter that is allocated, set, and freed by the caller of a function or interface method.</span></span> <span data-ttu-id="55fdf-327">Un parametro in non viene modificato dalla funzione chiamata.</span><span class="sxs-lookup"><span data-stu-id="55fdf-327">An in parameter is not modified by the called function.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**parametro in/out**</span><span class="sxs-lookup"><span data-stu-id="55fdf-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**in/out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-329">Parametro inizialmente allocato dal chiamante di una funzione o di un metodo di interfaccia, e impostato, liberato e riallocato, se necessario, dal processo chiamato.</span><span class="sxs-lookup"><span data-stu-id="55fdf-329">A parameter that is initially allocated by the caller of a function or interface method, and set, freed, and reallocated, if necessary, by the process that is called.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**attivazione sul posto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**in-place activation**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-331">Modifica di un oggetto incorporato all'interno della finestra del relativo contenitore utilizzando gli strumenti forniti dal server.</span><span class="sxs-lookup"><span data-stu-id="55fdf-331">Editing an embedded object within the window of its container, using tools provided by the server.</span></span> <span data-ttu-id="55fdf-332">Gli oggetti collegati non supportano l'attivazione sul posto; vengono sempre modificati nella finestra del server.</span><span class="sxs-lookup"><span data-stu-id="55fdf-332">Linked objects do not support in-place activation; they are always edited in the window of the server.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**Server in-process**</span><span class="sxs-lookup"><span data-stu-id="55fdf-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**in-process server**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-334">Server implementato come una DLL eseguita nello spazio di processo del client.</span><span class="sxs-lookup"><span data-stu-id="55fdf-334">A server implemented as a DLL that runs in the process space of the client.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**istanza**</span><span class="sxs-lookup"><span data-stu-id="55fdf-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**instance**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-336">Oggetto per cui viene allocata la memoria o persistente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-336">An object for which memory is allocated or which is persistent.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="55fdf-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-338">Gruppo di funzioni semanticamente correlate che consentono di accedere a un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="55fdf-338">A group of semantically related functions that provide access to a COM object.</span></span> <span data-ttu-id="55fdf-339">Ogni interfaccia OLE definisce un contratto che consente agli oggetti di interagire in base al Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="55fdf-339">Each OLE interface defines a contract that allows objects to interact according to the Component Object Model (COM).</span></span> <span data-ttu-id="55fdf-340">Sebbene OLE fornisca molte implementazioni di interfaccia, la maggior parte delle interfacce può essere implementata anche dagli sviluppatori che progettano applicazioni OLE.</span><span class="sxs-lookup"><span data-stu-id="55fdf-340">While OLE provides many interface implementations, most interfaces can also be implemented by developers designing OLE applications.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**identificatore di interfaccia (IID)**</span><span class="sxs-lookup"><span data-stu-id="55fdf-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**interface identifier (IID)**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-342">Identificatore univoco globale (GUID) associato a un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="55fdf-342">A globally unique identifier (GUID) associated with an interface.</span></span> <span data-ttu-id="55fdf-343">Alcune funzioni accettano IID come parametri per consentire al chiamante di specificare quale puntatore a interfaccia deve essere restituito.</span><span class="sxs-lookup"><span data-stu-id="55fdf-343">Some functions take IIDs as parameters to allow the caller to specify which interface pointer should be returned.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**moniker elemento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**item moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-345">Moniker basato su una stringa che identifica un oggetto in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="55fdf-345">A moniker based on a string that identifies an object in a container.</span></span> <span data-ttu-id="55fdf-346">I moniker degli elementi possono identificare oggetti più piccoli di un file, inclusi gli oggetti incorporati in un documento composto o uno pseudo-oggetto, ad esempio un intervallo di celle in un foglio di calcolo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-346">Item monikers can identify objects smaller than a file, including embedded objects in a compound document, or a pseudo-object (like a range of cells in a spreadsheet).</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licenze**</span><span class="sxs-lookup"><span data-stu-id="55fdf-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licensing**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-348">Funzionalità di COM che consente di controllare la creazione di oggetti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-348">A feature of COM that provides control over object creation.</span></span> <span data-ttu-id="55fdf-349">Gli oggetti con licenza possono essere creati solo dai client autorizzati a utilizzarli.</span><span class="sxs-lookup"><span data-stu-id="55fdf-349">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="55fdf-350">Le licenze sono implementate in COM tramite l'interfaccia [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) e dal supporto di un codice di licenza che può essere passato in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-350">Licensing is implemented in COM through the [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**link (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="55fdf-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**link object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-352">Oggetto COM creato quando un oggetto COM collegato viene creato o caricato.</span><span class="sxs-lookup"><span data-stu-id="55fdf-352">A COM object that is created when a linked COM object is created or loaded.</span></span> <span data-ttu-id="55fdf-353">L'oggetto link viene fornito da OLE e implementa l'interfaccia [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-353">The link object is provided by OLE and implements the [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**oggetto collegato**</span><span class="sxs-lookup"><span data-stu-id="55fdf-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**linked object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-355">Oggetto COM i cui dati di origine si trovano fisicamente in cui è stato inizialmente creato.</span><span class="sxs-lookup"><span data-stu-id="55fdf-355">A COM object whose source data physically resides where it was initially created.</span></span> <span data-ttu-id="55fdf-356">Con il documento composto viene mantenuto solo un moniker che rappresenta i dati di origine e i dati di presentazione appropriati.</span><span class="sxs-lookup"><span data-stu-id="55fdf-356">Only a moniker that represents the source data and the appropriate presentation data are kept with the compound document.</span></span> <span data-ttu-id="55fdf-357">Le modifiche apportate all'origine del collegamento vengono riflesse automaticamente nell'oggetto collegato.</span><span class="sxs-lookup"><span data-stu-id="55fdf-357">Changes made to the link source are automatically reflected in the linked object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**origine collegamento**</span><span class="sxs-lookup"><span data-stu-id="55fdf-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**link source**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-359">Dati che rappresenta l'origine di un oggetto collegato.</span><span class="sxs-lookup"><span data-stu-id="55fdf-359">The data that is the source of a linked object.</span></span> <span data-ttu-id="55fdf-360">Un'origine di collegamento può essere un file o una parte di un file, ad esempio un intervallo selezionato di celle all'interno di un file (detto anche pseudo oggetto).</span><span class="sxs-lookup"><span data-stu-id="55fdf-360">A link source may be a file or a portion of a file, such as a selected range of cells within a file (also called a pseudo object).</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**stato caricato**</span><span class="sxs-lookup"><span data-stu-id="55fdf-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**loaded state**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-362">Lo stato di un oggetto dopo la relativa struttura di dati è stato caricato in memoria e accessibile al processo client.</span><span class="sxs-lookup"><span data-stu-id="55fdf-362">The state of an object after its data structures have been loaded into memory and are accessible to the client process.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**server locale**</span><span class="sxs-lookup"><span data-stu-id="55fdf-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**local server**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-364">Un server out-of-process implementato come. Applicazione EXE in esecuzione nello stesso computer dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="55fdf-364">An out-of-process server implemented as an .EXE application running on the same computer as its client application.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**blocco**</span><span class="sxs-lookup"><span data-stu-id="55fdf-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**lock**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-366">Un puntatore mantenuto e possibilmente un conteggio di riferimenti incrementato in un oggetto in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-366">A pointer held to-and possibly, a reference count incremented on-a running object.</span></span> <span data-ttu-id="55fdf-367">OLE definisce due tipi di blocchi che possono essere conservati su un oggetto: forte e debole.</span><span class="sxs-lookup"><span data-stu-id="55fdf-367">OLE defines two types of locks that can be held on an object: strong and weak.</span></span> <span data-ttu-id="55fdf-368">Per implementare un blocco sicuro, è necessario che un server mantenga sia un puntatore che un conteggio dei riferimenti, in modo che l'oggetto rimanga "bloccato" nella memoria almeno finché il server non chiama [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="55fdf-368">To implement a strong lock, a server must maintain both a pointer and a reference count, so that the object will remain "locked" in memory at least until the server calls [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="55fdf-369">Per implementare un blocco debole, il server gestisce solo un puntatore all'oggetto, in modo che l'oggetto possa essere eliminato da un altro processo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-369">To implement a weak lock, the server maintains only a pointer to the object, so that the object can be destroyed by another process.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshalling**</span><span class="sxs-lookup"><span data-stu-id="55fdf-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-371">Creazione di pacchetti e invio di chiamate al metodo di interfaccia attraverso limiti di thread o processi.</span><span class="sxs-lookup"><span data-stu-id="55fdf-371">Packaging and sending interface method calls across thread or process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**tipo di supporto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**media type**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-373">Estensione MIME che consente la negoziazione del formato dati tra un client e un oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-373">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Tipo di contenuto MIME**</span><span class="sxs-lookup"><span data-stu-id="55fdf-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**MIME content type**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-375">Estensione MIME che consente la negoziazione del formato dati tra un client e un oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-375">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Multipurpose Internet Mail Extension (MIME)**</span><span class="sxs-lookup"><span data-stu-id="55fdf-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Multipurpose Internet Mail Extension (MIME)**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-377">Protocollo Internet sviluppato originariamente per consentire lo scambio di messaggi di posta elettronica con contenuti avanzati in ambienti di rete, computer e posta elettronica eterogenei.</span><span class="sxs-lookup"><span data-stu-id="55fdf-377">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, computer, and email environments.</span></span> <span data-ttu-id="55fdf-378">In pratica, MIME è stato inoltre adottato ed esteso da applicazioni non di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="55fdf-378">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**</span><span class="sxs-lookup"><span data-stu-id="55fdf-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-380">Oggetto che implementa l'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-380">An object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="55fdf-381">Un moniker funge da nome che identifica in modo univoco un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="55fdf-381">A moniker acts as a name that uniquely identifies a COM object.</span></span> <span data-ttu-id="55fdf-382">Nello stesso modo in cui un percorso identifica un file nel file system, un moniker identifica un oggetto COM nello spazio dei nomi della directory.</span><span class="sxs-lookup"><span data-stu-id="55fdf-382">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**Classe moniker**</span><span class="sxs-lookup"><span data-stu-id="55fdf-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker class**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-384">Implementazione dell'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-384">An implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="55fdf-385">Le classi del moniker fornite dal sistema includono moniker di file, moniker di elementi, moniker compositi generici, anti-moniker, moniker di puntatore e moniker URL.</span><span class="sxs-lookup"><span data-stu-id="55fdf-385">System-supplied moniker classes include file monikers, item monikers, generic composite monikers, anti-monikers, pointer monikers, and URL monikers.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**client moniker**</span><span class="sxs-lookup"><span data-stu-id="55fdf-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**moniker client**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-387">Applicazione che usa i moniker per acquisire i puntatori di interfaccia agli oggetti gestiti da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-387">An application that uses monikers to acquire interface pointers to objects managed by another application.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**provider moniker**</span><span class="sxs-lookup"><span data-stu-id="55fdf-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**moniker provider**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-389">Applicazione che rende disponibili moniker che identificano gli oggetti gestiti, in modo che gli oggetti siano accessibili ad altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="55fdf-389">An application that makes available monikers that identify the objects it manages, so that the objects are accessible to other applications.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**estensione dello spazio dei nomi**</span><span class="sxs-lookup"><span data-stu-id="55fdf-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-391">Oggetto COM in-process che implementa [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)e [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), che vengono talvolta definiti interfacce di estensione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="55fdf-391">An in-process COM object that implements [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), and [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), which are sometimes referred to as the namespace extension interfaces.</span></span> <span data-ttu-id="55fdf-392">Un'estensione dello spazio dei nomi viene utilizzata per estendere lo spazio dei nomi della shell o per creare uno spazio dei nomi separato.</span><span class="sxs-lookup"><span data-stu-id="55fdf-392">A namespace extension is used either to extend the shell's namespace or to create a separate namespace.</span></span> <span data-ttu-id="55fdf-393">Gli utenti primari sono le finestre di dialogo Esplora risorse e file comuni.</span><span class="sxs-lookup"><span data-stu-id="55fdf-393">Primary users are the Windows Explorer and common file dialog boxes.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**dati nativi**</span><span class="sxs-lookup"><span data-stu-id="55fdf-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**native data**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-395">Dati utilizzati da un'applicazione server OLE durante la modifica di un oggetto incorporato.</span><span class="sxs-lookup"><span data-stu-id="55fdf-395">The data used by an OLE server application when editing an embedded object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**oggetto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-397">In OLE, una struttura di programmazione che incapsula i dati e le funzionalità che vengono definiti e allocati come singola unità e per cui l'unico accesso pubblico è attraverso le interfacce della struttura di programmazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-397">In OLE, a programming structure encapsulating both data and functionality that are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="55fdf-398">Un oggetto COM deve supportare come minimo l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , che mantiene l'esistenza dell'oggetto mentre viene utilizzata e fornisce l'accesso alle altre interfacce dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-398">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**stato dell'oggetto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**object state**</span></span> 
</dt> <dd>

<span data-ttu-id="55fdf-400">Relazione tra un oggetto documento composto nel relativo contenitore e l'applicazione responsabile della creazione dell'oggetto: attivo, passivo, caricato o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-400">The relationship between a compound document object in its container and the application responsible for the object's creation: active, passive, loaded, or running.</span></span> <span data-ttu-id="55fdf-401">Gli oggetti passivi vengono archiviati su disco o in un database e l'oggetto non è selezionato o attivo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-401">Passive objects are stored on disk or in a database, and the object is not selected or active.</span></span> <span data-ttu-id="55fdf-402">Nello stato Loaded, le strutture di dati dell'oggetto sono state caricate in memoria, ma non sono disponibili per operazioni come la modifica.</span><span class="sxs-lookup"><span data-stu-id="55fdf-402">In the loaded state, the object's data structures have been loaded into memory, but they are not available for operations such as editing.</span></span> <span data-ttu-id="55fdf-403">Gli oggetti in esecuzione sono entrambi caricati e disponibili per tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="55fdf-403">Running objects are both loaded and available for all operations.</span></span> <span data-ttu-id="55fdf-404">Gli oggetti attivi eseguono oggetti con un'interfaccia utente visibile.</span><span class="sxs-lookup"><span data-stu-id="55fdf-404">Active objects are running objects that have a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**nome del tipo di oggetto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**object type name**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-406">Stringa di identificazione univoca archiviata come parte delle informazioni disponibili per un oggetto nel database di registrazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-406">A unique identification string that is stored as part of the information available for an object in the registration database.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLE**</span><span class="sxs-lookup"><span data-stu-id="55fdf-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLE**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-408">Tecnologia basata su oggetti Microsoft per la condivisione di informazioni e servizi tra i limiti del computer e del processo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-408">Microsoft's object-based technology for sharing information and services across process and computer boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**server out-of-process**</span><span class="sxs-lookup"><span data-stu-id="55fdf-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**out-of-process server**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-410">Un server, implementato come. Applicazione EXE, che viene eseguita all'esterno del processo del client, nello stesso computer o in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-410">A server, implemented as an .EXE application, which runs outside the process of its client, either on the same computer or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**parametro out**</span><span class="sxs-lookup"><span data-stu-id="55fdf-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-412">Un parametro out viene allocato dalla funzione chiamata e liberata dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="55fdf-412">An out parameter is allocated by the function being called, and freed by caller.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**stato passivo**</span><span class="sxs-lookup"><span data-stu-id="55fdf-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**passive state**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-414">Stato di un oggetto COM quando è archiviato (su disco o in un database).</span><span class="sxs-lookup"><span data-stu-id="55fdf-414">The state of a COM object when it is stored (on disk or in a database).</span></span> <span data-ttu-id="55fdf-415">L'oggetto non è selezionato o attivo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-415">The object is not selected or active.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**Proprietà persistente**</span><span class="sxs-lookup"><span data-stu-id="55fdf-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**persistent property**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-417">Informazioni che possono essere archiviate in modo permanente come parte di un oggetto di archiviazione, ad esempio un file o una directory.</span><span class="sxs-lookup"><span data-stu-id="55fdf-417">Information that can be stored persistently as part of a storage object such as a file or directory.</span></span> <span data-ttu-id="55fdf-418">Le proprietà permanenti vengono raggruppate in set di proprietà, che possono essere visualizzati e modificati.</span><span class="sxs-lookup"><span data-stu-id="55fdf-418">Persistent properties are grouped into property sets, which can be displayed and edited.</span></span>

<span data-ttu-id="55fdf-419">Una proprietà persistente è diversa dalle proprietà di runtime di oggetti creati con controlli OLE e tecnologie di automazione, che possono essere utilizzate per influire sul comportamento del sistema.</span><span class="sxs-lookup"><span data-stu-id="55fdf-419">A persistent property is different from the run-time properties of objects created with OLE Controls and Automation technologies, which can be used to affect system behavior.</span></span> <span data-ttu-id="55fdf-420">La struttura [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) definisce tutti i tipi validi di proprietà permanenti, mentre la struttura **Variant** definisce tutti i tipi validi di proprietà della fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-420">The [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) structure defines all valid types of persistent properties, whereas the **VARIANT** structure defines all valid types of run-time properties.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**archiviazione permanente**</span><span class="sxs-lookup"><span data-stu-id="55fdf-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-422">Archiviazione di un file o di un oggetto in un supporto, ad esempio un file system o un database, in modo che l'oggetto e i relativi dati vengano mantenuti quando il file viene chiuso e riaperto in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="55fdf-422">Storage of a file or object in a medium such as a file system or database so that the object and its data persist when the file is closed and then re-opened at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**oggetto Picture**</span><span class="sxs-lookup"><span data-stu-id="55fdf-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**picture object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-424">Oggetto COM che fornisce l'accesso alle immagini GDI implementando l'interfaccia [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-424">A COM object that provides access to GDI images by implementing the [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**moniker puntatore**</span><span class="sxs-lookup"><span data-stu-id="55fdf-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**pointer moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-426">Moniker che esegue il mapping di un puntatore a interfaccia a un oggetto in memoria.</span><span class="sxs-lookup"><span data-stu-id="55fdf-426">A moniker that maps an interface pointer to an object in memory.</span></span> <span data-ttu-id="55fdf-427">Mentre la maggior parte dei moniker identifica gli oggetti che possono essere archiviati in modo permanente, i moniker del puntatore identificano gli oggetti che non possono.</span><span class="sxs-lookup"><span data-stu-id="55fdf-427">Whereas most monikers identify objects that can be persistently stored, pointer monikers identify objects that cannot.</span></span> <span data-ttu-id="55fdf-428">Consentono a tali oggetti di partecipare a un'operazione di associazione del moniker.</span><span class="sxs-lookup"><span data-stu-id="55fdf-428">They allow such objects to participate in a moniker binding operation.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**dati di presentazione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**presentation data**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-430">Dati utilizzati da un contenitore per la visualizzazione di oggetti incorporati o collegati.</span><span class="sxs-lookup"><span data-stu-id="55fdf-430">The data used by a container to display embedded or linked objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**verbo primario**</span><span class="sxs-lookup"><span data-stu-id="55fdf-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**primary verb**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-432">L'azione associata all'operazione più comune o preferita eseguita dagli utenti in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-432">The action associated with the most common or preferred operation users perform on an object.</span></span> <span data-ttu-id="55fdf-433">Il verbo primario è sempre definito come verbo zero nel database di registrazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="55fdf-433">The primary verb is always defined as verb zero in the system registration database.</span></span> <span data-ttu-id="55fdf-434">Il verbo primario di un oggetto viene eseguito facendo doppio clic sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-434">An object's primary verb is executed by double-clicking on the object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="55fdf-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-436">Informazioni associate a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-436">Information that is associated with an object.</span></span> <span data-ttu-id="55fdf-437">In OLE le proprietà rientrano in due categorie: proprietà della fase di esecuzione e proprietà permanenti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-437">In OLE, properties fall into two categories: run-time properties and persistent properties.</span></span> <span data-ttu-id="55fdf-438">Le proprietà in fase di esecuzione sono in genere associate a oggetti controllo o ai relativi contenitori.</span><span class="sxs-lookup"><span data-stu-id="55fdf-438">Run-time properties are typically associated with control objects or their containers.</span></span> <span data-ttu-id="55fdf-439">Il colore di sfondo, ad esempio, è una proprietà della fase di esecuzione impostata dal contenitore di un controllo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-439">For example, background color is a run-time property set by a control's container.</span></span> <span data-ttu-id="55fdf-440">Le proprietà permanenti sono associate a oggetti archiviati.</span><span class="sxs-lookup"><span data-stu-id="55fdf-440">Persistent properties are associated with stored objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**frame proprietà**</span><span class="sxs-lookup"><span data-stu-id="55fdf-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**property frame**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-442">Meccanismo dell'interfaccia utente che visualizza una o più pagine delle proprietà per un controllo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-442">The user interface mechanism that displays one or more property pages for a control.</span></span> <span data-ttu-id="55fdf-443">Il sistema di runtime dei controlli OLE fornisce un'implementazione standard di un frame di proprietà a cui è possibile accedere tramite la funzione di supporto [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-443">The OLE Controls run-time system provides a standard implementation of a property frame that can be accessed by using the [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) helper function.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**identificatore di proprietà**</span><span class="sxs-lookup"><span data-stu-id="55fdf-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**property identifier**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-445">Intero con segno a quattro byte che identifica una proprietà persistente all'interno di un set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="55fdf-445">A four-byte signed integer that identifies a persistent property within a property set.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**pagina delle proprietà**</span><span class="sxs-lookup"><span data-stu-id="55fdf-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**property page**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-447">Oggetto COM con il proprio CLSID che fa parte di un'interfaccia utente, implementata da un controllo e che consente di visualizzare e impostare le proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-447">A COM object with its own CLSID that is part of a user interface, implemented by a control, and allows the control's properties to be viewed and set.</span></span> <span data-ttu-id="55fdf-448">Gli oggetti della pagina delle proprietà implementano l'interfaccia [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-448">Property page objects implement the [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**sito della pagina delle proprietà**</span><span class="sxs-lookup"><span data-stu-id="55fdf-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**property page site**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-450">Posizione all'interno di un frame di proprietà in cui viene visualizzata una pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="55fdf-450">The location within a property frame where a property page is displayed.</span></span> <span data-ttu-id="55fdf-451">Il frame della proprietà implementa l'interfaccia [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) , che contiene i metodi per gestire i siti di ogni pagina delle proprietà fornita da un controllo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-451">The property frame implements the [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) interface, which contains methods to manage the sites of each of the property pages supplied by a control.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**set di proprietà**</span><span class="sxs-lookup"><span data-stu-id="55fdf-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**property set**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-453">Un gruppo di proprietà correlate logicamente associato a un oggetto archiviato in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-453">A logically related group of properties that is associated with a persistently stored object.</span></span> <span data-ttu-id="55fdf-454">Per creare, aprire, eliminare o enumerare uno o più set di proprietà, implementare l'interfaccia [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-454">To create, open, delete, or enumerate one or more property sets, implement the [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="55fdf-455">Se si usano file composti, è possibile usare l'implementazione di OLE di questa interfaccia anziché implementarne di personalizzati.</span><span class="sxs-lookup"><span data-stu-id="55fdf-455">If you are using compound files, you can use OLE's implementation of this interface rather than implementing your own.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**archiviazione set di proprietà**</span><span class="sxs-lookup"><span data-stu-id="55fdf-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**property set storage**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-457">Oggetto di archiviazione COM che include un set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="55fdf-457">A COM storage object that holds a property set.</span></span> <span data-ttu-id="55fdf-458">Una risorsa di archiviazione del set di proprietà è un oggetto dipendente associato a e gestito da un oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-458">A property set storage is a dependent object associated with and managed by a storage object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**finestra delle proprietà**</span><span class="sxs-lookup"><span data-stu-id="55fdf-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**property sheet**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-460">Set di pagine delle proprietà per uno o più oggetti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-460">A set of property pages for one or more objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**proxy**</span><span class="sxs-lookup"><span data-stu-id="55fdf-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**proxy**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-462">Oggetto specifico dell'interfaccia che consente di impacchettare i parametri per l'interfaccia in preparazione per una chiamata a un metodo remoto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-462">An interface-specific object that packages parameters for that interface in preparation for a remote method call.</span></span> <span data-ttu-id="55fdf-463">Un proxy viene eseguito nello spazio degli indirizzi del mittente e comunica con uno stub corrispondente nello spazio degli indirizzi del destinatario.</span><span class="sxs-lookup"><span data-stu-id="55fdf-463">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**gestione proxy**</span><span class="sxs-lookup"><span data-stu-id="55fdf-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-465">Nel marshalling standard, proxy che gestisce tutti i proxy di interfaccia per un singolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-465">In standard marshaling, a proxy that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo-oggetto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-467">Parte di un documento o di un oggetto incorporato, ad esempio un intervallo di celle in un foglio di calcolo, che può essere l'origine di un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="55fdf-467">A portion of a document or embedded object, such as a range of cells in a spreadsheet, that can be the source for a COM object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**conteggio dei riferimenti**</span><span class="sxs-lookup"><span data-stu-id="55fdf-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-469">Conservazione di un conteggio di ogni puntatore di interfaccia in un oggetto per garantire che l'oggetto non venga eliminato definitivamente prima del rilascio di tutti i relativi riferimenti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-469">Keeping a count of each interface pointer held on an object to ensure that the object is not destroyed before all references to it are released.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**moniker relativo**</span><span class="sxs-lookup"><span data-stu-id="55fdf-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**relative moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-471">Moniker che specifica la posizione di un oggetto rispetto alla posizione di un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-471">A moniker that specifies the location of an object relative to the location of another object.</span></span> <span data-ttu-id="55fdf-472">Un moniker relativo è analogo a un percorso relativo, ad esempio. \\ backup \\ report. old.</span><span class="sxs-lookup"><span data-stu-id="55fdf-472">A relative moniker is analogous to a relative path, such as ..\\backup\\report.old.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**server remoto**</span><span class="sxs-lookup"><span data-stu-id="55fdf-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**remote server**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-474">Un'applicazione server, implementata come EXE, in esecuzione in un computer diverso dall'applicazione client che la utilizza.</span><span class="sxs-lookup"><span data-stu-id="55fdf-474">A server application, implemented as an EXE, running on a different computer from the client application using it.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**ripristinare**</span><span class="sxs-lookup"><span data-stu-id="55fdf-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**revert**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-476">Per rimuovere le modifiche apportate a un oggetto a partire dall'ultima volta in cui è stato eseguito il commit delle modifiche o l'archiviazione dell'oggetto è stata aperta.</span><span class="sxs-lookup"><span data-stu-id="55fdf-476">To discard any changes made to an object since the last time the changes were committed or the object's storage was opened.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**oggetto di archiviazione radice**</span><span class="sxs-lookup"><span data-stu-id="55fdf-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**root storage object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-478">Oggetto di archiviazione più esterno in un documento.</span><span class="sxs-lookup"><span data-stu-id="55fdf-478">The outermost storage object in a document.</span></span> <span data-ttu-id="55fdf-479">Un oggetto di archiviazione radice può contenere altri oggetti di archiviazione e di flusso annidati.</span><span class="sxs-lookup"><span data-stu-id="55fdf-479">A root storage object can contain other nested storage and stream objects.</span></span> <span data-ttu-id="55fdf-480">Ad esempio, un documento composto viene salvato su disco come una serie di oggetti di archiviazione e di flusso all'interno di un oggetto di archiviazione radice.</span><span class="sxs-lookup"><span data-stu-id="55fdf-480">For example, a compound document is saved on disk as a series of storage and stream objects within a root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**stato di esecuzione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**running state**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-482">Stato di un oggetto COM quando viene eseguita l'applicazione server ed è possibile accedere alle relative interfacce e ricevere una notifica delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="55fdf-482">The state of a COM object when its server application is running and it is possible to access its interfaces and receive notification of changes.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**esecuzione tabella oggetti (ROT)**</span><span class="sxs-lookup"><span data-stu-id="55fdf-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**running object table (ROT)**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-484">Tabella accessibile a livello globale in ogni computer che tiene traccia di tutti gli oggetti COM nello stato di esecuzione che possono essere identificati da un moniker.</span><span class="sxs-lookup"><span data-stu-id="55fdf-484">A globally accessible table on each computer that keeps track of all COM objects in the running state that can be identified by a moniker.</span></span> <span data-ttu-id="55fdf-485">I provider moniker registrano un oggetto nella tabella, che incrementa il conteggio dei riferimenti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-485">Moniker providers register an object in the table, which increments the object's reference count.</span></span> <span data-ttu-id="55fdf-486">Prima che l'oggetto possa essere eliminato definitivamente, il moniker deve essere rilasciato dalla tabella.</span><span class="sxs-lookup"><span data-stu-id="55fdf-486">Before the object can be destroyed, its moniker must be released from the table.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**Proprietà della fase di esecuzione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**run-time property**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-488">Informazioni di stato discrete associate a un oggetto controllo o al relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="55fdf-488">Discrete state information associated with a control object or its container.</span></span> <span data-ttu-id="55fdf-489">Sono disponibili tre tipi di proprietà di runtime: proprietà di ambiente, proprietà del controllo e proprietà estese.</span><span class="sxs-lookup"><span data-stu-id="55fdf-489">There are three types of run-time properties: ambient properties, control properties, and extended properties.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**registrazione automatica**</span><span class="sxs-lookup"><span data-stu-id="55fdf-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**self-registration**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-491">Processo mediante il quale un server può eseguire le proprie operazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="55fdf-491">The process by which a server can perform its own registry operations.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**applicazione server**</span><span class="sxs-lookup"><span data-stu-id="55fdf-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**server application**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-493">Un'applicazione in grado di creare oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="55fdf-493">An application that can create COM objects.</span></span> <span data-ttu-id="55fdf-494">Le applicazioni contenitore possono quindi incorporare o collegarsi a questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="55fdf-494">Container applications can then embed or link to these objects.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**oggetto statico**</span><span class="sxs-lookup"><span data-stu-id="55fdf-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**static object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-496">Oggetto che contiene solo una presentazione, senza dati nativi.</span><span class="sxs-lookup"><span data-stu-id="55fdf-496">An object that contains only a presentation, with no native data.</span></span> <span data-ttu-id="55fdf-497">Un contenitore può considerare un oggetto statico come se fosse un oggetto collegato o incorporato, ad eccezione del fatto che non è possibile modificare un oggetto statico.</span><span class="sxs-lookup"><span data-stu-id="55fdf-497">A container can treat a static object as though it were a linked or embedded object, except that it is not possible to edit a static object.</span></span>

<span data-ttu-id="55fdf-498">Un oggetto statico può risultare, ad esempio, dalla suddivisione di un collegamento su un oggetto collegato, ovvero l'applicazione server non è disponibile o l'utente non desidera che l'oggetto collegato venga aggiornato più.</span><span class="sxs-lookup"><span data-stu-id="55fdf-498">A static object can result, for example, from the breaking of a link on a linked object-that is, the server application is unavailable, or the user doesn't want the linked object to be updated anymore.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**oggetto di archiviazione**</span><span class="sxs-lookup"><span data-stu-id="55fdf-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**storage object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-500">Oggetto COM che implementa l'interfaccia [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-500">A COM object that implements the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="55fdf-501">Un oggetto di archiviazione contiene oggetti di archiviazione annidati o oggetti flusso, ottenendo l'equivalente di una struttura di directory/file all'interno di un singolo file.</span><span class="sxs-lookup"><span data-stu-id="55fdf-501">A storage object contains nested storage objects or stream objects, resulting in the equivalent of a directory/file structure within a single file.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**oggetto Stream**</span><span class="sxs-lookup"><span data-stu-id="55fdf-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**stream object**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-503">Oggetto COM che implementa l'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-503">A COM object that implements the [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="55fdf-504">Un oggetto flusso è analogo a un file in una directory/file system.</span><span class="sxs-lookup"><span data-stu-id="55fdf-504">A stream object is analogous to a file in a directory/file system.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Archiviazione strutturata**</span><span class="sxs-lookup"><span data-stu-id="55fdf-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Structured Storage**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-506">Tecnologia OLE per l'archiviazione di file composti in file System nativi.</span><span class="sxs-lookup"><span data-stu-id="55fdf-506">OLE's technology for storing compound files in native file systems.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**Stub**</span><span class="sxs-lookup"><span data-stu-id="55fdf-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**stub**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-508">Quando viene effettuato il marshalling dei parametri di un metodo di interfaccia o di una funzione attraverso un limite del processo, lo stub è un oggetto specifico dell'interfaccia che consente di decreare il pacchetto dei parametri di marshalling e di chiamare il metodo richiesto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-508">When a function's or interface method's parameters are marshaled across a process boundary, the stub is an interface-specific object that unpackages the marshaled parameters and calls the required method.</span></span> <span data-ttu-id="55fdf-509">Lo stub viene eseguito nello spazio degli indirizzi del destinatario e comunica con un proxy corrispondente nello spazio degli indirizzi del mittente.</span><span class="sxs-lookup"><span data-stu-id="55fdf-509">The stub runs in the receiver's address space and communicates with a corresponding proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**gestione Stub**</span><span class="sxs-lookup"><span data-stu-id="55fdf-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**stub manager**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-511">Gestisce tutti gli stub di interfaccia per un singolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="55fdf-511">Manages all of the interface stubs for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**chiamata sincrona**</span><span class="sxs-lookup"><span data-stu-id="55fdf-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**synchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-513">Una chiamata di funzione che non consente l'esecuzione di istruzioni aggiuntive nel processo chiamante finché la funzione non restituisce.</span><span class="sxs-lookup"><span data-stu-id="55fdf-513">A function call that does not allow further instructions in the calling process to be executed until the function returns.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**Registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="55fdf-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**system registry**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-515">Un repository di informazioni a livello di sistema supportato da Windows, che contiene informazioni sul sistema e le relative applicazioni, inclusi client e server OLE.</span><span class="sxs-lookup"><span data-stu-id="55fdf-515">A system-wide repository of information supported by Windows, which contains information about the system and its applications, including OLE clients and servers.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**modalità di accesso transazionale**</span><span class="sxs-lookup"><span data-stu-id="55fdf-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**transacted access mode**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-517">Una delle due modalità di accesso in cui è possibile aprire un oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-517">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="55fdf-518">Quando viene aperto in modalità transazionale, le modifiche vengono archiviate nei buffer finché l'oggetto di archiviazione radice non esegue il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="55fdf-518">When opened in transacted mode, changes are stored in buffers until the root storage object commits its changes.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**informazioni sul tipo**</span><span class="sxs-lookup"><span data-stu-id="55fdf-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**type information**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-520">Informazioni sulla classe di un oggetto fornita da una libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="55fdf-520">Information about an object's class provided by a type library.</span></span> <span data-ttu-id="55fdf-521">Per fornire informazioni sul tipo, un oggetto COM implementa l'interfaccia [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-521">To provide type information, a COM object implements the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interface.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**trasferimento dati uniforme**</span><span class="sxs-lookup"><span data-stu-id="55fdf-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**uniform data transfer**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-523">Modello per il trasferimento dei dati attraverso gli appunti, il trascinamento della selezione o l'automazione.</span><span class="sxs-lookup"><span data-stu-id="55fdf-523">A model for transferring data through the clipboard, drag and drop, or Automation.</span></span> <span data-ttu-id="55fdf-524">Gli oggetti conformi a questo modello implementano l'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="55fdf-524">Objects conforming to this model implement the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="55fdf-525">Questo modello sostituisce DDE (Dynamic Data Exchange).</span><span class="sxs-lookup"><span data-stu-id="55fdf-525">This model replaces DDE (dynamic data exchange).</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**</span><span class="sxs-lookup"><span data-stu-id="55fdf-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-527">Decompressione dei parametri che sono stati inviati a un proxy tra i limiti del processo.</span><span class="sxs-lookup"><span data-stu-id="55fdf-527">Unpacking parameters that have been sent to a proxy across process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**URL (Universal Resource Locator)**</span><span class="sxs-lookup"><span data-stu-id="55fdf-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**universal resource locator (URL)**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-529">Identificatore utilizzato dal World Wide Web per i nomi e le posizioni degli oggetti su Internet.</span><span class="sxs-lookup"><span data-stu-id="55fdf-529">The identifier used by the World Wide Web for the names and locations of objects on the Internet.</span></span> <span data-ttu-id="55fdf-530">OLE fornisce una classe moniker, moniker URL, la cui implementazione può essere utilizzata per associare un client a oggetti identificati da un URL.</span><span class="sxs-lookup"><span data-stu-id="55fdf-530">OLE provides a moniker class, URL moniker, whose implementation can be used to bind a client to objects identified by a URL.</span></span>

</dd> <dt>

<span data-ttu-id="55fdf-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Moniker URL**</span><span class="sxs-lookup"><span data-stu-id="55fdf-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**URL moniker**</span></span>
</dt> <dd>

<span data-ttu-id="55fdf-532">Moniker basato su un URL (Universal Resource Locator).</span><span class="sxs-lookup"><span data-stu-id="55fdf-532">A moniker based on a universal resource locator (URL).</span></span> <span data-ttu-id="55fdf-533">Un client può usare i moniker URL per eseguire l'associazione a oggetti che si trovano su Internet.</span><span class="sxs-lookup"><span data-stu-id="55fdf-533">A client can use URL monikers to bind to objects that reside on the Internet.</span></span> <span data-ttu-id="55fdf-534">La classe del moniker URL fornita dal sistema supporta l'associazione sincrona e asincrona.</span><span class="sxs-lookup"><span data-stu-id="55fdf-534">The system-supplied URL moniker class supports both synchronous and asynchronous binding.</span></span>

</dd> </dl>

 

 