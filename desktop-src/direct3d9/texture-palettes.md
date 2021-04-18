---
description: Direct3D 9 supporta le trame con tavolozza tramite un set di tavolozze di voci 256 associate all'oggetto IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Tavolozze delle trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303974"
---
# <a name="texture-palettes-direct3d-9"></a><span data-ttu-id="1f8a1-103">Tavolozze delle trame (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1f8a1-103">Texture Palettes (Direct3D 9)</span></span>

<span data-ttu-id="1f8a1-104">Direct3D 9 supporta le trame con tavolozza tramite un set di tavolozze di voci 256 associate all'oggetto [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="1f8a1-104">Direct3D 9 supports paletted textures through a set of 256 entry palettes associated with the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) object.</span></span> <span data-ttu-id="1f8a1-105">Una tavolozza viene resa corrente chiamando il metodo [**IDirect3DDevice9:: SetCurrentTexturePalette**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="1f8a1-105">A palette is made current by calling the [**IDirect3DDevice9::SetCurrentTexturePalette**](/windows/desktop/api) method.</span></span> <span data-ttu-id="1f8a1-106">La tavolozza corrente viene usata per tradurre tutte le trame con tavolozza per tutte le fasi di trama attive.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-106">The current palette is used for translating all paletted textures for all active texture stages.</span></span> <span data-ttu-id="1f8a1-107">[**IDirect3DDevice9:: SetPaletteEntries**](/windows/desktop/api) Aggiorna tutte le voci della tavolozza 256.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-107">[**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) updates all of a palette's 256 entries.</span></span> <span data-ttu-id="1f8a1-108">Ogni voce è una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) nel formato D3DFMT \_ A8R8G8B8.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-108">Each entry is a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure of the format D3DFMT\_A8R8G8B8.</span></span> <span data-ttu-id="1f8a1-109">Per impostazione predefinita, tutte le voci sono 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-109">All entries default to 0xFFFFFFFF.</span></span>

<span data-ttu-id="1f8a1-110">Le tavolozze [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contengono un canale alfa.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-110">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) palettes contain an alpha channel.</span></span> <span data-ttu-id="1f8a1-111">Questo canale alfa può essere usato quando \_ è impostato il flag di funzionalità del dispositivo ALPHAPALETTE D3DPTEXTURECAPS, che indica che il dispositivo supporta Alpha dalla tavolozza.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-111">This alpha channel can be used when the D3DPTEXTURECAPS\_ALPHAPALETTE device capability flag is set, indicating that the device supports alpha from the palette.</span></span> <span data-ttu-id="1f8a1-112">Il canale alfa della tavolozza viene usato quando il formato della trama non ha un canale alfa.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-112">The palette alpha channel is used when the texture format does not have an alpha channel.</span></span> <span data-ttu-id="1f8a1-113">Se il dispositivo non supporta Alpha dalla tavolozza e il formato di trama non ha un canale alfa, viene usato il valore 0xFF per Alpha.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-113">If the device does not support alpha from the palette and the texture format does not have an alpha channel, then a value of 0xFF is used for alpha.</span></span>

<span data-ttu-id="1f8a1-114">È disponibile un massimo di 65.536 tavolozze (0x0000FFFF).</span><span class="sxs-lookup"><span data-stu-id="1f8a1-114">There is a maximum of 65,536 (0x0000FFFF) palettes.</span></span> <span data-ttu-id="1f8a1-115">Poiché le risorse di memoria associate al set di tavolozze sono proporzionali al numero massimo di tavolozza a cui fa riferimento un'applicazione, utilizzare numeri di tavolozza contigui a partire da zero.</span><span class="sxs-lookup"><span data-stu-id="1f8a1-115">Because memory resources associated with the set of palettes are proportional to the maximum palette number that an application references, use contiguous palette numbers starting at zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f8a1-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f8a1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f8a1-117">Concetti di base sulla texturing</span><span class="sxs-lookup"><span data-stu-id="1f8a1-117">Basic Texturing Concepts</span></span>](basic-texturing-concepts.md)
</dt> </dl>

 

 
