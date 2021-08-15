---
title: loop - ps
description: Avvia un ciclo... endloop - ps block.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a08d2954b478bd6afd0c52d517e07a82ba3ee148dd07f839ec7d8787d93c2134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510984"
---
# <a name="loop---ps"></a>loop - ps

Avvia un ciclo... [endloop - ps](endloop---ps.md) block.

## <a name="syntax"></a>Sintassi



| loop aL, i\# |
|--------------|



 

Dove:

-   aL è il [registro dei contatori dei cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) che contiene il conteggio del ciclo corrente.
-   i \# è un registro di integer [costanti.](dx9-graphics-reference-asm-ps-registers-constant-integer.md) Vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| loop                  |      |      |      |      |      |      |       | x    | x     |



 

-   Loop [Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) contiene il numero di cicli corrente e può essere usato per l'indirizzamento relativo in Input Color [Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v ) all'interno del \# blocco loop.
-   i \# .x specifica il conteggio delle iterazioni. L'intervallo valido \[ è 0, 255 \] . Si noti che questa istruzione non incrementa o decrementa il valore di i \# .x.
-   i \# .y specifica il valore iniziale del registro aL [(Loop Counter Register).](dx9-graphics-reference-asm-ps-registers-loop-counter.md) L'intervallo valido \[ è 0, 255 \] . Si noti che questa istruzione non incrementa o decrementa il valore di i \# .y.
-   \#i.z specifica le dimensioni del passaggio/stride. L'intervallo valido è \[ -128, 127 \] .
-   i \# .w non viene usato dal blocco di ciclo e deve essere 0.
-   I blocchi di ciclo possono essere annidati. Vedere [Flow Limitazioni del controllo di accesso](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Se annidato, il valore del registro dei [contatori](dx9-graphics-reference-asm-ps-registers-loop-counter.md) di cicli fa riferimento al blocco di ciclo di inclusione immediato.
-   I blocchi di ciclo possono essere completamente all'interno di un blocco if \* o che lo circondano completamente. Non è consentito alcun intervallo.

## <a name="example"></a>Esempio


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




