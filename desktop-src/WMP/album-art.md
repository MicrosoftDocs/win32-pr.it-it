---
title: Album artistico
description: Album artistico
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Windows Media Player Mobile Skins, album Art
- Skin, album Art
- informazioni di riferimento per Skins, album Art
- file di immagine per Skins, album Art
- Album Art in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298028"
---
# <a name="album-art"></a><span data-ttu-id="2daad-108">Album artistico</span><span class="sxs-lookup"><span data-stu-id="2daad-108">Album Art</span></span>

<span data-ttu-id="2daad-109">Quando si crea un'interfaccia per Windows Media Player 10 mobile o versione successiva, è possibile che si desideri visualizzare gli album grafici che fanno riferimento all'elemento multimediale attualmente in riproduzione.</span><span class="sxs-lookup"><span data-stu-id="2daad-109">When you create a skin for Windows Media Player 10 Mobile or later, you may want to display album art that relates to the currently playing media item.</span></span> <span data-ttu-id="2daad-110">Quando si progetta l'interfaccia, è consigliabile riservare spazio nell'immagine di sfondo per contenere l'immagine dell'album.</span><span class="sxs-lookup"><span data-stu-id="2daad-110">When you design your skin, you will want to reserve space in the Background image to contain the album art.</span></span>

<span data-ttu-id="2daad-111">La sezione album art del file di definizione dell'interfaccia deve iniziare con la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="2daad-111">The Album Art section of the skin definition file must begin with the following line:</span></span>


```C++
[ Album Art ]

```



<span data-ttu-id="2daad-112">È quindi necessario aggiungere le informazioni che specificano la posizione e le dimensioni dell'immagine dell'album nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2daad-112">You then must add information that specifies the location and size of the album art in your skin.</span></span> <span data-ttu-id="2daad-113">È necessario immettere quattro numeri interi positivi, separati da virgole che definiscono la sinistra, la parte superiore, la larghezza e l'altezza dell'arte dell'album, in pixel, rispetto all'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="2daad-113">You must enter four positive integers, separated by commas that define the left, top, width, and height of the album art, in pixels, relative to the background image.</span></span> <span data-ttu-id="2daad-114">Nell'esempio seguente viene illustrato come specificare le dimensioni:</span><span class="sxs-lookup"><span data-stu-id="2daad-114">The following example shows how to specify dimensions:</span></span>


```C++
//  <Location>
//  ----------
   5,37,230,155

```



<span data-ttu-id="2daad-115">Se si prevede di includere una sezione video nell'interfaccia utente, è possibile usare le stesse dimensioni e la stessa posizione per l'arte degli album per conservare spazio.</span><span class="sxs-lookup"><span data-stu-id="2daad-115">If you plan on including a video section in your skin, you can use the same size and location for your album art to conserve space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2daad-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2daad-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2daad-117">**Riferimento all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="2daad-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




