---
description: Direct3D supporta l'ombreggiatura sia flat che Gouraud. Il valore predefinito è Gouraud shading. Per controllare la modalità di ombreggiatura corrente, l'applicazione C++ specifica un membro del tipo enumerato D3DSHADEMODE per lo \_ stato di rendering D3DRS MODOOMBRA.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Stato ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebac826704fee0e1903c1aa2a2348bff4a089c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304063"
---
# <a name="shading-state-direct3d-9"></a><span data-ttu-id="a4b0c-105">Stato ombreggiatura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a4b0c-105">Shading State (Direct3D 9)</span></span>

<span data-ttu-id="a4b0c-106">Direct3D supporta l'ombreggiatura sia flat che Gouraud.</span><span class="sxs-lookup"><span data-stu-id="a4b0c-106">Direct3D supports both flat and Gouraud shading.</span></span> <span data-ttu-id="a4b0c-107">Il valore predefinito è Gouraud shading.</span><span class="sxs-lookup"><span data-stu-id="a4b0c-107">The default is Gouraud shading.</span></span> <span data-ttu-id="a4b0c-108">Per controllare la modalità di ombreggiatura corrente, l'applicazione C++ specifica un membro del tipo enumerato [**D3DSHADEMODE**](./d3dshademode.md) per lo \_ stato di rendering D3DRS MODOOMBRA.</span><span class="sxs-lookup"><span data-stu-id="a4b0c-108">To control the current shading mode, your C++ application specifies a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type for the D3DRS\_SHADEMODE render state.</span></span>

<span data-ttu-id="a4b0c-109">Nell'esempio di codice C++ riportato di seguito viene illustrato il processo di impostazione dello stato di ombreggiatura sulla modalità ombreggiatura piatta.</span><span class="sxs-lookup"><span data-stu-id="a4b0c-109">The following C++ code example demonstrates the process of setting the shading state to flat shading mode.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a><span data-ttu-id="a4b0c-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4b0c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4b0c-111">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="a4b0c-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
