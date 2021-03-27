---
title: Se bool-PS
description: Inizio di un blocco If.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719354"
---
# <a name="if-bool---ps"></a>Se bool-PS

Inizio di un blocco If.

## <a name="syntax"></a>Sintassi



| Se bool |
|---------|



 

Dove:

-   bool è un numero di registro bool (Boolean). Vedere [Registro booleano costante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Se bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Se il registro booleano di origine nell'istruzione If è true, viene eseguito il codice racchiuso dall'istruzione if e il corrispondente [endif-PS](endif---ps.md) o [else-PS](else---ps.md) . In caso contrario, il codice racchiuso da Else-PS... vengono eseguite le istruzioni endif-PS. Questa istruzione usa uno slot di istruzione.

Un blocco if può essere annidato.

Un blocco If non può risiedere in un blocco di ciclo.

Un blocco if può essere seguito da un blocco di istruzioni e/o da un'istruzione [else-PS](else---ps.md) e/o da un'istruzione [endif-PS](endif---ps.md) .

## <a name="example"></a>Esempio

Questa istruzione fornisce il controllo di flusso statico condizionale.


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[else-PS](else---ps.md)
</dt> <dt>

[endif-PS](endif---ps.md)
</dt> </dl>

 

 




