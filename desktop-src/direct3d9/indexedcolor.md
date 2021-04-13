---
description: È costituito da un parametro di indice e da un colore RGBA e viene usato per definire i colori dei vertici di rete. L'indice definisce il vertice a cui viene applicato il colore.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895cf56efedfa7214bcfa6acafd32ab9324bbe8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341706"
---
# <a name="indexedcolor"></a><span data-ttu-id="3a093-104">IndexedColor</span><span class="sxs-lookup"><span data-stu-id="3a093-104">IndexedColor</span></span>

<span data-ttu-id="3a093-105">È costituito da un parametro di indice e da un colore RGBA e viene usato per definire i colori dei vertici di rete.</span><span class="sxs-lookup"><span data-stu-id="3a093-105">Consists of an index parameter and an RGBA color and is used for defining mesh vertex colors.</span></span> <span data-ttu-id="3a093-106">L'indice definisce il vertice a cui viene applicato il colore.</span><span class="sxs-lookup"><span data-stu-id="3a093-106">The index defines the vertex to which the color is applied.</span></span>

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

<span data-ttu-id="3a093-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="3a093-107">Where:</span></span>

-   <span data-ttu-id="3a093-108">index-un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="3a093-108">index - A DWORD.</span></span> <span data-ttu-id="3a093-109">Vedere la descrizione sopra.</span><span class="sxs-lookup"><span data-stu-id="3a093-109">See the description above.</span></span>
-   <span data-ttu-id="3a093-110">indexColor: modello ColorRGBA.</span><span class="sxs-lookup"><span data-stu-id="3a093-110">indexColor - A ColorRGBA template.</span></span> <span data-ttu-id="3a093-111">Vedere [**ColorRGBA**](colorrgba.md).</span><span class="sxs-lookup"><span data-stu-id="3a093-111">See [**ColorRGBA**](colorrgba.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3a093-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a093-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a093-113">Modelli</span><span class="sxs-lookup"><span data-stu-id="3a093-113">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



