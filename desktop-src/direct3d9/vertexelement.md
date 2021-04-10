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
# <a name="vertexelement"></a>VertexElement

Descrive un singolo elemento Vertex in una dichiarazione di vertice.

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

Dove:

-   Tipo: tipo di dati vertex. Vedere [**D3DDECLTYPE**](./d3ddecltype.md).
-   Metodo di elaborazione mosaico. Vedere [**D3DDECLMETHOD**](./d3ddeclmethod.md).
-   Utilizzo previsto per i dati dei vertici. Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).
-   UsageIndex: modifica i dati di utilizzo. Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)
</dt> </dl>

 

 
