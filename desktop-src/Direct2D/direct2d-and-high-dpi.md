---
title: Direct2D e High-DPI
description: Viene descritto il modo in cui Direct2D supporta la visualizzazione a DPI elevato.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, High-DPI
- DPI elevato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963402"
---
# <a name="direct2d-and-high-dpi"></a><span data-ttu-id="d10c6-105">Direct2D e High-DPI</span><span class="sxs-lookup"><span data-stu-id="d10c6-105">Direct2D and High-DPI</span></span>

<span data-ttu-id="d10c6-106">La scrittura di un'applicazione in grado di riconoscere DPI è la chiave per rendere l'interfaccia utente (UI) molto coerente in un'ampia gamma di impostazioni di visualizzazione a DPI elevato.</span><span class="sxs-lookup"><span data-stu-id="d10c6-106">Writing a DPI-aware application is the key to making a user interface (UI) look consistently good across a wide variety of high-DPI display settings.</span></span> <span data-ttu-id="d10c6-107">Un'applicazione che non è compatibile con DPI ma è in esecuzione in un'impostazione di visualizzazione a DPI elevato può soffrire di molti artefatti visivi, inclusa la scalabilità non corretta di elementi dell'interfaccia utente, testo ritagliato e immagini sfocate.</span><span class="sxs-lookup"><span data-stu-id="d10c6-107">An application that is not DPI-aware but is running on a high-DPI display setting can suffer from many visual artifacts, including incorrect scaling of UI elements, clipped text, and blurry images.</span></span> <span data-ttu-id="d10c6-108">Aggiungendo il supporto nell'applicazione per la compatibilità con DPI, è possibile rendere la presentazione dell'interfaccia utente dell'applicazione più prevedibile, rendendola più visivamente accattivante e più facile da leggere per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="d10c6-108">By adding support in your application for DPI-awareness, you make the presentation of your application's UI more predictable, making it more visually appealing and easier to read for users.</span></span> <span data-ttu-id="d10c6-109">Per fortuna, Direct2D rende più semplice che mai scrivere applicazioni che funzionano correttamente in un valore DPI elevato.</span><span class="sxs-lookup"><span data-stu-id="d10c6-109">Fortunately, Direct2D makes it easier than ever to write applications that work well in high-DPI.</span></span> <span data-ttu-id="d10c6-110">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="d10c6-110">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d10c6-111">Supporto di valori DPI alti in Direct2D</span><span class="sxs-lookup"><span data-stu-id="d10c6-111">High-DPI Support in Direct2D</span></span>](#high-dpi-support-in-direct2d)
-   [<span data-ttu-id="d10c6-112">Windows 8 e High-DPI</span><span class="sxs-lookup"><span data-stu-id="d10c6-112">Windows 8 and High-DPI</span></span>](#windows-8-and-high-dpi)
-   [<span data-ttu-id="d10c6-113">Che cos'è un DIP?</span><span class="sxs-lookup"><span data-stu-id="d10c6-113">What is a DIP?</span></span>](#what-is-a-dip)
-   [<span data-ttu-id="d10c6-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d10c6-114">Related topics</span></span>](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a><span data-ttu-id="d10c6-115">Supporto di valori DPI alti in Direct2D</span><span class="sxs-lookup"><span data-stu-id="d10c6-115">High-DPI Support in Direct2D</span></span>

<span data-ttu-id="d10c6-116">Direct2D fornisce le seguenti funzionalità per l'utilizzo di scenari ad alta risoluzione:</span><span class="sxs-lookup"><span data-stu-id="d10c6-116">Direct2D provides the following features for working with high-DPI scenarios:</span></span>

-   <span data-ttu-id="d10c6-117">Viene rispettato automaticamente il valore DPI del sistema quando si crea una destinazione di rendering a finestra, purché il manifesto dell'applicazione indichi che l'applicazione gestisce correttamente il valore DPI.</span><span class="sxs-lookup"><span data-stu-id="d10c6-117">It automatically honors the system DPI when creating a windowed render target, so long as the application manifest indicates that the application handles DPI correctly.</span></span> <span data-ttu-id="d10c6-118">Per informazioni su come dichiarare che l'applicazione è compatibile con DPI, vedere [come assicurarsi che l'applicazione venga visualizzata correttamente in schermi con valori DPI alti](how-to--size-a-window-properly-for-high-dpi-displays.md).</span><span class="sxs-lookup"><span data-stu-id="d10c6-118">(For information on how to declare that your application is DPI-aware, see [How to Ensure That Your Application Displays Properly on High-DPI Displays](how-to--size-a-window-properly-for-high-dpi-displays.md).)</span></span>
-   <span data-ttu-id="d10c6-119">Esprime le coordinate in DIP (device independent pixel), che consente la scalabilità automatica dell'applicazione in caso di modifica dell'impostazione DPI.</span><span class="sxs-lookup"><span data-stu-id="d10c6-119">It expresses coordinates in DIPs (Device Independent Pixels), which enables the application to scale automatically when the DPI setting changes.</span></span>
-   <span data-ttu-id="d10c6-120">Consente alle bitmap di avere un valore DPI e di ridimensionarle correttamente tenendo conto del valore DPI.</span><span class="sxs-lookup"><span data-stu-id="d10c6-120">It enables bitmaps to have a DPI and correctly scales them by taking the DPI into account.</span></span> <span data-ttu-id="d10c6-121">Questa funzionalità può essere usata anche per gestire le icone con diverse risoluzioni.</span><span class="sxs-lookup"><span data-stu-id="d10c6-121">This feature can also be used to maintain icons at different resolutions.</span></span>
-   <span data-ttu-id="d10c6-122">Esprime la maggior parte delle risorse in DIP, rendendo automaticamente le risorse indipendenti dalla risoluzione.</span><span class="sxs-lookup"><span data-stu-id="d10c6-122">It expresses most resources in DIPs, which makes the resources automatically independent of resolution.</span></span>
-   <span data-ttu-id="d10c6-123">Usa uno spazio delle coordinate a virgola mobile e l'anti-aliasing, quindi qualsiasi contenuto può essere ridimensionato in qualsiasi valore DPI arbitrario.</span><span class="sxs-lookup"><span data-stu-id="d10c6-123">It uses a floating-point coordinate space and antialiasing, so any content can be scaled to any arbitrary DPI.</span></span>

<span data-ttu-id="d10c6-124">La pipeline di grafica Direct2D è progettata per la scalabilità da 96 DPI a 1200DPI.</span><span class="sxs-lookup"><span data-stu-id="d10c6-124">The Direct2D graphics pipeline is designed to scale from 96 DPI to 1200DPI.</span></span>

## <a name="windows-8-and-high-dpi"></a><span data-ttu-id="d10c6-125">Windows 8 e High-DPI</span><span class="sxs-lookup"><span data-stu-id="d10c6-125">Windows 8 and High-DPI</span></span>

<span data-ttu-id="d10c6-126">A partire da Windows 8 sono disponibili funzionalità aggiuntive per il supporto di valori DPI alti.</span><span class="sxs-lookup"><span data-stu-id="d10c6-126">Starting with Windows 8, there are additional features for high-DPI support.</span></span>

<span data-ttu-id="d10c6-127">Se il valore DPI del contesto di dispositivo è sufficientemente elevato, Direct2D modifica la soglia utilizzata per abilitare l'anti-aliasing verticale del testo.</span><span class="sxs-lookup"><span data-stu-id="d10c6-127">If the device context DPI is high enough, Direct2D changes the threshold it uses to enable vertical antialiasing of text.</span></span> <span data-ttu-id="d10c6-128">In questo modo si ottiene un rendering del testo più veloce sulle visualizzazioni con valori DPI alti.</span><span class="sxs-lookup"><span data-stu-id="d10c6-128">This results in faster text rendering on high-DPI displays.</span></span> <span data-ttu-id="d10c6-129">Inoltre, è possibile impostare la modalità unità su pixel anziché DIP usando il metodo [**ID2D1DeviceContext:: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .</span><span class="sxs-lookup"><span data-stu-id="d10c6-129">Additionally, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span> <span data-ttu-id="d10c6-130">Se si imposta la modalità unità su pixel e il valore DPI del contesto di dispositivo sul valore DPI dello schermo, l'ottimizzazione è ancora abilitata.</span><span class="sxs-lookup"><span data-stu-id="d10c6-130">If you set the unit mode to pixels and the device context DPI to the screen DPI, the optimization is still enabled.</span></span>

## <a name="what-is-a-dip"></a><span data-ttu-id="d10c6-131">Che cos'è un DIP?</span><span class="sxs-lookup"><span data-stu-id="d10c6-131">What is a DIP?</span></span>

<span data-ttu-id="d10c6-132">Un Device Independent Pixel (DIP) è un pixel logico che esegue il mapping ai pixel del dispositivo fisico tramite un valore scalare, il valore DPI.</span><span class="sxs-lookup"><span data-stu-id="d10c6-132">A device independent pixel (DIP) is a logical pixel that maps to the pixels of the physical device through a scalar, the DPI.</span></span> <span data-ttu-id="d10c6-133">DPI corrisponde ai punti per pollice, dove un punto rappresenta un pixel del dispositivo fisico.</span><span class="sxs-lookup"><span data-stu-id="d10c6-133">DPI stands for dots per inch, where a dot represents a physical device pixel.</span></span> <span data-ttu-id="d10c6-134">La nomenclatura deriva dalla stampa, dove i punti rappresentano il punto di input penna più piccolo che può produrre un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d10c6-134">(The nomenclature comes from printing, where dots are the smallest ink dot that a printing process can produce).</span></span> <span data-ttu-id="d10c6-135">Poiché un monitor standard ha usato 96 punti per pollice, un valore DPI 96 significava che un Device Independent Pixel (o DIP) ha eseguito il mapping di 1:1 con un pixel fisico.</span><span class="sxs-lookup"><span data-stu-id="d10c6-135">Because a standard monitor used to have 96 dots per inch, a DPI of 96 meant that a device independent pixel (or DIP) mapped 1:1 with a physical pixel.</span></span> <span data-ttu-id="d10c6-136">Ad esempio, se il valore DPI era 96 \* 2 = 192, un singolo DIP includerebbe due pixel fisici.</span><span class="sxs-lookup"><span data-stu-id="d10c6-136">For example, if the DPI were 96\*2 = 192, then a single DIP would encompass two physical pixels.</span></span>

<span data-ttu-id="d10c6-137">Esistono molti motivi per cui le applicazioni non gestiscono necessariamente questo ridimensionamento correttamente; uno dei motivi più semplici è che richiede un lavoro aggiuntivo per individuare e usare questo valore scalare durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="d10c6-137">There are many reasons why applications don't necessarily handle this scaling correctly; one of the simplest reasons is that it requires extra work to discover and use this scalar value when rendering.</span></span> <span data-ttu-id="d10c6-138">In Direct2D il ridimensionamento viene applicato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d10c6-138">In Direct2D, the scaling is applied by default.</span></span> <span data-ttu-id="d10c6-139">A causa di questo mapping, i pixel del dispositivo fisico possono finire con le coordinate del DIP frazionario, uno dei motivi per cui Direct2D usa uno spazio delle coordinate a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="d10c6-139">Because of this mapping, physical device pixels might end up at fractional DIP coordinates, which is one of the reasons why Direct2D uses a floating-point coordinate space.</span></span>

<dl> <span data-ttu-id="d10c6-140">pixel fisico = (DIP × DPI)/96</span><span class="sxs-lookup"><span data-stu-id="d10c6-140">physical pixel = (dip × DPI) / 96</span></span>  
</dl>

<span data-ttu-id="d10c6-141">Per convertire un pixel fisico in un DIP, utilizzare la formula seguente:</span><span class="sxs-lookup"><span data-stu-id="d10c6-141">To convert a physical pixel to a DIP, use this formula:</span></span>

<dl> <span data-ttu-id="d10c6-142">DIP = (pixel fisico × 96)/DPI</span><span class="sxs-lookup"><span data-stu-id="d10c6-142">dip = (physical pixel × 96) / DPI</span></span>  
</dl>

> [!Note]
>
> <span data-ttu-id="d10c6-143">A partire da Windows 8, è possibile impostare la modalità unità su pixel anziché DIP usando il metodo [**ID2D1DeviceContext:: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .</span><span class="sxs-lookup"><span data-stu-id="d10c6-143">Starting with Windows 8, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d10c6-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d10c6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d10c6-145">Come verificare che l'applicazione venga visualizzata correttamente su schermi con DPI elevato</span><span class="sxs-lookup"><span data-stu-id="d10c6-145">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 