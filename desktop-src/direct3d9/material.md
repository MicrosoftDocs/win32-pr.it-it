---
description: Definisce un colore di materiale di base che può essere applicato a una mesh completa o ai singoli visi della mesh. La potenza è l'esponente speculare del materiale.
ms.assetid: vs|directx_sdk|~\material.htm
title: Materiale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480701"
---
# <a name="material"></a><span data-ttu-id="0f248-104">Materiale</span><span class="sxs-lookup"><span data-stu-id="0f248-104">Material</span></span>

<span data-ttu-id="0f248-105">Definisce un colore di materiale di base che può essere applicato a una mesh completa o ai singoli visi della mesh.</span><span class="sxs-lookup"><span data-stu-id="0f248-105">Defines a basic material color that can be applied to either a complete mesh or a mesh's individual faces.</span></span> <span data-ttu-id="0f248-106">La potenza è l'esponente speculare del materiale.</span><span class="sxs-lookup"><span data-stu-id="0f248-106">The power is the specular exponent of the material.</span></span>

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

<span data-ttu-id="0f248-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="0f248-107">Where:</span></span>

-   <span data-ttu-id="0f248-108">faceColor-colore della faccia.</span><span class="sxs-lookup"><span data-stu-id="0f248-108">faceColor - Face color.</span></span> <span data-ttu-id="0f248-109">Modello ColorRGBA.</span><span class="sxs-lookup"><span data-stu-id="0f248-109">A ColorRGBA template.</span></span> <span data-ttu-id="0f248-110">Vedere [**ColorRGBA**](colorrgba.md).</span><span class="sxs-lookup"><span data-stu-id="0f248-110">See [**ColorRGBA**](colorrgba.md).</span></span>
-   <span data-ttu-id="0f248-111">esponente di colore speculare del materiale di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="0f248-111">power - Material specular color exponent.</span></span>
-   <span data-ttu-id="0f248-112">specularColor-colore speculare materiale.</span><span class="sxs-lookup"><span data-stu-id="0f248-112">specularColor - Material specular color.</span></span> <span data-ttu-id="0f248-113">Modello ColorRGB.</span><span class="sxs-lookup"><span data-stu-id="0f248-113">A ColorRGB template.</span></span> <span data-ttu-id="0f248-114">Vedere [**ColorRGB**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="0f248-114">See [**ColorRGB**](colorrgb.md).</span></span>
-   <span data-ttu-id="0f248-115">emissiveColor-colore emissivo materiale.</span><span class="sxs-lookup"><span data-stu-id="0f248-115">emissiveColor - Material emissive color.</span></span> <span data-ttu-id="0f248-116">Modello ColorRGB.</span><span class="sxs-lookup"><span data-stu-id="0f248-116">A ColorRGB template.</span></span> <span data-ttu-id="0f248-117">Vedere [**ColorRGB**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="0f248-117">See [**ColorRGB**](colorrgb.md).</span></span>

> [!Note]  
> <span data-ttu-id="0f248-118">Il colore di ambiente richiede un componente alfa.</span><span class="sxs-lookup"><span data-stu-id="0f248-118">The ambient color requires an alpha component.</span></span>

 

<span data-ttu-id="0f248-119">[**TextureFilename**](texturefilename.md) è un oggetto dati facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0f248-119">[**TextureFilename**](texturefilename.md) is an optional data object.</span></span> <span data-ttu-id="0f248-120">Se questo oggetto non è presente, il volto è senza trame.</span><span class="sxs-lookup"><span data-stu-id="0f248-120">If this object is not present, the face is untextured.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f248-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f248-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f248-122">Modelli</span><span class="sxs-lookup"><span data-stu-id="0f248-122">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



