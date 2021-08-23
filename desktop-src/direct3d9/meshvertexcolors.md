---
description: Specifica i colori dei vertici per una mesh, anziché applicare un materiale per ogni viso o per mesh.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035f8d51ae692b0edd20f7b06b5ab8e756ff73d9cd8265d64700ce5374f9a15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628331"
---
# <a name="meshvertexcolors"></a>MeshVertexColors

Specifica i colori dei vertici per una mesh, anziché applicare un materiale per ogni viso o per mesh.

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

Dove:

-   nVertexColors : numero di colori. Corrisponde al numero di vertici nella mesh.
-   array IndexColor vertexColors \[ nVertexColors \] : matrice di colori indicizzati. Vedere [**IndexedColor**](indexedcolor.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



