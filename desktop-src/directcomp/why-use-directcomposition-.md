---
title: Perché usare DirectComposition
description: In questo argomento vengono descritte le funzionalità e i vantaggi di Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Perché usare DirectComposition
- motivi per usare DirectComposition
- Funzionalità e vantaggi di DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300304"
---
# <a name="why-use-directcomposition"></a><span data-ttu-id="4f1af-106">Perché usare DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="4f1af-106">Why use DirectComposition?</span></span>

> [!NOTE]
> <span data-ttu-id="4f1af-107">Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="4f1af-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="4f1af-108">Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="4f1af-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="4f1af-109">In questo argomento vengono descritte le funzionalità e i vantaggi di Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="4f1af-109">This topic describes the capabilities and benefits of Microsoft DirectComposition.</span></span> <span data-ttu-id="4f1af-110">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f1af-110">It contains the following sections:</span></span>

-   [<span data-ttu-id="4f1af-111">Creare un'interfaccia utente visivamente accattivante</span><span class="sxs-lookup"><span data-stu-id="4f1af-111">Create a visually engaging user interface</span></span>](#create-a-visually-engaging-user-interface)
-   [<span data-ttu-id="4f1af-112">Abilita animazioni complete e uniformi per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="4f1af-112">Enable rich, smooth animations for your application</span></span>](#enable-rich-smooth-animations-for-your-application)
-   [<span data-ttu-id="4f1af-113">Combinare bitmap da un'ampia gamma di origini</span><span class="sxs-lookup"><span data-stu-id="4f1af-113">Combine bitmaps from a variety of sources</span></span>](#combine-bitmaps-from-a-variety-of-sources)
-   [<span data-ttu-id="4f1af-114">Risparmio di memoria tramite l'integrazione con DWM</span><span class="sxs-lookup"><span data-stu-id="4f1af-114">Memory savings though integration with DWM</span></span>](#memory-savings-though-integration-with-dwm)
-   [<span data-ttu-id="4f1af-115">Mantieni gli elementi già disponibili</span><span class="sxs-lookup"><span data-stu-id="4f1af-115">Keep what you already have</span></span>](#keep-what-you-already-have)
-   [<span data-ttu-id="4f1af-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f1af-116">Related topics</span></span>](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a><span data-ttu-id="4f1af-117">Creare un'interfaccia utente visivamente accattivante</span><span class="sxs-lookup"><span data-stu-id="4f1af-117">Create a visually engaging user interface</span></span>

<span data-ttu-id="4f1af-118">DirectComposition consente di combinare e animare gli oggetti [*visivi*](directcomposition-glossary.md) per creare un'interfaccia utente visivamente accattivante per le applicazioni basate su Windows.</span><span class="sxs-lookup"><span data-stu-id="4f1af-118">DirectComposition lets you combine and animate [*visuals*](directcomposition-glossary.md) to create a visually engaging UI for your Windows-based applications.</span></span> <span data-ttu-id="4f1af-119">Può aiutare a offrire all'applicazione un aspetto univoco, definendo un'identità che la distingue dalle altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4f1af-119">It can help give your application a unique look and feel, establishing an identity that sets it apart from other applications.</span></span>

<span data-ttu-id="4f1af-120">DirectComposition può anche semplificare l'uso delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4f1af-120">DirectComposition can also help make your applications easier to use.</span></span> <span data-ttu-id="4f1af-121">Puoi ad esempio usarlo per creare segnali visivi e transizioni di schermata animate che mostrano le relazioni tra gli elementi sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="4f1af-121">For example, you can use it to create visual cues and animated screen transitions that show relationships among items on the screen.</span></span>

## <a name="enable-rich-smooth-animations-for-your-application"></a><span data-ttu-id="4f1af-122">Abilita animazioni complete e uniformi per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="4f1af-122">Enable rich, smooth animations for your application</span></span>

<span data-ttu-id="4f1af-123">DirectComposition è un motore di composizione bitmap a prestazioni elevate che usa grafica con accelerazione hardware per ottenere frequenze di fotogrammi elevate, ottenendo una panoramica uniforme e coerente, uno scorrimento e animazioni di contenuto complesso.</span><span class="sxs-lookup"><span data-stu-id="4f1af-123">DirectComposition is a high-performance bitmap composition engine that uses hardware-accelerated graphics to achieve high frame rates, resulting in smooth and consistent panning, scrolling, and animations of complex content.</span></span> <span data-ttu-id="4f1af-124">Poiché opera su un thread dedicato separato dal thread usato per il rendering dell'interfaccia utente dell'applicazione, DirectComposition non può mai "affamare" il thread dell'interfaccia utente o interferire con la capacità dell'applicazione di disegnare gli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4f1af-124">Because it operates on a dedicated thread that is separate from the thread used to render the application UI, DirectComposition can never "starve" the UI thread or interfere with the application's ability to draw its UI elements.</span></span>

## <a name="combine-bitmaps-from-a-variety-of-sources"></a><span data-ttu-id="4f1af-125">Combinare bitmap da un'ampia gamma di origini</span><span class="sxs-lookup"><span data-stu-id="4f1af-125">Combine bitmaps from a variety of sources</span></span>

<span data-ttu-id="4f1af-126">Molte applicazioni basate su Windows hanno un'interfaccia utente costituita da elementi creati da un'ampia gamma di Framework di grafica diversi.</span><span class="sxs-lookup"><span data-stu-id="4f1af-126">Many Windows-based applications have a UI that consists of elements created by a variety of different graphics frameworks.</span></span> <span data-ttu-id="4f1af-127">Ad esempio, un'applicazione può utilizzare Windows Form per creare una barra di stato, Windows Graphics Device Interface (GDI) per creare il contenuto della finestra principale, Microsoft DirectX per il contenuto grafico e così via.</span><span class="sxs-lookup"><span data-stu-id="4f1af-127">For example, an application might use Windows Forms to create a status bar, Windows Graphics Device Interface (GDI) to create the main window content, Microsoft DirectX for graphics content, and so on.</span></span> <span data-ttu-id="4f1af-128">DirectComposition consente di combinare il contenuto di un'ampia gamma di Framework di grafica e di eseguirne il rendering nella stessa finestra di primo livello o figlio senza doversi preoccupare di ciò che accade se il contenuto di Framework diversi si sovrappone.</span><span class="sxs-lookup"><span data-stu-id="4f1af-128">DirectComposition enables you to combine the content from a variety of graphics frameworks and have it render to the same top-level or child window without needing to worry about what happens if the content from different frameworks overlaps.</span></span>

## <a name="memory-savings-though-integration-with-dwm"></a><span data-ttu-id="4f1af-129">Risparmio di memoria tramite l'integrazione con DWM</span><span class="sxs-lookup"><span data-stu-id="4f1af-129">Memory savings though integration with DWM</span></span>

<span data-ttu-id="4f1af-130">Le composizioni e le animazioni create da DirectComposition vengono passate a un componente incorporato di Windows denominato [Gestione finestre desktop (DWM)](/windows/desktop/dwm/dwm-overview) per il rendering sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="4f1af-130">Compositions and animations created by DirectComposition are passed to a built-in component of Windows called [Desktop Window Manager (DWM)](/windows/desktop/dwm/dwm-overview) for rendering to the screen.</span></span> <span data-ttu-id="4f1af-131">Non sono pertanto necessari particolari componenti di rendering o Framework dell'interfaccia utente nel computer.</span><span class="sxs-lookup"><span data-stu-id="4f1af-131">Therefore, no special rendering components or UI frameworks are required on the computer.</span></span>

## <a name="keep-what-you-already-have"></a><span data-ttu-id="4f1af-132">Mantieni gli elementi già disponibili</span><span class="sxs-lookup"><span data-stu-id="4f1af-132">Keep what you already have</span></span>

<span data-ttu-id="4f1af-133">Il codice dell'interfaccia utente in un'applicazione esistente basata su Windows rappresenta un investimento significativo.</span><span class="sxs-lookup"><span data-stu-id="4f1af-133">The UI code in an existing Windows-based application represents a significant investment.</span></span> <span data-ttu-id="4f1af-134">Nella maggior parte dei casi, DirectComposition consente di comporre e animare il contenuto dell'interfaccia utente esistente.</span><span class="sxs-lookup"><span data-stu-id="4f1af-134">For the most part, DirectComposition lets you compose and animate your existing UI content.</span></span> <span data-ttu-id="4f1af-135">Ciò significa che è possibile usare DirectComposition per apportare aggiornamenti significativi e miglioramenti all'interfaccia utente dell'applicazione senza dover apportare modifiche estese alla base di codice dell'interfaccia utente esistente.</span><span class="sxs-lookup"><span data-stu-id="4f1af-135">This means you can use DirectComposition to make significant updates and enhancements to your application UI without needing to make extensive changes to your existing UI code base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f1af-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f1af-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f1af-137">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="4f1af-137">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 