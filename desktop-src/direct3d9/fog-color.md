---
description: Il colore di nebbia per la nebbia dei pixel e dei vertici viene impostato tramite lo \_ stato di rendering FogColor di D3DRS. I valori dello stato di rendering possono essere qualsiasi colore RGB, specificato come colore RGBA. Il componente alfa viene ignorato.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Colore nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048869"
---
# <a name="fog-color-direct3d-9"></a><span data-ttu-id="8984b-105">Colore nebbia (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8984b-105">Fog Color (Direct3D 9)</span></span>

<span data-ttu-id="8984b-106">Il colore di nebbia per la nebbia dei pixel e dei vertici viene impostato tramite lo \_ stato di rendering FogColor di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="8984b-106">Fog color for both pixel and vertex fog is set through the D3DRS\_FOGCOLOR render state.</span></span> <span data-ttu-id="8984b-107">I valori dello stato di rendering possono essere qualsiasi colore RGB, specificato come colore RGBA.</span><span class="sxs-lookup"><span data-stu-id="8984b-107">The render state values can be any RGB color, specified as an RGBA color.</span></span> <span data-ttu-id="8984b-108">Il componente alfa viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="8984b-108">The alpha component is ignored.</span></span>

<span data-ttu-id="8984b-109">Nell'esempio C++ riportato di seguito il colore della nebbia viene impostato su bianco.</span><span class="sxs-lookup"><span data-stu-id="8984b-109">The following C++ example sets the fog color to white.</span></span>


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



<span data-ttu-id="8984b-110">La nebbia viene applicata in modo diverso dalla pipeline della funzione fissa e dalla pipeline programmabile.</span><span class="sxs-lookup"><span data-stu-id="8984b-110">Fog is applied differently by the fixed function pipeline and the programmable pipeline.</span></span>

1.  <span data-ttu-id="8984b-111">Se il driver supporta D3DPMISCCAPS \_ FOGANDSPECULARALPHA:</span><span class="sxs-lookup"><span data-stu-id="8984b-111">If the driver supports D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="8984b-112">Se viene usata la pipeline della funzione fissa e D3DRS \_ FogColor è impostato, V1. w (nella pixel shader) è uguale al valore impostato in fog RenderState.</span><span class="sxs-lookup"><span data-stu-id="8984b-112">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, v1.w (in the pixel shader) equals the value set in fog renderstate.</span></span>
    -   <span data-ttu-id="8984b-113">Se viene usata la pipeline programmabile, V1. w (nella pixel shader) è uguale a 0, anche se oD1. w è scritto in modo esplicito in un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="8984b-113">If the programmable pipeline is used, then v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>
2.  <span data-ttu-id="8984b-114">Se il driver non supporta il \_ FOGANDSPECULARALPHA D3DPMISCCAPS:</span><span class="sxs-lookup"><span data-stu-id="8984b-114">If the driver does NOT support D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="8984b-115">Se viene usata la pipeline della funzione fissa e \_ viene impostato D3DRS FogColor, V1. w (nel pixel shader) è uguale al valore impostato in fog RenderState.</span><span class="sxs-lookup"><span data-stu-id="8984b-115">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, then v1.w (in the pixel shader) equals value set in fog renderstate.</span></span>
    -   <span data-ttu-id="8984b-116">Se oFog viene scritto in modo esplicito in un vertex shader, V1. w (nella pixel shader) è uguale a oFog, con un valore compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="8984b-116">If oFog is explicitly written in a vertex shader, v1.w (in the pixel shader) equals oFog, clamped between 0 and 1.</span></span>
    -   <span data-ttu-id="8984b-117">Se nessuno dei due casi precedenti si applica, V1. w (nella pixel shader) è uguale a 0, anche se oD1. w è scritto in modo esplicito in un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="8984b-117">If neither of the above two cases applies, v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>

<span data-ttu-id="8984b-118">Per ulteriori informazioni, vedere [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="8984b-118">For more information, see [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8984b-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8984b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8984b-120">Tipi di nebbia</span><span class="sxs-lookup"><span data-stu-id="8984b-120">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



