---
title: Formati di file di immagine
description: Formati di file di immagine
ms.assetid: 803479e8-0e00-4724-80b7-9d86709c43db
keywords:
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, formati di file
- Windows Media Player Skin, formati di file per l'arte
- interfacce, formati di file per l'arte
- formati di file per l'arte personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35af72fd502cb23e81063fe9513b4a9311f9557
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332436"
---
# <a name="art-file-formats"></a><span data-ttu-id="eeb8a-110">Formati di file di immagine</span><span class="sxs-lookup"><span data-stu-id="eeb8a-110">Art File Formats</span></span>

<span data-ttu-id="eeb8a-111">I formati di file di immagine seguenti sono riconosciuti da Windows Media Player per le interfacce:</span><span class="sxs-lookup"><span data-stu-id="eeb8a-111">The following art file formats are recognized by Windows Media Player for skins:</span></span>



| <span data-ttu-id="eeb8a-112">Formato</span><span class="sxs-lookup"><span data-stu-id="eeb8a-112">Format</span></span>                                  | <span data-ttu-id="eeb8a-113">Estensione</span><span class="sxs-lookup"><span data-stu-id="eeb8a-113">Extension</span></span>   | <span data-ttu-id="eeb8a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeb8a-114">Description</span></span>                                                                                        |
|-----------------------------------------|-------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb8a-115">Bitmap</span><span class="sxs-lookup"><span data-stu-id="eeb8a-115">Bitmap</span></span>                                  | <span data-ttu-id="eeb8a-116">bmp</span><span class="sxs-lookup"><span data-stu-id="eeb8a-116">.bmp</span></span>        | <span data-ttu-id="eeb8a-117">Le immagini bitmap sono consigliate perché offrono il massimo controllo sull'immagine e sui colori esatti.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-117">Bitmap images are recommended because they offer the most control over the exact image and colors.</span></span> |
| <span data-ttu-id="eeb8a-118">Graphics Interchange Format (GIF)</span><span class="sxs-lookup"><span data-stu-id="eeb8a-118">Graphics Interchange Format (GIF)</span></span>       | <span data-ttu-id="eeb8a-119">gif</span><span class="sxs-lookup"><span data-stu-id="eeb8a-119">.gif</span></span>        | <span data-ttu-id="eeb8a-120">Formato di immagine compresso usato per le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-120">Compressed image format used for webpages.</span></span> <span data-ttu-id="eeb8a-121">Sono supportate le gif animate.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-121">Animated GIFs are supported.</span></span>                            |
| <span data-ttu-id="eeb8a-122">Joint Photographic Experts Group (JPEG)</span><span class="sxs-lookup"><span data-stu-id="eeb8a-122">Joint Photographic Experts Group (JPEG)</span></span> | <span data-ttu-id="eeb8a-123">.jpeg, .jpg</span><span class="sxs-lookup"><span data-stu-id="eeb8a-123">.jpeg, .jpg</span></span> | <span data-ttu-id="eeb8a-124">Formato di immagine compresso usato per le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-124">Compressed image format used for webpages.</span></span>                                                         |
| <span data-ttu-id="eeb8a-125">Portable Network Graphics (PNG)</span><span class="sxs-lookup"><span data-stu-id="eeb8a-125">Portable Network Graphics (PNG)</span></span>         | <span data-ttu-id="eeb8a-126">png</span><span class="sxs-lookup"><span data-stu-id="eeb8a-126">.png</span></span>        | <span data-ttu-id="eeb8a-127">Formato di immagine compresso usato per le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-127">Compressed image format used for webpages.</span></span>                                                         |



 

<span data-ttu-id="eeb8a-128">Se si usa uno dei formati di file compressi che definisce un colore come trasparente per un Web browser, non definire un colore come trasparente nel file di immagine.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-128">If you use one of the compressed file formats that defines a color as transparent to a Web browser, do not define a color as transparent in the image file.</span></span> <span data-ttu-id="eeb8a-129">Usare un colore visibile per rappresentare le aree trasparenti nell'immagine e quindi definire il colore come trasparente nel file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-129">Use a visible color to represent transparent areas in your image, and then define that color as transparent in the skin definition file.</span></span> <span data-ttu-id="eeb8a-130">Se, ad esempio, si crea un file GIF con alcune aree trasparenti, questi non saranno trasparenti nell'immagine finale e non sarà possibile usare il colore impostato come trasparente nel file gif per il colore della trasparenza nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="eeb8a-130">For example, if you create a GIF file with some areas transparent, they will not be transparent in your final image and you will not be able to use the color you set as transparent in your gif file for the transparency color in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeb8a-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eeb8a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeb8a-132">**File di immagine**</span><span class="sxs-lookup"><span data-stu-id="eeb8a-132">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 




