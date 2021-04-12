---
description: In genere, l'applicazione eseguirà il rendering di scene 3D in maniera più realistica se usa mappe chiare colorate. Una mappa chiara colorata usa i dati RGB nella mappa chiara per le relative informazioni di illuminazione.
ms.assetid: 47760884-7b9f-45de-9d4a-faf822da899f
title: Mappe per la luce del colore (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 621c5056fe2cbb9e6446adfb5dcad3079c0d90bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483173"
---
# <a name="color-light-maps-direct3d-9"></a><span data-ttu-id="dee80-104">Mappe per la luce del colore (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dee80-104">Color Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="dee80-105">In genere, l'applicazione eseguirà il rendering di scene 3D in maniera più realistica se usa mappe chiare colorate.</span><span class="sxs-lookup"><span data-stu-id="dee80-105">Your application will usually render 3D scenes more realistically if it uses colored light maps.</span></span> <span data-ttu-id="dee80-106">Una mappa chiara colorata usa i dati RGB nella mappa chiara per le relative informazioni di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="dee80-106">A colored light map uses the RGB data in the light map for its lighting information.</span></span>

<span data-ttu-id="dee80-107">Nell'esempio di codice C++ riportato di seguito viene illustrato il mapping leggero con i dati cromatici RGB.</span><span class="sxs-lookup"><span data-stu-id="dee80-107">The following C++ code example demonstrates light mapping with RGB color data.</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains RGB light map data.

// Set the light map texture as the first texture.
d3dDevice->SetTexture(0, lptexLightMap);

d3dDevice->SetTextureStageState( 0,D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0,D3DTSS_COLORARG2, D3DTA_DIFFUSE );
```



<span data-ttu-id="dee80-108">Questo esempio imposta la mappa chiara come prima trama.</span><span class="sxs-lookup"><span data-stu-id="dee80-108">This example sets the light map as the first texture.</span></span> <span data-ttu-id="dee80-109">Imposta quindi lo stato della prima fase di fusione per modulare i dati della trama in ingresso.</span><span class="sxs-lookup"><span data-stu-id="dee80-109">It then sets the state of the first blending stage to modulate the incoming texture data.</span></span> <span data-ttu-id="dee80-110">Usa la prima trama e il colore corrente della primitiva come argomenti dell'operazione di modulazione.</span><span class="sxs-lookup"><span data-stu-id="dee80-110">It uses the first texture and the current color of the primitive as the arguments to the modulate operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dee80-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dee80-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dee80-112">Mapping chiaro con trame</span><span class="sxs-lookup"><span data-stu-id="dee80-112">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



