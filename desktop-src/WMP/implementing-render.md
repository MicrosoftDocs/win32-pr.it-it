---
title: Implementazione di rendering
description: Implementazione di rendering
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- Visualizzazioni, eventi temporizzati
- Visualizzazioni personalizzate, eventi temporizzati
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Visualizzazioni, funzione RenderWindow
- Visualizzazioni personalizzate, funzione RenderWindow
- Funzione di rendering, parametri
- RenderWindow (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046313"
---
# <a name="implementing-render"></a><span data-ttu-id="2ddeb-111">Implementazione di rendering</span><span class="sxs-lookup"><span data-stu-id="2ddeb-111">Implementing Render</span></span>

<span data-ttu-id="2ddeb-112">Il modo più semplice per considerare la programmazione della visualizzazione è che si sta creando un gestore per un evento temporizzato.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-112">The easiest way to think of visualization programming is that you are creating a handler for a timed event.</span></span> <span data-ttu-id="2ddeb-113">A intervalli specifici, Windows Media Player acquisisce uno snapshot dei dati audio che sta eseguendo e fornisce i dati dello snapshot alla visualizzazione attualmente caricata.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-113">At specific intervals, Windows Media Player takes a snapshot of the audio data it is playing, and provides the snapshot data to the currently loaded visualization.</span></span> <span data-ttu-id="2ddeb-114">Questa operazione è simile alla programmazione basata su eventi ed è parte del modello di programmazione di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-114">This is similar to event-driven programming and is part of the programming model of Microsoft Windows.</span></span> <span data-ttu-id="2ddeb-115">Si scrive il codice e si attende che venga chiamato da un particolare evento.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-115">You write code and wait for it to be called by a particular event.</span></span>

<span data-ttu-id="2ddeb-116">Se il codice è un'implementazione della funzione [IWMPEffects:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) per il rendering in modalità senza finestra, riceve i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ddeb-116">If your code is an implementation of the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function for rendering in windowless mode, it receives the following parameters:</span></span>

<span data-ttu-id="2ddeb-117">*TimedLevel*</span><span class="sxs-lookup"><span data-stu-id="2ddeb-117">*TimedLevel*</span></span>

<span data-ttu-id="2ddeb-118">Si tratta di una struttura che definisce i dati audio che verranno analizzati dal codice.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-118">This is a structure that defines the audio data your code will be analyzing.</span></span> <span data-ttu-id="2ddeb-119">La struttura è costituita da due matrici.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-119">The structure is composed of two arrays.</span></span> <span data-ttu-id="2ddeb-120">La prima matrice è basata sulle informazioni sulla frequenza e contiene uno snapshot dello spettro audio diviso in 1024 porzioni.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-120">The first array is based on frequency information and contains a snapshot of the audio spectrum divided into 1024 portions.</span></span> <span data-ttu-id="2ddeb-121">Ogni cella della matrice contiene un valore compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-121">Each cell of the array contains a value from 0 to 255.</span></span> <span data-ttu-id="2ddeb-122">La prima cella inizia a 20 Hz e l'ultimo a 22050 Hz.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-122">The first cell starts at 20 Hz and the last at 22050 Hz.</span></span> <span data-ttu-id="2ddeb-123">La matrice è bidimensionale per rappresentare audio stereo.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-123">The array is two dimensional to represent stereo audio.</span></span> <span data-ttu-id="2ddeb-124">La seconda matrice è basata sulle informazioni sulla forma d'onda e corrisponde alla potenza audio, in cui l'onda è più forte, maggiore è il valore.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-124">The second array is based on waveform information and corresponds to audio power, where the stronger the wave is, the larger the value.</span></span> <span data-ttu-id="2ddeb-125">La matrice di forme d'onda è uno snapshot granulare delle ultime 1024 sezioni di alimentazione audio acquisite a intervalli di tempo molto piccoli.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-125">The waveform array is a granular snapshot of the last 1024 slices of audio power taken at very small time intervals.</span></span> <span data-ttu-id="2ddeb-126">Questa matrice è anche di due dimensioni per rappresentare audio stereo.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-126">This array also is two dimensional to represent stereo audio.</span></span>

<span data-ttu-id="2ddeb-127">*HDC*</span><span class="sxs-lookup"><span data-stu-id="2ddeb-127">*HDC*</span></span>

<span data-ttu-id="2ddeb-128">Si tratta di un handle Microsoft Windows per un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-128">This is a Microsoft Windows handle to a device context.</span></span> <span data-ttu-id="2ddeb-129">In questo modo è possibile identificare la superficie di disegno in Windows.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-129">This gives a way to identify the drawing surface to Windows.</span></span> <span data-ttu-id="2ddeb-130">Non è necessario crearlo, ma è sufficiente utilizzarlo per chiamate di funzioni di disegno specifiche.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-130">You do not need to create it, you just need to use it for specific drawing function calls.</span></span>

<span data-ttu-id="2ddeb-131">*RECT*</span><span class="sxs-lookup"><span data-stu-id="2ddeb-131">*RECT*</span></span>

<span data-ttu-id="2ddeb-132">Si tratta di un rettangolo di Microsoft Windows che definisce la dimensione di una superficie di disegno.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-132">This is a Microsoft Windows rectangle that defines the size of a drawing surface.</span></span> <span data-ttu-id="2ddeb-133">Si tratta di un rettangolo semplice con quattro proprietà: **Left**, **right**, **Top** e **Bottom**.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-133">This is a simple rectangle with four properties: **left**, **right**, **top**, and **bottom**.</span></span> <span data-ttu-id="2ddeb-134">I valori effettivi vengono forniti da Windows Media Player in modo che sia possibile determinare il modo in cui l'utente o lo sviluppatore di Skin ha ridimensionato la finestra da cui verrà disegnato.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-134">The actual values are supplied by Windows Media Player so that you can determine how the user or skin developer has sized the window you will draw on.</span></span> <span data-ttu-id="2ddeb-135">Determina anche la posizione sull'HDC su cui deve essere eseguito il rendering dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-135">It also determines the position on the HDC that the effect is supposed to render on.</span></span>

<span data-ttu-id="2ddeb-136">Se il codice è un'implementazione della funzione **IWMPEffects2:: RenderWindowed** per il rendering in una finestra, riceve i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ddeb-136">If your code is an implementation of the **IWMPEffects2::RenderWindowed** function for rendering in a window, it receives the following parameters:</span></span>

<span data-ttu-id="2ddeb-137">*TimedLevel*</span><span class="sxs-lookup"><span data-stu-id="2ddeb-137">*TimedLevel*</span></span>

<span data-ttu-id="2ddeb-138">Si tratta delle stesse informazioni ricevute dalla funzione **Render** .</span><span class="sxs-lookup"><span data-stu-id="2ddeb-138">This is the same information that the **Render** function receives.</span></span>

<span data-ttu-id="2ddeb-139">*fRequiredRender*</span><span class="sxs-lookup"><span data-stu-id="2ddeb-139">*fRequiredRender*</span></span>

<span data-ttu-id="2ddeb-140">Il parametro *fRequiredRender* informa che la visualizzazione deve essere ridisegnata, ad esempio quando viene trascinata un'altra finestra.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-140">The *fRequiredRender* parameter informs you that your visualization must repaint itself—for example, when another window is dragged over it.</span></span> <span data-ttu-id="2ddeb-141">Quando questo valore è false, è possibile ignorare il codice di rendering se l'elemento multimediale corrente viene arrestato o sospeso.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-141">When this value is false, you can safely skip over the rendering code if the current media item is stopped or paused.</span></span> <span data-ttu-id="2ddeb-142">Ciò consente di evitare l'utilizzo inutilmente di cicli della CPU.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-142">This lets you avoid consuming CPU cycles unnecessarily.</span></span>

<span data-ttu-id="2ddeb-143">Il plug-in di esempio generato dalla procedura guidata plug-in non fornisce un'implementazione personalizzata per **RenderWindowed**.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-143">The sample plug-in generated by the Plug-in Wizard does not provide a custom implementation for **RenderWindowed**.</span></span> <span data-ttu-id="2ddeb-144">Al contrario, il codice del plug-in di esempio recupera il contesto di dispositivo dalla finestra padre fornita da Windows Media Player in [IWMPEffects2:: create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), quindi recupera le dimensioni della finestra padre come struttura Rect, quindi chiama per **eseguire il rendering** usando il contesto di dispositivo, il recto e il puntatore a livello temporizzato da **RenderWindowed**.</span><span class="sxs-lookup"><span data-stu-id="2ddeb-144">Instead, the sample plug-in code retrieves the device context from the parent window provided by Windows Media Player in [IWMPEffects2::Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), then retrieves the dimensions of the parent window as a RECT structure, and then calls through to **Render** using the device context, the RECT, and the timed level pointer from **RenderWindowed**.</span></span>

<span data-ttu-id="2ddeb-145">Nelle sezioni seguenti vengono fornite ulteriori informazioni sull'implementazione di **Render**:</span><span class="sxs-lookup"><span data-stu-id="2ddeb-145">The following sections provide more information about implementing **Render**:</span></span>

-   [<span data-ttu-id="2ddeb-146">Utilizzo di livelli temporizzati</span><span class="sxs-lookup"><span data-stu-id="2ddeb-146">Using Timed Levels</span></span>](using-timed-levels.md)
-   [<span data-ttu-id="2ddeb-147">Uso dei contesti di dispositivo</span><span class="sxs-lookup"><span data-stu-id="2ddeb-147">Using Device Contexts</span></span>](using-device-contexts.md)
-   [<span data-ttu-id="2ddeb-148">Uso di rettangoli</span><span class="sxs-lookup"><span data-stu-id="2ddeb-148">Using Rectangles</span></span>](using-rectangles.md)
-   [<span data-ttu-id="2ddeb-149">Esempio di codice di rendering</span><span class="sxs-lookup"><span data-stu-id="2ddeb-149">Sample Render Code</span></span>](sample-render-code.md)

## <a name="related-topics"></a><span data-ttu-id="2ddeb-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ddeb-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ddeb-151">**Implementazione del codice**</span><span class="sxs-lookup"><span data-stu-id="2ddeb-151">**Implementing Your Code**</span></span>](implementing-your-code.md)
</dt> </dl>

 

 




