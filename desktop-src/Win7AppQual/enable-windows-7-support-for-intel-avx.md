---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Abilita il supporto di Windows 7 per Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318576"
---
# <a name="enable-windows-7-support-for-intel-avx"></a><span data-ttu-id="d28dc-103">Abilita il supporto di Windows 7 per Intel AVX</span><span class="sxs-lookup"><span data-stu-id="d28dc-103">Enable Windows 7 Support for Intel AVX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="d28dc-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="d28dc-104">Affected Platforms</span></span>

 <span data-ttu-id="d28dc-105">**Client** -Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="d28dc-105">**Clients** - Windows 7 SP1</span></span>  
<span data-ttu-id="d28dc-106">**Server** -Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="d28dc-106">**Servers** - Windows Server 2008 R2 SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="d28dc-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="d28dc-107">Feature Impact</span></span>

 <span data-ttu-id="d28dc-108">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="d28dc-108">**Severity** - Low</span></span>  
<span data-ttu-id="d28dc-109">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="d28dc-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="d28dc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d28dc-110">Description</span></span>

<span data-ttu-id="d28dc-111">Intel<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="d28dc-111">Intel<sup>?</sup></span></span> <span data-ttu-id="d28dc-112">Advanced Vector Extensions (AVX)<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="d28dc-112">Advanced Vector Extensions (AVX)<sup>?</sup></span></span> <span data-ttu-id="d28dc-113">è un'estensione di vettore a virgola mobile SIMD a 256 bit di architettura Intel.</span><span class="sxs-lookup"><span data-stu-id="d28dc-113">is a 256-bit SIMD floating-point vector extension of Intel architecture.</span></span> <span data-ttu-id="d28dc-114">Sono incluse le estensioni per i set di istruzioni e di registro.</span><span class="sxs-lookup"><span data-stu-id="d28dc-114">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="d28dc-115">Microsoft ha sviluppato alcuni miglioramenti dell'API, ad esempio le funzioni XState, che consentono alle applicazioni di accedere e modificare le informazioni e lo stato delle funzionalità del processore esteso, incluso AVX.</span><span class="sxs-lookup"><span data-stu-id="d28dc-115">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including AVX.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="d28dc-116">Scenari di utilizzo</span><span class="sxs-lookup"><span data-stu-id="d28dc-116">Usage Scenarios</span></span>

<span data-ttu-id="d28dc-117">Esistono tre livelli generali di impatto potenziale.</span><span class="sxs-lookup"><span data-stu-id="d28dc-117">There are three general levels of potential impact.</span></span>

<span data-ttu-id="d28dc-118">**Livello 1:** Le applicazioni che non usano direttamente Intel AVX non vedranno alcun effetto sulle funzionalità anche se chiamano librerie o usano compilatori che usano o generano indirettamente estensioni Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="d28dc-118">**Level 1:** Applications that do not directly use Intel AVX will not see any impact to their functionality even if they call into libraries or use compilers that indirectly use or generate Intel AVX extensions.</span></span> <span data-ttu-id="d28dc-119">Rappresenta di gran lunga la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d28dc-119">This represents by far the majority of applications.</span></span>

<span data-ttu-id="d28dc-120">**Livello 2:** Le applicazioni avanzate che usano in modo esplicito il set di istruzioni Intel AVX potranno accedere e modificare il contenuto del registro AVX quando viene generata un'eccezione hardware.</span><span class="sxs-lookup"><span data-stu-id="d28dc-120">**Level 2:** Advanced applications that explicitly use the Intel AVX instruction set will be able to access and change AVX register contents when a hardware exception is raised.</span></span> <span data-ttu-id="d28dc-121">Un numero molto ridotto di applicazioni rientra in questa categoria, perché implica una conoscenza approfondita del flusso di istruzioni in esecuzione al momento dell'eccezione, ad esempio le applicazioni con sezioni scritte in linguaggio assembly o quelle che generano codice macchina in fase di esecuzione, ad esempio Runtime di codice gestito con compilazione just-in-time.</span><span class="sxs-lookup"><span data-stu-id="d28dc-121">A very small number of applications would fall into this category, as it implies an intimate knowledge of the instruction stream executing at the time of the exception, such as applications with sections written in assembly language or those that generate machine code at runtime (for example, managed code runtimes with just-in-time compilation).</span></span>

<span data-ttu-id="d28dc-122">**Livello 3:** Le applicazioni del debugger saranno in grado di accedere e modificare lo stato AVX nell'applicazione di cui viene eseguito il debug.</span><span class="sxs-lookup"><span data-stu-id="d28dc-122">**Level 3:** Debugger applications will be able to access and manipulate the AVX state in the application being debugged.</span></span>

## <a name="how-to-leverage-feature-capabilities"></a><span data-ttu-id="d28dc-123">Come sfruttare le funzionalità delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="d28dc-123">How to Leverage Feature Capabilities</span></span>

<span data-ttu-id="d28dc-124">**Livello 1:** Non è necessaria alcuna azione per le applicazioni per l'uso di Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="d28dc-124">**Level 1:** No action is necessary for applications to use Intel AVX.</span></span>

<span data-ttu-id="d28dc-125">**Livello 2:** Le applicazioni in questa categoria hanno la possibilità di accedere e modificare lo stato AVX al momento dell'eccezione dall'interno dei relativi filtri eccezioni.</span><span class="sxs-lookup"><span data-stu-id="d28dc-125">**Level 2:** Applications in this category have the option to access and manipulate AVX state at the time of the exception from within their exception filters.</span></span> <span data-ttu-id="d28dc-126">Dopo aver ottenuto il contesto del processore di base tramite GetExceptionInformation, i filtri devono:</span><span class="sxs-lookup"><span data-stu-id="d28dc-126">After obtaining the base processor context via GetExceptionInformation, filters should:</span></span>

 <span data-ttu-id="d28dc-127">**1.** controllare il valore del flag **\_ XSTATE del contesto** .</span><span class="sxs-lookup"><span data-stu-id="d28dc-127">**1.** Check the value of the **CONTEXT\_XSTATE** flag.</span></span> <span data-ttu-id="d28dc-128">Questo flag indica la presenza di almeno una funzionalità XState nel contesto.</span><span class="sxs-lookup"><span data-stu-id="d28dc-128">This flag indicates the presence of at least one XState feature in the context.</span></span>  
<span data-ttu-id="d28dc-129">**2.** in tal caso, chiamare **GetXStateFeaturesMask** e testare il valore del flag **XSTATE \_ AVX** nella maschera restituita.</span><span class="sxs-lookup"><span data-stu-id="d28dc-129">**2.** If this is the case, call **GetXStateFeaturesMask** and test the value of the **XSTATE\_AVX** flag in the returned mask.</span></span> <span data-ttu-id="d28dc-130">Indica la presenza dello stato AVX nel contesto.</span><span class="sxs-lookup"><span data-stu-id="d28dc-130">This indicates the presence of AVX state in the context.</span></span>  
<span data-ttu-id="d28dc-131">**3.** chiamare **LocateXStateFeature** per recuperare il percorso effettivo in cui è archiviato lo stato AVX.</span><span class="sxs-lookup"><span data-stu-id="d28dc-131">**3.** Call **LocateXStateFeature** to retrieve the actual location where the AVX state is stored.</span></span>  

<span data-ttu-id="d28dc-132">**Livello 3:** Non è necessario aggiornare le applicazioni del debugger esistenti a meno che non si vogliano accedere ai registri Intel AVX:</span><span class="sxs-lookup"><span data-stu-id="d28dc-132">**Level 3:** It is not necessary to update existing debugger applications unless they wish access the Intel AVX registers:</span></span>

<span data-ttu-id="d28dc-133">**1.** per determinare se AVX è abilitato, il debugger deve usare:</span><span class="sxs-lookup"><span data-stu-id="d28dc-133">**1.** To determine if AVX is enabled, the debugger should use:</span></span>

-   <span data-ttu-id="d28dc-134">GetEnabledXStateFeatures per ottenere una maschera delle funzionalità XState abilitate nei processori x86 o x64 per determinare quali funzionalità sono presenti e abilitate nel sistema prima di usare una funzionalità del processore XState o per tentare di modificare i contesti XState</span><span class="sxs-lookup"><span data-stu-id="d28dc-134">GetEnabledXStateFeatures to get a mask of enabled XState features on x86 or x64 processors to determine what features are present and enabled on the system before using an XState processor feature or attempting to manipulate XState contexts</span></span>

  
<span data-ttu-id="d28dc-135">**2.** se AVX è presente e si vuole recuperare e modificare lo stato AVX dall'applicazione di cui è in corso il debug (ad esempio, GetThreadContext e SetThreadContext), il debugger deve usare:</span><span class="sxs-lookup"><span data-stu-id="d28dc-135">**2.** If AVX is present and you wish to retrieve and manipulate the AVX state from the application being debugged (for example, GetThreadContext and SetThreadContext), the debugger should use:</span></span>

-   <span data-ttu-id="d28dc-136">Funzione InitializeContext per inizializzare una struttura di contesto all'interno di un buffer con le dimensioni e l'allineamento necessari</span><span class="sxs-lookup"><span data-stu-id="d28dc-136">InitializeContext Function to Initialize a context structure inside a buffer with the necessary size and alignment</span></span>
-   <span data-ttu-id="d28dc-137">Funzione CopyContext per copiare una struttura del contesto di origine (incluso qualsiasi XState) in una struttura del contesto di destinazione inizializzata</span><span class="sxs-lookup"><span data-stu-id="d28dc-137">CopyContext Function to copy a source context structure (including any XState) onto an initialized destination context structure</span></span>

  
<span data-ttu-id="d28dc-138">**3.** per eseguire il test, impostare e individuare lo stato AVX all'interno di un contesto del processore, il debugger deve usare:</span><span class="sxs-lookup"><span data-stu-id="d28dc-138">**3.** To test, set and locate the AVX state within a processor context, the debugger should use:</span></span>

-   <span data-ttu-id="d28dc-139">LocateXStateFeature per recuperare un puntatore allo stato del processore per una singola funzionalità XState all'interno di una struttura del contesto</span><span class="sxs-lookup"><span data-stu-id="d28dc-139">LocateXStateFeature to retrieve a pointer to the processor state for an individual XState feature within a context structure</span></span>
-   <span data-ttu-id="d28dc-140">GetXStateFeaturesMask per restituire la maschera delle funzionalità di XState impostate all'interno di una struttura del contesto</span><span class="sxs-lookup"><span data-stu-id="d28dc-140">GetXStateFeaturesMask to return the mask of XState features set within a context structure</span></span>
-   <span data-ttu-id="d28dc-141">SetXStateFeaturesMask impostare la maschera delle funzionalità di XState impostate all'interno di una struttura del contesto</span><span class="sxs-lookup"><span data-stu-id="d28dc-141">SetXStateFeaturesMask to set the mask of XState features set within a context structure</span></span>

  


## <a name="links-to-other-resources"></a><span data-ttu-id="d28dc-142">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="d28dc-142">Links to Other Resources</span></span>

-   <span data-ttu-id="d28dc-143">Per informazioni sulle funzioni XState nel Windows SDK, vedere funzioni di [debug](../debug/debugging-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d28dc-143">For information about the XState functions in the Windows SDK, see [Debugging Functions](../debug/debugging-functions.md).</span></span>
-   <span data-ttu-id="d28dc-144">Per una panoramica delle istruzioni e delle funzionalità di Intel AVX, vedere la pagina relativa [a Intel AVX: nuove frontiere nei miglioramenti delle prestazioni e nell'efficienza energetica](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span><span class="sxs-lookup"><span data-stu-id="d28dc-144">For an overview of the instructions and capabilities of the Intel AVX, see [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span></span>

 

 
