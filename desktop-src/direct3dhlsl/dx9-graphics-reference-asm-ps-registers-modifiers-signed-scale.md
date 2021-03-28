---
title: Adattamento con firma del registro di origine
description: Sottrae 0,5 da ogni canale e ridimensiona il risultato per 2,0. Il Nome BX2 deriva da bias e scale-Times-Two, ovvero l'operazione eseguita.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222119"
---
# <a name="source-register-signed-scaling"></a>Adattamento con firma del registro di origine

Sottrae 0,5 da ogni canale e ridimensiona il risultato per 2,0. Il Nome BX2 deriva da bias e scale-Times-Two, ovvero l'operazione eseguita.

## <a name="syntax"></a>Sintassi


```
source register_bx2
```



## <a name="register"></a>Registrazione

Registro di origine. Per altre informazioni sui tipi di registro, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Commenti

Questa operazione viene in genere usata per espandere i dati da \[ 0,0 a 1,0 a \] \[ -1,0 a 1,0 \] . Questo modificatore è progettato per essere utilizzato con le istruzioni aritmetiche. Questo modificatore viene comunemente usato per gli input per l'istruzione del prodotto dot ([DP3-PS](dp3---ps.md)). \_L'utilizzo di BX2 su dati non compresi nell'intervallo compreso tra 0 e 1 può produrre risultati non definiti.

L'operazione di scalabilità con segno viene applicata ai dati letti dal registro prima dell'esecuzione dell'istruzione successiva. L'operazione viene applicata a tutti e quattro i canali di colore (RGBA) come indicato di seguito:


```
y = 2(x - 0.5)
```



Il contenuto del registro non è stato modificato. Il modificatore viene applicato solo ai dati letti dal registro.

Questo modificatore si escludono a vicenda con l' [inversione del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) in modo che non possa essere applicato allo stesso registro.

Informazioni sulla versione:

-   Per PS \_ 1 \_ 0 e PS \_ 1 \_ 1, è possibile usare \_ BX2 in qualsiasi registro di origine per le istruzioni di trama nel formato texm3x2 \* e texm3x3 \* . \_non è possibile usare BX2 in nessuna delle altre istruzioni di trama, ad esempio [texreg2ar-PS](texreg2ar---ps.md) o [texreg2gb-PS](texreg2gb---ps.md).
-   Per PS \_ 1 \_ 2 e PS \_ 1 \_ 3, è possibile usare \_ BX2 in qualsiasi registro di origine per qualsiasi \* istruzione Tex, eccetto: [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [texbem-PS](texbem---ps.md) o [texbeml-PS](texbeml---ps.md).

## <a name="example"></a>Esempio

In questo esempio viene campionata una trama, i dati vengono convertiti nell'intervallo compreso tra-1 e + 1 e viene calcolato un prodotto punto.


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




