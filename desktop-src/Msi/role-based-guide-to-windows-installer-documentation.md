---
description: Windows Installer è la soluzione consigliata per l'installazione e la configurazione delle applicazioni in Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Guida basata sui ruoli per la documentazione di Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8a2138e963b6d29bd161df5e09144cf0cfd36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049700"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a><span data-ttu-id="ecbc2-103">Guida basata sui ruoli per la documentazione di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-103">Role-based Guide to Windows Installer Documentation</span></span>

<span data-ttu-id="ecbc2-104">Windows Installer è la soluzione consigliata per l'installazione e la configurazione delle applicazioni in Windows.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-104">Windows Installer is the recommended solution for the installation and setup of applications on Windows.</span></span> <span data-ttu-id="ecbc2-105">Pertanto, alcune delle informazioni contenute in questo SDK saranno di interesse per un'ampia gamma di sviluppatori di software e professionisti IT.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-105">Therefore, some of the information contained in this SDK will be of interest to a wide range of software development and IT professionals.</span></span> <span data-ttu-id="ecbc2-106">Questa sezione è costituita da una guida ai lettori che preferiscono visualizzare collegamenti ad argomenti organizzati in base al ruolo professionale e agli scenari di attività comuni.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-106">This section is provided as a guide to readers who prefer to see links to topics organized by professional role and common task scenarios.</span></span> <span data-ttu-id="ecbc2-107">Poiché i ruoli possono differire molto tra le organizzazioni, il raggruppamento seguente dovrebbe essere considerato solo come una guida a una posizione per iniziare a cercare le informazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-107">Because roles can differ greatly between organizations, the following grouping should only be considered as a guide to a location to start searching for the information you need.</span></span>

-   [<span data-ttu-id="ecbc2-108">Sviluppatori di applicazioni</span><span class="sxs-lookup"><span data-stu-id="ecbc2-108">Application Developers</span></span>](#application-developers)
-   [<span data-ttu-id="ecbc2-109">Autori installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-109">Setup Authors</span></span>](#setup-authors)
-   [<span data-ttu-id="ecbc2-110">Professionisti IT</span><span class="sxs-lookup"><span data-stu-id="ecbc2-110">IT Professionals</span></span>](#it-professionals)
-   [<span data-ttu-id="ecbc2-111">Sviluppatori di infrastrutture</span><span class="sxs-lookup"><span data-stu-id="ecbc2-111">Infrastructure Developers</span></span>](#infrastructure-developers)

<span data-ttu-id="ecbc2-112">Questa documentazione è destinata agli sviluppatori di software che desiderano creare applicazioni che utilizzano Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-112">This documentation is intended for software developers who want to make applications that use Windows Installer.</span></span> <span data-ttu-id="ecbc2-113">Come origine principale del materiale di riferimento per il programma di installazione, l'SDK fornisce informazioni sui pacchetti di installazione e il servizio del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-113">As the primary source of reference material for the installer, the SDK provides information about installation packages and the installer service.</span></span> <span data-ttu-id="ecbc2-114">Contiene descrizioni complete del Application Programming Interface (API) e degli elementi del database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-114">It contains complete descriptions of the application programming interface (API) and the elements of the installer database.</span></span>

<span data-ttu-id="ecbc2-115">Per ulteriori informazioni, vedere [altre origini di Windows Installer informazioni](other-sources-of-windows-installer-information.md).</span><span class="sxs-lookup"><span data-stu-id="ecbc2-115">For more information, see [Other Sources of Windows Installer Information](other-sources-of-windows-installer-information.md).</span></span>

## <a name="application-developers"></a><span data-ttu-id="ecbc2-116">Sviluppatori di applicazioni</span><span class="sxs-lookup"><span data-stu-id="ecbc2-116">Application Developers</span></span>

<span data-ttu-id="ecbc2-117">Gli sviluppatori di applicazioni creano applicazioni che chiamano il Windows Installer Application Programming Interface e installano i pacchetti di Windows Installer in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-117">Application developers create applications that call the Windows Installer application programming interface and install Windows installer packages at run time.</span></span> <span data-ttu-id="ecbc2-118">Il Windows Installer può funzionare in un'applicazione, ad esempio la riparazione automatica e l'installazione su richiesta.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-118">The Windows Installer can do work in an application such as self-repair and installation-on-demand.</span></span> <span data-ttu-id="ecbc2-119">In genere, gli sviluppatori di applicazioni eseguono le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-119">Typically, application Developers do the following:</span></span>

-   <span data-ttu-id="ecbc2-120">Consente l'installazione su richiesta di applicazioni in fase di esecuzione da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-120">Enable installation-on-demand of applications at run time from within another application.</span></span>

    <span data-ttu-id="ecbc2-121">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-121">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-122">Uso delle funzioni del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-122">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="ecbc2-123">Riferimento alla funzione Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-123">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="ecbc2-124">Installazione su richiesta</span><span class="sxs-lookup"><span data-stu-id="ecbc2-124">Installation-On-Demand</span></span>](installation-on-demand.md)
    -   [<span data-ttu-id="ecbc2-125">Gestione dei componenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-125">Component Management</span></span>](component-management.md)
    -   [<span data-ttu-id="ecbc2-126">Modifica dei collegamenti del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-126">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="ecbc2-127">**Proprietà OLEAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-127">**OLEAdvtSupport Property**</span></span>](oleadvtsupport.md)
    -   [<span data-ttu-id="ecbc2-128">Supporto della piattaforma per gli annunci</span><span class="sxs-lookup"><span data-stu-id="ecbc2-128">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)

-   <span data-ttu-id="ecbc2-129">Abilitare la riparazione automatica delle applicazioni reinstallando i componenti in base alle esigenze in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-129">Enable self-repair of applications by reinstalling components as needed at run time.</span></span>

    <span data-ttu-id="ecbc2-130">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-130">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-131">Uso delle funzioni del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-131">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="ecbc2-132">Riferimento alla funzione Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-132">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="ecbc2-133">Resilienza</span><span class="sxs-lookup"><span data-stu-id="ecbc2-133">Resiliency</span></span>](resiliency.md)
    -   [<span data-ttu-id="ecbc2-134">Resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="ecbc2-134">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="ecbc2-135">Ricerca di una funzionalità o di un componente danneggiato</span><span class="sxs-lookup"><span data-stu-id="ecbc2-135">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="ecbc2-136">Sostituzione dei file esistenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-136">Replacing Existing Files</span></span>](replacing-existing-files.md)

-   <span data-ttu-id="ecbc2-137">Consente di visualizzare un'interfaccia utente per raccogliere informazioni sull'utente e preferenze di configurazione la prima volta che un'applicazione viene installata o eseguita.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-137">Display a user interface to collect user information and configuration preferences the first time an application is installed or run.</span></span> <span data-ttu-id="ecbc2-138">L'interfaccia utente deve essere aggiunta dall'autore del programma di installazione del pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-138">The user interface must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="ecbc2-139">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-139">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-140">Uso delle funzioni del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-140">Using Installer Functions</span></span>](using-installer-functions.md)
    -   [<span data-ttu-id="ecbc2-141">Inizializzazione di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-141">Initializing an Application</span></span>](initializing-an-application.md)
    -   [<span data-ttu-id="ecbc2-142">Finestra di dialogo FirstRun</span><span class="sxs-lookup"><span data-stu-id="ecbc2-142">FirstRun Dialog</span></span>](firstrun-dialog.md)
    -   [<span data-ttu-id="ecbc2-143">Informazioni sull'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-143">About the User Interface</span></span>](about-the-user-interface.md)

-   <span data-ttu-id="ecbc2-144">Creare applicazioni che utilizzano un modello di riferimento indiretto per fare riferimento ai componenti con funzionalità parallele.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-144">Create applications that use an indirection model to refer to components with parallel functionality.</span></span> <span data-ttu-id="ecbc2-145">Le categorie di componenti qualificate devono essere aggiunte dall'autore del programma di installazione del pacchetto Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-145">The qualified component categories must be added by the Setup Author of the Windows Installer package.</span></span>

    <span data-ttu-id="ecbc2-146">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-146">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-147">Componenti qualificati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-147">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="ecbc2-148">Utilizzo di componenti qualificati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-148">Using Qualified Components</span></span>](using-qualified-components.md)

-   <span data-ttu-id="ecbc2-149">Usare gli assembly privati e affiancati per isolare le applicazioni e ridurre i conflitti di DLL.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-149">Use private and side-by-side assemblies to isolate applications and reduce DLL conflicts.</span></span>

    <span data-ttu-id="ecbc2-150">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-150">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-151">Assembly</span><span class="sxs-lookup"><span data-stu-id="ecbc2-151">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="ecbc2-152">Chiavi del registro di sistema dell'assembly scritte da Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-152">Assembly Registry Keys Written by Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="ecbc2-153">Installazione degli assembly Win32 per la condivisione side-by-side in Windows XP</span><span class="sxs-lookup"><span data-stu-id="ecbc2-153">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [<span data-ttu-id="ecbc2-154">Installazione di assembly Win32 per l'utilizzo privato di un'applicazione in Windows XP</span><span class="sxs-lookup"><span data-stu-id="ecbc2-154">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [<span data-ttu-id="ecbc2-155">Tabella MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="ecbc2-155">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="ecbc2-156">Tabella MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="ecbc2-156">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="ecbc2-157">**MsiProvideAssembly**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-157">**MsiProvideAssembly**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [<span data-ttu-id="ecbc2-158">**Proprietà MsiWin32AssemblySupport**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-158">**MsiWin32AssemblySupport Property**</span></span>](msiwin32assemblysupport.md)
    -   [<span data-ttu-id="ecbc2-159">**Proprietà MsiNetAssemblySupport**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-159">**MsiNetAssemblySupport Property**</span></span>](msinetassemblysupport.md)
    -   [<span data-ttu-id="ecbc2-160">**Componenti isolati**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-160">**Isolated Components**</span></span>](isolated-components.md)

-   <span data-ttu-id="ecbc2-161">Preparare l'applicazione per l'installazione degli aggiornamenti principali completi.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-161">Prepare the application to install its own comprehensive major upgrades.</span></span>

    <span data-ttu-id="ecbc2-162">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-162">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-163">Applicazione di patch e aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-163">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="ecbc2-164">Aggiornamenti principali</span><span class="sxs-lookup"><span data-stu-id="ecbc2-164">Major Upgrades</span></span>](major-upgrades.md)
    -   [<span data-ttu-id="ecbc2-165">**Proprietà UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-165">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="ecbc2-166">**Uso di un UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-166">**Using an UpgradeCode**</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="ecbc2-167">Impedire l'installazione di un pacchetto obsoleto in una versione più recente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-167">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   <span data-ttu-id="ecbc2-168">Preparare l'applicazione per l'installazione di aggiornamenti secondari, piccoli aggiornamenti o correzioni.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-168">Prepare the application to install its own minor upgrades, small updates, or fixes.</span></span>

    <span data-ttu-id="ecbc2-169">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-169">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-170">Applicazione di patch e aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-170">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="ecbc2-171">Aggiornamenti di piccole dimensioni</span><span class="sxs-lookup"><span data-stu-id="ecbc2-171">Small Updates</span></span>](small-updates.md)
    -   [<span data-ttu-id="ecbc2-172">Aggiornamenti secondari</span><span class="sxs-lookup"><span data-stu-id="ecbc2-172">Minor Upgrades</span></span>](minor-upgrades.md)

-   <span data-ttu-id="ecbc2-173">Organizzare le risorse dell'applicazione in componenti che possono funzionare con la Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-173">Organize application resources into components that can work with the Windows Installer.</span></span>

    <span data-ttu-id="ecbc2-174">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-174">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-175">Componenti Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-175">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="ecbc2-176">Utilizzo delle funzionalità e dei componenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-176">Working with Features and Components</span></span>](working-with-features-and-components.md)
    -   [<span data-ttu-id="ecbc2-177">Utilizzo di componenti transitivi</span><span class="sxs-lookup"><span data-stu-id="ecbc2-177">Using Transitive Components</span></span>](using-transitive-components.md)
    -   [<span data-ttu-id="ecbc2-178">Cosa accade se le regole dei componenti sono interrotte?</span><span class="sxs-lookup"><span data-stu-id="ecbc2-178">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="ecbc2-179">Organizzazione di applicazioni in componenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-179">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="ecbc2-180">Componenti isolati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-180">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="ecbc2-181">Componenti qualificati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-181">Qualified Components</span></span>](qualified-components.md)

## <a name="setup-authors"></a><span data-ttu-id="ecbc2-182">Autori installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-182">Setup Authors</span></span>

<span data-ttu-id="ecbc2-183">Gli autori del programma di installazione creano pacchetti di Windows Installer (file con estensione msi) che contengono la logica di installazione e le informazioni necessarie per installare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-183">Setup Authors create Windows Installer packages (.msi files) that contain the setup logic and information needed to install an application.</span></span> <span data-ttu-id="ecbc2-184">In genere usano strumenti di creazione, ad esempio [Orca.exe](orca-exe.md) per popolare il database Windows Installer con le informazioni e la logica di installazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-184">They typically use authoring tools such as [Orca.exe](orca-exe.md) to populate the Windows Installer database with the setup logic and information.</span></span> <span data-ttu-id="ecbc2-185">In genere, gli autori del programma di installazione eseguono le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-185">Typically, Setup Authors do the following:</span></span>

-   <span data-ttu-id="ecbc2-186">Determinare le funzionalità disponibili con diverse versioni di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-186">Determine the functionality available with different Windows Installer versions.</span></span>

    <span data-ttu-id="ecbc2-187">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-187">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-188">Determinazione della versione di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-188">Determining the Windows Installer Version</span></span>](determining-the-windows-installer-version.md)
    -   [<span data-ttu-id="ecbc2-189">Versioni rilasciate di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-189">Released Versions of Windows Installer</span></span>](released-versions-of-windows-installer.md)
    -   [<span data-ttu-id="ecbc2-190">Novità di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-190">What's New in Windows Installer</span></span>](what-s-new-in-windows-installer.md)

-   <span data-ttu-id="ecbc2-191">Organizzare le risorse dell'applicazione in componenti Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-191">Organize application resources into Windows Installer components.</span></span>

    <span data-ttu-id="ecbc2-192">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-192">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-193">Componenti Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-193">Windows Installer Components</span></span>](windows-installer-components.md)
    -   [<span data-ttu-id="ecbc2-194">Organizzazione di applicazioni in componenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-194">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)
    -   [<span data-ttu-id="ecbc2-195">Modifica del codice componente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-195">Changing the Component Code</span></span>](changing-the-component-code.md)
    -   [<span data-ttu-id="ecbc2-196">Cosa accade se le regole dei componenti sono interrotte?</span><span class="sxs-lookup"><span data-stu-id="ecbc2-196">What happens if the component rules are broken?</span></span>](what-happens-if-the-component-rules-are-broken.md)
    -   [<span data-ttu-id="ecbc2-197">Esempi di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-197">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="ecbc2-198">Utilizzare strumenti di creazione di pacchetti Windows Installer o strumenti SDK di terze parti, ad esempio [Orca.exe](orca-exe.md) per popolare un database di installazione e creare un pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-198">Use third-party Windows Installer package authoring tools or SDK tools such as [Orca.exe](orca-exe.md) to populate an installation database and create a Windows Installer package.</span></span>

    <span data-ttu-id="ecbc2-199">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-199">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-200">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-200">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="ecbc2-201">Pacchetto di installazione, informazioni sul database del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-201">Installation Package, About the Installer Database</span></span>](installation-package.md)
    -   [<span data-ttu-id="ecbc2-202">Estensioni di file Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-202">Windows Installer File Extensions</span></span>](windows-installer-file-extensions.md)
    -   [<span data-ttu-id="ecbc2-203">Tabelle di database</span><span class="sxs-lookup"><span data-stu-id="ecbc2-203">Database Tables</span></span>](database-tables.md)
    -   [<span data-ttu-id="ecbc2-204">Codici del pacchetto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-204">Package Codes</span></span>](package-codes.md)
    -   [<span data-ttu-id="ecbc2-205">Creazione di un pacchetto di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="ecbc2-205">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="ecbc2-206">Windows Installer su sistemi operativi a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ecbc2-206">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="ecbc2-207">Denominazione di tabelle, proprietà e azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="ecbc2-207">Naming Custom Tables, Properties, and Actions</span></span>](naming-custom-tables-properties-and-actions.md)
    -   [<span data-ttu-id="ecbc2-208">Limitazioni OLE sui flussi</span><span class="sxs-lookup"><span data-stu-id="ecbc2-208">OLE Limitations on Streams</span></span>](ole-limitations-on-streams.md)
    -   [<span data-ttu-id="ecbc2-209">Formato della definizione di colonna</span><span class="sxs-lookup"><span data-stu-id="ecbc2-209">Column Definition Format</span></span>](column-definition-format.md)
    -   [<span data-ttu-id="ecbc2-210">Riduzione delle dimensioni di un file con estensione msi</span><span class="sxs-lookup"><span data-stu-id="ecbc2-210">Reducing the Size of an .msi File</span></span>](reducing-the-size-of-an--msi-file.md)

-   <span data-ttu-id="ecbc2-211">Creare il database di Windows Installer per installare i file.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-211">Author the Windows Installer database to install files.</span></span>

    <span data-ttu-id="ecbc2-212">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-212">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-213">Gruppo di tabelle Core</span><span class="sxs-lookup"><span data-stu-id="ecbc2-213">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="ecbc2-214">Gruppo di tabelle file</span><span class="sxs-lookup"><span data-stu-id="ecbc2-214">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="ecbc2-215">Tabella file</span><span class="sxs-lookup"><span data-stu-id="ecbc2-215">File Table</span></span>](file-table.md)
    -   [<span data-ttu-id="ecbc2-216">Ricerca file</span><span class="sxs-lookup"><span data-stu-id="ecbc2-216">File Searching</span></span>](file-searching.md)
    -   [<span data-ttu-id="ecbc2-217">Costo file</span><span class="sxs-lookup"><span data-stu-id="ecbc2-217">File Costing</span></span>](file-costing.md)
    -   [<span data-ttu-id="ecbc2-218">Installazione file</span><span class="sxs-lookup"><span data-stu-id="ecbc2-218">File Installation</span></span>](file-installation.md)
    -   [<span data-ttu-id="ecbc2-219">File complementari</span><span class="sxs-lookup"><span data-stu-id="ecbc2-219">Companion Files</span></span>](companion-files.md)
    -   [<span data-ttu-id="ecbc2-220">Regole di controllo delle versioni dei file</span><span class="sxs-lookup"><span data-stu-id="ecbc2-220">File Versioning Rules</span></span>](file-versioning-rules.md)
    -   [<span data-ttu-id="ecbc2-221">Controllo delle versioni dei file predefinito</span><span class="sxs-lookup"><span data-stu-id="ecbc2-221">Default File Versioning</span></span>](default-file-versioning.md)
    -   [<span data-ttu-id="ecbc2-222">Sostituzione dei file esistenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-222">Replacing Existing Files</span></span>](replacing-existing-files.md)
    -   [<span data-ttu-id="ecbc2-223">Uso di cabinet e origini compresse</span><span class="sxs-lookup"><span data-stu-id="ecbc2-223">Using Cabinets and Compressed Sources</span></span>](using-cabinets-and-compressed-sources.md)
    -   [<span data-ttu-id="ecbc2-224">Rimozione di file bloccati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-224">Removing Stranded Files</span></span>](removing-stranded-files.md)
    -   [<span data-ttu-id="ecbc2-225">Installazione di componenti permanenti, file, tipi di carattere, chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-225">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="ecbc2-226">Tabella FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="ecbc2-226">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
    -   [<span data-ttu-id="ecbc2-227">Ricerca di un file e creazione di una proprietà che contiene il percorso del file</span><span class="sxs-lookup"><span data-stu-id="ecbc2-227">Searching for a File and Creating a Property Holding the File's Path</span></span>](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [<span data-ttu-id="ecbc2-228">Ricerca di una directory e di un file nella directory</span><span class="sxs-lookup"><span data-stu-id="ecbc2-228">Searching for a Directory and a File in the Directory</span></span>](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [<span data-ttu-id="ecbc2-229">Esempi di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-229">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="ecbc2-230">Creare un database di Windows Installer che installa una struttura di directory e le cartelle.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-230">Author a Windows Installer database that installs a directory structure and folders.</span></span>

    <span data-ttu-id="ecbc2-231">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-231">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-232">Gruppo di tabelle Core</span><span class="sxs-lookup"><span data-stu-id="ecbc2-232">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="ecbc2-233">Gruppo di tabelle file</span><span class="sxs-lookup"><span data-stu-id="ecbc2-233">File Tables Group</span></span>](file-tables-group.md)
    -   [<span data-ttu-id="ecbc2-234">Tabella componenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-234">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="ecbc2-235">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="ecbc2-235">Directory Table</span></span>](directory-table.md)
    -   [<span data-ttu-id="ecbc2-236">Uso della tabella di directory</span><span class="sxs-lookup"><span data-stu-id="ecbc2-236">Using the Directory Table</span></span>](using-the-directory-table.md)
    -   [<span data-ttu-id="ecbc2-237">Utilizzo di una proprietà di directory in un percorso</span><span class="sxs-lookup"><span data-stu-id="ecbc2-237">Using a Directory Property in a Path</span></span>](using-a-directory-property-in-a-path.md)
    -   [<span data-ttu-id="ecbc2-238">Proprietà cartella di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-238">System Folder Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="ecbc2-239">Tabella CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ecbc2-239">CreateFolder Table</span></span>](createfolder-table.md)
    -   [<span data-ttu-id="ecbc2-240">Tabella LockPermissions</span><span class="sxs-lookup"><span data-stu-id="ecbc2-240">LockPermissions Table</span></span>](lockpermissions-table.md)
    -   [<span data-ttu-id="ecbc2-241">Tabella MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="ecbc2-241">MsiLockPermissionsEx Table</span></span>](msilockpermissionsex-table.md)
    -   [<span data-ttu-id="ecbc2-242">Modifica del percorso di destinazione per una directory</span><span class="sxs-lookup"><span data-stu-id="ecbc2-242">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="ecbc2-243">Esempi di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-243">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="ecbc2-244">Creare un database di Windows Installer che installa le chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-244">Author a Windows Installer database that installs registry keys.</span></span>

    <span data-ttu-id="ecbc2-245">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-245">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-246">Gruppo di tabelle Core</span><span class="sxs-lookup"><span data-stu-id="ecbc2-246">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="ecbc2-247">Gruppo di tabelle del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-247">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="ecbc2-248">Tabella del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-248">Registry Table</span></span>](registry-table.md)
    -   [<span data-ttu-id="ecbc2-249">Modifica del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-249">Modifying the Registry</span></span>](modifying-the-registry.md)
    -   [<span data-ttu-id="ecbc2-250">Aggiunta o rimozione di chiavi del registro di sistema durante l'installazione o la rimozione di componenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-250">Adding or Removing Registry Keys on the Installation or Removal of Components</span></span>](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [<span data-ttu-id="ecbc2-251">Aggiunta e rimozione di un'applicazione senza traccia nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-251">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="ecbc2-252">Installazione di componenti permanenti, file, tipi di carattere, chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-252">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
    -   [<span data-ttu-id="ecbc2-253">Ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-253">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [<span data-ttu-id="ecbc2-254">Ricerca di una voce del registro di sistema e creazione di una proprietà contenente il valore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-254">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [<span data-ttu-id="ecbc2-255">Chiavi del registro di sistema dell'assembly scritte dal Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-255">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="ecbc2-256">Disinstalla chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-256">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
    -   [<span data-ttu-id="ecbc2-257">Tabella SelfReg</span><span class="sxs-lookup"><span data-stu-id="ecbc2-257">SelfReg Table</span></span>](selfreg-table.md)
    -   [<span data-ttu-id="ecbc2-258">Specifica dell'ordine di registrazione automatica</span><span class="sxs-lookup"><span data-stu-id="ecbc2-258">Specifying the Order of Self Registration</span></span>](specifying-the-order-of-self-registration.md)
    -   [<span data-ttu-id="ecbc2-259">Esempi di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-259">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="ecbc2-260">Creare un database di Windows Installer che installa i servizi.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-260">Author a Windows Installer database that installs services.</span></span>

    <span data-ttu-id="ecbc2-261">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-261">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-262">Tabella ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="ecbc2-262">ServiceInstall Table</span></span>](serviceinstall-table.md)
    -   [<span data-ttu-id="ecbc2-263">Tabella ServiceControl</span><span class="sxs-lookup"><span data-stu-id="ecbc2-263">ServiceControl Table</span></span>](servicecontrol-table.md)
    -   [<span data-ttu-id="ecbc2-264">Tabella componenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-264">Component Table</span></span>](component-table.md)

-   <span data-ttu-id="ecbc2-265">Creare un database di Windows Installer che installa componenti isolati o componenti COM.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-265">Author a Windows Installer database that installs isolated components or COM components.</span></span>

    <span data-ttu-id="ecbc2-266">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-266">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-267">Gruppo di tabelle del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-267">Registry Tables Group</span></span>](registry-tables-group.md)
    -   [<span data-ttu-id="ecbc2-268">Tabella classi</span><span class="sxs-lookup"><span data-stu-id="ecbc2-268">Class Table</span></span>](class-table.md)
    -   [<span data-ttu-id="ecbc2-269">Tabella ComPlus</span><span class="sxs-lookup"><span data-stu-id="ecbc2-269">Complus Table</span></span>](complus-table.md)
    -   [<span data-ttu-id="ecbc2-270">Componenti isolati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-270">Isolated Components</span></span>](isolated-components.md)
    -   [<span data-ttu-id="ecbc2-271">Utilizzo di componenti isolati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-271">Using Isolated Components</span></span>](using-isolated-components.md)
    -   [<span data-ttu-id="ecbc2-272">Installazione di componenti isolati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-272">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
    -   [<span data-ttu-id="ecbc2-273">Reinstallazione dei componenti isolati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-273">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
    -   [<span data-ttu-id="ecbc2-274">Rimozione di componenti isolati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-274">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
    -   [<span data-ttu-id="ecbc2-275">Installazione di un componente COM in un percorso privato</span><span class="sxs-lookup"><span data-stu-id="ecbc2-275">Installing a COM Component to a Private Location</span></span>](installing-a-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="ecbc2-276">Rendere privato un componente COM in un pacchetto esistente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-276">Make a COM Component in an Existing Package Private</span></span>](make-a-com-component-in-an-existing-package-private.md)
    -   [<span data-ttu-id="ecbc2-277">Installazione di un'applicazione COM+ con la Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-277">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
    -   [<span data-ttu-id="ecbc2-278">Installazione di un componente non COM in una posizione privata</span><span class="sxs-lookup"><span data-stu-id="ecbc2-278">Installing a non-COM Component to a Private Location</span></span>](installing-a-non-com-component-to-a-private-location.md)
    -   [<span data-ttu-id="ecbc2-279">Creare un componente non COM in un pacchetto esistente privato</span><span class="sxs-lookup"><span data-stu-id="ecbc2-279">Make a non-COM Component in an Existing Package Private</span></span>](make-a-non-com-component-in-an-existing-package-private.md)

-   <span data-ttu-id="ecbc2-280">Consente di creare un database Windows Installer per l'installazione degli assembly.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-280">Author a Windows Installer database that installs assemblies.</span></span>

    <span data-ttu-id="ecbc2-281">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-281">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-282">Tabella MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="ecbc2-282">MsiAssembly Table</span></span>](msiassembly-table.md)
    -   [<span data-ttu-id="ecbc2-283">Tabella MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="ecbc2-283">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)
    -   [<span data-ttu-id="ecbc2-284">Assembly</span><span class="sxs-lookup"><span data-stu-id="ecbc2-284">Assemblies</span></span>](assemblies.md)
    -   [<span data-ttu-id="ecbc2-285">Chiavi del registro di sistema dell'assembly scritte dal Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-285">Assembly Registry Keys Written by the Windows Installer</span></span>](assembly-registry-keys-written-by-windows-installer-.md)
    -   [<span data-ttu-id="ecbc2-286">Installazione degli assembly Win32</span><span class="sxs-lookup"><span data-stu-id="ecbc2-286">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)

-   <span data-ttu-id="ecbc2-287">Creazione di un database di Windows Installer che consente di installare driver e convertitori ODBC.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-287">Author a Windows Installer database that installs ODBC drivers and translators.</span></span>

    <span data-ttu-id="ecbc2-288">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-288">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-289">Tabella ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="ecbc2-289">ODBCAttribute Table</span></span>](odbcattribute-table.md)
    -   [<span data-ttu-id="ecbc2-290">Tabella ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="ecbc2-290">ODBCDriver Table</span></span>](odbcdriver-table.md)
    -   [<span data-ttu-id="ecbc2-291">Tabella ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="ecbc2-291">ODBCTranslator Table</span></span>](odbctranslator-table.md)
    -   [<span data-ttu-id="ecbc2-292">Tabella ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="ecbc2-292">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
    -   [<span data-ttu-id="ecbc2-293">Tabella ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="ecbc2-293">ODBCSourceAttribute Table</span></span>](odbcsourceattribute-table.md)

-   <span data-ttu-id="ecbc2-294">Creare un database di Windows Installer che installa MIME.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-294">Author a Windows Installer database that installs MIME.</span></span>

    <span data-ttu-id="ecbc2-295">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-295">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-296">Tabella MIME</span><span class="sxs-lookup"><span data-stu-id="ecbc2-296">MIME Table</span></span>](mime-table.md)
    -   [<span data-ttu-id="ecbc2-297">Tabella di estensione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-297">Extension Table</span></span>](extension-table.md)
    -   [<span data-ttu-id="ecbc2-298">Modifica del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-298">Modifying the Registry</span></span>](modifying-the-registry.md)

-   <span data-ttu-id="ecbc2-299">Creazione di un database di Windows Installer per l'installazione delle variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-299">Author a Windows Installer database that installs environment variables.</span></span>

    <span data-ttu-id="ecbc2-300">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-300">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-301">Tabella ambiente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-301">Environment Table</span></span>](environment-table.md)

-   <span data-ttu-id="ecbc2-302">Creare un database di Windows Installer che installa i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-302">Author a Windows Installer database that installs shortcuts.</span></span>

    <span data-ttu-id="ecbc2-303">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-303">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-304">Tabella di collegamento</span><span class="sxs-lookup"><span data-stu-id="ecbc2-304">Shortcut Table</span></span>](shortcut-table.md)
    -   [<span data-ttu-id="ecbc2-305">Tabella MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="ecbc2-305">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
    -   [<span data-ttu-id="ecbc2-306">Modifica dei collegamenti del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-306">Editing Installer Shortcuts</span></span>](editing-installer-shortcuts.md)
    -   [<span data-ttu-id="ecbc2-307">Esempi di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-307">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="ecbc2-308">Creare un database di Windows Installer che installa più istanze di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-308">Author a Windows Installer database that installs multiple instances of applications.</span></span>

    <span data-ttu-id="ecbc2-309">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-309">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-310">Installazione di più istanze di prodotti e patch</span><span class="sxs-lookup"><span data-stu-id="ecbc2-310">Installing Multiple Instances of Products and Patches</span></span>](installing-multiple-instances-of-products-and-patches.md)
    -   [<span data-ttu-id="ecbc2-311">Creazione di più istanze con le trasformazioni dell'istanza</span><span class="sxs-lookup"><span data-stu-id="ecbc2-311">Authoring Multiple Instances with Instance Transforms</span></span>](authoring-multiple-instances-with-instance-transforms.md)
    -   [<span data-ttu-id="ecbc2-312">Installazione di più istanze con le trasformazioni dell'istanza</span><span class="sxs-lookup"><span data-stu-id="ecbc2-312">Installing Multiple Instances with Instance Transforms</span></span>](installing-multiple-instances-with-instance-transforms.md)

-   <span data-ttu-id="ecbc2-313">Specificare gli Stati e le opzioni di selezione delle funzionalità predefinite.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-313">Specify default feature selection states and options.</span></span>

    <span data-ttu-id="ecbc2-314">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-314">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-315">Gruppo di tabelle Core</span><span class="sxs-lookup"><span data-stu-id="ecbc2-315">Core Tables Group</span></span>](core-tables-group.md)
    -   [<span data-ttu-id="ecbc2-316">Tabella componenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-316">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="ecbc2-317">Tabella delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="ecbc2-317">Feature Table</span></span>](feature-table.md)
    -   [<span data-ttu-id="ecbc2-318">Tabella FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="ecbc2-318">FeatureComponents Table</span></span>](featurecomponents-table.md)
    -   [<span data-ttu-id="ecbc2-319">Controllo degli Stati di selezione delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="ecbc2-319">Controlling Feature Selection States</span></span>](controlling-feature-selection-states.md)
    -   [<span data-ttu-id="ecbc2-320">Proprietà opzioni di installazione funzionalità</span><span class="sxs-lookup"><span data-stu-id="ecbc2-320">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="ecbc2-321">Specificare le condizioni che devono essere soddisfatte per installare un'applicazione o i componenti selezionati.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-321">Specify conditions that must be met to install an application or selected components.</span></span>

    <span data-ttu-id="ecbc2-322">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-322">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-323">Tabella Condition</span><span class="sxs-lookup"><span data-stu-id="ecbc2-323">Condition Table</span></span>](condition-table.md)
    -   [<span data-ttu-id="ecbc2-324">Tabella LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="ecbc2-324">LaunchCondition Table</span></span>](launchcondition-table.md)
    -   [<span data-ttu-id="ecbc2-325">Tabella componenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-325">Component Table</span></span>](component-table.md)
    -   [<span data-ttu-id="ecbc2-326">Uso delle proprietà nelle istruzioni condizionali</span><span class="sxs-lookup"><span data-stu-id="ecbc2-326">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="ecbc2-327">Sintassi dell'istruzione condizionale</span><span class="sxs-lookup"><span data-stu-id="ecbc2-327">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="ecbc2-328">Esecuzione delle azioni di condizionamento durante la rimozione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-328">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="ecbc2-329">Esempi di sintassi di istruzioni condizionali</span><span class="sxs-lookup"><span data-stu-id="ecbc2-329">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)

-   <span data-ttu-id="ecbc2-330">Consente di creare la sequenza di azioni utilizzata per installare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-330">Author the sequence of actions used to install the application.</span></span>

    <span data-ttu-id="ecbc2-331">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-331">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-332">Utilizzo di una tabella di sequenza</span><span class="sxs-lookup"><span data-stu-id="ecbc2-332">Using a Sequence Table</span></span>](using-a-sequence-table.md)
    -   [<span data-ttu-id="ecbc2-333">Gruppo tabelle procedure di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-333">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)
    -   [<span data-ttu-id="ecbc2-334">Esempio dettagliato della tabella Sequence</span><span class="sxs-lookup"><span data-stu-id="ecbc2-334">Sequence Table Detailed Example</span></span>](sequence-table-detailed-example.md)
    -   [<span data-ttu-id="ecbc2-335">Azioni con restrizioni di sequenziazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-335">Actions with Sequencing Restrictions</span></span>](actions-with-sequencing-restrictions.md)
    -   [<span data-ttu-id="ecbc2-336">Azioni senza restrizioni di sequenziazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-336">Actions without Sequencing Restrictions</span></span>](actions-without-sequencing-restrictions.md)
    -   [<span data-ttu-id="ecbc2-337">Uso delle proprietà nelle istruzioni condizionali</span><span class="sxs-lookup"><span data-stu-id="ecbc2-337">Using Properties in Conditional Statements</span></span>](using-properties-in-conditional-statements.md)
    -   [<span data-ttu-id="ecbc2-338">Sintassi dell'istruzione condizionale</span><span class="sxs-lookup"><span data-stu-id="ecbc2-338">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
    -   [<span data-ttu-id="ecbc2-339">Esempi di sintassi di istruzioni condizionali</span><span class="sxs-lookup"><span data-stu-id="ecbc2-339">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
    -   [<span data-ttu-id="ecbc2-340">Esecuzione delle azioni di condizionamento durante la rimozione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-340">Conditioning Actions to Run During Removal</span></span>](conditioning-actions-to-run-during-removal.md)
    -   [<span data-ttu-id="ecbc2-341">Azioni standard</span><span class="sxs-lookup"><span data-stu-id="ecbc2-341">Standard Actions</span></span>](standard-actions.md)
    -   [<span data-ttu-id="ecbc2-342">Esempi di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-342">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="ecbc2-343">Preparare il pacchetto di installazione dell'applicazione per gli aggiornamenti futuri dell'applicazione da parte del servizio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-343">Prepare the installation package of the application for future upgrades of the application by the Windows Installer service.</span></span>

    <span data-ttu-id="ecbc2-344">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-344">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-345">Applicazione di patch e aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-345">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="ecbc2-346">Preparazione di un'applicazione per aggiornamenti principali futuri</span><span class="sxs-lookup"><span data-stu-id="ecbc2-346">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
    -   [<span data-ttu-id="ecbc2-347">Uso di un UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="ecbc2-347">Using an UpgradeCode</span></span>](using-an-upgradecode.md)
    -   [<span data-ttu-id="ecbc2-348">Aggiorna tabella</span><span class="sxs-lookup"><span data-stu-id="ecbc2-348">Upgrade Table</span></span>](upgrade-table.md)
    -   [<span data-ttu-id="ecbc2-349">**Proprietà UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-349">**UpgradeCode Property**</span></span>](upgradecode.md)
    -   [<span data-ttu-id="ecbc2-350">Impedire l'installazione di un pacchetto obsoleto in una versione più recente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-350">Preventing an Old Package from Installing Over a Newer Version</span></span>](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [<span data-ttu-id="ecbc2-351">Modifica del codice del prodotto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-351">Changing the Product Code</span></span>](changing-the-product-code.md)
    -   [<span data-ttu-id="ecbc2-352">Aggiornamento degli assembly</span><span class="sxs-lookup"><span data-stu-id="ecbc2-352">Updating Assemblies</span></span>](updating-assemblies.md)
    -   [<span data-ttu-id="ecbc2-353">Esempi di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-353">Windows Installer Examples</span></span>](windows-installer-examples.md)

-   <span data-ttu-id="ecbc2-354">Risolvere i problemi relativi ai pacchetti Windows Installer in fase di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-354">Troubleshoot Windows Installer packages under development.</span></span>

    <span data-ttu-id="ecbc2-355">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-355">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-356">Convalida del pacchetto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-356">Package Validation</span></span>](package-validation.md)
    -   [<span data-ttu-id="ecbc2-357">Analizzatori di coerenza interni-CIEM</span><span class="sxs-lookup"><span data-stu-id="ecbc2-357">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
    -   [<span data-ttu-id="ecbc2-358">Registrazione Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-358">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="ecbc2-359">Verifica dell'installazione di funzionalità, componenti, file</span><span class="sxs-lookup"><span data-stu-id="ecbc2-359">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="ecbc2-360">Creazione di un pacchetto di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="ecbc2-360">Authoring a Large Package</span></span>](authoring-a-large-package.md)
    -   [<span data-ttu-id="ecbc2-361">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="ecbc2-361">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="ecbc2-362">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-362">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
    -   [<span data-ttu-id="ecbc2-363">Convalida di moduli merge</span><span class="sxs-lookup"><span data-stu-id="ecbc2-363">Validating Merge Modules</span></span>](validating-merge-modules.md)
    -   [<span data-ttu-id="ecbc2-364">Convalida di un database di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-364">Validating an Installation Database</span></span>](validating-an-installation-database.md)
    -   [<span data-ttu-id="ecbc2-365">Convalida di un aggiornamento dell'installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-365">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)
    -   [<span data-ttu-id="ecbc2-366">Ricerca di una funzionalità o di un componente danneggiato</span><span class="sxs-lookup"><span data-stu-id="ecbc2-366">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="ecbc2-367">Messaggi di errore Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-367">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="ecbc2-368">Registrazione delle richieste di riavvio</span><span class="sxs-lookup"><span data-stu-id="ecbc2-368">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="ecbc2-369">Verificare la configurazione e l'installazione sicure dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-369">Ensure a secure setup and installation of the application.</span></span>

    <span data-ttu-id="ecbc2-370">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-370">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-371">Linee guida per la creazione di installazioni sicure</span><span class="sxs-lookup"><span data-stu-id="ecbc2-371">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="ecbc2-372">Linee guida per la protezione di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="ecbc2-372">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="ecbc2-373">Sicurezza azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="ecbc2-373">Custom Action Security</span></span>](custom-action-security.md)
    -   [<span data-ttu-id="ecbc2-374">Linee guida per la protezione dei pacchetti nei computer bloccati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-374">Guidelines for Securing Packages on Locked-Down Computers</span></span>](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [<span data-ttu-id="ecbc2-375">Creazione di un'installazione firmata completamente verificata tramite l'automazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-375">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [<span data-ttu-id="ecbc2-376">Esempio di installazione di Windows Installer basata su Windows</span><span class="sxs-lookup"><span data-stu-id="ecbc2-376">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="ecbc2-377">Creazione dell'interfaccia utente per l'input della password</span><span class="sxs-lookup"><span data-stu-id="ecbc2-377">Authoring the User Interface for Password Input</span></span>](authoring-the-user-interface-for-password-input.md)
    -   [<span data-ttu-id="ecbc2-378">Firme digitali e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-378">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
    -   [<span data-ttu-id="ecbc2-379">Uso di Windows Installer con UAC</span><span class="sxs-lookup"><span data-stu-id="ecbc2-379">Using Windows Installer with UAC</span></span>](using-windows-installer-with-uac.md)
    -   [<span data-ttu-id="ecbc2-380">Applicazione di patch al controllo dell'account utente (UAC)</span><span class="sxs-lookup"><span data-stu-id="ecbc2-380">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
    -   [<span data-ttu-id="ecbc2-381">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="ecbc2-381">Msicert.exe</span></span>](msicert-exe.md)
    -   [<span data-ttu-id="ecbc2-382">**Proprietà AdminUser**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-382">**AdminUser property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="ecbc2-383">**Proprietà Privileged**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-383">**Privileged property**</span></span>](privileged.md)
    -   [<span data-ttu-id="ecbc2-384">**Proprietà SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-384">**SecureCustomProperties property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="ecbc2-385">Creare un'interfaccia utente per presentare le opzioni per configurare l'installazione e ottenere informazioni dall'utente sul processo di installazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-385">Create a user interface to present options to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="ecbc2-386">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-386">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-387">Informazioni sull'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-387">About the User Interface</span></span>](about-the-user-interface.md)
    -   [<span data-ttu-id="ecbc2-388">Aggiunta di controlli e testo</span><span class="sxs-lookup"><span data-stu-id="ecbc2-388">Adding Controls and Text</span></span>](adding-controls-and-text.md)
    -   [<span data-ttu-id="ecbc2-389">Creazione di un controllo ProgressBar</span><span class="sxs-lookup"><span data-stu-id="ecbc2-389">Authoring a ProgressBar Control</span></span>](authoring-a-progressbar-control.md)
    -   [<span data-ttu-id="ecbc2-390">Creazione di messaggi di richiesta del disco</span><span class="sxs-lookup"><span data-stu-id="ecbc2-390">Authoring Disk Prompt Messages</span></span>](authoring-disk-prompt-messages.md)
    -   [<span data-ttu-id="ecbc2-391">Creazione di un condizionale "attendere..." MessageBox</span><span class="sxs-lookup"><span data-stu-id="ecbc2-391">Authoring a Conditional "Please Wait . . ." Message Box</span></span>](authoring-a-conditional-please-wait-------message-box.md)
    -   [<span data-ttu-id="ecbc2-392">Visualizzazione in anteprima dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-392">Previewing the User Interface</span></span>](previewing-the-user-interface.md)
    -   [<span data-ttu-id="ecbc2-393">Aggiunta di testo archiviato in una proprietà</span><span class="sxs-lookup"><span data-stu-id="ecbc2-393">Adding Text Stored in a Property</span></span>](adding-text-stored-in-a-property.md)
    -   [<span data-ttu-id="ecbc2-394">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-394">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   <span data-ttu-id="ecbc2-395">Creare un'interfaccia utente esterna per presentare un'interfaccia utente personalizzata per configurare l'installazione e ottenere informazioni dall'utente sul processo di installazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-395">Create an external user interface to present a custom user interface to configure the installation and obtain information from the user about the pending installation process.</span></span>

    <span data-ttu-id="ecbc2-396">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-396">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-397">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-397">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [<span data-ttu-id="ecbc2-398">Monitoraggio di un'installazione mediante MsiSetExternalUIRecord</span><span class="sxs-lookup"><span data-stu-id="ecbc2-398">Monitoring an Installation Using MsiSetExternalUIRecord</span></span>](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [<span data-ttu-id="ecbc2-399">Analisi di messaggi di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-399">Parsing Windows Installer Messages</span></span>](parsing-windows-installer-messages.md)
    -   [<span data-ttu-id="ecbc2-400">Restituzione di valori da un gestore di interfaccia utente esterno</span><span class="sxs-lookup"><span data-stu-id="ecbc2-400">Returning Values from an External User Interface Handler</span></span>](returning-values-from-an-external-user-interface-handler.md)
    -   [<span data-ttu-id="ecbc2-401">\_gestore INSTALLUI</span><span class="sxs-lookup"><span data-stu-id="ecbc2-401">INSTALLUI\_HANDLER</span></span>](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [<span data-ttu-id="ecbc2-402">Gestione dei messaggi di stato tramite MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="ecbc2-402">Handling Progress Messages Using MsiSetExternalUI</span></span>](handling-progress-messages-using-msisetexternalui.md)
    -   [<span data-ttu-id="ecbc2-403">Monitoraggio di un'installazione mediante MsiSetExternalUI</span><span class="sxs-lookup"><span data-stu-id="ecbc2-403">Monitoring an Installation Using MsiSetExternalUI</span></span>](monitoring-an-installation-using-msisetexternalui.md)

-   <span data-ttu-id="ecbc2-404">Impostare le informazioni per l'applicazione in **installazione** applicazioni (ARP.)</span><span class="sxs-lookup"><span data-stu-id="ecbc2-404">Set information for the application in **Add/Remove Programs** (ARP.)</span></span>

    <span data-ttu-id="ecbc2-405">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-405">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-406">Configurazione di installazione applicazioni con Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-406">Configuring Add/Remove Programs with Windows Installer</span></span>](configuring-add-remove-programs-with-windows-installer.md)
    -   [<span data-ttu-id="ecbc2-407">Aggiunta e rimozione di un'applicazione senza traccia nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-407">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [<span data-ttu-id="ecbc2-408">Disinstalla chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-408">Uninstall Registry Key</span></span>](uninstall-registry-key.md)

-   <span data-ttu-id="ecbc2-409">Scrivere azioni personalizzate per gestire la logica di installazione che non è supportata in modo nativo da Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-409">Write custom actions to handle setup logic that is not natively supported by Windows Installer.</span></span>

    <span data-ttu-id="ecbc2-410">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-410">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-411">Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="ecbc2-411">Custom Actions</span></span>](custom-actions.md)
    -   [<span data-ttu-id="ecbc2-412">Elenco riepilogativo di tutti i tipi di azione personalizzati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-412">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)
    -   [<span data-ttu-id="ecbc2-413">Linee guida per la protezione di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="ecbc2-413">Guidelines for Securing Custom Actions</span></span>](guidelines-for-securing-custom-actions.md)
    -   [<span data-ttu-id="ecbc2-414">Riferimento all'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="ecbc2-414">Custom Action Reference</span></span>](custom-action-reference.md)
    -   [<span data-ttu-id="ecbc2-415">Uso di un'azione personalizzata per creare account utente in un computer locale</span><span class="sxs-lookup"><span data-stu-id="ecbc2-415">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="ecbc2-416">Uso di un'azione personalizzata per avviare un file installato al termine dell'installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-416">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [<span data-ttu-id="ecbc2-417">Accesso a un database o a una sessione dall'interno di un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="ecbc2-417">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="ecbc2-418">Accesso alla sessione corrente del programma di installazione dall'interno di un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="ecbc2-418">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [<span data-ttu-id="ecbc2-419">Modifica dello stato del sistema mediante un'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="ecbc2-419">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)

-   <span data-ttu-id="ecbc2-420">Bootstrap del Windows Installer nel computer di un utente.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-420">Bootstrap the Windows Installer onto a user's computer.</span></span>

    <span data-ttu-id="ecbc2-421">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-421">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-422">Bootstrap</span><span class="sxs-lookup"><span data-stu-id="ecbc2-422">Bootstrapping</span></span>](bootstrapping.md)
    -   [<span data-ttu-id="ecbc2-423">Instmsi.exe</span><span class="sxs-lookup"><span data-stu-id="ecbc2-423">Instmsi.exe</span></span>](instmsi-exe.md)
    -   [<span data-ttu-id="ecbc2-424">Bootstrap di download Internet</span><span class="sxs-lookup"><span data-stu-id="ecbc2-424">Internet Download Bootstrapping</span></span>](internet-download-bootstrapping.md)
    -   [<span data-ttu-id="ecbc2-425">Msistuff.exe</span><span class="sxs-lookup"><span data-stu-id="ecbc2-425">Msistuff.exe</span></span>](msistuff-exe.md)
    -   [<span data-ttu-id="ecbc2-426">Esempio di installazione di Windows Installer basata su Windows</span><span class="sxs-lookup"><span data-stu-id="ecbc2-426">A URL-Based Windows Installer Installation Example</span></span>](a-url-based-windows-installer-installation-example.md)
    -   [<span data-ttu-id="ecbc2-427">Configurazione delle risorse Setup.exe</span><span class="sxs-lookup"><span data-stu-id="ecbc2-427">Configuring the Setup.exe Resources</span></span>](configuring-the-setup-exe-resources.md)
    -   [<span data-ttu-id="ecbc2-428">Download di un'installazione da Internet</span><span class="sxs-lookup"><span data-stu-id="ecbc2-428">Downloading an Installation from the Internet</span></span>](downloading-an-installation-from-the-internet.md)

-   <span data-ttu-id="ecbc2-429">Rispettare Active Accessibility linee guida per la scrittura di pacchetti Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-429">Adhere to Active Accessibility guidelines when writing Windows Installer packages.</span></span>

    <span data-ttu-id="ecbc2-430">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-430">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-431">Accessibilità</span><span class="sxs-lookup"><span data-stu-id="ecbc2-431">Accessibility</span></span>](accessibility.md)

-   <span data-ttu-id="ecbc2-432">Preparare l'internazionalizzazione della configurazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-432">Prepare for the internationalization of an application setup.</span></span>

    <span data-ttu-id="ecbc2-433">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-433">For more information, see the following:</span></span>

    -   <span data-ttu-id="ecbc2-434">[Preparazione di un pacchetto di Windows Installer per la localizzazione](preparing-a-windows-installer-package-for-localization.md),</span><span class="sxs-lookup"><span data-stu-id="ecbc2-434">[Preparing a Windows Installer Package for Localization](preparing-a-windows-installer-package-for-localization.md),</span></span>
    -   [<span data-ttu-id="ecbc2-435">Localizzazione di un pacchetto di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-435">Localizing a Windows Installer Package</span></span>](localizing-a-windows-installer-package.md)
    -   [<span data-ttu-id="ecbc2-436">Gestione della tabella codici (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="ecbc2-436">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
    -   [<span data-ttu-id="ecbc2-437">Aggiunta di risorse localizzate</span><span class="sxs-lookup"><span data-stu-id="ecbc2-437">Adding Localized Resources</span></span>](adding-localized-resources.md)
    -   [<span data-ttu-id="ecbc2-438">Esempio di localizzazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-438">A Localization Example</span></span>](a-localization-example.md)
    -   [<span data-ttu-id="ecbc2-439">Localizzazione delle tabelle Error e ActionText</span><span class="sxs-lookup"><span data-stu-id="ecbc2-439">Localizing the Error and ActionText Tables</span></span>](localizing-the-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="ecbc2-440">Localizzazione di colonne di database</span><span class="sxs-lookup"><span data-stu-id="ecbc2-440">Localizing Database Columns</span></span>](localizing-database-columns.md)
    -   [<span data-ttu-id="ecbc2-441">Creazione di un database con una tabella codici neutra</span><span class="sxs-lookup"><span data-stu-id="ecbc2-441">Creating a Database with a Neutral Code Page</span></span>](creating-a-database-with-a-neutral-code-page.md)
    -   [<span data-ttu-id="ecbc2-442">Gestione delle tabelle codici per le tabelle importate ed esportate</span><span class="sxs-lookup"><span data-stu-id="ecbc2-442">Code Page Handling of Imported and Exported Tables</span></span>](code-page-handling-of-imported-and-exported-tables.md)
    -   [<span data-ttu-id="ecbc2-443">Localizzazione della lingua visualizzata dalle finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="ecbc2-443">Localizing the Language Displayed by Dialogs</span></span>](localizing-the-language-displayed-by-dialogs.md)
    -   [<span data-ttu-id="ecbc2-444">Importazione delle tabelle ActionText e degli errori localizzati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-444">Importing Localized Error and ActionText Tables</span></span>](importing-localized-error-and-actiontext-tables.md)
    -   [<span data-ttu-id="ecbc2-445">Aggiornamento delle proprietà ProductLanguage e ProductCode</span><span class="sxs-lookup"><span data-stu-id="ecbc2-445">Updating ProductLanguage and ProductCode Properties</span></span>](updating-productlanguage-and-productcode-properties.md)
    -   [<span data-ttu-id="ecbc2-446">Aggiornamento di un flusso di informazioni di riepilogo</span><span class="sxs-lookup"><span data-stu-id="ecbc2-446">Updating a Summary Information Stream</span></span>](updating-a-summary-information-stream.md)
    -   [<span data-ttu-id="ecbc2-447">Componenti qualificati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-447">Qualified Components</span></span>](qualified-components.md)
    -   [<span data-ttu-id="ecbc2-448">Tabella UIText</span><span class="sxs-lookup"><span data-stu-id="ecbc2-448">UIText Table</span></span>](uitext-table.md)
    -   [<span data-ttu-id="ecbc2-449">Gestisci lingua e tabella codici</span><span class="sxs-lookup"><span data-stu-id="ecbc2-449">Manage Language and Codepage</span></span>](manage-language-and-codepage.md)
    -   [<span data-ttu-id="ecbc2-450">Controllo della tabella codici del database di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-450">Checking the Installation Database Code Page</span></span>](checking-the-installation-database-code-page.md)

-   <span data-ttu-id="ecbc2-451">Creare pacchetti di Windows Installer per piattaforme a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-451">Create Windows Installer packages for 32-bit and 64-bit platforms.</span></span>

    <span data-ttu-id="ecbc2-452">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-452">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-453">Windows Installer su sistemi operativi a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ecbc2-453">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)
    -   [<span data-ttu-id="ecbc2-454">Azioni personalizzate a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ecbc2-454">64-Bit Custom Actions</span></span>](64-bit-custom-actions.md)
    -   [<span data-ttu-id="ecbc2-455">Uso di azioni personalizzate a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ecbc2-455">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)
    -   [<span data-ttu-id="ecbc2-456">Uso di moduli unione a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ecbc2-456">Using 64-bit Merge Modules</span></span>](using-64-bit-merge-modules.md)

-   <span data-ttu-id="ecbc2-457">Ridistribuire i componenti di Windows Installer condivisi e la logica di installazione come moduli unione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-457">Redistribute shared Windows Installer components and setup logic as merge modules.</span></span>

    <span data-ttu-id="ecbc2-458">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-458">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-459">Unisci moduli</span><span class="sxs-lookup"><span data-stu-id="ecbc2-459">Merge Modules</span></span>](merge-modules.md)
    -   [<span data-ttu-id="ecbc2-460">Creazione di una trasformazione lingua per un modulo merge a più lingue</span><span class="sxs-lookup"><span data-stu-id="ecbc2-460">Authoring a Language Transform for a Multiple Language Merge Module</span></span>](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [<span data-ttu-id="ecbc2-461">Applicazione di un modulo merge configurabile con personalizzazioni</span><span class="sxs-lookup"><span data-stu-id="ecbc2-461">Applying a Configurable Merge Module with Customizations</span></span>](applying-a-configurable-merge-module-with-customizations.md)

-   <span data-ttu-id="ecbc2-462">Pianificare o disattivare il riavvio durante un'installazione di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-462">Schedule or suppress reboots during a Windows Installer installation.</span></span>

    <span data-ttu-id="ecbc2-463">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-463">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-464">Riavvio del sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-464">System Reboots</span></span>](system-reboots.md)
    -   [<span data-ttu-id="ecbc2-465">Registrazione delle richieste di riavvio</span><span class="sxs-lookup"><span data-stu-id="ecbc2-465">Logging of Reboot Requests</span></span>](logging-of-reboot-requests.md)

-   <span data-ttu-id="ecbc2-466">Creare aggiornamenti o correzioni per un'applicazione esistente creando una patch.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-466">Create updates or fixes for an existing application by creating a patch.</span></span>

    <span data-ttu-id="ecbc2-467">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-467">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-468">Creazione di una patch di aggiornamento di piccole dimensioni</span><span class="sxs-lookup"><span data-stu-id="ecbc2-468">Creating a Small Update Patch</span></span>](creating-a-small-update-patch.md)
    -   [<span data-ttu-id="ecbc2-469">Un piccolo esempio di patch di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ecbc2-469">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)

-   <span data-ttu-id="ecbc2-470">Creare un pacchetto a doppio scopo in grado di installare un'applicazione solo per l'utente corrente o per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-470">Author a dual-purpose package capable of installing an application either for only the current user or for all users of the computer.</span></span>

    <span data-ttu-id="ecbc2-471">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-471">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-472">Contesto di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-472">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="ecbc2-473">Creazione di pacchetti singoli</span><span class="sxs-lookup"><span data-stu-id="ecbc2-473">Single Package Authoring</span></span>](single-package-authoring.md)
    -   [<span data-ttu-id="ecbc2-474">Esempio di creazione di pacchetti singoli</span><span class="sxs-lookup"><span data-stu-id="ecbc2-474">Single Package Authoring Example</span></span>](single-package-authoring-example.md)

-   <span data-ttu-id="ecbc2-475">Personalizzare i servizi nel computer usando il Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-475">Customize services on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="ecbc2-476">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-476">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-477">Uso della configurazione dei servizi</span><span class="sxs-lookup"><span data-stu-id="ecbc2-477">Using Services Configuration</span></span>](using-services-configuration.md)

-   <span data-ttu-id="ecbc2-478">Proteggere le risorse del computer utilizzando il Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-478">Secure resources on the computer using the Windows Installer.</span></span>

    <span data-ttu-id="ecbc2-479">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-479">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-480">Linee guida per la creazione di installazioni sicure</span><span class="sxs-lookup"><span data-stu-id="ecbc2-480">Guidelines for Authoring Secure Installations</span></span>](guidelines-for-authoring-secure-installations.md)
    -   [<span data-ttu-id="ecbc2-481">Protezione delle risorse</span><span class="sxs-lookup"><span data-stu-id="ecbc2-481">Securing Resources</span></span>](securing-resources-.md)

-   <span data-ttu-id="ecbc2-482">Enumerare tutti i componenti installati nel computer e ottenere il percorso della chiave per il componente.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-482">Enumerate all components installed on the computer and obtain the key path for the component.</span></span>

    <span data-ttu-id="ecbc2-483">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-483">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-484">Enumerazione dei componenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-484">Enumerating Components</span></span>](enumerating-components-.md)

-   <span data-ttu-id="ecbc2-485">Installare più pacchetti usando l' [*elaborazione delle transazioni*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ecbc2-485">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="ecbc2-486">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-486">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-487">Installazioni con più pacchetti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-487">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="ecbc2-488">Incorporare un'interfaccia utente personalizzata nel pacchetto di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-488">Embed a custom user interface in the Windows Installer package.</span></span>

    <span data-ttu-id="ecbc2-489">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-489">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-490">Utilizzo dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-490">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="ecbc2-491">Uso di un'interfaccia utente incorporata</span><span class="sxs-lookup"><span data-stu-id="ecbc2-491">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="it-professionals"></a><span data-ttu-id="ecbc2-492">Professionisti IT</span><span class="sxs-lookup"><span data-stu-id="ecbc2-492">IT Professionals</span></span>

<span data-ttu-id="ecbc2-493">I professionisti IT e gli amministratori possono personalizzare e distribuire i pacchetti di Windows Installer esistenti.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-493">IT Professionals and Administrators customize and deploy existing Windows Installer packages.</span></span> <span data-ttu-id="ecbc2-494">Questi utenti riassemblano le configurazioni per le applicazioni esistenti in pacchetti di installazione Windows Installer e installano e gestiscono immagini amministrative di Windows Installer installazioni sulle reti.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-494">These users repackage setups for existing applications into Windows Installer installation packages, and install and maintain administrative images of Windows Installer installations on networks.</span></span>

-   <span data-ttu-id="ecbc2-495">Personalizzare le applicazioni e il programma di installazione tramite la generazione e l'applicazione di trasformazioni Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-495">Customize applications and setup by generating and applying Windows Installer transforms</span></span>

    <span data-ttu-id="ecbc2-496">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-496">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-497">Personalizzazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-497">Customization</span></span>](customization.md)
    -   [<span data-ttu-id="ecbc2-498">Trasformazioni di database</span><span class="sxs-lookup"><span data-stu-id="ecbc2-498">Database Transforms</span></span>](database-transforms.md)
    -   [<span data-ttu-id="ecbc2-499">Esempio di trasformazione della personalizzazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-499">A Customization Transform Example</span></span>](a-customization-transform-example.md)
    -   [<span data-ttu-id="ecbc2-500">Unioni e trasformazioni</span><span class="sxs-lookup"><span data-stu-id="ecbc2-500">Merges and Transforms</span></span>](merges-and-transforms.md)
    -   [<span data-ttu-id="ecbc2-501">Uso delle trasformazioni per aggiungere risorse</span><span class="sxs-lookup"><span data-stu-id="ecbc2-501">Using Transforms to Add Resources</span></span>](using-transforms-to-add-resources.md)
    -   [<span data-ttu-id="ecbc2-502">Genera una trasformazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-502">Generate a Transform</span></span>](generate-a-transform.md)
    -   [<span data-ttu-id="ecbc2-503">Opzioni della riga di comando</span><span class="sxs-lookup"><span data-stu-id="ecbc2-503">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="ecbc2-504">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="ecbc2-504">Msitran.exe</span></span>](msitran-exe.md)
    -   [<span data-ttu-id="ecbc2-505">Applicare una trasformazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-505">Apply a Transform</span></span>](apply-a-transform.md)
    -   [<span data-ttu-id="ecbc2-506">Visualizzazione di una trasformazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-506">View a Transform</span></span>](view-a-transform.md)
    -   [<span data-ttu-id="ecbc2-507">Visualizzare le differenze tra due database</span><span class="sxs-lookup"><span data-stu-id="ecbc2-507">View Differences Between Two Databases</span></span>](view-differences-between-two-databases.md)
    -   [<span data-ttu-id="ecbc2-508">Applicazione di patch a applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="ecbc2-508">Patching Customized Applications</span></span>](patching-customized-applications.md)

-   <span data-ttu-id="ecbc2-509">Distribuire un pacchetto di installazione di Windows Installer, aggiornamento o patch.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-509">Deploy a Windows Installer installation package, update, or patch.</span></span>

    <span data-ttu-id="ecbc2-510">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-510">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-511">Installazione di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-511">Installing an Application</span></span>](installing-an-application.md)
    -   [<span data-ttu-id="ecbc2-512">Applicazione di patch e aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-512">Patching and Upgrades</span></span>](patching-and-upgrades.md)
    -   [<span data-ttu-id="ecbc2-513">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="ecbc2-513">Transforms</span></span>](transforms.md)
    -   [<span data-ttu-id="ecbc2-514">Installazione di un pacchetto con privilegi elevati per un amministratore non</span><span class="sxs-lookup"><span data-stu-id="ecbc2-514">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="ecbc2-515">Applicazione degli aggiornamenti principali mediante l'applicazione di patch all'installazione locale del prodotto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-515">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="ecbc2-516">Applicazione degli aggiornamenti principali tramite l'installazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-516">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="ecbc2-517">Applicazione di piccoli aggiornamenti con l'applicazione di patch all'installazione locale del prodotto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-517">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="ecbc2-518">Applicazione di piccoli aggiornamenti con la reinstallazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-518">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="ecbc2-519">Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa</span><span class="sxs-lookup"><span data-stu-id="ecbc2-519">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="ecbc2-520">Applicazione di patch alle installazioni iniziali</span><span class="sxs-lookup"><span data-stu-id="ecbc2-520">Patching Initial Installations</span></span>](patching-initial-installations.md)
    -   [<span data-ttu-id="ecbc2-521">Opzioni della riga di comando</span><span class="sxs-lookup"><span data-stu-id="ecbc2-521">Command Line Options</span></span>](command-line-options.md)

-   <span data-ttu-id="ecbc2-522">Risolvere i problemi relativi ai pacchetti Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-522">Troubleshoot Windows Installer packages.</span></span>

    <span data-ttu-id="ecbc2-523">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-523">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-524">Registrazione Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-524">Windows Installer Logging</span></span>](windows-installer-logging.md)
    -   [<span data-ttu-id="ecbc2-525">Verifica dell'installazione di funzionalità, componenti, file</span><span class="sxs-lookup"><span data-stu-id="ecbc2-525">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
    -   [<span data-ttu-id="ecbc2-526">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="ecbc2-526">Wilogutl.exe</span></span>](wilogutl-exe.md)
    -   [<span data-ttu-id="ecbc2-527">Ricerca di una funzionalità o di un componente danneggiato</span><span class="sxs-lookup"><span data-stu-id="ecbc2-527">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
    -   [<span data-ttu-id="ecbc2-528">Messaggi di errore Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-528">Windows Installer Error Messages</span></span>](windows-installer-error-messages.md)
    -   [<span data-ttu-id="ecbc2-529">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="ecbc2-529">Msicert.exe</span></span>](msicert-exe.md)

-   <span data-ttu-id="ecbc2-530">Utilizzare gli script per eseguire query Windows Installer pacchetti per ottenere informazioni su un prodotto e modificarne l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-530">Use scripting to query Windows Installer packages for information about a product and modify the installation.</span></span>

    <span data-ttu-id="ecbc2-531">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-531">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-532">Interfaccia di automazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-532">Automation Interface</span></span>](automation-interface.md)
    -   [<span data-ttu-id="ecbc2-533">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-533">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
    -   [<span data-ttu-id="ecbc2-534">Utilizzo di Windows Installer con WMI</span><span class="sxs-lookup"><span data-stu-id="ecbc2-534">Using Windows Installer with WMI</span></span>](using-windows-installer-with-wmi.md)

-   <span data-ttu-id="ecbc2-535">Creare e gestire le installazioni amministrative.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-535">Create and maintain administrative installations.</span></span>

    <span data-ttu-id="ecbc2-536">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-536">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-537">Installazione amministrativa</span><span class="sxs-lookup"><span data-stu-id="ecbc2-537">Administrative Installation</span></span>](administrative-installation.md)
    -   [<span data-ttu-id="ecbc2-538">Opzioni della riga di comando</span><span class="sxs-lookup"><span data-stu-id="ecbc2-538">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="ecbc2-539">**Proprietà AdminProperties**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-539">**AdminProperties Property**</span></span>](adminproperties.md)
    -   [<span data-ttu-id="ecbc2-540">Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa</span><span class="sxs-lookup"><span data-stu-id="ecbc2-540">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="ecbc2-541">Applicazione di un pacchetto di patch a un'installazione amministrativa</span><span class="sxs-lookup"><span data-stu-id="ecbc2-541">Applying a Patch Package to an Administrative Installation</span></span>](applying-a-patch-package-to-an-administrative-installation.md)
    -   [<span data-ttu-id="ecbc2-542">Ordine di esecuzione delle azioni</span><span class="sxs-lookup"><span data-stu-id="ecbc2-542">Action Execution Order</span></span>](action-execution-order.md)
    -   [<span data-ttu-id="ecbc2-543">**Proprietà IsAdminPackage**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-543">**IsAdminPackage Property**</span></span>](isadminpackage.md)
    -   [<span data-ttu-id="ecbc2-544">Ordine di precedenza delle proprietà</span><span class="sxs-lookup"><span data-stu-id="ecbc2-544">Order of Property Precedence</span></span>](order-of-property-precedence.md)
    -   [<span data-ttu-id="ecbc2-545">**Proprietà AdminProperties**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-545">**AdminProperties Property**</span></span>](adminproperties.md)

-   <span data-ttu-id="ecbc2-546">Rendere disponibile un'applicazione per tutti gli utenti di un computer o solo per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-546">Make an application available to all users of a computer or to a specified user only.</span></span>

    <span data-ttu-id="ecbc2-547">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-547">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-548">Contesto di installazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-548">Installation Context</span></span>](installation-context.md)
    -   [<span data-ttu-id="ecbc2-549">**Proprietà ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-549">**ALLUSERS Property**</span></span>](allusers.md)

-   <span data-ttu-id="ecbc2-550">Interpretare i pacchetti, installare i prodotti e configurare le opzioni delle funzionalità tramite una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-550">Interpret packages, install products, and configure feature options using a command line.</span></span>

    <span data-ttu-id="ecbc2-551">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-551">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-552">Opzioni della riga di comando</span><span class="sxs-lookup"><span data-stu-id="ecbc2-552">Command Line Options</span></span>](command-line-options.md)
    -   [<span data-ttu-id="ecbc2-553">Impostazione dei valori delle proprietà pubbliche nella riga di comando</span><span class="sxs-lookup"><span data-stu-id="ecbc2-553">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
    -   [<span data-ttu-id="ecbc2-554">Recupero e impostazione delle proprietà</span><span class="sxs-lookup"><span data-stu-id="ecbc2-554">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
    -   [<span data-ttu-id="ecbc2-555">Reinstallazione di una funzionalità o di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-555">Reinstalling a Feature or Application</span></span>](reinstalling-a-feature-or-application.md)
    -   [<span data-ttu-id="ecbc2-556">Applicazione di piccoli aggiornamenti con l'applicazione di patch all'installazione locale del prodotto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-556">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [<span data-ttu-id="ecbc2-557">Applicazione di piccoli aggiornamenti con la reinstallazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-557">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
    -   [<span data-ttu-id="ecbc2-558">Modifica del percorso di destinazione per una directory</span><span class="sxs-lookup"><span data-stu-id="ecbc2-558">Changing the Target Location for a Directory</span></span>](changing-the-target-location-for-a-directory.md)
    -   [<span data-ttu-id="ecbc2-559">Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa</span><span class="sxs-lookup"><span data-stu-id="ecbc2-559">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)
    -   [<span data-ttu-id="ecbc2-560">Applicazione degli aggiornamenti principali tramite l'installazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-560">Applying Major Upgrades by Installing the Product</span></span>](applying-major-upgrades-by-installing-the-product.md)
    -   [<span data-ttu-id="ecbc2-561">Proprietà di configurazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-561">Configuration Properties</span></span>](property-reference.md)
    -   [<span data-ttu-id="ecbc2-562">Proprietà opzioni di installazione funzionalità</span><span class="sxs-lookup"><span data-stu-id="ecbc2-562">Feature Installation Options Properties</span></span>](property-reference.md)

-   <span data-ttu-id="ecbc2-563">Usare i criteri per gestire i diritti e le autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-563">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="ecbc2-564">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-564">For more information, see the following:</span></span>

    -   <span data-ttu-id="ecbc2-565">[Criteri del computer](machine-policies.md),</span><span class="sxs-lookup"><span data-stu-id="ecbc2-565">[Machine Policies](machine-policies.md),</span></span>
    -   <span data-ttu-id="ecbc2-566">[Criteri utente](user-policies.md),</span><span class="sxs-lookup"><span data-stu-id="ecbc2-566">[User Policies](user-policies.md),</span></span>
    -   [<span data-ttu-id="ecbc2-567">Installazione di un pacchetto con privilegi elevati per un amministratore non</span><span class="sxs-lookup"><span data-stu-id="ecbc2-567">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="ecbc2-568">Annuncio di un'applicazione Per-User da installare con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-568">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="ecbc2-569">Uso di un'azione personalizzata per creare account utente in un computer locale</span><span class="sxs-lookup"><span data-stu-id="ecbc2-569">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="ecbc2-570">**Proprietà AdminUser**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-570">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="ecbc2-571">**Proprietà Privileged**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-571">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="ecbc2-572">**Proprietà EnableUserControl**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-572">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="ecbc2-573">**Proprietà UserSID**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-573">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="ecbc2-574">**Proprietà SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-574">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

-   <span data-ttu-id="ecbc2-575">Installare più pacchetti usando l' [*elaborazione delle transazioni*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ecbc2-575">Install multiple packages using [*transaction processing*](t-gly.md).</span></span>

    <span data-ttu-id="ecbc2-576">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-576">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-577">Installazioni con più pacchetti</span><span class="sxs-lookup"><span data-stu-id="ecbc2-577">Multiple-Package Installations</span></span>](multiple-package-installations.md)

-   <span data-ttu-id="ecbc2-578">Incorporare un'interfaccia utente personalizzata all'interno di un pacchetto di Windows Installer..</span><span class="sxs-lookup"><span data-stu-id="ecbc2-578">Embed a custom user interface within a Windows Installer package..</span></span>

    <span data-ttu-id="ecbc2-579">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-579">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-580">Utilizzo dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-580">Using the User Interface</span></span>](using-the-user-interface.md)
    -   [<span data-ttu-id="ecbc2-581">Uso di un'interfaccia utente incorporata</span><span class="sxs-lookup"><span data-stu-id="ecbc2-581">Using an Embedded UI</span></span>](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a><span data-ttu-id="ecbc2-582">Sviluppatori di infrastrutture</span><span class="sxs-lookup"><span data-stu-id="ecbc2-582">Infrastructure Developers</span></span>

<span data-ttu-id="ecbc2-583">Gli sviluppatori di infrastrutture possono creare piattaforme unificate per la distribuzione e la gestione del software che usa il servizio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-583">Infrastructure Developers can create unified platforms for the deployment and management of software that uses the Windows Installer service.</span></span> <span data-ttu-id="ecbc2-584">Possono utilizzare l'interfaccia di programmazione Windows Installer per eseguire query, gestire e distribuire applicazioni, patch e origini in un sistema.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-584">They can use the Windows Installer programming interface to query, manage, and distribute applications, patches, and sources on a system.</span></span>

-   <span data-ttu-id="ecbc2-585">Individuazione, inventario ed esecuzione di query per lo stato, le informazioni e i client dei componenti.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-585">Locate, inventory and query for the state, information, and clients of components.</span></span>

    <span data-ttu-id="ecbc2-586">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-586">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-587">Funzioni specifiche del componente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-587">Component-Specific Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="ecbc2-588">Funzioni di stato del sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-588">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="ecbc2-589">Oggetto Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-589">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="ecbc2-590">Oggetto Product</span><span class="sxs-lookup"><span data-stu-id="ecbc2-590">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="ecbc2-591">Patch (oggetto)</span><span class="sxs-lookup"><span data-stu-id="ecbc2-591">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="ecbc2-592">Inventario ed esecuzione di query per informazioni e lo stato di prodotti e funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-592">Inventory and query for information and the state of products and features.</span></span>

    <span data-ttu-id="ecbc2-593">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-593">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-594">Inventario di prodotti e patch</span><span class="sxs-lookup"><span data-stu-id="ecbc2-594">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="ecbc2-595">Funzioni di stato del sistema</span><span class="sxs-lookup"><span data-stu-id="ecbc2-595">System Status Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="ecbc2-596">Funzioni di query sul prodotto</span><span class="sxs-lookup"><span data-stu-id="ecbc2-596">Product Query Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="ecbc2-597">Oggetto Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-597">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="ecbc2-598">Oggetto Product</span><span class="sxs-lookup"><span data-stu-id="ecbc2-598">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="ecbc2-599">Patch (oggetto)</span><span class="sxs-lookup"><span data-stu-id="ecbc2-599">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="ecbc2-600">Migliorare la resilienza dell'origine usando il Windows Installer per eseguire l'inventario, eseguire query e modificare l'elenco di origine di applicazioni, aggiornamenti e patch.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-600">Improve source resiliency by using the Windows Installer to inventory, query, and modify the source list of applications, upgrades, and patches.</span></span>

    <span data-ttu-id="ecbc2-601">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-601">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-602">**SOURCEs (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-602">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="ecbc2-603">**Resilienza di origine**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-603">**Source Resiliency**</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="ecbc2-604">Funzioni di installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-604">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="ecbc2-605">Oggetto Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-605">Installer Object</span></span>](installer-object.md)
    -   [<span data-ttu-id="ecbc2-606">Oggetto Product</span><span class="sxs-lookup"><span data-stu-id="ecbc2-606">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="ecbc2-607">Patch (oggetto)</span><span class="sxs-lookup"><span data-stu-id="ecbc2-607">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="ecbc2-608">Migliorare la resilienza dell'origine usando il Windows Installer per l'inventario, la query e la modifica delle origini multimediali.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-608">Improve source resiliency by using the Windows Installer to inventory, query, and modify media sources.</span></span>

    <span data-ttu-id="ecbc2-609">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-609">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-610">**SOURCEs (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-610">**SOURCELIST Property**</span></span>](sourcelist.md)
    -   [<span data-ttu-id="ecbc2-611">Resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="ecbc2-611">Source Resiliency</span></span>](source-resiliency.md)
    -   [<span data-ttu-id="ecbc2-612">Funzioni di installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="ecbc2-612">Installation and Configuration Functions</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="ecbc2-613">Oggetto Product</span><span class="sxs-lookup"><span data-stu-id="ecbc2-613">Product Object</span></span>](product-object.md)
    -   [<span data-ttu-id="ecbc2-614">Patch (oggetto)</span><span class="sxs-lookup"><span data-stu-id="ecbc2-614">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="ecbc2-615">Inventario ed esecuzione di query per le informazioni e lo stato delle patch.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-615">Inventory and query for information and the state of patches.</span></span>

    <span data-ttu-id="ecbc2-616">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-616">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-617">Inventario di prodotti e patch</span><span class="sxs-lookup"><span data-stu-id="ecbc2-617">Inventory products and patches</span></span>](inventory-products-and-patches-.md)
    -   [<span data-ttu-id="ecbc2-618">Riferimento alla funzione Installer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-618">Installer Function Reference</span></span>](installer-function-reference.md)
    -   [<span data-ttu-id="ecbc2-619">Patch (oggetto)</span><span class="sxs-lookup"><span data-stu-id="ecbc2-619">Patch Object</span></span>](patch-object.md)

-   <span data-ttu-id="ecbc2-620">Usare i criteri per gestire i diritti e le autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-620">Work with policy to manage access rights and permissions.</span></span>

    <span data-ttu-id="ecbc2-621">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ecbc2-621">For more information, see the following:</span></span>

    -   [<span data-ttu-id="ecbc2-622">Criteri del computer</span><span class="sxs-lookup"><span data-stu-id="ecbc2-622">Machine Policies</span></span>](machine-policies.md)
    -   [<span data-ttu-id="ecbc2-623">Criteri utente</span><span class="sxs-lookup"><span data-stu-id="ecbc2-623">User Policies</span></span>](user-policies.md)
    -   [<span data-ttu-id="ecbc2-624">Installazione di un pacchetto con privilegi elevati per un amministratore non</span><span class="sxs-lookup"><span data-stu-id="ecbc2-624">Installing a Package with Elevated Privileges for a Non-Admin</span></span>](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [<span data-ttu-id="ecbc2-625">Annuncio di un'applicazione Per-User da installare con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="ecbc2-625">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [<span data-ttu-id="ecbc2-626">Uso di un'azione personalizzata per creare account utente in un computer locale</span><span class="sxs-lookup"><span data-stu-id="ecbc2-626">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [<span data-ttu-id="ecbc2-627">**Proprietà AdminUser**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-627">**AdminUser Property**</span></span>](adminuser.md)
    -   [<span data-ttu-id="ecbc2-628">**Proprietà Privileged**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-628">**Privileged Property**</span></span>](privileged.md)
    -   [<span data-ttu-id="ecbc2-629">**Proprietà EnableUserControl**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-629">**EnableUserControl Property**</span></span>](enableusercontrol.md)
    -   [<span data-ttu-id="ecbc2-630">**Proprietà UserSID**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-630">**UserSID Property**</span></span>](usersid.md)
    -   [<span data-ttu-id="ecbc2-631">**Proprietà SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="ecbc2-631">**SecureCustomProperties Property**</span></span>](securecustomproperties.md)

 

 



