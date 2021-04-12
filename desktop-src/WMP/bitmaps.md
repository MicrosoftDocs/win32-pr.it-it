---
title: Bitmap (Windows Media Player SDK)
description: Bitmap
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, bitmap
- interfacce, bitmap
- informazioni di riferimento per interfacce, bitmap
- bitmap nelle interfacce, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474764"
---
# <a name="bitmaps-windows-media-player-sdk"></a><span data-ttu-id="5c4dd-107">Bitmap (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="5c4dd-107">Bitmaps (Windows Media Player SDK)</span></span>

<span data-ttu-id="5c4dd-108">È necessario usare una o più immagini nell'interfaccia personalizzata e ogni immagine deve essere definita nel file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5c4dd-108">You must use one or more images in your skin, and each image must be defined in the skin definition file.</span></span> <span data-ttu-id="5c4dd-109">Se non si definisce un'immagine in questa sezione, l'interfaccia non sarà in grado di utilizzarla.</span><span class="sxs-lookup"><span data-stu-id="5c4dd-109">If you do not define an image in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="5c4dd-110">Il termine "bitmap" viene usato in tutto il riferimento in senso generico e fa riferimento alle immagini bitmap con estensione bmp, immagini GIF con estensione gif, immagini JPEG con estensione jpg e immagini PNG con estensione png.</span><span class="sxs-lookup"><span data-stu-id="5c4dd-110">The term "bitmap" is used throughout the reference in a generic sense, and refers to bitmap images with a .bmp extension, GIF images with a .gif extension, JPEG images with a .jpg extension, and PNG images with a .png extension.</span></span>

<span data-ttu-id="5c4dd-111">La sezione bitmap del file di definizione dell'interfaccia personalizzata inizia con questa riga:</span><span class="sxs-lookup"><span data-stu-id="5c4dd-111">The Bitmaps section of the skin definition file begins with this line:</span></span>


```C++
[ Bitmaps ]

```



<span data-ttu-id="5c4dd-112">È quindi necessario aggiungere una o più righe contenenti informazioni su ognuna delle immagini nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5c4dd-112">You then must add one or more lines that contain information about each of the images in your skin.</span></span>

<span data-ttu-id="5c4dd-113">Una linea tipica potrebbe essere:</span><span class="sxs-lookup"><span data-stu-id="5c4dd-113">A typical line might be:</span></span>


```C++
    Background  Background.bmp  0,0

```



<span data-ttu-id="5c4dd-114">È possibile usare il modello seguente per la sezione bitmap del file di definizione dell'interfaccia personalizzata:</span><span class="sxs-lookup"><span data-stu-id="5c4dd-114">You can use the following template for the Bitmaps section of your skin definition file:</span></span>


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



<span data-ttu-id="5c4dd-115">Per le informazioni bitmap per ogni riga della sezione bitmap, è necessario utilizzare l'ordine seguente.</span><span class="sxs-lookup"><span data-stu-id="5c4dd-115">You must use the following order for bitmap information for each line in the Bitmap section.</span></span> <span data-ttu-id="5c4dd-116">Ogni parte della riga è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="5c4dd-116">Each part of the line is required.</span></span>

1.  [<span data-ttu-id="5c4dd-117">Tipo di bitmap</span><span class="sxs-lookup"><span data-stu-id="5c4dd-117">Bitmap Type</span></span>](bitmap-type.md)
2.  [<span data-ttu-id="5c4dd-118">Nome file</span><span class="sxs-lookup"><span data-stu-id="5c4dd-118">File Name</span></span>](file-name.md)
3.  [<span data-ttu-id="5c4dd-119">Coordinate</span><span class="sxs-lookup"><span data-stu-id="5c4dd-119">Coordinates</span></span>](coordinates.md)

<span data-ttu-id="5c4dd-120">Per un esempio di codice bitmap, vedere la [sezione relativa alla bitmap di esempio](sample-bitmap-section.md).</span><span class="sxs-lookup"><span data-stu-id="5c4dd-120">For an example of bitmap code, see [Sample Bitmap Section](sample-bitmap-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c4dd-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c4dd-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c4dd-122">**Riferimento all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="5c4dd-122">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




