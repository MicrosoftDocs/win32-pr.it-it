---
description: Descrive un singolo elemento Vertex in una dichiarazione di vertice.
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: VertexElement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 049511c89b335c0da31a9f41344082c3b818fa0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124743"
---
# <a name="vertexelement"></a><span data-ttu-id="b9786-103">VertexElement</span><span class="sxs-lookup"><span data-stu-id="b9786-103">VertexElement</span></span>

<span data-ttu-id="b9786-104">Descrive un singolo elemento Vertex in una dichiarazione di vertice.</span><span class="sxs-lookup"><span data-stu-id="b9786-104">Describes an individual vertex element in a vertex declaration.</span></span>

``` syntax
template VertexElement 
{ 
    < F752461C-1E23-48f6-B9F8-8350850F336F > 
    DWORD Type; 
    DWORD Method; 
    DWORD Usage; 
    DWORD UsageIndex; 
} 
```

<span data-ttu-id="b9786-105">Dove:</span><span class="sxs-lookup"><span data-stu-id="b9786-105">Where:</span></span>

-   <span data-ttu-id="b9786-106">Tipo: tipo di dati vertex.</span><span class="sxs-lookup"><span data-stu-id="b9786-106">Type - Vertex data type.</span></span> <span data-ttu-id="b9786-107">Vedere [**D3DDECLTYPE**](./d3ddecltype.md).</span><span class="sxs-lookup"><span data-stu-id="b9786-107">See [**D3DDECLTYPE**](./d3ddecltype.md).</span></span>
-   <span data-ttu-id="b9786-108">Metodo di elaborazione mosaico.</span><span class="sxs-lookup"><span data-stu-id="b9786-108">Method - Tessellator processing method.</span></span> <span data-ttu-id="b9786-109">Vedere [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="b9786-109">See [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>
-   <span data-ttu-id="b9786-110">Utilizzo previsto per i dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="b9786-110">Usage - Intended use of the vertex data.</span></span> <span data-ttu-id="b9786-111">Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="b9786-111">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>
-   <span data-ttu-id="b9786-112">UsageIndex: modifica i dati di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="b9786-112">UsageIndex - Modifies the usage data.</span></span> <span data-ttu-id="b9786-113">Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="b9786-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b9786-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9786-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9786-115">Modelli</span><span class="sxs-lookup"><span data-stu-id="b9786-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="b9786-116">**D3DVERTEXELEMENT9**</span><span class="sxs-lookup"><span data-stu-id="b9786-116">**D3DVERTEXELEMENT9**</span></span>](d3dvertexelement9.md)
</dt> </dl>

 

 
