---
description: Alcune schede dei tasti di scelta rapida 3D meno recenti non supportano la combinazione di trame usando il valore alfa del pixel di destinazione.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Mappe chiare monocromatiche (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303801"
---
# <a name="monochrome-light-maps-direct3d-9"></a><span data-ttu-id="4eb68-103">Mappe chiare monocromatiche (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4eb68-103">Monochrome Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="4eb68-104">Alcune schede dei tasti di scelta rapida 3D meno recenti non supportano la combinazione di trame usando il valore alfa del pixel di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4eb68-104">Some older 3D accelerator boards do not support texture blending using the alpha value of the destination pixel.</span></span> <span data-ttu-id="4eb68-105">Per ulteriori informazioni, vedere [Alpha texture blending (Direct3D 9)](alpha-texture-blending.md) .</span><span class="sxs-lookup"><span data-stu-id="4eb68-105">See [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) for more information.</span></span> <span data-ttu-id="4eb68-106">Questi adapter, in genere, non supportano la combinazione di più trame.</span><span class="sxs-lookup"><span data-stu-id="4eb68-106">These adapters also generally do not support multiple texture blending.</span></span> <span data-ttu-id="4eb68-107">Se l'applicazione è in esecuzione in una scheda, ad esempio, può usare la combinazione di trame MultiPASS per eseguire il mapping chiaro monocromatico.</span><span class="sxs-lookup"><span data-stu-id="4eb68-107">If your application is running on an adapter such as this, it can use multipass texture blending to perform monochrome light mapping.</span></span>

<span data-ttu-id="4eb68-108">Per eseguire il mapping chiaro monocromatico, un'applicazione archivia le informazioni di illuminazione nei dati alfa delle trame della mappa chiara.</span><span class="sxs-lookup"><span data-stu-id="4eb68-108">To perform monochrome light mapping, an application stores the lighting information in the alpha data of its light map textures.</span></span> <span data-ttu-id="4eb68-109">L'applicazione usa le funzionalità di filtro della trama di Direct3D per eseguire un mapping da ogni pixel nell'immagine della primitiva a un Texel corrispondente nella mappa chiara.</span><span class="sxs-lookup"><span data-stu-id="4eb68-109">The application uses the texture filtering capabilities of Direct3D to perform a mapping from each pixel in the primitive's image to a corresponding texel in the light map.</span></span> <span data-ttu-id="4eb68-110">Imposta il fattore di fusione di origine sul valore alfa del Texel corrispondente.</span><span class="sxs-lookup"><span data-stu-id="4eb68-110">It sets the source blending factor to the alpha value of the corresponding texel.</span></span>

<span data-ttu-id="4eb68-111">Nell'esempio seguente viene illustrato il modo in cui un'applicazione può utilizzare una trama come mappa chiara monocromatica:</span><span class="sxs-lookup"><span data-stu-id="4eb68-111">The following example illustrates how an application can use a texture as a monochrome light map:</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



<span data-ttu-id="4eb68-112">Poiché gli adattatori di visualizzazione che non supportano la fusione alfa di destinazione in genere non supportano la combinazione di più trame, in questo esempio viene impostata la mappa chiara come prima trama, disponibile in tutte le schede di accelerazione 3D.</span><span class="sxs-lookup"><span data-stu-id="4eb68-112">Because display adapters that do not support destination alpha blending usually do not support multiple texture blending, this example sets the light map as the first texture, which is available on all 3D accelerator cards.</span></span> <span data-ttu-id="4eb68-113">Il codice di esempio imposta l'operazione di colore per la fase di fusione della trama per combinare i dati della trama con il colore esistente della primitiva.</span><span class="sxs-lookup"><span data-stu-id="4eb68-113">The sample code sets the color operation for the texture's blending stage to blend the texture data with the primitive's existing color.</span></span> <span data-ttu-id="4eb68-114">Quindi seleziona la prima trama e il colore esistente della primitiva come dati di input.</span><span class="sxs-lookup"><span data-stu-id="4eb68-114">It then selects the first texture and the primitive's existing color as the input data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4eb68-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4eb68-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4eb68-116">Mapping chiaro con trame</span><span class="sxs-lookup"><span data-stu-id="4eb68-116">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



