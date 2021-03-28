---
title: Rep-vs
description: Avvia una Rep... blocco endrep.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398228"
---
# <a name="rep---vs"></a>Rep-vs

Avvia una Rep... blocco [endrep](endrep---vs.md) .

## <a name="syntax"></a>Sintassi



| Rep i\# |
|---------|



 

dove i \# è un registro di tipo integer che specifica il numero di ripetizioni nel componente. x. Vedere [registro integer costanti](dx9-graphics-reference-asm-vs-registers-constant-integer.md).

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Rep                    |      | x    | x    | x     | x    | x     |



 

-   i \# . x specifica il numero di iterazioni. L'intervallo valido è \[ 0, 255 \] . Si noti che questa istruzione non incrementa o decrementa il valore di i \# . x.
-   i \# . yzw non vengono utilizzati dal blocco REPEAT.
-   I blocchi di ripetizione possono essere annidati. Vedere [limiti di nidificazione del controllo di flusso](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   I blocchi di ripetizione possono trovarsi completamente all'interno di un \* blocco if o circondarli completamente. Nessun a cavallo consentito.
-   L'uso della stessa i \# per le istruzioni di rep diverse o nidificate è corretto. ogni ciclo viene iterato in base al numero specificato.

## <a name="example"></a>Esempio


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




