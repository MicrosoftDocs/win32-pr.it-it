---
description: Introduzione allo sviluppo di filtri DirectShow
ms.assetid: d5162ea4-ef37-4993-a82c-782f03b08c64
title: Introduzione allo sviluppo di filtri DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a42c5d2437b32f521b0efc39775f186267d3c99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303957"
---
# <a name="introduction-to-directshow-filter-development"></a><span data-ttu-id="7107b-103">Introduzione allo sviluppo di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="7107b-103">Introduction to DirectShow Filter Development</span></span>

<span data-ttu-id="7107b-104">Questa sezione fornisce una breve descrizione delle attività necessarie per lo sviluppo di un filtro DirectShow personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7107b-104">This section gives a brief outline of the tasks involved in developing a custom DirectShow filter.</span></span> <span data-ttu-id="7107b-105">Vengono inoltre forniti collegamenti ad argomenti che illustrano queste attività in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="7107b-105">It also provides links to topics that discuss these tasks in greater detail.</span></span> <span data-ttu-id="7107b-106">Prima di leggere questa sezione, leggere gli argomenti [relativi a DirectShow](about-directshow.md), che descrivono l'architettura complessiva di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7107b-106">Before reading this section, read the topics in [About DirectShow](about-directshow.md), which describe the overall DirectShow architecture.</span></span>

<span data-ttu-id="7107b-107">**Libreria di classi base DirectShow**</span><span class="sxs-lookup"><span data-stu-id="7107b-107">**DirectShow Base Class Library**</span></span>

<span data-ttu-id="7107b-108">DirectShow SDK include un set di classi C++ per la scrittura dei filtri.</span><span class="sxs-lookup"><span data-stu-id="7107b-108">The DirectShow SDK includes a set of C++ classes for writing filters.</span></span> <span data-ttu-id="7107b-109">Sebbene non siano necessari, queste classi rappresentano la modalità consigliata per scrivere un nuovo filtro.</span><span class="sxs-lookup"><span data-stu-id="7107b-109">Although they are not required, these classes are the recommended way to write a new filter.</span></span> <span data-ttu-id="7107b-110">Per usare le classi base, compilarle in una libreria statica e collegare il file con estensione LIB al progetto, come descritto in [creazione di filtri DirectShow](building-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7107b-110">To use the base classes, compile them into a static library and link the .lib file to your project, as described in [Building DirectShow Filters](building-directshow-filters.md).</span></span>

<span data-ttu-id="7107b-111">La libreria di classi di base definisce una classe radice per i filtri, la classe [**CBaseFilter**](cbasefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="7107b-111">The base class library defines a root class for filters, the [**CBaseFilter**](cbasefilter.md) class.</span></span> <span data-ttu-id="7107b-112">Diverse altre classi derivano da **CBaseFilter** e sono specializzate per determinati tipi di filtri.</span><span class="sxs-lookup"><span data-stu-id="7107b-112">Several other classes derive from **CBaseFilter**, and are specialized for particular kinds of filters.</span></span> <span data-ttu-id="7107b-113">Ad esempio, la classe [**CTransformFilter**](ctransformfilter.md) è progettata per i filtri di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="7107b-113">For example, the [**CTransformFilter**](ctransformfilter.md) class is designed for transform filters.</span></span> <span data-ttu-id="7107b-114">Per creare un nuovo filtro, implementare una classe che eredita da una delle classi di filtro.</span><span class="sxs-lookup"><span data-stu-id="7107b-114">To create a new filter, implement a class that inherits from one of the filter classes.</span></span> <span data-ttu-id="7107b-115">Ad esempio, la dichiarazione di classe potrebbe essere la seguente:</span><span class="sxs-lookup"><span data-stu-id="7107b-115">For example, your class declaration might be as follows:</span></span>


```C++
class CMyFilter : public CTransformFilter
{
private:
    /* Declare variables and methods that are specific to your filter.
public:
    /* Override various methods in CTransformFilter */
};
```



<span data-ttu-id="7107b-116">Per ulteriori informazioni sulle classi base di DirectShow, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7107b-116">For more information about the DirectShow base classes, see the following topics:</span></span>

-   [<span data-ttu-id="7107b-117">Classi base di DirectShow</span><span class="sxs-lookup"><span data-stu-id="7107b-117">DirectShow Base Classes</span></span>](directshow-base-classes.md)
-   [<span data-ttu-id="7107b-118">Creazione di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="7107b-118">Building DirectShow Filters</span></span>](building-directshow-filters.md)

<span data-ttu-id="7107b-119">**Creazione di pin**</span><span class="sxs-lookup"><span data-stu-id="7107b-119">**Creating Pins**</span></span>

<span data-ttu-id="7107b-120">Un filtro deve creare uno o più pin.</span><span class="sxs-lookup"><span data-stu-id="7107b-120">A filter must create one or more pins.</span></span> <span data-ttu-id="7107b-121">Il numero di pin può essere corretto in fase di progettazione oppure il filtro può creare nuovi PIN in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="7107b-121">The number of pins can be fixed at design time, or the filter can create new pins as needed.</span></span> <span data-ttu-id="7107b-122">I pin derivano in genere dalla classe [**CBasePin**](cbasepin.md) o da una classe che eredita **CBasePin**, ad esempio [**CBaseInputPin**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="7107b-122">Pins generally derive from the [**CBasePin**](cbasepin.md) class, or from a class that inherits **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md).</span></span> <span data-ttu-id="7107b-123">I pin del filtro devono essere dichiarati come variabili membro nella classe filter.</span><span class="sxs-lookup"><span data-stu-id="7107b-123">The filter's pins should be declared as member variables in the filter class.</span></span> <span data-ttu-id="7107b-124">Alcune classi di filtro definiscono già i pin, ma se il filtro eredita direttamente da **CBaseFilter**, è necessario dichiarare i pin nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="7107b-124">Some of the filter classes already define the pins, but if your filter inherits directly from **CBaseFilter**, you must declare the pins in your derived class.</span></span>

<span data-ttu-id="7107b-125">**Negoziazione di connessioni pin**</span><span class="sxs-lookup"><span data-stu-id="7107b-125">**Negotiating Pin Connections**</span></span>

<span data-ttu-id="7107b-126">Quando il gestore del grafico dei filtri tenta di connettere due filtri, i pin devono concordare su vari aspetti.</span><span class="sxs-lookup"><span data-stu-id="7107b-126">When the Filter Graph Manager tries to connect two filters, the pins must agree on various things.</span></span> <span data-ttu-id="7107b-127">In caso affermativo, il tentativo di connessione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7107b-127">If they cannot, the connection attempt fails.</span></span> <span data-ttu-id="7107b-128">In genere, i pin negoziano quanto segue:</span><span class="sxs-lookup"><span data-stu-id="7107b-128">Generally, pins negotiate the following:</span></span>

-   <span data-ttu-id="7107b-129">Transport.</span><span class="sxs-lookup"><span data-stu-id="7107b-129">Transport.</span></span> <span data-ttu-id="7107b-130">Il trasporto è il meccanismo che i filtri utilizzeranno per spostare gli esempi di supporti dal pin di output al pin di input.</span><span class="sxs-lookup"><span data-stu-id="7107b-130">The transport is the mechanism that the filters will use to move media samples from the output pin to the input pin.</span></span> <span data-ttu-id="7107b-131">Ad esempio, è possibile usare l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ("modello push") o l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) ("modello pull").</span><span class="sxs-lookup"><span data-stu-id="7107b-131">For example, they can use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface ("push model") or the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface ("pull model").</span></span>
-   <span data-ttu-id="7107b-132">Tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="7107b-132">Media type.</span></span> <span data-ttu-id="7107b-133">Quasi tutti i pin utilizzano i tipi di supporto per descrivere il formato dei dati che verranno recapitati.</span><span class="sxs-lookup"><span data-stu-id="7107b-133">Almost all pins use media types to describe the format of the data they will deliver.</span></span>
-   <span data-ttu-id="7107b-134">Allocatore.</span><span class="sxs-lookup"><span data-stu-id="7107b-134">Allocator.</span></span> <span data-ttu-id="7107b-135">L'allocatore è l'oggetto che crea i buffer che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="7107b-135">The allocator is the object that creates the buffers that hold the data.</span></span> <span data-ttu-id="7107b-136">I pin devono accettare quale pin fornirà l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="7107b-136">The pins must agree which pin will provide the allocator.</span></span> <span data-ttu-id="7107b-137">Devono inoltre accettare le dimensioni dei buffer, il numero di buffer da creare e altre proprietà del buffer.</span><span class="sxs-lookup"><span data-stu-id="7107b-137">They must also agree on the size of the buffers, the number of buffers to create, and other buffer properties.</span></span>

<span data-ttu-id="7107b-138">Le classi base implementano un Framework per queste negoziazioni.</span><span class="sxs-lookup"><span data-stu-id="7107b-138">The base classes implement a framework for these negotiations.</span></span> <span data-ttu-id="7107b-139">Per completare i dettagli, è necessario eseguire l'override di diversi metodi della classe di base.</span><span class="sxs-lookup"><span data-stu-id="7107b-139">You must complete the details by overriding various methods in the base class.</span></span> <span data-ttu-id="7107b-140">Il set di metodi di cui è necessario eseguire l'override dipende dalla classe e dalla funzionalità del filtro.</span><span class="sxs-lookup"><span data-stu-id="7107b-140">The set of methods that you must override depends on the class and on the functionality of your filter.</span></span> <span data-ttu-id="7107b-141">Per ulteriori informazioni, vedere [la](how-filters-connect.md)pagina relativa alla modalità di connessione dei filtri.</span><span class="sxs-lookup"><span data-stu-id="7107b-141">For more information, see [How Filters Connect](how-filters-connect.md).</span></span>

<span data-ttu-id="7107b-142">**Elaborazione e distribuzione di dati**</span><span class="sxs-lookup"><span data-stu-id="7107b-142">**Processing and Delivering Data**</span></span>

<span data-ttu-id="7107b-143">La funzione principale della maggior parte dei filtri consiste nell'elaborare e distribuire i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="7107b-143">The primary function of most filters is to process and deliver media data.</span></span> <span data-ttu-id="7107b-144">Il modo in cui si verifica dipende dal tipo di filtro:</span><span class="sxs-lookup"><span data-stu-id="7107b-144">How that occurs depends on the type of filter:</span></span>

-   <span data-ttu-id="7107b-145">Un'origine push dispone di un thread di lavoro che compila continuamente campioni con dati e li recapita a valle.</span><span class="sxs-lookup"><span data-stu-id="7107b-145">A push source has a worker thread that continuously fills samples with data and delivers them downstream.</span></span>
-   <span data-ttu-id="7107b-146">Un'origine pull Attende che l'elemento adiacente downstream richieda un campione.</span><span class="sxs-lookup"><span data-stu-id="7107b-146">A pull source waits for its downstream neighbor to request a sample.</span></span> <span data-ttu-id="7107b-147">Risponde scrivendo i dati in un esempio e recapitando l'esempio al filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="7107b-147">It responds by writing data into a sample and delivering the sample to the downstream filter.</span></span> <span data-ttu-id="7107b-148">Il filtro downstream crea il thread che guida il flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="7107b-148">The downstream filter creates the thread that drives the data flow.</span></span>
-   <span data-ttu-id="7107b-149">A un filtro di trasformazione sono stati recapitati esempi dal rispettivo Neighbor upstream.</span><span class="sxs-lookup"><span data-stu-id="7107b-149">A transform filter has samples delivered to it by its upstream neighbor.</span></span> <span data-ttu-id="7107b-150">Quando riceve un esempio, elabora i dati e li recapita a valle.</span><span class="sxs-lookup"><span data-stu-id="7107b-150">When it receives a sample, it processes the data and delivers it downstream.</span></span>
-   <span data-ttu-id="7107b-151">Un filtro renderer riceve esempi da upstream e li pianifica per il rendering in base agli indicatori temporali.</span><span class="sxs-lookup"><span data-stu-id="7107b-151">A renderer filter receives samples from upstream, and schedules them for rendering based on the time stamps.</span></span>

<span data-ttu-id="7107b-152">Altre attività correlate al flusso includono lo scaricamento dei dati dal grafico, la gestione della fine del flusso e la risposta alle richieste di ricerca.</span><span class="sxs-lookup"><span data-stu-id="7107b-152">Other tasks related to streaming include flushing data from the graph, handling the end of the stream, and responding to seek requests.</span></span> <span data-ttu-id="7107b-153">Per ulteriori informazioni su questi problemi, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7107b-153">For more information about these issues, see the following topics:</span></span>

-   [<span data-ttu-id="7107b-154">Flusso di dati per sviluppatori di filtri</span><span class="sxs-lookup"><span data-stu-id="7107b-154">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="7107b-155">Gestione controllo qualità</span><span class="sxs-lookup"><span data-stu-id="7107b-155">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="7107b-156">Thread e sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="7107b-156">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

<span data-ttu-id="7107b-157">**Supporto di COM**</span><span class="sxs-lookup"><span data-stu-id="7107b-157">**Supporting COM**</span></span>

<span data-ttu-id="7107b-158">I filtri DirectShow sono oggetti COM, in genere inclusi in una dll.</span><span class="sxs-lookup"><span data-stu-id="7107b-158">DirectShow filters are COM objects, typically packaged in DLLs.</span></span> <span data-ttu-id="7107b-159">La libreria di classi di base implementa un Framework per supportare COM.</span><span class="sxs-lookup"><span data-stu-id="7107b-159">The base class library implements a framework for supporting COM.</span></span> <span data-ttu-id="7107b-160">Viene descritta nella sezione [DirectShow e com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="7107b-160">It is described in the section [DirectShow and COM](directshow-and-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7107b-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7107b-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7107b-162">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="7107b-162">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



