---
title: rep - vs
description: Avviare un rappresentante... blocco endrep.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e800f2ef313cd5c9a4fc90d7205502db5532ae24f51ec0f1255d05cc9a589bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853791"
---
# <a name="rep---vs"></a>rep - vs

Avviare un rappresentante... [blocco endrep.](endrep---vs.md)

## <a name="syntax"></a>Sintassi



| rep i\# |
|---------|



 

dove i \# è un registro integer che specifica il conteggio delle ripetizioni nel componente .x. Vedere [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Rappresentante                    |      | x    | x    | x     | x    | x     |



 

-   i \# .x specifica il conteggio delle iterazioni. L'intervallo valido \[ è 0, 255 \] . Si noti che questa istruzione non incrementa o decrementa il valore di i \# .x.
-   i \# .yzw non vengono usati dal blocco repeat.
-   I blocchi di ripetizione possono essere annidati. Vedere [Flow limiti di annidamento del controllo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   I blocchi di ripetizione possono essere completamente all'interno di un blocco if \* o che lo circondano completamente. Non è consentito alcun intervallo.
-   L'uso della stessa i per istruzioni di ripetizione diverse o annidate è un'ottima cosa: ogni ciclo esegue \# l'iterazione in base al conteggio specificato.

## <a name="example"></a>Esempio


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




