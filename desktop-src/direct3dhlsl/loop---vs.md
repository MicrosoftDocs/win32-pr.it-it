---
title: loop - vs
description: Avviare un ciclo... blocco endloop.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a211014137f35c39a6b89cd16f0e27687b4daafd89841f752312f459531cab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986441"
---
# <a name="loop---vs"></a>loop - vs

Avviare un ciclo... [blocco endloop.](endloop---vs.md)

## <a name="syntax"></a>Sintassi



| ciclo aL, i\# |
|--------------|



 

Dove:

-   aL è il [registro contatori del ciclo](dx9-graphics-reference-asm-vs-registers-loop-counter.md) che contiene il conteggio del ciclo corrente.
-   i \# è un registro di [interi costanti.](dx9-graphics-reference-asm-vs-registers-constant-integer.md) Vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| loop                   |      | x    | x    | x     | x    | x     |



 

-   [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) contiene il conteggio del ciclo corrente e può essere usato per l'indirizzamento relativo in Constant Integer [Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c) o \# Output [Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o ) all'interno del blocco \# di ciclo.
-   i \# .x specifica il conteggio delle iterazioni. L'intervallo valido \[ è 0, 255 \] . Si noti che questa istruzione non incrementa o decrementa il valore di i \# .x.
-   i \# .y specifica il valore iniziale del registro [loop counter register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL). L'intervallo valido \[ è 0, 255 \] . Si noti che questa istruzione non incrementa o decrementa il valore di i \# .y.
-   i \# .z specifica le dimensioni di step/stride. L'intervallo valido \[ è -128, 127. \]
-   i \# .w non viene usato e deve essere impostato su 0.
-   I blocchi di ciclo possono essere annidati. Vedere [Flow limiti di annidamento del controllo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   Quando è annidato, il valore del [registro](dx9-graphics-reference-asm-vs-registers-loop-counter.md) contatori del ciclo (aL) fa riferimento al blocco di ciclo di inclusione immediato.
-   I blocchi di ciclo possono essere completamente all'interno di un blocco if \* o che lo circondano completamente. Non è consentito alcun intervallo.

## <a name="example"></a>Esempio


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




