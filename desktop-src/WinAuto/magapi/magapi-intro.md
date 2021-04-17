---
title: Panoramica dell'API di ingrandimento
description: Questo argomento descrive l'API di ingrandimento e spiega come usarlo in un'applicazione.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Ingrandimento
- applicazioni di ingrandimento schermo
- Ingrandimento
- elaborazione di immagini personalizzate
- Magnification.dll
- creazione di controlli Magnifier
- ingrandimento selettivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300038"
---
# <a name="magnification-api-overview"></a><span data-ttu-id="f7102-110">Panoramica dell'API di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="f7102-110">Magnification API Overview</span></span>

<span data-ttu-id="f7102-111">L'API di ingrandimento consente ai fornitori di Assistive Technology di sviluppare applicazioni di ingrandimento dello schermo eseguite in Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f7102-111">The Magnification API enables assistive technology vendors to develop screen magnification applications that run on Microsoft Windows.</span></span> <span data-ttu-id="f7102-112">Questo argomento descrive l'API di ingrandimento e spiega come usarlo in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7102-112">This topic describes the Magnification API and explains how to use it in an application.</span></span> <span data-ttu-id="f7102-113">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7102-113">It contains the following sections:</span></span>

- [<span data-ttu-id="f7102-114">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="f7102-114">Getting Started</span></span>](#getting-started)
- [<span data-ttu-id="f7102-115">Concetti di base</span><span class="sxs-lookup"><span data-stu-id="f7102-115">Basic Concepts</span></span>](#basic-concepts)
  - [<span data-ttu-id="f7102-116">Tipi di lente di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="f7102-116">Types of Magnifiers</span></span>](#types-of-magnifiers)
  - [<span data-ttu-id="f7102-117">Fattore di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="f7102-117">Magnification Factor</span></span>](#magnification-factor)
  - [<span data-ttu-id="f7102-118">Effetti colore</span><span class="sxs-lookup"><span data-stu-id="f7102-118">Color Effects</span></span>](#color-effects)
  - [<span data-ttu-id="f7102-119">Rettangolo di origine</span><span class="sxs-lookup"><span data-stu-id="f7102-119">Source Rectangle</span></span>](#source-rectangle)
  - [<span data-ttu-id="f7102-120">Elenco filtri</span><span class="sxs-lookup"><span data-stu-id="f7102-120">Filter List</span></span>](#filter-list)
  - [<span data-ttu-id="f7102-121">Trasformazione input</span><span class="sxs-lookup"><span data-stu-id="f7102-121">Input Transform</span></span>](#input-transform)
  - [<span data-ttu-id="f7102-122">Cursore di sistema</span><span class="sxs-lookup"><span data-stu-id="f7102-122">System Cursor</span></span>](#system-cursor)
- [<span data-ttu-id="f7102-123">Inizializzazione della libreria di runtime della lente di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="f7102-123">Initializing the Magnifier Run-time Library</span></span>](#initializing-the-magnifier-run-time-library)
- [<span data-ttu-id="f7102-124">Uso di Full-Screen Magnifier</span><span class="sxs-lookup"><span data-stu-id="f7102-124">Using the Full-Screen Magnifier</span></span>](#using-the-full-screen-magnifier)
- [<span data-ttu-id="f7102-125">Uso del controllo Magnifier</span><span class="sxs-lookup"><span data-stu-id="f7102-125">Using the Magnifier Control</span></span>](#using-the-magnifier-control)
  - [<span data-ttu-id="f7102-126">Creazione del controllo Magnifier</span><span class="sxs-lookup"><span data-stu-id="f7102-126">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
  - [<span data-ttu-id="f7102-127">Inizializzazione del controllo</span><span class="sxs-lookup"><span data-stu-id="f7102-127">Initializing the Control</span></span>](#initializing-the-control)
  - [<span data-ttu-id="f7102-128">Impostazione del rettangolo di origine</span><span class="sxs-lookup"><span data-stu-id="f7102-128">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
  - [<span data-ttu-id="f7102-129">Applicazione degli effetti colore</span><span class="sxs-lookup"><span data-stu-id="f7102-129">Applying Color Effects</span></span>](#applying-color-effects)
  - [<span data-ttu-id="f7102-130">Ingrandimento selettivo</span><span class="sxs-lookup"><span data-stu-id="f7102-130">Selective Magnification</span></span>](#selective-magnification)
- [<span data-ttu-id="f7102-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7102-131">Related topics</span></span>](#related-topics)

## <a name="getting-started"></a><span data-ttu-id="f7102-132">Introduzione</span><span class="sxs-lookup"><span data-stu-id="f7102-132">Getting Started</span></span>

<span data-ttu-id="f7102-133">La versione originale dell'API di ingrandimento è supportata in Windows Vista e nei sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="f7102-133">The original release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="f7102-134">In Windows 8 e versioni successive, l'API supporta funzionalità aggiuntive, tra cui l'ingrandimento a schermo intero e l'impostazione della visibilità del cursore di sistema ingrandito.</span><span class="sxs-lookup"><span data-stu-id="f7102-134">On Windows 8 and later, the API supports additional features, including full-screen magnification and setting the visibility of the magnified system cursor.</span></span>

<span data-ttu-id="f7102-135">Il supporto per l'API di ingrandimento è fornito da Magnification.dll.</span><span class="sxs-lookup"><span data-stu-id="f7102-135">Support for the Magnification API is provided by Magnification.dll.</span></span> <span data-ttu-id="f7102-136">Per compilare l'applicazione, includere ingrandimento. h e collegamento a ingrandimento. lib.</span><span class="sxs-lookup"><span data-stu-id="f7102-136">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="f7102-137">L'API di ingrandimento non è supportata in WOW64; ovvero, un'applicazione di Magnifier a 32 bit non verrà eseguita correttamente in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f7102-137">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="basic-concepts"></a><span data-ttu-id="f7102-138">Concetti di base</span><span class="sxs-lookup"><span data-stu-id="f7102-138">Basic Concepts</span></span>

<span data-ttu-id="f7102-139">Questa sezione descrive i concetti fondamentali su cui si basa l'API di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="f7102-139">This section describes the fundamental concepts that the magnification API is based on.</span></span> <span data-ttu-id="f7102-140">Contiene le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7102-140">It contains the following parts:</span></span>

- [<span data-ttu-id="f7102-141">Tipi di lente di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="f7102-141">Types of Magnifiers</span></span>](#types-of-magnifiers)
- [<span data-ttu-id="f7102-142">Fattore di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="f7102-142">Magnification Factor</span></span>](#magnification-factor)
- [<span data-ttu-id="f7102-143">Effetti colore</span><span class="sxs-lookup"><span data-stu-id="f7102-143">Color Effects</span></span>](#color-effects)
- [<span data-ttu-id="f7102-144">Rettangolo di origine</span><span class="sxs-lookup"><span data-stu-id="f7102-144">Source Rectangle</span></span>](#source-rectangle)
- [<span data-ttu-id="f7102-145">Elenco filtri</span><span class="sxs-lookup"><span data-stu-id="f7102-145">Filter List</span></span>](#filter-list)
- [<span data-ttu-id="f7102-146">Trasformazione input</span><span class="sxs-lookup"><span data-stu-id="f7102-146">Input Transform</span></span>](#input-transform)
- [<span data-ttu-id="f7102-147">Cursore di sistema</span><span class="sxs-lookup"><span data-stu-id="f7102-147">System Cursor</span></span>](#system-cursor)

### <a name="types-of-magnifiers"></a><span data-ttu-id="f7102-148">Tipi di lente di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="f7102-148">Types of Magnifiers</span></span>

<span data-ttu-id="f7102-149">L'API supporta due tipi di lente di ingrandimento, il *Magnifier a schermo intero* e il *controllo lente di ingrandimento*.</span><span class="sxs-lookup"><span data-stu-id="f7102-149">The API supports two types of magnifiers, the *full-screen magnifier* and the *magnifier control*.</span></span> <span data-ttu-id="f7102-150">La lente di ingrandimento a schermo intero consente di ingrandire il contenuto dell'intero schermo, mentre il controllo Magnifier ingrandisce il contenuto di una particolare area dello schermo e visualizza il contenuto in una finestra.</span><span class="sxs-lookup"><span data-stu-id="f7102-150">The full-screen magnifier magnifies the content of the entire screen, while the magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="f7102-151">Per entrambe le lenti, le immagini e il testo sono ingranditi ed entrambi consentono di controllare la quantità di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="f7102-151">For both magnifiers, images and text are magnified, and both enable you to control the amount of magnification.</span></span> <span data-ttu-id="f7102-152">È anche possibile applicare effetti cromatici al contenuto della schermata ingrandita, semplificando la visualizzazione per gli utenti che hanno difetti di colore o che necessitano di colori con un contrasto maggiore o minore.</span><span class="sxs-lookup"><span data-stu-id="f7102-152">You can also apply color effects to the magnified screen content, making it easier to see for people who have color deficiencies or need colors that have more or less contrast.</span></span>

> [!Important]  
> <span data-ttu-id="f7102-153">L'API di controllo Magnifier è disponibile in Windows Vista e nei sistemi operativi successivi, mentre l'API di ingrandimento a schermo intero è disponibile solo nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f7102-153">The magnifier control API is available on Windows Vista and later operating systems, while the full-screen magnifier API is available only on Windows 8 and later operating systems.</span></span>

### <a name="magnification-factor"></a><span data-ttu-id="f7102-154">Fattore di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="f7102-154">Magnification Factor</span></span>

<span data-ttu-id="f7102-155">Sia il controllo Magnifier a schermo intero che il controllo Magnifier applicano una trasformazione di ridimensionamento per ingrandire il contenuto dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-155">Both the full-screen magnifier and the magnifier control apply a scale transformation to magnify screen content.</span></span> <span data-ttu-id="f7102-156">La quantità di ingrandimento applicata dalla trasformazione scala è detta *fattore di ingrandimento*.</span><span class="sxs-lookup"><span data-stu-id="f7102-156">The amount of magnification applied by the scale transformation is called the *magnification factor*.</span></span> <span data-ttu-id="f7102-157">Viene espresso come valore a virgola mobile dove 1,0 corrisponde a nessun ingrandimento e i valori più grandi comportano una quantità di ingrandimento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="f7102-157">It is expressed as a floating-point value where 1.0 corresponds to no magnification, and larger values result in a corresponding amount of magnification.</span></span> <span data-ttu-id="f7102-158">Ad esempio, il valore 1,5 rende il contenuto della schermata 50% più grande.</span><span class="sxs-lookup"><span data-stu-id="f7102-158">For example, a value of 1.5 makes the screen content 50 percent larger.</span></span> <span data-ttu-id="f7102-159">Un fattore di ingrandimento inferiore a 1,0 non è valido.</span><span class="sxs-lookup"><span data-stu-id="f7102-159">A magnification factor less than 1.0 is not valid.</span></span>

### <a name="color-effects"></a><span data-ttu-id="f7102-160">Effetti colore</span><span class="sxs-lookup"><span data-stu-id="f7102-160">Color Effects</span></span>

<span data-ttu-id="f7102-161">Gli effetti cromatici si ottengono applicando una matrice di trasformazione dei colori 5 per 5 ai colori del contenuto della schermata ingrandita.</span><span class="sxs-lookup"><span data-stu-id="f7102-161">Color effects are achieved by applying a 5-by-5 color transformation matrix to the colors of the magnified screen content.</span></span> <span data-ttu-id="f7102-162">La matrice determina le intensità dei componenti rosso, blu, verde e alfa del contenuto.</span><span class="sxs-lookup"><span data-stu-id="f7102-162">The matrix determines the intensities of the red, blue, green, and alpha components of the content.</span></span> <span data-ttu-id="f7102-163">Per ulteriori informazioni, vedere [utilizzo di una matrice di colori per trasformare un singolo colore](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) nella documentazione di Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="f7102-163">For more information, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the Windows GDI+ documentation.</span></span>

### <a name="source-rectangle"></a><span data-ttu-id="f7102-164">Rettangolo di origine</span><span class="sxs-lookup"><span data-stu-id="f7102-164">Source Rectangle</span></span>

<span data-ttu-id="f7102-165">La lente di ingrandimento a schermo intero applica la trasformazione scala e la trasformazione colore a tutto lo schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-165">The full-screen magnifier applies the scale transformation and color transformation to the entire screen.</span></span> <span data-ttu-id="f7102-166">Il controllo Magnifier, invece, copia un'area dello schermo, denominata *rettangolo di origine*, in una bitmap fuori schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-166">The magnifier control, on the other hand, copies an area of the screen, called the *source rectangle*, to an off-screen bitmap.</span></span> <span data-ttu-id="f7102-167">Successivamente, il controllo applica la trasformazione di ridimensionamento e la trasformazione del colore, se presente, alla bitmap fuori schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-167">Next, the control applies the scale transformation and the color transformation, if any, to the off-screen bitmap.</span></span> <span data-ttu-id="f7102-168">Infine, il controllo Visualizza la bitmap ridimensionata e con colore trasformato nella finestra di controllo lente di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="f7102-168">Finally, the control displays the scaled and color-transformed bitmap in the magnifier control window.</span></span>

### <a name="filter-list"></a><span data-ttu-id="f7102-169">Elenco filtri</span><span class="sxs-lookup"><span data-stu-id="f7102-169">Filter List</span></span>

<span data-ttu-id="f7102-170">Per impostazione predefinita, il controllo Magnifier ingrandisce tutte le finestre nel rettangolo di origine specificato.</span><span class="sxs-lookup"><span data-stu-id="f7102-170">By default, the magnifier control magnifies all windows in the specified source rectangle.</span></span> <span data-ttu-id="f7102-171">Tuttavia, fornendo un *elenco di filtri* per gli handle di finestra, è possibile controllare quali finestre sono incluse nel contenuto ingrandito e quali non lo sono.</span><span class="sxs-lookup"><span data-stu-id="f7102-171">However, by providing a *filter list* of window handles, you can control which windows are included in the magnified content, and which are not.</span></span> <span data-ttu-id="f7102-172">Per altre informazioni, vedere [ingrandimento selettivo](#selective-magnification).</span><span class="sxs-lookup"><span data-stu-id="f7102-172">For more information, see [Selective Magnification](#selective-magnification).</span></span>

<span data-ttu-id="f7102-173">La lente di ingrandimento a schermo intero non supporta un elenco di filtri; che ingrandisce sempre tutte le finestre sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-173">The full-screen magnifier does not support a filter list; it always magnifies all windows on the screen.</span></span>

### <a name="input-transform"></a><span data-ttu-id="f7102-174">Trasformazione input</span><span class="sxs-lookup"><span data-stu-id="f7102-174">Input Transform</span></span>

<span data-ttu-id="f7102-175">In genere, il contenuto della schermata ingrandita è "invisibile" all'input penna o tocco utente.</span><span class="sxs-lookup"><span data-stu-id="f7102-175">Normally, magnified screen content is "invisible" to user pen or touch input.</span></span> <span data-ttu-id="f7102-176">Se, ad esempio, l'utente tocca l'immagine ingrandita di un controllo, il sistema non passa necessariamente l'input al controllo.</span><span class="sxs-lookup"><span data-stu-id="f7102-176">For example, if the user taps the magnified image of a control, the system does not necessarily pass the input to the control.</span></span> <span data-ttu-id="f7102-177">Il sistema passa invece l'input a qualsiasi elemento, se presente, che si trova in corrispondenza delle coordinate dello schermo toccato sul desktop non ingrandito.</span><span class="sxs-lookup"><span data-stu-id="f7102-177">Instead, the system passes the input to whatever item (if any) resides at the tapped screen coordinates on the unmagnified desktop.</span></span> <span data-ttu-id="f7102-178">La funzione [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) consente di specificare una *trasformazione di input* che esegue il mapping dello spazio delle coordinate del contenuto della schermata ingrandita allo spazio delle coordinate dello schermo effettivo (non ingrandito).</span><span class="sxs-lookup"><span data-stu-id="f7102-178">The [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) function enables you to specify an *input transformation* that maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space.</span></span> <span data-ttu-id="f7102-179">In questo modo, il sistema può passare l'input penna o tocco immesso nel contenuto della schermata ingrandita all'elemento dell'interfaccia utente corretto sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-179">This enables the system to pass pen or touch input that is entered in magnified screen content, to the correct UI element on the screen.</span></span>

> [!Note]  
> <span data-ttu-id="f7102-180">Il processo chiamante deve disporre dei privilegi UIAccess per impostare la trasformazione di input.</span><span class="sxs-lookup"><span data-stu-id="f7102-180">The calling process must have UIAccess privileges to set the input transform.</span></span> <span data-ttu-id="f7102-181">Per ulteriori informazioni, vedere l'articolo relativo alle [considerazioni sulla sicurezza di automazione interfaccia utente](../uiauto-securityoverview.md) e [/MANIFESTUAC (incorporare informazioni sul controllo dell'account utente nel manifesto)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest)</span><span class="sxs-lookup"><span data-stu-id="f7102-181">For more information, see [UI Automation Security Considerations](../uiauto-securityoverview.md) and [/MANIFESTUAC (Embeds UAC information in manifest)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span></span>

### <a name="system-cursor"></a><span data-ttu-id="f7102-182">Cursore di sistema</span><span class="sxs-lookup"><span data-stu-id="f7102-182">System Cursor</span></span>

<span data-ttu-id="f7102-183">La funzione [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) consente di visualizzare o nascondere il cursore di sistema.</span><span class="sxs-lookup"><span data-stu-id="f7102-183">The [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function enables you to show or hide the system cursor.</span></span> <span data-ttu-id="f7102-184">Se si Visualizza il cursore di sistema quando la lente di ingrandimento a schermo intero è attiva, il cursore di sistema viene sempre ingrandito insieme al resto del contenuto dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-184">If you show the system cursor when the full-screen magnifier is active, the system cursor is always magnified along with the rest of the screen content.</span></span> <span data-ttu-id="f7102-185">Se si nasconde il cursore di sistema quando la lente di ingrandimento a schermo intero è attiva, il cursore di sistema non è visibile.</span><span class="sxs-lookup"><span data-stu-id="f7102-185">If you hide the system cursor when the full-screen magnifier is active, the system cursor is not visible at all.</span></span>

<span data-ttu-id="f7102-186">Con il controllo Magnifier, la funzione [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) Mostra o nasconde il cursore di sistema non ingrandito, ma non ha alcun effetto sul cursore di sistema ingrandito.</span><span class="sxs-lookup"><span data-stu-id="f7102-186">With the magnifier control, the [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function shows or hides the unmagnified system cursor, but has no effect on the magnified system cursor.</span></span> <span data-ttu-id="f7102-187">La visibilità del cursore di sistema ingrandito varia a seconda che il controllo Magnifier abbia lo stile [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f7102-187">The visibility of the magnified system cursor depends on whether the magnifier control has the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style.</span></span> <span data-ttu-id="f7102-188">Se ha questo stile, il controllo Magnifier Visualizza il cursore di sistema ingrandito, insieme al contenuto della schermata ingrandita, ogni volta che il cursore di sistema immette il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="f7102-188">If it has this style, the magnifier control displays the magnified system cursor, along with the magnified screen content, whenever the system cursor enters the source rectangle.</span></span>

## <a name="initializing-the-magnifier-run-time-library"></a><span data-ttu-id="f7102-189">Inizializzazione della libreria di runtime della lente di ingrandimento</span><span class="sxs-lookup"><span data-stu-id="f7102-189">Initializing the Magnifier Run-time Library</span></span>

<span data-ttu-id="f7102-190">Prima di poter chiamare qualsiasi altra funzione API Magnifier, è necessario creare e inizializzare gli oggetti di runtime della lente di ingrandimento chiamando la funzione [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) .</span><span class="sxs-lookup"><span data-stu-id="f7102-190">Before you can call any other magnifier API functions, you must create and initialize the magnifier run-time objects by calling the [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) function.</span></span> <span data-ttu-id="f7102-191">Analogamente, dopo aver completato l'utilizzo dell'API Magnifier, chiamare la funzione [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) per eliminare gli oggetti di runtime della lente di ingrandimento e liberare le risorse di sistema associate.</span><span class="sxs-lookup"><span data-stu-id="f7102-191">Similarly, after you finish using the magnifier API, call the [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) function to destroy the magnifier run-time objects and free the associated system resources.</span></span>

## <a name="using-the-full-screen-magnifier"></a><span data-ttu-id="f7102-192">Uso di Full-Screen Magnifier</span><span class="sxs-lookup"><span data-stu-id="f7102-192">Using the Full-Screen Magnifier</span></span>

<span data-ttu-id="f7102-193">Per usare la funzione di ingrandimento a schermo intero, chiamare la funzione [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) .</span><span class="sxs-lookup"><span data-stu-id="f7102-193">To use the full-screen magnifier, call the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function.</span></span> <span data-ttu-id="f7102-194">Il parametro *magLevel* specifica il fattore di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="f7102-194">The *magLevel* parameter specifies the magnification factor.</span></span> <span data-ttu-id="f7102-195">I parametri *xoffset* e *yoffset* specificano in che modo il contenuto della schermata ingrandita è posizionato rispetto allo schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-195">The *xOffset* and *yOffset* parameters specify how the magnified screen content is positioned relative to the screen.</span></span>

<span data-ttu-id="f7102-196">Quando il contenuto della schermata viene ingrandito, diventa più grande della schermata stessa.</span><span class="sxs-lookup"><span data-stu-id="f7102-196">When the screen content is magnified, it becomes larger than the screen itself.</span></span> <span data-ttu-id="f7102-197">Una parte del contenuto si estende oltre i bordi dello schermo e diventa invisibile per l'utente.</span><span class="sxs-lookup"><span data-stu-id="f7102-197">Some portion of the content extends beyond the edges of the screen and becomes invisible to the user.</span></span> <span data-ttu-id="f7102-198">I parametri *xoffset* e *YOffset* della funzione [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) determinano quale parte del contenuto della schermata ingrandita viene visualizzata sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-198">The *xOffset* and *yOffset* parameters of the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function determine which portion of the magnified screen content appears on the screen.</span></span> <span data-ttu-id="f7102-199">Insieme, i parametri specificano le coordinate di un punto nel contenuto della schermata non ingrandita.</span><span class="sxs-lookup"><span data-stu-id="f7102-199">Together, the parameters specify the coordinates of a point in the unmagnified screen content.</span></span> <span data-ttu-id="f7102-200">Quando il contenuto viene ingrandito, viene posizionato con il punto specificato nell'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-200">When the content is magnified, it is positioned with the specified point at the upper-left corner of the screen.</span></span>

<span data-ttu-id="f7102-201">Nell'esempio seguente viene impostato il fattore di ingrandimento per il magnifier a schermo intero e il centro del contenuto della schermata ingrandita al centro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-201">The following example sets the magnification factor for the full-screen magnifier and places the center of the magnified screen content at the center of the screen.</span></span>

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

<span data-ttu-id="f7102-202">Usare la funzione [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) per applicare gli effetti dei colori al contenuto a schermo intero impostando una matrice di trasformazione dei colori definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7102-202">Use the [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) function to apply color effects to the full-screen content by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="f7102-203">Nell'esempio seguente viene impostata una matrice di trasformazione dei colori che converte i colori in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="f7102-203">For example, the following example sets a color transformation matrix that converts colors to grayscale.</span></span>

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

<span data-ttu-id="f7102-204">È possibile recuperare il fattore di ingrandimento e i valori di offset correnti chiamando la funzione [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) .</span><span class="sxs-lookup"><span data-stu-id="f7102-204">You can retrieve the current magnification factor and offset values by calling the [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) function.</span></span> <span data-ttu-id="f7102-205">È possibile recuperare la matrice di trasformazione del colore corrente chiamando la funzione [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) .</span><span class="sxs-lookup"><span data-stu-id="f7102-205">You can retrieve the current color transformation matrix by calling the [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) function.</span></span>

## <a name="using-the-magnifier-control"></a><span data-ttu-id="f7102-206">Uso del controllo Magnifier</span><span class="sxs-lookup"><span data-stu-id="f7102-206">Using the Magnifier Control</span></span>

<span data-ttu-id="f7102-207">Il controllo Magnifier ingrandisce il contenuto di una particolare area dello schermo e visualizza il contenuto in una finestra.</span><span class="sxs-lookup"><span data-stu-id="f7102-207">The magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="f7102-208">Questa sezione descrive come usare il controllo Magnifier.</span><span class="sxs-lookup"><span data-stu-id="f7102-208">This section describes how to use the magnifier control.</span></span> <span data-ttu-id="f7102-209">Contiene le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7102-209">It contains the following parts:</span></span>

- [<span data-ttu-id="f7102-210">Creazione del controllo Magnifier</span><span class="sxs-lookup"><span data-stu-id="f7102-210">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
- [<span data-ttu-id="f7102-211">Inizializzazione del controllo</span><span class="sxs-lookup"><span data-stu-id="f7102-211">Initializing the Control</span></span>](#initializing-the-control)
- [<span data-ttu-id="f7102-212">Impostazione del rettangolo di origine</span><span class="sxs-lookup"><span data-stu-id="f7102-212">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
- [<span data-ttu-id="f7102-213">Applicazione degli effetti colore</span><span class="sxs-lookup"><span data-stu-id="f7102-213">Applying Color Effects</span></span>](#applying-color-effects)
- [<span data-ttu-id="f7102-214">Ingrandimento selettivo</span><span class="sxs-lookup"><span data-stu-id="f7102-214">Selective Magnification</span></span>](#selective-magnification)

### <a name="creating-the-magnifier-control"></a><span data-ttu-id="f7102-215">Creazione del controllo Magnifier</span><span class="sxs-lookup"><span data-stu-id="f7102-215">Creating the Magnifier Control</span></span>

<span data-ttu-id="f7102-216">Il controllo Magnifier deve essere ospitato in una finestra creata con lo stile esteso [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f7102-216">The magnifier control must be hosted in a window created with the [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) extended style.</span></span> <span data-ttu-id="f7102-217">Dopo aver creato la finestra host, chiamare [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) per impostare l'opacità della finestra host.</span><span class="sxs-lookup"><span data-stu-id="f7102-217">After creating the host window, call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) to set the opacity of the host window.</span></span> <span data-ttu-id="f7102-218">La finestra host viene in genere impostata sull'opacità completa per impedire la visualizzazione del contenuto della schermata sottostante.</span><span class="sxs-lookup"><span data-stu-id="f7102-218">The host window is typically set to full opacity to prevent the underlying screen content from showing though.</span></span> <span data-ttu-id="f7102-219">Nell'esempio seguente viene illustrato come impostare la finestra host sull'opacità completa:</span><span class="sxs-lookup"><span data-stu-id="f7102-219">The following example shows how to set the host window to full opacity:</span></span>

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

<span data-ttu-id="f7102-220">Se si applica lo stile [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) alla finestra host, i clic del mouse vengono passati all'oggetto che si trova dietro la finestra host nella posizione del cursore del mouse.</span><span class="sxs-lookup"><span data-stu-id="f7102-220">If you apply the [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) style to the host window, mouse clicks are passed to whatever object is behind the host window at the location of the mouse cursor.</span></span> <span data-ttu-id="f7102-221">Tenere presente che, poiché la finestra host non elabora i clic del mouse, l'utente non sarà in grado di spostare o ridimensionare la finestra di ingrandimento tramite il mouse.</span><span class="sxs-lookup"><span data-stu-id="f7102-221">Be aware that, because the host window does not process mouse clicks, the user will not be able to move or resize the magnification window by using the mouse.</span></span>

<span data-ttu-id="f7102-222">La classe Window della finestra di controllo Magnifier deve essere **WC_MAGNIFIER**.</span><span class="sxs-lookup"><span data-stu-id="f7102-222">The window class of the magnifier control window must be **WC_MAGNIFIER**.</span></span> <span data-ttu-id="f7102-223">Se si applica lo stile [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) , il controllo Magnifier include il cursore di sistema nel contenuto della schermata ingrandita e il cursore viene ingrandito insieme al contenuto dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f7102-223">If you apply the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style, the magnifier control includes the system cursor in the magnified screen contents, and the cursor is magnified along with the screen contents.</span></span>

<span data-ttu-id="f7102-224">Dopo aver creato il controllo Magnifier, mantenerlo in modo che sia possibile passarlo ad altre funzioni.</span><span class="sxs-lookup"><span data-stu-id="f7102-224">After you create the magnifier control, keep the window handle so that you can pass it to other functions.</span></span>

<span data-ttu-id="f7102-225">Nell'esempio seguente viene illustrato come creare il controllo Magnifier.</span><span class="sxs-lookup"><span data-stu-id="f7102-225">The following example shows how to create the magnifier control.</span></span>

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a><span data-ttu-id="f7102-226">Inizializzazione del controllo</span><span class="sxs-lookup"><span data-stu-id="f7102-226">Initializing the Control</span></span>

<span data-ttu-id="f7102-227">Dopo aver creato il controllo Magnifier, è necessario chiamare la funzione [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) per specificare il fattore di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="f7102-227">After creating the magnifier control, you must call the [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) function to specify the magnification factor.</span></span> <span data-ttu-id="f7102-228">Si tratta semplicemente di specificare una matrice di</span><span class="sxs-lookup"><span data-stu-id="f7102-228">This is simply a matter of specifying a matrix of</span></span>

<span data-ttu-id="f7102-229">(*n*, 0,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="f7102-229">(*n*, 0.0, 0.0)</span></span>

<span data-ttu-id="f7102-230">(0,0, *n*, 0,0)</span><span class="sxs-lookup"><span data-stu-id="f7102-230">(0.0, *n*, 0.0)</span></span>

<span data-ttu-id="f7102-231">(0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="f7102-231">(0.0, 0.0, 1.0)</span></span>

<span data-ttu-id="f7102-232">dove *n* è il fattore di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="f7102-232">where *n* is the magnification factor.</span></span>

<span data-ttu-id="f7102-233">Nell'esempio seguente viene illustrato come impostare il fattore di ingrandimento per il controllo Magnifier.</span><span class="sxs-lookup"><span data-stu-id="f7102-233">The following example shows how to set the magnification factor for the magnifier control.</span></span>

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a><span data-ttu-id="f7102-234">Impostazione del rettangolo di origine</span><span class="sxs-lookup"><span data-stu-id="f7102-234">Setting the Source Rectangle</span></span>

<span data-ttu-id="f7102-235">Quando l'utente sposta il cursore del mouse intorno allo schermo, l'applicazione chiama la funzione [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) per specificare la parte della schermata sottostante da ingrandire.</span><span class="sxs-lookup"><span data-stu-id="f7102-235">As the user moves the mouse cursor around the screen, your application calls the [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) function to specify the part of the underlying screen that is to be magnified.</span></span>

<span data-ttu-id="f7102-236">La funzione di esempio seguente calcola la posizione e le dimensioni del rettangolo di origine (in base alla posizione del mouse e alle dimensioni della finestra di ingrandimento divisa per il fattore di ingrandimento) e imposta di conseguenza il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="f7102-236">The following example function calculates the position and dimensions of the source rectangle (based on the mouse position and the dimensions of the magnifier window divided by the magnification factor) and sets the source rectangle accordingly.</span></span> <span data-ttu-id="f7102-237">La funzione centra anche l'area client della finestra host nella posizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="f7102-237">The function also centers the client area of the host window at the mouse position.</span></span> <span data-ttu-id="f7102-238">Questa funzione verrebbe chiamata a intervalli per aggiornare la finestra di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="f7102-238">This function would be called at intervals to update the magnification window.</span></span>

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a><span data-ttu-id="f7102-239">Applicazione degli effetti colore</span><span class="sxs-lookup"><span data-stu-id="f7102-239">Applying Color Effects</span></span>

<span data-ttu-id="f7102-240">Un controllo Magnifier con lo stile [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) applica una matrice di trasformazione dei colori incorporata che inverte i colori del contenuto della schermata ingrandita.</span><span class="sxs-lookup"><span data-stu-id="f7102-240">A magnifier control that has the [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) style applies a built-in color transformation matrix that inverts the colors of the magnified screen content.</span></span> <span data-ttu-id="f7102-241">Nella figura seguente viene illustrato il contenuto della schermata in un controllo Magnifier con lo stile **MS_INVERTCOLORS** .</span><span class="sxs-lookup"><span data-stu-id="f7102-241">The following illustration shows screen content in a magnifier control that has the **MS_INVERTCOLORS** style.</span></span>

![screenshot del contenuto ingrandito con colori invertiti](images/color-inversion.png)

<span data-ttu-id="f7102-243">La funzione [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) consente di applicare altri effetti sui colori impostando una matrice di trasformazione dei colori definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7102-243">The [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) function enables you to apply other color effects by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="f7102-244">La funzione seguente, ad esempio, imposta una matrice di trasformazione dei colori che converte i colori in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="f7102-244">For example, the following function sets a color transformation matrix that converts colors to grayscale.</span></span>


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

<span data-ttu-id="f7102-245">Per ulteriori informazioni sul funzionamento delle trasformazioni dei colori, vedere [utilizzo di una matrice di colori per trasformare un singolo colore](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) nella documentazione di GDI+.</span><span class="sxs-lookup"><span data-stu-id="f7102-245">For more information about how color transformations work, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the GDI+ documentation.</span></span>

### <a name="selective-magnification"></a><span data-ttu-id="f7102-246">Ingrandimento selettivo</span><span class="sxs-lookup"><span data-stu-id="f7102-246">Selective Magnification</span></span>

<span data-ttu-id="f7102-247">Per impostazione predefinita, l'ingrandimento viene applicato a tutte le finestre diverse dalla finestra di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="f7102-247">By default, magnification is applied to all windows other than the magnification window itself.</span></span> <span data-ttu-id="f7102-248">Per specificare le finestre da ingrandire, chiamare la funzione [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) .</span><span class="sxs-lookup"><span data-stu-id="f7102-248">To specify which windows are to be magnified, call the [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) function.</span></span> <span data-ttu-id="f7102-249">Questo metodo accetta un elenco di finestre da ingrandire o un elenco di finestre da escludere dall'ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="f7102-249">This method takes either a list of windows to magnify, or a list of windows to exclude from magnification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7102-250">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7102-250">Related topics</span></span>

[<span data-ttu-id="f7102-251">API Magnification</span><span class="sxs-lookup"><span data-stu-id="f7102-251">Magnification API</span></span>](entry-magapi-sdk.md)