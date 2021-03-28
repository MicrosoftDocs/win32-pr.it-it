---
title: Se prede-vs
description: Inizio di un'se prede-vs... else-vs... endif-vs blocco, con la condizione ricavata dal contenuto del registro predicato.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335476"
---
# <a name="if-pred---vs"></a>Se prede-vs

Inizio di un'se prede-vs... [else-vs](else---vs.md)... [endif-vs](endif---vs.md) blocco, con la condizione ricavata dal contenuto del registro predicato.

## <a name="syntax"></a>Sintassi



| Se \[ ! \] prede. replicateSwizzle |
|-------------------------------|



 

Dove:

-   \[!\] un modificatore facoltativo NOT. Il valore viene modificato nel registro predicato.
-   prede è il registro predicato, P0. Vedere [registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   replicateSwizzle è un singolo componente copiato (o replicato) in tutti i quattro componenti (swizzled). I componenti validi sono: x, y, z, w o r, g, b, a.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Se prede                |      |      | x    | x     | x    | x     |



 

Questa istruzione viene utilizzata per ignorare un blocco di codice, in base a un canale del registro predicato. Each se il \_ blocco prede deve terminare con un'istruzione else o endif.

Tali restrizioni includono:

Se i \_ blocchi di predazione possono essere annidati. Viene conteggiata la profondità di nidificazione dinamica totale insieme a [if \_ comp](if-comp---vs.md) Blocks.

Un blocco If prede non può risiedere in \_ un blocco di ciclo, deve trovarsi completamente al suo interno o racchiuderlo tra loro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




