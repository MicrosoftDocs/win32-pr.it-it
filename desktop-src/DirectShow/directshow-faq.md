---
description: Domande frequenti su DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: Domande frequenti su DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521794"
---
# <a name="directshow-faq"></a><span data-ttu-id="62cb3-103">Domande frequenti su DirectShow</span><span class="sxs-lookup"><span data-stu-id="62cb3-103">DirectShow FAQ</span></span>

<span data-ttu-id="62cb3-104">Questo articolo risponde a molte domande frequenti su Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="62cb3-104">This article answers many frequently asked questions about Microsoft DirectShow.</span></span>

<span data-ttu-id="62cb3-105">**Quali sistemi operativi sono supportati da DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-105">**What operating systems does DirectShow support?**</span></span>

<span data-ttu-id="62cb3-106">DirectShow è disponibile in tutte le versioni supportate di Windows.</span><span class="sxs-lookup"><span data-stu-id="62cb3-106">DirectShow is available in all supported versions of Windows.</span></span>

<span data-ttu-id="62cb3-107">**Quante conoscenze COM è necessario programmare con DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-107">**How much COM knowledge do I need to program with DirectShow?**</span></span>

<span data-ttu-id="62cb3-108">Per lo sviluppo di applicazioni, è necessario comprendere le nozioni di base per l'utilizzo di oggetti COM: come crearne un'istanza, accedere alle interfacce che espongono e gestire i conteggi dei riferimenti su tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="62cb3-108">For application development, you need to understand the basics of working with COM objects: how to instantiate them, access the interfaces they expose, and manage reference counts on those interfaces.</span></span> <span data-ttu-id="62cb3-109">Per lo sviluppo di filtri sono necessarie altre informazioni COM.</span><span class="sxs-lookup"><span data-stu-id="62cb3-109">Filter development requires more COM knowledge.</span></span>

<span data-ttu-id="62cb3-110">**Quali formati sono supportati da DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-110">**What formats does DirectShow support?**</span></span>

<span data-ttu-id="62cb3-111">Vedere [formati supportati in DirectShow](supported-formats-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="62cb3-111">See [Supported Formats in DirectShow](supported-formats-in-directshow.md).</span></span>

<span data-ttu-id="62cb3-112">**È disponibile un elenco di compatibilità hardware (HCL) DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-112">**Is there a DirectShow Hardware Compatibility List (HCL)?**</span></span>

<span data-ttu-id="62cb3-113">No.</span><span class="sxs-lookup"><span data-stu-id="62cb3-113">No.</span></span> <span data-ttu-id="62cb3-114">DirectShow usa le funzionalità hardware Microsoft DirectDraw e Microsoft DirectSound se sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="62cb3-114">DirectShow uses Microsoft DirectDraw and Microsoft DirectSound hardware capabilities if they are available.</span></span> <span data-ttu-id="62cb3-115">Quando non è disponibile hardware speciale, DirectShow USA GDI per creare video e le  \* API multimediali di Wave per riprodurre l'audio.</span><span class="sxs-lookup"><span data-stu-id="62cb3-115">When no special hardware is available, DirectShow uses GDI to draw video and the **waveOut** \* multimedia APIs to play audio.</span></span>

<span data-ttu-id="62cb3-116">**Quali lingue è possibile utilizzare per scrivere un'applicazione DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-116">**What languages can I use to write a DirectShow application?**</span></span>

<span data-ttu-id="62cb3-117">DirectShow è progettato principalmente per lo sviluppo in C++.</span><span class="sxs-lookup"><span data-stu-id="62cb3-117">DirectShow is designed primarily for C++ development.</span></span> <span data-ttu-id="62cb3-118">Un piccolo set di sottoinsiemi dell'API DirectShow viene esposto tramite Visual Basic 6,0; Questa funzionalità è tuttavia deprecata.</span><span class="sxs-lookup"><span data-stu-id="62cb3-118">A small sub-set of the DirectShow API is exposed through Visual Basic 6.0; however, this feature is deprecated.</span></span>

<span data-ttu-id="62cb3-119">**DirectShow sarà sempre accessibile tramite codice gestito?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-119">**Will DirectShow ever be accessible through managed code?**</span></span>

<span data-ttu-id="62cb3-120">Microsoft non prevede l'implementazione di un'API DirectShow gestita.</span><span class="sxs-lookup"><span data-stu-id="62cb3-120">Microsoft has no current plans to implement a managed DirectShow API.</span></span>

<span data-ttu-id="62cb3-121">**Quale compilatore è necessario per lo sviluppo DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-121">**What compiler do I need for DirectShow development?**</span></span>

<span data-ttu-id="62cb3-122">Qualsiasi compilatore in grado di generare oggetti Component Object Model (COM) dovrebbe funzionare una volta che l'ambiente del compilatore è stato configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="62cb3-122">Any compiler capable of generating Component Object Model (COM) objects should work once the compiler's environment has been configured correctly.</span></span>

<span data-ttu-id="62cb3-123">**In che modo DirectShow è correlato a Microsoft DirectX?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-123">**How does DirectShow relate to Microsoft DirectX?**</span></span>

<span data-ttu-id="62cb3-124">Internamente, DirectShow usa DirectSound e DirectDraw quando l'hardware lo supporta.</span><span class="sxs-lookup"><span data-stu-id="62cb3-124">Internally, DirectShow uses DirectSound and DirectDraw when the hardware supports it.</span></span> <span data-ttu-id="62cb3-125">I filtri per il renderer video e il mixer sovrapposto utilizzano le superfici DirectDraw 3 e DirectDraw 5.</span><span class="sxs-lookup"><span data-stu-id="62cb3-125">The Video Renderer and Overlay Mixer filters use DirectDraw 3 and DirectDraw 5 surfaces.</span></span> <span data-ttu-id="62cb3-126">Il video che combina il renderer 7 (solo Windows XP) usa le superfici di DirectDraw 7.</span><span class="sxs-lookup"><span data-stu-id="62cb3-126">The Video Mixing Renderer 7 (Windows XP only) uses DirectDraw 7 surfaces.</span></span> <span data-ttu-id="62cb3-127">Il renderer di video mixing 9 e il renderer video migliorato usano le API Microsoft Direct3D più recenti.</span><span class="sxs-lookup"><span data-stu-id="62cb3-127">The Video Mixing Renderer 9 and the Enhanced Video Renderer use the latest Microsoft Direct3D APIs.</span></span> <span data-ttu-id="62cb3-128">Non è necessario usare le altre API DirectX per scrivere un'applicazione DirectShow, sebbene sia possibile combinarle.</span><span class="sxs-lookup"><span data-stu-id="62cb3-128">You do not need to use the other DirectX APIs to write a DirectShow application, although it is possible to combine them.</span></span>

<span data-ttu-id="62cb3-129">**In che modo DirectShow è correlato a Microsoft ActiveMovie?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-129">**How does DirectShow relate to Microsoft ActiveMovie?**</span></span>

<span data-ttu-id="62cb3-130">ActiveMovie è il nome originale di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="62cb3-130">ActiveMovie was the original name for DirectShow.</span></span> <span data-ttu-id="62cb3-131">Il termine ActiveMovie non viene più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="62cb3-131">The term ActiveMovie is no longer used.</span></span>

<span data-ttu-id="62cb3-132">**Il codice sorgente per l'utilità GraphEdit è disponibile? È possibile ridistribuire GraphEdit?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-132">**Is the source code to the GraphEdit utility available? Can GraphEdit be redistributed?**</span></span>

<span data-ttu-id="62cb3-133">No, l'origine non è disponibile e Graphedt.exe non è ridistribuibile.</span><span class="sxs-lookup"><span data-stu-id="62cb3-133">No, the source is not available, and Graphedt.exe is not redistributable.</span></span>

<span data-ttu-id="62cb3-134">**DMOs sostituire i filtri DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-134">**Do DMOs replace DirectShow filters?**</span></span>

<span data-ttu-id="62cb3-135">Microsoft DirectX Media Objects (DMOs) può essere usato in un'applicazione DirectShow.</span><span class="sxs-lookup"><span data-stu-id="62cb3-135">Microsoft DirectX Media Objects (DMOs) can be used in a DirectShow application.</span></span> <span data-ttu-id="62cb3-136">Per codificatori, decodificatori ed effetti, è consigliabile scrivere un DMO anziché un filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="62cb3-136">For encoders, decoders, and effects, you are encouraged to write a DMO instead of a DirectShow filter.</span></span> <span data-ttu-id="62cb3-137">Nota: se si vuole usare l'accelerazione video DirectX nel decodificatore, è necessario implementarla come filtro. Per altri scopi, un filtro DirectShow potrebbe essere più appropriato.</span><span class="sxs-lookup"><span data-stu-id="62cb3-137">(Note: If you want to use DirectX Video Acceleration in your decoder, you must implement it as a filter.) For other purposes, a DirectShow filter might be more appropriate.</span></span> <span data-ttu-id="62cb3-138">Per altre informazioni su DMOs, vedere [oggetti multimediali DirectX](directx-media-objects.md).</span><span class="sxs-lookup"><span data-stu-id="62cb3-138">For more information about DMOs, see [DirectX Media Objects](directx-media-objects.md).</span></span>

<span data-ttu-id="62cb3-139">**Sto eseguendo un file di formato AVI con Windows Media Player. Posso ascoltare l'audio, ma sembra che non sia presente alcun video, ma vedo solo il nero. Cosa c'è che non va?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-139">**I'm playing an AVI format file with Windows Media Player. I can hear the audio, but there doesn't seem to be any video-instead, I just see black. What's wrong?**</span></span>

<span data-ttu-id="62cb3-140">Probabilmente il file è stato codificato con un codec non presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="62cb3-140">Probably the file was encoded with a codec that is not present on your system.</span></span> <span data-ttu-id="62cb3-141">Anche se il formato di file AVI è comune, è possibile creare file AVI con diversi formati di compressione (codec).</span><span class="sxs-lookup"><span data-stu-id="62cb3-141">Although the AVI file format is common, AVI files can be created with many different compression formats (codecs).</span></span> <span data-ttu-id="62cb3-142">Se si prova a riprodurre un file AVI che usa un codec non supportato, è possibile udire il componente audio, ma il video verrà visualizzato come schermata nera oppure il contenuto della schermata rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="62cb3-142">If you try to play an AVI file that uses an unsupported codec, you might hear the audio component, but the video will display as a black screen or the screen contents will remain unchanged.</span></span>

> [!Note]  
> <span data-ttu-id="62cb3-143">Windows Media Player spesso tenta di scaricare e installare un codec se non è presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="62cb3-143">Windows Media Player often attempts to download and install a codec if it is not present on your system.</span></span>

 

<span data-ttu-id="62cb3-144">**Ricerca per categorie compilare l'applicazione? Quali librerie e file di intestazione sono necessari?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-144">**How do I build my application? What libraries and header files do I need?**</span></span>

<span data-ttu-id="62cb3-145">Vedere [configurazione dell'ambiente di compilazione](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="62cb3-145">See [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="62cb3-146">**GraphEdit Visualizza numerosi filtri che non sono documentati. Quali sono i filtri?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-146">**GraphEdit displays a lot of filters that aren't documented. What are these filters?**</span></span>

<span data-ttu-id="62cb3-147">GraphEdit enumera tutti i filtri registrati nel sistema in una categoria di filtro.</span><span class="sxs-lookup"><span data-stu-id="62cb3-147">GraphEdit enumerates all of the filters that are registered on your system in a filter category.</span></span> <span data-ttu-id="62cb3-148">Potrebbero essere inclusi i filtri installati da applicazioni di terze parti o installati da altre tecnologie Microsoft, ad esempio Windows Media o NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="62cb3-148">This might include filters installed by third-party applications, or installed by other Microsoft technologies, such as Windows Media or NetMeeting.</span></span> <span data-ttu-id="62cb3-149">Inoltre, alcuni filtri DirectShow fungono da wrapper per codec o dispositivi hardware, con ogni codec o dispositivo visualizzato come filtro distinto.</span><span class="sxs-lookup"><span data-stu-id="62cb3-149">Also, some DirectShow filters act as wrappers for codecs or hardware devices, with each codec or device appearing as a distinct filter.</span></span> <span data-ttu-id="62cb3-150">Il codec video Microsoft H. 263 viene usato da NetMeeting e non è più supportato in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="62cb3-150">The Microsoft H.263 Video Codec is used by NetMeeting and is no longer supported in DirectShow.</span></span> <span data-ttu-id="62cb3-151">Per altre informazioni, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="62cb3-151">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="62cb3-152">**Si sono verificati problemi durante la creazione del grafico personalizzato a livello di codice.**</span><span class="sxs-lookup"><span data-stu-id="62cb3-152">**I'm having trouble building my custom graph programmatically.**</span></span>

<span data-ttu-id="62cb3-153">Per prima cosa, provare a creare il grafico di filtro con GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="62cb3-153">First try building the filter graph with GraphEdit.</span></span> <span data-ttu-id="62cb3-154">Questo strumento consente di simulare rapidamente numerose possibilità.</span><span class="sxs-lookup"><span data-stu-id="62cb3-154">This tool enables you to simulate lots of possibilities quickly.</span></span> <span data-ttu-id="62cb3-155">GraphEdit è sempre un ottimo punto di partenza per testare il grafo prima di provare a compilarlo con il codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="62cb3-155">GraphEdit is always a great place to test out the graph before attempting to build it with source code.</span></span>

<span data-ttu-id="62cb3-156">Per ulteriori informazioni sulla creazione di grafici, vedere gli articoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="62cb3-156">For more information about graph building, see the following articles:</span></span>

-   [<span data-ttu-id="62cb3-157">Creazione del grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="62cb3-157">Building the Filter Graph</span></span>](building-the-filter-graph.md)
-   [<span data-ttu-id="62cb3-158">Enumerazione di oggetti in un grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="62cb3-158">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)

<span data-ttu-id="62cb3-159">**Come è possibile rilevare se DirectShow è installato in un computer specifico?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-159">**How can I detect whether DirectShow is installed on a given machine?**</span></span>

<span data-ttu-id="62cb3-160">Chiamare **CoCreateInstance** per creare un'istanza del gestore del grafo dei filtri.</span><span class="sxs-lookup"><span data-stu-id="62cb3-160">Call **CoCreateInstance** to create an instance of the Filter Graph Manager.</span></span> <span data-ttu-id="62cb3-161">Se la chiamata ha esito positivo, DirectShow viene installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="62cb3-161">If this call succeeds, DirectShow is installed on the machine.</span></span> <span data-ttu-id="62cb3-162">Nel codice seguente viene illustrato come eseguire questa operazione:</span><span class="sxs-lookup"><span data-stu-id="62cb3-162">The following code shows how to do this:</span></span>


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



<span data-ttu-id="62cb3-163">**Ricerca per categorie modificare le impostazioni di un filtro senza visualizzare la pagina delle proprietà?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-163">**How do I change a filter's settings without displaying the property page?**</span></span>

<span data-ttu-id="62cb3-164">La maggior parte dei filtri espone una o più interfacce per l'impostazione delle proprietà nel filtro.</span><span class="sxs-lookup"><span data-stu-id="62cb3-164">Most filters expose one or more interfaces for setting properties on the filter.</span></span> <span data-ttu-id="62cb3-165">Per il filtro in questione, vedere la pagina di riferimento.</span><span class="sxs-lookup"><span data-stu-id="62cb3-165">Consult the reference page for the filter in question.</span></span> <span data-ttu-id="62cb3-166">(Vedere [filtri DirectShow](directshow-filters.md)).</span><span class="sxs-lookup"><span data-stu-id="62cb3-166">(See [DirectShow Filters](directshow-filters.md).)</span></span>

<span data-ttu-id="62cb3-167">**È possibile testare il filtro con GraphEdit?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-167">**Can I test my filter with GraphEdit?**</span></span>

<span data-ttu-id="62cb3-168">Durante lo sviluppo di un filtro, GraphEdit può essere utile per visualizzare le connessioni tra i filtri.</span><span class="sxs-lookup"><span data-stu-id="62cb3-168">While you are developing a filter, GraphEdit can help you to visualize the connections between filters.</span></span> <span data-ttu-id="62cb3-169">Può inoltre fornire un rapido test della funzionalità di un filtro.</span><span class="sxs-lookup"><span data-stu-id="62cb3-169">It can also provide a quick test of a filter's functionality.</span></span> <span data-ttu-id="62cb3-170">Tuttavia, non è concepita come una piattaforma di test affidabile.</span><span class="sxs-lookup"><span data-stu-id="62cb3-170">However, it is not meant as a robust test platform.</span></span>

<span data-ttu-id="62cb3-171">**Con quale anello dei privilegi vengono eseguiti i filtri?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-171">**At what privilege ring do filters run?**</span></span>

<span data-ttu-id="62cb3-172">I filtri vengono eseguiti in corrispondenza del Ring 3, sebbene alcuni filtri controllino i dispositivi di streaming eseguiti in corrispondenza dell'anello 0.</span><span class="sxs-lookup"><span data-stu-id="62cb3-172">Filters run at ring 3, although some filters control streaming devices that run at ring 0.</span></span> <span data-ttu-id="62cb3-173">Per ulteriori informazioni, vedere [come i dispositivi hardware partecipano al grafico dei filtri](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="62cb3-173">For more information, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>

<span data-ttu-id="62cb3-174">**È necessario usare un debugger del kernel?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-174">**Do I need to use a kernel debugger?**</span></span>

<span data-ttu-id="62cb3-175">Dipende dal progetto specifico.</span><span class="sxs-lookup"><span data-stu-id="62cb3-175">That depends on your specific project.</span></span> <span data-ttu-id="62cb3-176">L'installazione delle librerie di runtime di debug DirectX significa che si stanno installando driver di debug e altri componenti in modalità kernel e che se l'applicazione causa un'asserzione di debug in uno di questi componenti, il computer verrà riavviato automaticamente a meno che non si disponga di un debugger del kernel collegato al processo.</span><span class="sxs-lookup"><span data-stu-id="62cb3-176">Installing the DirectX debug runtime libraries means that you are installing debug drivers and other kernel mode components, and that if your application causes a debug assert in one of these components, your machine will automatically reboot unless you have a kernel debugger attached to your process.</span></span>

<span data-ttu-id="62cb3-177">**Quando eseguo l'applicazione nel debugger, si arresta in modo anomalo.**</span><span class="sxs-lookup"><span data-stu-id="62cb3-177">**When I run my application in the debugger, it crashes.**</span></span>

<span data-ttu-id="62cb3-178">Alcuni decodificatori sono progettati in modo da non funzionare mentre l'applicazione è collegata al debugger.</span><span class="sxs-lookup"><span data-stu-id="62cb3-178">Some decoders are designed not to work while the application is attached to the debugger.</span></span> <span data-ttu-id="62cb3-179">Provare a eseguire l'applicazione all'esterno del debugger.</span><span class="sxs-lookup"><span data-stu-id="62cb3-179">Try running the application outside the debugger.</span></span>

<span data-ttu-id="62cb3-180">**Come \_ funziona la macro GUID define?**</span><span class="sxs-lookup"><span data-stu-id="62cb3-180">**How does the DEFINE\_GUID macro work?**</span></span>

<span data-ttu-id="62cb3-181">La macro **define \_ GUID** risolve il problema della dichiarazione dei `extern` riferimenti ai valori GUID nel codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="62cb3-181">The **DEFINE\_GUID** macro solves the problem of declaring `extern` references to GUID values in your source code.</span></span> <span data-ttu-id="62cb3-182">Si supponga, ad esempio, che il progetto contenga tre file di origine, src1. cpp, src2. cpp e Src3. cpp, e che tutti e tre i file usino un determinato valore GUID definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="62cb3-182">For example, suppose that your project has three source files, Src1.cpp, Src2.cpp, and Src3.cpp, and all three files use a certain GUID value that you have defined.</span></span> <span data-ttu-id="62cb3-183">Il valore GUID deve essere definito esattamente una volta nel progetto e gli altri file di origine devono dichiarare i relativi `extern` riferimenti.</span><span class="sxs-lookup"><span data-stu-id="62cb3-183">The GUID value must be defined exactly once in your project, and the other source files must declare `extern` references to it.</span></span> <span data-ttu-id="62cb3-184">Con la macro **Definisci \_ GUID** , è possibile usare lo stesso file di intestazione per entrambi gli scopi.</span><span class="sxs-lookup"><span data-stu-id="62cb3-184">With the **DEFINE\_GUID** macro, you can use the same header file for both purposes.</span></span> <span data-ttu-id="62cb3-185">Nel file di intestazione dichiarare il GUID come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="62cb3-185">In your header file, declare the GUID as follows:</span></span>


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



<span data-ttu-id="62cb3-186">(In questo esempio sono presenti zeri, inserire i valori GUID effettivi). È possibile utilizzare l'utilità Guidgen.exe per creare un nuovo GUID e incollarlo nel file di intestazione nel formato **di \_ GUID Definisci** .</span><span class="sxs-lookup"><span data-stu-id="62cb3-186">(Where this example has zeroes, put the actual GUID values.) You can use the Guidgen.exe utility to create a new GUID and paste it into the header file in the **DEFINE\_GUID** format.</span></span> <span data-ttu-id="62cb3-187">Includere il file di intestazione in ogni file di origine che fa riferimento al GUID.</span><span class="sxs-lookup"><span data-stu-id="62cb3-187">Include this header file in every source file that references the GUID.</span></span> <span data-ttu-id="62cb3-188">In esattamente uno dei file di origine includere il file di intestazione INITGUID. h prima del file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="62cb3-188">In exactly one of the source files, include the header file Initguid.h before your header file.</span></span> <span data-ttu-id="62cb3-189">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="62cb3-189">For example:</span></span>


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



<span data-ttu-id="62cb3-190">Ogni volta che il file di intestazione INITGUID. h non è incluso, la macro di **Definisci \_ GUID** crea un `extern` riferimento al valore GUID.</span><span class="sxs-lookup"><span data-stu-id="62cb3-190">Wherever the Initguid.h header file is not included, the **DEFINE\_GUID** macro creates an `extern` reference to the GUID value.</span></span> <span data-ttu-id="62cb3-191">Quando viene incluso il file di intestazione INITGUID. h, la macro **define \_ GUID** viene ridefinita in modo che **define \_ GUID** crei una dichiarazione di definizione del GUID.</span><span class="sxs-lookup"><span data-stu-id="62cb3-191">When the Initguid.h header file is included, it redefines the **DEFINE\_GUID** macro so that **DEFINE\_GUID** creates a defining declaration of the GUID.</span></span>

<span data-ttu-id="62cb3-192">Se non si include Initguid. h in uno dei file di origine, verrà ricevuto un errore di collegamento "simbolo esterno non risolto".</span><span class="sxs-lookup"><span data-stu-id="62cb3-192">If you do not include Initguid.h in any of the source files, you will get a link error "unresolved external symbol."</span></span> <span data-ttu-id="62cb3-193">Se si include Initguid. h due volte per lo stesso GUID, viene ricevuto un errore di compilazione "ridefinizione; inizializzazione multipla ".</span><span class="sxs-lookup"><span data-stu-id="62cb3-193">If you include Initguid.h twice for the same GUID, you will get a compile error "redefinition; multiple initialization."</span></span> <span data-ttu-id="62cb3-194">Per risolvere questi errori, assicurarsi che Initguid. h sia incluso una sola volta.</span><span class="sxs-lookup"><span data-stu-id="62cb3-194">To resolve these errors, make sure that Initguid.h is included exactly once.</span></span> <span data-ttu-id="62cb3-195">Inoltre, non includere Initguid. h all'interno di un file di intestazione precompilato, perché in effetti l'intestazione precompilata è inclusa in ogni file di origine.</span><span class="sxs-lookup"><span data-stu-id="62cb3-195">Also, do not include Initguid.h inside a precompiled header file, because in effect the precompiled header is included in every source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62cb3-196">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62cb3-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62cb3-197">Introduzione a DirectShow</span><span class="sxs-lookup"><span data-stu-id="62cb3-197">Introduction to DirectShow</span></span>](introduction-to-directshow.md)
</dt> </dl>

 

 



