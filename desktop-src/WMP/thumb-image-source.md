---
title: Origine immagine Thumb
description: Origine immagine Thumb
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player Mobile Skins, trackbars
- interfacce, TrackBar
- riferimento per Skin, trackbars
- TrackBar in interfacce, origine immagine
- TrackBar in Skin, origine immagine Thumb
- origine immagine per Skin, trackbars
- Thumb, origine immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044376"
---
# <a name="thumb-image-source"></a><span data-ttu-id="12ebe-110">Origine immagine Thumb</span><span class="sxs-lookup"><span data-stu-id="12ebe-110">Thumb Image Source</span></span>

<span data-ttu-id="12ebe-111">È necessario definire il nome del file che contiene l'immagine Thumb.</span><span class="sxs-lookup"><span data-stu-id="12ebe-111">You must define the name of the file that contains the thumb image.</span></span> <span data-ttu-id="12ebe-112">Deve essere un nome di file valido con estensione bmp, gif, jpg o png.</span><span class="sxs-lookup"><span data-stu-id="12ebe-112">This must be a valid file name with the extension .bmp, .gif, .jpg, or .png.</span></span> <span data-ttu-id="12ebe-113">Il file deve contenere tre immagini side-by-side di dimensioni identiche.</span><span class="sxs-lookup"><span data-stu-id="12ebe-113">The file must contain three side-by-side images of identical size.</span></span> <span data-ttu-id="12ebe-114">Devono essere adiacenti tra loro senza spazi.</span><span class="sxs-lookup"><span data-stu-id="12ebe-114">They must be adjacent to each other with no space between.</span></span> <span data-ttu-id="12ebe-115">La posizione superiore sinistra dell'immagine di sinistra deve essere nell'angolo superiore sinistro del file.</span><span class="sxs-lookup"><span data-stu-id="12ebe-115">The top-left position of the left image must be at the top-left corner of the file.</span></span> <span data-ttu-id="12ebe-116">L'immagine a sinistra è l'immagine normale per l'immagine del cursore e l'immagine al centro raffigura lo stato di push e l'immagine a destra illustra lo stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="12ebe-116">The image on the left side is the normal image for the thumb image, and the image in the middle depicts the pushed state and the image on the right depicts the disabled state.</span></span>


```C++
SeekThumb.bmp

```



<span data-ttu-id="12ebe-117">Potrebbe essere necessario rendere trasparente alcune aree dell'immagine Thumb.</span><span class="sxs-lookup"><span data-stu-id="12ebe-117">You may want to make certain areas of the thumb image transparent.</span></span> <span data-ttu-id="12ebe-118">Ciò consentirà di creare immagini Thumb in forme diverse da rettangolare.</span><span class="sxs-lookup"><span data-stu-id="12ebe-118">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="12ebe-119">Qualsiasi area dell'immagine Thumb riempita con il colore specificato dal valore RGB 255, 0, 255 verrà visualizzata trasparente nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="12ebe-119">Any region of the thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12ebe-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12ebe-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12ebe-121">**TrackBar**</span><span class="sxs-lookup"><span data-stu-id="12ebe-121">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




