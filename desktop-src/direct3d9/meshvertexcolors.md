---
description: Specifica i colori dei vertici per una mesh, anziché applicare un materiale per volto o per mesh.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401136"
---
# <a name="meshvertexcolors"></a>MeshVertexColors

Specifica i colori dei vertici per una mesh, anziché applicare un materiale per volto o per mesh.

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

Dove:

-   nVertexColors: numero di colori. Corrisponde al numero di vertici nella rete.
-   Array IndexColor vertexColors \[ nVertexColors \] -matrice di colori indicizzati. Vedere [**IndexedColor**](indexedcolor.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



