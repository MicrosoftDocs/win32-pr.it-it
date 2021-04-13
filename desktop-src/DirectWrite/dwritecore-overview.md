---
title: Panoramica di DWriteCore
description: DWriteCore è l'implementazione del progetto di riunione di DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 12/09/2020
ms.openlocfilehash: 605cab8d0cd0511b5ca3b0b14d517cdc3f290573
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351036"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="c3af1-105">Panoramica di DWriteCore</span><span class="sxs-lookup"><span data-stu-id="c3af1-105">DWriteCore overview</span></span>

<span data-ttu-id="c3af1-106">DWriteCore è l'implementazione del [progetto di riunione](/windows/apps/project-reunion/) di [DirectWrite](./direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="c3af1-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md).</span></span> <span data-ttu-id="c3af1-107">DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme.</span><span class="sxs-lookup"><span data-stu-id="c3af1-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="c3af1-108">In questo argomento introduttivo viene descritto che cos'è DWriteCore e viene illustrato come installarlo nel proprio ambiente di sviluppo e come programma.</span><span class="sxs-lookup"><span data-stu-id="c3af1-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="c3af1-109">Proposta di valore di DWriteCore</span><span class="sxs-lookup"><span data-stu-id="c3af1-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="c3af1-110">[DirectWrite](./direct-write-portal.md) supporta una vasta gamma di funzionalità che lo rendono lo strumento di rendering dei tipi di carattere preferito in Windows per la maggior parte delle app &mdash; , sia tramite chiamate dirette che tramite [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="c3af1-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="c3af1-111">DirectWrite include un sistema di layout del testo indipendente dal dispositivo, un sottopixel di qualità elevata per il rendering del testo di [Microsoft ClearType](/typography/cleartype/) , un testo con accelerazione hardware, testo in più formati, funzionalità [OpenType®](/typography/opentype/) tipografiche avanzate, supporto del linguaggio Wide e layout e rendering compatibili con [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="c3af1-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="c3af1-112">DirectWrite è stato disponibile a partire da Windows Vista SP2 e si è evoluto nel corso degli anni per includere funzionalità più avanzate, ad esempio tipi di carattere variabili, che consentono agli sviluppatori di applicare stili, pesi e altri attributi a un tipo di carattere con una sola risorsa del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="c3af1-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables developers to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="c3af1-113">A causa della durata prolungata di DirectWrite, tuttavia, gli anticipi nello sviluppo hanno avuto la tendenza a lasciare le versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="c3af1-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="c3af1-114">Inoltre, lo stato di DirectWrite come tecnologia di rendering del testo Premier è limitato solo a Windows, lasciando le applicazioni multipiattaforma a scrivere il proprio stack di rendering del testo o a utilizzare soluzioni di terze parti.</span><span class="sxs-lookup"><span data-stu-id="c3af1-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="c3af1-115">DWriteCore risolve i problemi fondamentali di isolamento delle funzionalità di versione e compatibilità multipiattaforma rimuovendo la libreria dal sistema e indirizzando tutti i possibili endpoint supportati.</span><span class="sxs-lookup"><span data-stu-id="c3af1-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="c3af1-116">A tal fine, DWriteCore è stato integrato in Project Reunion con un'API pubblica supportata su tutti gli endpoint di Windows fino a Windows 8 e apre la porta per l'uso multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="c3af1-116">To that end, we've integrated DWriteCore into Project Reunion with a public API that's supported on all Windows endpoints down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="c3af1-117">Il valore principale che DWriteCore fornisce, come sviluppatore, in Project Reunion è che fornisce l'accesso a tutte le funzionalità di DirectWrite correnti, fino a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c3af1-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to all current DirectWrite features all the way down-level to Windows 8.</span></span> <span data-ttu-id="c3af1-118">Tutte le funzionalità di DWriteCore funzioneranno in tutte le versioni di livello inferiore. in altre parole, tutte le funzionalità correnti funzioneranno in Windows 8, 8,1 e in tutte le versioni di Windows 10, senza alcuna disparità in merito alle funzionalità che possono funzionare per le versioni.</span><span class="sxs-lookup"><span data-stu-id="c3af1-118">All features of DWriteCore will function the same on all down-level versions; in other words, all current features will work on Windows 8, 8.1, and all versions of Windows 10, without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="c3af1-119">App demo DWriteCore &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="c3af1-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="c3af1-120">DWriteCore viene illustrato tramite l'app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , disponibile per il download e lo studio.</span><span class="sxs-lookup"><span data-stu-id="c3af1-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="c3af1-121">Introduzione a DWriteCore</span><span class="sxs-lookup"><span data-stu-id="c3af1-121">Get started with DWriteCore</span></span>

<span data-ttu-id="c3af1-122">Per la versione preliminare del progetto Reunion 0,1, attualmente non è supportata l'installazione del pacchetto NuGet di riunione del progetto nei propri progetti.</span><span class="sxs-lookup"><span data-stu-id="c3af1-122">For the Project Reunion 0.1 Prerelease, we currently don't support installing the Project Reunion NuGet package into your own projects.</span></span> <span data-ttu-id="c3af1-123">Al contrario, l'opzione attualmente supportata per la programmazione personalizzata con DWriteCore consiste nell'iniziare con il progetto di app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) e basare lo sviluppo su tale progetto.</span><span class="sxs-lookup"><span data-stu-id="c3af1-123">Instead, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span>

<span data-ttu-id="c3af1-124">È quindi possibile rimuovere qualsiasi codice sorgente (o file) esistente dal progetto di esempio e aggiungere eventuali nuovi codici sorgente (o file) al progetto.</span><span class="sxs-lookup"><span data-stu-id="c3af1-124">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span> <span data-ttu-id="c3af1-125">Per ulteriori informazioni sulla programmazione con DWriteCore, vedere la sezione [Programming with DWriteCore](#programming-with-dwritecore) più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="c3af1-125">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="c3af1-126">Fasi di rilascio di DWriteCore</span><span class="sxs-lookup"><span data-stu-id="c3af1-126">The release phases of DWriteCore</span></span>

<span data-ttu-id="c3af1-127">Il porting di DirectWrite a DWriteCore è un progetto sufficientemente grande per estendere più cicli di rilascio di Windows.</span><span class="sxs-lookup"><span data-stu-id="c3af1-127">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="c3af1-128">Il progetto è suddiviso in fasi, ciascuna delle quali corrisponde a un blocco di funzionalità fornito in una versione.</span><span class="sxs-lookup"><span data-stu-id="c3af1-128">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="c3af1-129">Funzionalità nella versione corrente di DWriteCore</span><span class="sxs-lookup"><span data-stu-id="c3af1-129">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="c3af1-130">La versione di DWriteCore attualmente disponibile contiene gli strumenti di base che gli sviluppatori hanno bisogno di utilizzare DWriteCore, incluse le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="c3af1-130">The version of DWriteCore currently available contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="c3af1-131">Enumerazione del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="c3af1-131">Font enumeration.</span></span>
- <span data-ttu-id="c3af1-132">API del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="c3af1-132">Font API.</span></span>
- <span data-ttu-id="c3af1-133">Shaping.</span><span class="sxs-lookup"><span data-stu-id="c3af1-133">Shaping.</span></span>
- <span data-ttu-id="c3af1-134">API per il rendering di basso livello.</span><span class="sxs-lookup"><span data-stu-id="c3af1-134">Low-level rendering APIs.</span></span> <span data-ttu-id="c3af1-135">Questa operazione è parziale alla fase corrente &mdash; DWriteCore non interagisce con [Direct2D](../direct2d/direct2d-portal.md), ma è possibile usare [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="c3af1-135">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="c3af1-136">Funzionalità di layout del testo di base.</span><span class="sxs-lookup"><span data-stu-id="c3af1-136">Basic text layout functionality.</span></span>
- <span data-ttu-id="c3af1-137">API per il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="c3af1-137">Text-rendering APIs.</span></span>
- <span data-ttu-id="c3af1-138">Destinazione di rendering bitmap.</span><span class="sxs-lookup"><span data-stu-id="c3af1-138">Bitmap render target.</span></span>
- <span data-ttu-id="c3af1-139">Tipi di carattere colore.</span><span class="sxs-lookup"><span data-stu-id="c3af1-139">Color fonts.</span></span>
- <span data-ttu-id="c3af1-140">Ottimizzazioni varie (pulizia della cache dei tipi di carattere, caricatore del tipo di carattere in memoria e così via).</span><span class="sxs-lookup"><span data-stu-id="c3af1-140">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="c3af1-141">La funzionalità banner in questa fase è il colore dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="c3af1-141">The banner feature at this stage is color fonts.</span></span> <span data-ttu-id="c3af1-142">I tipi di carattere colori consentono di eseguire il rendering dei tipi di carattere con funzionalità di colore più sofisticate, oltre a semplici colori singoli</span><span class="sxs-lookup"><span data-stu-id="c3af1-142">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="c3af1-143">Ad esempio, i tipi di carattere a colori sono la capacità di eseguire il rendering dei tipi di carattere emoji e dell'icona della barra degli strumenti, ad esempio il secondo utilizzato da Office.</span><span class="sxs-lookup"><span data-stu-id="c3af1-143">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="c3af1-144">I tipi di carattere di colore sono stati introdotti per la prima volta in Windows 8.1, ma la funzionalità è stata notevolmente espansa in Windows 10, versione 1607 (aggiornamento dell'anniversario).</span><span class="sxs-lookup"><span data-stu-id="c3af1-144">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="c3af1-145">Il lavoro di pulizia della cache dei tipi di carattere e del caricatore del tipo di carattere in memoria consente un caricamento più rapido dei tipi di carattere e i miglioramenti della memoria.</span><span class="sxs-lookup"><span data-stu-id="c3af1-145">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="c3af1-146">Grazie a queste funzionalità, è possibile iniziare subito a sfruttare alcune delle funzionalità di base moderne di DirectWrite, &mdash; ad esempio i tipi di carattere variabili &mdash; di livello inferiore a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c3af1-146">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts&mdash;down-level to Windows 8.</span></span> <span data-ttu-id="c3af1-147">Questa iterazione della libreria può essere usata anche in [Android](https://www.android.com/)e **Linux**.</span><span class="sxs-lookup"><span data-stu-id="c3af1-147">This iteration of the library can also be consumed on [Android](https://www.android.com/), and **Linux**.</span></span> <span data-ttu-id="c3af1-148">I tipi di carattere variabili sono una delle funzionalità più importanti per i clienti di DirectWrite. sono stati introdotti in Windows 10, versione 1709 (Fall Creators Update), quindi l'accesso alle versioni precedenti è una grande vantaggio per gli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="c3af1-148">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a massive boon to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="c3af1-149">Il nostro invito per gli sviluppatori DirectWrite</span><span class="sxs-lookup"><span data-stu-id="c3af1-149">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="c3af1-150">DWriteCore, insieme ad altri componenti di riunione del progetto, verranno sviluppati con apertura al feedback degli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="c3af1-150">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="c3af1-151">Ti invitiamo a iniziare a esplorare DWriteCore e a fornire informazioni dettagliate o richieste per lo sviluppo di funzionalità nel [repository GitHub del progetto Reunion](https://github.com/microsoft/ProjectReunion/).</span><span class="sxs-lookup"><span data-stu-id="c3af1-151">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="c3af1-152">Programmazione con DWriteCore</span><span class="sxs-lookup"><span data-stu-id="c3af1-152">Programming with DWriteCore</span></span>

<span data-ttu-id="c3af1-153">Come già indicato, per la versione preliminare del progetto Reunion 0,1, l'opzione attualmente supportata per la programmazione personalizzata con DWriteCore consiste nell'iniziare con il progetto di app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="c3af1-153">As already mentioned, for the Project Reunion 0.1 Prerelease, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project.</span></span>

<span data-ttu-id="c3af1-154">Analogamente a quanto avviene con [DirectWrite](./direct-write-portal.md), è possibile programmare con DWriteCore tramite la relativa API Light com, tramite l'interfaccia [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="c3af1-154">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="c3af1-155">**DWriteCoreGallery** include già il `dwrite_core.h` file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="c3af1-155">**DWriteCoreGallery** already includes the `dwrite_core.h` header file.</span></span> <span data-ttu-id="c3af1-156">Tale intestazione definisce innanzitutto il token *DWRITE_CORE* e quindi include `dwrite_3.h` .</span><span class="sxs-lookup"><span data-stu-id="c3af1-156">That header first defines the token *DWRITE_CORE*, and then it includes `dwrite_3.h`.</span></span> <span data-ttu-id="c3af1-157">Il token *DWRITE_CORE* è importante, perché indirizza le intestazioni incluse successivamente per rendere disponibili tutte le API DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="c3af1-157">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="c3af1-158">Una volta incluso un progetto `dwrite_core.h` , è possibile procedere e scrivere codice, compilare ed eseguire.</span><span class="sxs-lookup"><span data-stu-id="c3af1-158">Once a project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

```cppwinrt
// pch.h
...
#include <dwrite_core.h>
```

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="c3af1-159">API nuove o diverse per DWriteCore</span><span class="sxs-lookup"><span data-stu-id="c3af1-159">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="c3af1-160">La superficie dell'API DWriteCore è sostanzialmente identica a quella di [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="c3af1-160">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="c3af1-161">Tuttavia, esiste un numero ridotto di nuove API che sono presenti solo in DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="c3af1-161">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="c3af1-162">Creare un oggetto factory con restrizioni</span><span class="sxs-lookup"><span data-stu-id="c3af1-162">Create a restricted factory object</span></span>

<span data-ttu-id="c3af1-163">L'enumerazione [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) dispone di una nuova &mdash; **DWRITE_FACTORY_TYPE_RESTRICTED** costante.</span><span class="sxs-lookup"><span data-stu-id="c3af1-163">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_RESTRICTED**.</span></span> <span data-ttu-id="c3af1-164">Una factory con restrizioni è più bloccata rispetto a una factory isolata.</span><span class="sxs-lookup"><span data-stu-id="c3af1-164">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="c3af1-165">Non interagisce in alcun modo con una cache dei tipi di carattere incrociata o persistente.</span><span class="sxs-lookup"><span data-stu-id="c3af1-165">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="c3af1-166">Inoltre, la raccolta di tipi di carattere del sistema restituita da questa Factory include solo tipi di carattere noti.</span><span class="sxs-lookup"><span data-stu-id="c3af1-166">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="c3af1-167">Ecco come è possibile usare **DWRITE_FACTORY_TYPE_RESTRICTED** per creare un oggetto Factory limitato quando si chiama la funzione [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) free.</span><span class="sxs-lookup"><span data-stu-id="c3af1-167">Here's how you can use **DWRITE_FACTORY_TYPE_RESTRICTED** to create a restricted factory object when you call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCreateFactory(
    DWRITE_FACTORY_TYPE_RESTRICTED,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="c3af1-168">Se si passa **DWRITE_FACTORY_TYPE_RESTRICTED** a una versione precedente di DirectWrite che non la supporta, **DWriteCreateFactory** restituisce **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="c3af1-168">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="c3af1-169">Disegno di glifi in una bitmap di memoria di sistema</span><span class="sxs-lookup"><span data-stu-id="c3af1-169">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="c3af1-170">DirectWrite dispone di un'interfaccia di destinazione di rendering bitmap che supporta il rendering di glifi in una bitmap nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="c3af1-170">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="c3af1-171">Attualmente, tuttavia, l'unico modo per ottenere l'accesso ai dati pixel sottostanti consiste nel passare attraverso GDI, quindi l'API non è utilizzabile tra piattaforme diverse.</span><span class="sxs-lookup"><span data-stu-id="c3af1-171">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="c3af1-172">Per ovviare a questo problema, è possibile aggiungere un metodo per recuperare i dati pixel.</span><span class="sxs-lookup"><span data-stu-id="c3af1-172">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="c3af1-173">Quindi DWriteCore introduce l'interfaccia [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) e il relativo metodo [**IDWriteBitmapRenderTarget2:: getbitmapdata**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="c3af1-173">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="c3af1-174">Tale metodo accetta un parametro di tipo (puntatore a) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), che è un nuovo struct.</span><span class="sxs-lookup"><span data-stu-id="c3af1-174">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="c3af1-175">L'applicazione crea una destinazione di rendering bitmap chiamando [IDWriteGdiInterop:: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="c3af1-175">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="c3af1-176">In Windows una destinazione di rendering bitmap incapsula un controller di dominio di memoria GDI con una bitmap indipendente dal dispositivo GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="c3af1-176">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="c3af1-177">[IDWriteBitmapRenderTarget::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) esegue il rendering dei GLIFI in DIB.</span><span class="sxs-lookup"><span data-stu-id="c3af1-177">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="c3af1-178">DirectWrite esegue il rendering dei glifi senza passare attraverso GDI.</span><span class="sxs-lookup"><span data-stu-id="c3af1-178">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="c3af1-179">L'applicazione può quindi ottenere l' **HDC** dalla destinazione di rendering bitmap e usare [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) per copiare i pixel in una finestra **HDC**.</span><span class="sxs-lookup"><span data-stu-id="c3af1-179">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="c3af1-180">Sulle piattaforme non Windows, l'applicazione può comunque creare una destinazione di rendering bitmap, ma incapsula semplicemente una matrice di memoria di sistema senza **HDC** e nessuna DIB.</span><span class="sxs-lookup"><span data-stu-id="c3af1-180">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="c3af1-181">Senza un **HDC**, è necessario un altro modo per consentire all'applicazione di ottenere i pixel della bitmap in modo che possano copiarli o usarli in altro modo.</span><span class="sxs-lookup"><span data-stu-id="c3af1-181">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="c3af1-182">Anche in Windows, è talvolta utile ottenere i dati effettivi dei pixel e viene illustrato il modo corrente per eseguire questa operazione nell'esempio di codice riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c3af1-182">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="c3af1-183">Altre differenze di API tra DWriteCore e DirectWrite</span><span class="sxs-lookup"><span data-stu-id="c3af1-183">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="c3af1-184">Esistono alcune API che sono solo Stub o si comportano in modo diverso nelle piattaforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="c3af1-184">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="c3af1-185">Ad esempio, [IDWriteGdiInterop:: CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) restituisce **E_NOTIMPL** su piattaforme non Windows, dal momento che non esiste alcuna cosa come un **HDC** senza [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="c3af1-185">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="c3af1-186">Infine, esistono alcune altre API Windows che vengono in genere usate insieme a DirectWrite (Direct2D è un esempio importante).</span><span class="sxs-lookup"><span data-stu-id="c3af1-186">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="c3af1-187">Attualmente, Direct2D e DWriteCore, tuttavia, non interagiscono.</span><span class="sxs-lookup"><span data-stu-id="c3af1-187">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="c3af1-188">Se ad esempio si crea un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) con DWriteCore e lo si passa a [**D2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c3af1-188">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>