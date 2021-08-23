---
title: Registro colori di input
description: Registro di input pixel shader contenente il colore dei vertici.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fcabc6dcf5043c23be252fe6ac25c99da505e33b7c670c95ee5672b50ddb74bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744631"
---
# <a name="input-color-register"></a>Registro colori di input

Registro di input pixel shader contenente il colore dei vertici.

## <a name="syntax"></a>Sintassi


```
dcl v#.writeMask
```



dove:

-   [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) è un'istruzione di dichiarazione di registro.
-   v è un registro di input \# e è il numero di registro. Il numero di registri consentiti è determinato dalla versione dello shader.
-   writeMask determina quali componenti (fino a quattro) vengono scritti. I componenti validi sono: (x,y,z,w) o (r,g,b,a).

## <a name="remarks"></a>Commenti

I registri colori sono registri di sola lettura. Ogni registro contiene valori RGBA a quattro componenti iterati dai vertici di input. Hanno una precisione inferiore rispetto alla maggior parte dei registri, con 8 bit di dati senza segno nell'intervallo (0, +1). Non è possibile usare più di una istruzione in una singola istruzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registri](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[ps \_ 2 \_ 0 Registri](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[ps \_ 2 \_ x Registri](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[ps \_ 3 \_ 0 Registri](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




