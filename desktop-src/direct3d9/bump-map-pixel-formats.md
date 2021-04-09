---
description: Una mappa Bump è un oggetto IDirect3DTexture9 che usa un formato pixel specializzato.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formati di pixel della mappa Bump (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049253"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a><span data-ttu-id="f09c7-103">Formati di pixel della mappa Bump (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f09c7-103">Bump Map Pixel Formats (Direct3D 9)</span></span>

<span data-ttu-id="f09c7-104">Una mappa Bump è un oggetto [**IDirect3DTexture9**](/windows/desktop/api) che usa un formato pixel specializzato.</span><span class="sxs-lookup"><span data-stu-id="f09c7-104">A bump map is an [**IDirect3DTexture9**](/windows/desktop/api) object that uses a specialized pixel format.</span></span> <span data-ttu-id="f09c7-105">Anziché archiviare i componenti di colore rosso, verde e blu, ogni pixel in una mappa Bump archivia i valori delta per l'utente e v (D<sub>U</sub> e d<sub>v</sub>) e talvolta un componente di luminanza, L. Questi valori vengono applicati dal sistema come descritto nell'argomento relativo alle [formule di mapping Bump (Direct3D 9)](bump-mapping-formulas.md) .</span><span class="sxs-lookup"><span data-stu-id="f09c7-105">Rather than storing red, green, and blue color components, each pixel in a bump map stores the delta values for u and v (D<sub>U</sub> and D<sub>V</sub>) and sometimes a luminance component, L. These values are applied by the system as described in the [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md) topic.</span></span>

<span data-ttu-id="f09c7-106">È possibile specificare un formato pixel di mappa a urto impostando il formato su uno dei seguenti elementi: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT X8L8V8U8, \_ D3DFMT \_ Q8W8V8U8 o D3DFMT V16U16 \_ .</span><span class="sxs-lookup"><span data-stu-id="f09c7-106">You can specify a bump map pixel format by setting the format to one of the following: D3DFMT\_CxV8U8, D3DFMT\_V8U8, D3DFMT\_L6V5U5, D3DFMT\_X8L8V8U8, D3DFMT\_Q8W8V8U8, or D3DFMT\_V16U16.</span></span> <span data-ttu-id="f09c7-107">Per le descrizioni, vedere [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="f09c7-107">For descriptions, see [D3DFORMAT](d3dformat.md).</span></span>

<span data-ttu-id="f09c7-108">I componenti D<sub>U</sub> e d<sub>V</sub> di un pixel sono valori con segno compreso tra-1,0 e + 1,0.</span><span class="sxs-lookup"><span data-stu-id="f09c7-108">The D<sub>U</sub> and D<sub>V</sub> components of a pixel are signed values that range from - 1.0 to +1.0.</span></span> <span data-ttu-id="f09c7-109">Il componente luminanza, se usato, è un valore Unsigned Integer compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="f09c7-109">The luminance component, when used, is an unsigned integer value that ranges from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="f09c7-110">Prima di selezionare un formato pixel per la mappa Bump, verificare che il formato specifico sia supportato.</span><span class="sxs-lookup"><span data-stu-id="f09c7-110">Before picking a bump map pixel format, check if the particular format is supported.</span></span> <span data-ttu-id="f09c7-111">Per altre informazioni, vedere [uso di bump mapping (Direct3D 9)](using-bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="f09c7-111">For more information, see [Using Bump Mapping (Direct3D 9)](using-bump-mapping.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f09c7-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f09c7-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f09c7-113">Bump mapping</span><span class="sxs-lookup"><span data-stu-id="f09c7-113">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



