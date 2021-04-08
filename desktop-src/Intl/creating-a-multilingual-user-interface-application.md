---
description: Questa esercitazione illustra come eseguire un'applicazione monolingua e prepararla per l'internazionalizzazione. Questa applicazione è costituita da una soluzione completa compilata in Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Aggiunta del supporto dell'interfaccia utente multilingue a un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884589"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a><span data-ttu-id="3a367-104">Aggiunta del supporto dell'interfaccia utente multilingue a un'applicazione</span><span class="sxs-lookup"><span data-stu-id="3a367-104">Adding Multilingual User Interface Support to an Application</span></span>

<span data-ttu-id="3a367-105">Questa esercitazione illustra come eseguire un'applicazione monolingua e prepararla per l'internazionalizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-105">This tutorial demonstrates how to take a monolingual application and make it world-ready.</span></span> <span data-ttu-id="3a367-106">Questa applicazione è costituita da una soluzione completa compilata in Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3a367-106">This application is in the form of a complete solution that is built within Microsoft Visual Studio.</span></span>

-   [<span data-ttu-id="3a367-107">Overview</span><span class="sxs-lookup"><span data-stu-id="3a367-107">Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="3a367-108">L'idea alla base di Hello MUI</span><span class="sxs-lookup"><span data-stu-id="3a367-108">The Idea Behind Hello MUI</span></span>](#the-idea-behind-hello-mui)
-   [<span data-ttu-id="3a367-109">Configurazione della soluzione Hello MUI</span><span class="sxs-lookup"><span data-stu-id="3a367-109">Setting up the Hello MUI Solution</span></span>](#setting-up-the-hello-mui-solution)
    -   [<span data-ttu-id="3a367-110">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="3a367-110">Platform Requirements</span></span>](#platform-requirements)
    -   [<span data-ttu-id="3a367-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="3a367-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="3a367-112">Passaggio 0: creazione di Hello MUI hardcoded</span><span class="sxs-lookup"><span data-stu-id="3a367-112">Step 0: Creating the Hard-coded Hello MUI</span></span>](#step-0-creating-the-hard-coded-hello-mui)
-   [<span data-ttu-id="3a367-113">Passaggio 1: implementazione del modulo Resource di base</span><span class="sxs-lookup"><span data-stu-id="3a367-113">Step 1: Implementing the Basic Resource Module</span></span>](#step-1-implementing-the-basic-resource-module)
-   [<span data-ttu-id="3a367-114">Passaggio 2: compilazione del modulo Resource di base</span><span class="sxs-lookup"><span data-stu-id="3a367-114">Step 2: Building the Basic Resource Module</span></span>](#step-2-building-the-basic-resource-module)
    -   [<span data-ttu-id="3a367-115">Suddivisione dei diversi moduli di risorse della lingua: Panoramica</span><span class="sxs-lookup"><span data-stu-id="3a367-115">Splitting the Various Language Resource Modules: An Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="3a367-116">Suddivisione dei diversi moduli di risorse della lingua: creazione dei file</span><span class="sxs-lookup"><span data-stu-id="3a367-116">Splitting the Various Language Resource Modules: Creating the Files</span></span>](#splitting-the-various-language-resource-modules-creating-the-files)
-   [<span data-ttu-id="3a367-117">Passaggio 3: creazione di un Resource-Savvy "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3a367-117">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>](#step-3-creating-a-resource-savvy-hello-mui)
-   [<span data-ttu-id="3a367-118">Passaggio 4: globalizzazione di "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3a367-118">Step 4: Globalizing "Hello MUI"</span></span>](#step-4-globalizing-hello-mui)
-   [<span data-ttu-id="3a367-119">Passaggio 5: personalizzazione di "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3a367-119">Step 5: Customizing "Hello MUI"</span></span>](#step-5-customizing-hello-mui)
-   [<span data-ttu-id="3a367-120">Considerazioni aggiuntive per MUI</span><span class="sxs-lookup"><span data-stu-id="3a367-120">Additional Considerations for MUI</span></span>](#additional-considerations-for-mui)
    -   [<span data-ttu-id="3a367-121">Supporto per le applicazioni console</span><span class="sxs-lookup"><span data-stu-id="3a367-121">Support for Console Applications</span></span>](#support-for-console-applications)
    -   [<span data-ttu-id="3a367-122">Determinazione delle lingue da supportare in fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="3a367-122">Determination of Languages to Support at Run-Time</span></span>](#determination-of-languages-to-support-at-run-time)
    -   [<span data-ttu-id="3a367-123">Supporto per script complessi nelle versioni precedenti a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a367-123">Complex Script Support in Versions Prior to Windows Vista</span></span>](#complex-script-support-in-versions-prior-to-windows-vista)
-   [<span data-ttu-id="3a367-124">Summary</span><span class="sxs-lookup"><span data-stu-id="3a367-124">Summary</span></span>](#summary)

## <a name="overview"></a><span data-ttu-id="3a367-125">Panoramica</span><span class="sxs-lookup"><span data-stu-id="3a367-125">Overview</span></span>

<span data-ttu-id="3a367-126">A partire da Windows Vista, il sistema operativo Windows è stato creato da zero per essere una piattaforma multilingue, con supporto aggiuntivo che consente di creare applicazioni multilingue che usano il modello di risorse MUI di Windows.</span><span class="sxs-lookup"><span data-stu-id="3a367-126">Beginning with Windows Vista, the Windows operating system itself was built from the ground up to be a multilingual platform, with additional support that enables you to create multilingual applications that use the Windows MUI resource model.</span></span>

<span data-ttu-id="3a367-127">In questa esercitazione viene illustrato questo nuovo supporto per le applicazioni multilingue, coprendo gli aspetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a367-127">This tutorial illustrates this new support for multilingual applications by covering the following aspects:</span></span>

-   <span data-ttu-id="3a367-128">Usa il migliorato supporto della piattaforma MUI per abilitare facilmente le applicazioni multilingue.</span><span class="sxs-lookup"><span data-stu-id="3a367-128">Uses the improved MUI platform support to easily enable multilingual applications.</span></span>
-   <span data-ttu-id="3a367-129">Estende le applicazioni multilingue da eseguire nelle versioni di Windows precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3a367-129">Extends multilingual applications to run on versions of Windows prior to Windows Vista.</span></span>
-   <span data-ttu-id="3a367-130">Vengono riportate le considerazioni aggiuntive relative allo sviluppo di applicazioni multilingue specializzate, ad esempio applicazioni console.</span><span class="sxs-lookup"><span data-stu-id="3a367-130">Touches on the additional considerations involved in developing specialized multilingual applications such as console applications.</span></span>

<span data-ttu-id="3a367-131">Questi collegamenti forniscono un breve aggiornamento sui concetti di internazionalizzazione e MUI:</span><span class="sxs-lookup"><span data-stu-id="3a367-131">These links help provide a quick refresher on the concepts on internationalization and MUI:</span></span>

-   <span data-ttu-id="3a367-132">[Panoramica rapida dell'internazionalizzazione](understanding-internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="3a367-132">[Quick overview of internationalization](understanding-internationalization.md).</span></span>
-   <span data-ttu-id="3a367-133">[Concetti di MUI](understanding-mui.md).</span><span class="sxs-lookup"><span data-stu-id="3a367-133">[MUI Concepts](understanding-mui.md).</span></span>
-   <span data-ttu-id="3a367-134">[Uso di MUI per lo sviluppo di applicazioni Win32](using-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3a367-134">[Using MUI to develop Win32 applications](using-multilingual-user-interface.md).</span></span>

### <a name="the-idea-behind-hello-mui"></a><span data-ttu-id="3a367-135">L'idea alla base di Hello MUI</span><span class="sxs-lookup"><span data-stu-id="3a367-135">The Idea Behind Hello MUI</span></span>

<span data-ttu-id="3a367-136">Probabilmente si ha familiarità con l'applicazione Hello World classica, che illustra i concetti di programmazione di base.</span><span class="sxs-lookup"><span data-stu-id="3a367-136">You are probably familiar with the classic Hello World application, which illustrates basic programming concepts.</span></span> <span data-ttu-id="3a367-137">Questa esercitazione usa un approccio simile per illustrare come usare il modello di risorse MUI per aggiornare un'applicazione monolingua per creare una versione multilingue denominata Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="3a367-137">This tutorial takes a similar approach to illustrate how to use the MUI resource model to update a monolingual application to create a multilingual version called Hello MUI.</span></span>

> [!Note]  
> <span data-ttu-id="3a367-138">Le attività di questa esercitazione sono descritte in passaggi dettagliati a causa della precisione con cui devono essere eseguite queste attività e della necessità di spiegare i dettagli agli sviluppatori che hanno poca esperienza con queste attività.</span><span class="sxs-lookup"><span data-stu-id="3a367-138">The tasks in this tutorial are described in detailed steps because of the precision with which these activities must be performed, and the need to explain the details to developers who have little experience with these tasks.</span></span>

 

## <a name="setting-up-the-hello-mui-solution"></a><span data-ttu-id="3a367-139">Configurazione della soluzione Hello MUI</span><span class="sxs-lookup"><span data-stu-id="3a367-139">Setting up the Hello MUI Solution</span></span>

<span data-ttu-id="3a367-140">Questi passaggi illustrano come preparare la creazione della soluzione Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="3a367-140">These steps outline how to prepare to create the Hello MUI solution.</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="3a367-141">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="3a367-141">Platform Requirements</span></span>

<span data-ttu-id="3a367-142">È necessario compilare gli esempi di codice in questa esercitazione utilizzando Windows Software Development Kit (SDK) per Windows 7 e Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="3a367-142">You must compile the code samples in this tutorial using the Windows Software Development Kit (SDK) for Windows 7 and Visual Studio 2008.</span></span> <span data-ttu-id="3a367-143">Windows 7 SDK verrà installato in Windows XP, Windows Vista e Windows 7 e la soluzione di esempio può essere compilata in una qualsiasi di queste versioni del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3a367-143">The Windows 7 SDK will install on Windows XP, Windows Vista and Windows 7, and the sample solution can be built on any of these operating system versions.</span></span>

<span data-ttu-id="3a367-144">Tutti gli esempi di codice in questa esercitazione sono progettati per essere eseguiti in versioni x86 e x64 di Windows XP, Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3a367-144">All code samples in this tutorial are designed to be executed on x86 and x64 versions of Windows XP, Windows Vista and Windows 7.</span></span> <span data-ttu-id="3a367-145">Le parti specifiche che non funzioneranno in Windows XP sono denominate laddove appropriato.</span><span class="sxs-lookup"><span data-stu-id="3a367-145">Specific parts that will not work on Windows XP are called out where appropriate.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3a367-146">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="3a367-146">Prerequisites</span></span>

1.  <span data-ttu-id="3a367-147">Installare Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="3a367-147">Install Visual Studio 2008.</span></span>

    <span data-ttu-id="3a367-148">Per ulteriori informazioni, vedere il [centro per sviluppatori di Visual Studio](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a367-148">For more information, see the [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

2.  <span data-ttu-id="3a367-149">Installare la Windows SDK per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3a367-149">Install the Windows SDK for Windows 7.</span></span>

    <span data-ttu-id="3a367-150">È possibile installarlo dalla pagina Windows SDK del centro per [sviluppatori Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a367-150">You can install it from the Windows SDK page of the [Windows Developer Center](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="3a367-151">L'SDK include utilità per lo sviluppo di applicazioni per le versioni del sistema operativo a partire da Windows XP attraverso le versioni più recenti.</span><span class="sxs-lookup"><span data-stu-id="3a367-151">The SDK includes utilities to develop applications for OS versions starting from Windows XP through the most recent.</span></span>

    > [!Note]  
    > <span data-ttu-id="3a367-152">Se il pacchetto non viene installato nel percorso predefinito o se non si sta eseguendo l'installazione nell'unità di sistema, che in genere è l'unità C, prendere nota del percorso di installazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-152">If you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>

     

3.  <span data-ttu-id="3a367-153">Configurare i parametri della riga di comando di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3a367-153">Configure the Visual Studio command line parameters.</span></span>

    1.  <span data-ttu-id="3a367-154">Aprire una finestra di comando di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3a367-154">Open a Visual Studio command window.</span></span>
    2.  <span data-ttu-id="3a367-155">Digitare **percorso set**.</span><span class="sxs-lookup"><span data-stu-id="3a367-155">Type **set path**.</span></span>
    3.  <span data-ttu-id="3a367-156">Verificare che la variabile Path includa il percorso della cartella bin di Windows 7 SDK:... Microsoft SDK \\ Windows \\ v 7.0 \\ bin</span><span class="sxs-lookup"><span data-stu-id="3a367-156">Confirm that the path variable includes the path of the bin folder of the Windows 7 SDK: ...Microsoft SDKs\\Windows\\v7.0\\bin</span></span>

4.  <span data-ttu-id="3a367-157">Installare il pacchetto aggiuntivo per le API NLS di livello inferiore Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a367-157">Install the Microsoft NLS downlevel APIs add-on package.</span></span>
    > [!Note]  
    > <span data-ttu-id="3a367-158">Nel contesto di questa esercitazione, questo pacchetto è necessario solo se si intende personalizzare l'applicazione per l'esecuzione in versioni di Windows precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3a367-158">In the context of this tutorial, this package is necessary only if you will be customizing the application to run on Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="3a367-159">Vedere [passaggio 5: personalizzazione di Hello MUI](#step-5-customizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="3a367-159">See [Step 5: Customizing Hello MUI](#step-5-customizing-hello-mui).</span></span>

     

    1.  <span data-ttu-id="3a367-160">Scaricare e installare il pacchetto dal relativo [sito di download](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="3a367-160">Download and install the package from its [download site](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span></span>
    2.  <span data-ttu-id="3a367-161">Come per il Windows SDK, se il pacchetto non viene installato nel percorso predefinito o se non si esegue l'installazione nell'unità di sistema, che è in genere l'unità C, prendere nota del percorso di installazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-161">As with the Windows SDK, if you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>
    3.  <span data-ttu-id="3a367-162">Se la piattaforma di sviluppo è Windows XP o Windows Server 2003, verificare che Nlsdl.dll sia installato e registrato correttamente.</span><span class="sxs-lookup"><span data-stu-id="3a367-162">If your development platform is Windows XP or Windows Server 2003, confirm that Nlsdl.dll is installed and registered correctly.</span></span>

        1.  <span data-ttu-id="3a367-163">Passare alla cartella "Redist" sotto il percorso di installazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-163">Browse to the "redist" folder under the install path location.</span></span>
        2.  <span data-ttu-id="3a367-164">Eseguire il nlsdl ridistribuibile \* appropriato. exe, ad esempio nlsdl.x86.exe.</span><span class="sxs-lookup"><span data-stu-id="3a367-164">Run the appropriate redistributable Nlsdl.\*.exe, such as nlsdl.x86.exe.</span></span> <span data-ttu-id="3a367-165">Questo passaggio consente di installare e registrare Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="3a367-165">This step installs and registers Nlsdl.dll.</span></span>

    > [!Note]  
    > <span data-ttu-id="3a367-166">Se si sviluppa un'applicazione che utilizza MUI e che deve essere eseguita nelle versioni di Windows precedenti a Windows Vista, è necessario che Nlsdl.dll sia presente nella piattaforma Windows di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-166">If you develop an application that uses MUI and that must run on Windows versions prior to Windows Vista, Nlsdl.dll must be present on the destination Windows platform.</span></span> <span data-ttu-id="3a367-167">Nella maggior parte dei casi, ciò significa che l'applicazione deve portare e installare il programma di installazione di nlsdl ridistribuibile (e non solo copiare Nlsdl.dll).</span><span class="sxs-lookup"><span data-stu-id="3a367-167">In most cases, this means that the application needs to carry and install the redistributable Nlsdl installer (and not merely copy Nlsdl.dll itself).</span></span>

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a><span data-ttu-id="3a367-168">Passaggio 0: creazione di Hello MUI hardcoded</span><span class="sxs-lookup"><span data-stu-id="3a367-168">Step 0: Creating the Hard-coded Hello MUI</span></span>

<span data-ttu-id="3a367-169">Questa esercitazione inizia con la versione monolingue dell'applicazione Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="3a367-169">This tutorial begins with the monolingual version of the Hello MUI application.</span></span> <span data-ttu-id="3a367-170">L'applicazione presuppone l'uso del linguaggio di programmazione C++, delle stringhe di caratteri wide e della funzione [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) per l'output.</span><span class="sxs-lookup"><span data-stu-id="3a367-170">The application assumes the use of the C++ programming language, wide character strings, and the [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) function for output.</span></span>

<span data-ttu-id="3a367-171">Per iniziare, creare l' \_ applicazione GuiStep 0 iniziale, nonché la soluzione HelloMUI, che contiene tutte le applicazioni in questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-171">Begin by creating the initial GuiStep\_0 application, as well as the HelloMUI solution, which contain all of the applications in this tutorial.</span></span>

1.  <span data-ttu-id="3a367-172">In Visual Studio 2008 creare un nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="3a367-172">In Visual Studio 2008, create a new project.</span></span> <span data-ttu-id="3a367-173">Usare le impostazioni e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a367-173">Use the following settings and values:</span></span>

    1.  <span data-ttu-id="3a367-174">Tipo di progetto: in Visual C++ selezionare Win32, quindi in modelli Visual Studio installati selezionare progetto Win32.</span><span class="sxs-lookup"><span data-stu-id="3a367-174">Project type: Under Visual C++ select Win32, and then under Visual Studio installed templates select Win32 Project.</span></span>
    2.  <span data-ttu-id="3a367-175">Nome: GuiStep \_ 0.</span><span class="sxs-lookup"><span data-stu-id="3a367-175">Name: GuiStep\_0.</span></span>
    3.  <span data-ttu-id="3a367-176">Percorso: *ProjectRootDirectory* (i passaggi successivi fanno riferimento a questa directory).</span><span class="sxs-lookup"><span data-stu-id="3a367-176">Location: *ProjectRootDirectory* (Later steps reference this directory).</span></span>
    4.  <span data-ttu-id="3a367-177">Nome soluzione: HelloMUI.</span><span class="sxs-lookup"><span data-stu-id="3a367-177">Solution Name: HelloMUI.</span></span>
    5.  <span data-ttu-id="3a367-178">Selezionare Crea directory per soluzione.</span><span class="sxs-lookup"><span data-stu-id="3a367-178">Select Create directory for solution.</span></span>
    6.  <span data-ttu-id="3a367-179">Nella creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="3a367-179">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="3a367-180">Configurare il modello di threading del progetto:</span><span class="sxs-lookup"><span data-stu-id="3a367-180">Configure the project threading model:</span></span>

    1.  <span data-ttu-id="3a367-181">Nella Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep \_ 0, quindi scegliere Proprietà.</span><span class="sxs-lookup"><span data-stu-id="3a367-181">In the Solution Explorer, right-click the project GuiStep\_0, and then select Properties.</span></span>
    2.  <span data-ttu-id="3a367-182">Nella finestra di dialogo Pagine delle proprietà del progetto:</span><span class="sxs-lookup"><span data-stu-id="3a367-182">In the project Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="3a367-183">Nell'elenco a discesa in alto a sinistra impostare configurazione su tutte le configurazioni.</span><span class="sxs-lookup"><span data-stu-id="3a367-183">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="3a367-184">In proprietà di configurazione espandere C/C++, selezionare generazione codice e impostare libreria di runtime: debug multithread (/MTd).</span><span class="sxs-lookup"><span data-stu-id="3a367-184">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="3a367-185">Sostituire il contenuto di GuiStep \_ 0. cpp con il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="3a367-185">Replace the contents of GuiStep\_0.cpp with the following code:</span></span>
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  <span data-ttu-id="3a367-186">Compilare ed eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-186">Build and run the application.</span></span>

<span data-ttu-id="3a367-187">Il codice sorgente semplice precedente rende la scelta di progettazione semplicistica, o incorporare, tutto l'output visualizzato dall'utente, in questo caso il testo "Hello MUI".</span><span class="sxs-lookup"><span data-stu-id="3a367-187">The straightforward source code above makes the simplistic design choice of hard-coding, or embedding, all the output the user will see—in this case the text "Hello MUI".</span></span> <span data-ttu-id="3a367-188">Questa scelta limita l'utilità dell'applicazione per gli utenti che non riconoscono la parola inglese "Hello".</span><span class="sxs-lookup"><span data-stu-id="3a367-188">This choice limits the utility of the application for users who don't recognize the English word "Hello."</span></span> <span data-ttu-id="3a367-189">Poiché MUI è un acronimo di inglese basato su tecnologia, per questa esercitazione si presuppone che la stringa rimanga "MUI" per tutte le lingue.</span><span class="sxs-lookup"><span data-stu-id="3a367-189">Because MUI is a technology-based English acronym, it is assumed for this tutorial that the string remains "MUI" for all languages.</span></span>

## <a name="step-1-implementing-the-basic-resource-module"></a><span data-ttu-id="3a367-190">Passaggio 1: implementazione del modulo Resource di base</span><span class="sxs-lookup"><span data-stu-id="3a367-190">Step 1: Implementing the Basic Resource Module</span></span>

<span data-ttu-id="3a367-191">Microsoft Win32 ha esposto a lungo la possibilità per gli sviluppatori di applicazioni di separare i dati delle risorse dell'interfaccia utente dal codice sorgente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-191">Microsoft Win32 has long exposed the capability for application developers to separate their UI resource data from application source code.</span></span> <span data-ttu-id="3a367-192">Questa separazione è costituita dal modello di risorsa Win32, in cui le stringhe, le bitmap, le icone, i messaggi e gli altri elementi normalmente visualizzati a un utente vengono inseriti in una sezione distinta del file eseguibile, separati dal codice eseguibile.</span><span class="sxs-lookup"><span data-stu-id="3a367-192">This separation comes in the form of the Win32 resource model, in which strings, bitmaps, icons, messages and other items normally displayed to a user are packaged into a distinct section of the executable, separated from executable code.</span></span>

<span data-ttu-id="3a367-193">Per illustrare questa separazione tra il codice eseguibile e la creazione di pacchetti di dati delle risorse, in questo passaggio l'esercitazione posiziona la stringa "Hello" hardcoded in precedenza (la risorsa "en-US") nella sezione delle risorse di un modulo DLL nel \_ progetto HelloModule en \_ US.</span><span class="sxs-lookup"><span data-stu-id="3a367-193">To illustrate this separation between executable code and resource data packaging, in this step the tutorial places the previously hard-coded "Hello" string (the "en-US" resource) into the resource section of a DLL module in the HelloModule\_en\_us project.</span></span>

<span data-ttu-id="3a367-194">Questa DLL Win32 può inoltre contenere la funzionalità eseguibile del tipo di libreria (come qualsiasi altra DLL).</span><span class="sxs-lookup"><span data-stu-id="3a367-194">This Win32 DLL could also contain library type executable functionality (as any other DLL might).</span></span> <span data-ttu-id="3a367-195">Tuttavia, per concentrarsi sugli aspetti correlati alle risorse Win32, il codice della DLL di run-time viene eliminato in DllMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="3a367-195">But to help focus on the Win32 resource-related aspects, we leave the run-time DLL code stubbed out in dllmain.cpp.</span></span> <span data-ttu-id="3a367-196">Nelle sezioni successive di questa esercitazione vengono usati i dati della risorsa HelloModule compilati in questo articolo e viene anche presentato il codice di runtime appropriato.</span><span class="sxs-lookup"><span data-stu-id="3a367-196">Subsequent sections of this tutorial make use of the HelloModule resource data being built here and also present appropriate runtime code.</span></span>

<span data-ttu-id="3a367-197">Per costruire un modulo di risorse Win32, iniziare creando una DLL con un valore DllMain eliminato:</span><span class="sxs-lookup"><span data-stu-id="3a367-197">To construct a Win32 resource module, start by creating a DLL with a stubbed out dllmain:</span></span>

1.  <span data-ttu-id="3a367-198">Aggiungere un nuovo progetto alla soluzione HelloMUI:</span><span class="sxs-lookup"><span data-stu-id="3a367-198">Add a new project to the HelloMUI solution:</span></span>

    1.  <span data-ttu-id="3a367-199">Scegliere Aggiungi dal menu file, quindi nuovo progetto.</span><span class="sxs-lookup"><span data-stu-id="3a367-199">From the File menu, select Add, and then New Project.</span></span>
    2.  <span data-ttu-id="3a367-200">Tipo di progetto: progetto Win32.</span><span class="sxs-lookup"><span data-stu-id="3a367-200">Project type: Win32 Project.</span></span>
    3.  <span data-ttu-id="3a367-201">Nome: HelloModule \_ en \_ US.</span><span class="sxs-lookup"><span data-stu-id="3a367-201">Name: HelloModule\_en\_us.</span></span>
    4.  <span data-ttu-id="3a367-202">Percorso: *ProjectRootDirectory* \\ HelloMUI.</span><span class="sxs-lookup"><span data-stu-id="3a367-202">Location: *ProjectRootDirectory*\\HelloMUI.</span></span>
    5.  <span data-ttu-id="3a367-203">Nella creazione guidata applicazione Win32 selezionare tipo di applicazione: DLL.</span><span class="sxs-lookup"><span data-stu-id="3a367-203">In the Win32 Application Wizard, select Application type: DLL.</span></span>

2.  <span data-ttu-id="3a367-204">Configurare il modello di threading del progetto:</span><span class="sxs-lookup"><span data-stu-id="3a367-204">Configure this project's threading model:</span></span>

    1.  <span data-ttu-id="3a367-205">Nel Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto HelloModule \_ en \_ US e scegliere Proprietà.</span><span class="sxs-lookup"><span data-stu-id="3a367-205">In the Solution Explorer, right-click the project HelloModule\_en\_us and select Properties.</span></span>
    2.  <span data-ttu-id="3a367-206">Nella finestra di dialogo Pagine delle proprietà del progetto:</span><span class="sxs-lookup"><span data-stu-id="3a367-206">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="3a367-207">Nell'elenco a discesa in alto a sinistra impostare configurazione su tutte le configurazioni.</span><span class="sxs-lookup"><span data-stu-id="3a367-207">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="3a367-208">In proprietà di configurazione espandere C/C++, selezionare generazione codice e impostare libreria di runtime: debug multithread (/MTd).</span><span class="sxs-lookup"><span data-stu-id="3a367-208">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="3a367-209">Esaminare DllMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="3a367-209">Examine dllmain.cpp.</span></span> <span data-ttu-id="3a367-210">(Potrebbe essere necessario aggiungere l'oggetto senza riferimenti \_ Macro di parametri per il codice generato, come in questo caso, per consentirne la compilazione a livello di avviso 4.</span><span class="sxs-lookup"><span data-stu-id="3a367-210">(You may want to add the UNREFERENCED\_PARAMETER macros to the generated code, as we have here, to enable it to compile at warning level 4.)</span></span>
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  <span data-ttu-id="3a367-211">Aggiungere un file di definizione delle risorse HelloModule. RC al progetto:</span><span class="sxs-lookup"><span data-stu-id="3a367-211">Add a resource-definition file HelloModule.rc to the project:</span></span>

    1.  <span data-ttu-id="3a367-212">Nel progetto HelloModule \_ en \_ US, fare clic con il pulsante destro del mouse sulla cartella file di risorse e scegliere Aggiungi, quindi selezionare nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="3a367-212">Under the project HelloModule\_en\_us, right-click the Resource Files folder, and select Add, and then select New Item.</span></span>
    2.  <span data-ttu-id="3a367-213">Nella finestra di dialogo Aggiungi nuovo elemento scegliere gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a367-213">In the Add New Item dialog box, choose the following:</span></span>

        1.  <span data-ttu-id="3a367-214">Categorie: in Visual C++ selezionare la risorsa e quindi in "modelli Visual Studio installati" selezionare file di risorse (. RC).</span><span class="sxs-lookup"><span data-stu-id="3a367-214">Categories: Under Visual C++ select Resource, and then under "Visual Studio installed templates" select Resource File (.rc).</span></span>
        2.  <span data-ttu-id="3a367-215">Nome: HelloModule.</span><span class="sxs-lookup"><span data-stu-id="3a367-215">Name: HelloModule.</span></span>
        3.  <span data-ttu-id="3a367-216">Percorso: accettare il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3a367-216">Location: accept the default.</span></span>
        4.  <span data-ttu-id="3a367-217">Fare clic su Aggiungi.</span><span class="sxs-lookup"><span data-stu-id="3a367-217">Click Add.</span></span>

    3.  <span data-ttu-id="3a367-218">Specifica che il nuovo file HelloModule. RC deve essere salvato come Unicode:</span><span class="sxs-lookup"><span data-stu-id="3a367-218">Specify that the new HelloModule.rc file is to be saved as Unicode:</span></span>

        1.  <span data-ttu-id="3a367-219">Nella Esplora soluzioni fare clic con il pulsante destro del mouse su HelloModule. RC e selezionare Visualizza codice.</span><span class="sxs-lookup"><span data-stu-id="3a367-219">In the Solution Explorer, right-click HelloModule.rc, and select View Code.</span></span>
        2.  <span data-ttu-id="3a367-220">Se viene visualizzato un messaggio che indica che il file è già aperto e chiede se si desidera chiuderlo, fare clic su Sì.</span><span class="sxs-lookup"><span data-stu-id="3a367-220">If you see a message that tells you that the file is already open, and asks whether you want to close it, click Yes.</span></span>
        3.  <span data-ttu-id="3a367-221">Con il file visualizzato come testo, scegliere il file di selezione dei menu e quindi Opzioni di salvataggio avanzate.</span><span class="sxs-lookup"><span data-stu-id="3a367-221">With the file displayed as text, make the menu selection File and then Advanced Save Options.</span></span>
        4.  <span data-ttu-id="3a367-222">In codifica specificare Unicode-codepage 1200.</span><span class="sxs-lookup"><span data-stu-id="3a367-222">Under Encoding, specify Unicode - Codepage 1200.</span></span>
        5.  <span data-ttu-id="3a367-223">Fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="3a367-223">Click OK.</span></span>
        6.  <span data-ttu-id="3a367-224">Salvare e chiudere HelloModule. RC.</span><span class="sxs-lookup"><span data-stu-id="3a367-224">Save and close HelloModule.rc.</span></span>

    4.  <span data-ttu-id="3a367-225">Aggiungere una tabella di stringhe contenente la stringa "Hello":</span><span class="sxs-lookup"><span data-stu-id="3a367-225">Add a string table containing the "Hello" string:</span></span>

        1.  <span data-ttu-id="3a367-226">Nella Visualizzazione risorse fare clic con il pulsante destro del mouse su HelloModule. RC e scegliere Aggiungi risorsa.</span><span class="sxs-lookup"><span data-stu-id="3a367-226">In the Resource View, right-click HelloModule.rc and select Add Resource.</span></span>
        2.  <span data-ttu-id="3a367-227">Selezionare tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="3a367-227">Select String Table.</span></span>
        3.  <span data-ttu-id="3a367-228">Fare clic su New.</span><span class="sxs-lookup"><span data-stu-id="3a367-228">Click New.</span></span>
        4.  <span data-ttu-id="3a367-229">Aggiungere una stringa alla tabella delle stringhe:</span><span class="sxs-lookup"><span data-stu-id="3a367-229">Add a string to the String Table:</span></span>

            1.  <span data-ttu-id="3a367-230">ID: Salve \_ MUI \_ Str \_ 0.</span><span class="sxs-lookup"><span data-stu-id="3a367-230">ID: HELLO\_MUI\_STR\_0.</span></span>
            2.  <span data-ttu-id="3a367-231">Valore: 0</span><span class="sxs-lookup"><span data-stu-id="3a367-231">Value: 0.</span></span>
            3.  <span data-ttu-id="3a367-232">Didascalia: Hello.</span><span class="sxs-lookup"><span data-stu-id="3a367-232">Caption: Hello.</span></span>

        <span data-ttu-id="3a367-233">Se si visualizza HelloModule. RC come testo ora, verranno visualizzate varie parti del codice sorgente specifico per le risorse.</span><span class="sxs-lookup"><span data-stu-id="3a367-233">If you view HelloModule.rc as text now, you will see various pieces of resource-specific source code.</span></span> <span data-ttu-id="3a367-234">Il primo interesse è la sezione che descrive la stringa "Hello":</span><span class="sxs-lookup"><span data-stu-id="3a367-234">The one of greatest interest is the section that describes the "Hello" string:</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        <span data-ttu-id="3a367-235">Questa stringa "Hello" è la risorsa che deve essere localizzata, ovvero convertita, in ogni lingua che l'applicazione spera di supportare.</span><span class="sxs-lookup"><span data-stu-id="3a367-235">This "Hello" string is the resource that needs to be localized (that is, translated) into every language that the application hopes to support.</span></span> <span data-ttu-id="3a367-236">Ad esempio, il HelloModule \_ TA \_ in Project (che verrà creato nel passaggio successivo) conterrà la propria versione localizzata di HelloModule. RC per "ta-in":</span><span class="sxs-lookup"><span data-stu-id="3a367-236">For example, the HelloModule\_ta\_in project (which you will create in the next step) will contain its own localized version of HelloModule.rc for "ta-IN":</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  <span data-ttu-id="3a367-237">Compilare il \_ progetto HelloModule en \_ US per assicurarsi che non siano presenti errori.</span><span class="sxs-lookup"><span data-stu-id="3a367-237">Build the HelloModule\_en\_us project to be sure there are no errors.</span></span>

5.  <span data-ttu-id="3a367-238">Creare sei altri progetti nella soluzione HelloMUI (o il numero desiderato) per creare sei altre DLL di risorse per altre lingue.</span><span class="sxs-lookup"><span data-stu-id="3a367-238">Create six more projects in the HelloMUI solution (or as many of them as you wish) to create six more resource DLLs for additional languages.</span></span> <span data-ttu-id="3a367-239">Usare i valori in questa tabella:</span><span class="sxs-lookup"><span data-stu-id="3a367-239">Use the values in this table:</span></span>

    | <span data-ttu-id="3a367-240">Project name (Nome progetto)</span><span class="sxs-lookup"><span data-stu-id="3a367-240">Project name</span></span>        | <span data-ttu-id="3a367-241">Nome del file RC</span><span class="sxs-lookup"><span data-stu-id="3a367-241">Name of .rc file</span></span> | <span data-ttu-id="3a367-242">ID stringa</span><span class="sxs-lookup"><span data-stu-id="3a367-242">String ID</span></span>          | <span data-ttu-id="3a367-243">Valore stringa</span><span class="sxs-lookup"><span data-stu-id="3a367-243">String value</span></span> | <span data-ttu-id="3a367-244">Didascalia stringa</span><span class="sxs-lookup"><span data-stu-id="3a367-244">String caption</span></span> |
    |---------------------|------------------|--------------------|--------------|----------------|
    | <span data-ttu-id="3a367-245">HelloModule \_ de \_ de</span><span class="sxs-lookup"><span data-stu-id="3a367-245">HelloModule\_de\_de</span></span> | <span data-ttu-id="3a367-246">HelloModule</span><span class="sxs-lookup"><span data-stu-id="3a367-246">HelloModule</span></span>      | <span data-ttu-id="3a367-247">HELLo \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a367-247">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3a367-248">0</span><span class="sxs-lookup"><span data-stu-id="3a367-248">0</span></span>            | <span data-ttu-id="3a367-249">Hallo</span><span class="sxs-lookup"><span data-stu-id="3a367-249">Hallo</span></span>          |
    | <span data-ttu-id="3a367-250">HelloModule \_ es \_ es</span><span class="sxs-lookup"><span data-stu-id="3a367-250">HelloModule\_es\_es</span></span> | <span data-ttu-id="3a367-251">HelloModule</span><span class="sxs-lookup"><span data-stu-id="3a367-251">HelloModule</span></span>      | <span data-ttu-id="3a367-252">HELLo \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a367-252">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3a367-253">0</span><span class="sxs-lookup"><span data-stu-id="3a367-253">0</span></span>            | <span data-ttu-id="3a367-254">Hola</span><span class="sxs-lookup"><span data-stu-id="3a367-254">Hola</span></span>           |
    | <span data-ttu-id="3a367-255">HelloModule \_ fr \_ fr</span><span class="sxs-lookup"><span data-stu-id="3a367-255">HelloModule\_fr\_fr</span></span> | <span data-ttu-id="3a367-256">HelloModule</span><span class="sxs-lookup"><span data-stu-id="3a367-256">HelloModule</span></span>      | <span data-ttu-id="3a367-257">HELLo \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a367-257">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3a367-258">0</span><span class="sxs-lookup"><span data-stu-id="3a367-258">0</span></span>            | <span data-ttu-id="3a367-259">Bonjour</span><span class="sxs-lookup"><span data-stu-id="3a367-259">Bonjour</span></span>        |
    | <span data-ttu-id="3a367-260">HelloModule \_ Hi \_ in</span><span class="sxs-lookup"><span data-stu-id="3a367-260">HelloModule\_hi\_in</span></span> | <span data-ttu-id="3a367-261">HelloModule</span><span class="sxs-lookup"><span data-stu-id="3a367-261">HelloModule</span></span>      | <span data-ttu-id="3a367-262">HELLo \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a367-262">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3a367-263">0</span><span class="sxs-lookup"><span data-stu-id="3a367-263">0</span></span>            | <span data-ttu-id="3a367-264">नमस्</span><span class="sxs-lookup"><span data-stu-id="3a367-264">नमस्</span></span>           |
    | <span data-ttu-id="3a367-265">HelloModule \_ ur \_ ur</span><span class="sxs-lookup"><span data-stu-id="3a367-265">HelloModule\_ru\_ru</span></span> | <span data-ttu-id="3a367-266">HelloModule</span><span class="sxs-lookup"><span data-stu-id="3a367-266">HelloModule</span></span>      | <span data-ttu-id="3a367-267">HELLo \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a367-267">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3a367-268">0</span><span class="sxs-lookup"><span data-stu-id="3a367-268">0</span></span>            | <span data-ttu-id="3a367-269">Здравствуйте</span><span class="sxs-lookup"><span data-stu-id="3a367-269">Здравствуйте</span></span>   |
    | <span data-ttu-id="3a367-270">HelloModule \_ TA \_ in</span><span class="sxs-lookup"><span data-stu-id="3a367-270">HelloModule\_ta\_in</span></span> | <span data-ttu-id="3a367-271">HelloModule</span><span class="sxs-lookup"><span data-stu-id="3a367-271">HelloModule</span></span>      | <span data-ttu-id="3a367-272">HELLo \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="3a367-272">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="3a367-273">0</span><span class="sxs-lookup"><span data-stu-id="3a367-273">0</span></span>            | <span data-ttu-id="3a367-274">வணக்கம்</span><span class="sxs-lookup"><span data-stu-id="3a367-274">வணக்கம்</span></span>        |

    

     

<span data-ttu-id="3a367-275">Per ulteriori informazioni sulla sintassi e la struttura dei file RC, vedere [informazioni sui file di risorse](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="3a367-275">For more about .rc file structure and syntax, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

## <a name="step-2-building-the-basic-resource-module"></a><span data-ttu-id="3a367-276">Passaggio 2: compilazione del modulo Resource di base</span><span class="sxs-lookup"><span data-stu-id="3a367-276">Step 2: Building the Basic Resource Module</span></span>

<span data-ttu-id="3a367-277">Usando i modelli di risorse precedenti, la compilazione di uno dei sette progetti HelloModule comporterebbe sette DLL separate.</span><span class="sxs-lookup"><span data-stu-id="3a367-277">Using previous resource models, building any one of the seven HelloModule projects would result in seven separate DLLs.</span></span> <span data-ttu-id="3a367-278">Ogni DLL conterrà una sezione delle risorse con una singola stringa localizzata nella lingua appropriata.</span><span class="sxs-lookup"><span data-stu-id="3a367-278">Each DLL would contain a resource section with a single string localized into the appropriate language.</span></span> <span data-ttu-id="3a367-279">Sebbene sia appropriato per il modello di risorse Win32 storico, questo progetto non sfrutta i vantaggi di MUI.</span><span class="sxs-lookup"><span data-stu-id="3a367-279">Although appropriate for the historic Win32 resource model, this design does not take advantage of MUI.</span></span>

<span data-ttu-id="3a367-280">In Windows Vista SDK e versioni successive, MUI consente di suddividere i file eseguibili in codice sorgente e moduli di contenuto localizzabili.</span><span class="sxs-lookup"><span data-stu-id="3a367-280">In the Windows Vista SDK and later, MUI provides the ability to split executables into source code and localizable content modules.</span></span> <span data-ttu-id="3a367-281">Con la personalizzazione aggiuntiva più avanti nel passaggio 5, le applicazioni possono essere abilitate per l'esecuzione del supporto multilingue nelle versioni precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3a367-281">With the additional customization that is covered later in Step 5, applications can be enabled for multi-lingual support to run on versions prior to Windows Vista.</span></span>

<span data-ttu-id="3a367-282">I meccanismi principali disponibili per suddividere le risorse dal codice eseguibile, a partire da Windows Vista, sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a367-282">The primary mechanisms available to split resources from executable code, starting with Windows Vista, are:</span></span>

-   <span data-ttu-id="3a367-283">Utilizzando rc.exe (il compilatore RC) con commutatori specifici o</span><span class="sxs-lookup"><span data-stu-id="3a367-283">Using rc.exe (the RC Compiler) with specific switches, or</span></span>
-   <span data-ttu-id="3a367-284">Utilizzando uno strumento di suddivisione dello stile di post-compilazione denominato muirct.exe.</span><span class="sxs-lookup"><span data-stu-id="3a367-284">Using a post-build style splitting tool named muirct.exe.</span></span>

<span data-ttu-id="3a367-285">Per ulteriori informazioni, vedere [Utilità risorse](resource-utilities.md) .</span><span class="sxs-lookup"><span data-stu-id="3a367-285">See [Resource Utilities](resource-utilities.md) for more information.</span></span>

<span data-ttu-id="3a367-286">Per semplicità, in questa esercitazione viene usato muirct.exe per suddividere il file eseguibile "Hello MUI".</span><span class="sxs-lookup"><span data-stu-id="3a367-286">For the sake of simplicity, this tutorial uses muirct.exe to split the "Hello MUI" executable.</span></span>

### <a name="splitting-the-various-language-resource-modules-an-overview"></a><span data-ttu-id="3a367-287">Suddivisione dei diversi moduli di risorse della lingua: Panoramica</span><span class="sxs-lookup"><span data-stu-id="3a367-287">Splitting the Various Language Resource Modules: An Overview</span></span>

<span data-ttu-id="3a367-288">Per suddividere le dll in un HelloModule.dll eseguibile, oltre a una HelloModule.dll. MUI per ognuna delle sette lingue supportate in questa esercitazione, è necessario un processo multiparte.</span><span class="sxs-lookup"><span data-stu-id="3a367-288">A multi-part process is involved in splitting the DLLs into one executable HelloModule.dll, plus a HelloModule.dll.mui for each of the seven supported languages within this tutorial.</span></span> <span data-ttu-id="3a367-289">In questa panoramica vengono descritti i passaggi necessari. la sezione successiva presenta un file di comando che esegue questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="3a367-289">This overview describes the required steps; the next section presents a command file that performs those steps.</span></span>

<span data-ttu-id="3a367-290">Per prima cosa, suddividere il modulo HelloModule.dll solo in lingua inglese usando il comando:</span><span class="sxs-lookup"><span data-stu-id="3a367-290">First, split the English-only HelloModule.dll module by using the command:</span></span>


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



<span data-ttu-id="3a367-291">La riga di comando precedente usa il file di configurazione DoReverseMuiLoc. rcconfig.</span><span class="sxs-lookup"><span data-stu-id="3a367-291">The command line above uses the configuration file DoReverseMuiLoc.rcconfig.</span></span> <span data-ttu-id="3a367-292">Questo tipo di file di configurazione viene in genere usato da muirct.exe per suddividere le risorse tra la DLL indipendente dalla lingua e i file con estensione MUI dipendenti dal linguaggio.</span><span class="sxs-lookup"><span data-stu-id="3a367-292">This type of configuration file is typically used by muirct.exe to split resources between the language-neutral (LN) DLL and the language-dependent .mui files.</span></span> <span data-ttu-id="3a367-293">In questo caso, il file XML DoReverseMuiLoc. rcconfig (elencato nella sezione successiva) indica molti tipi di risorse, ma tutti rientrano nella categoria di file "localizedResources" o MUI e non sono presenti risorse nella categoria indipendente dal linguaggio.</span><span class="sxs-lookup"><span data-stu-id="3a367-293">In this case, the DoReverseMuiLoc.rcconfig xml file (listed in the next section) indicates many resource types, but they all fall into the "localizedResources" or .mui file category, and there are no resources in the language-neutral category.</span></span> <span data-ttu-id="3a367-294">Per altre informazioni su come preparare un file di configurazione delle risorse, vedere [preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="3a367-294">For more information about how to prepare a resource configuration file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="3a367-295">Oltre a creare un file HelloModule.dll. MUI che contiene la stringa inglese "Hello", muirct.exe incorpora anche una risorsa MUI nel modulo HelloModule.dll durante la suddivisione.</span><span class="sxs-lookup"><span data-stu-id="3a367-295">In addition to creating a HelloModule.dll.mui file which contains the English string "Hello", muirct.exe also embeds a MUI resource into the HelloModule.dll module during the splitting.</span></span> <span data-ttu-id="3a367-296">Per eseguire correttamente il caricamento in fase di esecuzione delle risorse appropriate dai moduli HelloModule.dll. mui specifici del linguaggio, è necessario che i checksum dei file con estensione mui siano corretti in modo che corrispondano ai valori di checksum nel modulo di base lingua-indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="3a367-296">In order to properly load at run-time the appropriate resources from the language-specific HelloModule.dll.mui modules, each .mui file must have its checksums fixed-up to match the checksums in the baseline language-neutral LN module.</span></span> <span data-ttu-id="3a367-297">Questa operazione viene eseguita tramite un comando, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="3a367-297">This is done by a command such as:</span></span>


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



<span data-ttu-id="3a367-298">Analogamente, viene richiamato muirct.exe per creare un file HelloModule.dll. MUI per ognuno degli altri linguaggi.</span><span class="sxs-lookup"><span data-stu-id="3a367-298">Similarly, muirct.exe is invoked to create a HelloModule.dll.mui file for each of the other languages.</span></span> <span data-ttu-id="3a367-299">In questi casi, tuttavia, la DLL indipendente dalla lingua viene eliminata, perché sarà necessaria solo la prima creazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-299">However, in those cases the language-neutral DLL is discarded, as only the first one created will be needed.</span></span> <span data-ttu-id="3a367-300">I comandi che elaborano le risorse spagnole e francesi hanno un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="3a367-300">The commands that process the Spanish and French resources look like this:</span></span>


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



<span data-ttu-id="3a367-301">Uno degli aspetti più importanti da notare nella muirct.exe righe di comando precedente è che il flag-x viene usato per specificare un ID lingua di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-301">One of the most important things to notice in the muirct.exe command lines above is that the -x flag is used to specify a target language ID.</span></span> <span data-ttu-id="3a367-302">Il valore fornito per muirct.exe è diverso per ogni modulo di HelloModule.dll specifico della lingua.</span><span class="sxs-lookup"><span data-stu-id="3a367-302">The value provided to muirct.exe is different for each language-specific HelloModule.dll module.</span></span> <span data-ttu-id="3a367-303">Il valore di questo linguaggio è Central e viene usato da muirct.exe per contrassegnare in modo appropriato il file con estensione MUI durante la suddivisione.</span><span class="sxs-lookup"><span data-stu-id="3a367-303">This language value is central and is used by muirct.exe to appropriately mark the .mui file during splitting.</span></span> <span data-ttu-id="3a367-304">Un valore non corretto produce errori di caricamento delle risorse per quel particolare file con estensione MUI in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3a367-304">An incorrect value produces resource loading failures for that particular .mui file at run-time.</span></span> <span data-ttu-id="3a367-305">Per ulteriori informazioni sul mapping tra nome del linguaggio e LCID, vedere [costanti e stringhe degli identificatori di lingua](language-identifier-constants-and-strings.md) .</span><span class="sxs-lookup"><span data-stu-id="3a367-305">See [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md) for more details on mapping language name to LCID.</span></span>

<span data-ttu-id="3a367-306">Ogni file Split. MUI viene inserito in una directory corrispondente al nome della lingua, immediatamente sotto la directory in cui risiederà la HelloModule.dll indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="3a367-306">Each split .mui file ends up being placed into a directory corresponding to its language name, immediately underneath the directory in which the language-neutral HelloModule.dll will reside.</span></span> <span data-ttu-id="3a367-307">Per ulteriori informazioni sul posizionamento dei file con estensione MUI, vedere [distribuzione di applicazioni](application-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="3a367-307">For more about .mui file placement, see [Application Deployment](application-deployment.md).</span></span>

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a><span data-ttu-id="3a367-308">Suddivisione dei diversi moduli di risorse della lingua: creazione dei file</span><span class="sxs-lookup"><span data-stu-id="3a367-308">Splitting the Various Language Resource Modules: Creating the Files</span></span>

<span data-ttu-id="3a367-309">Per questa esercitazione è possibile creare un file di comando contenente i comandi per suddividere le varie dll e richiamarlo manualmente.</span><span class="sxs-lookup"><span data-stu-id="3a367-309">For this tutorial you create a command file containing the commands to split the various DLLs, and you invoke it manually.</span></span> <span data-ttu-id="3a367-310">Si noti che durante il lavoro di sviluppo effettivo, è possibile ridurre il rischio di errori di compilazione includendo questi comandi come eventi di pre-compilazione o post-compilazione nella soluzione HelloMUI, ma questo esula dall'ambito di questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-310">Note that in actual development work, you could reduce the potential for build errors by including these commands as pre-build or post-build events in the HelloMUI solution, but that is beyond the scope of this tutorial.</span></span>

<span data-ttu-id="3a367-311">Creare i file per la build di debug:</span><span class="sxs-lookup"><span data-stu-id="3a367-311">Create the files for the debug build:</span></span>

1.  <span data-ttu-id="3a367-312">Creare un file di comando DoReverseMuiLoc. cmd contenente i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a367-312">Create a command file DoReverseMuiLoc.cmd containing the following commands:</span></span>
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  <span data-ttu-id="3a367-313">Creare un file XML DoReverseMuiLoc. rcconfig contenente le righe seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a367-313">Create an xml file DoReverseMuiLoc.rcconfig containing the following lines:</span></span>
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  <span data-ttu-id="3a367-314">Copiare DoReverseMuiLoc. cmd e DoReverseMuiLoc. rcconfig in *ProjectRootDirectory* \\ HelloMUI \\ debug.</span><span class="sxs-lookup"><span data-stu-id="3a367-314">Copy DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig to *ProjectRootDirectory*\\HelloMUI\\Debug.</span></span>
4.  <span data-ttu-id="3a367-315">Aprire il prompt dei comandi di Visual Studio 2008 e passare alla directory di debug.</span><span class="sxs-lookup"><span data-stu-id="3a367-315">Open the Visual Studio 2008 command prompt and navigate to the Debug directory.</span></span>
5.  <span data-ttu-id="3a367-316">Eseguire DoReverseMuiLoc. cmd.</span><span class="sxs-lookup"><span data-stu-id="3a367-316">Run DoReverseMuiLoc.cmd.</span></span>

<span data-ttu-id="3a367-317">Quando si crea una build di rilascio, si copiano gli stessi file DoReverseMuiLoc. cmd e DoReverseMuiLoc. rcconfig nella directory della versione ed eseguire il file di comando.</span><span class="sxs-lookup"><span data-stu-id="3a367-317">When you create a release build, you copy the same DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig files to the Release directory and run the command file there.</span></span>

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a><span data-ttu-id="3a367-318">Passaggio 3: creazione di un Resource-Savvy "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3a367-318">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>

<span data-ttu-id="3a367-319">Basandosi sull'GuiStep iniziale hardcoded \_0.exe esempio precedente, è possibile estendere la portata dell'applicazione a più utenti del linguaggio scegliendo di incorporare il modello di risorse Win32.</span><span class="sxs-lookup"><span data-stu-id="3a367-319">Building on the initial hard-coded GuiStep\_0.exe example from above, you could extend the reach of the application to multiple language users by choosing to incorporate the Win32 resource model.</span></span> <span data-ttu-id="3a367-320">Il nuovo codice di runtime presentato in questo passaggio include la logica di caricamento dei moduli ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) e il recupero di stringhe ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).</span><span class="sxs-lookup"><span data-stu-id="3a367-320">The new run-time code presented in this step includes the module loading ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) and string retrieval ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)) logic.</span></span>

1.  <span data-ttu-id="3a367-321">Aggiungere un nuovo progetto alla soluzione HelloMUI (usando il menu file di selezione, Aggiungi e nuovo progetto) con i valori e le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a367-321">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="3a367-322">Tipo di progetto: progetto Win32.</span><span class="sxs-lookup"><span data-stu-id="3a367-322">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="3a367-323">Nome: GuiStep \_ 1.</span><span class="sxs-lookup"><span data-stu-id="3a367-323">Name: GuiStep\_1.</span></span>
    3.  <span data-ttu-id="3a367-324">Percorso: accettare il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3a367-324">Location: accept the default.</span></span>
    4.  <span data-ttu-id="3a367-325">Nella creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="3a367-325">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="3a367-326">Impostare questo progetto per l'esecuzione dall'interno di Visual Studio e configurarne il modello di threading:</span><span class="sxs-lookup"><span data-stu-id="3a367-326">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="3a367-327">Nella Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep \_ 1 e selezionare Imposta come progetto di avvio.</span><span class="sxs-lookup"><span data-stu-id="3a367-327">In the Solution Explorer, right-click the project GuiStep\_1 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="3a367-328">Fare di nuovo clic con il pulsante destro del mouse e scegliere Proprietà.</span><span class="sxs-lookup"><span data-stu-id="3a367-328">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="3a367-329">Nella finestra di dialogo Pagine delle proprietà del progetto:</span><span class="sxs-lookup"><span data-stu-id="3a367-329">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="3a367-330">Nell'elenco a discesa in alto a sinistra impostare configurazione su tutte le configurazioni.</span><span class="sxs-lookup"><span data-stu-id="3a367-330">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="3a367-331">In proprietà di configurazione espandere C/C++, selezionare generazione codice e impostare libreria di runtime: debug multithread (/MTd).</span><span class="sxs-lookup"><span data-stu-id="3a367-331">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="3a367-332">Sostituire il contenuto di GuiStep \_ 1. cpp con il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="3a367-332">Replace the contents of GuiStep\_1.cpp with the following code:</span></span>
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  <span data-ttu-id="3a367-333">Compilare ed eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-333">Build and run the application.</span></span> <span data-ttu-id="3a367-334">L'output verrà visualizzato nella lingua attualmente impostata come lingua di visualizzazione del computer (purché sia una delle sette lingue compilate).</span><span class="sxs-lookup"><span data-stu-id="3a367-334">The output will be displayed in the language currently set as the display language of the computer (provided it is one of the seven languages we have built).</span></span>

## <a name="step-4-globalizing-hello-mui"></a><span data-ttu-id="3a367-335">Passaggio 4: globalizzazione di "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3a367-335">Step 4: Globalizing "Hello MUI"</span></span>

<span data-ttu-id="3a367-336">Sebbene l'esempio precedente sia in grado di visualizzare l'output in lingue diverse, il numero di aree è ridotto.</span><span class="sxs-lookup"><span data-stu-id="3a367-336">Although the previous example is able to display its output in different languages, it falls short in a number of areas.</span></span> <span data-ttu-id="3a367-337">Probabilmente il più evidente è che l'applicazione è disponibile solo in un piccolo subset di linguaggi rispetto al sistema operativo Windows stesso.</span><span class="sxs-lookup"><span data-stu-id="3a367-337">Perhaps the most noticeable is that the application is only available in a small subset of languages when compared to the Windows operating system itself.</span></span> <span data-ttu-id="3a367-338">Se, ad esempio, l' \_ applicazione GuiStep 1 del passaggio precedente è stata installata in una build giapponese di Windows, è probabile che si verifichino errori nella posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="3a367-338">If, for example, the GuiStep\_1 application from the previous step were installed on a Japanese build of Windows, resource location failures would be likely.</span></span>

<span data-ttu-id="3a367-339">Per risolvere questo problema, sono disponibili due opzioni principali:</span><span class="sxs-lookup"><span data-stu-id="3a367-339">To address this situation, you have two primary options:</span></span>

-   <span data-ttu-id="3a367-340">Verificare che siano incluse le risorse in un linguaggio di fallback finale predeterminato.</span><span class="sxs-lookup"><span data-stu-id="3a367-340">Ensure that resources in a predetermined ultimate fallback language are included.</span></span>
-   <span data-ttu-id="3a367-341">Consente all'utente finale di configurare le preferenze di lingua da un sottoinsieme di linguaggi specificamente supportati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-341">Provide a way for the end user to configure their language preferences from among the subset of languages specifically supported by the application.</span></span>

<span data-ttu-id="3a367-342">Di queste opzioni, l'unico che fornisce un linguaggio di fallback finale è altamente consigliato e viene implementato in questa esercitazione passando il flag-g a muirct.exe, come illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3a367-342">Of these options, the one providing an ultimate fallback language is highly advisable and is implemented in this tutorial by passing the -g flag to muirct.exe, as seen above.</span></span> <span data-ttu-id="3a367-343">Questo flag indica muirct.exe di creare una lingua specifica (de-DE/0x0407) la lingua di fallback finale associata al modulo dll indipendente dalla lingua (HelloModule.dll).</span><span class="sxs-lookup"><span data-stu-id="3a367-343">This flag tells muirct.exe to make a specific language (de-DE / 0x0407) the ultimate fallback language associated with the language-neutral dll module (HelloModule.dll).</span></span> <span data-ttu-id="3a367-344">In fase di esecuzione questo parametro viene usato come ultima risorsa per generare il testo da visualizzare all'utente.</span><span class="sxs-lookup"><span data-stu-id="3a367-344">At run-time this parameter is used as a last resort to generate text to display to the user.</span></span> <span data-ttu-id="3a367-345">Nel caso in cui non venga individuato un linguaggio di fallback finale e non siano disponibili risorse appropriate nel file binario indipendente dalla lingua, il caricamento della risorsa ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3a367-345">In the event that an ultimate fallback language is not found and no appropriate resource is available in the language-neutral binary, loading of the resource fails.</span></span> <span data-ttu-id="3a367-346">È pertanto necessario determinare con attenzione gli scenari che potrebbero verificarsi nell'applicazione e pianificare di conseguenza il linguaggio di fallback finale.</span><span class="sxs-lookup"><span data-stu-id="3a367-346">Therefore you should carefully determine the scenarios that your application might encounter and plan the ultimate fallback language accordingly.</span></span>

<span data-ttu-id="3a367-347">L'altra opzione di consentire le preferenze per la lingua configurabile e il caricamento delle risorse in base a questa gerarchia definita dall'utente può aumentare significativamente la soddisfazione dei clienti.</span><span class="sxs-lookup"><span data-stu-id="3a367-347">The other option of allowing for configurable language preferences and loading resources based on this user-defined hierarchy can greatly increase customer satisfaction.</span></span> <span data-ttu-id="3a367-348">Sfortunatamente, complica anche la funzionalità necessaria all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-348">Unfortunately, it also complicates the functionality needed within the application.</span></span>

<span data-ttu-id="3a367-349">Questo passaggio dell'esercitazione usa un meccanismo di file di testo semplificato per abilitare la configurazione della lingua utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="3a367-349">This step of the tutorial uses a simplified text file mechanism to enable custom user language configuration.</span></span> <span data-ttu-id="3a367-350">Il file di testo viene analizzato in fase di esecuzione dall'applicazione e l'elenco di lingue analizzate e convalidate viene usato per stabilire un elenco di fallback personalizzato.</span><span class="sxs-lookup"><span data-stu-id="3a367-350">The text file is parsed at run-time by the application, and the parsed and validated language list is used in establishing a custom fallback list.</span></span> <span data-ttu-id="3a367-351">Una volta stabilito l'elenco di fallback personalizzato, le API di Windows caricherà le risorse in base alla precedenza della lingua impostata in questo elenco.</span><span class="sxs-lookup"><span data-stu-id="3a367-351">After the custom fallback list is established, the Windows APIs will load resources according to the language precedence set forth in this list.</span></span> <span data-ttu-id="3a367-352">Il resto del codice è simile a quello riportato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="3a367-352">The remainder of the code is similar to that found in the preceding step.</span></span>

1.  <span data-ttu-id="3a367-353">Aggiungere un nuovo progetto alla soluzione HelloMUI (usando il menu file di selezione, Aggiungi e nuovo progetto) con i valori e le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a367-353">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="3a367-354">Tipo di progetto: progetto Win32.</span><span class="sxs-lookup"><span data-stu-id="3a367-354">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="3a367-355">Nome: GuiStep \_ 2.</span><span class="sxs-lookup"><span data-stu-id="3a367-355">Name: GuiStep\_2.</span></span>
    3.  <span data-ttu-id="3a367-356">Percorso: accettare il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3a367-356">Location: accept the default.</span></span>
    4.  <span data-ttu-id="3a367-357">Nella creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="3a367-357">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="3a367-358">Impostare questo progetto per l'esecuzione dall'interno di Visual Studio e configurarne il modello di threading:</span><span class="sxs-lookup"><span data-stu-id="3a367-358">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="3a367-359">Nella Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep \_ 2 e selezionare Imposta come progetto di avvio.</span><span class="sxs-lookup"><span data-stu-id="3a367-359">In the Solution Explorer, right-click the project GuiStep\_2 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="3a367-360">Fare di nuovo clic con il pulsante destro del mouse e scegliere Proprietà.</span><span class="sxs-lookup"><span data-stu-id="3a367-360">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="3a367-361">Nella finestra di dialogo Pagine delle proprietà del progetto:</span><span class="sxs-lookup"><span data-stu-id="3a367-361">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="3a367-362">Nell'elenco a discesa in alto a sinistra impostare configurazione su tutte le configurazioni.</span><span class="sxs-lookup"><span data-stu-id="3a367-362">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="3a367-363">In proprietà di configurazione espandere C/C++, selezionare generazione codice e impostare libreria di runtime: debug multithread (/MTd).</span><span class="sxs-lookup"><span data-stu-id="3a367-363">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="3a367-364">Sostituire il contenuto di GuiStep \_ 2. cpp con il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="3a367-364">Replace the contents of GuiStep\_2.cpp with the following code:</span></span>
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="3a367-365">Creare un file di testo Unicode langs.txt contenente la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="3a367-365">Create a Unicode text file langs.txt containing the following line:</span></span>

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > <span data-ttu-id="3a367-366">Assicurarsi di salvare il file come Unicode.</span><span class="sxs-lookup"><span data-stu-id="3a367-366">Be sure to save the file as Unicode.</span></span>

     

    <span data-ttu-id="3a367-367">Copiare langs.txt nella directory da cui viene eseguito il programma:</span><span class="sxs-lookup"><span data-stu-id="3a367-367">Copy langs.txt to the directory from which the program will run:</span></span>

    -   <span data-ttu-id="3a367-368">Se eseguito da Visual Studio, copiarlo in *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.</span><span class="sxs-lookup"><span data-stu-id="3a367-368">If running from within Visual Studio, copy it to *ProjectRootDirectory*\\HelloMUI\\GuiStep\_2.</span></span>
    -   <span data-ttu-id="3a367-369">Se eseguito da Esplora risorse, copiarlo nella stessa directory di GuiStep \_2.exe.</span><span class="sxs-lookup"><span data-stu-id="3a367-369">If running from Windows Explorer, copy it to the same directory as GuiStep\_2.exe.</span></span>

5.  <span data-ttu-id="3a367-370">Compilare ed eseguire il progetto.</span><span class="sxs-lookup"><span data-stu-id="3a367-370">Build and run the project.</span></span> <span data-ttu-id="3a367-371">Provare a modificare langs.txt in modo che vengano visualizzate lingue diverse all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3a367-371">Try editing langs.txt so that different languages appear at the front of the list.</span></span>

## <a name="step-5-customizing-hello-mui"></a><span data-ttu-id="3a367-372">Passaggio 5: personalizzazione di "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="3a367-372">Step 5: Customizing "Hello MUI"</span></span>

<span data-ttu-id="3a367-373">Alcune delle funzionalità di run-time indicate finora in questa esercitazione sono disponibili solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3a367-373">A number of the run-time features mentioned so far within this tutorial are available only on Windows Vista and later.</span></span> <span data-ttu-id="3a367-374">Potrebbe essere necessario riutilizzare lo sforzo investito nella localizzazione e nella suddivisione delle risorse rendendo l'applicazione funzionante sulle versioni del sistema operativo Windows di livello inferiore, ad esempio Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a367-374">You may wish to re-use the effort invested in localizing and splitting resources by making the application work on downlevel Windows operating system versions, such as Windows XP.</span></span> <span data-ttu-id="3a367-375">Questo processo comporta la modifica dell'esempio precedente in due aree principali:</span><span class="sxs-lookup"><span data-stu-id="3a367-375">This process involves adjusting the previous example in two key areas:</span></span>

-   <span data-ttu-id="3a367-376">Le funzioni di caricamento delle risorse precedenti a Windows Vista, ad esempio [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)e altre, non sono compatibili con MUI.</span><span class="sxs-lookup"><span data-stu-id="3a367-376">The pre-Windows Vista resource loading functions (such as [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), and others) are non-MUI aware.</span></span> <span data-ttu-id="3a367-377">Le applicazioni fornite con le risorse divise (file in e MUI) devono caricare i moduli delle risorse usando una di queste due funzioni:</span><span class="sxs-lookup"><span data-stu-id="3a367-377">Applications that ship with split resources (LN and .mui files) must load resource modules using one of these two functions:</span></span>

    -   <span data-ttu-id="3a367-378">Se l'applicazione deve essere eseguita solo in Windows Vista e versioni successive, dovrebbe caricare i moduli delle risorse con [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span><span class="sxs-lookup"><span data-stu-id="3a367-378">If the application is to be run only on Windows Vista and later, it should load resource modules with [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span>
    -   <span data-ttu-id="3a367-379">Se l'applicazione deve essere eseguita nelle versioni precedenti a Windows Vista, oltre che in Windows Vista o versioni successive, è necessario utilizzare [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), che è una funzione di livello inferiore specificata in Windows 7 SDK.</span><span class="sxs-lookup"><span data-stu-id="3a367-379">If the application is to be run on versions prior to Windows Vista, as well as Windows Vista or later, it must use [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), which is a specific downlevel function provided in the Windows 7 SDK.</span></span>

-   <span data-ttu-id="3a367-380">Il supporto per la gestione delle lingue e gli ordini di fallback della lingua offerti nelle versioni precedenti a Windows Vista del sistema operativo Windows differisce significativamente da quello in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3a367-380">The language management and language fallback order support offered in pre-Windows Vista versions of the Windows operating system differs significantly from that in Windows Vista and later.</span></span> <span data-ttu-id="3a367-381">Per questo motivo, le applicazioni che consentono il fallback della lingua configurata dall'utente devono modificare le proprie procedure di gestione della lingua:</span><span class="sxs-lookup"><span data-stu-id="3a367-381">For this reason, applications that allow user-configured language fallback must adjust their language management practices:</span></span>

    -   <span data-ttu-id="3a367-382">Se l'applicazione deve essere eseguita solo in Windows Vista e versioni successive, è sufficiente impostare l'elenco di lingue utilizzando [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) .</span><span class="sxs-lookup"><span data-stu-id="3a367-382">If the application is to be run only on Windows Vista and later, setting the language list using [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) is sufficient.</span></span>
    -   <span data-ttu-id="3a367-383">Se l'applicazione deve essere eseguita in tutte le versioni di Windows, è necessario costruire il codice che verrà eseguito su piattaforme di livello inferiore per scorrere l'elenco di lingue configurato dall'utente e verificare il modulo di risorse desiderato.</span><span class="sxs-lookup"><span data-stu-id="3a367-383">If the application is to be run on all Windows versions, code must be constructed that will run on downlevel platforms to iterate through the user configured language list and probe for the desired resource module.</span></span> <span data-ttu-id="3a367-384">Questo può essere visualizzato nelle sezioni 1C e 2 del codice fornito più avanti in questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="3a367-384">This can be seen in sections 1c and 2 of the code provided later in this step.</span></span>

<span data-ttu-id="3a367-385">Creare un progetto in grado di usare i moduli di risorse localizzati in qualsiasi versione di Windows:</span><span class="sxs-lookup"><span data-stu-id="3a367-385">Create a project that can use the localized resource modules on any version of Windows:</span></span>

1.  <span data-ttu-id="3a367-386">Aggiungere un nuovo progetto alla soluzione HelloMUI (usando il menu file di selezione, Aggiungi e nuovo progetto) con i valori e le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a367-386">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="3a367-387">Tipo di progetto: progetto Win32.</span><span class="sxs-lookup"><span data-stu-id="3a367-387">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="3a367-388">Nome: GuiStep \_ 3.</span><span class="sxs-lookup"><span data-stu-id="3a367-388">Name: GuiStep\_3.</span></span>
    3.  <span data-ttu-id="3a367-389">Percorso: accettare il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3a367-389">Location: accept the default.</span></span>
    4.  <span data-ttu-id="3a367-390">Nella creazione guidata applicazione Win32 selezionare il tipo di applicazione predefinito: applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="3a367-390">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="3a367-391">Impostare questo progetto per l'esecuzione dall'interno di Visual Studio e configurarne il modello di Threading.</span><span class="sxs-lookup"><span data-stu-id="3a367-391">Set this project to run from within Visual Studio, and configure its threading model.</span></span> <span data-ttu-id="3a367-392">Inoltre, configurarlo per aggiungere le intestazioni e le librerie necessarie.</span><span class="sxs-lookup"><span data-stu-id="3a367-392">Also, configure it to add the necessary headers and libraries.</span></span>

    > [!Note]  
    > <span data-ttu-id="3a367-393">Nei percorsi usati in questa esercitazione si presuppone che il pacchetto Windows 7 SDK e le API NLS di livello inferiore siano stati installati nelle directory predefinite.</span><span class="sxs-lookup"><span data-stu-id="3a367-393">The paths used in this tutorial assume that the Windows 7 SDK and the Microsoft NLS downlevel APIs package were installed to their default directories.</span></span> <span data-ttu-id="3a367-394">In caso contrario, modificare i percorsi in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="3a367-394">If that is not the case, modify the paths appropriately.</span></span>

     

    1.  <span data-ttu-id="3a367-395">Nella Esplora soluzioni fare clic con il pulsante destro del mouse sul progetto GuiStep \_ 3 e selezionare Imposta come progetto di avvio.</span><span class="sxs-lookup"><span data-stu-id="3a367-395">In the Solution Explorer, right-click the project GuiStep\_3 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="3a367-396">Fare di nuovo clic con il pulsante destro del mouse e scegliere Proprietà.</span><span class="sxs-lookup"><span data-stu-id="3a367-396">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="3a367-397">Nella finestra di dialogo Pagine delle proprietà del progetto:</span><span class="sxs-lookup"><span data-stu-id="3a367-397">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="3a367-398">Nell'elenco a discesa in alto a sinistra impostare configurazione su tutte le configurazioni.</span><span class="sxs-lookup"><span data-stu-id="3a367-398">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="3a367-399">In proprietà di configurazione espandere C/C++, selezionare generazione codice e impostare libreria di runtime: debug multithread (/MTd).</span><span class="sxs-lookup"><span data-stu-id="3a367-399">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>
        3.  <span data-ttu-id="3a367-400">Selezionare generale e aggiungere a directory di inclusione aggiuntive:</span><span class="sxs-lookup"><span data-stu-id="3a367-400">Select General and add to Additional Include Directories:</span></span>

            -   <span data-ttu-id="3a367-401">"C: \\ API NLS di livello inferiore Microsoft \\ includono".</span><span class="sxs-lookup"><span data-stu-id="3a367-401">"C:\\Microsoft NLS Downlevel APIs\\Include".</span></span>

        4.  <span data-ttu-id="3a367-402">Selezionare la lingua e impostare considera WCHAR \_ t come tipo incorporato: No (/Zc: WCHAR \_ t-).</span><span class="sxs-lookup"><span data-stu-id="3a367-402">Select Language and set Treat wchar\_t as Built-in Type: No (/Zc:wchar\_t-).</span></span>
        5.  <span data-ttu-id="3a367-403">Selezionare Avanzate e impostare la convenzione di chiamata: \_ stdcall (/gz).</span><span class="sxs-lookup"><span data-stu-id="3a367-403">Select Advanced and set Calling Convention: \_stdcall (/Gz).</span></span>
        6.  <span data-ttu-id="3a367-404">In proprietà di configurazione espandere linker, selezionare input e aggiungere a dipendenze aggiuntive:</span><span class="sxs-lookup"><span data-stu-id="3a367-404">Under Configuration Properties expand Linker, select Input, and add to Additional Dependencies:</span></span>

            -   <span data-ttu-id="3a367-405">"C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ lib \\ MUILoad. lib".</span><span class="sxs-lookup"><span data-stu-id="3a367-405">"C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Lib\\MUILoad.lib".</span></span>
            -   <span data-ttu-id="3a367-406">"C: \\ API NLS di livello inferiore Microsoft \\ lib \\ x86 \\ nlsdl. lib".</span><span class="sxs-lookup"><span data-stu-id="3a367-406">"C:\\Microsoft NLS Downlevel APIs\\Lib\\x86\\Nlsdl.lib".</span></span>

3.  <span data-ttu-id="3a367-407">Sostituire il contenuto di GuiStep \_ 3. cpp con il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="3a367-407">Replace the contents of GuiStep\_3.cpp with the following code:</span></span>
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="3a367-408">Creare o copiare langs.txt nella directory appropriata, come descritto in precedenza in [Step 4: globalizzating "Hello MUI"](#step-4-globalizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="3a367-408">Create or copy langs.txt to the appropriate directory, as previously described in [Step 4: Globalizing "Hello MUI"](#step-4-globalizing-hello-mui).</span></span>
5.  <span data-ttu-id="3a367-409">Compilare ed eseguire il progetto.</span><span class="sxs-lookup"><span data-stu-id="3a367-409">Build and run the project.</span></span>

> [!Note]  
> <span data-ttu-id="3a367-410">Se l'applicazione deve essere eseguita nelle versioni di Windows precedenti a Windows Vista, assicurarsi di leggere i documenti forniti con il pacchetto di [API NLS](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) di livello inferiore di Microsoft per informazioni su come ridistribuire Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="3a367-410">If the application should run on Windows versions prior to Windows Vista, be sure to read the documents that came with the [Microsoft NLS downlevel APIs](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) package on how to redistribute Nlsdl.dll.</span></span>

 

## <a name="additional-considerations-for-mui"></a><span data-ttu-id="3a367-411">Considerazioni aggiuntive per MUI</span><span class="sxs-lookup"><span data-stu-id="3a367-411">Additional Considerations for MUI</span></span>

### <a name="support-for-console-applications"></a><span data-ttu-id="3a367-412">Supporto per le applicazioni console</span><span class="sxs-lookup"><span data-stu-id="3a367-412">Support for Console Applications</span></span>

<span data-ttu-id="3a367-413">Le tecniche descritte in questa esercitazione possono anche essere usate nelle applicazioni console.</span><span class="sxs-lookup"><span data-stu-id="3a367-413">The techniques covered in this tutorial can also be used in console applications.</span></span> <span data-ttu-id="3a367-414">Tuttavia, a differenza della maggior parte dei controlli GUI standard, la finestra di comando di Windows non può visualizzare caratteri per tutte le lingue.</span><span class="sxs-lookup"><span data-stu-id="3a367-414">However, unlike most standard GUI controls, the Windows command window cannot display characters for all languages.</span></span> <span data-ttu-id="3a367-415">Per questo motivo, le applicazioni console multilingue richiedono particolare attenzione.</span><span class="sxs-lookup"><span data-stu-id="3a367-415">For this reason, multilingual console applications require special attention.</span></span>

<span data-ttu-id="3a367-416">Chiamando le API [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) o [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) con flag di filtro specifici, le funzioni di caricamento delle risorse rimuovono i probe delle risorse della lingua per linguaggi specifici che in genere non sono visualizzati all'interno di una finestra di comando.</span><span class="sxs-lookup"><span data-stu-id="3a367-416">Calling the APIs [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) or [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) with specific filtering flags causes the resource loading functions to remove language resource probes for specific languages that are not normally displayed within a command window.</span></span> <span data-ttu-id="3a367-417">Quando questi flag sono impostati, gli algoritmi di impostazione della lingua consentono solo le lingue che verranno visualizzate correttamente nella finestra di comando affinché si trovino nell'elenco di fallback.</span><span class="sxs-lookup"><span data-stu-id="3a367-417">When these flags are set, the language-setting algorithms allow only those languages that will display properly in the command window to be on the fallback list.</span></span>

<span data-ttu-id="3a367-418">Per altre informazioni sull'uso di queste API per compilare un'applicazione console multilingue, vedere le sezioni Note di [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) e [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="3a367-418">For more information on using these APIs to build a multilingual console application, see the remarks sections of [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) and [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span>

### <a name="determination-of-languages-to-support-at-run-time"></a><span data-ttu-id="3a367-419">Determinazione delle lingue da supportare in Run-Time</span><span class="sxs-lookup"><span data-stu-id="3a367-419">Determination of Languages to Support at Run-Time</span></span>

<span data-ttu-id="3a367-420">È possibile adottare uno dei seguenti suggerimenti di progettazione per determinare le lingue che l'applicazione deve supportare in fase di esecuzione:</span><span class="sxs-lookup"><span data-stu-id="3a367-420">You can adopt one of the following design suggestions to determine which languages your application should support at run-time:</span></span>

-   <span data-ttu-id="3a367-421">**Durante l'installazione, consentire all'utente finale di selezionare la lingua preferita da un elenco di lingue supportate**</span><span class="sxs-lookup"><span data-stu-id="3a367-421">**During installation, enable the end user to select the preferred language from a list of supported languages**</span></span>

-   <span data-ttu-id="3a367-422">**Leggi un elenco di lingue da un file di configurazione**</span><span class="sxs-lookup"><span data-stu-id="3a367-422">**Read a language list from a configuration file**</span></span>

    <span data-ttu-id="3a367-423">Alcuni dei progetti in questa esercitazione contengono una funzione utilizzata per analizzare un file di configurazione langs.txt, che contiene un elenco di lingue.</span><span class="sxs-lookup"><span data-stu-id="3a367-423">Some of the projects in this tutorial contain a function used to parse a langs.txt configuration file, which contains a language list.</span></span>

    <span data-ttu-id="3a367-424">Poiché questa funzione accetta input esterno, convalidare le lingue fornite come input.</span><span class="sxs-lookup"><span data-stu-id="3a367-424">Because this function takes external input, validate the languages that are provided as input.</span></span> <span data-ttu-id="3a367-425">Per ulteriori informazioni sull'esecuzione di tale convalida, vedere le funzioni [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) o [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) .</span><span class="sxs-lookup"><span data-stu-id="3a367-425">See the [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) or [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) functions for more details on performing that validation.</span></span>

-   <span data-ttu-id="3a367-426">**Eseguire una query sul sistema operativo per determinare quali lingue sono installate**</span><span class="sxs-lookup"><span data-stu-id="3a367-426">**Query the operating system to determine which languages are installed**</span></span>

    <span data-ttu-id="3a367-427">Questo approccio consente all'applicazione di usare la stessa lingua del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3a367-427">This approach helps the application use the same language as the operating system.</span></span> <span data-ttu-id="3a367-428">Sebbene non richieda la richiesta dell'utente, se si sceglie questa opzione, tenere presente che le lingue del sistema operativo possono essere aggiunte o rimosse in qualsiasi momento e possono essere modificate dopo che l'utente ha installato l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-428">Although this does not require user prompting, if you choose this option, be aware that operating system languages can be added or removed at any time and can change after the user installs the application.</span></span> <span data-ttu-id="3a367-429">Tenere inoltre presente che in alcuni casi il sistema operativo viene installato con supporto di lingua limitato e l'applicazione offre un valore maggiore se supporta lingue non supportate dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3a367-429">Also, be aware that in some cases, the operating system is installed with limited language support, and the application offers more value if it supports languages that the operating system does not support.</span></span>

    <span data-ttu-id="3a367-430">Per ulteriori informazioni su come determinare le lingue attualmente installate nel sistema operativo, vedere la funzione [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .</span><span class="sxs-lookup"><span data-stu-id="3a367-430">For more information on how to determine the currently installed languages in the operating system, see the [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) function.</span></span>

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a><span data-ttu-id="3a367-431">Supporto per script complessi nelle versioni precedenti a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a367-431">Complex Script Support in Versions Prior to Windows Vista</span></span>

<span data-ttu-id="3a367-432">Quando un'applicazione che supporta alcuni script complessi viene eseguita in una versione di Windows precedente a Windows Vista, il testo in tale script potrebbe non essere visualizzato correttamente nei componenti della GUI.</span><span class="sxs-lookup"><span data-stu-id="3a367-432">When an application that supports certain complex scripts runs on a version of Windows prior to Windows Vista, text in that script may not display properly in GUI components.</span></span> <span data-ttu-id="3a367-433">Nel progetto di livello inferiore all'interno di questa esercitazione, ad esempio, gli script Hi-IN e TA-IN potrebbero non essere visualizzati nella finestra di messaggio a causa di problemi relativi all'elaborazione di script complessi e alla mancanza di tipi di carattere correlati.</span><span class="sxs-lookup"><span data-stu-id="3a367-433">For example, in the downlevel project within this tutorial, hi-IN and ta-IN scripts may not display in the message box due to issues with processing complex scripts and the lack of related fonts.</span></span> <span data-ttu-id="3a367-434">In genere, i problemi di questa natura si presentano come caselle quadrate nel componente GUI.</span><span class="sxs-lookup"><span data-stu-id="3a367-434">Normally, problems of this nature present themselves as square boxes in the GUI component.</span></span>

<span data-ttu-id="3a367-435">Per ulteriori informazioni su come abilitare l'elaborazione di script complessi, vedere [supporto di script e tipi di carattere in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a367-435">More information about how to enable complex script processing can be found at [Script and Font Support in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="3a367-436">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="3a367-436">Summary</span></span>

<span data-ttu-id="3a367-437">Questa esercitazione ha globalizzato un'applicazione monolingua e ha illustrato le procedure consigliate seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a367-437">This tutorial globalized a monolingual application and demonstrated the following best practices.</span></span>

-   <span data-ttu-id="3a367-438">Progettare l'applicazione per sfruttare il modello di risorse Win32.</span><span class="sxs-lookup"><span data-stu-id="3a367-438">Design the application to take advantage of the Win32 resource model.</span></span>
-   <span data-ttu-id="3a367-439">Utilizzare la suddivisione MUI delle risorse in file binari satellite (file con estensione MUI).</span><span class="sxs-lookup"><span data-stu-id="3a367-439">Utilize MUI splitting of resources into satellite binaries (.mui files).</span></span>
-   <span data-ttu-id="3a367-440">Verificare che il processo di localizzazione aggiorni le risorse nei file con estensione MUI per adattarle alla lingua di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-440">Ensure that the localization process updates the resources in the .mui files to be appropriate for the target language.</span></span>
-   <span data-ttu-id="3a367-441">Assicurarsi che la creazione di pacchetti e la distribuzione dell'applicazione, i file con estensione MUI associati e il contenuto della configurazione vengano eseguiti correttamente per consentire alle API di caricamento delle risorse di trovare il contenuto localizzato.</span><span class="sxs-lookup"><span data-stu-id="3a367-441">Ensure that packaging and deployment of the application, associated .mui files, and configuration content is done correctly to allow the resource loading APIs to find the localized content.</span></span>
-   <span data-ttu-id="3a367-442">Fornire all'utente finale un meccanismo per modificare la configurazione della lingua dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a367-442">Provide the end user a mechanism to adjust the language configuration of the application.</span></span>
-   <span data-ttu-id="3a367-443">Modificare il codice di runtime per sfruttare i vantaggi della configurazione del linguaggio, in modo da rendere l'applicazione più rispondente alle esigenze degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="3a367-443">Adjust the run-time code to take advantage of language configuration, to make the application more responsive to end user needs.</span></span>

 

 
