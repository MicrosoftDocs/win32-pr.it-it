---
description: La fusione di nebbia si riferisce all'applicazione del fattore di nebbia ai colori dell'oggetto e della nebbia per produrre il colore finale visualizzato in una scena, come descritto in formule di nebbia (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Blending di nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123351"
---
# <a name="fog-blending-direct3d-9"></a><span data-ttu-id="b0381-103">Blending di nebbia (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b0381-103">Fog Blending (Direct3D 9)</span></span>

<span data-ttu-id="b0381-104">La fusione di nebbia si riferisce all'applicazione del fattore di nebbia ai colori dell'oggetto e della nebbia per produrre il colore finale visualizzato in una scena, come descritto in [formule di nebbia (Direct3D 9)](fog-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="b0381-104">Fog blending refers to the application of the fog factor to the fog and object colors to produce the final color that appears in a scene, as discussed in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="b0381-105">Lo \_ stato di rendering FOGENABLE di D3DRS controlla la fusione di nebbia.</span><span class="sxs-lookup"><span data-stu-id="b0381-105">The D3DRS\_FOGENABLE render state controls fog blending.</span></span> <span data-ttu-id="b0381-106">Impostare questo stato di rendering su **true** per abilitare la fusione di nebbia, come illustrato nel codice di esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="b0381-106">Set this render state to **TRUE** to enable fog blending as shown in the following example code.</span></span> <span data-ttu-id="b0381-107">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="b0381-107">The default is **FALSE**.</span></span>


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



<span data-ttu-id="b0381-108">È necessario abilitare la fusione di nebbia sia per la nebbia dei pixel che per il vertice.</span><span class="sxs-lookup"><span data-stu-id="b0381-108">You must enable fog blending for both pixel fog and vertex fog.</span></span> <span data-ttu-id="b0381-109">Per informazioni sull'uso di questi tipi di nebbia, vedere [pixel Fog (Direct3D 9)](pixel-fog.md) e [Vertex Fog (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="b0381-109">For information about using these types of fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0381-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0381-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0381-111">Tipi di nebbia</span><span class="sxs-lookup"><span data-stu-id="b0381-111">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



