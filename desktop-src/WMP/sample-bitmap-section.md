---
title: Sezione bitmap di esempio
description: Sezione bitmap di esempio
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, bitmap
- interfacce, bitmap
- informazioni di riferimento per interfacce, bitmap
- bitmap in interfacce, sezione bitmap
- file di definizione dell'interfaccia, sezione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856569"
---
# <a name="sample-bitmap-section"></a><span data-ttu-id="b9730-108">Sezione bitmap di esempio</span><span class="sxs-lookup"><span data-stu-id="b9730-108">Sample Bitmap Section</span></span>

<span data-ttu-id="b9730-109">Le righe seguenti mostrano una tipica sezione bitmap di un file di definizione dell'interfaccia personalizzata:</span><span class="sxs-lookup"><span data-stu-id="b9730-109">The following lines show a typical Bitmaps section of a skin definition file:</span></span>


```C++
[ Bitmaps ]

//  <Type>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0
    

```



<span data-ttu-id="b9730-110">Definisce cinque bitmap che vengono usate per creare un'immagine di sfondo, immagini per i pulsanti disabilitati e di cui è stato eseguito il push, un'immagine di area per i pulsanti di area e un'immagine con privilegi avanzati per trackbars.</span><span class="sxs-lookup"><span data-stu-id="b9730-110">This defines five bitmaps that are used to create a Background image, images for Disabled and Pushed buttons, a Region image for region buttons, and a Super image for trackbars.</span></span>

> [!Note]  
> <span data-ttu-id="b9730-111">L'area e le bitmap con privilegi avanzati sono deprecate nelle interfacce per Windows Media Player 10 mobile o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b9730-111">The Region and Super bitmaps are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b9730-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9730-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9730-113">**Bitmap**</span><span class="sxs-lookup"><span data-stu-id="b9730-113">**Bitmaps**</span></span>](bitmaps.md)
</dt> </dl>

 

 




