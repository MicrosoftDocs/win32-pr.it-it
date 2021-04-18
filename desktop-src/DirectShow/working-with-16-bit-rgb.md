---
description: Uso di RGB a 16 bit
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Uso di RGB a 16 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313393"
---
# <a name="working-with-16-bit-rgb"></a><span data-ttu-id="66058-103">Uso di RGB a 16 bit</span><span class="sxs-lookup"><span data-stu-id="66058-103">Working with 16-bit RGB</span></span>

<span data-ttu-id="66058-104">Sono definiti due formati per RGB non compresso a 16 bit:</span><span class="sxs-lookup"><span data-stu-id="66058-104">Two formats are defined for 16-bit uncompressed RGB:</span></span>

-   <span data-ttu-id="66058-105">MEDIASUBTYPE \_ 555 utilizza cinque bit per i componenti rosso, verde e blu in un pixel.</span><span class="sxs-lookup"><span data-stu-id="66058-105">MEDIASUBTYPE\_555 uses five bits each for the red, green, and blue components in a pixel.</span></span> <span data-ttu-id="66058-106">Il bit più significativo nella **parola** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="66058-106">The most significant bit in the **WORD** is ignored.</span></span>
-   <span data-ttu-id="66058-107">MEDIASUBTYPE \_ 565 utilizza cinque bit per i componenti rosso e blu e sei bit per il componente verde.</span><span class="sxs-lookup"><span data-stu-id="66058-107">MEDIASUBTYPE\_565 uses five bits for the red and blue components, and six bits for the green component.</span></span> <span data-ttu-id="66058-108">Questo formato riflette il fatto che la visione umana è più sensibile alle parti verdi dello spettro visibile.</span><span class="sxs-lookup"><span data-stu-id="66058-108">This format reflects the fact that human vision is most sensitive to the green portions of the visible spectrum.</span></span>

<span data-ttu-id="66058-109">**RGB 565**</span><span class="sxs-lookup"><span data-stu-id="66058-109">**RGB 565**</span></span>

<span data-ttu-id="66058-110">Per estrarre i componenti dei colori da un'immagine RGB 565, considerare ogni pixel come un tipo di **parola** e usare le maschere di bit seguenti:</span><span class="sxs-lookup"><span data-stu-id="66058-110">To extract the color components from an RGB 565 image, treat each pixel as a **WORD** type and use the following bit masks:</span></span>


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



<span data-ttu-id="66058-111">Ottenere i componenti dei colori da un pixel come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="66058-111">Get the color components from a pixel as follows:</span></span>


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



<span data-ttu-id="66058-112">Tenere presente che i canali rosso e blu sono a 5 bit e il canale verde è a 6 bit.</span><span class="sxs-lookup"><span data-stu-id="66058-112">Remember that the red and blue channels are 5 bits and the green channel is 6 bits.</span></span> <span data-ttu-id="66058-113">Per convertire questi valori in componenti a 8 bit (per RGB a 24 bit o a 32 bit), è necessario spostare a sinistra il numero di bit appropriato:</span><span class="sxs-lookup"><span data-stu-id="66058-113">To convert these values to 8-bit components (for 24-bit or 32-bit RGB), you must left-shift the appropriate number of bits:</span></span>


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="66058-114">Invertire questo processo per creare un pixel RGB 565.</span><span class="sxs-lookup"><span data-stu-id="66058-114">Reverse this process to create an RGB 565 pixel.</span></span> <span data-ttu-id="66058-115">Supponendo che i valori dei colori siano stati troncati al numero corretto di bit:</span><span class="sxs-lookup"><span data-stu-id="66058-115">Assuming the color values have been truncated to the correct number of bits:</span></span>


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



<span data-ttu-id="66058-116">**RGB 555**</span><span class="sxs-lookup"><span data-stu-id="66058-116">**RGB 555**</span></span>

<span data-ttu-id="66058-117">L'uso di RGB 555 è essenzialmente uguale a quello di RGB 565, tranne per le maschere di bit e le operazioni di spostamento di bit sono diverse.</span><span class="sxs-lookup"><span data-stu-id="66058-117">Working with RGB 555 is essentially the same as RGB 565, except the bit masks and bit shift operations are different.</span></span> <span data-ttu-id="66058-118">Per ottenere i componenti colore da un pixel RGB 555, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="66058-118">To get the color components from an RGB 555 pixel, do the following:</span></span>


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="66058-119">Per comprimere i valori di colore rosso, verde e blu in un pixel RGB 555, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="66058-119">To pack the red, green, and blue color values into an RGB 555 pixel, do the following:</span></span>


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a><span data-ttu-id="66058-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66058-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66058-121">Sottotipi video RGB non compressi</span><span class="sxs-lookup"><span data-stu-id="66058-121">Uncompressed RGB Video Subtypes</span></span>](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



