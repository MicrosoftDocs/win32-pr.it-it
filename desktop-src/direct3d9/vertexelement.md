---
description: Descrive un singolo elemento vertice in una dichiarazione di vertice.
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: VertexElement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2ecef6cfa8c522532599acef1b83343c64edd2b5eca93fe461d8bf8419ada8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518853"
---
# <a name="vertexelement"></a>VertexElement

Descrive un singolo elemento vertice in una dichiarazione di vertice.

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

-   Tipo: tipo di dati Vertice. Vedere [**D3DDECLTYPE**](./d3ddecltype.md).
-   Metodo : metodo di elaborazione tessellator. Vedere [**D3DDECLMETHOD**](./d3ddeclmethod.md).
-   Utilizzo: uso previsto dei dati dei vertici. Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).
-   UsageIndex: modifica i dati di utilizzo. Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)
</dt> </dl>

 

 
