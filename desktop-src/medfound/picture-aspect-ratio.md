---
description: In questo argomento vengono descritti due concetti correlati, proporzioni dell'immagine e proporzioni in pixel.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Proporzioni immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226514"
---
# <a name="picture-aspect-ratio"></a><span data-ttu-id="778b1-103">Proporzioni immagine</span><span class="sxs-lookup"><span data-stu-id="778b1-103">Picture Aspect Ratio</span></span>

<span data-ttu-id="778b1-104">In questo argomento vengono descritti due concetti correlati, proporzioni dell'immagine e proporzioni in pixel.</span><span class="sxs-lookup"><span data-stu-id="778b1-104">This topic describes two related concepts, picture aspect ratio and pixel aspect ratio.</span></span> <span data-ttu-id="778b1-105">Viene quindi descritto come questi concetti vengono espressi in Microsoft Media Foundation utilizzando i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="778b1-105">It then describes how these concepts are expressed in Microsoft Media Foundation using media types.</span></span>

-   [<span data-ttu-id="778b1-106">Proporzioni immagine</span><span class="sxs-lookup"><span data-stu-id="778b1-106">Picture Aspect Ratio</span></span>](#picture-aspect-ratio)
    -   [<span data-ttu-id="778b1-107">Letterboxing</span><span class="sxs-lookup"><span data-stu-id="778b1-107">Letterboxing</span></span>](#letterboxing)
    -   [<span data-ttu-id="778b1-108">Pan-and-Scan</span><span class="sxs-lookup"><span data-stu-id="778b1-108">Pan-and-Scan</span></span>](#pan-and-scan)
-   [<span data-ttu-id="778b1-109">Proporzioni pixel</span><span class="sxs-lookup"><span data-stu-id="778b1-109">Pixel Aspect Ratio</span></span>](#pixel-aspect-ratio)
-   [<span data-ttu-id="778b1-110">Utilizzo delle proporzioni</span><span class="sxs-lookup"><span data-stu-id="778b1-110">Working with Aspect Ratios</span></span>](#working-with-aspect-ratios)
-   [<span data-ttu-id="778b1-111">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="778b1-111">Code Examples</span></span>](#code-examples)
    -   [<span data-ttu-id="778b1-112">Ricerca dell'area di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="778b1-112">Finding the Display Area</span></span>](#finding-the-display-area)
    -   [<span data-ttu-id="778b1-113">Conversione tra proporzioni in pixel</span><span class="sxs-lookup"><span data-stu-id="778b1-113">Converting Between Pixel Aspect Ratios</span></span>](#converting-between-pixel-aspect-ratios)
    -   [<span data-ttu-id="778b1-114">Calcolo dell'area letterbox</span><span class="sxs-lookup"><span data-stu-id="778b1-114">Calculating the Letterbox Area</span></span>](#calculating-the-letterbox-area)
-   [<span data-ttu-id="778b1-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="778b1-115">Related topics</span></span>](#related-topics)

## <a name="picture-aspect-ratio"></a><span data-ttu-id="778b1-116">Proporzioni immagine</span><span class="sxs-lookup"><span data-stu-id="778b1-116">Picture Aspect Ratio</span></span>

<span data-ttu-id="778b1-117">Proporzioni *immagine* definisce la forma dell'immagine video visualizzata.</span><span class="sxs-lookup"><span data-stu-id="778b1-117">*Picture aspect ratio* defines the shape of the displayed video image.</span></span> <span data-ttu-id="778b1-118">L'aspetto dell'immagine è X:Y, dove X:Y è il rapporto tra la larghezza dell'immagine e l'altezza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="778b1-118">Picture aspect ratio is notated X:Y, where X:Y is the ratio of picture width to picture height.</span></span> <span data-ttu-id="778b1-119">La maggior parte degli standard video usa proporzioni dell'immagine 4:3 o 16:9.</span><span class="sxs-lookup"><span data-stu-id="778b1-119">Most video standards use either 4:3 or 16:9 picture aspect ratio.</span></span> <span data-ttu-id="778b1-120">Le proporzioni 16:9 sono comunemente denominate *widescreen*.</span><span class="sxs-lookup"><span data-stu-id="778b1-120">The 16:9 aspect ratio is commonly called *widescreen*.</span></span> <span data-ttu-id="778b1-121">Cinema film usa spesso una proporzione 1:85:1 o 1:66:1.</span><span class="sxs-lookup"><span data-stu-id="778b1-121">Cinema film often uses a 1:85:1 or 1:66:1 aspect ratio.</span></span> <span data-ttu-id="778b1-122">Le proporzioni dell'immagine sono denominate anche proporzioni di *visualizzazione* (Dar).</span><span class="sxs-lookup"><span data-stu-id="778b1-122">Picture aspect ratio is also called *display aspect ratio* (DAR).</span></span>

![diagramma che mostra le proporzioni 4:3 e 16:9](images/aspect-ratio01.png)

<span data-ttu-id="778b1-124">In alcuni casi l'immagine video non ha la stessa forma dell'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="778b1-124">Sometimes the video image does not have the same shape as the display area.</span></span> <span data-ttu-id="778b1-125">Ad esempio, un video 4:3 potrebbe essere visualizzato su un televisore widescreen (16 × 9).</span><span class="sxs-lookup"><span data-stu-id="778b1-125">For example, a 4:3 video might be shown on a widescreen (16×9) television.</span></span> <span data-ttu-id="778b1-126">Nel video del computer il video potrebbe essere visualizzato all'interno di una finestra con dimensioni arbitrarie.</span><span class="sxs-lookup"><span data-stu-id="778b1-126">In computer video, the video might be shown inside a window that has an arbitrary size.</span></span> <span data-ttu-id="778b1-127">In tal caso, è possibile creare l'immagine in tre modi per adattarla all'area di visualizzazione:</span><span class="sxs-lookup"><span data-stu-id="778b1-127">In that case, there are three ways the image can be made to fit within the display area:</span></span>

-   <span data-ttu-id="778b1-128">Estendere l'immagine lungo un asse per adattarla all'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="778b1-128">Stretch the image along one axis to fit the display area.</span></span>
-   <span data-ttu-id="778b1-129">Ridimensionare l'immagine per adattarla all'area di visualizzazione, mantenendo le proporzioni originali dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="778b1-129">Scale the image to fit the display area, while maintaining the original picture aspect ratio.</span></span>
-   <span data-ttu-id="778b1-130">Ritagliare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="778b1-130">Crop the image.</span></span>

<span data-ttu-id="778b1-131">L'adattamento dell'immagine per adattarla all'area di visualizzazione è quasi sempre errato, perché non mantiene le proporzioni dell'immagine corrette.</span><span class="sxs-lookup"><span data-stu-id="778b1-131">Stretching the image to fit the display area is almost always wrong, because it does not preserve the correct picture aspect ratio.</span></span>

### <a name="letterboxing"></a><span data-ttu-id="778b1-132">Letterboxing</span><span class="sxs-lookup"><span data-stu-id="778b1-132">Letterboxing</span></span>

<span data-ttu-id="778b1-133">Il processo di ridimensionamento di un'immagine widescreen per adattarsi a una visualizzazione 4:3 è denominato *letterbox*, illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="778b1-133">The process of scaling a widescreen image to fit a 4:3 display is called *letterboxing*, shown in the next diagram.</span></span> <span data-ttu-id="778b1-134">Le aree rectanglular risultanti nella parte superiore e inferiore dell'immagine vengono in genere compilate con il nero, sebbene sia possibile utilizzare altri colori.</span><span class="sxs-lookup"><span data-stu-id="778b1-134">The resulting rectanglular areas at the top and bottom of the image are typically filled with black, although other colors can be used.</span></span>

![diagramma che mostra la modalità corretta per la letterbox](images/aspect-ratio02.png)

<span data-ttu-id="778b1-136">In caso contrario, il ridimensionamento di un'immagine 4:3 per adattarsi a una visualizzazione widescreen viene talvolta denominato *pillarbox*.</span><span class="sxs-lookup"><span data-stu-id="778b1-136">The reverse case, scaling a 4:3 image to fit a widescreen display, is sometimes called *pillarboxing*.</span></span> <span data-ttu-id="778b1-137">Tuttavia, il termine *letterbox* viene anche usato in senso generale, per indicare la scalabilità di un'immagine video per adattarsi a qualsiasi area di visualizzazione specificata.</span><span class="sxs-lookup"><span data-stu-id="778b1-137">However, the term *letterbox* is also used in a general sense, to mean scaling a video image to fit any given display area.</span></span>

![diagramma che mostra pillarbox](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a><span data-ttu-id="778b1-139">Pan-and-Scan</span><span class="sxs-lookup"><span data-stu-id="778b1-139">Pan-and-Scan</span></span>

<span data-ttu-id="778b1-140">Pan-and-Scan è una tecnica per cui un'immagine in formato widescreen viene ritagliata in un'area rettangolare da 4 × 3, per la visualizzazione in un dispositivo di visualizzazione 4:3.</span><span class="sxs-lookup"><span data-stu-id="778b1-140">Pan-and-scan is a technique whereby a widescreen image is cropped to a 4×3 rectangular area, for display on a 4:3 display device.</span></span> <span data-ttu-id="778b1-141">L'immagine risultante riempie l'intero schermo, senza richiedere le aree della cassetta nera, ma le parti dell'immagine originale vengono ritagliate dall'immagine.</span><span class="sxs-lookup"><span data-stu-id="778b1-141">The resulting image fills the entire display, without requiring black letterbox areas, but portions of the original image are cropped out of the picture.</span></span> <span data-ttu-id="778b1-142">L'area ritagliata può spostarsi dal fotogramma al frame, in quanto l'area di interesse viene spostata.</span><span class="sxs-lookup"><span data-stu-id="778b1-142">The area that is cropped can move from frame to frame, as the area of interest shifts.</span></span> <span data-ttu-id="778b1-143">Il termine "Pan" in *Pan-and-Scan* si riferisce all'effetto di panning causato dallo spostamento dell'area di Pan-and-Scan.</span><span class="sxs-lookup"><span data-stu-id="778b1-143">The term "pan" in *pan-and-scan* refers to the panning effect that is caused by moving the pan-and-scan area.</span></span>

![diagramma che illustra la Panoramica di Pan-and-Scan](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a><span data-ttu-id="778b1-145">Proporzioni pixel</span><span class="sxs-lookup"><span data-stu-id="778b1-145">Pixel Aspect Ratio</span></span>

<span data-ttu-id="778b1-146">Proporzioni *pixel* (par) misura la forma di un pixel.</span><span class="sxs-lookup"><span data-stu-id="778b1-146">*Pixel aspect ratio* (PAR) measures the shape of a pixel.</span></span>

<span data-ttu-id="778b1-147">Quando viene acquisita un'immagine digitale, l'immagine viene campionata verticalmente e orizzontalmente, ottenendo una matrice rettangolare di campioni quantizzati, denominati *pixel* o *Pels*.</span><span class="sxs-lookup"><span data-stu-id="778b1-147">When a digital image is captured, the image is sampled both vertically and horizontally, resulting in a rectangular array of quantized samples, called *pixels* or *pels*.</span></span> <span data-ttu-id="778b1-148">La forma della griglia di campionamento determina la forma dei pixel nell'immagine digitalizzata.</span><span class="sxs-lookup"><span data-stu-id="778b1-148">The shape of the sampling grid determines the shape of the pixels in the digitized image.</span></span>

<span data-ttu-id="778b1-149">Di seguito è riportato un esempio che usa piccoli numeri per semplificare la matematica.</span><span class="sxs-lookup"><span data-stu-id="778b1-149">Here is an example that uses small numbers to keep the math simple.</span></span> <span data-ttu-id="778b1-150">Si supponga che l'immagine originale sia quadrata (ovvero, le proporzioni dell'immagine sono 1:1); e si supponga che la griglia di campionamento includa 12 elementi, disposti in una griglia di 4 × 3.</span><span class="sxs-lookup"><span data-stu-id="778b1-150">Suppose that the original image is square (that is, the picture aspect ratio is 1:1); and suppose the sampling grid contains 12 elements, arranged in a 4×3 grid.</span></span> <span data-ttu-id="778b1-151">La forma di ogni pixel risultante sarà più alta rispetto a quella estesa.</span><span class="sxs-lookup"><span data-stu-id="778b1-151">The shape of each resulting pixel will be taller than it is wide.</span></span> <span data-ttu-id="778b1-152">In particolare, la forma di ogni pixel sarà 3 × 4.</span><span class="sxs-lookup"><span data-stu-id="778b1-152">Specifically, the shape of each pixel will be 3×4.</span></span> <span data-ttu-id="778b1-153">I pixel che non sono quadrati sono detti *pixel non quadrati*.</span><span class="sxs-lookup"><span data-stu-id="778b1-153">Pixels that are not square are called *non-square pixels*.</span></span>

![diagramma che mostra una griglia di campionamento non quadrato](images/aspect-ratio05.png)

<span data-ttu-id="778b1-155">Le proporzioni dei pixel si applicano anche al dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="778b1-155">Pixel aspect ratio also applies to the display device.</span></span> <span data-ttu-id="778b1-156">La forma fisica del dispositivo di visualizzazione e la risoluzione dei pixel fisici (in orizzontale e in basso) determinano la PAR del dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="778b1-156">The physical shape of the display device and the physical pixel resolution (across and down) determine the PAR of the display device.</span></span> <span data-ttu-id="778b1-157">I monitoraggi computer utilizzano in genere pixel quadrati.</span><span class="sxs-lookup"><span data-stu-id="778b1-157">Computer monitors generally use square pixels.</span></span> <span data-ttu-id="778b1-158">Se la par dell'immagine e la PAR della visualizzazione non corrispondono, l'immagine deve essere ridimensionata in una dimensione, verticalmente o orizzontalmente, per poter essere visualizzata correttamente.</span><span class="sxs-lookup"><span data-stu-id="778b1-158">If the image PAR and the display PAR do not match, the image must be scaled in one dimension, either vertically or horizontally, in order to display correctly.</span></span> <span data-ttu-id="778b1-159">La formula seguente mette in relazione PAR, Display aspect ratio (DAR) e dimensioni dell'immagine in pixel:</span><span class="sxs-lookup"><span data-stu-id="778b1-159">The following formula relates PAR, display aspect ratio (DAR), and image size in pixels:</span></span>

<span data-ttu-id="778b1-160">*Dar* = (*Larghezza immagine* in pixel  /  *altezza in pixel*) × *par*</span><span class="sxs-lookup"><span data-stu-id="778b1-160">*DAR* = (*image width in pixels* / *image height in pixels*) × *PAR*</span></span>

<span data-ttu-id="778b1-161">Si noti che la larghezza dell'immagine e l'altezza dell'immagine in questa formula fanno riferimento all'immagine in memoria, non all'immagine visualizzata.</span><span class="sxs-lookup"><span data-stu-id="778b1-161">Note that image width and image height in this formula refer to the image in memory, not the displayed image.</span></span>

<span data-ttu-id="778b1-162">Ecco un esempio reale: il video analogico NTSC-M contiene 480 righe di analisi nell'area immagine attiva.</span><span class="sxs-lookup"><span data-stu-id="778b1-162">Here is a real-world example: NTSC-M analog video contains 480 scan lines in the active image area.</span></span> <span data-ttu-id="778b1-163">ITU-R REC. BT. 601 specifica una frequenza di campionamento orizzontale di 704 pixel visibili per riga, restituendo un'immagine digitale con 704 x 480 pixel.</span><span class="sxs-lookup"><span data-stu-id="778b1-163">ITU-R Rec. BT.601 specifies a horizontal sampling rate of 704 visible pixels per line, yielding a digital image with 704 x 480 pixels.</span></span> <span data-ttu-id="778b1-164">Le proporzioni dell'immagine desiderate sono pari a 4:3, ottenendo un valore pari a 10:11.</span><span class="sxs-lookup"><span data-stu-id="778b1-164">The intended picture aspect ratio is 4:3, yielding a PAR of 10:11.</span></span>

-   <span data-ttu-id="778b1-165">DAR: 4:3</span><span class="sxs-lookup"><span data-stu-id="778b1-165">DAR: 4:3</span></span>
-   <span data-ttu-id="778b1-166">Larghezza in pixel: 704</span><span class="sxs-lookup"><span data-stu-id="778b1-166">Width in pixels: 704</span></span>
-   <span data-ttu-id="778b1-167">Altezza in pixel: 480</span><span class="sxs-lookup"><span data-stu-id="778b1-167">Height in pixels: 480</span></span>
-   <span data-ttu-id="778b1-168">PAR: 10/11</span><span class="sxs-lookup"><span data-stu-id="778b1-168">PAR: 10/11</span></span>

<span data-ttu-id="778b1-169">4/3 = (704/420) x (10/11)</span><span class="sxs-lookup"><span data-stu-id="778b1-169">4/3 = (704/420) x (10/11)</span></span>

<span data-ttu-id="778b1-170">Per visualizzare correttamente questa immagine in un dispositivo di visualizzazione con pixel quadrati, è necessario ridimensionare la larghezza di 10/11 o l'altezza di 11/10.</span><span class="sxs-lookup"><span data-stu-id="778b1-170">To display this image correctly on a display device with square pixels, you must scale either the width by 10/11 or the height by 11/10.</span></span>

## <a name="working-with-aspect-ratios"></a><span data-ttu-id="778b1-171">Utilizzo delle proporzioni</span><span class="sxs-lookup"><span data-stu-id="778b1-171">Working with Aspect Ratios</span></span>

<span data-ttu-id="778b1-172">La forma corretta di un frame video è definita dalle proporzioni in *pixel* (par) e dall' *area di visualizzazione*.</span><span class="sxs-lookup"><span data-stu-id="778b1-172">The correct shape of a video frame is defined by the *pixel aspect ratio* (PAR) and the *display area*.</span></span>

-   <span data-ttu-id="778b1-173">Il PAR definisce la forma dei pixel in un'immagine.</span><span class="sxs-lookup"><span data-stu-id="778b1-173">The PAR defines the shape of the pixels in an image.</span></span> <span data-ttu-id="778b1-174">I pixel quadrati hanno proporzioni pari a 1:1.</span><span class="sxs-lookup"><span data-stu-id="778b1-174">Square pixels have an aspect ratio of 1:1.</span></span> <span data-ttu-id="778b1-175">Tutte le altre proporzioni descrivono un pixel non quadrato.</span><span class="sxs-lookup"><span data-stu-id="778b1-175">Any other aspect ratio describes a non-square pixel.</span></span> <span data-ttu-id="778b1-176">Ad esempio, la televisione NTSC USA un 10:11 PAR.</span><span class="sxs-lookup"><span data-stu-id="778b1-176">For example, NTSC television uses a 10:11 PAR.</span></span> <span data-ttu-id="778b1-177">Supponendo che si stia visualizzando il video in un monitor del computer, la visualizzazione avrà i pixel quadrati (1:1 PAR).</span><span class="sxs-lookup"><span data-stu-id="778b1-177">Assuming that you are presenting the video on a computer monitor, the display will have square pixels (1:1 PAR).</span></span> <span data-ttu-id="778b1-178">La PAR del contenuto di origine viene specificata nell'attributo [**delle \_ \_ \_ proporzioni \_ del pixel MF mt**](mf-mt-pixel-aspect-ratio-attribute.md) sul tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="778b1-178">The PAR of the source content is given in the [**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute on the media type.</span></span>
-   <span data-ttu-id="778b1-179">L'area di visualizzazione è l'area dell'immagine video che deve essere visualizzata.</span><span class="sxs-lookup"><span data-stu-id="778b1-179">The display area is the region of the video image that is intended to be shown.</span></span> <span data-ttu-id="778b1-180">Esistono due aree di visualizzazione rilevanti che possono essere specificate nel tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="778b1-180">There are two relevant display areas that might be specified in the media type:</span></span>
    -   <span data-ttu-id="778b1-181">Apertura Pan-and-Scan.</span><span class="sxs-lookup"><span data-stu-id="778b1-181">Pan-and-scan aperture.</span></span> <span data-ttu-id="778b1-182">L'apertura Pan-and-Scan è un'area di video da 4 × 3 che dovrebbe essere visualizzata in modalità Pan/Scan.</span><span class="sxs-lookup"><span data-stu-id="778b1-182">The pan-and-scan aperture is a 4×3 region of video that should be displayed in pan/scan mode.</span></span> <span data-ttu-id="778b1-183">Viene usato per mostrare contenuto a schermo intero in una visualizzazione 4 × 3 senza letterbox.</span><span class="sxs-lookup"><span data-stu-id="778b1-183">It is used to show wide-screen content on a 4×3 display without letterboxing.</span></span> <span data-ttu-id="778b1-184">L'apertura di Pan-and-Scan è specificata nell'attributo dell'apertura di Pan [**\_ \_ \_ \_ Scan MF mt**](mf-mt-pan-scan-aperture-attribute.md) e deve essere usata solo quando l'attributo [**MF \_ mt \_ Pan \_ Scan \_ Enabled**](mf-mt-pan-scan-enabled-attribute.md) è **true**.</span><span class="sxs-lookup"><span data-stu-id="778b1-184">The pan-and-scan aperture is given in the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute and should be used only when the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute is **TRUE**.</span></span>
    -   <span data-ttu-id="778b1-185">Visualizza apertura.</span><span class="sxs-lookup"><span data-stu-id="778b1-185">Display aperture.</span></span> <span data-ttu-id="778b1-186">Questa apertura è definita in alcuni standard video.</span><span class="sxs-lookup"><span data-stu-id="778b1-186">This aperture is defined in some video standards.</span></span> <span data-ttu-id="778b1-187">Qualsiasi elemento all'esterno dell'apertura di visualizzazione è l'area di overscan e non deve essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="778b1-187">Anything outside of the display aperture is the overscan region and should not be displayed.</span></span> <span data-ttu-id="778b1-188">Ad esempio, la televisione NTSC è 720 × 480 pixel con un diaframma di visualizzazione di 704 × 480.</span><span class="sxs-lookup"><span data-stu-id="778b1-188">For example, NTSC television is 720×480 pixels with a display aperture of 704×480.</span></span> <span data-ttu-id="778b1-189">L'apertura di visualizzazione viene specificata nell'attributo di [**\_ \_ \_ \_ apertura della visualizzazione minima MF mt**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="778b1-189">The display aperture is given in the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span> <span data-ttu-id="778b1-190">Se presente, deve essere usato quando la modalità Pan-and-Scan è **false**.</span><span class="sxs-lookup"><span data-stu-id="778b1-190">If present, it should be used when pan-and-scan mode is **FALSE**.</span></span>

<span data-ttu-id="778b1-191">Se la modalità Pan-and-can è **false** e non è definita alcuna apertura di visualizzazione, verrà visualizzato l'intero frame video.</span><span class="sxs-lookup"><span data-stu-id="778b1-191">If pan-and-can mode is **FALSE** and no display aperture is defined, the entire video frame should be displayed.</span></span> <span data-ttu-id="778b1-192">In realtà, questo è il caso per la maggior parte dei contenuti video diversi dalla televisione e dal video DVD.</span><span class="sxs-lookup"><span data-stu-id="778b1-192">In fact, this is the case for most video content other than television and DVD video.</span></span> <span data-ttu-id="778b1-193">Le proporzioni dell'intera immagine vengono calcolate come (  /  *Altezza area di visualizzazione* Larghezza area di visualizzazione) × *par*.</span><span class="sxs-lookup"><span data-stu-id="778b1-193">The aspect ratio of the entire picture is calculated as (*display area width* / *display area height*) × *PAR*.</span></span>

## <a name="code-examples"></a><span data-ttu-id="778b1-194">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="778b1-194">Code Examples</span></span>

### <a name="finding-the-display-area"></a><span data-ttu-id="778b1-195">Ricerca dell'area di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="778b1-195">Finding the Display Area</span></span>

<span data-ttu-id="778b1-196">Nel codice seguente viene illustrato come ottenere l'area di visualizzazione dal tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="778b1-196">The following code shows how to get the display area from the media type.</span></span>


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a><span data-ttu-id="778b1-197">Conversione tra proporzioni in pixel</span><span class="sxs-lookup"><span data-stu-id="778b1-197">Converting Between Pixel Aspect Ratios</span></span>

<span data-ttu-id="778b1-198">Nel codice riportato di seguito viene illustrato come convertire un rettangolo da una proporzioni in pixel (PAR) a un altro, mantenendo le proporzioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="778b1-198">The following code shows how to convert a rectangle from one pixel aspect ratio (PAR) to another, while preserving the picture aspect ratio.</span></span>


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a><span data-ttu-id="778b1-199">Calcolo dell'area letterbox</span><span class="sxs-lookup"><span data-stu-id="778b1-199">Calculating the Letterbox Area</span></span>

<span data-ttu-id="778b1-200">Il codice seguente calcola l'area Letterbox, dato un rettangolo di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="778b1-200">The following code calculates the letterbox area, given a source and destination rectangle.</span></span> <span data-ttu-id="778b1-201">Si presuppone che entrambi i rettangoli abbiano lo stesso PAR.</span><span class="sxs-lookup"><span data-stu-id="778b1-201">It is assumed that both rectangles have the same PAR.</span></span>


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a><span data-ttu-id="778b1-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="778b1-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="778b1-203">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="778b1-203">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="778b1-204">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="778b1-204">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="778b1-205">**\_ \_ \_ apertura minima schermo \_ MF mt**</span><span class="sxs-lookup"><span data-stu-id="778b1-205">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="778b1-206">**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="778b1-206">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="778b1-207">**\_ \_ Analisi panoramica MF \_ mt \_ abilitata**</span><span class="sxs-lookup"><span data-stu-id="778b1-207">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[<span data-ttu-id="778b1-208">**proporzioni MF \_ mt \_ pixel \_ \_**</span><span class="sxs-lookup"><span data-stu-id="778b1-208">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



