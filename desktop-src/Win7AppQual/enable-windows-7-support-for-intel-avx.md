---
description: Abilitare il supporto di Windows 7 per Intel AVX
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Abilitare il supporto di Windows 7 per Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1509bac62634c85aa733b2c1de0c152169ac6cda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088459"
---
# <a name="enable-windows-7-support-for-intel-avx"></a><span data-ttu-id="bd481-103">Abilitare il supporto di Windows 7 per Intel AVX</span><span class="sxs-lookup"><span data-stu-id="bd481-103">Enable Windows 7 Support for Intel AVX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="bd481-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="bd481-104">Affected Platforms</span></span>

 <span data-ttu-id="bd481-105">**Client** - Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="bd481-105">**Clients** - Windows 7 SP1</span></span>  
<span data-ttu-id="bd481-106">**Server** - Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="bd481-106">**Servers** - Windows Server 2008 R2 SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="bd481-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="bd481-107">Feature Impact</span></span>

 <span data-ttu-id="bd481-108">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="bd481-108">**Severity** - Low</span></span>  
<span data-ttu-id="bd481-109">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="bd481-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="bd481-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd481-110">Description</span></span>

<span data-ttu-id="bd481-111">Intel<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="bd481-111">Intel<sup>?</sup></span></span> <span data-ttu-id="bd481-112">Advanced Vector Extensions (AVX)<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="bd481-112">Advanced Vector Extensions (AVX)<sup>?</sup></span></span> <span data-ttu-id="bd481-113">è un'estensione di vettore a virgola mobile SIMD a 256 bit dell'architettura Intel.</span><span class="sxs-lookup"><span data-stu-id="bd481-113">is a 256-bit SIMD floating-point vector extension of Intel architecture.</span></span> <span data-ttu-id="bd481-114">Include estensioni sia per i set di istruzioni che per i set di registri.</span><span class="sxs-lookup"><span data-stu-id="bd481-114">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="bd481-115">Microsoft ha sviluppato alcuni miglioramenti delle API, ad esempio le funzioni XState, che consentono alle applicazioni di accedere e modificare le informazioni e lo stato delle funzionalità estese del processore, incluso AVX.</span><span class="sxs-lookup"><span data-stu-id="bd481-115">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including AVX.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="bd481-116">Scenari di utilizzo</span><span class="sxs-lookup"><span data-stu-id="bd481-116">Usage Scenarios</span></span>

<span data-ttu-id="bd481-117">Esistono tre livelli generali di potenziale impatto.</span><span class="sxs-lookup"><span data-stu-id="bd481-117">There are three general levels of potential impact.</span></span>

<span data-ttu-id="bd481-118">**Livello 1:** Le applicazioni che non usano direttamente Intel AVX non noteranno alcun impatto sulle relative funzionalità, anche se chiamano librerie o usano compilatori che usano o generano indirettamente estensioni Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="bd481-118">**Level 1:** Applications that do not directly use Intel AVX will not see any impact to their functionality even if they call into libraries or use compilers that indirectly use or generate Intel AVX extensions.</span></span> <span data-ttu-id="bd481-119">Rappresenta di gran lunga la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bd481-119">This represents by far the majority of applications.</span></span>

<span data-ttu-id="bd481-120">**Livello 2:** Le applicazioni avanzate che usano in modo esplicito il set di istruzioni Intel AVX potranno accedere e modificare il contenuto del registro AVX quando viene generata un'eccezione hardware.</span><span class="sxs-lookup"><span data-stu-id="bd481-120">**Level 2:** Advanced applications that explicitly use the Intel AVX instruction set will be able to access and change AVX register contents when a hardware exception is raised.</span></span> <span data-ttu-id="bd481-121">Un numero molto ridotto di applicazioni rientra in questa categoria, perché implica una conoscenza approfondita del flusso di istruzioni in esecuzione al momento dell'eccezione, ad esempio le applicazioni con sezioni scritte in linguaggio assembly o quelle che generano codice macchina in fase di esecuzione (ad esempio, runtime di codice gestito con compilazione JIT).</span><span class="sxs-lookup"><span data-stu-id="bd481-121">A very small number of applications would fall into this category, as it implies an intimate knowledge of the instruction stream executing at the time of the exception, such as applications with sections written in assembly language or those that generate machine code at runtime (for example, managed code runtimes with just-in-time compilation).</span></span>

<span data-ttu-id="bd481-122">**Livello 3:** Le applicazioni del debugger saranno in grado di accedere e modificare lo stato AVX nell'applicazione di cui è in corso il debug.</span><span class="sxs-lookup"><span data-stu-id="bd481-122">**Level 3:** Debugger applications will be able to access and manipulate the AVX state in the application being debugged.</span></span>

## <a name="how-to-leverage-feature-capabilities"></a><span data-ttu-id="bd481-123">Come sfruttare le funzionalità delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="bd481-123">How to Leverage Feature Capabilities</span></span>

<span data-ttu-id="bd481-124">**Livello 1:** Non è necessaria alcuna azione per l'uso di Intel AVX da parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bd481-124">**Level 1:** No action is necessary for applications to use Intel AVX.</span></span>

<span data-ttu-id="bd481-125">**Livello 2:** Le applicazioni in questa categoria hanno la possibilità di accedere e modificare lo stato AVX al momento dell'eccezione dall'interno dei filtri eccezioni.</span><span class="sxs-lookup"><span data-stu-id="bd481-125">**Level 2:** Applications in this category have the option to access and manipulate AVX state at the time of the exception from within their exception filters.</span></span> <span data-ttu-id="bd481-126">Dopo aver ottenuto il contesto del processore di base tramite GetExceptionInformation, i filtri devono:</span><span class="sxs-lookup"><span data-stu-id="bd481-126">After obtaining the base processor context via GetExceptionInformation, filters should:</span></span>

 <span data-ttu-id="bd481-127">**1.** Controllare il valore del flag **CONTEXT \_ XSTATE.**</span><span class="sxs-lookup"><span data-stu-id="bd481-127">**1.** Check the value of the **CONTEXT\_XSTATE** flag.</span></span> <span data-ttu-id="bd481-128">Questo flag indica la presenza di almeno una funzionalità XState nel contesto.</span><span class="sxs-lookup"><span data-stu-id="bd481-128">This flag indicates the presence of at least one XState feature in the context.</span></span>  
<span data-ttu-id="bd481-129">**2.** In questo caso, chiamare **GetXStateFeaturesMask** e testare il valore del flag **\_ AVX XSTATE** nella maschera restituita.</span><span class="sxs-lookup"><span data-stu-id="bd481-129">**2.** If this is the case, call **GetXStateFeaturesMask** and test the value of the **XSTATE\_AVX** flag in the returned mask.</span></span> <span data-ttu-id="bd481-130">Indica la presenza dello stato AVX nel contesto.</span><span class="sxs-lookup"><span data-stu-id="bd481-130">This indicates the presence of AVX state in the context.</span></span>  
<span data-ttu-id="bd481-131">**3.** Chiamare **LocateXStateFeature** per recuperare la posizione effettiva in cui è archiviato lo stato AVX.</span><span class="sxs-lookup"><span data-stu-id="bd481-131">**3.** Call **LocateXStateFeature** to retrieve the actual location where the AVX state is stored.</span></span>  

<span data-ttu-id="bd481-132">**Livello 3:** Non è necessario aggiornare le applicazioni debugger esistenti a meno che non vogliano accedere ai registri Intel AVX:</span><span class="sxs-lookup"><span data-stu-id="bd481-132">**Level 3:** It is not necessary to update existing debugger applications unless they wish access the Intel AVX registers:</span></span>

<span data-ttu-id="bd481-133">**1.** Per determinare se AVX è abilitato, il debugger deve usare:</span><span class="sxs-lookup"><span data-stu-id="bd481-133">**1.** To determine if AVX is enabled, the debugger should use:</span></span>

-   <span data-ttu-id="bd481-134">GetEnabledXStateFeatures per ottenere una maschera delle funzionalità XState abilitate nei processori x86 o x64 per determinare quali funzionalità sono presenti e abilitate nel sistema prima di usare una funzionalità del processore XState o tentare di modificare i contesti XState</span><span class="sxs-lookup"><span data-stu-id="bd481-134">GetEnabledXStateFeatures to get a mask of enabled XState features on x86 or x64 processors to determine what features are present and enabled on the system before using an XState processor feature or attempting to manipulate XState contexts</span></span>

  
<span data-ttu-id="bd481-135">**2.** Se AVX è presente e si vuole recuperare e modificare lo stato AVX dall'applicazione in fase di debug ,ad esempio GetThreadContext e SetThreadContext, il debugger deve usare:</span><span class="sxs-lookup"><span data-stu-id="bd481-135">**2.** If AVX is present and you wish to retrieve and manipulate the AVX state from the application being debugged (for example, GetThreadContext and SetThreadContext), the debugger should use:</span></span>

-   <span data-ttu-id="bd481-136">Funzione InitializeContext per inizializzare una struttura di contesto all'interno di un buffer con le dimensioni e l'allineamento necessari</span><span class="sxs-lookup"><span data-stu-id="bd481-136">InitializeContext Function to Initialize a context structure inside a buffer with the necessary size and alignment</span></span>
-   <span data-ttu-id="bd481-137">Funzione CopyContext per copiare una struttura del contesto di origine (incluso qualsiasi XState) in una struttura del contesto di destinazione inizializzata</span><span class="sxs-lookup"><span data-stu-id="bd481-137">CopyContext Function to copy a source context structure (including any XState) onto an initialized destination context structure</span></span>

  
<span data-ttu-id="bd481-138">**3.** Per testare, impostare e individuare lo stato AVX all'interno di un contesto del processore, il debugger deve usare:</span><span class="sxs-lookup"><span data-stu-id="bd481-138">**3.** To test, set and locate the AVX state within a processor context, the debugger should use:</span></span>

-   <span data-ttu-id="bd481-139">LocateXStateFeature per recuperare un puntatore allo stato del processore per una singola funzionalità XState all'interno di una struttura di contesto</span><span class="sxs-lookup"><span data-stu-id="bd481-139">LocateXStateFeature to retrieve a pointer to the processor state for an individual XState feature within a context structure</span></span>
-   <span data-ttu-id="bd481-140">GetXStateFeaturesMask per restituire la maschera delle funzionalità XState impostate all'interno di una struttura di contesto</span><span class="sxs-lookup"><span data-stu-id="bd481-140">GetXStateFeaturesMask to return the mask of XState features set within a context structure</span></span>
-   <span data-ttu-id="bd481-141">SetXStateFeaturesMask per impostare la maschera delle funzionalità XState impostate all'interno di una struttura di contesto</span><span class="sxs-lookup"><span data-stu-id="bd481-141">SetXStateFeaturesMask to set the mask of XState features set within a context structure</span></span>

  


## <a name="links-to-other-resources"></a><span data-ttu-id="bd481-142">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="bd481-142">Links to Other Resources</span></span>

-   <span data-ttu-id="bd481-143">Per informazioni sulle funzioni XState nel Windows SDK, vedere [Funzioni di debug.](../debug/debugging-functions.md)</span><span class="sxs-lookup"><span data-stu-id="bd481-143">For information about the XState functions in the Windows SDK, see [Debugging Functions](../debug/debugging-functions.md).</span></span>
-   <span data-ttu-id="bd481-144">Per una panoramica delle istruzioni e delle funzionalità di Intel AVX, vedere [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span><span class="sxs-lookup"><span data-stu-id="bd481-144">For an overview of the instructions and capabilities of the Intel AVX, see [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span></span>

 

 
