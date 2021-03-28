---
title: ciclo-PS
description: Avvia un ciclo... blocco EndLoop-PS.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046092"
---
# <a name="loop---ps"></a>ciclo-PS

Avvia un ciclo... blocco [EndLoop-PS](endloop---ps.md) .

## <a name="syntax"></a>Sintassi



| ciclo aL, i\# |
|--------------|



 

Dove:

-   aL è il [registro del contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) che contiene il numero di cicli corrente.
-   i \# è un [Registro di tipo Integer costante](dx9-graphics-reference-asm-ps-registers-constant-integer.md). Vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| loop                  |      |      |      |      |      |      |       | x    | x     |



 

-   Il [registro del contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) include il numero di cicli corrente e può essere usato per l'indirizzamento relativo nel [Registro colori di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) all'interno del blocco del ciclo.
-   i \# . x specifica il numero di iterazioni. L'intervallo valido è \[ 0, 255 \] . Si noti che questa istruzione non incrementa o decrementa il valore di i \# . x.
-   i \# . y specifica il valore iniziale del registro del [contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al). L'intervallo valido è \[ 0, 255 \] . Si noti che questa istruzione non incrementa o decrementa il valore di i \# . y.
-   i \# . z specifica la dimensione step/stride. L'intervallo valido è \[ -128, 127 \] .
-   i \# . w non viene usato dal blocco del ciclo e deve essere 0.
-   I blocchi di ciclo possono essere annidati. Vedere [limitazioni del controllo di flusso](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Quando nidificato, il valore del [registro del contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) si riferisce al blocco del ciclo di inclusione immediato.
-   I blocchi di ciclo possono trovarsi completamente all'interno di un \* blocco if o circondarli completamente. Nessun a cavallo consentito.

## <a name="example"></a>Esempio


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




