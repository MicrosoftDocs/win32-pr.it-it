---
description: Il motore di illuminazione Direct3D può usare i dati relativi al colore per ogni vertice durante l'illuminazione se si indica al runtime che i dati sono presenti.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Stato del colore Per-Vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401059"
---
# <a name="per-vertex-color-state-direct3d-9"></a><span data-ttu-id="23efc-103">Stato del colore Per-Vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23efc-103">Per-Vertex Color State (Direct3D 9)</span></span>

<span data-ttu-id="23efc-104">Il motore di illuminazione Direct3D può usare i dati relativi al colore per ogni vertice durante l'illuminazione se si indica al runtime che i dati sono presenti.</span><span class="sxs-lookup"><span data-stu-id="23efc-104">The Direct3D lighting engine can use per-vertex color data when performing lighting if you tell the runtime the data is present.</span></span> <span data-ttu-id="23efc-105">Questa operazione viene eseguita attivando lo stato di rendering seguente:</span><span class="sxs-lookup"><span data-stu-id="23efc-105">This is done by turning on the following render state:</span></span>


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



<span data-ttu-id="23efc-106">Se il colore per vertice è abilitato, le applicazioni possono configurare l'origine da cui il sistema recupera le informazioni sui colori per un vertice.</span><span class="sxs-lookup"><span data-stu-id="23efc-106">If per-vertex color is enabled, applications can configure the source from which the system retrieves color information for a vertex.</span></span> <span data-ttu-id="23efc-107">Gli \_ Stati di rendering D3DRS AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS EMISSIVEMATERIALSOURCE \_ e D3DRS \_ SPECULARMATERIALSOURCE controllano rispettivamente le origini dei componenti di ambiente, diffuse, emissivo e speculare.</span><span class="sxs-lookup"><span data-stu-id="23efc-107">The D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE render states control the ambient, diffuse, emissive, and specular color component sources, respectively.</span></span> <span data-ttu-id="23efc-108">Ogni stato può essere impostato sui membri del tipo enumerato [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) , che definisce le costanti che indicano al sistema di usare il materiale corrente, il colore diffuso o il colore speculare come origine per il componente colore specificato.</span><span class="sxs-lookup"><span data-stu-id="23efc-108">Each state can be set to members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type, which defines constants that instruct the system to use the current material, diffuse color, or specular color as the source for the specified color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23efc-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23efc-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23efc-110">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="23efc-110">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
