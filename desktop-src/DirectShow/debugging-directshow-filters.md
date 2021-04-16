---
description: Molte delle funzionalità di debug descritte in questo argomento sono implementate nella libreria di classi base DirectShow. Per altre informazioni, vedere classi base di DirectShow.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Debug dei filtri DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522554"
---
# <a name="debugging-directshow-filters"></a><span data-ttu-id="ee47f-104">Debug dei filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="ee47f-104">Debugging DirectShow Filters</span></span>

<span data-ttu-id="ee47f-105">Molte delle funzionalità di debug descritte in questo argomento sono implementate nella libreria di classi base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ee47f-105">Many of the debugging facilities described in this topic are implemented in the DirectShow base class library.</span></span> <span data-ttu-id="ee47f-106">Per altre informazioni, vedere [classi base di DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ee47f-106">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="assertion-checking"></a><span data-ttu-id="ee47f-107">Verifica dell'asserzione</span><span class="sxs-lookup"><span data-stu-id="ee47f-107">Assertion Checking</span></span>

<span data-ttu-id="ee47f-108">Usare il controllo dell'asserzione in tutta liberalità.</span><span class="sxs-lookup"><span data-stu-id="ee47f-108">Use assertion checking liberally.</span></span> <span data-ttu-id="ee47f-109">Le asserzioni possono verificare i presupposti che si apportano nel codice sulle precondizioni e le postcondizioni.</span><span class="sxs-lookup"><span data-stu-id="ee47f-109">Assertions can verify assumptions that you make in your code about preconditions and postconditions.</span></span> <span data-ttu-id="ee47f-110">DirectShow fornisce diverse macro di asserzione.</span><span class="sxs-lookup"><span data-stu-id="ee47f-110">DirectShow provides several assertion macros.</span></span> <span data-ttu-id="ee47f-111">Per altre informazioni, vedere [macro ASSERT e breakpoint](assert-and-breakpoint-macros.md).</span><span class="sxs-lookup"><span data-stu-id="ee47f-111">For more information, see [Assert and Breakpoint Macros](assert-and-breakpoint-macros.md).</span></span>

## <a name="object-names"></a><span data-ttu-id="ee47f-112">Nomi di oggetti</span><span class="sxs-lookup"><span data-stu-id="ee47f-112">Object Names</span></span>

<span data-ttu-id="ee47f-113">Nelle build di debug è presente un elenco globale di oggetti che derivano dalla classe [**CBaseObject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="ee47f-113">In debug builds, there is a global list of objects that derive from the [**CBaseObject**](cbaseobject.md) class.</span></span> <span data-ttu-id="ee47f-114">Man mano che vengono creati, gli oggetti vengono aggiunti all'elenco.</span><span class="sxs-lookup"><span data-stu-id="ee47f-114">As objects are created, they are added to the list.</span></span> <span data-ttu-id="ee47f-115">Quando vengono eliminati definitivamente, vengono rimossi dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="ee47f-115">When they are destroyed, they are removed from the list.</span></span> <span data-ttu-id="ee47f-116">Per visualizzare un elenco di tali oggetti, chiamare la funzione [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) .</span><span class="sxs-lookup"><span data-stu-id="ee47f-116">To display a list of those objects, call the [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function.</span></span>

<span data-ttu-id="ee47f-117">Il metodo del costruttore per la classe base [**CBaseObject**](cbaseobject.md) , e la maggior parte delle classi derivate da esso, include un parametro per il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ee47f-117">The constructor method for the [**CBaseObject**](cbaseobject.md) base class—and most classes derived from it—includes a parameter for the name of the object.</span></span> <span data-ttu-id="ee47f-118">Assegnare agli oggetti nomi univoci per identificarli.</span><span class="sxs-lookup"><span data-stu-id="ee47f-118">Give your objects unique names to identify them.</span></span> <span data-ttu-id="ee47f-119">Usare la macro [**Name**](name.md) quando si dichiara il nome, in modo che il nome venga allocato solo nelle compilazioni di debug.</span><span class="sxs-lookup"><span data-stu-id="ee47f-119">Use the [**NAME**](name.md) macro when you declare the name, so that the name is allocated only in debug builds.</span></span> <span data-ttu-id="ee47f-120">Nelle compilazioni finali il nome diventa **null**.</span><span class="sxs-lookup"><span data-stu-id="ee47f-120">In retail builds, the name becomes **NULL**.</span></span>

## <a name="debug-logging"></a><span data-ttu-id="ee47f-121">Registrazione debug</span><span class="sxs-lookup"><span data-stu-id="ee47f-121">Debug Logging</span></span>

<span data-ttu-id="ee47f-122">La funzione [**DbgLog**](dbglog.md) Visualizza i messaggi di debug durante l'esecuzione del programma.</span><span class="sxs-lookup"><span data-stu-id="ee47f-122">The [**DbgLog**](dbglog.md) function displays debugging messages as your program executes.</span></span> <span data-ttu-id="ee47f-123">Usare questa funzione per tenere traccia dell'esecuzione dell'applicazione o del filtro.</span><span class="sxs-lookup"><span data-stu-id="ee47f-123">Use this function to trace the execution of your application or filter.</span></span> <span data-ttu-id="ee47f-124">È possibile registrare i codici restituiti, i valori delle variabili e altre informazioni rilevanti.</span><span class="sxs-lookup"><span data-stu-id="ee47f-124">You can log return codes, the values of variables, and any other relevant information.</span></span>

<span data-ttu-id="ee47f-125">Ogni messaggio di debug dispone di un tipo, ad esempio log \_ Trace o log \_ Error e un livello di debug, che indica l'importanza del messaggio.</span><span class="sxs-lookup"><span data-stu-id="ee47f-125">Every debug message has a type, such as LOG\_TRACE or LOG\_ERROR, and a debug level, which indicates the importance of the message.</span></span> <span data-ttu-id="ee47f-126">I messaggi con livelli di debug inferiori sono più importanti rispetto a quelli con livelli più elevati.</span><span class="sxs-lookup"><span data-stu-id="ee47f-126">Messages with lower debug levels are more important than those with higher levels.</span></span>

<span data-ttu-id="ee47f-127">Nell'esempio seguente un filtro ipotetico disconnette un pin da una matrice di pin.</span><span class="sxs-lookup"><span data-stu-id="ee47f-127">In the following example, a hypothetical filter disconnects a pin from an array of pins.</span></span> <span data-ttu-id="ee47f-128">Se il tentativo di disconnessione ha esito positivo, il filtro Visualizza un messaggio di traccia del LOG \_ .</span><span class="sxs-lookup"><span data-stu-id="ee47f-128">If the disconnect attempt succeeds, the filter displays a LOG\_TRACE message.</span></span> <span data-ttu-id="ee47f-129">Se il tentativo non riesce, viene visualizzato un \_ messaggio di errore di log:</span><span class="sxs-lookup"><span data-stu-id="ee47f-129">If the attempt fails, it displays a LOG\_ERROR message:</span></span>


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



<span data-ttu-id="ee47f-130">Quando si esegue il debug, è possibile impostare il livello di debug per ogni tipo di messaggio.</span><span class="sxs-lookup"><span data-stu-id="ee47f-130">When you are debugging, you can set the debug level for each message type.</span></span> <span data-ttu-id="ee47f-131">Ogni modulo (DLL o eseguibile) mantiene inoltre i propri livelli di debug.</span><span class="sxs-lookup"><span data-stu-id="ee47f-131">Also, each module (DLL or executable) maintains its own debugging levels.</span></span> <span data-ttu-id="ee47f-132">Se si sta testando un filtro, aumentare i livelli di debug per la DLL che contiene il filtro.</span><span class="sxs-lookup"><span data-stu-id="ee47f-132">If you are testing a filter, raise the debug levels for the DLL that contains the filter.</span></span>

<span data-ttu-id="ee47f-133">Per altre informazioni, vedere [debug di funzioni di output](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ee47f-133">For more information, see [Debug Output Functions](debug-output-functions.md).</span></span>

## <a name="critical-sections"></a><span data-ttu-id="ee47f-134">Sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="ee47f-134">Critical Sections</span></span>

<span data-ttu-id="ee47f-135">Per semplificare la traccia dei deadlock, includere asserzioni che determinano se il codice chiamante possiede una sezione critica specificata.</span><span class="sxs-lookup"><span data-stu-id="ee47f-135">To make deadlocks easier to track, include assertions that determine whether the calling code owns a given critical section.</span></span> <span data-ttu-id="ee47f-136">Le funzioni [**CritCheckIn**](critcheckin.md) e [**CritCheckOut**](critcheckout.md) indicano se il thread chiamante è proprietario di una sezione critica.</span><span class="sxs-lookup"><span data-stu-id="ee47f-136">The [**CritCheckIn**](critcheckin.md) and [**CritCheckOut**](critcheckout.md) functions indicate whether the calling thread owns a critical section.</span></span> <span data-ttu-id="ee47f-137">In genere, queste funzioni vengono chiamate dall'interno di una macro ASSERT.</span><span class="sxs-lookup"><span data-stu-id="ee47f-137">Typically, you would call these functions from inside an assert macro.</span></span>

<span data-ttu-id="ee47f-138">È anche possibile usare la funzione [**DbgLockTrace**](dbglocktrace.md) per tracciare quando le sezioni critiche vengono mantenute o rilasciate.</span><span class="sxs-lookup"><span data-stu-id="ee47f-138">You can also use the [**DbgLockTrace**](dbglocktrace.md) function to trace when critical sections are held or released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee47f-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee47f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee47f-140">Debug in DirectShow</span><span class="sxs-lookup"><span data-stu-id="ee47f-140">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



