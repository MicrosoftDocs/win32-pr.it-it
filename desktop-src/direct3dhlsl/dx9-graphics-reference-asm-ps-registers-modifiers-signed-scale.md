---
title: Scalabilità firmata del registro di origine
description: Sottrae 0,5 da ogni canale e ridimensiona il risultato di 2,0. Il nome bx2 deriva da bias e scale-times-two, ovvero l'operazione eseguita.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 161cacbf9f10a36e65f37816970aea5d5d804096151a4ae1ce3f814be918ae08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854601"
---
# <a name="source-register-signed-scaling"></a>Scalabilità firmata del registro di origine

Sottrae 0,5 da ogni canale e ridimensiona il risultato di 2,0. Il nome bx2 deriva da bias e scale-times-two, ovvero l'operazione eseguita.

## <a name="syntax"></a>Sintassi


```
source register_bx2
```



## <a name="register"></a>Registrazione

Registro di origine. Per altre informazioni sui tipi di registro, vedere [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Commenti

Questa operazione viene comunemente usata per espandere i dati da \[ 0.0 a 1.0 \] a \[ -1.0 a 1.0. \] Questo modificatore è progettato per l'uso con le istruzioni aritmetiche. Questo modificatore viene comunemente usato sugli input per l'istruzione dot product ([dp3 - ps](dp3---ps.md)). \_L'uso di bx2 su dati esterni all'intervallo da 0 a 1 può produrre risultati non definiti.

L'operazione di ridimensionamento con segno viene applicata ai dati letti dal registro prima dell'esecuzione dell'istruzione successiva. L'operazione viene applicata a tutti e quattro i canali di colore (RGBA) come segue:


```
y = 2(x - 0.5)
```



Il contenuto del registro non viene modificato. Il modificatore viene applicato solo ai dati letti dal registro.

Questo modificatore si escludono a vicenda [con Source Register Invert,](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) quindi non può essere applicato allo stesso registro.

Informazioni sulla versione:

-   Per ps 1 0 e ps 1 1, è possibile usare bx2 in qualsiasi registro di origine per istruzioni di trama nel \_ \_ formato \_ \_ \_ texm3x2 e \* texm3x3 \* . \_bx2 non può essere usato in nessuna delle altre istruzioni di trama, ad esempio [texreg2ar - ps](texreg2ar---ps.md) o [texreg2gb - ps](texreg2gb---ps.md).
-   Per ps 1 2 e ps 1 3, è possibile usare bx2 in qualsiasi registro di origine per qualsiasi istruzione tex ad eccezione \_ \_ \_ \_ \_ \* di: [texreg2ar - ps](texreg2ar---ps.md), [texreg2gb - ps](texreg2gb---ps.md), [texbem - ps](texbem---ps.md) o [texbeml - ps](texbeml---ps.md).

## <a name="example"></a>Esempio

Questo esempio esegue un esempio di trama, converte i dati nell'intervallo da -1 a +1 e calcola un prodotto punto.


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




