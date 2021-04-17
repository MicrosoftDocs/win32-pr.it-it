---
title: Uso di DirectX con schermi HDR e colori avanzati
description: In questo argomento viene fornita una panoramica tecnica sul rendering di contenuti High Dynamic Range Direct3D 11 e Direct3D 12 in una visualizzazione HDR10 con il supporto dei colori avanzati di Windows 10.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104566148"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a><span data-ttu-id="8cb8e-103">Uso di DirectX con schermi di intervallo dinamici elevati e colori avanzati</span><span class="sxs-lookup"><span data-stu-id="8cb8e-103">Using DirectX with high dynamic range Displays and Advanced Color</span></span>

<span data-ttu-id="8cb8e-104">In questo argomento viene fornita una panoramica tecnica sull'output di contenuto Direct3D 11 e Direct3D 11 (HDR) a una visualizzazione HDR10 con il supporto di colori avanzati di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-104">This topic provides a technical overview of outputting high dynamic range (HDR) Direct3D 11 and Direct3D 12 content to an HDR10 display using Windows 10 advanced color support.</span></span> <span data-ttu-id="8cb8e-105">Vengono riepilogate alcune delle principali differenze concettuali tra l'output e la visualizzazione di HDR10 rispetto alle visualizzazioni standard tradizionali (SDR, Dynamic Range) standard.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-105">It summarizes some key conceptual differences between outputting to HDR10 displays as compared to traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="8cb8e-106">Vengono inoltre illustrati i principali requisiti tecnici che consentono all'app di supportare correttamente Windows Advanced Color, oltre a raccomandazioni e procedure consigliate.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-106">It also covers the key technical requirements for your app to properly support Windows advanced color, as well as recommendations and best practices.</span></span>

## <a name="introduction"></a><span data-ttu-id="8cb8e-107">Introduzione</span><span class="sxs-lookup"><span data-stu-id="8cb8e-107">Introduction</span></span>

<span data-ttu-id="8cb8e-108">Windows 10 supporta le visualizzazioni HDR e altri colori avanzati, che offrono una fedeltà dei colori significativamente superiore rispetto alla visualizzazione SDR tradizionale.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-108">Windows 10 supports HDR and other advanced color displays, which provide significantly higher color fidelity than traditional SDR displays.</span></span> <span data-ttu-id="8cb8e-109">È possibile usare Direct3D, Direct2D e altre API grafiche per eseguire il rendering del contenuto HDR in una visualizzazione idonea.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-109">You can use Direct3D, Direct2D and other graphics APIs to render HDR content to a capable display.</span></span>

<span data-ttu-id="8cb8e-110">Windows Advanced Color si riferisce a diverse tecnologie correlate, introdotte per la prima volta con Windows 10 versione 1703, che forniscono il supporto per le visualizzazioni che superano le funzionalità di colore di standard standard (SDR) tradizionale.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-110">Windows advanced color refers to several related technologies, first introduced with Windows 10 version 1703, that provide support for displays that exceed the color capabilities of traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="8cb8e-111">Le tre principali funzionalità estese sono descritte di seguito.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-111">The three major extended capabilities are described below.</span></span> <span data-ttu-id="8cb8e-112">Il tipo più comune di visualizzazione dei colori avanzata, HDR10, supporta tutte e tre le funzionalità estese.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-112">The most common type of advanced color display, HDR10, supports all three extended capabilities.</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="8cb8e-113">Intervallo dinamico elevato</span><span class="sxs-lookup"><span data-stu-id="8cb8e-113">High dynamic range</span></span>

<span data-ttu-id="8cb8e-114">L'intervallo dinamico si riferisce alla differenza tra la luminosità massima e minima in una scena. Questa operazione viene spesso misurata in nit (candela per centimetro quadrato).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-114">Dynamic range refers to the difference between the maximum and minimum luminance in a scene; this is often measured in nits (candelas per square centimeter).</span></span> <span data-ttu-id="8cb8e-115">Le scene reali, ad esempio questo tramonto, presentano spesso intervalli dinamici di 10 ordini di grandezza della luminanza; l'occhio umano può discernere un intervallo ancora maggiore dopo l'adattamento.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-115">Real world scenes, such as this sunset, often have dynamic ranges of 10 orders of magnitude of luminance; the human eye can discern an even greater range after adaptation.</span></span>

![immagine di un tramonto con luminosità e punti più bui nella scena con etichetta](images/HDR-HDR.jpg)

<span data-ttu-id="8cb8e-117">Da Direct3D 9, i motori grafici sono stati in grado di eseguire internamente il rendering delle scene con questo livello di fedeltà fisicamente accurata.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-117">Ever since Direct3D 9, graphics engines have been able to internally render their scenes with this level of physically accurate fidelity.</span></span> <span data-ttu-id="8cb8e-118">Tuttavia, un tipico display con intervalli dinamici standard è in grado di riprodurre solo più di 3 ordini di grandezza della luminanza e pertanto qualsiasi contenuto con rendering HDR doveva essere Tonemapped (compresso) nell'intervallo limitato dello schermo.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-118">However, a typical standard dynamic range display can reproduce only a little more than 3 orders of magnitude of luminance, and therefore any HDR-rendered content had to be tonemapped (compressed) into the limited range of the display.</span></span> <span data-ttu-id="8cb8e-119">Le nuove visualizzazioni HDR, incluse quelle conformi allo standard HDR10 (BT. 2100), interrompono questa limitazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-119">New HDR displays, including those that comply with the HDR10 (BT.2100) standard, break through this limitation.</span></span>

### <a name="wide-color-gamut-with-automatic-system-color-management"></a><span data-ttu-id="8cb8e-120">Ampia gamma di colori con gestione automatica dei colori del sistema</span><span class="sxs-lookup"><span data-stu-id="8cb8e-120">Wide color gamut with automatic system color management</span></span>

<span data-ttu-id="8cb8e-121">Il gamut dei colori si riferisce all'intervallo e alla saturazione dei colori che possono essere riprodotti da una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-121">Color gamut refers to the range and saturation of hues that a display can reproduce.</span></span> <span data-ttu-id="8cb8e-122">Il colore naturale più saturo che l'occhio umano può percepire è pura, luce monocromatica, ad esempio ciò che è prodotto da un laser.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-122">The most saturated natural color the human eye can perceive is pure, monochromatic light such as what is produced by a laser.</span></span> <span data-ttu-id="8cb8e-123">Tuttavia, le visualizzazioni dei consumer mainstream possono spesso riprodurre colori solo all'interno della gamut sRGB, che rappresenta solo il 35% di tutti i colori percepibili.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-123">However, mainstream consumer displays can often reproduce colors only within the sRGB gamut, which represents only about 35% of all human-perceivable colors.</span></span> <span data-ttu-id="8cb8e-124">Il diagramma seguente è una rappresentazione del "locus spettrale" umano o di tutti i colori percepibili (a un determinato livello di luminanza), in cui il triangolo più piccolo è la gamut di sRGB.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-124">The diagram below is a representation of the human "spectral locus", or all perceivable colors (at a given luminance level), where the smaller triangle is the sRGB gamut.</span></span>

![diagramma del locus e della gamut dello spettro umano](images/HDR-WCG.jpg)

<span data-ttu-id="8cb8e-126">Gli schermi High end e Professional PC presentano gamme di colori supportate a lungo, significativamente più larghe rispetto a sRGB, ad esempio Adobe RGB e D65-P3.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-126">High end, professional PC displays have long supported color gamuts that are significantly wider than sRGB, such as Adobe RGB and D65-P3.</span></span> <span data-ttu-id="8cb8e-127">E questo ampio numero di visualizzazioni è sempre più comune.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-127">And these wide gamut displays are becoming more common.</span></span> <span data-ttu-id="8cb8e-128">Tuttavia, prima del colore avanzato, Windows non ha eseguito alcuna gestione dei colori a livello di sistema per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-128">However, prior to advanced color, Windows didn't perform any system-level color management for applications.</span></span> <span data-ttu-id="8cb8e-129">Ciò significava che se un'app DirectX veniva sottoposta a rendering, ad esempio, un rosso o RGB (1.0, 0,0, 0,0) alla catena di scambio, Windows analizzava semplicemente il rosso più saturo che la visualizzazione poteva riprodurre, indipendentemente dalla gamma di colori effettiva dello schermo.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-129">This meant that if a DirectX app rendered, for example, a pure red or RGB(1.0, 0.0, 0.0) to its swap chain, then Windows would simply scan out the most saturated red that the display could reproduce, regardless of what the actual color gamut of the display was.</span></span>

<span data-ttu-id="8cb8e-130">Le app che necessitavano di un'accuratezza dei colori elevata potevano eseguire query sulle funzionalità cromatiche dello schermo (ad esempio, usando i profili ICC) ed eseguire la gestione dei colori in-process per individuare correttamente la gamma di colori della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-130">Apps that needed high color accuracy could query the color capabilities of the display (for example, using ICC profiles), and perform their own in-process color management to correctly target the display's color gamut.</span></span> <span data-ttu-id="8cb8e-131">Tuttavia, la maggior parte delle app e del contenuto visivo presuppone che la visualizzazione sia sRGB e che si basino sul sistema operativo per soddisfare questo presupposto.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-131">However, the vast majority of apps and visual content assume that the display is sRGB, and they rely on the operating system to fulfill this assumption.</span></span>

<span data-ttu-id="8cb8e-132">Windows Advanced Color consente la gestione automatica dei colori a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-132">Windows advanced color adds automatic system-level color management.</span></span> <span data-ttu-id="8cb8e-133">Il Gestione finestre desktop (DWM) è il compositor di Windows.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-133">The Desktop Window Manager (DWM) is Windows' compositor.</span></span> <span data-ttu-id="8cb8e-134">Quando è abilitata la funzionalità colore avanzato, DWM esegue una conversione esplicita dei colori dallo spazio dei colori del contenuto visivo dell'app allo spazio colore della composizione canonica, che è scRGB.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-134">When advanced color is enabled, the DWM performs an explicit color conversion from the app visual content's colorspace to a canonical composition color space, which is scRGB.</span></span> <span data-ttu-id="8cb8e-135">Windows quindi color: converte il contenuto del framebuffer composto nello spazio colore nativo della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-135">Windows then color-converts the composed framebuffer content to the display's native color space.</span></span> <span data-ttu-id="8cb8e-136">In questo modo, il contenuto sRGB tradizionale ottiene automaticamente un comportamento accurato per il colore, mentre le app compatibili con i colori avanzate possono sfruttare le funzionalità di colore complete dello schermo.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-136">In this way, traditional sRGB content automatically gets color-accurate behavior, while advanced color-aware apps can take advantage of the full color capabilities of the display.</span></span>

### <a name="deep-precisionbit-depth"></a><span data-ttu-id="8cb8e-137">Precisione profonda/profondità bit</span><span class="sxs-lookup"><span data-stu-id="8cb8e-137">Deep precision/bit depth</span></span>

<span data-ttu-id="8cb8e-138">La precisione numerica, o la profondità del bit, si riferisce a rappresentare o distinguere colori simili ma distinti senza bande né artefatti.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-138">Numerical precision, or bit depth, refers to representing or distinguishing between similar but distinct colors without banding nor artifacts.</span></span> <span data-ttu-id="8cb8e-139">Il PC mainstream Visualizza il supporto di 8 bit per canale di colore, mentre l'occhio umano richiede almeno 10-12 bit di precisione per evitare distorsioni percepibili, senza ricorrere a tecniche come la dithering o a seconda delle condizioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-139">Mainstream PC displays support 8 bits per color channel, while the human eye requires at least 10-12 bits of precision to avoid perceivable distortions, without resorting to techniques such as dithering or depending on viewing conditions.</span></span>

![immagine di turbine a 2 bit simulati per canale di colore rispetto a 8 bit per canale](images/HDR-bitdepth.jpg)

<span data-ttu-id="8cb8e-141">Prima del colore avanzato, le app con finestra con restrizioni di DWM potevano inviare il contenuto solo a 8 bit per canale di colore, anche se la visualizzazione supportava una profondità di bit superiore.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-141">Prior to advanced color, the DWM restricted windowed apps to output content at only 8 bits per color channel, even if the display supported a higher bit depth.</span></span> <span data-ttu-id="8cb8e-142">Quando il colore avanzato è abilitato, DWM ne esegue la composizione usando il punto a virgola mobile a metà precisione IEEE (FP16), eliminando eventuali colli di bottiglia e consentendo l'uso della precisione completa dello schermo.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-142">When advanced color is enabled, the DWM performs its composition using IEEE half-precision floating point (FP16), eliminating any bottlenecks, and allowing the full precision of the display to be used.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="8cb8e-143">Requisiti di sistema</span><span class="sxs-lookup"><span data-stu-id="8cb8e-143">System Requirements</span></span>

### <a name="operating-system-os"></a><span data-ttu-id="8cb8e-144">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8cb8e-144">Operating system (OS)</span></span>

<span data-ttu-id="8cb8e-145">Il supporto dei colori avanzati è stato prima fornito con Windows 10, versione 1703, ed è stato notevolmente migliorato a ogni aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-145">Advanced color support first shipped with Windows 10, version 1703, and it has been significantly improved with each update.</span></span> <span data-ttu-id="8cb8e-146">Questo argomento presuppone che l'applicazione sia destinata a Windows 10, versione 1903 o successiva.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-146">This topic assumes that your app is targeting Windows 10, version 1903, or later.</span></span>

### <a name="display"></a><span data-ttu-id="8cb8e-147">Visualizza</span><span class="sxs-lookup"><span data-stu-id="8cb8e-147">Display</span></span>

<span data-ttu-id="8cb8e-148">Per sfruttare i vantaggi di un intervallo dinamico elevato, è necessario disporre di una visualizzazione che supporti lo standard HDR10.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-148">To take advantage of high dynamic range, you must have a display that supports the HDR10 standard.</span></span> <span data-ttu-id="8cb8e-149">Windows funziona al meglio con le visualizzazioni con [certificazione VESA DisplayHDR](https://displayhdr.org/).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-149">Windows works best with displays that are [VESA DisplayHDR certified](https://displayhdr.org/).</span></span>

### <a name="graphics-processor-gpu"></a><span data-ttu-id="8cb8e-150">Processore grafico (GPU)</span><span class="sxs-lookup"><span data-stu-id="8cb8e-150">Graphics processor (GPU)</span></span>

<span data-ttu-id="8cb8e-151">È necessaria una GPU recente.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-151">A recent GPU is required.</span></span> <span data-ttu-id="8cb8e-152">Per supportare le visualizzazioni HDR10, Windows 10 richiede uno dei seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-152">To support HDR10 displays, Windows 10 requires one of the following.</span></span>

* <span data-ttu-id="8cb8e-153">NVIDIA GeForce 1000 Series (Pascal) o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8cb8e-153">Nvidia GeForce 1000 series (Pascal), or newer</span></span>
* <span data-ttu-id="8cb8e-154">Serie AMD Radeon RX 400 (Polaris) o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8cb8e-154">AMD Radeon RX 400 series (Polaris), or newer</span></span>
* <span data-ttu-id="8cb8e-155">Serie Intel Core 7 selezionata (KABY Lake) o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8cb8e-155">Selected Intel Core 7 series (Kaby Lake), or newer</span></span>

<span data-ttu-id="8cb8e-156">Si noti che i requisiti hardware aggiuntivi si applicano a seconda degli scenari, tra cui l'accelerazione del codec hardware (HEVC a 10 bit, VP9 a 10 bit e così via) e il supporto PlayReady (SL3000).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-156">Note that additional hardware requirements apply depending on the scenarios, including hardware codec acceleration (10 bit HEVC, 10 bit VP9, etc.) and PlayReady support (SL3000).</span></span> <span data-ttu-id="8cb8e-157">Per informazioni più specifiche, contattare il fornitore della GPU.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-157">Contact your GPU vendor for more specific information.</span></span>

### <a name="graphics-driver-wddm"></a><span data-ttu-id="8cb8e-158">Driver Graphics (WDDM)</span><span class="sxs-lookup"><span data-stu-id="8cb8e-158">Graphics driver (WDDM)</span></span>

<span data-ttu-id="8cb8e-159">Il driver di grafica disponibile più recente è fortemente consigliato, da Windows Update o dal sito Web del fornitore della GPU o del produttore del computer.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-159">The latest available graphics driver is strongly recommended, either from Windows Update or from the GPU vendor or PC manufacturer's website.</span></span> <span data-ttu-id="8cb8e-160">Per Windows 10, versione 1903 e versioni successive, è consigliabile che i driver supportino almeno Windows Display Driver Model (WDDM) versione 2,6.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-160">For Windows 10, version 1903, and later, we recommend drivers that support at least Windows Display Driver Model (WDDM) version 2.6.</span></span>

## <a name="supported-rendering-apis"></a><span data-ttu-id="8cb8e-161">API di rendering supportate</span><span class="sxs-lookup"><span data-stu-id="8cb8e-161">Supported rendering APIs</span></span>

<span data-ttu-id="8cb8e-162">Windows 10 supporta un'ampia gamma di Framework e API per il rendering.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-162">Windows 10 supports a wide variety of rendering APIs and frameworks.</span></span> <span data-ttu-id="8cb8e-163">Il supporto dei colori avanzati si basa fondamentalmente sull'app per poter eseguire una presentazione moderna usando DXGI o le API del livello visivo.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-163">Advanced color support fundamentally relies on your app being able to perform modern presentation using either DXGI or the Visual Layer APIs.</span></span>

* [<span data-ttu-id="8cb8e-164">Infrastruttura grafica DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="8cb8e-164">DirectX Graphics Infrastructure (DXGI)</span></span>](../direct3ddxgi/dx-graphics-dxgi.md)
* [<span data-ttu-id="8cb8e-165">Livello visivo (Windows. UI. Composition)</span><span class="sxs-lookup"><span data-stu-id="8cb8e-165">Visual Layer (Windows.UI.Composition)</span></span>](/windows/uwp/composition/visual-layer)

<span data-ttu-id="8cb8e-166">Pertanto, qualsiasi API di rendering che può restituire uno di questi metodi di presentazione può supportare il colore avanzato.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-166">Therefore, any rendering API that can output to one of these presentations methods can support advanced color.</span></span> <span data-ttu-id="8cb8e-167">Questo include, ma non è limitato a questi.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-167">This includes but is not limited to these.</span></span>

* [<span data-ttu-id="8cb8e-168">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="8cb8e-168">Direct3D 11</span></span>](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [<span data-ttu-id="8cb8e-169">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8cb8e-169">Direct3D 12</span></span>](../direct3d12/direct3d-12-graphics.md)
* [<span data-ttu-id="8cb8e-170">Direct2D</span><span class="sxs-lookup"><span data-stu-id="8cb8e-170">Direct2D</span></span>](../direct2d/direct2d-portal.md)
* [<span data-ttu-id="8cb8e-171">Win2D</span><span class="sxs-lookup"><span data-stu-id="8cb8e-171">Win2D</span></span>](https://github.com/Microsoft/Win2D)
  * <span data-ttu-id="8cb8e-172">Richiede l'uso delle API **CanvasSwapChain** o **CanvasSwapChainPanel** di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-172">Requires using the lower level **CanvasSwapChain** or **CanvasSwapChainPanel** APIs.</span></span>
* [<span data-ttu-id="8cb8e-173">**Windows.UI.Input.Inking**</span><span class="sxs-lookup"><span data-stu-id="8cb8e-173">**Windows.UI.Input.Inking**</span></span>](/uwp/api/Windows.UI.Input.Inking)
  * <span data-ttu-id="8cb8e-174">Supporta il rendering dell'input penna personalizzato con DirectX.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-174">Supports custom dry ink rendering using DirectX.</span></span>
* [<span data-ttu-id="8cb8e-175">XAML</span><span class="sxs-lookup"><span data-stu-id="8cb8e-175">XAML</span></span>](/windows/uwp/xaml-platform/)
  * <span data-ttu-id="8cb8e-176">Supporta la riproduzione di video HDR usando **mediaplayerelement**.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-176">Supports playback of HDR videos using **MediaPlayerElement**.</span></span>
  * <span data-ttu-id="8cb8e-177">Supporta la decodifica di immagini JPEG XR usando l'elemento **Image** .</span><span class="sxs-lookup"><span data-stu-id="8cb8e-177">Supports decode of JPEG XR images using **Image** element.</span></span>
  * <span data-ttu-id="8cb8e-178">Supporta l'interoperabilità DirectX con **SwapChainPanel**.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-178">Supports DirectX interop using **SwapChainPanel**.</span></span>

## <a name="handling-dynamic-display-capabilities"></a><span data-ttu-id="8cb8e-179">Gestione delle funzionalità di visualizzazione dinamiche</span><span class="sxs-lookup"><span data-stu-id="8cb8e-179">Handling dynamic display capabilities</span></span>

<span data-ttu-id="8cb8e-180">Windows 10 supporta un'ampia gamma di schermi avanzati che supportano i colori, da pannelli integrati con efficienza energetica ai monitor e ai televisori di giochi high-end.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-180">Windows 10 supports an enormous range of advanced color-capable displays, from power-efficient integrated panels to high end gaming monitors and TVs.</span></span> <span data-ttu-id="8cb8e-181">Gli utenti di Windows si aspettano che l'app gestisca facilmente tutte queste varianti, incluse le visualizzazioni SDR esistenti.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-181">Windows users expect that your app will seamlessly handle all of these variations, including ubiquitous existing SDR displays.</span></span>

<span data-ttu-id="8cb8e-182">Windows 10 offre agli utenti il controllo delle funzionalità di colore HDR e avanzate.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-182">Windows 10 provides control over HDR and advanced color capabilities to the user.</span></span> <span data-ttu-id="8cb8e-183">L'app deve rilevare la configurazione della visualizzazione corrente e rispondere in modo dinamico alle modifiche della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-183">Your app must detect the current display's configuration, and respond dynamically to any changes in capability.</span></span> <span data-ttu-id="8cb8e-184">Questo problema può verificarsi per diversi motivi, ad esempio perché l'utente ha abilitato o disabilitato una funzionalità o ha spostato l'app tra diversi schermi oppure lo stato di alimentazione del sistema è cambiato.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-184">This could occur for many reasons, for example, because the user enabled or disabled a feature, or moved the app between different displays, or the system's power state changed.</span></span>

### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="8cb8e-185">App piattaforma UWP (Universal Windows Platform) (UWP)</span><span class="sxs-lookup"><span data-stu-id="8cb8e-185">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="8cb8e-186">Se si sta scrivendo un'app UWP, indipendentemente dall'API di rendering grafica in uso, usare [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) per ottenere le funzionalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-186">If you're writing a UWP app, regardless of the graphics rendering API you're using, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get display capabilities.</span></span> <span data-ttu-id="8cb8e-187">Ottenere un'istanza di **AdvancedColorInfo** da [**DisplayInformation:: GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-187">Obtain an instance of **AdvancedColorInfo** from [**DisplayInformation::GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span></span>

<span data-ttu-id="8cb8e-188">Per verificare il tipo di colore avanzato attualmente attivo, utilizzare la proprietà [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) .</span><span class="sxs-lookup"><span data-stu-id="8cb8e-188">To check what advanced color kind is currently active, use the [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) property.</span></span> <span data-ttu-id="8cb8e-189">In Windows 10, versione 1903 e versioni successive, restituisce uno dei tre valori possibili: **SDR**, **WCG** o **HDR**.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-189">In Windows 10, version 1903, and later, this returns one of three possible values: **SDR**, **WCG**, or **HDR**.</span></span> <span data-ttu-id="8cb8e-190">Si tratta della proprietà più importante da controllare ed è necessario configurare la pipeline di rendering e presentazione in risposta al tipo attivo.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-190">This is the most important property to check, and you should configure your render and presentation pipeline in response to the active kind.</span></span>

<span data-ttu-id="8cb8e-191">Per verificare quali tipi di colore avanzati sono supportati, ma non necessariamente attivi, chiamare [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-191">To check what advanced color kinds are supported, but not necessarily active, call [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span></span> <span data-ttu-id="8cb8e-192">Queste informazioni possono essere usate, ad esempio, per richiedere all'utente di passare all'app impostazioni di Windows in modo da abilitare l'abilitazione di HDR o WCG.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-192">You could use this information, for example, to prompt the user to navigate to the Windows Settings app so that they can enable HDR or WCG.</span></span>

<span data-ttu-id="8cb8e-193">Gli altri membri di **AdvancedColorInfo** forniscono informazioni quantitative sul volume di colori fisico del pannello (luminanza e cromatura), corrispondenti ai metadati HDR statici di SMPTE St. 2086.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-193">The other members of **AdvancedColorInfo** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="8cb8e-194">Usare queste informazioni per configurare il mapping di tonemapping e gamut di HDR dell'app.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-194">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="8cb8e-195">Per gestire le modifiche apportate alle funzionalità avanzate dei colori, effettuare la registrazione per l'evento [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) .</span><span class="sxs-lookup"><span data-stu-id="8cb8e-195">To handle changes in advanced color capabilities, register for the [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) event.</span></span> <span data-ttu-id="8cb8e-196">Questo evento viene generato se per qualsiasi motivo viene modificato un parametro delle funzionalità di colore avanzate della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-196">This event is raised if any parameter of the display's advanced color capabilities changes for any reason.</span></span>

<span data-ttu-id="8cb8e-197">Gestire questo evento ottenendo una nuova istanza di **AdvancedColorInfo** e controllando quali valori sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-197">Handle this event by obtaining a new instance of **AdvancedColorInfo**, and checking which values have changed.</span></span>

### <a name="desktop-win32-directx-apps"></a><span data-ttu-id="8cb8e-198">App DirectX desktop (Win32)</span><span class="sxs-lookup"><span data-stu-id="8cb8e-198">Desktop (Win32) DirectX apps</span></span>

<span data-ttu-id="8cb8e-199">Se si sta scrivendo un'app Win32 e si usa DirectX per eseguire il rendering, usare [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) per ottenere le funzionalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-199">If you're writing a Win32 app, and using DirectX to render, then use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get display capabilities.</span></span> <span data-ttu-id="8cb8e-200">Ottenere un'istanza di questo struct tramite [**IDXGIOutput6:: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-200">Obtain an instance of this struct via [**IDXGIOutput6::GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span></span>

<span data-ttu-id="8cb8e-201">Per verificare il tipo di colore avanzato attualmente attivo, utilizzare la proprietà dello **spazio** dei colori, che è di tipo [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), e contiene uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cb8e-201">To check what advanced color kind is currently active, use the **ColorSpace** property, which is of type [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), and contains one of the following values:</span></span>

* <span data-ttu-id="8cb8e-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span><span class="sxs-lookup"><span data-stu-id="8cb8e-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span></span>
* <span data-ttu-id="8cb8e-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span><span class="sxs-lookup"><span data-stu-id="8cb8e-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span></span>

> [!Note]
> <span data-ttu-id="8cb8e-204">Altri tipi di colori avanzati, ad esempio WCG, vengono considerati come DSP da DXGI.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-204">Other advanced color kinds such as WCG are treated as SDR by DXGI.</span></span> <span data-ttu-id="8cb8e-205">Non è possibile usare DXGI per identificare una visualizzazione WCG.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-205">You can't use DXGI to identify a WCG display.</span></span>

> [!Note]
> <span data-ttu-id="8cb8e-206">DXGI non consente di controllare quali tipi di colore avanzati sono supportati ma non attivi al momento.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-206">DXGI doesn't let you check what advanced color kinds are supported but not active at the moment.</span></span>

<span data-ttu-id="8cb8e-207">La maggior parte degli altri membri di **DXGI_OUTPUT_DESC1** fornisce informazioni quantitative sul volume di colori fisico (luminanza e cromatura) del pannello, corrispondenti ai metadati HDR statici di SMPTE St. 2086.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-207">Most of the other members of **DXGI_OUTPUT_DESC1** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="8cb8e-208">Usare queste informazioni per configurare il mapping di tonemapping e gamut di HDR dell'app.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-208">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="8cb8e-209">Le app Win32 non hanno un meccanismo nativo per rispondere alle modifiche avanzate della funzionalità colore.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-209">Win32 apps don't have a native mechanism to respond to advanced color capability changes.</span></span> <span data-ttu-id="8cb8e-210">Se invece l'app usa un ciclo di rendering, è necessario eseguire una query su [**IDXGIFactory1:: uncurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) con ogni frame.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-210">Instead, if your app uses a render loop, then you should query [**IDXGIFactory1::IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) with each frame.</span></span> <span data-ttu-id="8cb8e-211">Se viene segnalato **false**, è necessario ottenere un nuovo **DXGI_OUTPUT_DESC1** e verificare quali valori sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-211">If it reports **FALSE**, then you should obtain a new **DXGI_OUTPUT_DESC1**, and check which values have changed.</span></span>

<span data-ttu-id="8cb8e-212">Inoltre, il message pump Win32 deve gestire il messaggio di [**WM_SIZE**](../winmsg/wm-size.md) , che indica che è possibile che l'applicazione sia stata spostata tra diverse visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-212">In addition, your Win32 message pump should handle the [**WM_SIZE**](../winmsg/wm-size.md) message, which indicates that your app may have moved between different displays.</span></span>

> [!Note]
> <span data-ttu-id="8cb8e-213">Per ottenere un nuovo **DXGI_OUTPUT_DESC1**, è necessario ottenere la visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-213">To obtain a new **DXGI_OUTPUT_DESC1**, you must obtain the current display.</span></span> <span data-ttu-id="8cb8e-214">Tuttavia, non è necessario chiamare **IDXGISwapChain:: GetContainingOutput**.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-214">However, you should not call **IDXGISwapChain::GetContainingOutput**.</span></span> <span data-ttu-id="8cb8e-215">Ciò è dovuto al fatto che le catene di scambio restituiranno un output DXGI non aggiornato quando **DXGIFactory:: l'oggetto** è false e la ricreazione della catena di scambio per ottenere un output corrente genera una schermata nera temporanea.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-215">This is because swap chains will return a stale DXGI output once **DXGIFactory::IsCurrent** is false, and recreating the swap chain to get a current output results in a temporary black screen.</span></span> <span data-ttu-id="8cb8e-216">È invece consigliabile enumerare i limiti di tutti gli output di DXGI e determinare quale è la più grande intersezione con i limiti della finestra dell'app.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-216">Instead, we recommend that you enumerate through the bounds of all DXGI outputs, and determine which one has the greatest intersection with your app window's bounds.</span></span>

<span data-ttu-id="8cb8e-217">L'esempio di codice seguente deriva dal [repository DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-217">The following code example comes from the [DirectX-Graphics-Samples repository](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span>

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a><span data-ttu-id="8cb8e-218">Configurazione della catena di scambio DirectX</span><span class="sxs-lookup"><span data-stu-id="8cb8e-218">Setting up Your DirectX swap chain</span></span>

<span data-ttu-id="8cb8e-219">Una volta stabilito che la visualizzazione supporta attualmente le funzionalità di colore avanzate, configurare la catena di scambio come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-219">Once you have determined that the display currently supports advanced color capabilities, configure your swap chain as follows.</span></span>

### <a name="use-a-flip-presentation-model-effect"></a><span data-ttu-id="8cb8e-220">Usare un effetto del modello Flip Presentation</span><span class="sxs-lookup"><span data-stu-id="8cb8e-220">Use a flip presentation model effect</span></span>

<span data-ttu-id="8cb8e-221">Quando si crea la catena di scambio usando **CreateSwapChainFor [HWND | Composizione | CoreWindow]** metodi, è necessario usare il modello DXGI Flip selezionando l'opzione **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** o **DXGI_SWAP_EFFECT_FLIP_DISCARD** , che rende la catena di scambio idonea per l'elaborazione dei colori avanzata da DWM e varie ottimizzazioni a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-221">When creating your swap chain using the **CreateSwapChainFor[Hwnd|Composition|CoreWindow]** methods, you must use the DXGI flip model by selecting either the **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** or **DXGI_SWAP_EFFECT_FLIP_DISCARD** option, which makes your swap chain eligible for advanced color processing from DWM and various fullscreen optimizations.</span></span> <span data-ttu-id="8cb8e-222">Per ulteriori informazioni, vedere l'argomento [per ottenere prestazioni ottimali, utilizzare DXGI flip model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb8e-222">For more information, refer to the [For best performance, use DXGI flip model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) topic.</span></span>

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a><span data-ttu-id="8cb8e-223">Opzione 1.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-223">Option 1.</span></span> <span data-ttu-id="8cb8e-224">Usare il formato pixel FP16 e lo spazio colore scRGB</span><span class="sxs-lookup"><span data-stu-id="8cb8e-224">Use FP16 pixel format and scRGB color space</span></span>

<span data-ttu-id="8cb8e-225">Windows 10 supporta due combinazioni principali di formato pixel e spazio colore per i colori avanzati.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-225">Windows 10 supports two main combinations of pixel format and color space for advanced color.</span></span> <span data-ttu-id="8cb8e-226">Selezionarne uno in base ai requisiti specifici dell'app.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-226">Select one based on your app's specific requirements.</span></span>

<span data-ttu-id="8cb8e-227">Per le app per utilizzo generico, quando si crea una catena di scambio è consigliabile specificare [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-227">For general-purpose apps, when creating your swap chain we recommend specifying [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="8cb8e-228">Questo è noto anche come *FP16* nel [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-228">That's also known as *FP16* in your [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="8cb8e-229">Per impostazione predefinita, una catena di scambio creata con un formato pixel a virgola mobile viene considerata come se utilizzasse lo spazio colore [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) , noto anche come *ScRGB*.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-229">By default, a swap chain created with a floating point pixel format is treated as if it uses the [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) color space, which is also known as *scRGB*.</span></span>

<span data-ttu-id="8cb8e-230">Questa combinazione fornisce l'intervallo numerico e la precisione per specificare quasi tutti i colori fisicamente possibili ed eseguire l'elaborazione arbitraria, inclusa la fusione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-230">This combination provides you with the numeric range and precision to specify almost any physically possible color, and perform arbitrary processing including blending.</span></span> <span data-ttu-id="8cb8e-231">Inoltre, se si usa Direct2D, Win2D o Windows. UI. Composition, questa è l'unica combinazione supportata per qualsiasi catena di scambio o destinazione intermedia che contiene contenuto colore avanzato.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-231">In addition, if you're using Direct2D, Win2D, or Windows.UI.Composition, then this is the only supported combination for any swap chain or intermediate target that contains advanced color content.</span></span> 

<span data-ttu-id="8cb8e-232">Il compromesso principale di questa opzione è che utilizza 64 bit per pixel, che raddoppiano l'utilizzo della larghezza di banda e della memoria GPU rispetto ai formati di pixel UINT8 SDR tradizionali.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-232">The main tradeoff of this option is that it consumes 64 bits per pixel, which doubles GPU bandwidth and memory consumption compared to the traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="8cb8e-233">Inoltre, scRGB utilizza valori numerici che non rientrano nell'intervallo normalizzato [0,1] per rappresentare i colori che non rientrano nel gamut di sRGB e/o superiori a 80 nit di luminanza.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-233">In addition, scRGB uses numeric values that are outside the normalized [0, 1] range to represent colors that are outside the sRGB gamut and/or greater than 80 nits of luminance.</span></span> <span data-ttu-id="8cb8e-234">Ad esempio, scRGB (1,0, 1,0, 1,0) codifica il bianco D65 standard a 80 nit; Tuttavia, scRGB (12,5, 12,5, 12,5) codifica lo stesso D65 bianco a un livello molto più luminoso di 1000 nit.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-234">For example, scRGB (1.0, 1.0, 1.0) encodes the standard D65 white at 80 nits; but scRGB (12.5, 12.5, 12.5) encodes the same D65 white at a much brighter 1000 nits.</span></span> <span data-ttu-id="8cb8e-235">Alcune operazioni grafiche richiedono un intervallo numerico normalizzato ed è necessario modificare l'operazione o rinormalizzare i valori dei colori.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-235">Some graphics operations require a normalized numeric range, and you must either modify the operation, or re-normalize color values.</span></span>

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a><span data-ttu-id="8cb8e-236">Opzione 2: usare il formato pixel UINT10/RGB10 e lo spazio colore HDR10/BT. 2100</span><span class="sxs-lookup"><span data-stu-id="8cb8e-236">Option 2: Use UINT10/RGB10 pixel format and HDR10/BT.2100 color space</span></span>

<span data-ttu-id="8cb8e-237">Per le app che usano contenuto con codifica HDR10, ad esempio lettori multimediali o app che dovrebbero essere usate principalmente in scenari a schermo intero, ad esempio giochi, quando si crea la catena di scambio è consigliabile specificare [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-237">For apps that consume HDR10-encoded content, such as media players, or apps that are expected to be used mainly in fullscreen scenarios such as games, when creating your swap chain you should consider specifying [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="8cb8e-238">Per impostazione predefinita, questo viene considerato come usando lo spazio dei colori di sRGB; Pertanto, è necessario chiamare in modo esplicito [**IDXGISwapChain3:: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)e impostare come spazio colore [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), noto anche come HDR10/BT. 2100.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-238">By default, this is treated as using the sRGB color space; therefore, you must explicitly call [**IDXGISwapChain3::SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1), and set as your color space [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), also known as HDR10/BT.2100.</span></span>

<span data-ttu-id="8cb8e-239">Questa combinazione presenta restrizioni più restrittive rispetto a FP16.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-239">This combination has more stringent restrictions than FP16.</span></span> <span data-ttu-id="8cb8e-240">Questa operazione può essere usata solo con Direct3D 11 o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-240">You can use this only with Direct3D 11 or Direct3D 12.</span></span> <span data-ttu-id="8cb8e-241">Inoltre, UINT10/HDR10 presenta limitazioni come formato temporaneo perché usa la funzione ST. 2084 EOTF ("gamma"), che è altamente non lineare, e ottimizzata come formato wire, e perché offre solo 2 bit di alfa.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-241">In addition, UINT10/HDR10 has limitations as an intermediate format because it uses the ST.2084 EOTF ("gamma" function), which is highly nonlinear, and optimized as a wire format, and because it offers only 2 bits of alpha.</span></span>

<span data-ttu-id="8cb8e-242">Questa combinazione può tuttavia offrire potenti ottimizzazioni delle prestazioni quando viene usata nell'output finale dell'app.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-242">However, this combination can offer powerful performance optimizations when used in your app's final output.</span></span> <span data-ttu-id="8cb8e-243">USA gli stessi 32 bit per pixel dei formati UINT8 SDR pixel tradizionali.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-243">It consumes the same 32 bits per pixel as traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="8cb8e-244">Inoltre, in alcuni scenari a schermo intero, il sistema operativo può ottimizzare le prestazioni analizzando direttamente la superficie di HDR10.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-244">In addition, in certain fullscreen scenarios, the OS can optimize performance by directly scanning out the HDR10 surface.</span></span>

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a><span data-ttu-id="8cb8e-245">Uso di una catena di scambio colori avanzata quando la visualizzazione è in modalità SDR</span><span class="sxs-lookup"><span data-stu-id="8cb8e-245">Using an advanced color swap chain when the display is in SDR mode</span></span>

<span data-ttu-id="8cb8e-246">È possibile usare una catena di scambio dei colori avanzata anche se la visualizzazione non supporta alcune o tutte le funzionalità di colore avanzate richieste dal contenuto.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-246">You can use an advanced color swap chain even if the display doesn't support some or all of the advanced color capabilities your content requires.</span></span> <span data-ttu-id="8cb8e-247">In questi casi, il Gestione finestre desktop (DWM) downconvert il contenuto per adattarlo alle funzionalità della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-247">In those cases, the Desktop Window Manager (DWM) will downconvert your content to fit the display's capabilities.</span></span> <span data-ttu-id="8cb8e-248">In Windows 10, versione 1903 e successive, eseguirà il ritaglio numerico; Se, ad esempio, si esegue il rendering in una catena di scambio FP16 scRGB, tutti gli elementi esterni all'intervallo numerico [0, 1] vengono ritagliati.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-248">In Windows 10, version 1903, and later, it will perform numeric clipping; for example, if you render to an FP16 scRGB swap chain, then everything outside of the [0, 1] numeric range is clipped.</span></span>

<span data-ttu-id="8cb8e-249">Questo comportamento Downconversion si verifica anche se la finestra dell'app si trova a due o più schermi con funzionalità di colore avanzate diverse.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-249">This downconversion behavior will also occur if your app window is straddling two or more displays with differing advanced color capabilities.</span></span> <span data-ttu-id="8cb8e-250">**AdvancedColorInfo** e **IDXGIOutput6** vengono estratti per segnalare solo le caratteristiche della visualizzazione "principale" (definite come visualizzazione contenente il centro della finestra).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-250">**AdvancedColorInfo** and **IDXGIOutput6** are abstracted to report only the "main" display's characteristics (defined as the display containing the center of the window).</span></span>

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a><span data-ttu-id="8cb8e-251">Eseguire correttamente il rendering del contenuto SDR con il livello bianco di riferimento SDR</span><span class="sxs-lookup"><span data-stu-id="8cb8e-251">Correctly render SDR content with SDR reference white level</span></span>

<span data-ttu-id="8cb8e-252">In molti scenari, l'app vuole eseguire il rendering del contenuto sia di SDR che di HDR; ad esempio, il rendering di sottotitoli o controlli di trasporto su video HDR o sull'interfaccia utente in una scena di gioco.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-252">In many scenarios, your app will want to render both SDR and HDR content; for example, rendering subtitles or transport controls over HDR video, or UI into a game scene.</span></span> <span data-ttu-id="8cb8e-253">È importante comprendere il concetto di *livello bianco di riferimento SDR* per garantire che il contenuto SDR appaia corretto in una visualizzazione HDR.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-253">It is important to understand the concept of *SDR reference white level* to ensure that your SDR content looks correct on an HDR display.</span></span>

<span data-ttu-id="8cb8e-254">Windows considera il contenuto HDR come _riferimento alla scena_, ovvero un particolare valore di colore deve essere visualizzato a un livello di luminanza specifico. ad esempio, scRGB (1,0, 1,0, 1,0) e HDR10 (497, 497, 497) codificano entrambi esattamente D65 bianchi alla luminanza di 80 nit.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-254">Windows treats HDR content as _scene-referred_, meaning that a particular color value should be displayed at a specific luminance level; for example, scRGB (1.0, 1.0, 1.0) and HDR10 (497, 497, 497) both encode exactly D65 white at 80 nits luminance.</span></span> <span data-ttu-id="8cb8e-255">Nel frattempo, il contenuto SDR è stato tradizionalmente reso di _output_ (o a cui viene fatto riferimento), vale a dire che la luminanza viene lasciata all'utente o al dispositivo. ad esempio, sRGB (1,0, 1,0, 1,0) codifica D65 bianco come negli esempi HDR, ma con qualsiasi luminanza massima per la quale è configurata la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-255">Meanwhile, SDR content traditionally has been _output-referred_ (or display-referred), meaning that its luminance is left up to the user or the device; for example sRGB (1.0, 1.0, 1.0) encodes D65 white as in the HDR examples, but at whatever maximum luminance the display is configured for.</span></span> <span data-ttu-id="8cb8e-256">Windows consente all'utente di modificare il _livello di riferimento di DSP_ in base alla preferenza. si tratta della luminanza che Windows eseguirà il rendering di sRGB (1,0, 1,0, 1,0) in.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-256">Windows allows the user to adjust the _SDR reference white level_ to their preference; this is the luminance that Windows will render sRGB (1.0, 1.0, 1.0) at.</span></span> <span data-ttu-id="8cb8e-257">Nei monitoraggi HDR del desktop i livelli bianchi di riferimento SDR sono in genere impostati su circa 200 nit.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-257">On desktop HDR monitors, SDR reference white levels are typically set to around 200 nits.</span></span>

> [!Note]
> <span data-ttu-id="8cb8e-258">In una visualizzazione che supporta un controllo della luminosità, ad esempio su un portatile, Windows modificherà anche la luminosità del contenuto HDR (a cui si fa riferimento) in modo che corrisponda al livello di luminosità desiderato dell'utente, ma ciò è invisibile all'app.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-258">On a display that supports a brightness control, such as on a laptop, Windows will also adjust the luminance of HDR (scene-referred) content to match the user's desired brightness level, but this is invisible to the app.</span></span> <span data-ttu-id="8cb8e-259">A meno che non si stia tentando di garantire una riproduzione accurata del segnale HDR, in genere è possibile ignorare questo problema.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-259">Unless you're trying to guarantee bit-accurate reproduction of the HDR signal, you can generally ignore this.</span></span>

<span data-ttu-id="8cb8e-260">Se l'app esegue sempre il rendering di SDR e HDR per separare le superfici e si basa sulla composizione del sistema operativo, Windows eseguirà automaticamente la regolazione corretta per incrementare il contenuto di SDR al livello bianco desiderato.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-260">If your app always renders SDR and HDR to separate surfaces, and relies on OS composition, then Windows will automatically perform the correct adjustment to boost SDR content to the desired white level.</span></span> <span data-ttu-id="8cb8e-261">Ad esempio, se l'app usa XAML ed esegue il rendering del contenuto HDR nel proprio **SwapChainPanel**.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-261">For example, if your app uses XAML and renders HDR content to its own **SwapChainPanel**.</span></span>

<span data-ttu-id="8cb8e-262">Tuttavia, se l'app esegue la propria composizione di DSP e contenuto HDR in un'unica superficie, si è responsabili dell'esecuzione autonoma della regolazione del livello bianco di riferimento SDR.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-262">However, if your app performs its own composition of SDR and HDR content into a single surface, then you're responsible for performing the SDR reference white level adjustment yourself.</span></span> <span data-ttu-id="8cb8e-263">In caso contrario, il contenuto di SDR potrebbe sembrare troppo debole presumendo condizioni di visualizzazione desktop tipiche.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-263">Otherwise the SDR content might appear too dim assuming typical desktop viewing conditions.</span></span> <span data-ttu-id="8cb8e-264">Per prima cosa, è necessario ottenere il livello bianco di riferimento SDR corrente, quindi è necessario modificare i valori dei colori di qualsiasi contenuto SDR di cui si sta eseguendo il rendering.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-264">First, you must obtain the current SDR reference white level, and then you must adjust the color values of any SDR content you're rendering.</span></span>

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a><span data-ttu-id="8cb8e-265">Passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-265">Step 1.</span></span> <span data-ttu-id="8cb8e-266">Ottenere il livello bianco di riferimento SDR corrente</span><span class="sxs-lookup"><span data-stu-id="8cb8e-266">Obtain the current SDR reference white level</span></span>

<span data-ttu-id="8cb8e-267">Attualmente, solo le app UWP possono ottenere il livello bianco di riferimento SDR corrente tramite [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-267">Currently, only UWP apps can obtain the current SDR reference white level via [**AdvancedColorInfo.SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span></span> <span data-ttu-id="8cb8e-268">Questa API richiede un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-268">This API requires a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

### <a name="step-2-adjust-color-values-of-sdr-content"></a><span data-ttu-id="8cb8e-269">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="8cb8e-269">Step 2.</span></span> <span data-ttu-id="8cb8e-270">Modificare i valori dei colori del contenuto SDR</span><span class="sxs-lookup"><span data-stu-id="8cb8e-270">Adjust color values of SDR content</span></span>

<span data-ttu-id="8cb8e-271">Windows definisce il livello del bianco di riferimento nominale o predefinito a 80 pidocchi; Se quindi si esegue il rendering di un bianco standard (1,0, 1,0, 1,0) in una catena di scambio FP16, questo verrà riprodotto alla luminanza di 80 nit.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-271">Windows defines the nominal, or default, reference white level at 80 nits; therefore if you were to render a standard sRGB (1.0, 1.0, 1.0) white to an FP16 swap chain, it would be reproduced at 80 nits luminance.</span></span> <span data-ttu-id="8cb8e-272">Per corrispondere al livello di riferimento effettivo definito dall'utente, è necessario modificare il contenuto SDR da 80 nit al livello specificato tramite **AdvancedColorInfo. SdrWhiteLevelInNits**.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-272">In order to match the actual user-defined reference white level, you must adjust SDR content from 80 nits to the level specified via **AdvancedColorInfo.SdrWhiteLevelInNits**.</span></span>

<span data-ttu-id="8cb8e-273">Se si esegue il rendering usando FP16 e ScRGB o qualsiasi spazio di colore che usa la gamma lineare (1,0), è possibile moltiplicare semplicemente il valore del colore SDR per _AdvancedColorInfo. SdrWhiteLevelInNits_  /  _80_.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-273">If you're rendering using FP16 and scRGB, or any color space that uses linear (1.0) gamma, then you can simply multiply the SDR color value by _AdvancedColorInfo.SdrWhiteLevelInNits_ / _80_.</span></span> <span data-ttu-id="8cb8e-274">Se si usa Direct2D, esiste una costante predefinita [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), che ha un valore di 80.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-274">If you're using Direct2D, there is a predefined constant [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), which has a value of 80.</span></span>

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

<span data-ttu-id="8cb8e-275">Se si esegue il rendering usando uno spazio di colore gamma non lineare, ad esempio HDR10, l'esecuzione della regolazione del livello bianco di SDR è più complessa. Se si sta scrivendo un pixel shader personalizzato, è consigliabile prendere in considerazione la conversione in gamma lineare per applicare la regolazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-275">If you're rendering using a nonlinear gamma color space such as HDR10, then performing SDR white level adjustment is more complex; if you're writing your own pixel shader you should consider converting into linear gamma to apply the adjustment.</span></span>

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a><span data-ttu-id="8cb8e-276">Adattare il contenuto HDR alle funzionalità dello schermo usando tonemapping</span><span class="sxs-lookup"><span data-stu-id="8cb8e-276">Adapt HDR content to the display's capabilities using tonemapping</span></span>

<span data-ttu-id="8cb8e-277">Le visualizzazioni HDR e dei colori avanzati variano significativamente in termini di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-277">HDR and advanced color displays vary greatly in terms of their capabilities.</span></span> <span data-ttu-id="8cb8e-278">Ad esempio, la luminanza minima e massima e la gamma di colori che sono in grado di riprodurre.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-278">For example, the minimum and maximum luminance and the color gamut they are capable of reproducing.</span></span> <span data-ttu-id="8cb8e-279">In molti casi, il contenuto HDR conterrà i colori che superano le funzionalità della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-279">In many cases, your HDR content will contain colors that exceed the display's capabilities.</span></span> <span data-ttu-id="8cb8e-280">Per ottenere la migliore qualità dell'immagine, è importante eseguire tonemapping HDR, comprimendo essenzialmente l'intervallo di colori per adattarlo alla visualizzazione, mantenendo al tempo stesso la finalità visiva del contenuto.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-280">For the best image quality it is important for you to perform HDR tonemapping, essentially compressing the range of colors to fit the display while best preserving the visual intent of the content.</span></span>

<span data-ttu-id="8cb8e-281">Il più importante parametro singolo per adattarsi a è la luminanza massima, nota anche come MaxCLL (Content Light Level); tonemappers più sofisticate adatteranno anche la luminosità minima (MinCLL) e/o le primarie colore.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-281">The most important single parameter to adapt for is max luminance, also known as MaxCLL (content light level); more sophisticated tonemappers will also adapt min luminance (MinCLL) and/or color primaries.</span></span>

### <a name="step-1-get-the-displays-color-volume-capabilities"></a><span data-ttu-id="8cb8e-282">Passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-282">Step 1.</span></span> <span data-ttu-id="8cb8e-283">Ottenere le funzionalità del volume di colori della visualizzazione</span><span class="sxs-lookup"><span data-stu-id="8cb8e-283">Get the display's color volume capabilities</span></span>

#### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="8cb8e-284">App piattaforma UWP (Universal Windows Platform) (UWP)</span><span class="sxs-lookup"><span data-stu-id="8cb8e-284">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="8cb8e-285">Usare [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) per ottenere il volume di colori della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-285">Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get the display's color volume.</span></span>

#### <a name="win32-desktop-directx-apps"></a><span data-ttu-id="8cb8e-286">App DirectX Win32 (desktop)</span><span class="sxs-lookup"><span data-stu-id="8cb8e-286">Win32 (desktop) DirectX apps</span></span>

<span data-ttu-id="8cb8e-287">Usare [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) per ottenere il volume di colori della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-287">Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get the display's color volume.</span></span>

### <a name="step-2-get-the-contents-color-volume-information"></a><span data-ttu-id="8cb8e-288">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="8cb8e-288">Step 2.</span></span> <span data-ttu-id="8cb8e-289">Ottenere le informazioni sul volume di colori del contenuto</span><span class="sxs-lookup"><span data-stu-id="8cb8e-289">Get the content's color volume information</span></span>

<span data-ttu-id="8cb8e-290">A seconda della provenienza del contenuto HDR, esistono diversi modi possibili per determinare le informazioni relative alla luminanza e al gamut dei colori.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-290">Depending on where your HDR content came from, there are multiple potential ways to determine its luminance and color gamut information.</span></span> <span data-ttu-id="8cb8e-291">Alcuni file di immagine e video HDR contengono metadati SMPTE ST. 2086.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-291">Certain HDR video and image files contain SMPTE ST.2086 metadata.</span></span> <span data-ttu-id="8cb8e-292">Se il rendering del contenuto è stato eseguito in modo dinamico, potrebbe essere possibile estrarre le informazioni sulle scene dalle fasi di rendering interne, ad esempio la fonte di luce più luminosa in una scena.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-292">If your content was rendered dynamically, then you may be able to extract scene information from the internal rendering stages, for example the brightest light source in a scene.</span></span>

<span data-ttu-id="8cb8e-293">Una soluzione più generale ma costosa dal punto di vista del calcolo consiste nell'eseguire un istogramma o un altro passaggio di analisi nel frame sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-293">A more general but computationally expensive solution is to run a histogram or other analysis pass on the rendered frame.</span></span> <span data-ttu-id="8cb8e-294">L' [esempio di Direct2D Advanced color images SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) illustra come eseguire questa operazione tramite Direct2D; di seguito sono elencati i frammenti di codice più rilevanti:</span><span class="sxs-lookup"><span data-stu-id="8cb8e-294">The [Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) demonstrates how to do this using Direct2D; the most relevant code snippets are included below:</span></span>

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a><span data-ttu-id="8cb8e-295">Passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-295">Step 3.</span></span> <span data-ttu-id="8cb8e-296">Eseguire l'operazione HDR tonemapping</span><span class="sxs-lookup"><span data-stu-id="8cb8e-296">Perform the HDR tonemapping operation</span></span>

<span data-ttu-id="8cb8e-297">Tonemapping è intrinsecamente un processo con perdita di perdite e può essere ottimizzato per una serie di metriche percettive o oggettive, quindi non esiste un algoritmo standard.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-297">Tonemapping is inherently a lossy process, and can be optimized for a number of perceptual or objective metrics, so there is no one standard algorithm.</span></span> <span data-ttu-id="8cb8e-298">Windows fornisce un [effetto Tonemapper HDR](../direct2d/hdr-tone-map-effect.md) incorporato come parte di Direct2D, oltre che nella pipeline di riproduzione video HDR Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-298">Windows provides a built-in [HDR tonemapper effect](../direct2d/hdr-tone-map-effect.md) as part of Direct2D as well as in the Media Foundation HDR video playback pipeline.</span></span> <span data-ttu-id="8cb8e-299">Altri algoritmi di uso comune includono le voci ACE filmica, Reinhard e ITU-R BT. 2390-3 EETF (funzione di trasferimento elettrico-elettrico).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-299">Some other commonly used algorithms include ACES Filmic, Reinhard, and ITU-R BT.2390-3 EETF (electrical-electrical transfer function).</span></span>

<span data-ttu-id="8cb8e-300">Di seguito è illustrato un operatore tonemapper di Reinhard semplificato.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-300">A simplified Reinhard tonemapper operator is shown below.</span></span>

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a><span data-ttu-id="8cb8e-301">Acquisizione di contenuto HDR e WCG</span><span class="sxs-lookup"><span data-stu-id="8cb8e-301">Capturing HDR and WCG content</span></span>

<span data-ttu-id="8cb8e-302">Le API che supportano la specifica di formati pixel, ad esempio quelle nello spazio dei nomi [**Windows. graphics. Capture**](/uwp/api/windows.graphics.capture) e il metodo [**IDXGIOutput5::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) , offrono la possibilità di acquisire contenuto HDR e WCG senza perdere le informazioni sui pixel.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-302">APIs that support specifying pixel formats, such as those in the [**Windows.Graphics.Capture**](/uwp/api/windows.graphics.capture) namespace, and the [**IDXGIOutput5::DuplicateOutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) method, provide the capability to capture HDR and WCG content without losing pixel information.</span></span> <span data-ttu-id="8cb8e-303">Si noti che dopo aver acquisito i frame di contenuto, è necessaria un'elaborazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-303">Note that after acquiring content frames, additional processing is required.</span></span> <span data-ttu-id="8cb8e-304">Ad esempio, il mapping del tono da HDR a SDR (ad esempio, la copia della schermata SDR per Internet Sharing) e il salvataggio del contenuto con il formato appropriato (ad esempio, JPEG XR).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-304">For example, HDR-to-SDR tone mapping (for example, SDR screenshot copy for Internet sharing) and content saving with proper format (for example, JPEG XR).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8cb8e-305">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="8cb8e-305">Additional resources</span></span>

* <span data-ttu-id="8cb8e-306">*Uso del rendering HDR con DirectX Tool Kit* per DirectX [11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-306">*Using HDR Rendering with the DirectX Tool Kit* for [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering) / [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span></span> <span data-ttu-id="8cb8e-307">Procedura dettagliata su come aggiungere il supporto HDR a un'app DirectX mediante DirectX Tool Kit (DirectXTK).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-307">Walkthrough of how to add HDR support to a DirectX app using the DirectX Tool Kit (DirectXTK).</span></span>
* <span data-ttu-id="8cb8e-308">[Esempio di Direct2D Advanced color images SDK](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-308">[Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span></span> <span data-ttu-id="8cb8e-309">Esempio di SDK UWP che implementa un visualizzatore di immagini HDR e WCG con rilevamento del colore avanzato tramite Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-309">UWP SDK sample implementing an advanced color-aware HDR and WCG image viewer using Direct2D.</span></span> <span data-ttu-id="8cb8e-310">Viene illustrata la gamma completa di procedure consigliate per le app UWP, tra cui la risposta alla visualizzazione delle modifiche alle funzionalità e la regolazione del livello di DSP bianco.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-310">Demonstrates the full range of best practices for UWP apps, including responding to display capability changes and adjusting for SDR white level.</span></span>
* <span data-ttu-id="8cb8e-311">[Esempio per desktop Direct3D 12 HDR](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-311">[Direct3D 12 HDR desktop sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span> <span data-ttu-id="8cb8e-312">Esempio di Desktop SDK che implementa una scena Direct3D 12 HDR di base.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-312">Desktop SDK sample implementing a basic Direct3D 12 HDR scene.</span></span>
* <span data-ttu-id="8cb8e-313">[Esempio Direct3D 12 HDR UWP](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-313">[Direct3D 12 HDR UWP sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span></span> <span data-ttu-id="8cb8e-314">UWP equivalente all'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-314">UWP equivalent of the above sample.</span></span>
* <span data-ttu-id="8cb8e-315">[Esempio di SIMPLEHDR PC Xbox ATG](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span><span class="sxs-lookup"><span data-stu-id="8cb8e-315">[Xbox ATG SimpleHDR PC sample](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span></span> <span data-ttu-id="8cb8e-316">Esempio di Desktop SDK che implementa una scena HDR 11 di base di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8cb8e-316">Desktop SDK sample implementing a basic Direct3D 11 HDR scene.</span></span>
