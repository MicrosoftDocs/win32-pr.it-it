---
description: Direct3D usa un tipo di filtro di trama lineare denominato filtro bilineare.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Filtro di trama lineare (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521929"
---
# <a name="linear-texture-filtering-direct3d-9"></a><span data-ttu-id="ac048-103">Filtro di trama lineare (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ac048-103">Linear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="ac048-104">Direct3D usa un tipo di filtro di trama lineare denominato filtro bilineare.</span><span class="sxs-lookup"><span data-stu-id="ac048-104">Direct3D uses a form of linear texture filtering called bilinear filtering.</span></span> <span data-ttu-id="ac048-105">Analogamente al [campionamento dei punti più vicini (Direct3D 9)](nearest-point-sampling.md), il filtro di trama bilineare prima calcola un indirizzo Texel, che in genere non è un indirizzo Integer.</span><span class="sxs-lookup"><span data-stu-id="ac048-105">Like [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md), bilinear texture filtering first computes a texel address, which is usually not an integer address.</span></span> <span data-ttu-id="ac048-106">Filtraggio bilineare trova quindi il Texel il cui indirizzo Integer è più vicino all'indirizzo calcolato.</span><span class="sxs-lookup"><span data-stu-id="ac048-106">Bilinear filtering then finds the texel whose integer address is closest to the computed address.</span></span> <span data-ttu-id="ac048-107">Il modulo di rendering Direct3D, inoltre, calcola una media ponderata dei Texel che si trovano immediatamente sopra, sotto, a sinistra di e a destra del punto di campionamento più vicino.</span><span class="sxs-lookup"><span data-stu-id="ac048-107">In addition, the Direct3D rendering module computes a weighted average of the texels that are immediately above, below, to the left of, and to the right of the nearest sample point.</span></span>

<span data-ttu-id="ac048-108">Selezionare filtro di trama bilineare richiamando il metodo [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) .</span><span class="sxs-lookup"><span data-stu-id="ac048-108">Select bilinear texture filtering by invoking the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="ac048-109">Impostare il valore del primo parametro sul numero di indice Integer (0-7) della trama per cui si seleziona un metodo di filtro della trama.</span><span class="sxs-lookup"><span data-stu-id="ac048-109">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="ac048-110">Passare D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER o D3DSAMP \_ MIPFILTER per il secondo parametro per impostare il filtro di ingrandimento, minification o mapping MIP.</span><span class="sxs-lookup"><span data-stu-id="ac048-110">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="ac048-111">Passare D3DTEXF \_ Linear nel terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="ac048-111">Pass D3DTEXF\_LINEAR in the third parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac048-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac048-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac048-113">Filtraggio trama</span><span class="sxs-lookup"><span data-stu-id="ac048-113">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 
