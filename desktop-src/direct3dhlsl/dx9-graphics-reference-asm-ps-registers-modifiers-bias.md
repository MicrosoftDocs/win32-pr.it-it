---
title: Bias del registro di origine
description: Sottrarre 0,5 da tutti i componenti.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955841"
---
# <a name="source-register-bias"></a>Bias del registro di origine

Sottrarre 0,5 da tutti i componenti.

## <a name="registers"></a>Registri

Registro di origine. Per altre informazioni sui tipi di registro, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Commenti

Il contenuto del registro non è stato modificato. Il modificatore viene applicato solo ai dati letti dal registro. La distorsione viene applicata a tutti e quattro i canali di colore (RGBA) come indicato di seguito:


```
output = (input - 0.5)
```



L'effetto è quello di modificare i dati compresi nell'intervallo compreso tra 0 e 1 in un intervallo compreso tra-0,5 e 0,5. L'applicazione di distorsioni ai dati all'esterno di questo intervallo può produrre risultati non definiti.

> [!Note]  
> Questo modificatore si escludono a vicenda con il [Registro di origine invertito](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), pertanto non può essere applicato allo stesso registro.

 

Questo modificatore viene utilizzato con le istruzioni aritmetiche.

## <a name="example"></a>Esempio

Questo esempio esegue la stessa operazione di D3DTOP \_ ADDSIGNED in DirectX 6,0 e 7,0 più sintassi di trama.


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




