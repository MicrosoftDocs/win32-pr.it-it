---
title: Registro colori di input
description: Registro di input pixel shader che contiene il colore del vertice.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396951"
---
# <a name="input-color-register"></a>Registro colori di input

Registro di input pixel shader che contiene il colore del vertice.

## <a name="syntax"></a>Sintassi


```
dcl v#.writeMask
```



dove:

-   [DCL-(SM2, SM3-PS ASM)](dcl---ps.md) è un'istruzione di dichiarazione Register.
-   v è un registro di input ed \# è il numero di registro. Il numero di registri consentito è determinato dalla versione dello shader.
-   writeMask determina quali componenti (fino a quattro) vengono scritti. I componenti validi sono: (x, y, z, w) o (r, g, b, a).

## <a name="remarks"></a>Commenti

I registri colori sono registri di sola lettura. Ogni registro contiene valori RGBA a quattro componenti iterati dai vertici di input. Hanno una precisione inferiore rispetto alla maggior parte dei registri, con una garanzia di 8 bit di dati non firmati nell'intervallo (0, + 1). Non è possibile usare più di uno in un'unica istruzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 registri PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[\_registri PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[\_registri PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[\_registri PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




