---
title: Linee guida generali per il porting
description: Il porting di applicazioni a 32 bit in Microsoft Windows a 64 bit sarà più semplice del porting di applicazioni a 16 bit in Windows a 32 bit. Tuttavia, lo spostamento andrà più agevolmente con un'attenta pianificazione. Di seguito sono riportate alcune linee guida generali.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- porting di applicazioni a 32 bit alla programmazione Windows a 64 bit di Windows a 64 bit
- Guida alla programmazione di Windows a 64 bit Guida alla programmazione Windows a 64 bit, linee guida per il porting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "104234430"
---
# <a name="general-porting-guidelines"></a><span data-ttu-id="4a19b-107">Linee guida generali per il porting</span><span class="sxs-lookup"><span data-stu-id="4a19b-107">General Porting Guidelines</span></span>

<span data-ttu-id="4a19b-108">Il porting di applicazioni a 32 bit in Microsoft Windows a 64 bit sarà più semplice del porting di applicazioni a 16 bit in Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4a19b-108">Porting 32-bit applications to 64-bit Microsoft Windows will be easier than it was porting 16-bit applications to 32-bit Windows.</span></span> <span data-ttu-id="4a19b-109">Tuttavia, lo spostamento andrà più agevolmente con un'attenta pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4a19b-109">However, the move will go more smoothly with some careful planning.</span></span> <span data-ttu-id="4a19b-110">Di seguito sono riportate alcune linee guida generali.</span><span class="sxs-lookup"><span data-stu-id="4a19b-110">The following are some general guidelines.</span></span>

## <a name="planning"></a><span data-ttu-id="4a19b-111">Pianificazione</span><span class="sxs-lookup"><span data-stu-id="4a19b-111">Planning</span></span>

-   <span data-ttu-id="4a19b-112">Determinare l'entità del lavoro richiesto per la porta.</span><span class="sxs-lookup"><span data-stu-id="4a19b-112">Determine the magnitude of the effort required for the port.</span></span> <span data-ttu-id="4a19b-113">Misurare la quantità di lavoro che è necessario identificando gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4a19b-113">Gauge how much work is involved by identifying the following items:</span></span>
    -   <span data-ttu-id="4a19b-114">Problema codice a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4a19b-114">Problem 32-bit code.</span></span> <span data-ttu-id="4a19b-115">Compilare il codice a 32 bit con il compilatore a 64 bit ed esaminare la portata degli errori e degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="4a19b-115">Compile your 32-bit code with the 64-bit compiler and examine the extent of the errors and warnings.</span></span>
    -   <span data-ttu-id="4a19b-116">Componenti o dipendenze condivise.</span><span class="sxs-lookup"><span data-stu-id="4a19b-116">Shared components or dependencies.</span></span> <span data-ttu-id="4a19b-117">Determinare quali componenti dell'applicazione hanno origine da altri team e se tali team pianificano di sviluppare versioni a 64 bit del codice.</span><span class="sxs-lookup"><span data-stu-id="4a19b-117">Determine which components in your application originate from other teams and whether those teams plan to develop 64-bit versions of their code.</span></span>
    -   <span data-ttu-id="4a19b-118">Codice dell'assembly o legacy.</span><span class="sxs-lookup"><span data-stu-id="4a19b-118">Legacy or assembly code.</span></span> <span data-ttu-id="4a19b-119">le applicazioni basate su Windows a 16 bit non vengono eseguite in Windows a 64 bit ed è necessario riscriverle.</span><span class="sxs-lookup"><span data-stu-id="4a19b-119">16-bit Windows-based applications do not run on 64-bit Windows and must be rewritten.</span></span> <span data-ttu-id="4a19b-120">Sebbene il codice assembly x86 venga eseguito in WOW64, può essere utile riscrivere questo codice per sfruttare la velocità dell'architettura Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="4a19b-120">While x86 assembly code runs in WOW64, you may want to rewrite this code to take advantage of the speed of the Intel Itanium architecture.</span></span>
-   <span data-ttu-id="4a19b-121">Trasferire l'intera applicazione, non solo parti di esso.</span><span class="sxs-lookup"><span data-stu-id="4a19b-121">Port the entire application, not just portions of it.</span></span>

    <span data-ttu-id="4a19b-122">Sebbene sia possibile trasferire parti di un'applicazione o limitare il codice a 2G con/LARGEADDRESSAWARE: NO, questa strategia commercia il guadagno a breve termine per il dolore a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="4a19b-122">Although it is possible to port pieces of an application or to limit code to 2G with /LARGEADDRESSAWARE:NO, this strategy trades short-term gain for long-term pain.</span></span>

    > [!Note]  
    > <span data-ttu-id="4a19b-123">/LARGEADDRESSAWARE: NO viene ignorato per un file binario ARM64.</span><span class="sxs-lookup"><span data-stu-id="4a19b-123">/LARGEADDRESSAWARE:NO is ignored for an ARM64 binary.</span></span>

     

-   <span data-ttu-id="4a19b-124">Trovare sostituzioni per le tecnologie che non verranno trasferite.</span><span class="sxs-lookup"><span data-stu-id="4a19b-124">Find substitutes for technologies that will not be ported.</span></span>

    <span data-ttu-id="4a19b-125">Alcune tecnologie, tra cui DAO (Data Access Object) e il motore di database Jet Red, non verranno trasferite in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4a19b-125">Some technologies, including DAO (Data Access Object) and the Jet Red database engine, will not be ported to 64-bit Windows.</span></span>

-   <span data-ttu-id="4a19b-126">Considerare la versione a 64 bit come versione del prodotto separata.</span><span class="sxs-lookup"><span data-stu-id="4a19b-126">Treat your 64-bit version as a separate product release.</span></span>

    <span data-ttu-id="4a19b-127">Anche se il prodotto a 64 bit può condividere la stessa codebase del 32 bit, è necessario un test aggiuntivo e potrebbe avere altre considerazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="4a19b-127">Even though your 64-bit product may share the same code base as your 32-bit, it needs additional testing and may have other release considerations.</span></span>

## <a name="development"></a><span data-ttu-id="4a19b-128">Sviluppo</span><span class="sxs-lookup"><span data-stu-id="4a19b-128">Development</span></span>

-   <span data-ttu-id="4a19b-129">Inizia subito a sviluppare codice conforme.</span><span class="sxs-lookup"><span data-stu-id="4a19b-129">Start developing compliant code now.</span></span>

    <span data-ttu-id="4a19b-130">Gli sviluppatori possono iniziare a scrivere codice conforme usando i file di intestazione di Windows più recenti e i nuovi tipi di dati senza effetti negativi sullo sviluppo di prodotti a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4a19b-130">Developers can start writing compliant code by using the latest Windows header files and the new data types with no adverse effects on 32-bit product development.</span></span> <span data-ttu-id="4a19b-131">Per altre informazioni, vedere [preparazione per Windows a 64 bit](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="4a19b-131">For more information, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

-   <span data-ttu-id="4a19b-132">Verificare che sia possibile compilare il codice per Windows a 32 e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4a19b-132">Ensure that your code can be compiled for both 32- and 64-bit Windows.</span></span>

    <span data-ttu-id="4a19b-133">Il nuovo modello di dati è stato progettato per consentire la compilazione di applicazioni a 32 e 64 bit da una singola codebase con poche modifiche.</span><span class="sxs-lookup"><span data-stu-id="4a19b-133">The new data model was designed to allow 32- and 64-bit applications to be built from a single code base with few modifications.</span></span> <span data-ttu-id="4a19b-134">I team di sviluppo SQL Server e Windows sviluppano versioni 32 e 64 dei prodotti dalla stessa codebase.</span><span class="sxs-lookup"><span data-stu-id="4a19b-134">The SQL Server and Windows development teams are developing 32- and 64-bit versions of their products from the same code base.</span></span>

-   <span data-ttu-id="4a19b-135">Utilizzare le nuove funzionalità di ottimizzazione del compilatore per ottenere prestazioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="4a19b-135">Use the compiler's new optimization features for best performance.</span></span>

    <span data-ttu-id="4a19b-136">L'ottimizzazione del codice per i processori Intel Itanium è più importante rispetto a quella di x86.</span><span class="sxs-lookup"><span data-stu-id="4a19b-136">Code optimization for Intel Itanium processors is more important than it was for the x86.</span></span> <span data-ttu-id="4a19b-137">Il compilatore presuppone la maggior parte delle funzioni di ottimizzazione precedentemente gestite dal microprocessore.</span><span class="sxs-lookup"><span data-stu-id="4a19b-137">The compiler assumes many of the optimization functions previously handled by the microprocessor.</span></span> <span data-ttu-id="4a19b-138">È possibile ottimizzare le prestazioni di un'applicazione a 64 bit utilizzando due nuove funzionalità di ottimizzazione del compilatore: *ottimizzazione* PGO e *ottimizzazione programma intera*.</span><span class="sxs-lookup"><span data-stu-id="4a19b-138">You can maximize the performance of a 64-bit application by using two new optimization features of the compiler: *Profile Guided Optimization* and *Whole Program Optimization*.</span></span> <span data-ttu-id="4a19b-139">Entrambe le funzionalità generano tempi di compilazione più lunghi e richiedono lo sviluppo iniziale di scenari di test efficaci.</span><span class="sxs-lookup"><span data-stu-id="4a19b-139">Both features result in longer build times and require the early development of good test scenarios.</span></span>

    <span data-ttu-id="4a19b-140">L' *ottimizzazione* PGO prevede un processo di compilazione in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="4a19b-140">*Profile Guided Optimization* involves a two-step compile process.</span></span> <span data-ttu-id="4a19b-141">Durante la prima compilazione, il codice viene instrumentato per acquisire il comportamento di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4a19b-141">During the first compile, the code is instrumented to capture the execution behavior.</span></span> <span data-ttu-id="4a19b-142">Queste informazioni vengono usate durante la seconda compilazione per guidare tutte le funzionalità di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="4a19b-142">This information is used during the second compile to guide all optimization features.</span></span>

    <span data-ttu-id="4a19b-143">L' *ottimizzazione dell'intero programma* analizza il codice in tutti i file dell'applicazione, non solo uno.</span><span class="sxs-lookup"><span data-stu-id="4a19b-143">*Whole Program Optimization* analyzes the code in all application files, not just a single one.</span></span> <span data-ttu-id="4a19b-144">Questo approccio aumenta le prestazioni in diversi modi, tra cui l'incorporamento migliore, nonché l'analisi degli effetti collaterali migliorata e le convenzioni di chiamata personalizzate.</span><span class="sxs-lookup"><span data-stu-id="4a19b-144">This approach increases performance in several ways, including better inlining, as well as improved side-effect analysis and custom calling conventions.</span></span>

## <a name="testing"></a><span data-ttu-id="4a19b-145">Test</span><span class="sxs-lookup"><span data-stu-id="4a19b-145">Testing</span></span>

-   <span data-ttu-id="4a19b-146">Determinare se testare il codice 64 o 32 bit in esecuzione in WOW64.</span><span class="sxs-lookup"><span data-stu-id="4a19b-146">Determine whether you'll test 64- or 32-bit code running in WOW64.</span></span>

    <span data-ttu-id="4a19b-147">Alcune applicazioni includono codice nativo a 64 bit e codice a 32 bit in esecuzione in WOW64.</span><span class="sxs-lookup"><span data-stu-id="4a19b-147">Some applications include both native 64-bit code and 32-bit code running in WOW64.</span></span> <span data-ttu-id="4a19b-148">Esaminare attentamente questo oggetto durante lo sviluppo di un piano di test e decidere se gli strumenti di test devono essere a 64 bit, a 32 bit o a una combinazione.</span><span class="sxs-lookup"><span data-stu-id="4a19b-148">Investigate this closely while developing a test plan, and decide whether your test tools should be 64-bit, 32-bit, or a combination.</span></span> <span data-ttu-id="4a19b-149">Spesso è necessario testare entrambe le versioni a 64 e 32 bit dell'applicazione in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4a19b-149">You will often need to test both the 64- and 32-bit versions of your application on 64-bit Windows.</span></span>

-   <span data-ttu-id="4a19b-150">Testare i componenti di uso frequente a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4a19b-150">Test frequently used 32-bit components.</span></span>

    <span data-ttu-id="4a19b-151">Innanzitutto, ricompilare il codice a 64 bit e testare.</span><span class="sxs-lookup"><span data-stu-id="4a19b-151">First, recompile your code to 64-bit and test.</span></span> <span data-ttu-id="4a19b-152">In secondo luogo, risolvere i problemi, ricompilare in 32 bit e quindi eseguire il test.</span><span class="sxs-lookup"><span data-stu-id="4a19b-152">Second, fix problems, recompile in 32-bits, and then test.</span></span> <span data-ttu-id="4a19b-153">Terzo, ricompilare a 64 bit e testare.</span><span class="sxs-lookup"><span data-stu-id="4a19b-153">Third, recompile to 64-bit and test.</span></span>

-   <span data-ttu-id="4a19b-154">Testare i componenti COM e RPC.</span><span class="sxs-lookup"><span data-stu-id="4a19b-154">Test COM and RPC components.</span></span>

    <span data-ttu-id="4a19b-155">Assicurarsi che i componenti COM e RPC sia a 32 che a 64 bit comunicano correttamente.</span><span class="sxs-lookup"><span data-stu-id="4a19b-155">Make sure that both 32- and 64-bit COM and RPC components communicate correctly.</span></span> <span data-ttu-id="4a19b-156">Potrebbe inoltre essere necessario testare le comunicazioni con componenti a 16 bit in una rete.</span><span class="sxs-lookup"><span data-stu-id="4a19b-156">You may also have to test communications with 16-bit components over a network.</span></span>

-   <span data-ttu-id="4a19b-157">Testare la versione a 32 bit su Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4a19b-157">Test your 32-bit version on 64-bit Windows.</span></span>

    <span data-ttu-id="4a19b-158">I clienti possono continuare a usare applicazioni a 32 bit su Windows a 64 bit in cui i problemi di prestazioni e memoria non sono considerazioni principali.</span><span class="sxs-lookup"><span data-stu-id="4a19b-158">Customers can continue to use 32-bit applications on 64-bit Windows where performance and memory issues are not major considerations.</span></span>

-   <span data-ttu-id="4a19b-159">Testare configurazioni di memoria diverse.</span><span class="sxs-lookup"><span data-stu-id="4a19b-159">Test different memory configurations.</span></span>

    <span data-ttu-id="4a19b-160">L'aggiunta di grandi quantità di memoria nel server talvolta espone problemi precedentemente inosservati nell'applicazione o nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4a19b-160">Adding large amounts of memory on the server sometimes exposes previously unnoticed problems in either the application or the operating system.</span></span>

 

 




