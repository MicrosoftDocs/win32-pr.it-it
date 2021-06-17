---
title: Panoramica di DWriteCore
description: DWriteCore è l'implementazione Project Implementation di DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 0f908f000d340f9cc9f374e036919422c4a940a6
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262643"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="d9aab-105">Panoramica di DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9aab-105">DWriteCore overview</span></span>

<span data-ttu-id="d9aab-106">DWriteCore è l'implementazione [project-of-project](/windows/apps/project-reunion/) di [DirectWrite (DirectWrite](./direct-write-portal.md) è l'API DirectX per il rendering di testo di alta qualità, i tipi di carattere del contorno indipendenti dalla risoluzione e il supporto completo di layout e testo Unicode).</span><span class="sxs-lookup"><span data-stu-id="d9aab-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="d9aab-107">DWriteCore è una forma di DirectWrite che viene eseguita nelle versioni di Windows fino a Windows 10, versione 1809 (10.0; Build 17763) e apre la porta per l'uso multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="d9aab-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 10, version 1809 (10.0; Build 17763), and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="d9aab-108">Questo argomento introduttivo descrive che cos'è DWriteCore e illustra come installarlo nell'ambiente di sviluppo e programmarlo con esso.</span><span class="sxs-lookup"><span data-stu-id="d9aab-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

> [!TIP]
> <span data-ttu-id="d9aab-109">Per le descrizioni e i collegamenti ai componenti DirectX nello sviluppo attivo, vedere il post di blog DirectX Landing Page (Pagina [di destinazione di DirectX).](https://devblogs.microsoft.com/directx/landing-page/)</span><span class="sxs-lookup"><span data-stu-id="d9aab-109">For descriptions of and links to DirectX components in active development, see the blog post [DirectX Landing Page](https://devblogs.microsoft.com/directx/landing-page/).</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="d9aab-110">Proposta di valore di DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9aab-110">The value proposition of DWriteCore</span></span>

<span data-ttu-id="d9aab-111">[DirectWrite](./direct-write-portal.md) supporta una vasta gamma di funzionalità che lo rendono lo strumento di rendering dei caratteri preferito in Windows per la maggior parte delle app, sia tramite chiamate dirette che &mdash; tramite [Direct2D.](../direct2d/direct2d-portal.md)</span><span class="sxs-lookup"><span data-stu-id="d9aab-111">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="d9aab-112">DirectWrite include un sistema di layout di testo indipendente dal dispositivo, rendering del testo [ClearType Microsoft ClearType](/typography/cleartype/) di qualità elevata, testo con accelerazione hardware, testo multi-formato, funzionalità [opentype avanzate®](/typography/opentype/) tipografia, supporto di lingue wide e layout e rendering compatibili con [GDI.](../gdi/windows-gdi.md)</span><span class="sxs-lookup"><span data-stu-id="d9aab-112">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="d9aab-113">DirectWrite è disponibile a partire da Windows Vista SP2 e si è evoluto nel corso degli anni per includere funzionalità più avanzate, ad esempio i tipi di carattere variabili, che consentono di applicare stili, pesi e altri attributi a un tipo di carattere con una sola risorsa tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d9aab-113">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables you to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="d9aab-114">A causa della lunga durata di DirectWrite, tuttavia, i progressi nello sviluppo hanno tendenziamente lasciato indietro le versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="d9aab-114">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="d9aab-115">Inoltre, lo stato di DirectWrite come tecnologia di rendering del testo premier è limitato solo a Windows, lasciando alle applicazioni multipiattaforma di scrivere il proprio stack di rendering del testo o di basarsi su soluzioni di terze parti.</span><span class="sxs-lookup"><span data-stu-id="d9aab-115">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="d9aab-116">DWriteCore risolve i problemi fondamentali dell'orfano delle funzionalità della versione e della compatibilità multipiattaforma rimuovendo la libreria dal sistema e selezionando come destinazione tutti i possibili endpoint supportati.</span><span class="sxs-lookup"><span data-stu-id="d9aab-116">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="d9aab-117">A tale scopo, DWriteCore è stato integrato in Project Oasi.</span><span class="sxs-lookup"><span data-stu-id="d9aab-117">To that end, we've integrated DWriteCore into Project Reunion.</span></span>

<span data-ttu-id="d9aab-118">Il valore principale che DWriteCore offre, in quanto sviluppatore, in Project Score è che fornisce l'accesso a molte (e infine a tutte) funzionalità DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d9aab-118">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to many (and eventually all) DirectWrite features.</span></span> <span data-ttu-id="d9aab-119">Tutte le funzionalità di DWriteCore funzioneranno allo stesso modo in tutte le versioni di livello inferiore senza alcuna disparità riguardo alle funzionalità che potrebbero funzionare in quali versioni.</span><span class="sxs-lookup"><span data-stu-id="d9aab-119">All features of DWriteCore will function the same on all down-level versions without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="d9aab-120">The DWriteCore demo app &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="d9aab-120">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="d9aab-121">DWriteCore viene illustrato tramite l'app di esempio [DWriteCoreGallery,](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) che è ora disponibile per il download e lo studio.</span><span class="sxs-lookup"><span data-stu-id="d9aab-121">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="d9aab-122">Introduzione a DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9aab-122">Get started with DWriteCore</span></span>

<span data-ttu-id="d9aab-123">DWriteCore fa parte di [ProjectUffio 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)</span><span class="sxs-lookup"><span data-stu-id="d9aab-123">DWriteCore is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="d9aab-124">Questa sezione descrive come configurare l'ambiente di sviluppo per la programmazione con DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="d9aab-124">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-project-reunion-05-vsix"></a><span data-ttu-id="d9aab-125">Installare Project 0.5 VSIX</span><span class="sxs-lookup"><span data-stu-id="d9aab-125">Install the Project Reunion 0.5 VSIX</span></span>

<span data-ttu-id="d9aab-126">In Visual Studio fare clic su **Estensioni**  >  **Gestisci estensioni,** cercare *Project Extensions* e scaricare l'estensione Project Project Extensions.</span><span class="sxs-lookup"><span data-stu-id="d9aab-126">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Project Reunion*, and download the Project Reunion extension.</span></span> <span data-ttu-id="d9aab-127">Chiudere e riaprire Visual Studio e seguire le istruzioni per installare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="d9aab-127">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="d9aab-128">Per altre informazioni, vedere [ProjectUffio 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)e [Configurare l'ambiente di sviluppo (per Project Project Project)](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment).</span><span class="sxs-lookup"><span data-stu-id="d9aab-128">For more info, see [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0), and [Set up your development environment (for Project Reunion)](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="d9aab-129">Creare un nuovo progetto</span><span class="sxs-lookup"><span data-stu-id="d9aab-129">Create a new project</span></span>

<span data-ttu-id="d9aab-130">In Visual Studio creare un nuovo progetto dal modello di progetto App vuota, in pacchetto **(WinUI 3 in Desktop).**</span><span class="sxs-lookup"><span data-stu-id="d9aab-130">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="d9aab-131">È possibile trovare il modello di progetto scegliendo il linguaggio: *C++.* platform: *ProjectNtassi*; Tipo di progetto: *Desktop.*</span><span class="sxs-lookup"><span data-stu-id="d9aab-131">You can find that project template by choosing language: *C++*; platform: *Project Reunion*; project type: *Desktop*.</span></span>

<span data-ttu-id="d9aab-132">Per altre informazioni, vedi [Introduzione a WinUI 3 per le app desktop.](/windows/apps/winui/winui3/get-started-winui3-for-desktop)</span><span class="sxs-lookup"><span data-stu-id="d9aab-132">For more info, see [Get started with WinUI 3 for desktop apps](/windows/apps/winui/winui3/get-started-winui3-for-desktop).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="d9aab-133">Installare il pacchetto NuGet Microsoft.ProjectReunion.DWrite</span><span class="sxs-lookup"><span data-stu-id="d9aab-133">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="d9aab-134">In Visual Studio fare clic  su Progetto Gestisci pacchetti NuGet... Sfoglia , digitare o incollare \>  \>  **Microsoft.ProjectReunion.DWrite**  nella casella di ricerca, selezionare l'elemento nei risultati della ricerca e quindi fare clic su Installa per installare il pacchetto per il progetto.</span><span class="sxs-lookup"><span data-stu-id="d9aab-134">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="d9aab-135">In alternativa, iniziare con l'app di esempio DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="d9aab-135">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="d9aab-136">In alternativa, è possibile programmare con DWriteCore iniziando con il progetto di app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) e basando lo sviluppo su tale progetto.</span><span class="sxs-lookup"><span data-stu-id="d9aab-136">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span> <span data-ttu-id="d9aab-137">È quindi possibile rimuovere qualsiasi codice sorgente (o file) esistente dal progetto di esempio e aggiungere qualsiasi nuovo codice sorgente (o file) al progetto.</span><span class="sxs-lookup"><span data-stu-id="d9aab-137">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="d9aab-138">Usare DWriteCore nel progetto</span><span class="sxs-lookup"><span data-stu-id="d9aab-138">Use DWriteCore in your project</span></span>

<span data-ttu-id="d9aab-139">Per altre informazioni sulla programmazione con DWriteCore, vedere la [sezione Programmazione con DWriteCore](#programming-with-dwritecore) più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="d9aab-139">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="d9aab-140">Fasi di rilascio di DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9aab-140">The release phases of DWriteCore</span></span>

<span data-ttu-id="d9aab-141">La portabilità di DirectWrite in DWriteCore è un progetto sufficientemente grande da estendersi su più cicli di rilascio di Windows.</span><span class="sxs-lookup"><span data-stu-id="d9aab-141">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="d9aab-142">Il progetto è suddiviso in fasi, ognuna delle quali corrisponde a un blocco di funzionalità fornito in una versione.</span><span class="sxs-lookup"><span data-stu-id="d9aab-142">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="d9aab-143">Funzionalità nella versione corrente di DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9aab-143">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="d9aab-144">La versione di DWriteCore attualmente disponibile fa parte di [ProjectScrive 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)</span><span class="sxs-lookup"><span data-stu-id="d9aab-144">The version of DWriteCore currently available is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="d9aab-145">Contiene gli strumenti di base che gli sviluppatori devono usare DWriteCore, incluse le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9aab-145">It contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="d9aab-146">Enumerazione dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="d9aab-146">Font enumeration.</span></span>
- <span data-ttu-id="d9aab-147">API del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d9aab-147">Font API.</span></span>
- <span data-ttu-id="d9aab-148">Modellatura.</span><span class="sxs-lookup"><span data-stu-id="d9aab-148">Shaping.</span></span>
- <span data-ttu-id="d9aab-149">API di rendering di basso livello.</span><span class="sxs-lookup"><span data-stu-id="d9aab-149">Low-level rendering APIs.</span></span> <span data-ttu-id="d9aab-150">Questa operazione è parziale nella fase &mdash; corrente. DWriteCore non interagisce con [Direct2D,](../direct2d/direct2d-portal.md)ma è possibile usare [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget.**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)</span><span class="sxs-lookup"><span data-stu-id="d9aab-150">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="d9aab-151">Funzionalità di layout di testo di base.</span><span class="sxs-lookup"><span data-stu-id="d9aab-151">Basic text layout functionality.</span></span>
- <span data-ttu-id="d9aab-152">API per il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="d9aab-152">Text-rendering APIs.</span></span>
- <span data-ttu-id="d9aab-153">Destinazione di rendering bitmap.</span><span class="sxs-lookup"><span data-stu-id="d9aab-153">Bitmap render target.</span></span>
- <span data-ttu-id="d9aab-154">Tipi di carattere a colori.</span><span class="sxs-lookup"><span data-stu-id="d9aab-154">Color fonts.</span></span>
- <span data-ttu-id="d9aab-155">Ottimizzazioni varie (pulizia della cache dei tipi di carattere, caricatore dei tipi di carattere in memoria e così via).</span><span class="sxs-lookup"><span data-stu-id="d9aab-155">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="d9aab-156">Una funzionalità banner è tipi di carattere a colori.</span><span class="sxs-lookup"><span data-stu-id="d9aab-156">A banner feature is color fonts.</span></span> <span data-ttu-id="d9aab-157">I tipi di carattere a colori consentono di eseguire il rendering dei tipi di carattere con funzionalità di colore più sofisticate oltre a semplici colori singoli.</span><span class="sxs-lookup"><span data-stu-id="d9aab-157">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="d9aab-158">Ad esempio, i tipi di carattere a colori sono ciò che consente di eseguire il rendering dei tipi di carattere icona emoji e barra degli strumenti (quest'ultimo viene usato da Office, ad esempio).</span><span class="sxs-lookup"><span data-stu-id="d9aab-158">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="d9aab-159">I tipi di carattere a colori sono stati introdotti per la prima volta Windows 8.1, ma la funzionalità è stata ampiamente ampliata in Windows 10 versione 1607 (Aggiornamento dell'anniversario).</span><span class="sxs-lookup"><span data-stu-id="d9aab-159">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="d9aab-160">Le operazioni di pulizia della cache dei tipi di carattere e del caricatore dei tipi di carattere in memoria consentono un caricamento più rapido dei tipi di carattere e miglioramenti della memoria.</span><span class="sxs-lookup"><span data-stu-id="d9aab-160">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="d9aab-161">Con queste funzionalità, è possibile iniziare immediatamente a sfruttare alcune delle funzionalità di base moderne di &mdash; DirectWrite, ad esempio i tipi di carattere variabili.</span><span class="sxs-lookup"><span data-stu-id="d9aab-161">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts.</span></span> <span data-ttu-id="d9aab-162">I tipi di carattere variabili sono una delle funzionalità più importanti per i clienti DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d9aab-162">Variable fonts are one of the most important features for DirectWrite customers.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="d9aab-163">L'invito a microsoft come sviluppatore DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d9aab-163">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="d9aab-164">DWriteCore, insieme ad altri componenti di Project Associate, verrà sviluppato con apertura al feedback degli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="d9aab-164">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="d9aab-165">Si invita a iniziare a esplorare DWriteCore e a fornire informazioni dettagliate o richieste sullo sviluppo di funzionalità nel [repository GitHub Project GitHub.](https://github.com/microsoft/ProjectReunion/)</span><span class="sxs-lookup"><span data-stu-id="d9aab-165">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="d9aab-166">Programmazione con DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9aab-166">Programming with DWriteCore</span></span>

<span data-ttu-id="d9aab-167">Proprio come con [DirectWrite,](./direct-write-portal.md)è possibile programmare con DWriteCore tramite la relativa API com-light, tramite [**l'interfaccia IDWriteFactory.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)</span><span class="sxs-lookup"><span data-stu-id="d9aab-167">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="d9aab-168">Per usare DWriteCore, è necessario includere il `dwrite_core.h` file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="d9aab-168">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="d9aab-169">Il `dwrite_core.h` file di intestazione definisce innanzitutto il token *DWRITE_CORE* e quindi include il file `dwrite_3.h` di intestazione.</span><span class="sxs-lookup"><span data-stu-id="d9aab-169">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes the `dwrite_3.h` header file.</span></span> <span data-ttu-id="d9aab-170">Il *DWRITE_CORE* token è importante, perché indica a tutte le intestazioni incluse successivamente di rendere disponibili tutte le API DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d9aab-170">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="d9aab-171">Dopo che il progetto ha incluso , è possibile procedere `dwrite_core.h` e scrivere codice, compilare ed eseguire.</span><span class="sxs-lookup"><span data-stu-id="d9aab-171">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="d9aab-172">API nuove o diverse per DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9aab-172">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="d9aab-173">La superficie dell'API DWriteCore è in gran parte uguale a come per [DirectWrite.](/windows/win32/api/_directwrite/)</span><span class="sxs-lookup"><span data-stu-id="d9aab-173">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="d9aab-174">Esiste tuttavia un numero ridotto di nuove API attualmente presenti solo in DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="d9aab-174">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-factory-object"></a><span data-ttu-id="d9aab-175">Creare un oggetto factory</span><span class="sxs-lookup"><span data-stu-id="d9aab-175">Create a factory object</span></span>

<span data-ttu-id="d9aab-176">La [**funzione gratuita DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) crea un oggetto factory che viene usato per la creazione successiva di singoli oggetti DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="d9aab-176">The [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) free function creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

<span data-ttu-id="d9aab-177">**DWriteCoreCreateFactory** è funzionalmente uguale alla funzione [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) esportata dalla versione di sistema di DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d9aab-177">**DWriteCoreCreateFactory** is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="d9aab-178">La funzione DWriteCore ha un nome diverso per evitare ambiguità.</span><span class="sxs-lookup"><span data-stu-id="d9aab-178">The DWriteCore function has a different name to avoid ambiguity.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="d9aab-179">Creare un oggetto factory con restrizioni</span><span class="sxs-lookup"><span data-stu-id="d9aab-179">Create a restricted factory object</span></span>

<span data-ttu-id="d9aab-180">L DWRITE_FACTORY_TYPE enumezione ha una nuova costante [](./dwrite/ne-dwrite-dwrite_factory_type.md) &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, che indica una factory con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="d9aab-180">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="d9aab-181">Una factory con restrizioni è più bloccata rispetto a una factory isolata.</span><span class="sxs-lookup"><span data-stu-id="d9aab-181">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="d9aab-182">Non interagisce in alcun modo con una cache dei tipi di carattere multi-processo né persistente.</span><span class="sxs-lookup"><span data-stu-id="d9aab-182">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="d9aab-183">Inoltre, la raccolta di tipi di carattere di sistema restituita da questa factory include solo tipi di carattere noti.</span><span class="sxs-lookup"><span data-stu-id="d9aab-183">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="d9aab-184">Ecco come è possibile usare **DWRITE_FACTORY_TYPE_ISOLATED2** per creare un oggetto factory con restrizioni quando si chiama la funzione [**gratuita DWriteCoreCreateFactory.**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md)</span><span class="sxs-lookup"><span data-stu-id="d9aab-184">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="d9aab-185">Se si passa **DWRITE_FACTORY_TYPE_ISOLATED2** a una versione precedente di DirectWrite che non la **supporta,** **DWriteCreateFactory** restituisce E_INVALIDARG .</span><span class="sxs-lookup"><span data-stu-id="d9aab-185">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="d9aab-186">Disegno di glifi in una bitmap della memoria di sistema</span><span class="sxs-lookup"><span data-stu-id="d9aab-186">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="d9aab-187">DirectWrite ha un'interfaccia di destinazione di rendering bitmap che supporta il rendering dei glifi in una bitmap nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="d9aab-187">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="d9aab-188">Tuttavia, attualmente l'unico modo per ottenere l'accesso ai dati pixel sottostanti è passare attraverso GDI e quindi l'API non è utilizzabile multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="d9aab-188">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="d9aab-189">Questo problema si può risolvere facilmente aggiungendo un metodo per recuperare i dati pixel.</span><span class="sxs-lookup"><span data-stu-id="d9aab-189">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="d9aab-190">DWriteCore introduce quindi [**l'interfaccia IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) e il relativo [**metodo IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="d9aab-190">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="d9aab-191">Tale metodo accetta un parametro di tipo (puntatore a) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), che è un nuovo struct.</span><span class="sxs-lookup"><span data-stu-id="d9aab-191">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="d9aab-192">L'applicazione crea una destinazione di rendering bitmap chiamando [IDWriteGdiInterop::CreateBitmapRenderTarget.](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)</span><span class="sxs-lookup"><span data-stu-id="d9aab-192">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="d9aab-193">In Windows, una destinazione di rendering bitmap incapsula un controller di dominio di memoria GDI con una bitmap GDI indipendente dal dispositivo (DIB) selezionata al suo interno.</span><span class="sxs-lookup"><span data-stu-id="d9aab-193">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="d9aab-194">[IDWriteBitmapRenderTarget::D rawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) esegue il rendering dei glifi nel DIB.</span><span class="sxs-lookup"><span data-stu-id="d9aab-194">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="d9aab-195">DirectWrite esegue il rendering dei glifi senza passare attraverso GDI.</span><span class="sxs-lookup"><span data-stu-id="d9aab-195">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="d9aab-196">L'applicazione può quindi ottenere **l'HDC** dalla destinazione di rendering bitmap e usare [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) per copiare i pixel in una **finestra HDC.**</span><span class="sxs-lookup"><span data-stu-id="d9aab-196">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="d9aab-197">Nelle piattaforme non Windows, l'applicazione può comunque creare una destinazione di rendering bitmap, ma incapsula semplicemente una matrice di memoria di sistema senza **HDC** e senza DIB.</span><span class="sxs-lookup"><span data-stu-id="d9aab-197">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="d9aab-198">Senza un **HDC,** l'applicazione deve avere un altro modo per ottenere i pixel bitmap in modo che possa copiarli o usarli in altro modo.</span><span class="sxs-lookup"><span data-stu-id="d9aab-198">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="d9aab-199">Anche in Windows, a volte è utile ottenere i dati pixel effettivi e viene illustrato il modo corrente per eseguire questa operazione nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="d9aab-199">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="d9aab-200">Altre differenze delle API tra DWriteCore e DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d9aab-200">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="d9aab-201">Esistono alcune API che sono solo stub o si comportano in modo leggermente diverso su piattaforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="d9aab-201">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="d9aab-202">Ad esempio, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) restituisce **E_NOTIMPL** su piattaforme non Windows, poiché non esiste un **HDC** senza [GDI.](../gdi/windows-gdi.md)</span><span class="sxs-lookup"><span data-stu-id="d9aab-202">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="d9aab-203">Infine, esistono alcune altre API di Windows che vengono in genere usate insieme a DirectWrite (Direct2D è un esempio di grande impatto).</span><span class="sxs-lookup"><span data-stu-id="d9aab-203">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="d9aab-204">Tuttavia, attualmente Direct2D e DWriteCore non interoperativizzano.</span><span class="sxs-lookup"><span data-stu-id="d9aab-204">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="d9aab-205">Ad esempio, se si crea un [**oggetto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando DWriteCore e lo si passa a [**D2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d9aab-205">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>
