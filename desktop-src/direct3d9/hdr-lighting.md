---
description: L'illuminazione nel mondo reale contiene un intervallo dinamico molto elevato (HDR) di valori di luminanza.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Illuminazione HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225295"
---
# <a name="hdr-lighting-direct3d-9"></a><span data-ttu-id="06f45-103">Illuminazione HDR (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="06f45-103">HDR Lighting (Direct3D 9)</span></span>

<span data-ttu-id="06f45-104">L'illuminazione nel mondo reale contiene un intervallo dinamico molto elevato (HDR) di valori di luminanza.</span><span class="sxs-lookup"><span data-stu-id="06f45-104">Lighting in the real world contains a very high dynamic range (HDR) of luminance values.</span></span> <span data-ttu-id="06f45-105">Il mondo reale ha circa 10 ordini di intervallo dinamico (DR) per i valori di luminanza distribuiti attraverso la gamma di oscurità alla luminosità.</span><span class="sxs-lookup"><span data-stu-id="06f45-105">The real world has about 10 orders of dynamic range (DR) for luminance values spread across the spectrum of darkness to brightness.</span></span> <span data-ttu-id="06f45-106">D'altra parte, una schermata del computer ha una gamma di visualizzazione molto limitata (o un intervallo di valori di luminanza): circa due ordini di intervallo dinamico.</span><span class="sxs-lookup"><span data-stu-id="06f45-106">On the other hand, a computer screen has a very limited display gamut (or range of luminance values): approximately two orders of dynamic range.</span></span> <span data-ttu-id="06f45-107">La sfida alla produzione di immagini con rendering HDR consiste nel mappare i valori HDR del mondo reale alla gamma limitata di uno schermo del computer.</span><span class="sxs-lookup"><span data-stu-id="06f45-107">The challenge to producing HDR rendered images is to map the real world HDR values into the limited gamut of a computer screen.</span></span>

<span data-ttu-id="06f45-108">Il mapping dei toni è la tecnica usata da DirectX per il mapping delle informazioni HDR in un intervallo più limitato.</span><span class="sxs-lookup"><span data-stu-id="06f45-108">Tone mapping is the technique used by DirectX for mapping HDR information into a more limited range.</span></span> <span data-ttu-id="06f45-109">Il mapping dei toni applicato al rendering CGI può migliorare significativamente la quantità di dettagli di illuminazione di cui è stato eseguito il rendering, consentendo di visualizzare i dettagli nelle aree più scure e mettendo a confronto le aree che sono così luminose, sembrano bruciate.</span><span class="sxs-lookup"><span data-stu-id="06f45-109">Tone mapping applied to CGI rendering can dramatically improve the amount of lighting detail rendered, allowing details in the darkest areas to be seen, and providing contrast in areas that are so bright, they appear burned.</span></span> <span data-ttu-id="06f45-110">Le scene risultanti eseguono il rendering con dettagli di illuminazione molto più visibili.</span><span class="sxs-lookup"><span data-stu-id="06f45-110">The resulting scenes render with far more visible lighting detail.</span></span>

<span data-ttu-id="06f45-111">L' [esempio HDRLighting](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) è un esempio di SDK che illustra l'illuminazione HDR.</span><span class="sxs-lookup"><span data-stu-id="06f45-111">[HDRLighting Sample](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) is a SDK sample that demonstrates HDR lighting.</span></span>

## <a name="tone-mapping"></a><span data-ttu-id="06f45-112">Mapping dei toni</span><span class="sxs-lookup"><span data-stu-id="06f45-112">Tone Mapping</span></span>

<span data-ttu-id="06f45-113">Il mapping dei toni consente in genere di simulare fenomeni ottici che non possono essere causati dal ripristino di emergenza del monitor.</span><span class="sxs-lookup"><span data-stu-id="06f45-113">Tone mapping generally simulates optical phenomena that cannot be caused by the DR of the monitor.</span></span> <span data-ttu-id="06f45-114">Esempi di questo scenario sono i fuochi o i fiori (che sono principalmente proprietà delle lenti), il turno blu che si verifica nell'occhio umano in condizioni di scarsa luminosità e altri adattamenti che sono il risultato della biochimica dell'occhio.</span><span class="sxs-lookup"><span data-stu-id="06f45-114">Examples of this are flares or blooming (which are mostly properties of lenses), the blue shift that happens in the human eye in low light conditions, and other adaptations that are a result of the biochemistry of the eye.</span></span> <span data-ttu-id="06f45-115">Se il ripristino di emergenza del display era sufficientemente grande, il mapping dei toni non sarebbe stato necessario, a meno che non si forniscano effetti artistici o alcune delle proprietà di una fotocamera o un dispositivo a pagamento (CCD).</span><span class="sxs-lookup"><span data-stu-id="06f45-115">If the DR of the display were large enough, tone mapping would not be as neccessary, except for providing artistic effects or some of the properties of a camera lens or a charge coupled device (CCD).</span></span>

<span data-ttu-id="06f45-116">Il mapping dei toni divide l'intervallo di valori di luminanza in una scena in un set di zone.</span><span class="sxs-lookup"><span data-stu-id="06f45-116">Tone mapping divides the range of luminance values in a scene into a set of zones.</span></span> <span data-ttu-id="06f45-117">Ogni zona comprende un intervallo di valori di luminanza.</span><span class="sxs-lookup"><span data-stu-id="06f45-117">Each zone encompasses a range of luminance values.</span></span>

<span data-ttu-id="06f45-118">HDR usa i termini seguenti:</span><span class="sxs-lookup"><span data-stu-id="06f45-118">HDR uses the following terms:</span></span>

-   <span data-ttu-id="06f45-119">Area-intervallo di valori di luminanza</span><span class="sxs-lookup"><span data-stu-id="06f45-119">Zone - range of luminance values</span></span>
-   <span data-ttu-id="06f45-120">Grigio medio-area della luminosità intermedia della scena</span><span class="sxs-lookup"><span data-stu-id="06f45-120">Middle gray - middle brightness region of the scene</span></span>
-   <span data-ttu-id="06f45-121">Intervallo dinamico-rapporto della luminanza della scena più alta alla luminanza della scena più bassa</span><span class="sxs-lookup"><span data-stu-id="06f45-121">Dynamic range - ratio of the highest scene luminance to the lowest scene luminance</span></span>
-   <span data-ttu-id="06f45-122">Misurazione soggettiva dell'illuminazione della scena: varia da chiaro a moderato a scuro</span><span class="sxs-lookup"><span data-stu-id="06f45-122">Key - subjective measurement of scene lighting: this varies from light to moderate to dark</span></span>

<span data-ttu-id="06f45-123">Per calcolare la luminanza dai valori RGB, usare:</span><span class="sxs-lookup"><span data-stu-id="06f45-123">To calculate luminance from RGB values, use this:</span></span>


```
L = 0.27R + 0.67G + 0.06B;
```



<span data-ttu-id="06f45-124">La luminanza media dei log è un'approssimazione utile per la chiave di una scena.</span><span class="sxs-lookup"><span data-stu-id="06f45-124">The log-average luminance is a useful approximation for the key of a scene.</span></span> <span data-ttu-id="06f45-125">Un'equazione generale ha un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="06f45-125">A general equation looks like this:</span></span>

<span data-ttu-id="06f45-126">L<sub>w</sub> = exp \[ 1/N ( \[ log Sum (Delta + L<sub>w</sub>(x, y)) \] ) \]</span><span class="sxs-lookup"><span data-stu-id="06f45-126">L<sub>w</sub> = exp\[ 1 / N( sum\[ log( delta + L<sub>w</sub>( x, y ) ) \] ) \]</span></span>

<span data-ttu-id="06f45-127">Dove:</span><span class="sxs-lookup"><span data-stu-id="06f45-127">Where:</span></span>

-   <span data-ttu-id="06f45-128">L<sub>w</sub> -log-luminanza media</span><span class="sxs-lookup"><span data-stu-id="06f45-128">L<sub>w</sub> - log-average luminance</span></span>
-   <span data-ttu-id="06f45-129">N: numero di pixel nell'immagine</span><span class="sxs-lookup"><span data-stu-id="06f45-129">N - number of pixels in the image</span></span>
-   <span data-ttu-id="06f45-130">Delta: fattore ridotto per evitare problemi con i pixel neri</span><span class="sxs-lookup"><span data-stu-id="06f45-130">delta - a small factor to avoid problems with black pixels</span></span>
-   <span data-ttu-id="06f45-131">L<sub>w</sub>(x, y): luminanza dello spazio globale per pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="06f45-131">L<sub>w</sub>( x, y ) - the world space luminance for pixel ( x, y )</span></span>

<span data-ttu-id="06f45-132">Per eseguire il mapping di questo oggetto a un valore grigio medio, di seguito è riportato un operatore di ridimensionamento della luminanza:</span><span class="sxs-lookup"><span data-stu-id="06f45-132">To map this to a middle-gray value, here is a luminance scaling operator:</span></span>

<span data-ttu-id="06f45-133">L (x, y) = a \* l<sub>w</sub>(x, y)/L<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="06f45-133">L( x, y ) = a \* L<sub>w</sub>( x, y ) / L<sub>w</sub></span></span>

<span data-ttu-id="06f45-134">Dove:</span><span class="sxs-lookup"><span data-stu-id="06f45-134">Where:</span></span>

-   <span data-ttu-id="06f45-135">L (x, y): luminanza ridimensionata per pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="06f45-135">L( x, y ) - scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="06f45-136">valore della chiave-image dopo l'applicazione del ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="06f45-136">a - image key value after applying the scaling</span></span>

<span data-ttu-id="06f45-137">Infine, di seguito è riportato un semplice operatore di mapping dei toni per comprimere le luminanze elevate:</span><span class="sxs-lookup"><span data-stu-id="06f45-137">And finally, here is a simple tone mapping operator for compressing the high luminances:</span></span>

<span data-ttu-id="06f45-138">L<sub>d</sub>(x, y) = l (x, y)/(1 + L (x, y))</span><span class="sxs-lookup"><span data-stu-id="06f45-138">L<sub>d</sub>( x, y ) = L( x, y ) / ( 1 + L( x, y ) )</span></span>

<span data-ttu-id="06f45-139">Dove:</span><span class="sxs-lookup"><span data-stu-id="06f45-139">Where:</span></span>

-   <span data-ttu-id="06f45-140">L<sub>d</sub>(x, y): luminanza compressa e scalata per pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="06f45-140">L<sub>d</sub>( x, y ) - compressed and scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="06f45-141">valore della chiave-image dopo l'applicazione del ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="06f45-141">a - image key value after applying the scaling</span></span>

<span data-ttu-id="06f45-142">Questo operatore ridimensiona le luminanze elevate di 1/L e le luminanze basse di 1.</span><span class="sxs-lookup"><span data-stu-id="06f45-142">This operator scales high luminances by 1/L and low luminances by 1.</span></span> <span data-ttu-id="06f45-143">Per ulteriori informazioni, vedere il seguente documento.</span><span class="sxs-lookup"><span data-stu-id="06f45-143">For more details, see the following paper.</span></span>

<span data-ttu-id="06f45-144">Reinhard, Erik, Mike Stark, Peter Shirley e James Ferwerda.</span><span class="sxs-lookup"><span data-stu-id="06f45-144">Reinhard, Erik, Mike Stark, Peter Shirley, and James Ferwerda.</span></span> <span data-ttu-id="06f45-145">["Riproduzione del tono fotografico per le immagini digitali"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span><span class="sxs-lookup"><span data-stu-id="06f45-145">["Photographic Tone Reproduction for Digital Images"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span></span> <span data-ttu-id="06f45-146">ACM Transactions on Graphics (TOG), procedimenti della 29a annuale Conference on computer graphics and Interactive Techniques (SIGGRAPH), pp. 267-276.</span><span class="sxs-lookup"><span data-stu-id="06f45-146">ACM Transactions on Graphics (TOG), Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques (SIGGRAPH), pp. 267-276.</span></span> <span data-ttu-id="06f45-147">New York, NY: ACM Press, 2002.</span><span class="sxs-lookup"><span data-stu-id="06f45-147">New York, NY: ACM Press, 2002.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06f45-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06f45-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06f45-149">Argomenti avanzati</span><span class="sxs-lookup"><span data-stu-id="06f45-149">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 



